ECS架构：
1.目的：
作为一种游戏开发架构模式，将所有要定期进行迭代的数据紧密打包到一起，以便可以一次性加载到缓存中，解决缓存不友好的问题。
2.组成：
Entity：仅包含一个 ID，用于替代 OOP 中“对象”的概念
Component：是一个仅包含相关数据的数据结构（POD类型，通常是一个结构体）
System：负责处理 Entity 和 Component 之间的交互
3.Entity：
仅包含一个 id
4.Component：
一些功能上相关的数据的集合，每一个组件都会有一个独一无二的 ID
5.Signature：
跟踪 Entity 拥有的所有 Component，并跟踪 System 关心哪些 Component
6.Entity Manager
负责分配 Entity ID，并记录 ID 的使用情况
7.Component Array
迭代数组中的所有索引，始终保持数组装满有效的数据。
8.Component Manager
在 Component 需要添加或删除时与所有不同的 ComponentArray 进行通信。
9.System
负责对一组具有特定 Component 签名的 Entity 列表进行处理（Entity 应该包含所有该 System 需要的 Components）
10.System Manager
负责维护已注册的 System 及其签名
11.Coordinator
建立三个 Manager 之间的交流
12.优缺点
面向对象的编程模式来说显然是有性能上的巨大优势，但没有面向对象的编程模式直观，不利于后期的修改和维护





MonoBehaviour 的生命周期；
 MonoBehaviour 的生命周期函数主要有：
OnValidate: 确认事件，脚本被加载、启用、禁用、Inspector 面板值被修改时，都会执行一次
Awake：唤醒事件，只执行 1 次，游戏一开始运行就执行。
OnEnable：启用事件，只执行 1 次，当脚本组件被启用的时候执行一次。
Start：开始事件，只执行 1 次。
FixedUpdate：固定更新事件，每隔 0.02 秒执行一次，所有物理组件相关的更新都在这个事件中处理。
Update：更新事件，每帧执行 1 次。
LateUpdate：稍后更新事件，每帧执行 1 次，在 Update 事件执行完毕后再执行。
OnGUI：GUI渲染事件，每帧执行 2 次。
OnDisable：禁用事件，只执行1 次，在 OnDestroy 事件前执行，或者当该脚本组件被禁用后，也会触发该事件。
OnDestroy：销毁事件，只执行 1 次，当脚本所挂载的游戏物体被销毁时执行。




设计模式 ：
1.认识：
是软件设计中常见问题的典型解决方案，可用于解决代码中反复出现的设计问题
2.模式内容：
 意图部分，动机部分 ，结构部分
3.模式的分类
创建型模式，结构型模式，行为模式
4.创建型模式
创建型模式提供了创建对象的机制，能够提升已有代码的灵
活性和可复用性。
5.结构型模式
结构型模式介绍如何将对象和类组装成较大的结构，并同时
保持结构的灵活和高效。
6.行为模式
行为模式负责对象间的高效沟通和职责委派。





                          
