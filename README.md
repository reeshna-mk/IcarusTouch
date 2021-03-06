IcarusTouch
==============

(former named *TouchContinuum*)

![blue](http://a6.sphotos.ak.fbcdn.net/hphotos-ak-ash4/299067_222700637789286_100001480546056_629480_1690295720_n.jpg?dl=1)__
![hot](http://a5.sphotos.ak.fbcdn.net/hphotos-ak-snc7/311805_222700691122614_100001480546056_629484_266904590_n.jpg?dl=1)

![cold](http://a8.sphotos.ak.fbcdn.net/hphotos-ak-ash4/303941_222700671122616_100001480546056_629483_2090968175_n.jpg?dl=1)__
![warm](http://a4.sphotos.ak.fbcdn.net/hphotos-ak-snc7/316868_222700654455951_100001480546056_629481_1168308683_n.jpg?dl=1)


![appearance panel](http://a3.sphotos.ak.fbcdn.net/hphotos-ak-snc7/302045_222700711122612_100001480546056_629485_1168915418_n.jpg?dl=1)__
![settings panel](http://a1.sphotos.ak.fbcdn.net/hphotos-ak-snc7/297911_222700724455944_100001480546056_629486_1335669365_n.jpg?dl=1)

![midi settings](http://a7.sphotos.ak.fbcdn.net/hphotos-ak-ash4/309539_222700734455943_100001480546056_629487_810765182_n.jpg?dl=1)__
![file settings](http://a8.sphotos.ak.fbcdn.net/hphotos-ak-ash4/310184_222700747789275_100001480546056_629488_1421361828_n.jpg?dl=1)

READ THIS FIRST
---------------

This application runs on the open source multitouch framework <Kivy>.
For informations on the Kivy framework, please refer to http://kivy.org

To install Kivy on your computer, see the Kivy documentation at
http://kivy.org/docs/installation/installation.html

...or, for windows, read the section "Getting Started under Windows" which is a
heavily summarized version of the above one.


About IcarusTouch
--------------------

This application is a multitouch instrument in form of a virtual piano keyboard.
It is able to handle the tone pitch in a "continuous" manner. Means, you can
drag a pressed note up and down the keyboard to change its pitch as well as
back and forward to apply some modulation on the tone.

The application is made in honor of the great but also costly Haaken Continuum
Fingerboard.

NOTE: This application only features a MIDI output to connect to a hardware or
software synthesizer. **There are no internal sounds at the moment!**


Getting Started under Windows
-----------------------------

After you downloaded the latest portable package of kivy on
http://kivy.org/#downloads, you have to unzip the package. Then drag the main.py
file of this application (in the "src" folder) over the unzipped file "kivy.bat"
to launch the python file with kivy.


Instruction Manual
------------------

### General:

When you launch the application, first of all, you see a keyboard in the middle.
On the bottom, you have four buttons. The rest of the screen consists of the
background image.


### Scrolling:

Apart from playing the keyboard (which I assume to not have to explain), it's
possible to scroll the keyboard "focus" up and down. You can do so by touching
the background and dragging left or right. The whole keyboard image is five
octaves long. You can also keep up playing while scrolling (but pay attention:
if you're holding a key and scroll up or down, the tone is moving with the new
keyboard position!).

### Buttons: Pitch Lock

The first button from the left indicates if pitch lock is enabled - pitch lock
means that every note (no matter of just touched or while dragging around) is
rounded straight to the next key under it (thus the scale will be forced to be
chromatic).


### Buttons: Y Axis

The second button from the left indicates whether the y axis on the keyboard is
used to modulate the volume or the aftertouch value over MIDI. If you selected
to modulate the volume, a value from 0 (bottom) to 127 (top) is sent for the
modulation wheel controller (CC#01) by default. You can also change the CC
controller number in the application setup described further down.


### Buttons: Look

The first little button from the left launches the appearance settings panels.
The panel on the left is used to choose the background image. The panel on the
right defines the keyboard image.
The images are all stored as .PNG images in directories named "backgrounds" or
"keyboards". This is also the place where the application will look for images
to preview in the panels. So if you want to use your own image you have to do
the following:

* Keyboard Image:
  * name convention: keyboard_*.PNG
  * size: 3000x468 pixels (containing 5 octaves). If you use other sizes, i
    don't give any warranty for correct image displaying.
  * place it somewhere in the folder called "keyboards".
  * [1] If you like, you can also create a thumbnail image of it so the panel
    loads faster. This one should have a resolution of 1250x195 pixel.

* Background Image:
  * name convention: background_*.PNG
  * size: doesn't matter for ME. It should match your target device resolution.
  * place it somewhere in the folder called "backgrounds".
  * [1] If you like, you can also create a thumbnail image of it so the panel
    loads faster. This one should have a height of about 180 pixel.

[1] If you don't include a thumbnail, the image is loaded on the panel in full
resolution resulting in a remarkable loading time the first time you open the
panels. --> *the thumbnail feature is not yet implemented!*

And remember: the selectable images are being loaded when you launch the app.
So if you want to use your own images, you have to restart the application.


### Buttons: Setup

The second little button from the left launches the built-in kivy settings
panel. It is used to set up all of the application settings you can think of.
It is organized in different sections from which you can choose one in the panel
on the left of the screen.
If you don't know what you're doing, please don't touch the sections "Advanced"
and "Kivy"...
The rest of the settings items are pretty much self-explanatory.

The app stores an INI-file in it's launch directory. So if you screwed up
something, just delete this file, restart the application and all of the
settings are turned back to default.


### MIDI

One or two words concerning the MIDI output: The preferred MIDI output device
can be set in the application settings. If you open the selection list for this
settings item, only the following devices are displayed:

* Output devices
* Devices which are not opened (except for the device opened by IcarusTouch)

If the preferred MIDI device could not be opened because it does not exist, the
software tries to open the systems default MIDI device.


### Hardware Requirements

You can use any of the touch inputs supported by the kivy framework
(http://kivy.org/docs/api-kivy.input.providers.html). You can also use your
mouse to control it if you like to.


Copyright and Contact
---------------------

IcarusTouch Copyright (C) 2011 Cyril Stoller

This program comes with ABSOLUTELY NO WARRANTY. This is free software,
and you are welcome to redistribute it under certain conditions;
see the source code for details.

For comments, suggestions or other messages contact me at:
cyril.stoller@gmail.com


Release Notes
-------------

Release history:

* **V1.0**: *first released version*

