## 系统分析与设计作业4  
### 1、 用例建模  
#### a. 阅读 Asg_RH 文档，绘制用例图。 按 Task1 要求，请使用工具 UMLet，截图格式务必是 png 并控制尺寸 
<img src="https://github.com/YitingKikyo/YitingKikyo.github.io/blob/master/_post/SystemAnalysis/pictures/reverse%20hotel.png" width= "70%">  
  
#### b. 选择你熟悉的定旅馆在线服务系统（或移动 APP），如绘制用例图。并满足以下要求:  
##### &emsp;- 对比 Asg_RH 用例图，请用色彩标注出创新用例或子用例  
##### &emsp;- 尽可能识别外部系统，并用色彩标注新的外部系统和服务  
选择的定旅馆在线服务系统为 **飞猪** ：  
<img src="https://github.com/YitingKikyo/YitingKikyo.github.io/blob/master/_post/SystemAnalysis/pictures/feizhu.png" width="70%">  

#### c. 对比两个时代、不同地区产品的用例图，总结在项目早期，发现创新的思路与方法  
1.  随着科技的进步，人们的需求也不断的在产生更大的变化，我们要走在科技前沿或者紧跟科技的步伐，运用最新的能为人们所用的科技设计创新的功能。  
2.  飞猪增加了定位、收藏、价格预估、最近浏览等功能列表，这个更贴近了人们的生活，获取了许多的方便，所以，满足顾客的需求，站在顾客的角度，以方便出发是个不错的选择。   
#### d. 请使用 SCRUM 方法，在（任务b）用例图基础上，编制某定旅馆开发的需求 （backlog）  

| 模块 | 实现 | 备注 |
| :----: | :----: | :----: |
| 选择酒店 | 选择位置、入住时间、离开时间、关键字，点击选择 | 关键字选填 | 
| 预定酒店 | 打开购物车/最近浏览/收藏，点击预定 | 可能会下架/已经被预定 | 
| 确认订单 | 填写预订人的信息 | 查看明细 |
| 支付订单 | 选择付款方式，输入密码 | 可以代付/余额或许不足 |  
  
### 2、业务建模  
#### a. 在（任务b）基础上，用活动图建模找酒店用例。简述利用流程图发现子用例的方法。  
<img src="https://github.com/YitingKikyo/YitingKikyo.github.io/blob/master/_post/SystemAnalysis/pictures/hw421.png" width="45%">  
  
##### 利用流程图发现子用例的方法:  
当流程图出现分支开始，沿着分支从开始到结束就是子用例。  
  
#### b. 选择你身边的银行 ATM，用活动图描绘取款业务流程  
<img src="https://github.com/YitingKikyo/YitingKikyo.github.io/blob/master/_post/SystemAnalysis/pictures/hw422.png" width="25%">  
  
#### **c. 查找淘宝退货业务官方文档，使用多泳道图，表达客户、淘宝网、淘宝商家服务系统、商家等用户和系统协同完成退货业务的过程。分析客户要完成退货业务，在淘宝网上需要实现哪些系统用例**     
<img src="https://github.com/YitingKikyo/YitingKikyo.github.io/blob/master/_post/SystemAnalysis/pictures/hw423.png">  
  
##### 客户要完成退货业务，在淘宝网上需要实现哪些系统:  
生成退款单、管理退款单、同意退款、不同意退款处理。  
  
### 3、用例文本编写  
#### 在大作业基础上，分析三种用例文本的优点和缺点  
##### 优点：  
 1.简洁、直观。不用用用例描述，系统交互行为很清晰地用图形表达出来。  
 2.规范、易理解。UML图不依赖开发语言，且使用有规范，使用的人都能清楚的了解别人的表达。  
 3.需求与设计分离。用例图没有包括具体的实现，是需求和设计分离的。  
##### 缺点：  
 1.不能表达非功能需求。用例图可以详细流畅的表达客户的需求，但是对于可靠性功能性这些非功能需求却不能表现出来。  
 2.对不懂UML的客户或程序员来说难以理解。用例图的每个符号/图形（例如小人、Notes、虚线箭头）都有自己的意思或者与其他元素的关系，对于不懂规范的人来说可能不能了解的很清楚。  
