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

* [Hypno Pack (VRChat)](https://illuminatedvr.gumroad.com/l/hypnopack) V1 (_Required for basic hypnosis effect._)
    * [ScreenSpace_UberShader](https://github.com/Leviant/ScreenSpace_Ubershader) 2.8.1 (_Odd installation, just drag and drop the source code into a new folder `Leviant/ScreenSpace_UberShader`_)
    * This package is only required for a mask texture sprite sheet. It's imported at a ridiculous resolution. Turn that down to improve everyone's VRAM, please.
* [【VRChatアバターギミック】DizzyMaker](https://zerofactory.booth.pm/items/5209239) 1.1.0 (_Required for blackout effect._)
    * [AmplifyScreenSpaceShader](https://vrcmods.com/download/4300) (_Odd package, don't ask me why ZeroFactory did this._)


## Installation

1. Install the packages in [#Dependencies](#dependencies)
2. [Add this package's listing to the VCC.](https://cassidyprather.github.io/avatar-syringe/)
3. Add this package to the project via the VCC.
4. Instantiate `Packages/Virtual Inebriation System/VIS` on the root of the avatar.
5. Override `VIS/Contact Tracker/Tracking Points.Parent Constraint.Sources` with a location on your avatar (e.g. an empty game object with a static offset from your hand).
6. For partial installs: Delete modules without required dependencies:
a. In the prefab override on the avatar
b. From the effects menu
c. From the corresponding layer(s) in the animator controller

## Notes for Use

* View the targeting reticle using the "preview" function.
* When a target is selected, their location is tracked and they get a flag indicating that they have been targeted. This flag is not cleared, even if tracking is lost. It is only cleared by the "reset" function.
* You can select several sequentially. However, only one user may have their location tracked at a time. Keep this in mind for effects that depend on avatar position.
* If multiple users are on top of each other, they will all be set as tracked. Make sure that their "player capsules" (shown via menu) of nearby players don't overlap with the laser, unless you want them to be selected.
* Targeting takes half a second. Make sure the target is in continuous contact with the laser the whole time.

## Conduct

This package contains content that will be disorienting and unpleasant for many users. Please content-tag your avatar appropriately and ask for consent before using the system on anyone.

This package uses multiple redundant materials from separate authors due to dependency resolution. It will increase the draw calls required to draw your avatar, when running, by a lot. Please be mindful of this in large instances.

## Legal

Copyright 2024 Cassidy Prather <pratherea@gmail.com>

Everything in this repository henceforth is licensed under [GPLv3](https://www.gnu.org/licenses/gpl-3.0.html) (See `COPYING`) unless otherwise specified. 

## Credits

* Template files from https://github.com/vrchat-community/template-package ([VRCHAT DISTRO LICENSE FILE](https://github.com/vrchat-community/template-package/blob/d9cf13fe9f56867cbf7315a4dbbf1901bc1537ec/Packages/com.vrchat.core.bootstrap/License.md))
* Icons from https://game-icons.net/ Creative Commons 3.0 BY license.
