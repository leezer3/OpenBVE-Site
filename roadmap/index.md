---
layout: page
title: Roadmap
description: "The current roadmap for OpenBVE development"
share: true
---

## Version 1.5

### Implemented Features:

* Added animated bogies to train cars. (This was previously possible with various physics based hacks, but not officially supported)
* Extend a range of variables available via the plugin interface & animated files.
* Port backend libraries to openTK.
* In-game menu and information displays re-written.
* Animated objects may now follow the path of Track 0.
* Package management: Allow developers to create a managed package format, providing an easy installation and metadata for routes and trains. (Largely complete!)

---

## Version 1.6

### Implemented Features:

* Deprecate the extensions.cfg files, in favour of an XML based system allowing much greater flexibility.
* Multiple views (Cab, passenger etc.) available per train.
* Object parsers converted to shared plugins.
* Touch controls available in 2D and 3D panels.

---

## Version 1.7

### Implemented Features:

* Further extend the XML configuration of trains, to allow the creation of custom 'consists'
* Route parser converted to a shared plugin. 
* Train parsers converted to a shared plugin.
* Re-write the main simulation renderer to move away from using openGL intermediate mode.


## Version 1.8

### Implemented Features:

* 64-bit builds, with a proxy to load existing train plugins.
* Add a parser for Mechanik routes.
* OpenGL main menu for systems not supporting WinForms.
* Scratch written BMP decoder.

## Version 1.9

Version 1.9 is currently under development. 

The current focus is on improving and implementing basic operations other than a simple linear world.

### Implemented Features:

* Add Quad-Tree visibility to allow for intersecting routefiles.
* Allow existing routefiles to be driven in the reverse direction.
* Implement basic uncoupling of cars from the player train.
* Scratch written PNG decoder.

### Planned Features:

* Basic coupling of trains.

## Version 1.10

### Planned Features:

* Allow running on other rails.
* Parser for MSTS trains.
* Keyframe based animation. 

## Version 2.0

### Planned Features:
* BVE5 routefile parser.