#Crouton

##Install ubuntu trusty with i3

    sudo apt-get install i3
    echo "exec i3" > ~/.xinitrc

### Chromium browser

    sudo apt-get install chromium-browser

### Firefox 35

    sudo apt-get install firefox
    
As with any new firefox installation, the first thing you should do is to fix the ridiculous minimum tab-with default and get rid of the atrocious tab-scroll (aka worst user interface ever invented).
- install this addon https://addons.mozilla.org/en-Us/firefox/addon/custom-tab-width/
    - restart
    - open addons page ```about:addons```
    - set min width to 1px

### Thunar File manager

    sudo apt-get install thunar

### XFCE4-terminal (a better terminal that supports copy/paste)

    sudo apt-get install xfce4-terminal

### Git, Curl

    sudo apt-get install git
    sudo apt-get install curl

### NVM and iojs

    sudo apt-get install build-essential
    sudo apt-get install libssl-dev
    curl https://raw.githubusercontent.com/creationix/nvm/v0.23.3/install.sh | bash
    nvm
    nvm install iojs
    node --version

### Git GUI

    sudo apt-get install git-gui
    git citool