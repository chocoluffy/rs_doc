# ReboSharp API

## What is R#(ReboSharp)
**ReboSharp's underlying is Reborn's proprietary assembly language. We have deeply transformed the underlying compilation, assembly, runtime interpreter and virtual containerized deployment methods, allowing creators to build Turing-complete 3D content and applications in languages they are familiar with, whether professional programming languages like C# and C++, or natural languages that everyone masters. **

Professional creators can use C# syntax, data structures, and built-in Unity interfaces to build 3D games, and use the Reborn SDK for recompilation and deployment. We provide a large number of modules and interfaces that can be used directly to help developers efficiently build a rich content ecosystem with low barriers.

## Supported C# Language Features:

- All logic control mechanisms: including 'if', 'else', 'while', 'for', 'do', 'foreach', 'switch', 'return', 'break', 'continue' and conditional tools (condition?trueOutcome:falseOutcome).
- External functions using 'out' or 'ref' attributes (e.g. multiple versions of Physics.Detect()).
- User-defined functions: including functions with input and output values, and those that extend and use flexible parameters.
- User-defined attributes.
- Adopt RebornScript features, including virtual functions.
- Interact with Unity/RS by accepting event responders with parameters.
- Embed variable values in strings.
- Initialize properties.
- Ability to make self-referencing function calls.
- Direct and indirect data type conversions.
- Array structures and their element accessors.
- Support instantiate.
- All built-in math functions.
- Bypass conditional operations (e.g. true || ValidateCondition() will not trigger ValidateCondition()).
Use 'typeof' for type retrieval.

The vast majority of commonly used C# syntax in daily projects is compatible.If you have any questions, feel free to join our [Discord server](https://discord.gg/kFs7h7vtJJ) and ask in the #SDK channel. We're happy to help clarify any part of the documentation or API usage.



# 1、SDK Installation

## SDK Download

[Download Unity SDK Here](https://reborn-dev.oss-cn-zhangjiakou.aliyuncs.com/4T2M2QiR/RebornSDK_1_5_8.unitypackage), **Unity version requirements are 2021.3.21 or above, create a new URP project.**

## SDK Installation

1. Drag the package into the project and click install; an installer will pop up. In the installer, click on Install Reborn SDK.
<div style="display: flex;">
  <div><img src="https://raw.githubusercontent.com/chocoluffy/rs_doc/aab7f8b4de8713792f214e19fa1a8f3d9b845202/images/demo1.png" alt="Image 1" style="height: 350px;" /></div>
  <div><img src="https://raw.githubusercontent.com/chocoluffy/rs_doc/master/images/demo2.png" alt="Image 2" style="height: 350px;" /></div>
</div>

2. Log in to the SDK tool and click on Install RebornScripts under the RebornScript section. As shown in Image 3, the installation is complete.
<div style="display: flex;">
  <div><img src="https://raw.githubusercontent.com/chocoluffy/rs_doc/master/images/demo3.png" alt="Image 1" style="height: 350px;"/></div>
  <div><img src="https://raw.githubusercontent.com/chocoluffy/rs_doc/master/images/demo4.png" alt="Image 2" style="height: 350px;"/></div>
  <div><img src="https://raw.githubusercontent.com/chocoluffy/rs_doc/master/images/demo5.png" alt="Image 3" style="height: 350px;"/></div>
</div>

3. RebornScript Example Scene
<div style="display: flex;">
  <div><img src="https://raw.githubusercontent.com/chocoluffy/rs_doc/master/images/demo6.png" alt="Image 1" style="height: 150px;"/></div>
</div>

<br><br>
 
 <br>
 <br>



# 2、R# Demo Project Template (RS Demo)

Whether you are a seasoned game developer with extreme enthusiasm for extended reality (XR), harnessing Unity and OpenXR along with native interaction technologies (XR Interaction Toolkit, aka XRI) to build stunning native XR games and apps centered on native gesture control, or a beginner just stepping into the 3D content creation field, eager to create 3D content of your own from scratch, and hoping that these creative works can seamlessly support multiple platforms including PC, mobile and XR, you will find templates and examples in our prepared demo project template library.

- **Grab Functionality**: Our R# framework not only fully supports XRI's variety of advanced functions and features, but also provides you with a fast and efficient path through its concise scripting language and XRI's official detailed documentation, allowing you to build rich, colorful, highly interactive XR content on multiple XR platforms like Quest, Vision Pro, PSVR, etc. without obstacles.
- **Teleport Functionality**: In R#, we have completed in-depth integration and optimization with Unity's native interfaces. For beginner developers who are new to development and interested in basic components and interaction logic, we especially recommend starting your development journey from this fundamental yet potential-rich template. With little or no complex code modification, or only very limited code adjustments, you can easily obtain a brand new, eye-opening native 3D interactive scene experience after uploading.
- **Rotate Object**: For beginner learners who are still in the learning stage, we strongly recommend that you thoroughly experiment with and deploy these basic templates before delving into more advanced and complex ones. By studying in depth the powerful capabilities of Unity's native interfaces and the versatility and flexibility of the C# programming language, you will gain a unique creative experience every time you tweak code and try different configurations.
- **Network Multiplayer**: The R# framework not only integrates highly complex multiplayer templates, but also carries a variety of simulation logic and algorithms. For beginners eager to start from scratch and gradually build their own multiplayer mini-game, whether your interests are multiplayer card games, social games, eSports, or open world games, we strongly recommend starting from this most basic template.
- **PVE Demo**: This is not just a template, it's a comprehensive tutorial. The R# framework provides efficient code compilation and optimization solutions for large-scale, production-level games. Once you have a certain grasp and understanding of multiplayer, we recommend starting from this comprehensive and detailed template to further build your own large, complex and highly personalized game or application.

If you have extensive 3D project development experience and are interested in native 3D content, professional creative content (PGC), and user generated content (UGC), we highly welcome you to communicate and collaborate directly with the administrators and developers of the Reborn community. At present, our community is enthusiastic about self-developing and open-sourcing various large game templates, including but not limited to first-person shooter (FPS), multiplayer online battle arena (MOBA), real-time strategy (RTS), massively multiplayer online (MMO), virtual reality MMO (VRMMO) and more. More excitingly, after the end of each Reborn organization's creative season, the most popular and innovative open source creative templates will have the opportunity to win the honor of "Best Creator", while also having the chance to win high cash prizes.

<div style="display: flex;">
  <div><img src="https://raw.githubusercontent.com/chocoluffy/rs_doc/master/images/reborn-demo-project.png" alt="Image 1" style="height: 350px;" /></div>
</div>

<br><br>

# 3、 Local Runtime Environment (RS Runtime Environment)

The Reborn client runtime simulator (aka RS Runtime Environment) is a tool that allows you to test your Reborn worlds directly in Unity! You can view the state of all objects for direct verification. 

**This is the most popular testing tool among Reborn community creators.** Imagine deploying a production Reborn environment locally in your Unity Editor! You don't have to debug after uploading, all interactions, multiplayer, networking, databases, can simulate the production Reborn runtime logic locally. By guiding creators to support debugging and runtime environments consistent with the production environment locally, it helps creators iterate content at high speed locally, and hand over the verified content to the cloud for distribution after final confirmation of no errors.

Feature Introduction:

- Debug everything in Unity. 
- View Reborn variables and memory error information in Play mode.
- Simulate player controllers.
- Grab props, use interactions, user interfaces.
- Simulate multiplayer.
- Simulate native interaction environments such as XR, PC, mobile, etc.

 <br> 
 <br>


# 4. Natural Language Large Model Code Generation (Reborn GameGPT)

**If you are new to C#, Unity development, and lack relevant prior knowledge. We strongly recommend you start your 3D native content creation journey through Reborn's code generation.**

This is not just a tool or service, it is a whole new content development paradigm that will greatly accelerate the game development cycle, quickly help creators complete the step from 0 to 1, improve development efficiency, and unleash creators' creative potential. 

Capability Overview:

- High-speed code generation. Through our language models, developers can generate complex game logic and components in minutes, greatly improving development speed.
- Programming language flexibility. Our models support C#, R# language generation tailored to the Unity programming environment to accommodate different development needs and environments. 
- Reduced development cycle. Let the model do basic code writing for you, and you will have more time to think about game design, complex code logic and user experience.


Experience Entry:

<div style="display: flex;">
  <div><img src="https://raw.githubusercontent.com/chocoluffy/rs_doc/master/images/reborn-gamegpt.png" alt="Image 1" style="height: 350px;" /></div>
</div>
<br>
<br>
- Please do not add special punctuation in your questions, please describe your requirements clearly with specific logic descriptions.


Usage:

- Let the model provide a basic template from 0 to 1, to help creators quickly start a project.
- Based on your existing inspiration, ask Reborn GameGPT directly to get source code for quick debugging and testing in the local Editor.
- For further iteration of existing features in existing projects, find better solutions and explore ideas.
- Combined with Reborn's hot update capability, generate code while deploying online, allowing your fans and friends to play your creative inspirations in the first time.

 
<br>
 <br>


# 5、 Common Issues

## 1. Using GetComponent<> to get your own custom scripts? 

Specific situation: 

For your own custom RebornScript (RS for short), after attaching it to a GameObject as a component, you want to use the native GetComponent<> or TryGetComponent<> to get the instantiated object of this script. (Note: Unity's native components like Audio Source, Transform, etc. are not affected).

Recommended solution:

To avoid using GetComponent, if you need to get the instantiated object, define the object (or array if multiple) of your custom class ahead of time. In edit mode, drag and assign it so you don't lose the object. 

Define a possible scenario: The character takes some damage when hit by a bullet. Potential issue: Assume the character has a custom RS script A, when the bullet collides with the character, it needs to call a function in that script, so it needs to know which instantiated object of A on the collided character to call, without using `GetComponent<A>`. Possible solutions:

- 1. No script on bullet, RS script A on character handles collision events, identifies bullet type by name (can't use tags/layers yet), and calls corresponding functions. Issue is having to use strings to identify bullet types for parameters and responses, very inconvenient.

- 2. Bullet has RS script B with its info like type, damage. B defines a global RS class C (think of C as controlling script, with N predefined A classes). On collision, B's callback (OnPlayerTrigger in RS) gets RSPlayer, uses player ID to get collided character, passes that + own info as params to C, which calls A's functions.

Example code (method 2):

```csharp
// Character RS script A 

public class A : RebornScriptBehaviour {

  //eg:
  
  public string name; 
  public int id;
  public int hp;

  //Take 1 damage when shot
  public void Damage(){
    if(hp > 0){
      hp -= 1; 
    }
  }

}

// Bullet script B
public class B : RebornScriptBehaviour {

  public C server;
  
  public override void OnPlayerTriggerEnter(RSPlayer player){
    //When player shot
    server.Hit(player.playerId); //Pass hit player id
  }
  
}

// Global control script 
public class C : RebornScriptBehaviour{
  
  public A[] players; //Default match playerIds
  
  public void Hit(int playerId){
    players[playerId].Damage(); 
  }

}
```

In summary, the current way to avoid GetComponent<> for interactions is a global RS class (one instance) - bullet as active, character as passive. Active gets global RS instance, which has passive objects, completing active-global-passive notification.

## 2. Need to consider authority with RSSync scripts

Specific situation:

For objects synced across clients with RSSync, only one client has authority over the object at a time. Only the client with authority can modify position, rotation, etc and have it sync.

Recommended approach: 

For use cases needing RSSync (e.g. objects that only one player can hold but others see move), check authority:

```csharp 
if(RSNetwork.LocalPlayer == RSNetwork.GetOwner(gameObject)){

  //Logic here syncs to all clients

}
```

Also, due to networking, objects may lose authority from client lag, especially when host switches scenes. To ensure safety and validity, we recommend forcing authority of synced objects to host, avoiding issues when host or sync owner leaves:

```csharp
if(RSNetwork.IsMaster){ //If local player is host

  RSNetwork.SetOwner(RSNetwork.LocalPlayer,gameObject); //Set authority to local player (host) 

}
```

## 3. Need to get current room's player GameObjects in real-time

Specific situation: 

Developers may need other players' position info (e.g. minimap showing teammates). This requires real-time position etc of room players. However, the following approach is insufficient:

```csharp
//Note - the following method is inadequate, for comparison only

//Example custom RS script 
public class Example : RebornScriptBehaviour {

  public GameObject parter1; //Teammate 1
  public GameObject parter2; //Teammate 2
  
  public void Init(){
    RSPlayer[] netPlayerList = RSPlayer.GetAllPlayers(); //Assume >= 3 players
    
    //No netPlayerList[0] since that is host/local player
    parter1 = netPlayerList[1]; 
    parter2 = netPlayerList[2];

  }
  
  public void Update(){
    Debug.Log(parter1.transform.position); //Logs old position
    Debug.Log(parter2.transform.position); //Logs old position
  }

}
```

Here, Init saves old positions that likely won't update. Instead, we recommend:


```csharp
public class Example : RebornScriptBehaviour {

  public void Update(){
    RSPlayer[] netPlayerList = RSPlayer.GetAllPlayers();
    
    Debug.Log(netPlayerList[1].gameObject.transform.position); //Logs current position
    Debug.Log(netPlayerList[2].gameObject.transform.position);

  }  
}
```

So in scenes needing real-time data, get latest player list in Update(). This has minimal performance impact, feel free to use.

## 4. Want RS script methods to be referenced directly by UnityActions

Recommended approach:

Wrap method in outer layer to enable parameterized references:

```csharp

public int index;

public void MyFunc(int n){
  // My function
}

//Call this externally 
public void MyFuncButton(){
  MyFunc(index); 
}

```

# 6、ReboSharp API Documentation

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