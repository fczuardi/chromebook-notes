#Crouton

##Install ubuntu trusty with i3

    sudo apt-get install i3
    echo "exec i3" > ~/.xinitrc


## Backup

### Create a chroot backup using crouton

    sudo edit-chroot -b chrootname 

### Break backup into smaller pieces (for cloud uploading, plyio)

    split -b 190M -d -a 3 foo foo
    
See http://unix.stackexchange.com/a/1589

### Chromium browser

    sudo apt-get install chromium-browser

### Firefox 35

See ```crouton/firefox.md```

### Thunar File manager

    sudo apt-get install thunar

### XFCE4-terminal (a better terminal that supports copy/paste)

    sudo apt-get install xfce4-terminal

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
    curl https://raw.githubusercontent.com/creationix/nvm/v0.23.3/install.sh | bash
    nvm
    nvm install iojs
    node --version
