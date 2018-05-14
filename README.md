st - simple terminal
--------------------
st is a simple terminal emulator for X which sucks less.

Version 0.8.1


Applied (official) patches
------------------------
The following patches have been applied, and fixed to co-exist

1. Scrollback support:
    - st-scrollback-0.8.diff
    - st-scrollback-mouse-0.8.diff

3. Align line vertically:
    - st-vertcenter-20180320-6ac8c8a.diff

4. Disable lighting up bold colors (to prepare for solarized patch):
    - st-no_bold_colors-0.8.1diff


Personal additions
------------------
- Default font is terminus at 14pt
- Modified solarized colorscheme for black background and other small tweaks
- Disabled -lrt in config.mk for compile on OpenBSD
- custom patch based on st-solarized-both-0.8.1diff
- switch theme with alt-tab


Requirements
------------
In order to build st you need the Xlib header files.


Installation
------------
Edit config.mk to match your local setup (st is installed into
the /usr/local namespace by default).

Afterwards enter the following command to build and install st (if
necessary as root):

    make clean install


Running st
----------
If you did not install st with make clean install, you must compile
the st terminfo entry with the following command:

    tic -sx st.info

See the man page for additional details.

Credits
-------
Based on Aurélien APTEL <aurelien dot aptel at gmail dot com> bt source code.

