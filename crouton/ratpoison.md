Ratpoison (window manager)
==========================

- Small / simple window manager
- a better solution for "just firefox" chroots than firefox directly on top of x11
    - clicking on the toolbar buttons works :)

Workspaces
----------

To enable workspaces and Alt+F1, F2, etc to change add this to the ```.ratpoisonrc``` file:

    exec /usr/bin/rpws init 9 -k