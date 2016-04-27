---
layout: page
title: Playing openBVE
description: "Instructions on how to install and play new addons"
share: true
---

# Japanese Signals and Signs

Some routes make use of Japanese signals and signs which are provided as part of openBVE. These signals and signs are explained on the following page.

---

## 1. Basic Signalling

<img src="/images/driving_signal.png" alt="A Japanese Signal">

A basic Japanese signal may contain up to six signal aspects. These aspects include:

|-----------------------------------------------------------------------|-------------------------------|
| Aspect																| Meaning						|
|-----------------------------------------------------------------------|-------------------------------|
|<font color="red">Red</font> 											| Stop							|
|<font color="yellow">Yellow- Yellow</font>								| Speed Restriction (25km/h)	|
|<font color="yellow">Yellow</font>										| Caution (45- 55km/h)			|
|<font color="yellow">Yellow</font> <font color="green">Green</font>	| Reduced Speed (65- 85km/h)    |
|<font color="green">Green</font>										| Proceed (45- 55km/h)			|
|<font color="green">Green Green</font>									| High-Speed Proceed (Unlimited)|
|-----------------------------------------------------------------------|-------------------------------|

The exact signal limits will depend on the particular route used.

**Note:** Route speed limits must be follwed independantly to the signal speed limits, with the lower value taking precedence.

---

## 2. Route Speed Limits

<img src="/images/driving_sign_1.jpg" alt="A Japanese Speed Limit Sign">

This sign updates the route speed, expressed as a value in km/h.

* If the new route speed limit is lower than the old one, the new route speed limits takes effect immediately upon passing the speed post with the front of the train. 

* If the new route speed limit is higher than the old one, the whole train must have passed the sign first before the new route speed limit takes effect. 

<img src="/images/driving_sign_2.jpg" alt="A Japanese Unlimited Speed Sign">

This updates the route speed limit to unlimited speed. 

* The whole train must have passed the sign first before the unlimited speed takes effect.

<img src="/images/driving_sign_3.jpg" alt="A Japanese Station Stop Point Sign">

This is a station stop point. 

* Stop in a way as for the front of the train to line up with the stop post. 

---

## 3. ATS-SN

ATS-SN (Automatic Train Stop - SN) is a Japanese safety system intended to prevent the train from passing a red signal by applying the emergency brake if the driver does not acknowledge alarms in time. 

<img src="/images/driving_tr_0.jpg" alt="A Japanese ATS-SN Transponder">

About 600 meters from a signal, an S-type transponder (white box) is placed that raises an alarm in the cab if the associated signal is red. 

1. This alarm has to be acknowledged within 5 seconds, or otherwise, an emergency brake application will be performed. 

2. In order to acknowledge the alarm, you need to cut off power and apply at least brake notch _B1_ (or _SRV_ with automatic air brakes), then press the **SECURITY_S (space)** key. 

3. The alarm will now go off and is replaced with a chime- This chime is intended to remind you that the upcoming signal is red and should not be canceled until you know otherwise. 

4. In order to cancel the chime, press the **SECURITY_A1 (insert)** key. 


About 20 meters from a signal, an SN-type transponder (green box) is sometimes placed. 

<img src="/images/driving_tr_1.jpg" alt="A Japanese ATS-SN Transponder">

* If the associated signal is red, the SN-type transponder directly forces an emergency brake application. 


After stop points, an accidental departure transponder (red box) is sometimes placed. 

<img src="/images/driving_tr_2.jpg" alt="A Japanese ATS-SN Transponder">

* If the associated signal is red, this transponder directly forces an emergency brake application. 

* This transponder also triggers if ATS-P is used.

Once an emergency brake application is performed, you have to reset the safety system. Do so by cutting power, applying the emergency brakes, setting the reverser to neutral, then pressing the **SECURITY_B1 (Home)** key.

* You can turn on the safety systems by pressing the **SECURITY_D (2)** key, and off by pressing the **SECURITY_E (3)** key.


Trains equipped with ATS-SN include these indicators in the bottom-right corner of the screen: 

|-----------|-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| Indicator | Meaning																																					|
|-----------|-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| ATS		| This is lit <font color="orange">orange</font> if ATS-SN is currently active.																				|
| ATS RUN	| This is lit <font color="red">red</font> when an alarm is active, or flashes <font color="red">Red</font> if an emergency brake application is performed.	|
|-----------|-----------------------------------------------------------------------------------------------------------------------------------------------------------|

---

## 4. ATS-P

ATS-P (Automatic Train stop - Pattern) is a Japanese safety system intended to prevent a train from passing a red signal by continuously calculating a brake curve and ensuring that the train does not exceed the calculated speed limit.

ATS-P is used along with ATS-SN. You can turn on the safety systems by pressing the **SECURITY_D (2)** key, and off by pressing the **SECURITY_E (3)** key. 

<img src="/images/driving_tr_3.jpg" alt="A Japanese ATS-P Transponder">

On several locations in front of a signal, pattern renewal transponders (white boxes) are placed. The farthest one is usually about 600 meters away from the signal.

* If not already active, passing such a transponder usually activates ATS-P. 

* If the associated signal is red, ATS-P calculates a brake curve and ensures that the train travels below the calculated speed limit. 

* There are no alarms that need to be acknowledged. If the train travels too fast, ATS-P brakes the train until below the calculated speed limit. 

* If you are too close to the signal, the allowed speed limit will become zero and you need to cancel the brake application manually. 

<img src="/images/driving_tr_4.jpg" alt="A Japanese ATS-P Transponder">

About 25 to 30 meters in front of a signal, an immediate stop transponder (yellow box) is usually placed.

* If the associated signal is red, passing the transponder will trigger the service brakes immediately. 

* In order to release the brake application, cut off power, move the reverser to neutral, apply full service brakes, then press the **SECURITY_B1 (home)** key. The brake application will now be released. 

* Alternatively, you can also acquire a brake release for 60 seconds by pressing the **SECURITY_B2 (end)** key. This is usually only done as an override mechanism to get a train approach a red signal more closely or to even pass the red signal, without triggering further brake applications. 

 Trains equipped with ATS-P include these indicators in the bottom-right corner of the screen:
 
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Indicator		| Meaning																																			|
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| P POWER 		| This is lit <font color="green">green</font> when ATS-P is currently active or can be switched to if ATS-SN is currently active.                  |
| PTN APPROACH 	| This is lit <font color="orange">orange</font> when the train exceeds the calculated speed limit.													|
| BRAKE RELEASE | This is lit <font color="orange">orange</font> when a brake release was acquired for 60 seconds.													|
| BRAKE APPLY 	| This is lit <font color="orange">orange</font> when the services brakes are applied by ATS-P.														|
| ATS-P 		| This is lit <font color="green">green</font> when ATS-P is currently active (turned on).															|
| FAILURE 		| This is lit <font color="red">red</font> whenever a failure occurs in the ATS-P system, and also briefly upon initialization of the safety system.|
|---------------|---------------------------------------------------------------------------------------------------------------------------------------------------|

---

## 5. ATC

ATC (automatic train control) is a Japanese safety system which replaces track-side signals by an in-cab signalling system. 

The system receives the location of the preceding train and can automatically determine the appropriate speed limit that needs to be followed. 

The openBVE implementation is a simplified and joined version of the great variety of ATC systems that exist in the real world.

The track must be equipped with ATC before it can be used. 

* In order to activate the system, press the **SECURITY_C2 (page down)** key in order to switch from ATS to ATC. 

* You can switch back to ATS at any time by pressing **SECURITY_C1 (page up)**. 

* You can turn on the safety systems by pressing the **SECURITY_D (2)** key, and off by pressing the **SECURITY_E (3)** key. 

Some trains can automatically switch between ATS and ATC at stations. On others, you will need to do this manually. 

<img src="/images/driving_3.jpg" alt="A Japanese Cab Equipped with ATC">

In a typical Japanese cab such as this, the in-cab signalling elements are placed around the speedometer and indicate the speed which you are currently allowed to maintain.

In km/h, the speed limits which ATC can apply are as follows:

<img src="/images/illustration_atc.jpg" alt="ATC Speed Limits">

If ATC is currently active, but the track is not equipped with ATC, a special symbol is usually displayed (e.g. a cross), while when ATS is currently active, this is also sometimes highlighted by a special symbol (e.g. ATS).

If the track is not equipped with ATC, an emergency brake application will be performed. If the track is equipped with ATC, but the train exceeds the permitted speed limit, a service brake application will be performed until the train travels below the speed limit. 

Trains equipped with ATC include these indicators in the bottom-right corner of the screen:

|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Indicator		| Meaning																																							|
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ATC 			| This is lit <font color="orange">orange</font> when ATC is currently active (turned on).																			|
| ATC POWER 	| This is lit <font color="orange">orange</font> when then ATC is currently active or when the train can be automatically switched to ATC at stations.				|
| ATC SRV 		| This is lit <font color="orange">orange</font> when a service brake application is performed, usually as a result of exceeding the speed limit.					|
| ATC EMG 		| This is lit <font color="orange">orange</font> when an emergency brake application is performed, usually due to the fact that the track is not equipped with ATC. |
|---------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|