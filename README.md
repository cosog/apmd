# 油气生产敏捷计算分析系统V7.1

[toc]

# 第1章 系统介绍

## 1.1 系统概述

《油气生产敏捷计算分析系统V7.1》主要在采集、控制的基础上，侧重油水井智能分析。模块主要包括实时评价、全天评价、生产报表、图形查询等。系统应用大数据分析方法，对工况、产量、时率、平衡、能耗等生产关键指标进行统计分析，及时发现生产不正常井，挖掘生产潜力井，提升对目标区块和单井的管控能力。  
该系统应用新的技术框架与云计算语言，打通采集、井场计算、传输、云计算、大数据分析应用的生态链。通过智能算法的合理分布、智能分权，简化系统的复杂性、提升系统的工程性，实现一套框架，完整的生态链产品。

![](https://github.com/cosog-chentr/apmd/blob/master/Image/PNG/001.png?raw=true)

## 1.2 环境要求

**1、Web服务器**  
CPU：4核或以上  
内存：8G或以上  
硬盘：500G或以上  
操作系统：建议Windows server 2012 64位  
数据库：Oracle 11g或以上  
JDK：8.0或以上  
Tomcat:9.0或以上

**2、云计算服务器**

CPU：4核或以上  
内存：8G或以上  
硬盘：80G或以上  
操作系统：建议Ubuntu server 16.04或以上

## 1.3 驱动说明

**1、中石油标准**  
支持中石油标准驱动及拓展驱动  
**2、中石化标准**  
支持中石化标准驱动及拓展驱动

## 1.4 授权说明

本软件适用于Windows、Linux、Mac64位及32位操作系统，请在购买时注明所需部署机器的版本型号、IP地址以及网卡物理地址。

## 1.5 公有云访问

系统访问地址：**http://39.98.134.121:16100/ap**

# 第2章 应用介绍

## 3.1 用户登录

本地服务器：**http://ip:16100/ap**  
用户名：system  
密码：123456

公有云服务器：**http://39.98.134.121:16100/ap**  
用户名、密码请咨询我们公司

浏览器要求：建议谷歌浏览器、360浏览器极速模式、IE9以上版本

![](https://github.com/cosog-chentr/apmd/blob/master/Image/PNG/002.png?raw=true)


# 3.2 页面布局

1、banner区：包括修改密码、退出、帮助及全屏按钮；  
2、功能导航区：系统各主功能模块；  
3、组织导航区：用户组织结构；  
4、统计区：井信息统计图表；  
5、单井数据区：单井分析、采集及控制详细信息。  
通过点击界面中缝位置的图标可实现界面伸缩。

![](https://github.com/cosog-chentr/apmd/blob/master/Image/PNG/003.png?raw=true)

![](https://github.com/cosog-chentr/apmd/blob/master/Image/GIF/001.gif?raw=true)

## 3.3 实时评价

根据油水井的动静态数据对单井进行实时评价。

### 3.3.1 统计

统计主标签：包括工况、产量、平衡、时率、效率、电量、通信；  
统计子标签：各主标签包含的子项，如平衡包括电流平衡和功率平衡；  
统计表/图：根据选择的各主标签、子标签显示相关统计信息。

![](https://github.com/cosog-chentr/apmd/blob/master/Image/PNG/004.png?raw=true)

### 3.3.2 目标井

如需查看某一类目标价的具体信息时，如游动凡尔失灵，可：  
1、点击统计图中“游动凡尔失灵”对应的饼或标签；  
2、统计表中显示该组织下的所有“游动凡尔失灵”井；  
3、右侧单井详情中显示该井的详细信息；  
4、选择一行后点击“查看历史”或双击该行可查看该井的历史信息。

![](https://github.com/cosog-chentr/apmd/blob/master/Image/PNG/005.png?raw=true)

### 3.3.3 单井数据

包括图形及分析、采集、控制。

![](https://github.com/cosog-chentr/apmd/blob/master/Image/PNG/006.png?raw=true)

#### 3.3.3.1 图形

**1、地面功图**  
（1）功图采集时间  
例如：2019-01-22 08:39:56  
（2）上理论载荷线  
上理论载荷=活塞以上液柱载荷+抽油杆在液柱中的载荷  
（3）下理论载荷线  
下理论载荷=抽油杆在液柱中的载荷  
（4）最大载荷  
功图最大载荷  
（5）最小载荷  
功图最小载荷

**2、泵功图**  
从上至下依次为：  
（1）地面功图  
（2）二级杆顶端功图  
（3）泵功图

**3、杆柱应力**  
根据杆柱组合，分析各级杆柱的受力情况，判断杆柱组合是否合理。  
（1）一级杆顶端应力百分比  
（2）二级杆顶端应力百分比  

$\frac 应力百分比={最大应力}{许用应力}$

**4、泵效组成**  
泵的实际排量与泵的理论排量之比的百分数称为泵效。