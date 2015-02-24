#Crouton

## Backup

### Create a chroot backup using crouton

    sudo edit-chroot -b chrootname 

### Backup splitted in smaller files (190M) of a chroot in a different path

    sudo edit-chroot -b -c /media/removable/FabricioZuardi/ -s 190 trusty

