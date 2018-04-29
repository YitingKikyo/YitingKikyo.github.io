## 系统分析与设计hw5   
### 领域建模  
* **a. 阅读 Asg_RH 文档，按用例构建领域模型。**
  * 按 Task2 要求，请使用工具 UMLet，截图格式务必是 png 并控制尺寸  
  * 说明：请不要受 PCMEF 层次结构影响。你需要识别实体（E）和 中介实体（M，也称状态实体）  
    * 在单页面应用（如 vue）中，E 一般与数据库构建有关， M 一般与 store 模式 有关  
    * 在 java web 应用中，E 一般与数据库构建有关， M 一般与 session 有关  
<img src="https://github.com/YitingKikyo/YitingKikyo.github.io/blob/master/_post/SystemAnalysis/pictures/511.png" width="70%">  

* **b. 数据库建模(E-R 模型)**  
-按 Task 3 要求，给出系统的 E-R 模型（数据逻辑模型）  
-建模工具 PowerDesigner（简称PD） 或开源工具 OpenSystemArchitect  
-不负责的链接 http://www.cnblogs.com/mcgrady/archive/2013/05/25/3098588.html  
-导出 Mysql 物理数据库的脚本  
-简单叙说 数据库逻辑模型 与 领域模型 的异同  
<img src="https://github.com/YitingKikyo/YitingKikyo.github.io/blob/master/_post/SystemAnalysis/pictures/521.png" width="60%">   
   
导出的Mysql物力数据库脚本为：  
```
if exists(select 1 from sys.sysforeignkey where role='FK_CUSTOMER_RELATIONS_RESERVAT') then
    alter table Customer
       delete foreign key FK_CUSTOMER_RELATIONS_RESERVAT
end if;

if exists(select 1 from sys.sysforeignkey where role='FK_CUSTOMER_CHOOSE_HOTEL') then
    alter table Customer
       delete foreign key FK_CUSTOMER_CHOOSE_HOTEL
end if;

if exists(select 1 from sys.sysforeignkey where role='FK_HOTEL_HAS_ROOM') then
    alter table Hotel
       delete foreign key FK_HOTEL_HAS_ROOM
end if;

if exists(select 1 from sys.sysforeignkey where role='FK_RESERVAT_RELATIONS_ROOM') then
    alter table Reservation
       delete foreign key FK_RESERVAT_RELATIONS_ROOM
end if;

drop index if exists Customer.Customer_PK;

drop table if exists Customer;

drop index if exists Hotel.choose_FK;

drop index if exists Hotel.Hotel_PK;

drop table if exists Hotel;

drop index if exists Reservation.Relationship_2_FK;

drop index if exists Reservation.Reservation_PK;

drop table if exists Reservation;

drop index if exists Room.Relationship_4_FK;

drop index if exists Room.has_FK;

drop index if exists Room.Room_PK;

drop table if exists Room;

/*==============================================================*/
/* Table: Customer                                              */
/*==============================================================*/
create table Customer 
(
   "customer full name" char(10)                       not null,
   "hotel name"         char(10)                       null,
   "reservation id"     integer                        null,
   "email address"      char(20)                       null,
   constraint PK_CUSTOMER primary key ("customer full name")
);

/*==============================================================*/
/* Index: Customer_PK                                           */
/*==============================================================*/
create unique index Customer_PK on Customer (
"customer full name" ASC
);

/*==============================================================*/
/* Table: Hotel                                                 */
/*==============================================================*/
create table Hotel 
(
   "hotel name"         char(10)                       not null,
   "room id"            integer                        null,
   description          char(256)                      null,
   constraint PK_HOTEL primary key ("hotel name")
);

/*==============================================================*/
/* Index: Hotel_PK                                              */
/*==============================================================*/
create unique index Hotel_PK on Hotel (
"hotel name" ASC
);

/*==============================================================*/
/* Index: choose_FK                                             */
/*==============================================================*/
create index choose_FK on Hotel (
"hotel name" ASC
);

/*==============================================================*/
/* Table: Reservation                                           */
/*==============================================================*/
create table Reservation 
(
   "reservation id"     integer                        not null,
   "room id"            integer                        null,
   "hotel name"         char(10)                       null,
   "check in date"      char(10)                       null,
   "check out date"     char(10)                       null,
   constraint PK_RESERVATION primary key ("reservation id")
);

/*==============================================================*/
/* Index: Reservation_PK                                        */
/*==============================================================*/
create unique index Reservation_PK on Reservation (
"reservation id" ASC
);

/*==============================================================*/
/* Index: Relationship_2_FK                                     */
/*==============================================================*/
create index Relationship_2_FK on Reservation (
"reservation id" ASC
);

/*==============================================================*/
/* Table: Room                                                  */
/*==============================================================*/
create table Room 
(
   "room id"            integer                        not null,
   type                 char(10)                       null,
   price                integer                        null,
   avalibility          smallint                       null,
   constraint PK_ROOM primary key ("room id")
);

/*==============================================================*/
/* Index: Room_PK                                               */
/*==============================================================*/
create unique index Room_PK on Room (
"room id" ASC
);

/*==============================================================*/
/* Index: has_FK                                                */
/*==============================================================*/
create index has_FK on Room (
"room id" ASC
);
/*==============================================================*/
/* Index: Relationship_4_FK                                     */
/*==============================================================*/
create index Relationship_4_FK on Room (
"room id" ASC
);

alter table Customer
   add constraint FK_CUSTOMER_RELATIONS_RESERVAT foreign key ("reservation id")
      references Reservation ("reservation id")
      on update restrict
      on delete restrict;

alter table Customer
   add constraint FK_CUSTOMER_CHOOSE_HOTEL foreign key ("hotel name")
      references Hotel ("hotel name")
      on update restrict
      on delete restrict;

alter table Hotel
   add constraint FK_HOTEL_HAS_ROOM foreign key ("room id")
      references Room ("room id")
      on update restrict
      on delete restrict;

alter table Reservation
   add constraint FK_RESERVAT_RELATIONS_ROOM foreign key ("room id")
      references Room ("room id")
      on update restrict
      on delete restrict;
```  
  
#### 数据库逻辑模型 与 领域模型 的异同 :  
#### 数据库逻辑模型：  
数据库逻辑模型就是把概念结构设计阶段设计好的E-R模型转换为与选用的DBMS产品所支持的逻辑结构。   
##### 逻辑模型描述的是对用户需求在技术上的实现方法  
   
##### 设计步骤：  
* 将概念结构转换为一般的关系、网状、层次模型  
* 将转换来的关系、网状、层次模型向特定 DBMS 支持下的数据模型转换  
* 对数据模型进行优化  
  
#### 领域模型：  
领域模型又称概念模型，主要是关注领域本身，并且建立领域之间的关系。  
领域之间的关系一般有泛化，依赖和关联。关联有一般关联，聚合和组合。  
在需求分析时，领域模型一般来自于业务描述中的名词和对名词的抽象。  
（但是不一定所有名词都是模型，可能是模型的属性，角色或跟业务无关的描述。）  
##### 领域模型描述的是业务中涉及到的业务实体以及相互之间的关系  
  
##### 设计步骤: 
* 从业务需求描述中，提取所有名词，一般时间地点可以除外  
* 分析名词，提取出实体，分析名词中的属性、实体、实例，形成操作实体集合  
* 从业务实体集合中抽象领域模型  
* 用UML提供的方法和图例进行领域模型设计，确定模型之间的关系   
