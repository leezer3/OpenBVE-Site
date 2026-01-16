---
layout: page
title: MSTS & OpenRails Train Compatability Information
description: "Information on MSTS & OpenRails Train Compatability"
share: true
---

# MSTS & OpenRails Train Compatability Information

---


OpenBVE v1.12.0.0 onwards contains an initial implentation of support for trains built for MSTS. Passive compatability for OpenRails is also present, but there are no plans to implement any OpenRails features at present.

This feature requires a complete MSTS / OpenRails installation, and trains may be loaded by browsing to the **TRAINS\\Consists** folder in the main menu. A consist may also used in a TrackFollowingObject by using the relative consist file name within the Consists folder, e.g. **scotsman.con**


In summary, the basic features of many basic diesel and electric trains will work reasonably well, including exteriors, animations and cabviews. The modelling for steam traction and the vaccum brake has not been implemented, but these will generally load into the game and be drivable.


Unfortunately, creating an independant implementation of a closed-source engine and it's quirks is a difficult task, and with this in mind, we would ask that issues are raised with us, rather than with authors directly.

We are actively working on these issues, and aim to improve this support in the future, with the help of our community of developers and users.


---

## Working Features
* Basic diesel traction modelling / physics.
* Basic electric traction modelling / physics.
* Cabviews
* Exterior models and animations.
* MSTS FreightAnims
* MSTS adhesion model- the replacement OpenRails adhesion model is **not** supported.
* Basic sounds.
* Steam and diesel funnel / exhaust particle effects.

## Not Currently Implemented
* Steam traction modelling / physics.
* Advanced sounds.
