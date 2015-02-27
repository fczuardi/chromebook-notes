Linux apps and tools
====================

Browsers
--------

### Chromium browser

Also available as a crouton target: ```-t chromium```

    sudo apt-get install chromium-browser

### Firefox 35

See ```crouton/firefox.md```

Desktop tools
-------------

### Thunar File manager

    sudo apt-get install thunar

### LXTerminal

    sudo apt-get install lxterminal

### killall

    sudo apt-get install psmisc

Development
-----------

### Git

    sudo apt-get install git
    git config --global user.email "email@example.com"
    git config --global user.name "Your Name"

### Git GUI

    sudo apt-get install git-gui
    git gui


### Remember ssh keys passwords

#### with keychain

    sudo apt-get install keychain
    nano ~/.xinitrc
    
http://blog.kylemanna.com/linux/2014/07/10/use-funtoos-keyhain-insetad-of-gnome-keyring/

```
eval $(keychain --eval --quiet)
```    

And use ```keychain ~/.ssh/your_key``` when you want to use it

    
#### with gnome-keyring

    sudo apt-get install gnome-keyring
    nano ~/.xinitrc
    
https://wiki.archlinux.org/index.php/GNOME_Keyring#xinitrc_method

```
eval $(/usr/bin/gnome-keyring-daemon --start --components=pkcs11,secrets,ssh)
export SSH_AUTH_SOCK

```
### Curl

    sudo apt-get install curl

### NVM and iojs

    sudo apt-get install build-essential
    sudo apt-get install libssl-dev
    sudo apt-get install curl
    sudo apt-get install build-essential libssl-dev curl
    curl https://raw.githubusercontent.com/creationix/nvm/v0.23.3/install.sh | bash
    source ~/.bashrc
    nvm
    nvm install iojs
    node --version

### Linux tips

#### find your IP address

    ip addr show

Launching Graphical apps on the host (chromeOS) window manager
---------------------------------------------------------------

About Aura and Ash: 
- http://www.chromium.org/developers/design-documents/aura
- http://www.chromestory.com/2012/04/aura-and-ash-in-chrome-os-what-are-they/
- http://www.slideshare.net/gnomekr/chromium-ui-frameworkshared
- https://code.google.com/p/chromium/issues/detail?id=319629
    - https://code.google.com/p/chromium-wm/


### XEyes (and other x-apps)

    sudo apt-get install x11-apps

### host-x11

Shortcut for setting DISPLAY=':0' and XAUTHORITY='/var/host/XAuthority':

    $ host-x11
    $ host-x11 xterm
    $ host-x11 xeyes

### copy / paste between chromeOS apps and hosted-x11 apps



### Using Linux Window Managers With ChromeOS X11!!

Save space by not installing x11 on the chroot :P

    sudo apt-get install tinywm
    host-x11 tinywm&
    # alt+left_click = move, alt+ right_click = resize
    jobs
    fg 1
    # ctrl+c to kill
    

    sudo apt-get install fluxbox
    host-x11 fluxbox&


    sudo apt-get install i3
    host-x11 i3&
    # victory!
    
    
### the boring / bloated way (use xiwi and the chrome extension)

Another way that allows a chroot x session inside an Ash window in the host (gives you exposê keyboard button support).

- xiwi-app branch https://github.com/dnschneid/crouton/tree/xiwi-app
    - if inside chroot use ```xiwi xterm```
    - can be launched when entering chroot with ```-b xiwi``` and the app
        - see https://github.com/dnschneid/crouton/blob/ca0d8ca11047ad88a0f6c84e7f44d0720d64991e/targets/xiwi#L404
    - uses ratpoison as the window manager with the following keyboard binds: 
        - Ctrl+Alt+Tab, Ctrl+Alt+Shift+Tab, Ctrl+Shif+Escape+Escape shortcuts
        - see https://github.com/dnschneid/crouton/commit/c22ca4591a9cdbb12dc76bff14ad58ff478c6231


