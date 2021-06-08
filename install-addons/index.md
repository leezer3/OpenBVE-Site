---
layout: page
title: Installing Addons
description: "Instructions on how to install and play new addons"
share: true
---

# Downloading Addons:

Addons for OpenBVE may be found on many sites around the internet. 

These may either be packaged as archives (.zip .7z and so-on), self-extracting Windows installers (.exe), or as OpenBVE package files.

# Installing Addons:

OpenBVE requires addons to be stored in a specific folder structure, which looks like this:
{% highlight bash %}
OpenBVE Addons Folder
├─── Railway		# The top-level directory for all routes
|    ├── Route		# Route files are in this folder
|    ├── Object		# Object files are in this folder
|    └── Sound		# Sound files are in this folder
└─── Train		# Trains are stored as subdirectories of this folder
{% endhighlight %}

You must first decide where you wish to store your OpenBVE addons, and create this folder structure- You are now ready to install your first addon!

Routes in archives are generally distributed in one of two ways:

1. An archive containing the complete folder structure described above.

2. Three seperate archives, one containing the object files, one containing the sound files, and one containing the route files.

If the archive you have conforms to the first example, then installation is simple- You just need to extract it to the root of your folder structure, and browse to this folder in OpenBVE.

On the other hand, if you have three archives, installation is a little more complex.

Generally speaking, you will need to extract the contents of each archive into the appropriate **_Object_** **_Route_** or **_Sound_** folder, but in some cases you will need to create a further subfolder manually.

Please follow the instructions on the download page of your route.

# Package Files:

OpenBVE also supports the use of *Package Files* 

These are simply an archive containing two metadata files- **_package.xml_** and **_package.png_**

Use the *Package Management* tab of the main OpenBVE application to install these.

They may also be extracted manually into the root OpenBVE addons folder.

# Mechanik Addons:

Recent versions of OpenBVE (nightly builds from 02/06/2021 onwards) also support routes created for the legacy DOS simulator Mechanik.

Each Mechanik addon should be extracted into a dedicated folder, e.g.
{% highlight bash %}
OpenBVE Addons Folder
└─── Mechanik			# The top-level directory for all Mechanik routes
	 ├── First Route	# All files for the first route are in this folder
	 └── Second Route	# All files for the second route are in this folder etc.
{% endhighlight %}

Mechanik routes are always provided as a single complete archive.