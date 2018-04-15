## Tools use -- UMLet  
### 简介
UMLet是一款具有简单的用户界面，免费且开源的UML建模工具。  
它能够快速的构建UML序列图，活动图等，并且可以将原型导出为eps，pdf，jpg，svg等格式。  
我们还可以在Eclipse下面创建自定义的元素。UMLet既可以鼓励运行，还可以作为Eclipse的插件运行在Windows，OS X和Linux平台上。  

### 下载
[UMLet下载地址](http://www.umlet.com/changes.htm)  
  
### 安装  
* 下载独立版本  
* 解压，双击UMLet.jar（你需要配置好java）  
* 打开即时使用  

### 使用  
![打开的界面](https://github.com/YitingKikyo/YitingKikyo.github.io/blob/master/_post/SystemAnalysis/pictures/umletStart.png)  

* 分区一：右上的UML Use Case，元素选取区，在这个区域里有下拉列表，可以很方便的选择。双击可以直接添加到分区三，也可以拖动到分区三。
* 分区二：右下的propertices，元素设置区，在区域一中选中元素，在此区域中可以进行详细的更改。  
* 分区三：左边的new，画图区，在这个区域里进行图形的制作操作。  
  
### 用例图  
#### 简介  
用例图是指由参与者（Actor）、用例（Use Case），边界以及它们之间的关系构成的用于描述系统功能的视图。  
用例图（User Case）是外部用户（被称为参与者）所能观察到的系统功能的模型图。用例图是系统的蓝图。  
用例图呈现了一些参与者，一些用例，以及它们之间的关系，主要用于对系统、子系统或类的功能行为进行建模。   
  
#### 结构  
一个用例图是一个包括参与者、由系统边界（一个矩形）封闭的一组用例、参与者和用例之间的关联、用例间的联系以及参与者的泛化等的图。  
<img src="https://github.com/YitingKikyo/YitingKikyo.github.io/blob/master/_post/SystemAnalysis/pictures/All.png" width="45%"/>

* 参与者：也叫动作者，表示系统用户能扮演的角色(role) 。  
&emsp;&emsp;&emsp;这些用户可能是人，可能是其他的计算机，一些硬件或者甚至是其它软件系统。  
&emsp;&emsp;&emsp;参与者不是指人或事物本身，而是表示人或事物当时所扮演的角色。比如小明是图书馆的管理员。
&emsp;&emsp;&emsp;*如上图的顾客、管理者等*
  
 * 系统边界：是用来表示正在建模系统的边界。边界内表示系统的组成部分，边界外表示系统外部。  的
&emsp;&emsp;&emsp;系统边界在画图中方框来表示，同时附上系统的名称，参与者画在边界的外面，用例画在边界里面。
&emsp;&emsp;&emsp;*如上图的方框 * 
  
* 用例：用例是系统中的一个功能单元，可以被描述为参与者与系统之间的一次交互作用。 
&emsp;&emsp;&emsp;表示处于同一系统中的参与者和用例之间的关系的图，称之为用例图，目的是显示哪个参与者参与了哪个用例的执行。 
&emsp;&emsp;&emsp;*如上图的椭圆圈*  
  
* 关系：常见关系类型有包含（Include）、扩展（Extend）和泛化（Generalization）。  
&emsp;&emsp;&emsp; **包含：**可以把几个用例的公共步骤分离出来成为一个单独的被包含用例。类似c语言中的include。如上图所示，查询员工信息即是分离出来的被包&emsp;&emsp;&emsp;含用例。  
&emsp;&emsp;&emsp;**扩展：**扩展关系是从扩展用例到基本用例的关系，它说明为扩展用例定义的行为如何插入到为基本用例定义的行为中。  
&emsp;&emsp;&emsp;它是以隐含形式插入的，也就是说，扩展用例并不在基本用例中显示。在以下几种情况下，可使用扩展用例：  
&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;a.表明用例的某一部分是可选的系统行为（这样，您就可以将模型中的可选行为和必选行为分开）；  
&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;b.表明只在特定条件（如例外条件）下才执行的分支流；  
&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;所插入的行为段和插入的顺序取决于在执行基本用例时与主角进行的交互。  
&emsp;&emsp;&emsp; *如上图的虚线带箭头的extents*   
  
&emsp;&emsp;&emsp;**泛化：**泛化和类中的泛化概念是一样的，子用例继承父用例的行为和含义，还可以增加或覆盖父用例的行为。  
&emsp;&emsp;&emsp;子用例可以出现在任何父用例出现的位置（父和子均有具体的实例）。

