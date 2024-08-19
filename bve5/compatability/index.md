---
layout: page
title: BVE5 Route Compatability Information
description: "Information on BVE5 Route Compatability"
share: true
---

# BVE5 Route Compatability Information

---


OpenBVE v1.11.0.0 onwards contains an initial implentation of support for the BVE5 routefile format.

This would not have been possible without the hard work of **S520**, and the parser library created by **aiosupersix**.


Please note that while many routes are fully playable this is **not** fully complete, and routes may not appear as the author intended them in some cases.


Unfortunately, creating an independant implementation of a closed-source engine and it's quirks is a difficult task, and with this in mind, we would ask that issues are raised with us, rather than with route authors directly.

We are actively working on these issues, and aim to improve this support in the future, with the help of our community of developers and users.


Whilst BVE5 trains are not currently supported, we would encourage you to try one of the many suitable trains created for BVE4 or OpenBVE as an alternative.


Finally, our thanks must as always go to Mr. Mackoy and Rock_On for the continuing development of BVE itself.


---

## Known Issues / Differences

* Routefiles using ATS-EX are not supported.
* Transparencies are handled differently between BVE5 and OpenBVE.
* Scripted trains do not currently support sounds.
* Scripted trains may behave unexpectedly compared to BVE5 after a jump between stations.
* Dynamically changing the viewing distance is not currently supported.
* Some animation effects may not be supported.
* Some objects may appear misplaced.
* Some objects using the **PutBetween** command may appear distorted.