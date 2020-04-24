---
layout: page
title: Source Code
description: "Instructions on how to get the OpenBVE source ode and build the program"
share: true
---

## Getting the source:

The source code for OpenBVE is stored as a standard Git repository, and is hosted by Github:

<http://github.com/leezer3/OpenBVE>

Either clone the Git repository, or download the latest copy using the buttons provided.

## Prerequisites

### Windows

#### When using .NET Framework

- Visual Studio 2017 or later, x86 or x64
- .NET Framework 4.7.2 or later, x86 or x64

#### When using Mono

- Mono 5.20.1 or later, x86 or x64
- NuGet client 2.16 or later

### Linux

- Mono 5.20.1 or later, x86 or x64
- NuGet client 2.16 or later
- OpenAL
- GNU Make
- debhelper (Debian and compatibles only)

#### Debian and compatibles

NOTE: You may need to get Mono from [the Mono project repository](https://www.mono-project.com/download/stable/#download-lin), not the distribution repository.

```
sudo apt install build-essential mono-devel libmono-i18n4.0-all nuget libopenal1 debhelper
```

#### RHEL and compatibles

NOTE: You need to get Mono from [the Mono project repository](https://www.mono-project.com/download/stable/#download-lin), not the distribution repository.

```
sudo dnf install @"Development Tools" mono-devel mono-locale-extras nuget openal-soft
```

#### Reference information

You can install the latest NuGet client using the command below.

```
sudo curl -o /usr/local/lib/nuget.exe https://dist.nuget.org/win-x86-commandline/latest/nuget.exe
echo -e '#!/bin/sh\nexec /usr/bin/mono /usr/local/lib/nuget.exe "$@"' | sudo tee /usr/local/bin/nuget
sudo chmod 755 /usr/local/bin/nuget
```

### Mac

- Mono 5.20.1 or later, x86 only
- NuGet client 2.16 or later
- OpenAL
- GNU Make

## Building

**Note that as NuGet packages are used, the first-time build requires an internet connection.**

### Windows

#### When to use .NET Framework

1. Open the main OpenBVE.sln file with Visual Studio.
2. Build the required project, allowing NuGet to restore the packages as required.

#### When to use Mono

1. Start "Open Mono Command Prompt" from the start menu.
2. Open the main openBVE source directory in this terminal.
3. Restore the packages as required. **nuget restore OpenBVE.sln**
4. Build the solution. **msbuild OpenBVE.sln**

### Mac / Linux

1. Open the main openBVE source directory in the terminal.
2. You may either build using the makefile, which supports the following options:
   - **make** - Restores the NuGet packages only.
   - **make all-release** - Creates a release build.
   - **make all-debug** - Creates a debug build.
   - **make clean-all** - Cleans release and debug builds.
   - **make openbve-release** - Creates a release build without tools.
   - **make openbve-debug** - Creates a debug build without tools.
   - **make debian** - On Debian and compatibles, creates an installable deb package.
   - **make publish** - On Mac, creates an app package.

## Developer documentation:

Developer documentation is also provided as part of the Git repository, and may be found at **Documentation\DeveloperDocumentation.html**