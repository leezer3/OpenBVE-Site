---
layout: page
title: The openBVE Plugin Interface
description: "A description of the functionality available via the openBVE plugin interface"
share: true
---

# Overview

openBVE supports the creation of train plugins in either C# , or as legacy Win32 DLLs.
These may be used to add functionality, and in many cases override the default behaviour of the simulation.
Available uses include:
* Displaying custom indicators in the cab.
* Playing custom sounds.
* Changing the power / brake handles set by the driver.
* Simulating safety equipment such as ATS or ATC.

# Initial Creation

In order to create a train plugin, first choose a programming language (for example C# or Visual Basic.NET) and a suitable development tool (for example MonoDevelop or SharpDevelop). 
Then create a new Class Library and reference OpenBveApi.dll (which comes with openBVE). 
Finally, create a public class that inherits the interface you want to implement (see the API documentation below).

# API Documentation

## The IRuntime Interface for Train Plugins

### Initial plugin load
Upon inital load of your plugin, the following functions are called in order:

 * Load
 * SetVehicleSpecs
 * Initialize
 * SetPower
 * SetBrake
 * SetReverser
 * SetSignal

The following functions are called when an event occurs within the game:

 * SetPower
 * SetBrake
 * SetReverser
 * KeyDown
 * KeyUp
 * HornBlow
 * DoorChange
 * SetSignal
 * SetBeacon
 * PerformAI

The following function is called when the plugin is unloaded:

 * Unload

### Function calls

The following is a list of all function calls along with explanations on their behavior:

{% highlight C# %}
bool Load(LoadProperties properties)
{% endhighlight %}

The method **Load** is called initally to load your plugin. It returns a boolean value, representing whether loading succeeded or failed (In which case your plugin will be unloaded).
It returns an instance of the LoadProperties class, which is used to initialise your plugin within the simulation.

|---------------|---------------------------------------------------------------------------|
|				|	LoadProperties (Class)													|
|---------------|---------------------------------------------------------------------------|
| PluginFolder	| A string representing the absolute on-disk path to the plugin folder.		|
| TrainFolder	| A string representing the absolute on-disk path to the train's folder.	|
| Panel			| An integer array, representing the panel variables returned by this train.|
| PlaySound		| The callback function used for playing sounds								|
| AISupport		| The extent to which the plugin supports the AI (None or basic)			|
| FailureReason	| A string representing the reason why the plugin failed to load.			|
|---------------|---------------------------------------------------------------------------|
{:.mbtablestyle}


|-------------------|-------------------------------------------------------------------------------------------------------------------|
|					|	AISupport (Enum)																								|
|-------------------|-------------------------------------------------------------------------------------------------------------------|
| AISupport.None	| The plugin does not provide an AI implementation for it's functions. Non-player trains will not use this plugin.	|
| AISupport.Basic	| The plugin supplies an AI implementation for it's functions. Non-player trains will use this plugin.				|
|-------------------|-------------------------------------------------------------------------------------------------------------------|
{:.mbtablestyle}

**Notes:**
You should initialize the *properties.Panel* array to any size and with any startup values you need. This array is processed after every call to *Elapse* in order to update custom panel indicators. These may be queried from a panel2.cfg file can query these values with the *ats[i]* variable, while developers of the panel.animated file can query these values with the *pluginState[i]* variable.

-----------------------------------------

{% highlight C# %}
void Unload()
{% endhighlight %}

The method **Unload** is called when your plugin is unloaded by the simulation, and should clean up any files you have open, or handles which you have created.

-----------------------------------------

{% highlight C# %}
void SetVehicleSpecs(VehicleSpecs specs)
{% endhighlight %}

The method **SetVehicleSpecs** is called after **Load** to inform the plugin about the specifications of the current train.

|---------------|-----------------------------------------------------------------------------------------------------------|
|				|	VehicleSpecs (Class)																					|
|---------------|-----------------------------------------------------------------------------------------------------------|
| PowerNotches	| An integer representing the total number of power notches for this train.									|
| BrakeType		| The type of brakes which this train is equipped with.														|
| BrakeNotches	| An integer representing the total number of service brake notches, but **excluding** the emergency brake.	|
| HasHoldBrake	| A boolean value defining whether this train is equipped with a hold brake.								|
| AtsNotch		| The index of the brake notch which corresponds to B1 or LAP												|
| B67Notch		| The index of the brake notch which corresponds to 70% of the available brake notches.						|
| Cars			| The number of cars which this train has.																	|
|---------------|-----------------------------------------------------------------------------------------------------------|
{:.mbtablestyle}

-----------------------------------------

{% highlight C# %}
void Initialize(InitializationModes mode)
{% endhighlight %}

The method **Initialze** is called after **SetVehicleSpecs** and is used to set the mode for the safety system to start in.

|---------------|-----------------------------------------------------------------------------------------------------------|
|				|	InitializationModes (Enum)																				|
|---------------|-----------------------------------------------------------------------------------------------------------|
| OnService		| The train starts with the service brakes applied. The safety system should be enabled.					|
| OnEmergency	| The train starts with the emergency brakes applied. The safety system should be enabled.					|
| OffEmergency	| The train starts with the emergency brakes applied. The safety system should be disabled.					|
|---------------|-----------------------------------------------------------------------------------------------------------|
{:.mbtablestyle}

**Notes:**
The initialization mode may be set in CSV/RW routes via the *Route.Change* command. 
Please note that any value between -2147483648 and 2147483647 can be conveyed to the plugin - the enumeration members are simply meant to standardize the meanings of the initialization modes.

