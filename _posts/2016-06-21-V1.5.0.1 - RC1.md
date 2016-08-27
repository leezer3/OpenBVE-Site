---
layout: post
title: openBVE v1.5.0.1 RC6
description: "The first stable release in the 1.5.0 series"
modified: 2016-08-27
tags: [welcome]
categories: [intro]
---

Almost two months after opening this site, it's now time to post the a series of release candidates for the new **1.5.0** stable series of builds.

*Version 1.5.0.1*

**Significant Changes:**

* Graphical/ audio backend ported to openTK.
* Package Managment system added.
* Correctly moving bogies added.
* Various animation variables added.
* Large numbers of bugs fixed. (Probably some new ones too!)
* New in-game map & gradient profile.
* Timetable display options improved.

*RC2:*

* Fix a critical Windows installer bug.

*RC3:*

* Improve error handling when loading the train.dat file
* Fix a crash when attempting to clone a null object.
* Add ~30 additional translatable strings. (Thanks **MarcRiera**!)

*RC4:*

* Selecting package dependancies could crash in some cases.
* It was possible to get the installer stuck in an unresolved state when a version conflict occured.
* The bug report dialog wasn't working properly on Linux due to path issues.
* Package websites missing the **http://** would cause a crash when clicked on.

*RC5:*

* Improved UI on package management. (Button placement etc. - Thanks MarcRiera)
* Fixed various bugs relating to packages with dependancies.
* Improve handling of various situations pertaining to a missing Data folder.
* Fix a crash when creating packages on some versions of OS-X.

*RC6:*

* Added a Recently Used folders list to the route and train browsers.
* Add the animation function *TrackFollowerFunction*
* Add railtypes to the list of available commands for use in a Cycle.
* Fix a crash when creating packages.
* Train packages could under certain circumstances acquire an extra 'Train' folder/
* The route and train lists under the 'Start' screen were not refreshed when installing or removing a package.
* Fix a rare crash encountered when loading a texture failed unexpectedly.

**Note:** 
The inital version of RC 6 contained two critical bugs on non-Windows platforms. These have now been fixed- Please re-download if openBVE fails to launch.
