Tips
====

Learn keyboard shortcuts
------------------------

To display all keyboard shortcuts on screen just type:

    ctrl+alt+/

Crosh terminal (for ssh)
------------------------

    ctrl+alt+t

(not only ssh, but other simple stuff like [ping and top][croshcommands] )

Opening crosh with a keyboard brings it inside a chrome browser tab, and ctrl+w will close it, if you want to open it in it's own window, [there is an app for that][croshwindow]

SSH
---

The regular crosh terminal have an ssh command, and there is also a [NaCl ssh App][secureshell] in the chrome store.

### SSH with password

 - Regular crosh can do it.

### SSH with keypairs

#### Downloading a private key generated elsewhere and using crosh
 - Crosh can do it if you copy a private key to either ```/media``` or ```/home/chronos/user``` folder
    - see http://kaleb.horns.by/comp/os/chrome/ssh-keys/
 - Crosh or chromeOS does not have the ability to generate one however, there is no ssh-keygen and will propably never have see https://code.google.com/p/chromium/issues/detail?id=194063
    - "crotch is a crutch and is not intended to be in the product long-term"
 - if you trust [this guy][travis] and don't have another machine to generate keys, you can risk using [this online tool][onlinekeygen] (probably not a good idea).

[travis]: http://travistidwell.com/blog/2013/09/06/an-online-rsa-public-and-private-key-generator/
[croshcommands]: http://www.howtogeek.com/170648/10-commands-included-in-chrome-oss-hidden-crosh-shell/
[croshwindow]: https://chrome.google.com/webstore/detail/crosh-window/nhbmpbdladcchdhkemlojfjdknjadhmh?hl=en
[onlinekeygen]: http://travistidwell.com/jsencrypt/demo/
[secureshell]: https://chrome.google.com/webstore/detail/secure-s