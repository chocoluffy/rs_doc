# 世界创作：Unity ReboSharp 使用文档

## 什么是R#（ReboSharp）

**ReboSharp 底层是Reborn专有的汇编语言。我们深度改造了引擎底层，让创作者能用自己熟悉的语言来构建图灵完备的3D内容与应用，无论是专业编程语言比如C#、C++，还是人人都掌握的自然语言。**

专业创作者可以使用C#语法、数据结构、Unity内置接口来构建3D游戏，并借助Reborn SDK进行重编译与部署，我们提供了大量可直接使用的功能模块与接口，帮助开发者高效低门槛构建丰富内容生态。

## 支持的 C# 功能语法：

- 所有逻辑控制机制：包括 'if'、'else'、'while'、'for'、'do'、'foreach'、'switch'、'return'、'break'、'continue' 和条件工具（条件？trueOutcome：falseOutcome）。
- 使用 'out' 或 'ref' 属性的外部函数（例如，多个版本的 Physics.Detect()）。
- 用户自定义函数：包括具有输入值和输出值的函数，以及那些扩展并使用灵活参数的函数。
- 用户自定义属性。
- 采用 RebornScript 功能，包括虚拟函数。
- 通过接受参数的事件响应器与 Unity/RS 进行交互。
- 在字符串中嵌入变量值。
- 初始化属性。
- 能够进行自引用函数调用。
- 直接和间接数据类型转换。
- 数组结构及其元素访问器。
- 支持instantiate。
- 所有内置数学函数。
- 绕过条件操作（例如，true || ValidateCondition() 不会触发 ValidateCondition()）。
- 使用 'typeof' 进行类型检索。

绝大多数日常项目用到的C#语法都是兼容的，如果遇到了你解决不了的问题，或者是希望增加API接口来实现更有创意的效果，请不用着急，加入QQ：788916776，和管理员取得联系，我们会最快时间给您技术支持！

<br>
<br>


# 1、SDK安装流程

## SDK下载

[点此处下载Unity SDK](https://reborn-dev.oss-cn-zhangjiakou.aliyuncs.com/4T2M2QiR/RebornSDK_1_6_8.unitypackage)，**Unity版本要求在2022.3.8或以上，新建URP工程。**

## SDK安装

1. 把package拖入工程，点击install，会弹出installer。在installer中，点击 Install Reborn SDK
<div style="display: flex;">
  <div><img src="https://raw.githubusercontent.com/chocoluffy/rs_doc/aab7f8b4de8713792f214e19fa1a8f3d9b845202/images/demo1.png" alt="Image 1" style="height: 350px;" /></div>
  <div><img src="https://raw.githubusercontent.com/chocoluffy/rs_doc/master/images/demo2.png" alt="Image 2" style="height: 350px;" /></div>
</div>

2. 在SDK tool中login，在RebornScript栏目下点击Install RebornScripts。如图三，安装完成。如果您之前并没有注册过Reborn账号并希望直接测试使用SDK，请联系社区管理员索取SDK测试账号与密码。
<div style="display: flex;">
  <div><img src="https://raw.githubusercontent.com/chocoluffy/rs_doc/master/images/demo3.png" alt="Image 1" style="height: 350px;" /></div>
  <div><img src="https://raw.githubusercontent.com/chocoluffy/rs_doc/master/images/demo4.png" alt="Image 2" style="height: 350px;" /></div>
  <div><img src="https://raw.githubusercontent.com/chocoluffy/rs_doc/master/images/demo5.png" alt="Image 3" style="height: 350px;" /></div>
</div>

3. 示例场景。下一小节我们将具体展开，借助完整的demo项目模版，创作者可以在无修改、或者小修改的情况下上传自己创作的内容至Reborn，极大降低创作者的开发门槛。
<div style="display: flex;">
  <div><img src="https://raw.githubusercontent.com/chocoluffy/rs_doc/master/images/demo6.png" alt="Image 1" style="height: 150px;" /></div>
</div>

<br><br>
 
 <br>
 <br>


# 2、R# Demo项目模版（RS Demo）

无论您是一位对扩展现实（Extended Reality，简称XR）怀有极度热诚的资深游戏开发者，动用Unity和OpenXR以及搭载的原生交互技术（XR Interaction Toolkit，简称XRI）来构建出以原生手势控制为核心的令人惊叹的XR原生游戏和应用，还是一名刚刚踏入3D内容创作领域的初学者，怀有一颗渴望从无到有地打造属于自己的3D内容之心，并希望这些创意作品能够无缝兼容包括PC、移动端以及XR在内的多种平台，您将在我们准备的Demo项目模板库中找到模板和范例。

- **抓取功能（Grab）**：我们的R#框架不仅全面地支持XRI的多种高级函数和特性，更通过其简明扼要的脚本语言以及XRI的官方详细文档，为您提供了一条快速而高效的路径，使您能够在Quest、Vision Pro、PSVR等多个XR平台上无障碍地构建出种类丰富、丰富多彩、高度互动的XR内容。

- **传送功能（Teleport）**：在R#中，我们已经与Unity的原生接口完成了深度的集成与优化。特别是对于那些初涉开发领域、对基础组件和交互逻辑有着浓厚兴趣的新手开发者，我们特别建议您从这个基础但却充满潜力的模板开始您的开发旅程。几乎无需复杂的代码修改，或者只需要进行非常有限的代码调整，上传后您便可轻松获得一款全新、令人眼前一亮的3D原生互动场景体验。

- **旋转物体（RotateObject）**：对于那些正处于学习阶段的初学者，我们更是强烈推荐您在深入挖掘更为高级复杂的模板之前，先将这几个基础模板进行全方位的实验和部署。通过深入研究Unity原生接口的强大功能以及C#编程语言的多样性和灵活性，您将在每次微调代码和尝试不同配置后都能获得一种独特的创作体验。

- **网络多人功能（Net）**：R#框架不仅集成了高度复杂的多人联机模板，还搭载了多种模拟逻辑和算法。对于渴望从零开始，逐步构建出一款属于自己的多人联机小游戏的初学者，无论您的兴趣点是多人卡牌、社交、电子竞技或者是开放世界类型的游戏，我们都强烈建议您从这个最为基础的模板开始。

- **PVE演示（PVE_DEMO）**：这不仅是一个模板，更是一个全面的教程。R#框架为大规模、生产级别的游戏提供了高效的代码编译和优化解决方案。当您已经对多人联机有了一定的把握和理解后，我们推荐您从这个全面而详尽的模板开始，进一步地构建出属于您自己的大型、复杂、高度个性化的游戏或应用。

如果您具备丰富的3D项目开发经验，并对3D原生内容、专业创作内容（PGC）、普通用户生成内容（UGC）持有浓厚兴趣，我们极其欢迎您与Reborn社区的管理员和开发者直接进行交流和合作。目前，我们的社区热衷于自发开发和开源各类大型游戏模板，包括但不限于第一人称射击（FPS）、多人在线战术竞技（MOBA）、实时策略（RTS）、大型多人在线（MMO）、虚拟现实多人在线（VRMMO）等多种类型。更令人振奋的是，每一个Reborn组织的创作赛季结束后，最受欢迎和最具创新性的开源创作模板将有机会获得“最佳创作者”的荣誉称号，同时还将有机会赢取高额现金奖励。

<div style="display: flex;">
  <div><img src="https://raw.githubusercontent.com/chocoluffy/rs_doc/master/images/reborn-demo-project.png" alt="Image 1" style="height: 350px;" /></div>
</div>

<br><br>
  

# 3、本地运行时虚拟环境（RS Runtime Environment）

Reborn 客户端运行时模拟器（简称 RS Runtime Environment）是一个工具，允许您直接在 Unity 中测试您的 Reborn 世界！您可以查看所有对象的状态以直接进行验证。

**这是Reborn社区创作者里最受欢迎的测试工具。** 想象你在本地Unity Editor环境部署了一份生产环境的Reborn！你不必在上传后再进行debug调试，一切交互、多人联机、网络、数据库，都可在本地模拟生产环境的Reborn运行逻辑。通过引导创作者在本地支持与生产环境一致的调试与运行环境，帮助创作者高速在本地迭代内容，并在最终确认内容无误后，交由云端分发。

功能介绍：

- 在 Unity 中调试一切。
- 在 Play 模式下查看 Reborn 变量与内存报错信息。
- 模拟玩家控制器。
- 抓取道具，使用交互，用户界面。
- 模拟多人联机。
- 模拟XR、PC、移动端等原生交互环境。

 <br>
 <br>

# 4、自然语言大模型生成代码（Reborn GameGPT）

**如果你刚入门C#、Unity开发，缺乏相关的先验知识。我们强烈推荐你通过Reborn代码生成的方式开始你的3D原生内容创作之旅。**

这不仅仅是一个工具或服务，更是一个全新的内容开发范式，将极大地加速游戏开发周期，快速帮助创作者完成从0到1的一步，提升开发效率，并解放开发者的创造性潜力。

能力概览：

- 高速代码生成。通过我们的语言模型，开发者能够在几分钟内生成复杂的游戏逻辑和组件，从而大大提高开发速度。
- 编程语言灵活性。我们的模型支持针对Unity编程环境的C#、R#语言生成，能够适应不同的开发需求和环境。
- 减少开发周期。让模型为你做基础代码编写，你将更多的时间可以用于思考游戏设计、复杂代码逻辑和用户体验。


体验入口：

<div style="display: flex;">
  <div><img src="https://raw.githubusercontent.com/chocoluffy/rs_doc/master/images/reborn-gamegpt.png" alt="Image 1" style="height: 350px;" /></div>
</div>
<br>
<br>
- 请注意不要在你的提问里添加特殊标点符号(逗号、问号等)，请以具体的逻辑描述清晰描述你的需求。


使用方式：

- 让模型提供从0到1的基础模版，方便创作者快速启动项目。比如：`generate a moving cube`
- 基于你的已有灵感向Reborn GameGPT直接提问，获取源代码，用于本地Editor的快速调试测试。
- 针对已有项目已有功能的进一步迭代，寻找更优解法，开拓思路。比如：`how to change the material on a GameObject`
- 搭配Reborn的热更新能力，边生成代码，边部署至线上，让你的粉丝们、朋友们在第一时间游玩你的灵感创作。

 
<br>
 <br>

# 5、常见问题

## 1.使用GetComponent<>获取自己编写的脚本？

**具体情况：**
对于自己编写的RebornScript（后续用RS代替），挂载于GameObject上作为组件后希望使用原生的GetComponent<>或者TryGetComponent<>来获取的这个脚本的实例化对象。（注：unity原生的组件例如Audio Source，Transform等不受其影响）

**建议方案：**
绕开GetComponent的方式，若有需要获取实例化对象，提前定义好自己编写的类的对象（若有多个则定义数组），在编辑状态下拖拽赋值，这样就不会丢失对象。
定义一个可能出现的场景：子弹射中角色，角色会对应的受到伤害。会出现的问题：假设角色身上有自定义的RS脚本A，当子弹碰撞到角色时需要调用该脚本中的函数，此时需要知道子弹碰到的角色身上所挂的是A的哪个实例化对象，在不使用`Get Component<A>`的情况下，可能会出现的问题和解决方案有：

- 1.子弹上不挂载脚本，角色的RS脚本A中加入碰撞事件，根据名字来判断子弹的类型（现在还无法使用tag和layer），并相应的调用函数，问题是参数与对于不同种类子弹的响应只能通过名字的字符串来进行识别，非常不方便。
- 2.在子弹上挂载一个RS脚本B，其中定义好子弹本身的信息，包括种类、伤害。且需要在B中定义一个RS类C（这个C可以理解为控制全局的脚本，C的实例中已经定义了N个RS类A且已被赋值），当子弹碰撞时，会回调B脚本中的碰撞事件（RebornScript中有可以重载的OnPlayerTrigger/Enter/Exit的方法，可以直接获取到RSPlayer对象），根据碰撞到的RSPlayer实例，可以获取到碰撞角色的ID，子弹的B脚本将获取到的ID以及自身的信息作为参数，传入C脚本，C脚本中编写对应的函数来实现对角色产生相应伤害的功能（例如调用A的某个函数）。
代码示例如下(方法二)：
```csharp
//用来管理角色的RS脚本A
public class A : RebornScriptBehaviour
{
    //eg:
    public string name;
    public int id;
    public int hp;
    
    //当玩家被子弹射中时受到一点伤害
    public void Damage()
    {
        if(hp > 0)
        {
            hp -= 1;
        }
    }
}
//挂载在子弹上的B脚本
public class B : RebornScriptBehaviour
{
    public C server;
    
    public override void OnPlayerTriggerEnter(RSPlayer player)
    {
        //当有玩家被子弹射中时
        server.Hit(player.playerId);//传入的参数为击中玩家的id
    }
}
//一个控制全局的脚本，完成接受主动方调用，再作用于被动方的任务
public class C : RebornScriptBehaviour
{
    public A[] players;//默认当前角色队列中的下表与玩家playerId相同
    
    public void Hit(int playerId)
    {
        players[playerId].Damage();
    }
}
```
总结
目前绕开Get Component<>的方法实现不同物体间相互作用的方式就是使用一个控制全局的RS类（原则上是一个实例化对象），在一组交互（比如子弹射中角色），子弹为主动方，角色为被动方，主动方需要提前获取全局的RS类的对象，RS类的对象需要提前获取被动方，这样完成一个主动方通知全局，全局通知被动方的过程。


## 2.使用RSSync脚本时，需要注意拥有权的问题。

**具体情况：**
对于在各个客户端中同步的物体（挂载了RSSync脚本），同时只有一个客户端对这个物体持有拥有权，只有持有拥有权的客户端对这个物体进行修改，例如改变位置，旋转等，才会被同步到所有的客户端。

**建议方案：**
对于需要使用到RSSync同步的应用场景（例如场景中一些同时只能被唯一一个玩家持有且其他玩家需要能看到此物体运动的情况），开发者需要使用：
```csharp
if(RSNetwork.LocalPlayer == RSNetwork.GetOwner(gameObject))
{
    //逻辑 产生的效果将被同步到各个客户端
}
```
除此之外，受到网络影响，某些物体可能会因为玩家本地的网络波动而丢失拥有者，这种问题尤其在房主切换场景时会频繁出现，因此为了确保代码的安全性与有效性，我们建议开发者将所有需要同步的物体的拥有权强制交给房主，这样可以避免原房主或某个同步物体拥有者退出房间时带来的不良影响。例子如下：
```csharp
if(RSNetwork.IsMaster)//判断本地玩家是否为房主
{
    RSNetwork.SetOwner(RSNetwork.LocalPlayer,gameObject); //将当前RS脚本所在物体的拥有权交予本地玩家（房主）
}
```

## 3.对于获取当前房间内游戏玩家的GameObject，需要实时获取并更新。

**具体情况：**
当开发者需要获取到不同玩家的位置信息（例如多人对战中小地图显示自己与队友的功能）时，毫无疑问是需要获取到当前房间内其他玩家的position等信息的，但是目前如果使用如下的方法：
```csharp
//请注意以下的方法是不足够好的形式，仅供与更好的方法对比参考使用
//假设我有一个自己定义的RS脚本Example
public class Example : RebornScriptBehaviour
{
    public GameObject parter1;//我的一号队友
    public GameObject parter2;//我的二号队友
    
    public void Init()
    {
        RSPlayer[] netPlayerList = RSPlayer.GetAllPlayers();//此处默认当前玩家队列内人数大于等于三人
        //没有netPlayerList[0]是因为还有房主/本地玩家自己。
        parter1 = netPlayerList[1];
        parter2 = netPlayerList[2];
    }
    public void Update()
    {
        Debug.Log(parter1.transform.position);//打印一号队友当前的位置
        Debug.Log(parter1.transform.position);//打印二号队友当前的位置
    }
    
}
```
以上的情况下，打印出的结果大概率是调用Init函数时角色所存在的位置且不会随着其他玩家的改变而打印出正确的位置。因此我们更推荐如下的形式：
```csharp
public class Example : RebornScriptBehaviour
{

    public void Update()
    {
        RSPlayer[] netPlayerList = RSPlayer.GetAllPlayers();//此处默认当前玩家队列内人数大于等于三人
        Debug.Log(netPlayerList[1].gameObject.transform.position);//打印一号队友当前的位置
        Debug.Log(netPlayerList[1].gameObject.transform.position);//打印二号队友当前的位置
        
        //此处附上获取本地玩家的方法:
       //Network.LocalPlayer.gameObject
    }
    
}
```
也就是在需要实时更新的场景下，在Update()中实时获取房间内的玩家队列并获取需要的玩家对象。这并不会对效率产生很大的影响，请放心使用。


## 4.RS脚本方法希望直接被UnityAction引用

**建议方案：**
通过在方法外包一层来实现带参数的引用
```csharp
public int index;

public void MyFunc(int n)
{
    // My function
}

//在方法内调用这个
public void MyFuncButton()
{
    MyFunc(index);
}
```
 
  
  <br>
 <br>

# 6、ReboSharp API接口

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