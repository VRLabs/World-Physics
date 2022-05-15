# World Physics
  
[![Generic badge](https://img.shields.io/badge/Unity-2019.4.31f1-informational.svg)](https://unity3d.com/unity/whats-new/2019.4.31)
[![Generic badge](https://img.shields.io/badge/SDK-AvatarSDK3-informational.svg)](https://vrchat.com/home/download)
[![Generic badge](https://img.shields.io/badge/License-MIT-informational.svg)](https://github.com/VRLabs/World-Physics/blob/main/LICENSE)
[![Generic badge](https://img.shields.io/github/downloads/VRLabs/World-Physics/total?label=Downloads)](https://github.com/VRLabs/World-Physics/releases/latest)

World Constraint + Physics.

## How it works

This package fixes two problems that break avatar physics in VRChat. First, it fixes a collision bug by keeping mirror-copies of collider components disabled. Second, it uses an animated world fixed joint to prevent incorrect movement over the network with rigidbodies under world constraints. Unity physics is complex and making things work as you intend beyond these fixes is your responsibility.

## Install guide

You must be using the latest [Avatars 3.0 Manager](https://github.com/VRLabs/Avatars-3.0-Manager) version, as it adds "IsMirror" as a default parameter.

[Local Mirror Detection](https://github.com/VRLabs/Local-Mirror-Detection) is required for this package to work. Import the package and merge the FX controller.

Merge the FX controller to your own FX controller, using the [Avatars 3.0 Manager](https://github.com/VRLabs/Avatars-3.0-Manager) tool.
 
"World Physics.prefab" should go to the base of your Unity scene, which will give it base Unity scaling.

Unpack the prefab by right-clicking it.

Place "World Physics" at the base of your avatar.

Remove "World Physics Target" outside of "World Physics" and place it anywhere in your avatar's hierarchy. For the demo, lift the "World Physics Target" position on the Y axis, so there is room for the cube to fall.

## How to use

This package is set up for a physics demo. A cube falls and collides with the world. Use the demo to learn basic avatar physics.

## Downloads

You can grab the latest version of the World Physics in [Releases](https://github.com/VRLabs/World-Physics/releases/latest).

## License

World Physics is available as-is under MIT. For more information see [LICENSE](https://github.com/VRLabs/World-Physics/blob/main/LICENSE).

## Contact us

If you need help, our support channel is on [Discord](https://discord.vrlabs.dev).
