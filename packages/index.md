---
layout: page
title: Creating Packages
description: "Instructions on how to create an addon package for use with the OpenBVE train simulator"
share: true
---

The following set of pages describes the process for creating an addon package for use with **OpenBVE**.

## The Package Manager:

Packages may be created and installed from within the main OpenBVE program, using the **Package Management** tab.

When opening this tab, you will first be presented with a list of the currently installed packages, switchable between *Routes* , *Trains* and *Other* .

<img src="/images/packages/main.jpg" alt="The package list">

The three buttons at the bottom of the page will allow you to install a package, create a new package, or uninstall an existing package respectively.

---

### Creating a Package:

In this example, I'll assume you're packaging the *OS_ATS Test Route* - You'll need to adjust the directories for whichever route or train you wish to package.

After clicking on the **Create Package** button, you will be presented with the following screen:

<img src="/images/packages/create1.jpg" alt="The package creation screen">

Select the *Package Type* as 'route', and that we are creating a new package. A GUID (Globally Unique Identifier) will be automatically assigned to the package.
 
Next, using the add items button, add the following folders:

{% highlight bash %}
OpenBVE Addons Folder
└─── Railway
     ├── Route
     |    └ OS_ATS_Test	# The routefiles are stored in this directory
     ├── Object
     |    └ OS_ATS_Test	# The object files are stored in this directory
     └── Sound
          └ OS_ATS_Test	# The sound files are stored in this directory
{% endhighlight %}

Finally, use the **Save As...** button to select a filename for the newly created package.

Clicking **Proceed** will move you on to the following screen:

<img src="/images/packages/create2.jpg" alt="The package details screen">

Here, you can add metadata to your package, such as the author, version etc.

The image for the package may be changed by clicking on the large image.

Similarly, the website for the package may be changed by clicking on the blue link.

The final step in package creation is adding dependancies and reccomendations- For example, you could set this route to depend on the *OS_ATS Test Trains* , and these will be prompted for on install if they are not already present.

To do this, simply select a package from the list, and press the **Add Dependancy** or **Add Reccomendation** buttons.

A dialog will then popup, allowing you to select the minimum and maximum versions that are required- If these are not met upon install, the user will be prompted to either continute anyway, or abort.

---

### The Package Format:

OpenBVE Packages have been designed as a simple, and easily extensible in future format.

They consist of an archive (Currently only ZIP is supported), containing two metadata files- **package.xml** and **package.png**

A manually created **package.xml** file should conform to the following basic structure:

{% highlight xml %}
<?xml version="1.0" encoding="utf-8"?>
<OpenBVE xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <Package>
    <Name>Example Package</Name>
    <Author>Example Author</Author>
    <GUID>d8c784c2-b453-4054-b86e-b6c27982f966</GUID>
    <PackageType>Route</PackageType>
    <Description>Example Description</Description>
    <PackageVersion>1.2.3.4</PackageVersion>
    <MinimumVersion />
    <MaximumVersion />
  </Package>
</OpenBVE>
{% endhighlight %}

Dependancies may be added using the following structure:

{% highlight xml %}
<?xml version="1.0" encoding="utf-8"?>
<OpenBVE xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <Package>
  <Package>
.....................
	<Dependancies>
		<Package>
			<Name>Example Dependancy</Name>
			<Author>Example Author</Author>
			<GUID>d8c784c2-b478-40ac-b86e-b6c27982f9de</GUID>
			<PackageType>Route</PackageType>
			<Description>Example Description</Description>
			<MinimumVersion>1.0</MinimumVersion>
			<MaximumVersion>2.0</MaximumVersion>
		</Package>	
	</Dependancies>
  </Package>
  </OpenBVE>
{% endhighlight %}

Reccomendations also follow the same format:


{% highlight xml %}
<?xml version="1.0" encoding="utf-8"?>
<OpenBVE xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <Package>
  <Package>
.....................
	<Reccomendations>
		<Package>
			<Name>Example Reccomendation</Name>
			<Author>Example Author</Author>
			<GUID>d8c784c2-b478-40ac-b86e-b6c27982f9de</GUID>
			<PackageType>Route</PackageType>
			<Description>Example Description</Description>
			<MinimumVersion>1.0</MinimumVersion>
			<MaximumVersion>2.0</MaximumVersion>
		</Package>	
	</Reccomendations>
  </Package>
  </OpenBVE>
{% endhighlight %}

It is reccomended that the **package.png** file be a square image of a minimum of 200px X 200px

