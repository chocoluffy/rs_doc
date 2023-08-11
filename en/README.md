# ReboSharp API

If you have any questions, feel free to join our [Discord server](https://discord.gg/kFs7h7vtJJ) and ask in the #SDK channel. We're happy to help clarify any part of the documentation or API usage.

## SDK Installation
1. Drag the package into the project and click install; an installer will pop up. In the installer, click on Install Reborn SDK.
<div style="display: flex;">
  <div><img src="https://raw.githubusercontent.com/chocoluffy/rs_doc/aab7f8b4de8713792f214e19fa1a8f3d9b845202/images/demo1.png" alt="Image 1" /></div>
  <div><img src="https://raw.githubusercontent.com/chocoluffy/rs_doc/master/images/demo2.png" alt="Image 2" /></div>
</div>

2. Log in to the SDK tool and click on Install RebornScripts under the RebornScript section. As shown in Image 3, the installation is complete.
<div style="display: flex;">
  <div><img src="https://raw.githubusercontent.com/chocoluffy/rs_doc/master/images/demo3.png" alt="Image 1" /></div>
  <div><img src="https://raw.githubusercontent.com/chocoluffy/rs_doc/master/images/demo4.png" alt="Image 2" /></div>
  <div><img src="https://raw.githubusercontent.com/chocoluffy/rs_doc/master/images/demo5.png" alt="Image 3" /></div>
</div>

3. RebornScript Example Scene
<div style="display: flex;">
  <div><img src="https://raw.githubusercontent.com/chocoluffy/rs_doc/master/images/demo6.png" alt="Image 1" /></div>
</div>

## RSNetwork

- `IsNetworkSettled` - Checks if the network is settled from perspective of this client.

- `IsMaster` - Checks if this client calling the method is the master client. 

- `IsClogged` - Checks if the network is congested from the perspective of this client.

- `LocalPlayer` - Gets the local player instance for the client calling this method.

- `MasterPlayer` - Gets the master client's player instance from the perspective of the client calling this method. 

- `IsOwner(RSPlayer player, GameObject obj)` - Check if the player is this GameObject's owner
  - `player`: The RSPlayer to check ownership for.
  - `obj`: The GameObject to check if player owns it.

- `GetOwner(GameObject obj)` - Get the owner of this GameObject
  - `obj`: The GameObject to get the owner of.

- `SetOwner(RSPlayer player, GameObject obj)` - Sets ownership of GameObject to provided player
  - `player`: The RSPlayer to set as owner. 
  - `obj`: The GameObject to set ownership of.

- `IsObjectReady(GameObject obj)` - Checks if networked GameObject is ready/spawned
  - `obj`: The GameObject to check readiness of.

- `Destroy(GameObject obj)` - Destroys the given networked GameObject
  - `obj`: The GameObject to destroy.

- `GetUniqueName(GameObject obj)` - Gets unique identifying name for GameObject
  - `obj`: The GameObject to get unique name for.

- `GetServerTimeInSeconds` - Gets time on server in seconds.

- `GetServerTimeInMilliseconds` - Gets time on server in milliseconds.

- `CalculateServerDeltaTime(double timeInSeconds, double previousTimeInSeconds)` - Calculates delta time between two server timestamps
  - `timeInSeconds`: Current server time in seconds.
  - `previousTimeInSeconds`: Previous server time in seconds.

- `CreateNetAudioAsset(long id, Vector3 pos, Quaternion rot)` - Spawns networked audio source
  - `id`: Unique ID for audio source.
  - `pos`: Position of audio source.
  - `rot`: Rotation of audio source.

- `SetNetMapCustomMessage(string message)` - Sets custom status text on net map
  - `message`: Custom status message string.

## RSProp

- `grabbable` - Bool indicating if prop can be grabbed directly.

- `wearable` - Bool indicating if prop can be worn.

- `scalable` - Bool indicating if scale can be adjusted when held.

- `grabState` - Current GrabState enum value.

- `grabType` - GrabType enum value.

- `specialMessage` - String for special status text.

- `currentPlayer` - Gets the currently grabbing RSPlayer.

- `currentHand` - Gets the currently grabbing hand (GrabHand enum).

- `Drop()` - Tells current owner to drop prop(self only).

- `GenerateHapticEvent(float duration, float amplitude, float frequency)` - Generates haptic event in grabbing hand.
  - `duration`: Haptic duration in seconds.
  - `amplitude`: Haptic amplitude 0-1.
  - `frequency`: Haptic frequency in Hz.

- `OnDestroy()` - Called on destroy. Calls RSInternalProp destroy logic.

- `PlayHaptics()` - Helper to trigger default haptic event.

- `GrabHand` - Enum representing left/right hand.

- `GrabState` - Enum representing all grab states. 

- `GrabType` - Enum describing grab mechanics.

## RSGraphics

- `Blit(Texture source, RenderTexture dest)`
  - `source`: The source texture to blit from.
  - `dest`: The destination render texture to blit to.

- `Blit(Texture source, RenderTexture dest, Material mat)`
  - `source`: The texture to blit.
  - `dest`: The render texture to blit to.
  - `mat`: The material to use for blitting.

- `Blit(Texture source, RenderTexture dest, Vector2 scale, Vector2 offset)`
  - `source`: Source texture.
  - `dest`: Destination render texture.
  - `scale`: Scale factor to apply when blitting.
  - `offset`: Offset to apply when blitting.
  
- `DrawMeshInstanced(Mesh mesh, Material mat, Matrix4x4[] matrices)`
  - `mesh`: The mesh to draw.
  - `mat`: The material to use.
  - `matrices`: Array of matrices to apply to each instance.

- `DrawMeshInstanced(Mesh mesh, Material mat, Matrix4x4[] matrices, int count)`
  - `mesh`: The mesh to draw.
  - `mat`: The material to use.
  - `matrices`: Array of matrices to apply.
  - `count`: How many instances to draw.

## RSPlayer

- `gameObject` - Gets the player's GameObject.

- `isMaster` - Checks if player is master client.

- `isMine` - Checks if player is local client. 

- `nickName` - Gets player's nickname string.

- `profilePicture` - Gets player's profile picture texture.

- `userId` - Gets player's unique identifier.

- `GetAllPlayers()` - Gets all RSPlayer instances.

- `GetPlayerCount()` - Gets number of players.

- `GetPlayerId(RSPlayer player)` - Gets ID for player.
  - `player`: The player to get ID for.

- `GetPlayerByGameObject(GameObject go)` - Lookup player by GameObject.
  - `go`: The player's GameObject.

- `GetPlayerById(int id)` - Lookup player by ID.
  - `id`: The ID to lookup.

- `GetBoneTransform(HumanBodyBones bone)` - Gets bone transform.
  - `bone`: The bone to get transform for.

- `GetBonePosition(HumanBodyBones bone)` - Gets bone position.
  - `bone`: The bone to get position for.  

- `GetBoneRotation(HumanBodyBones bone)` - Gets bone rotation.
  - `bone`: The bone to get rotation for.

- `GetCameraPosition()` - Gets camera position.

- `GetCameraRotation()` - Gets camera rotation.

- `GetPropInHand(GrabHand hand)` - Gets held prop for hand.
  - `hand`: The hand to get held prop for.

- `PlayHapticEventInHand(GrabHand hand, float duration, float amplitude, float frequency)` - Plays haptic on hand.
  - `hand`: The hand to play on.
  - `duration`: Haptic duration in seconds.
  - `amplitude`: Haptic amplitude 0-1.
  - `frequency`: Haptic frequency in Hz.

- `Teleport(Vector3 position, Quaternion rotation)` - Teleports player.
  - `position`: Teleport position.
  - `rotation`: Teleport rotation.

- `Respawn()` - Respawns the player.  

- `EnableGrab(bool enable)` - Enables/disables grabbing.
  - `enable`: True to enable, false to disable.

- `IsUserInVR()` - Checks if player is in VR.

- `GetPosition()` - Gets player position.

- `GetRotation()` - Gets player rotation.

## RSShader

- `PropertyToID(string name)` - Converts property name to shader ID.
  - `name`: Name of shader property.

- `SetGlobalInteger(int nameID, int value)` - Sets global integer shader property.
  - `nameID`: ID of property.
  - `value`: Integer value to set.

- `SetGlobalFloat(int nameID, float value)` - Sets global float property.
  - `nameID`: ID of property.
  - `value`: Float value to set.

- `SetGlobalTexture(int nameID, Texture value)` - Sets global texture property.
  - `nameID`: ID of property.
  - `value`: Texture value to set.

- `SetGlobalColor(int nameID, Color value)` - Sets global Color property.
  - `nameID`: ID of property.
  - `value`: Color value to set.

- `SetGlobalVector(int nameID, Vector4 value)` - Sets global vector property.
  - `nameID`: ID of property.
  - `value`: Vector4 value to set.  

- `SetGlobalMatrix(int nameID, Matrix4x4 value)` - Sets global matrix property.
  - `nameID`: ID of property.
  - `value`: Matrix4x4 value to set.

- `ValidateAgainstPropertyIDWhitelist(int nameID)` - Validates property ID is whitelisted.
  - `nameID`: ID of property.

- `ClearGlobalVariableWhitelist()` - Clears whitelist of allowed IDs.

- `ShaderVariableType` - Enum of different shader variable types.

## RSRenderTexture

- `GetTemporary(int width, int height, int depthBuffer, RenderTextureFormat format, etc...)` - Gets a temporary render texture.
  - `width`: Width in pixels of the texture.
  - `height`: Height in pixels of the texture.
  - `depthBuffer`: Size of depth buffer to use.
  - `format`: Format of render texture.

- `GetTemporary(RenderTextureDescriptor desc)` - Gets a temporary render texture.
  - `desc`: RenderTextureDescriptor defining settings.

- `ReleaseTemporary(RenderTexture texture)` - Releases a temporary texture.
  - `texture`: The temporary RenderTexture to release.

## RSMesh

- `Slice(GameObject go, Vector3 point, Vector3 direct, Material partMat, GameObject part1, GameObject part2)` - Slices a game object into two parts.
  - `go`: The GameObject to slice.
  - `point`: The point in world space where to perform the slice. 
  - `direct`: The direction of the slice.
  - `partMat`: The material to apply to the sliced surfaces.
  - `part1`: The first sliced GameObject part.
  - `part2`: The second sliced GameObject part.

## RSMath

- `FFT(float[] timeDomain)` - Performs a Fast Fourier Transform on the time domain audio data to convert it to frequency domain. Returns the frequency domain data.
  - `timeDomain`: The audio sample data in time domain.

- `CalculateDifferenceTotal(float[] array1, float[] array2, bool ignoreNegative)` - Calculate the sum of two arrays' differences.
  - `array1`: The first float array to compare.
  - `array2`: The second float array to compare.
  - `ignoreNegative`: Whether to ignore negative.

## RebornScriptBehaviour

- `SendCustomEvent(string eventName)` - Calls a custom event method on this behaviour.
  - `eventName`: Name of the 0 parameter public method to call.

- `SendCustomNetworkEvent(NetworkEventTarget target, string eventName)` - Sends custom network event.
  - `target`: Whether to send to owner or everyone.
  - `eventName`: Name of method to call.

- `SendNetMessage(NetworkEventTarget target, string content)` - Sends a network message.
  - `target`: Who to send the message to.
  - `content`: Message content string.

- `OnReceiveNetMessage(string content)` - Handles received messages.
  - `content`: Received message content.

- `UpdateNetMapCustomMessage()` - Signals to update net map text.

- `OnUpdateNetMapCustomMessageComplete()` - Callback when net map text updated.  

- `Interact()` - Called when a player click this gameobject.

- `OnDrop()` - Called when this object is dropped.

- `OnOwnershipTransferred(RSPlayer player)` - Called when ownership changes.
  - `player`: The new owning player.

- `OnGrab()` - Called when this object is grabbed.

- `OnPickupUseDown()` - Called when pickup use starts.

- `OnPickupUseUp()` - Called when pickup use ends.

- `OnHoverEnter()` - Called when a player's hand hovers over this object.

- `OnHoverExit()` - Called when a hover ends.

- `OnLeftTriggerDown()` - Called when left trigger pressed while holding object.

- `OnLeftTriggerUp()` - Called when left trigger released.

- `OnRightTriggerDown()` - Called when right trigger pressed while holding object.

- `OnRightTriggerUp()` - Called when right trigger released.  

- `OnPlayerJoined(RSPlayer player)` - Called when a player joins.
  - `player`: The player that joined.

- `OnPlayerLeft(RSPlayer player)` - Called when a player leaves.
  - `player`: The player that left.
  
- `OnPlayerTriggerEnter(RSPlayer player)` - Called when a player enters the trigger.
  - `player`: The player that entered the trigger.

- `OnPlayerTriggerExit(RSPlayer player)` - Called when a player exits the trigger.
  - `player`: The player that exited the trigger.

- `OnPlayerTriggerStay(RSPlayer player)` - Called each frame player is in trigger.
  - `player`: The player staying in the trigger.
  
- `OnReceiveNetMessage(string content)` - Called when this object receives a network message.
  - `content`: The message content string that was received.
  
- `OnUpdateNetMapCustomMessageComplete(string content)` - Called when updating net map text completes.
  - `content`: The updated status text.