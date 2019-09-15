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

Version 1.7 is currently under development. 
As the object parsers have now been converted to a plugin interface, the next step is to similarly convert the Route and Train parsers.
This will eventually hopefully allow the loading of a much larger range of content from other simulators.

### Planned Features:

* Further extend the XML configuration of trains, to allow the creation of custom 'consists'
* Route parser converted to a shared plugin. 
* Train parsers converted to a shared plugin.

### Work In Progress Features:

* Improve the simulation options available to train developers.
* Re-write the main simulation renderer to move away from using openGL intermediate mode.
* 64-bit builds, with a proxy to load existing train plugins.