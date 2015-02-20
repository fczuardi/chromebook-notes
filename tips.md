Tips
====

Learn keyboard shortcuts
------------------------

To display all keyboard shortcuts on screen just type:

    ctrl+alt+/

Crosh terminal (for ssh)
------------------------

    ctrl+alt+t

(not only ssh, but other simple stuff like ping and top, see http://www.howtogeek.com/170648/10-commands-included-in-chrome-oss-hidden-crosh-shell/ )

### SSH with password

 - Regular crosh can do it.

### SSH with keypairs

#### Downloading a private key generated elsewhere and using crosh
 - Crosh can do it if you copy a private key to either ```/media``` or ```/home/chronos/user``` folder
    - see http://kaleb.horns.by/comp/os/chrome/ssh-keys/
 - Crosh or chromeOS does not have the ability to generate one however, there is no ssh-keygen and will propably never have see https://code.google.com/p/chromium/issues/detail?id=194063
    - "crotch is a crutch and is not intended to be in the product long-term"

#### Using a NaCl ssh App

- Install [Secure Shell][secureshell] app
- 

[secureshell]: https://chrome.google.com/webstore/detail/secure-s