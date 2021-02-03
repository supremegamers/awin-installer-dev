# Advanced Android-x86 Installer Dev

If you just simply include the installer executable in your ISO root then that should be enough.
The files in the repo are just to help swap the files which are already pre-packed with the installer, you don't have to essentially include these in your ISO if you don't want to change anything. But if you want to use custom icon, grub config, preset name-version and control how the installer should behave then this is for you.

All you need is the `windows` folder from this repo at your ISO root.

Below I will try to explain what each of the files are used for.

### config.ini

It can predefine some of the meta-data and functions the installer is to use as preset instead of the default values.
For example, if you want to sepcify your operating system NAME and VERSION then you can do it in this file.

### logo.ico

By default the installer uses it's own icon for desktop shortcuts unless you put a custom `logo.ico` inside your `ISO/windows` folder.
So basically, when you put your own `logo.ico` inside the `windows` folder, the installer will use that for desktop shortcut instead of it's own.
* Delete this file if you don't wish to change it.

### ascii.art

This is the ascii art which is shown before rebooting thru the desktop shortcut created for your OS by the installer.
By default it uses a ascii art of `Android-x86` unless you put a custom version of yours.
* Delete this file if you don't wish to change it.

### Android-x86-ASG.cfg

If you want to change the grub submenu structure then you can do it over this file.
* Delete this file if you don't wish to change it.

### grub.cfg.footer

This file gets dynamically merged at the bottom of `C:\grub2\grub.cfg`.
If you want to change the structure of that then you may edit it.
* Delete this file if you don't wish to change it.
