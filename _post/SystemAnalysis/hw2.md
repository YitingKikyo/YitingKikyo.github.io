# 15331122 黄依婷 Hw2

# 1、简答题  
## 简述瀑布模型、增量模型、螺旋模型（含原型方法）的优缺点。  

* 瀑布模型：  
> ### 优点：
> 1. 有利于大型软件开发过程中人员的组织、管理，有利于软件开发方法和工具的研究，从而提高了大型软件项目开发的质量和效率。  
> 2. 定义了软件开发基本流程与活动  
>    创意阶段：描述问题，市场，关键技术等  
>    分析阶段：用户故事、领域模型、业务流程等  
> ......  
>（前提假设：需求是明确的，在短期内可获取，每个阶段是无差错的）
- - - 
> ### 缺点：
> 依赖问题：前面需求模糊，后面工作…  
> 容错问题：在后期发现需求问题，工作量难接受  
> 资源调配问题：知识技能需求不同、人员数量要求不同  
> 现象：延期，项目不可控  
![瀑布模型](https://github.com/YitingKikyo/YitingKikyo.github.io/blob/master/_post/SystemAnalysis/waterfall.png)

              
* 增量模型：优点：人员分配灵活，刚开始不用投入大量人力资源；
               如果核心产品很受欢迎，则可增加人力实现下一个增量；
               可先发布部分功能给客户，对客户起到镇静剂的作用。
         缺点：行开发构件有可能遇到不能集成的风险，软件必须具备开放式的体系结构；
               增量模型的灵活性可以使其适应这种变化的能力大大优于瀑布模型和快速原型模型，但也很容易退化为边做边改模型，从而使软件过程的控制失去整体性
               
* 螺旋模型：优点：设计上的灵活性,可以在项目的各个阶段进行变更；
               以小的分段来构建大型系统,使成本计算变得简单容易；
               客户始终参与每个阶段的开发,保证了项目不偏离正确方向以及项目的可控性；
               随着项目推进,客户始终掌握项目的最新信息 , 从而他或她能够和管理层有效地交互。 
         缺点：采用螺旋模型需要具有相当丰富的风险评估经验和专门知识，在风险较大的项目开发中，如果未能够及时标识风险，势必造成重大损失；
               过多的迭代次数会增加开发成本，延迟提交时间。

## 简述 UP 的三大特点，其中哪些内容体现了用户驱动的开发，哪些内容体现风险驱动的开发？
三大特点：
(1)用例驱动（Use Case Driven）
(2)以架构为中心的（Architecture Centric）
(3)受控的迭代式增量开发（Iterative and Evolutionary）
其中，1、3体现用户驱动开发，2体现风险驱动开发

## UP 四个阶段的划分准则是什么？关键的里程碑是什么？
先启阶段：获得项目的基础；生命周期目标
精化阶段：迭化系统构架；生命周期构架
构建阶段：构造软件；初始运作功能
移交阶段：把软件部署到用户环境；产品发布

## IT 项目管理中，“工期、质量、范围/内容” 三个元素中，在合同固定条件下，为什么说“范围/内容”是项目团队是易于控制的?
在合同中，工期是事先规定好的，是不可更改的，客户在合同中也规定了项目的验收条件，所以是项目团队不易于控制的。
范围、内容可以根据遇到的内容和工期的实际情况做适量的调整，是属于易于控制的。

## 为什么说，UP 为企业按固定节奏生产、固定周期发布软件产品提供了依据？
UP划分为四个阶段，每个阶段都有各自的里程碑，而只有完成本阶段的里程碑的条件才能进入下一个阶段，因此是固定节奏生产的。
在每个阶段中，UP可以进行多次迭代，每次迭代可以发布，因此为固定周期发布提供了依据。