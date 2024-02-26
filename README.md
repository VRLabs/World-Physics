<div align="center">

# World Physics

[![Generic badge](https://img.shields.io/github/downloads/VRLabs/World-Physics/total?label=Downloads)](https://github.com/VRLabs/World-Physics/releases/latest)
[![Generic badge](https://img.shields.io/badge/License-MIT-informational.svg)](https://github.com/VRLabs/World-Physics/blob/main/LICENSE)
[![Generic badge](https://img.shields.io/badge/Unity-2019.4.31f1-lightblue.svg)](https://unity3d.com/unity/whats-new/2019.4.31)
[![Generic badge](https://img.shields.io/badge/SDK-AvatarSDK3-lightblue.svg)](https://vrchat.com/home/download)

[![Generic badge](https://img.shields.io/discord/706913824607043605?color=%237289da&label=DISCORD&logo=Discord&style=for-the-badge)](https://discord.vrlabs.dev/)
[![Generic badge](https://img.shields.io/endpoint.svg?url=https%3A%2F%2Fshieldsio-patreon.vercel.app%2Fapi%3Fusername%3Dvrlabs%26type%3Dpatrons&style=for-the-badge)](https://patreon.vrlabs.dev/)

Easy fix for Physics components behaving weirdly in world space

![WorldPhysics](https://github.com/VRLabs/World-Physics/assets/76777936/6c14b351-fd2e-4b22-8873-6fe4633c692a)


### ⬇️ [Download Latest Version](https://github.com/VRLabs/World-Physics/releases/latest)


### 📦 [Add to VRChat Creator Companion](https://vrlabs.dev/packages?package=dev.vrlabs.world-physics)

</div>

## How it works

* By turning off colliders on the mirror clone we can prevent them from colliding with the player.
* By using an animated fixed joint we can prevent incorrect movement of rigidbodies under world constraints for remote players.

## Install guide

https://github.com/VRLabs/World-Physics/assets/76777936/670ed186-a9b0-45af-8f54-a1adb4ec8541

* Merge the Animator Controller ``World Physics FX`` to your own FX Controller, using the [Avatars 3.0 Manager](https://github.com/VRLabs/Avatars-3.0-Manager) tool.
* Drag & drop the ``World Physics`` prefab into the base of your Hierarchy.
* Right click and unpack the prefab, then drag & drop it onto your avatar.
* Expand the prefab hierarchy and find ``World Physics Target``
* Move ``World Physics Target`` outside of ``World Physics`` and place it anywhere in your avatars hierarchy as needed.
  * For the demo, lift the ``World Physics Target`` position on the Y axis, so there is room for the cube to fall.

## How to use

* This package is intended for leaning how these fixes work so you can apply them to your own systems. It is set up for a physics demo where cube falls and collides with the world.
* Unity physics are complex and making things work as you intend beyond these fixes is your responsibility.

## Performance stats

```c++
Colliders:          1
Constraints:        2
FX Animator Layers: 2
Rigidbodies:        2
```

## Hierarchy layout

```html
World Physics
|-Rigidbody
|  |-Collider
|  |-Cube
|-World Physics Target
```

## Contributors

* [lin](https://github.com/oofdesu)

## License

World Physics is available as-is under MIT. For more information see [LICENSE](https://github.com/VRLabs/World-Physics/blob/main/LICENSE).

​

<div align="center">

[<img src="https://github.com/VRLabs/Resources/raw/main/Icons/VRLabs.png" width="50" height="50">](https://vrlabs.dev "VRLabs")
<img src="https://github.com/VRLabs/Resources/raw/main/Icons/Empty.png" width="10">
[<img src="https://github.com/VRLabs/Resources/raw/main/Icons/Discord.png" width="50" height="50">](https://discord.vrlabs.dev/ "VRLabs")
<img src="https://github.com/VRLabs/Resources/raw/main/Icons/Empty.png" width="10">
[<img src="https://github.com/VRLabs/Resources/raw/main/Icons/Patreon.png" width="50" height="50">](https://patreon.vrlabs.dev/ "VRLabs")
<img src="https://github.com/VRLabs/Resources/raw/main/Icons/Empty.png" width="10">
[<img src="https://github.com/VRLabs/Resources/raw/main/Icons/Twitter.png" width="50" height="50">](https://twitter.com/vrlabsdev "VRLabs")

</div>

