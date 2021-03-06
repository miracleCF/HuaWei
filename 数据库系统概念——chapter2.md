# 数据库系统概念——chapter2

### 关系模型

**数据模型**是描述数据、数据联系、数据语义以及一致性约束的概念工具的集合。

**关系模型**利用表的集合来表示数据和数据间的联系，关系模型在逻辑层和视图层描述数据。

### 两个问题：

- 如何说明对数据的查询和更新请求
- 数据完整性和数据保护

### 关系数据库的结构：

关系数据库由表的集合组成。

**关系**——表

**元组**——行

**属性**——列

对于每一列，也就是每个属性，它的取值都有一个取值集合，也就是该属性的**域**。对于一个关系，要去所有的属性的域是原子的（即不可再分）。null值是一个特殊的值，表示值未知或不存在。

### 数据库模式

数据库模式：数据库的逻辑设计

数据库实例：给定时刻数据库中数据的快照

关系模式：属性序列+属性的域（对应程序设计语言中的类型）

关系实例：一个关系的特定实例，也就是一组行（对应程序设计语言的值）

### 码

一个关系中不同元组用属性值进行区分，一个关系中没有两个元组属性值相同

超码：一个或多个属性的集合，超码可以唯一标识一个元组。

候选码：最小超码，它的任意真子集都不能成为超码

主码：被数据库设计者选中的候选码

外码：关系模式r1包含关系模式r2的主码

参照完整性约束：参照关系中特点元组在外码的属性取值必然等于被参照关系某个元组的特定属性的取值

### 关系运算

运算施加于一个或一对关系上，运算结果是单个关系。

常见关系运算：

- 从单个关系中选出满足特定关系谓词的元组
- 从单个关系中选出特定的属性
- 自然连接
- 笛卡尔积

### 关系代数

- 选择（σ）
- 投影（π）
- 自然连接（⋈）
- 笛卡尔积（×）
- 并（∪）
- 差（−）
- 交（∩）
- 除（÷）
