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

## Building the source:

OpenBVE may either be built from the command line, using MSBuild or XBuild, or using your favorite .Net IDE.

### Command line buld:

For a command line build, you will need either msbuild (.Net) or xbuild (Mono). For msbuild, open a "Visual Studio command prompt", navigate to the OpenBVE folder and type:

```
msbuild OpenBVE\OpenBve.sln /p:Configuration=Release
```

For xbuild, make sure the tool is located in your path and type:

```
xbuild OpenBVE\OpenBve.sln /p:Configuration=Release
```

For an IDE build, you will need either Visual Studio 2013 or higher, MonoDevelop 2.4 or higher. Simply open OpenBve.sln and click "Build".

### Building the developer tools:

The developer tools (Route Viewer, Object Viewer etc.) are stored in the same Git repository as the main program. Please follow the above procedure, choosing which you wish to build.

## Developer documentation:

Developer documentation is also provided as part of the Git repository, and may be found at **Documentation\DeveloperDocumentation.html**