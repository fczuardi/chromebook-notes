Crouton
=======

Check https://github.com/dnschneid/crouton and https://github.com/dnschneid/crouton/wiki for documentation.

chroot jails
------------

- list available releases with ```sh crouton -r list``` 
- download a release tarbal with ```sh crouton -d -r release -f path/to/release.tar.bz2```
- list available targets with ```sh crouton -t help```
- create a chroot 
    - from a backup or release tarball ```sh crouton -f tarball -t target -t target -T yourCustomTarget -n chrootname``` 
    - or download a distro and create ```sh crouton -r release -t target -t target -T yourCustomTarget -n chrootname``` 

### USB Drive

Use ```-p``` to specify the location upon creation, or ```sudo edit-chroot -m```
to move if it is already created.

To open jails of USB Drive use ```-c``` to specify the chroots dir.

Example:

    # download ubuntu trusty release and create a tarball on the USB Drive
    sudo sh crouton -d -r trusty -f /media/removable/FabricioZuardi/backups/trusty.tar.bz2
    # using the USB Drive tarball as base, create a chroot on the USB Drive with the name trustyx11 and install the target x11
    sudo sh crouton -f /media/removable/FabricioZuardi/backups/trusty.tar.bz2 -t x11 -n trustyx11 -p /media/removable/FabricioZuardi/
    # enter the trustyx11 chroot located at the USB Drive
    sudo enter-chroot -c /media/removable/FabricioZuardi/chroots -n trustyx11    

Backup
------

### Create a chroot backup using crouton

    sudo edit-chroot -b chrootname 

### Backup splitted in smaller files (190M) of a chroot in a different path

    sudo edit-chroot -b -c /media/removable/FabricioZuardi/ -s 190 trusty

### Save on USB

To save a backup in the USB Drive instead of the Downloads folder use ```-f path/to/destinationfolder```:

```sudo edit-chroot -b trustyx11 -c /media/removable/FabricioZuardi/chroots -f /media/removable/FabricioZuardi/backups/```


Shared home folder between multiple chroots
-------------------------------------------

Only paths under ChromeOS ```~/Downloads```, ```/mnt/stateful_partition/crouton/shared```, and ```~/crouton/shared``` can be exposed to inside the jails, you can do this by editing the ```/etc/crouton/shares``` file, the 3 folders aboved can be referenced by the names ```downloads```, ```shared``` and ```encrypted```.

So, if you want to share the home folder of a user from one chroot in an USB Drive to another chroot in the same USB Drive, you have to create a symlink to the folder in one of the 3 directories of ChromeOS, for example, the  ```~/Downloads``` folder.

Example:

on the host:

    sudo ln -s /media/removable/FabricioZuardi/trusty/home/fabricio fabricio
    
on the chroot's ```/etc/crouton/shares```:

    downloads/fabricio /home/fabricio
    
And then, create a new user that will use this shared home folder:

    #create the user
    sudo adduser fabricio
    #set home folder ownership
    sudo chown fabricio:fabricio -R /home/fabricio
    
Logout and then to enter chroot using a different user use the ```-u``` option.

    sudo enter-chroot -c /media/removable/FabricioZuardi/chroots -n trustyx11 -u fabricio

