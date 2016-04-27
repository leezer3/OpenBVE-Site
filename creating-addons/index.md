---
layout: page
title: Developing Addons
description: "Instructions on how to develop addons for the openBVE train simulator"
share: true
---

The following set of pages describes the process for developing addons for **openBVE**.

## Basic Setup for creating a new addon:

In order to create openBVE addons, you should first download the **openBVE Developer's Tools** :

<a href="http://vps.bvecornwall.co.uk/OpenBVE/Stable/developerTools_1.4.4.0.7z" class="btn btn-info">Developer's Tools 1.4.4 (2016-04-01)</a>

This consists of two major tools- *Object Viewer* and *Route Viewer* , and two minor tools *Train Editor* and *Object Bender*

These should be extracted into your route openBVE folder, as they require data from the main download.

---

### Route Viewer

<img src="/images/routeviewer.jpg" alt="Route Viewer Screenshot">

Route Viewer allows you to render and view a route file. It supports viewing a route, reloading routes, visualising certain non-visual commands (such as *Track.Section* ), and jumping to stations and point of interest.

### Object Viewer

<img src="/images/objectviewer.jpg" alt="Route Viewer Screenshot">

Object Viewer allows you to view the 3D model formats which openBVE supports. It supports viewing multiple objects overlaid, reloading objects, and generates a list of errors in object files. 

---

### Train Editor

<img src="/images/traineditor.jpg" alt="Train Editor Screenshot">

The Train Editor allows the editing of a train.dat file, including modifying properties and values, previewing train acceleration curves, and plotting of train sounds pitch and volume. 

---

### Object Bender

ObjectBender is a utility that helps create curved objects from shorter segments, for example, a 25m-long curved rail from a 5m rail segment.

ObjectBender offers a graphical user interface (GUI) as well as a command line interface (CLI). The GUI allows you to quickly create longer objects, while the command line interface helps with repetitive tasks.

The following is a list of command line arguments. Use these in a batch file to quickly create multiple objects that constantly needs updating(for example, multiple rails for different radiuses from a single rail segment.

Example: 

```
ObjectBender input.csv output.csv /n=25 /s=1 /b=25 /r=600
```

|-----------------------------------|---------------------------------------------------------------------------------------------------|
| Argument							| Meaning																							|
|-----------------------------------|---------------------------------------------------------------------------------------------------|
| /?								| Shows the list of command-line arguments.															|
| InputFile							| The path to the input file. Can be a B3D or CSV file.												|
| OutputFile						| The path to the output file. Will be of the same format as the input file.						|
| /n=Segments						| The number of segments.																			|
| /s=SegmentLength					| The length of each segment in meters.																|
| /b=BlockLength					| The block length in meters. If zero, the object is not rotated for use as a rail object.			|
| /r=Radius							| The radius in meters. Negative values are left, positive ones right. Zero does not create a curve.|
| /g=RailGauge						| The gauge of the rail in millimeters. Only required if cant is applied.							|
| /u=InitialCant					| The cant at the beginning of the object in millimeters.											|
| /v=FinalCant						| The cant at the end of the object in millimeters.													|
| /a								| Appends to the output file instead of overwriting it												|
|-----------------------------------|---------------------------------------------------------------------------------------------------|