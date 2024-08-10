# Virtual Inebriation System

An avatar system for applying status effects to users in VRChat.

This is an advanced, personal system, and I will not be providing any technical support.

## Dependencies

### Packages

VRChat packages must be managed with the [VRChat Creator Companion (VCC)](https://vcc.docs.vrchat.com/).
VRLabs VCC listings are best aquired through [the organization website](https://vrlabs.dev/packages/).

* [FinalIK](https://assetstore.unity.com/packages/tools/animation/final-ik-14290) 2.3 **or** [VRLabs FinalIK Stub (no testing in editor)](https://github.com/VRLabs/Final-IK-Stub) 1.9.3
* [Contact Tracker](https://github.com/VRLabs/Contact-Tracker) 1.4.7
* [Selective Animation](https://github.com/VRLabs/Selective-Animation) 1.0.1
* [VRCFury](https://vrcfury.com/) 1.991.0

### Asset Bundles (Optional)

These dependencies must be "drag and dropped" into the root project's asset directory. They are unmanaged by package managers, and so will not recieve automatic updates.

* [ScreenSpace_UberShader](https://github.com/Leviant/ScreenSpace_Ubershader) 2.8.1 (_Odd installation, just drag and drop the source code into a new folder `Leviant/ScreenSpace_UberShader`)
* [Hypno Pack (VRChat)](https://illuminatedvr.gumroad.com/l/hypnopack) V1 (_Required for basic hypnosis effect._)
** This package is required for a mask texture sprite sheet. It's imported at a ridiculous resolution. Turn that down to improve everyone's VRAM, please.
* [【VRChatアバターギミック】DizzyMaker](https://zerofactory.booth.pm/items/5209239) 1.1.0 (_Required for blackout effect._)

## Installation

1. Install the packages in [#Dependencies](#dependencies)
2. [Add this package's listing to the VCC.](https://cassidyprather.github.io/avatar-syringe/)
3. Add this package to the project via the VCC.
4. Instantiate `Packages/Virtual Inebriation System/VIS` on the root of the avatar.
5. Override `VIS/Contact Tracker/Tracking Points.Parent Constraint.Sources` with a location on your avatar (e.g. an empty game object with a static offset from your hand).
6. Delete modules without required dependencies in the prefab override on the avatar.

## Conduct

This package contains content that will be disorienting and unpleasant for many users. Please content-tag your avatar appropriately and ask for consent before using the system on anyone.

## Legal

Copyright 2024 Cassidy Prather <pratherea@gmail.com>

Everything in this repository henceforth is licensed under [GPLv3](https://www.gnu.org/licenses/gpl-3.0.html) (See `COPYING`) unless otherwise specified. 

## Credits

* Template files from https://github.com/vrchat-community/template-package ([VRCHAT DISTRO LICENSE FILE](https://github.com/vrchat-community/template-package/blob/d9cf13fe9f56867cbf7315a4dbbf1901bc1537ec/Packages/com.vrchat.core.bootstrap/License.md))
* Icons from https://game-icons.net/ Creative Commons 3.0 BY license.
