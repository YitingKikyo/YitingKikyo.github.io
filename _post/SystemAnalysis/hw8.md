## hw 8 -- 架构建模 - 云时代的架构实践  
### 描述软件架构与框架之间的区别与联系 
#### 架构：  
* 定义：  
软件架构（software architecture）是一系列相关的抽象模式，用于指导大型软件系统各个方面的设计。  
是一个系统的草图，描述的对象是直接构成系统的抽象组件，各个组件之间的连接则明确和相对细致地描述组件之间的通讯。  
* 特点：  
一个软件系统从整体到部分的最高层次的划分（包括架构元件、联结器、任务流）

#### 框架：  
* 定义：  
框架（Framework）是整个或部分系统的可重用设计，表现为一组抽象构件及构件实例间交互的方法; (应用方面)  
框架是可被应用开发者定制的应用骨架。(目的方面)  
* 特点:
  * 一个框架是一个可复用的设计构件,通常以构件库的形式出现，一般是不断升级的  
  * 可重用设计，表现为一组抽象类以及其实例之间协作的方法  
* 为什么使用框架:  
解决技术整合的问题,将软件企业的研发将集中在应用的设计上，而不是具体的技术实现  
  
#### 总结：  
框架是软件，而架构不是软件。  
框架是针对系统设计的一个“半成品”软件，架构是将系统决策分为不同的部分、决定如何交互，是一个针对软件设计的决策。
架构比具体代码高一个层次，是一个抽象概念。  
架构决策体现在框架之中，都是为了解决复杂软件系统的实现而分而治之的结果。  


### 以你的项目为案例 
#### 绘制三层架构模型图，细致到分区  
<img src="https://github.com/YitingKikyo/YitingKikyo.github.io/blob/master/_post/SystemAnalysis/pictures/81.png" width="75%">  
  
#### 结合你程序的结构，从程序员角度说明三层架构给开发者带来的便利  
### 研究 VUE 与 Flux 状态管理的异同