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

Development
-----------

### Git

    sudo apt-get install git
    git config --global user.email "email@example.com"
    git config --global user.name "Your Name"

### Git GUI

    sudo apt-get install git-gui
    git gui

### Curl

    sudo apt-get install curl

### NVM and iojs

    sudo apt-get install build-essential
    sudo apt-get install libssl-dev
    sudo apt-get install curl
    curl https://raw.githubusercontent.com/creationix/nvm/v0.23.3/install.sh | bash
    source ~/.bashrc
    nvm
    nvm install iojs
    node --version
