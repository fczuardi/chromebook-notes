Firefox
=======

Ubuntu trusty has the **Firefox 35** on the package manager, and other versions
such as nightly or Developer Edition aren't available for download for the ARM 
(armhf) architecture :(

    sudo apt-get install firefox

Fix the tabscroll ugly and useless UI
-------------------------------------

As with any new firefox installation, the first thing you should do is to fix the ridiculous minimum tab-with default and get rid of the atrocious tab-scroll (aka worst user interface ever invented).
- install this addon https://addons.mozilla.org/en-Us/firefox/addon/custom-tab-width/
    - restart
    - open addons page ```about:addons```
    - set min width to 1px

Then, to remove tabbar clutter, create a folder named ```chrome``` on your Firefox profile folder, and add a ```userChrome.css``` file with the following customization:

```css
.tab-close-button,
.tabbrowser-arrowscrollbox > .scrollbutton-up,
.tabbrowser-arrowscrollbox > .scrollbutton-down,
.tabbrowser-arrowscrollbox > .arrowscrollbox-overflow-start-indicator,
.tabbrowser-arrowscrollbox > .arrowscrollbox-overflow-end-indicator {
    display:none !important;
}
```

