---
layout: page
title: Installing Addons
description: "Instructions on how to install and play new addons"
share: true
---

# Downloading Addons:

Addons for openBVE may be found on many sites around the internet. 

These may either be packaged as archives (.zip .7z and so-on), self-extracting Windows installers (.exe), or as openBVE package files.

# Installing Addons:

openBVE requires addons to be stored in a specific folder structure, which looks like this:
{% highlight bash %}
openBVE Addons Folder
├─── Railway		# The top-level directory for all routes
|    ├── Route		# Route files are in this folder
|    ├── Object		# Object files are in this folder
|    └── Sound		# Sound files are in this folder
└─── Train		# Trains are stored as subdirectories of this folder
{% endhighlight %}

You must first decide where you wish to store your openBVE addons, and create this folder structure- You are now ready to install your first addon!

Routes in archives are generally distributed in one of two ways:

1. An archive containing the complete folder structure described above.

2. Three seperate archives, one containing the object files, one containing the sound files, and one containing the route files.

If the archive you have conforms to the first example, then installation is simple- You just need to extract it to the root of your folder structure, and browse to this folder in openBVE.

On the other hand, if you have three archives, installation is a little more complex.

Generally speaking, you will need to extract the contents of each archive into the appropriate **_Object_** **_Route_** or **_Sound_** folder, but in some cases you will need to create a further subfolder manually.

Please follow the instructions on the download page of your route.

# Package Files:

openBVE also supports the use of *Package Files* 

These are simply an archive containing two metadata files- **_package.xml_** and **_package.png_**

Use the *Package Management* tab of the main openBVE application to install these.

They may also be extracted manually into the root openBVE addons folder.