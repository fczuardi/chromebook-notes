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
    curl https://raw.githubusercontent.com/creationix/nvm/v0.23.3/install.sh | bash
    source ~/.bashrc
    nvm
    nvm install iojs
    node --version
