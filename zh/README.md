# ReboSharp API文档

如果遇到了你解决不了的问题，或者是希望增加API接口来实现更有创意的效果，加入QQ：788916776，和管理员取得联系，我们会最快时间给您技术支持！

## SDK安装流程
1. 把package拖入工程，点击install，会弹出installer。在installer中，点击 Install Reborn SDK
<div style="display: flex;">
  <div><img src="https://raw.githubusercontent.com/chocoluffy/rs_doc/aab7f8b4de8713792f214e19fa1a8f3d9b845202/images/demo1.png" alt="Image 1" /></div>
  <div><img src="https://raw.githubusercontent.com/chocoluffy/rs_doc/master/images/demo2.png" alt="Image 2" /></div>
</div>

2. 在SDK tool中login，在RebornScript栏目下点击Install RebornScripts。如图三，安装完成
<div style="display: flex;">
  <div><img src="https://raw.githubusercontent.com/chocoluffy/rs_doc/master/images/demo3.png" alt="Image 1" /></div>
  <div><img src="https://raw.githubusercontent.com/chocoluffy/rs_doc/master/images/demo4.png" alt="Image 2" /></div>
  <div><img src="https://raw.githubusercontent.com/chocoluffy/rs_doc/master/images/demo5.png" alt="Image 3" /></div>
</div>

3. RebornScript示例场景
<div style="display: flex;">
  <div><img src="https://raw.githubusercontent.com/chocoluffy/rs_doc/master/images/demo6.png" alt="Image 1" /></div>
</div>

## RSNetwork

- `IsNetworkSettled` - 检查从这个客户端的视角网络是否稳定。

- `IsMaster` - 检查调用此方法的客户端是否是主控客户端。

- `IsClogged` - 从这个客户端的视角检查网络是否拥堵。

- `LocalPlayer` - 获取调用此方法的客户端的本地玩家实例。

- `MasterPlayer` - 从调用此方法的客户端的视角获取主控客户端的玩家实例。

- `IsOwner(RSPlayer player, GameObject obj)` - 检查玩家是否是这个GameObject的拥有者。
  - `player`: 要检查拥有权的RSPlayer。
  - `obj`: 要检查玩家是否拥有的GameObject。

- `GetOwner(GameObject obj)` - 获取这个GameObject的拥有者。
  - `obj`: 要获取拥有者的GameObject。

- `SetOwner(RSPlayer player, GameObject obj)` - 将GameObject的拥有权设置为提供的玩家。
  - `player`: 要设置为拥有者的RSPlayer。
  - `obj`: 要设置拥有权的GameObject。

- `IsObjectReady(GameObject obj)` - 检查网络化的GameObject是否准备就绪/已生成。
  - `obj`: 要检查就绪状态的GameObject。

- `Destroy(GameObject obj)` - 销毁给定的网络化GameObject。
  - `obj`: 要销毁的GameObject。

- `GetUniqueName(GameObject obj)` - 为GameObject获取唯一的标识名称。
  - `obj`: 要获取唯一名称的GameObject。

- `GetServerTimeInSeconds` - 以秒为单位获取服务器时间。

- `GetServerTimeInMilliseconds` - 以毫秒为单位获取服务器时间。

- `CalculateServerDeltaTime(double timeInSeconds, double previousTimeInSeconds)` - 计算两个服务器时间戳之间的时间差。
  - `timeInSeconds`: 秒中的当前服务器时间。
  - `previousTimeInSeconds`: 秒中的前一个服务器时间。

- `CreateNetAudioAsset(long id, Vector3 pos, Quaternion rot)` - 生成网络化音频源。
  - `id`: 音频源的唯一ID。
  - `pos`: 音频源的位置。
  - `rot`: 音频源的旋转。

- `SetNetMapCustomMessage(string message)` - 在网络地图上设置自定义状态文本。
  - `message`: 自定义状态消息字符串。

## RSProp

- `grabbable` - 布尔值,表示道具是否可以直接抓取。

- `wearable` - 布尔值,表示道具是否可以穿戴。

- `scalable` - 布尔值,表示是否可以在抓住时调整缩放。

- `grabState` - 当前的 GrabState 枚举值。

- `grabType` - GrabType 枚举值。

- `specialMessage` - 用于特殊状态文本的字符串。

- `currentPlayer` - 获取当前抓取中的 RSPlayer。

- `currentHand` - 获取当前抓取的手(GrabHand 枚举)。

- `Drop()` - 告诉当前拥有者放下道具(仅限自身)。

- `GenerateHapticEvent(float duration, float amplitude, float frequency)` - 在抓取手中生成触觉事件。
  - `duration`: 触觉持续时间,以秒为单位。
  - `amplitude`: 触觉幅度 0-1。
  - `frequency`: 触觉频率,以 Hz 为单位。

- `OnDestroy()` - 在销毁时调用。调用 RSInternalProp 销毁逻辑。

- `PlayHaptics()` - 帮助触发默认触觉事件。

- `GrabHand` - 表示左/右手的枚举。

- `GrabState` - 表示所有抓取状态的枚举。

- `GrabType` - 描述抓取机制的枚举。

## RSGraphics

- `Blit(Texture source, RenderTexture dest)`
  - `source`: 要从中拷贝的源纹理。
  - `dest`: 要拷贝到的目标渲染纹理。

- `Blit(Texture source, RenderTexture dest, Material mat)`
  - `source`: 要拷贝的纹理。
  - `dest`: 要拷贝到的渲染纹理。
  - `mat`: 用于拷贝的材质。

- `Blit(Texture source, RenderTexture dest, Vector2 scale, Vector2 offset)`
  - `source`: 源纹理。
  - `dest`: 目标渲染纹理。
  - `scale`: 拷贝时要应用的缩放系数。
  - `offset`: 拷贝时要应用的偏移量。
  
- `DrawMeshInstanced(Mesh mesh, Material mat, Matrix4x4[] matrices)`
  - `mesh`: 要绘制的网格。
  - `mat`: 要使用的材质。
  - `matrices`: 要应用于每个实例的矩阵数组。

- `DrawMeshInstanced(Mesh mesh, Material mat, Matrix4x4[] matrices, int count)`
  - `mesh`: 要绘制的网格。
  - `mat`: 要使用的材质。
  - `matrices`: 要应用的矩阵数组。
  - `count`: 要绘制的实例数量。

## RSPlayer

- `gameObject` - 获取玩家的GameObject。

- `isMaster` - 检查玩家是否是主控客户端。

- `isMine` - 检查玩家是否是本地客户端。

- `nickName` - 获取玩家的昵称字符串。

- `profilePicture` - 获取玩家的个人资料图片纹理。

- `userId` - 获取玩家的唯一标识符。

- `GetAllPlayers()` - 获取所有RSPlayer实例。

- `GetPlayerCount()` - 获取玩家数量。

- `GetPlayerId(RSPlayer player)` - 获取玩家的ID。
  - `player`: 要获取ID的玩家。

- `GetPlayerByGameObject(GameObject go)` - 通过GameObject查找玩家。
  - `go`: 玩家的GameObject。

- `GetPlayerById(int id)` - 通过ID查找玩家。
  - `id`: 要查找的ID。

- `GetBoneTransform(HumanBodyBones bone)` - 获取骨骼变换。
  - `bone`: 要获取变换的骨骼。

- `GetBonePosition(HumanBodyBones bone)` - 获取骨骼位置。
  - `bone`: 要获取位置的骨骼。

- `GetBoneRotation(HumanBodyBones bone)` - 获取骨骼旋转。
  - `bone`: 要获取旋转的骨骼。

- `GetCameraPosition()` - 获取相机位置。

- `GetCameraRotation()` - 获取相机旋转。

- `GetPropInHand(GrabHand hand)` - 获取手中持有的道具。
  - `hand`: 要获取持有道具的手。

- `PlayHapticEventInHand(GrabHand hand, float duration, float amplitude, float frequency)` - 在手上播放触觉。
  - `hand`: 要播放的手。
  - `duration`: 触觉持续时间,以秒为单位。
  - `amplitude`: 触觉幅度 0-1。
  - `frequency`: 触觉频率,以Hz为单位。

- `Teleport(Vector3 position, Quaternion rotation)` - 传送玩家。
  - `position`: 传送位置。
  - `rotation`: 传送旋转。

- `Respawn()` - 重新生成玩家。

- `EnableGrab(bool enable)` - 启用/禁用抓取。
  - `enable`: 设置为true启用,false禁用。

- `IsUserInVR()` - 检查玩家是否在VR中。

- `GetPosition()` - 获取玩家位置。

- `GetRotation()` - 获取玩家旋转。

## RSShader

- `PropertyToID(string name)` - 将属性名称转换为着色器ID。
  - `name`: 着色器属性的名称。

- `SetGlobalInteger(int nameID, int value)` - 设置全局整数着色器属性。
  - `nameID`: 属性的ID。
  - `value`: 要设置的整数值。

- `SetGlobalFloat(int nameID, float value)` - 设置全局浮点数属性。
  - `nameID`: 属性的ID。
  - `value`: 要设置的浮点数值。

- `SetGlobalTexture(int nameID, Texture value)` - 设置全局纹理属性。
  - `nameID`: 属性的ID。
  - `value`: 要设置的纹理值。

- `SetGlobalColor(int nameID, Color value)` - 设置全局颜色属性。
  - `nameID`: 属性的ID。
  - `value`: 要设置的颜色值。

- `SetGlobalVector(int nameID, Vector4 value)` - 设置全局矢量属性。
  - `nameID`: 属性的ID。
  - `value`: 要设置的Vector4值。

- `SetGlobalMatrix(int nameID, Matrix4x4 value)` - 设置全局矩阵属性。
  - `nameID`: 属性的ID。
  - `value`: 要设置的Matrix4x4值。

- `ValidateAgainstPropertyIDWhitelist(int nameID)` - 验证属性ID是否在白名单中。
  - `nameID`: 属性的ID。

- `ClearGlobalVariableWhitelist()` - 清除允许的ID白名单。

- `ShaderVariableType` - 不同着色器变量类型的枚举。

## RSRenderTexture  

- `GetTemporary(int width, int height, int depthBuffer, RenderTextureFormat format, 等等...)` - 获取临时渲染纹理。
  - `width`: 纹理的宽度,以像素为单位。
  - `height`: 纹理的高度,以像素为单位。 
  - `depthBuffer`: 要使用的深度缓冲区大小。
  - `format`: 渲染纹理的格式。

- `GetTemporary(RenderTextureDescriptor desc)` - 获取临时渲染纹理。
  - `desc`: 定义设置的RenderTextureDescriptor。

- `ReleaseTemporary(RenderTexture texture)` - 释放临时纹理。
  - `texture`: 要释放的临时RenderTexture。

## RSMesh

- `Slice(GameObject go, Vector3 point, Vector3 direct, Material partMat, GameObject part1, GameObject part2)` - 将游戏对象切片成两部分。
  - `go`: 要切片的GameObject。
  - `point`: 在世界空间中执行切片的点。
  - `direct`: 切片的方向。
  - `partMat`: 要应用于切片表面的材质。
  - `part1`: 第一个切片的GameObject部分。
  - `part2`: 第二个切片的GameObject部分。

## RSMath

- `FFT(float[] timeDomain)` - 对时间域音频数据执行快速傅里叶变换,将其转换为频域。返回频域数据。
  - `timeDomain`: 时间域中的音频样本数据。

- `CalculateDifferenceTotal(float[] array1, float[] array2, bool ignoreNegative)` - 计算两个数组差异的总和。
  - `array1`: 要比较的第一个浮点数数组。
  - `array2`: 要比较的第二个浮点数数组。
  - `ignoreNegative`: 是否忽略负值。

## RebornScriptBehaviour

- `SendCustomEvent(string eventName)` - 在此行为上调用自定义事件方法。
  - `eventName`: 要调用的0参数公共方法的名称。

- `SendCustomNetworkEvent(NetworkEventTarget target, string eventName)` - 发送自定义网络事件。
  - `target`: 是发送给拥有者还是每个人。
  - `eventName`: 要调用的方法名称。

- `SendNetMessage(NetworkEventTarget target, string content)` - 发送网络消息。
  - `target`: 发送消息的目标。
  - `content`: 消息内容字符串。

- `OnReceiveNetMessage(string content)` - 处理收到的消息。
  - `content`: 收到的消息内容。

- `UpdateNetMapCustomMessage()` - 发出更新网络地图文本的信号。

- `OnUpdateNetMapCustomMessageComplete()` - 当网络地图文本更新时的回调。

- `Interact()` - 当玩家点击此游戏对象时调用。

- `OnDrop()` - 当这个对象被丢弃时调用。 

- `OnOwnershipTransferred(RSPlayer player)` - 当拥有权更改时调用。
  - `player`: 新的拥有者玩家。

- `OnGrab()` - 当这个对象被抓取时调用。

- `OnPickupUseDown()` - 当拾取使用开始时调用。

- `OnPickupUseUp()` - 当拾取使用结束时调用。

- `OnHoverEnter()` - 当玩家的手悬停在此对象上时调用。

- `OnHoverExit()` - 当悬停结束时调用。

- `OnLeftTriggerDown()` - 持有对象时按下左扳机时调用。

- `OnLeftTriggerUp()` - 左扳机释放时调用。

- `OnRightTriggerDown()` - 持有对象时按下右扳机时调用。

- `OnRightTriggerUp()` - 右扳机释放时调用。

- `OnPlayerJoined(RSPlayer player)` - 当玩家加入时调用。
  - `player`: 加入的玩家。

- `OnPlayerLeft(RSPlayer player)` - 当玩家离开时调用。
  - `player`: 离开的玩家。

- `OnPlayerTriggerEnter(RSPlayer player)` - 当玩家进入触发器时调用。
  - `player`: 进入触发器的玩家。

- `OnPlayerTriggerExit(RSPlayer player)` - 当玩家离开触发器时调用。
  - `player`: 离开触发器的玩家。

- `OnPlayerTriggerStay(RSPlayer player)` - 玩家留在触发器中时每帧调用。
  - `player`: 停留在触发器中的玩家。

- `OnReceiveNetMessage(string content)` - 当此对象收到网络消息时调用。
  - `content`: 收到的消息内容字符串。

- `OnUpdateNetMapCustomMessageComplete(string content)` - 更新网络地图文本完成时调用。
  - `content`: 更新后的状态文本。