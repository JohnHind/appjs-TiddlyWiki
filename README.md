AppJS-TiddlyWiki
================

A plugin for http://tiddlywiki.com/ to support running inside http://appjs.org/. This gives you a wiki that runs inside its
own webkit browser (the browser used on iphone / ipad / android). This is ideal for carrying around with you on a usb-stick
and it lets you take your wiki with you wherever you go!

Quick Download
==============

You can download AppJS with TiddlyWiki containing the AppJS plugin that lets you save changes:

* windows: https://github.com/downloads/sihorton/appjs-TiddlyWiki/appjs-tiddlywiki-win32.zip
* linux-32bit: https://github.com/downloads/sihorton/appjs-TiddlyWiki/appjs-tiddlywiki-linux-ia32.tar.gz
* linux-64bit: https://github.com/downloads/sihorton/appjs-TiddlyWiki/appjs-tiddlywiki-linux-x64.tar.gz
* mac: https://github.com/downloads/sihorton/appjs-TiddlyWiki/appjs-tiddlywiki-darwin-ia32.zip

Plugin
======
The AppJS Plugin is hosted at http://sihorton.tiddlyspace.com/ 


Advantages
----------
* taking the browser with you means it won't break after getting some kind of auto update.
* no complex procedures or permissions dialogs are needed, it is able to save out of the box

Disadvantages
-------------
* it takes extra space (20 meg+)
* not all plugins / functions may work


Developers
==========

Upon startup AppJS adds an allowSave flag together with an externalJsSave() function and externalJsLoad() function. These 
functions allow TiddlyWiki to use the nodejs backend to load and save files. The tiddlywiki code also had to be modified 
where it was checking to make sure that a file:// url was being used.

Search for "AppJS" within the TiddlyWiki code to see what changes have been made.

Currently plugins may break when running within AppJS the main reason for this tends to be checks for the file:// protocol
being used (we don't use that protocol but still support saving).




