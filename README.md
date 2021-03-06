wmcliphist_x64
==============

Fork of wmcliphist (32bits). Some bugs are fixed in this version.

Copying
-------

This program is free software; you can redistribute it and/or modify it
under the terms of the GNU General Public License as published by the
Free Software Foundation; either version 2 of the License, or (at your
option) any later version.


What is it?
-----------

In short, it is clipboard history dockable application for Window Maker
(and maybe AfterStep with some little modifications - not tested).
wmcliphist keeps history of clipboard operations and allows you to put
previously copied items back to clipboard for pasting to other
applications. I wrote wmcliphist because there was no such application
suitable for usage in Window Maker and I was confused to run number of
KDE daemons for Klipper (which was the inspiration).


Features
--------

  * selectable number of items to keep
  * detachable (tear off) menu with clipboard history
  * possibility to lock item (locked items will not be overriden by new
    clipboard operations). To lock item press right mouse button on it.
  * saves history to file on exit (and loads it on start, of course :),
    periodicaly and/or on request
  * can handle binary data
  * configurable hotkey support (pop up menu at mouse cursor position)
  * regular expression driven actions (ignore/submenu/exec)
  * possibility to lock clipboard (new selections will not replace the
    current one and it could not be stored in history too)


Instalation
-----------

wmcliphist requires gtk+ and glib (fully tested only with 1.2.8 and
1.2.10, but probably will work with any 1.2.x version) and foodock
library for writing dockable applications based on gtk+ (included).
Hopefuly you'll only need to run

make all install

to compile and install wmcliphist. Note that you have to be root to
install program to /usr/local/bin (default). If it fails, check, that
you have installed gtk+, gtk+-devel, glib and glib-devel packages, make
and compiler (gcc). If it still fails, try to upgrade to up to date
versions of libraries listed above (see www.gtk.org).
wmcliphist was tested only on Linux (Red Hat Linux 7.2, kernel 2.4.9,
gcc 2.96), but it should compile and run on other un*x systems too.
After installing binary you can create your configuration file in
~/.wmcliphistrc (sample config file wmcliphistrc is included in
distribution archive).

Upgrading

Please note, that upgrade from version 0.1 will delete your old history!
If you are upgrading from version 0.2 to 0.3, move your ~/.wmcliphistrc
to ~/.wmcliphist.data and create new ~/.wmcliphistrc with configuration
(sample config file is included).


Usage
-----

wmcliphist accepts followinf options:

-h         show help
-n <num>   set number of items to keep (default 10)
-c color   set color for locked items (default is red)
-s <size>  choose wmcliphist icon size:
           16 = tiny 16x16 px icon
           30 = icon suitable for 32px dock/slit
           40 = icon suitable for 48px dock/slit
           60 = icon suitable for 64px dock/slit (default)
-i <num>   choose wmcliphist icon antialiasing:
           0 = for mid tones background (default)
           1 = for dark background
           2 = for light background

Example:

/usr/local/bin/wmcliphist -n 15 -c darkgreen

Some of theese options and many others can be set in ~/.wmcliphistrc too.

Left click on icon opens menu with history and right click opens
application menu. Right click on history menu item will lock it.
History menu can be opened at mouse cursor position with configurable
hotkey too.


ToDo
----

  * Maybe some configuration GUI? Who knows...
  * Separated history queues


Credits
-------

Michal Krause <michal (at) krause (dot) cz>
Daniel Richard G. <skunk (at) iskunk (dot) org> (icon set used from version 0.5)
Michael Beattie (new exec action handling in 0.6)
Vadim O. Ustiansky (some improvements in 0.7)


Special thanx
-------------

Alexey Vyskubov, <alexey@pepper.spb.ru>
foodock library

<mdem@chat.ru>
Downloader for X, from which I took inspiration for clipboard
monitoring. BTW, it's great peace of software, try it.


Download
--------

http://linux.nawebu.cz/wmcliphist/


Apology
-------

I'd like to apologize to all English speaking people for mangling of
their mother tongue :)
