---
layout: page
title: Playing openBVE
description: "Instructions on how to install and play new addons"
share: true
---

# A Quick Overview On the Simulation Controls

This page describes the basic driving controls and interfaces. When you are driving a train, the interface you are presented with looks somewhat like this:

<img src="/images/driving_1.jpg" alt="A sample cab-view">

In the following article, the invidual elements of the interface are explained and you are given instructions on how to operate the train. 

**_Please note:_** Controls are given with their name and their default keyboard configuration, e.g. **POWER_INCRASE (Z)**. If you remap the keyboard controls or assign controls to joysticks, work with the names to identify the underlying control.

Additionally, it should be noted that many trains use plugins that provide their own driving mechanisms and security systems. This page mainly depicts the built-in systems. You should, in any case, consult the operational manual of the train (if available) for more specific details.

---

## 1. The Reverser, Power Lever and Brake controls

The most basic controls in the train include the reverser, the power lever, the brake lever and the emergency brakes. 

1. The states of the reverser, power lever and brake lever are depicted in the bottom-left corner of the screen in this order. 

2. The emergency brake is depicted as part of the brake indicator if applied. 

3. If the train uses a combined power/brake handle, the power and brake indicators are merged into a single indicator.


### The Reverser

To change the direction of travel, operate the reverser. There are three states of the reverser: _B_ (Backwards), _N_ (Neutral) and _F_ (Forwards)

Normally, when you start the simulation, you will have to move the reverser into the forward position.

* In order to move the reverser toward the forward position by one notch, press the **REVERSER_FORWARD (F)** key. 

* To move the reverser backward by one notch, press the **REVERSER_BACKWARD (B)** key.

### The Power Lever

The power lever controls how much power is applied to the engines. If the power is cut off, the power indicator will display _N_. If a power notch is selected, the indicator will display anything like _P1_, _P2_, _P3_, and so on. The amount of power notches available depends on the train. Generally, a higher power notch corresponds to higher acceleration. Be aware though that applying too much power can result in wheel-slip, which prevents the train from accelerating altogether.

* In order to increase the power notch on a train with separate power/brake handles, press the **POWER_INCREASE (Z)** key. 

* To decrease the power notch, press the **POWER_DECREASE (A)** key. 

* On a train with a combined power/brake handle, press the **SINGLE_POWER (Z)** key to increase the power notch. 

* To decrease the power notch, press either the **SINGLE_NEUTRAL (A)** or the **SINGLE_BRAKE (Q)** key.

### The Notched Brake Lever

The brake lever controls how much power is applied to the electric brakes, or how much pressure is applied to the physical brakes. If the brakes are cut off, the indicator will display _N_. If a brake notch is selected, the indicator will display anything like _B1_, _B2_, _B3_, and so on. The amount of brake notches depends on the train. Higher brake notches correspond to higher deceleration. Be aware though that applying too much brake can result in wheel-lock, which prevents the train from decelerating altogether.

* In order to increase the brake notch on a train with separate power/brake handles, press the **BRAKE_INCREASE (.)** key. 

* To decrease the brake notch, press the **BRAKE_DECREASE (,)** key. 

* On a train with a combined power/brake handle, press the **SINGLE_BRAKE (Q)** key to increase the brake notch. 

* To decrease the brake notch, press either the **SINGLE_NEUTRAL (A)** or the **SINGLE_POWER (Z)** key.

Some trains are also equipped with a hold brake. The hold brake appears between the _N_ and _B1_ notch and allows the train to hold the speed when driving on a downward slope, meaning it automatically applies the brakes to prevent the train from accelerating. The hold brake does not apply power on an upward slope, though.

### The Automatic Air Brake

Some trains employ an automatic air brake which does not have brake notches but a brake valve that is operated manually. These trains always have separate power/brake handles. The states of this brake valve include _REL (release)_, _LAP (lap)_ and _SRV (service)_. 

* In order to move the valve from _REL_ to _LAP_, or from _LAP_ to _SRV_, press the **BRAKE_INCREASE (.)** key. 

* To move the valve from _SRV_ to _LAP_, or from _LAP_ to _REL_, press the **BRAKE_DECREASE (,)** key.

<img src="/images/driving_2.jpg" alt="A train with an automatic air brake">

In order to operate the automatic air brake, you need to observe the pressure in the brake cylinders. In the above screenshot, the brake cylinder is depicted by the red needle on the right gauge. When the brake valve is set to _REL (release)_, the pressure in the brake cylinder decreases. If at zero, the train does not decelerate any longer. When set to _SRV (service)_, the pressure increases. If at the maximum possible pressure, the train decelerates the strongest. When set to _LAP (lap)_, the pressure is kept at the current level, maintaining the current rate of deceleration.

Please note that with an automatic air brake, the brake valve does not control the brake cylinders directly, and as such, there are noticable delays from changing the valve position to the desired effect.

Additionally, some trains that use the automatic air brake don't include a brake cylinder needle in the cab. However, they may feature a brake pipe needle. The brake pipe is somewhat of an inverse readout: High pressure corresponds to low deceleration, while low pressure corresponds to high deceleration.

### The Emergency Brake

* On a train with separate power/brake handles, the emergency brakes can be applied by pressing the **BRAKE_EMERGENCY (/)** key. 

* With a combined power/brake handle, press the **SINGLE_EMERGENCY (1)** key. 

The emergency brakes, once applied, usually apply a higher level of deceleration than the service brakes.

In order to release the emergency brakes, press the key that corresponds to decreasing the brake notch, e.g. **BRAKE_DECREASE (,)**, **SINGLE_NEUTRAL (A)** or **SINGLE_POWER (Z)**, depending on the train. 

---

## 2. The EB and CONST SPEED systems

 Trains that are equipped with an _EB_ or a _CONST SPEED_ system include a respective indicator in the bottom-right corner of the screen.
 
The _EB_ system is a form of a vigilance device that keeps track of the reverser, power and brake levers. If present in a train and the controls remain unchanged for 60 seconds, an alarm will sound and the EB indicator lights up in <font color="orange">orange</font>. You now have 5 seconds to acknowledge the alarm by pressing the **SECURITY_A2 (delete)** key. Otherwise, an emergency brake application will be performed by ATS-SN. See the section about ATS-SN for further information about what to do.

The _CONST SPEED_ system allows the train to hold its current speed by reducing the power appropriately. It does not prevent the train from accelerating on a downward slope. If present in a train, the device can be switched on and off via the **DEVICE_CONSTSPEED (backspace)** key. If on, the _CONST SPEED_ indicator lights up in <font color="green">green</font>. Before turning the device on, increase the power notch to the desired maximum power. The _CONST SPEED_ device will then select any power setting up to that corresponding to the selected power notch. Usually, you should increase the power notch to maximum when using the _CONST SPEED_ device. 

---

## 3. Operating the Doors

 On some trains, you can manually operate the doors, while on others, the doors are automatic. The state of the doors is depicted by indicators at the bottom-middle of the screen if at least one door is not fully closed.
 
There are two indicators: L (left doors) and R (right doors). The indicators are color-coded to represent the current state. <font color="gray">Gray</font> indicates that the doors are fully closed, <font color="orange">orange</font> that they are neither fully opened nor fully closed, while <font color="green">green</font> or <font color="blue">blue</font> indicate that the doors are fully opened.

If the doors close automatically, the indicator displays <font color="blue">blue</font>, otherwise it will display <font color="green">green</font>, and you will have to close them manually.

If manual operation is possible, open or close the doors by pressing **DOORS_LEFT (F5)** for the left doors, or **DOORS_RIGHT (F6)** for the right doors. 