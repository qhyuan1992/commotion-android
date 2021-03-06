[![alt tag](http://img.shields.io/badge/maintainer-hawkinswnaf-blue.svg)](https://github.com/hawkinswnaf)
Commotion Mesh Tether
====================

Commotion Mesh Tether is a combination of tools to provide OLSR mesh networking
over wifi on an Android phone.  It handles setting up the wifi into ad-hoc
mode, setting up the IP address, and running the olsrd program.

It was originally based on the Barnacle Wifi Tether app.

https://code.commotionwireless.net/projects/commotion-android/

How to build
------------

Prerequisites:
1) Android NDK r4 or above
2) Eclipse and ADT plugin
3) sudo apt-get install bison flex make sed junit4
 
To build native components, run these commands in the root directory of this
project (i.e. /path/to/commotion-android):

 git submodule init
 git submodule update
 make -C external/
 ndk-build
 
To build the Android app, import the existing project into Eclipse and export 
an .apk file.  If you ran the NDK build after already having the project in
Eclipse, you'll need to refresh the project for Eclipse to see the new files.
To do that, right-click on the project, and select "Refresh".
