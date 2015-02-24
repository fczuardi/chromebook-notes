Crouton
=======

chroot jails
------------

- list available releases with ```sh crouton -r list``` 
- download a release tarbal with ```sh crouton -d -r release -f path/to/release.tar.bz2```
- list available targets with ```sh crouton -t help```
- create a chroot 
    - from a backup or release tarball ```sh crouton -f tarball -t target -t target -T yourCustomTarget -n chrootname``` 
    - or download a distro and create ```sh crouton -r release -t target -t target -T yourCustomTarget -n chrootname``` 

Example:

    sudo sh crouton -d -r sid -f /media/removable/FabricioZuardi/backups/sid.tar.bz2
    sudo sh crouton -d -r trusty -f /media/removable/FabricioZuardi/backups/trusty.tar.bz2
    sudo sh crouton -f /media/removable/FabricioZuardi/backups/trusty.tar.bz2 -t x11 -n trustyx11 -p /media/removable/FabricioZuardi/
    
### USB Drive

Use ```-p``` to specify the location upon creation, or ```sudo edit-chroot -m```
to move if it is already created.

To open jails of USB Drive use ```-c``` to specify the chroots dir.

To save a backup in the USB Drive instead of the Downloads folder:

```sudo edit-chroot -f /path/to/folder -b nameofchroot```


Backup
------

### Create a chroot backup using crouton

    sudo edit-chroot -b chrootname 

### Backup splitted in smaller files (190M) of a chroot in a different path

    sudo edit-chroot -b -c /media/removable/FabricioZuardi/ -s 190 trusty

