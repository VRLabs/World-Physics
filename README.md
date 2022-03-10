<div>
  <h1>World Physics</h1>
  <p>
     World Constraint + Physics.
  </p>
  <a href="https://github.com/VRLabs/World-Physics/releases/latest">
    <img src="https://img.shields.io/badge/Unity-2019.4-green.svg?style=flat-square">
  </a>
  <br />
</div>

## How it works

This package fixes two problems that break avatar physics in VRChat. First, it fixes a collision bug by keeping mirror-copies of collider components disabled. Second, it uses an animated world constraint to prevent incorrect movement over the network with rigidbodies in world space. Unity physics is complex and making things work as you intend beyond these fixes is your responsibility.

## Install guide

Merge the FX and Gesture controllers to your own FX and Gesture controllers, using the [Avatars 3.0 Manager](https://github.com/VRLabs/Avatars-3.0-Manager) tool.
 
"World Physics.prefab" should go to the base of your Unity scene, which will give it base Unity scaling.

Unpack the prefab by right-clicking it.

Place "World Physics" at the base of your avatar.

Remove "Rigidbody Target" outside of "World Physics" and place it anywhere in your avatar's hierarchy. For the demo, lift the Rigidbody Target position on the Y axis, so there is room for the cube to fall.

Use the [Layer Weight Tool](https://github.com/VRLabs/Layer-Weight-Tool/). Open VRLabs from the menu bar. Click "Apply Weight Controls".

## How to use

Testing in Unity requires the [3.0 emulator by Lyuma](https://github.com/lyuma/Av3Emulator).

"Rigidbody" and "Collider" are set up for a physics demo. A cube falls and collides with the world.

Select the World Physics object. The animator component references "Fix Colliders.controller", which plays "Fix Colliders.anim" outside of the local mirror.

Edit "Fix Colliders.anim" to enable collider components used for physics. Collider components being used for physics should be off by default, or they'll be on in the mirror and break collision. Make sure you're animating using paths that properly reference children of the World Physics object. Your paths should not have the "World Physics" name in them.

Animate the collider game object active or inactive if you need to handle the collider in your FX layer. Don't animate the collider component or you may undo the fix.

Pay attention to the way the "Physics Demo" layer is split by IsLocal. The "Is Kinematic" rigidbody setting on the World Physics object should be on locally, and off remotely.

The "Is Kinematic" property doesn't seem to persist, so you must constantly animate this property if you want it to stay the way you animated it.

Using gravity seems to have some minor local-only issues on the Y axis and with culling. Not really a big deal, hard to even notice. Doesn't happen if you don't use gravity on a given rigidbody.

## Downloads

You can grab the latest version of the World Physics in [Releases](https://github.com/VRLabs/World-Physics/releases/latest).

## License

World Physics is available as-is under MIT. For more information see [LICENSE](https://github.com/VRLabs/World-Physics/blob/main/LICENSE).

## Contact us

If you need help, our support channel is on [Discord](https://discord.vrlabs.dev).
