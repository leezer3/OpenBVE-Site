---
layout: page
title: OpenBVE- Accessibility
description: "Description of accessibility settings for OpenBVE"
share: true
---

# Playing OpenBVE: Acessibility

---

As far as possible, we'd like OpenBVE to be accessible for all players. We include various accessibility helpers to help support this, which are described below:

## Screen Reader Support

OpenBVE uses the <a href="https://github.com/dkager/tolk">TOLK library</a> to provide screen reader support in-game.
This will read all in-game messages, and the in-game menu if a supported screen reader is present on the system.

## Accessibility Hotkeys

Sevral new accessibility hotkeys are available. These will not be set by default on existing installations, and must either be set manually, or the controls reset to default.

* **ACCESSIBILITY_CURRENT_SPEED** - Announces the current speed of the train. Set by default to _SHIFT + CTRL + S_

* **ACCESSIBILITY_NEXT_SIGNAL** - Announces the distance to the next signal, and it's current aspect. Set by default to _SHIFT + CTRL + A_

* **ACCESSIBILITY_NEXT_STATION**- Announces the distance to and name of the next station. Set by default to _SHIFT + CTRL + T_

## Accessibility Helpers

Several optional accessibility helpers are also available. As these may be considered to be potentially disruptive, they must be enabled under **Options ==> Verbosity ==> Accessibility Aids**

They are as follows:

* A message is shown / announced when 500m from the next station.

* A message is shown / announced when 500m from the next signal.

* The stop position overlay is supplemented by an audible tone.

* When the player handle position is changed, the current position is shown / announced.

