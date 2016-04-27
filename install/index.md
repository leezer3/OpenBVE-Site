---
layout: page
title: Installing openBVE
description: "Instructions on how to install the main openBVE program"
share: true
---

# Windows:

<img src="/images/windows.png" alt="Windows Icon">

If you have not already done so, download the latest stable version of openBVE and extract it to a folder of your choice. This folder will be called your openBVE folder from here on. 

First try launching the program, by double-clicking on the main **_openbve.exe_** in the top-level openBVE folder.
In many cases, _Windows Update_ will have already installed the .Net framework for you, and you will need to do nothing.

If however, this is not the case please download the .Net framework Web Installer from Microsoft: 

<a href="http://go.microsoft.com/fwlink/?LinkId=181011" class="btn btn-info">http://go.microsoft.com/fwlink/?LinkId=181011</a>

Follow the instructions in this installer, and then try launching the program again.

---

# Linux:

<img src="/images/linux.png" alt="Windows Icon">

Some Linux distributions provide openBVE as a ready-to-install package. 

In some cases, this version may be behind the most recent stable version. 

### Ubuntu and Debian:
openBVE is part of the main package repositories, and may be installed using the following *apt-get* command:
```apt-get install openbve```


### Arch Linux
openBVE is part of the 'City' unofficial repository.

### Other Distributions:
If you have not already done so, download the latest stable version of openBVE and extract it to a folder of your choice. This folder will be called your openBVE folder from here on. 

You will then need to install the latest version of the Mono framework, using the packages provided by the Mono Project:

<a href="http://www.mono-project.com" class="btn btn-info">http://www.mono-project.com</a>

Alternatively, Mono will usually be available via your distribution's package manager.


### Launching the Program:
openBVE may be launched from a terminal using the command `mono openbve.exe` in the root openBVE folder.
If you installed openBVE using a distribution's packaged version, then an icon will hopefully have been added to your Games menu.

---

# Mac OS-X:

<img src="/images/apple.png" alt="Apple Icon">

If you have not already done so, download the latest stable version of openBVE.

Mount the **_.dmg_** file, and drag openBVE to your applications folder.

Please note that openBVE is an unsigned application, and depending on your security settings may require you to add an exception to OS-X's gatekeeper, as described in this Apple Support document:

<https://support.apple.com/kb/PH18657?locale=en_US>

Double-click on the openBVE application, and it will automatically prompt you to download and install the Mono framework if required.