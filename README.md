# 《油气生产敏捷计算分析系统V7.1》用户手册

- [第一章 系统介绍](README.md#第一章-系统介绍)
    - [1.1 系统概述](README.md#11-系统概述)
    - [1.2 环境要求](README.md#12-环境要求)
    - [1.3 驱动说明](README.md#13-驱动说明)
    - [1.4 授权说明](README.md#14-授权说明)
- [第二章 应用介绍](README.md#第二章-应用介绍)  
    - [2.1 用户登录](README.md#21-用户登录)
    - [2.2 页面布局](README.md#22-页面布局)
    - [2.3 实时评价](README.md#23-实时评价)
      - [2.3.1 统计](README.md#231-统计)
      - [2.3.2 目标井](README.md#232-目标井)
      - [2.3.3 单井数据](README.md#233-单井数据)
    - [2.4 全天评价](README.md#24-全天评价)
    - [2.5 生产报表](README.md#25-生产报表)
    - [2.6 图形查询](README.md#26-图形查询)
    - [2.7 权限管理](README.md#27-权限管理)
      - [2.7.1 单位管理](README.md#271-单位管理)
      - [2.7.2 用户管理](README.md#272-用户管理)
      - [2.7.3 角色管理](README.md#273-角色管理)  
    - [2.8 数据配置](README.md#28-数据配置)  
      - [2.8.1 井名信息](README.md#281-井名信息)  
      - [2.8.2 生产数据](README.md#282-生产数据)  
      - [2.8.3 采控配置](README.md#283-采控配置)  
      - [2.8.4 计算维护](README.md#284-计算维护) 
    - [2.9 系统配置](README.md#29-系统配置)  
      - [2.9.1 模块配置](README.md#291-模块配置) 
      - [2.9.2 字典配置](README.md#292-字典配置) 
      - [2.9.3 统计配置](README.md#293-统计配置) 
      - [2.9.4 报警配置](README.md#294-报警配置) 

# 第一章 系统介绍

## 1.1 系统概述

&emsp;&emsp;《油气生产敏捷计算分析系统V7.1》主要在采集、控制的基础上，侧重油水井智能分析。模块主要包括实时评价、全天评价、生产报表、图形查询等。系统应用大数据分析方法，对工况、产量、时率、平衡、能耗等生产关键指标进行统计分析，及时发现生产不正常井，挖掘生产潜力井，提升对目标区块和单井的管控能力。  
&emsp;&emsp;该系统应用新的技术框架与云计算语言，打通采集、井场计算、传输、云计算、大数据分析应用的生态链。通过智能算法的合理分布、智能分权，简化系统的复杂性、提升系统的工程性，实现一套框架，完整的生态链产品。

## 1.2 环境要求

**1.Web服务器**  
>- CPU：2核及以上  
>- 内存：8G及以上  
>- 硬盘：500G及以上  
>- 操作系统：建议Windows server 2012 64位及以上  
>- 数据库：Oracle 11g及以上  
>- JDK：8.0及以上  
>- Tomcat:9.0及以上

**2.云计算服务器**

>- CPU：2核及以上  
>- 内存：8G及以上  
>- 硬盘：80G及以上  
>- 操作系统：建议Ubuntu server 16.04及以上

## 1.3 驱动说明

**1.中石油标准**  
&emsp;&emsp;支持中石油A11标准及拓展驱动  
**2.中石化标准**  
&emsp;&emsp;支持中石化“四化”标准及拓展驱动

## 1.4 授权说明

&emsp;&emsp;系统适用于Windows、Linux、Mac 64位及32位操作系统，请在购买时注明所需部署机器的版本型号、IP地址以及网卡物理地址。

# 第二章 应用介绍

## 2.1 用户登录

&emsp;&emsp;本地：**http://IP:16100/ap**  
&emsp;&emsp;用户名：system  
&emsp;&emsp;密码：123456

&emsp;&emsp;公有云：**http://39.98.134.121:16100/ap**  
&emsp;&emsp;用户名、密码请咨询本公司

&emsp;&emsp;**浏览器要求：建议谷歌浏览器、360浏览器极速模式、IE9以上版本**

![登录首页](./Image/PNG/002.png?raw=true)


## 2.2 页面布局

>1. banner区：包括修改密码、退出、帮助及全屏按钮；  
>2. 功能导航区：系统各主功能模块；  
>3. 组织导航区：用户组织结构；  
>4. 统计区：井信息统计图表；  
>5. 单井数据区：单井分析、采集及控制详细信息。

&emsp;&emsp;通过点击界面中缝位置的图标![伸缩按钮](https://github.com/cosog-chentr/apmd/blob/master/Image/PNG/025.png?raw=true)或![伸缩按钮](https://github.com/cosog-chentr/apmd/blob/master/Image/PNG/026.png?raw=true)可实现界面伸缩。

![页面布局](https://github.com/cosog-chentr/apmd/blob/master/Image/PNG/003.png?raw=true)

![列表伸缩](https://github.com/cosog-chentr/apmd/blob/master/Image/GIF/001.gif?raw=true)

## 2.3 实时评价

&emsp;&emsp;根据油井的动静态数据对单井进行实时评价。

### 2.3.1 统计

>1. 统计主标签：包括工况、产量、平衡、时率、效率、电量、通信；  
>2. 统计子标签：各主标签包含的子项，如平衡包括电流平衡和功率平衡；  
>3. 统计表/图：根据选择的主标签、子标签显示相关统计信息。

![统计](https://github.com/cosog-chentr/apmd/blob/master/Image/PNG/004.png?raw=true)

### 2.3.2 目标井

&emsp;&emsp;如需查看某一类目标井的具体信息时，例如游动凡尔失灵，  
>1. 点击统计图中“游动凡尔失灵”对应的饼或标签；  
>2. 统计表中显示该组织下的所有“游动凡尔失灵”井；  
>3. 右侧单井详情中显示该井的详细信息；  
>4. 选择一行后点击**查看历史**或**双击**该行可查看该井的历史信息。

![目标井](https://github.com/cosog-chentr/apmd/blob/master/Image/PNG/005.png?raw=true)

### 2.3.3 单井数据

&emsp;&emsp;包括图形及分析、采集、控制。

![单井数据](https://github.com/cosog-chentr/apmd/blob/master/Image/PNG/006.png?raw=true)

#### 2.3.3.1 图形

**1. 地面功图**  
> （1）功图采集时间  
&emsp;&emsp;例如：2019-01-22 08:39:56  
> （2）上理论载荷线  
&emsp;&emsp;上理论载荷=活塞以上液柱载荷+抽油杆在液柱中的载荷  
> （3）下理论载荷线  
&emsp;&emsp;下理论载荷=抽油杆在液柱中的载荷  
> （4）最大载荷  
&emsp;&emsp;功图最大载荷  
> （5）最小载荷  
&emsp;&emsp;功图最小载荷  

![地面功图](https://github.com/cosog-chentr/apmd/blob/master/Image/PNG/027.png?raw=true) 

**2. 泵功图**  
&emsp;&emsp;从上至下依次为：  
> （1）地面功图  
> （2）二级杆顶端功图  
> （3）泵功图  

![泵功图](https://github.com/cosog-chentr/apmd/blob/master/Image/PNG/028.png?raw=true)

**3. 杆柱应力**  
&emsp;&emsp;根据杆柱组合，分析各级杆柱的受力情况，判断杆柱组合是否合理。  
> （1）一级杆顶端应力百分比  
> （2）二级杆顶端应力百分比  
> （3）应力百分比=最大应力/许用应力  

![杆柱应力图](https://github.com/cosog-chentr/apmd/blob/master/Image/PNG/029.png?raw=true)

**4. 泵效组成**  
&emsp;&emsp;泵的实际排量与泵的理论排量之比的百分数称为泵效。

![泵效组成图](https://github.com/cosog-chentr/apmd/blob/master/Image/PNG/030.png?raw=true)

**5. 电流平衡度**

&emsp;&emsp;电流平衡度计算：  
&emsp;&emsp;电流平衡度=下冲程电流最大值/上冲程电流最大值  
![电流图](https://github.com/cosog-chentr/apmd/blob/master/Image/PNG/031.png?raw=true)

**6. 功率平衡度**

&emsp;&emsp;电功图是电的有功功率图，功率平衡度计算：  
&emsp;&emsp;功率平衡度=下冲程有功功率最大值/上冲程有功功率最大值  
![电功图](https://github.com/cosog-chentr/apmd/blob/master/Image/PNG/032.png?raw=true)

#### 2.3.3.2 分析

&emsp;&emsp;显示计算分析结果参数及曲线，包括产量构成、泵效、系统效率、泵出入口参数等。

![分析](https://github.com/cosog-chentr/apmd/blob/master/Image/PNG/007.png?raw=true)

#### 2.3.3.3 采集

&emsp;&emsp;显示传感器采集数据及曲线，包括通信状态、运行状态、油（套）压、电参数等。

![采集](https://github.com/cosog-chentr/apmd/blob/master/Image/PNG/008.png?raw=true)

#### 2.3.3.4 控制

&emsp;&emsp;井场视频显示及设备控制，**支持数字化抽油机平衡控制和频率控制**。

![控制](https://github.com/cosog-chentr/apmd/blob/master/Image/PNG/009.png?raw=true)

## 2.4 全天评价

&emsp;&emsp;根据全天的采集数据与分析结果对单井进行全天评价。

![统计](https://github.com/cosog-chentr/apmd/blob/master/Image/PNG/010.png?raw=true)  

![目标井](https://github.com/cosog-chentr/apmd/blob/master/Image/PNG/011.png?raw=true)

## 2.5 生产报表

![生产报表](https://github.com/cosog-chentr/apmd/blob/master/Image/PNG/013.png?raw=true)

## 2.6 图形查询

&emsp;&emsp;默认显示所有井最新地面功图，选择某一口井显示该井历史地面功图。

![图形查询](https://github.com/cosog-chentr/apmd/blob/master/Image/PNG/014.png?raw=true)

## 2.7 权限管理

&emsp;&emsp;系统部署完成后需要新建单位、用户并划分权限。

### 2.7.1 单位管理

1. 使用系统管理员账号登录系统。  
2. 进入**单位管理**模块创建单位组织。如模拟油田公司—模拟采油厂—四矿。  
3. 点击![创建按钮](https://github.com/cosog-chentr/apmd/blob/master/Image/PNG/015.png?raw=true)，创建模拟油田公司；填写完成后，点击![保存按钮](https://github.com/cosog-chentr/apmd/blob/master/Image/PNG/016.png?raw=true)，完成创建。  
>- 上级单位：由于模拟油田公司为根节点，上级单位不选择；  
>- 单位类别：按实际选择，局级；  
>- 单位名称：模拟油田公司；  
>- 单位编码、单位级别：确定上级单位、单位类别后自动生成；  
>- 单位说明：可不填写。  
4. 点击![](https://github.com/cosog-chentr/apmd/blob/master/Image/PNG/015.png?raw=true)，创建模拟采油厂；填写完成后，点击![](https://github.com/cosog-chentr/apmd/blob/master/Image/PNG/016.png?raw=true)，完成创建。  
>- 上级单位：已创建根节点，选择模拟油田公司；  
>- 单位类别：按实际选择，厂级；
>- 单位名称：模拟采油厂。  
5. 依次完成各级单位组织创建。

![创建模拟油田公司](https://github.com/cosog-chentr/apmd/blob/master/Image/GIF/002.gif?raw=true)  

![创建模拟采油厂](https://github.com/cosog-chentr/apmd/blob/master/Image/GIF/003.gif?raw=true)

### 2.7.2 用户管理

&emsp;&emsp;接下来进入**用户管理**模块，为不同的单位组织创建用户。点击![创建按钮](https://github.com/cosog-chentr/apmd/blob/master/Image/PNG/015.png?raw=true)，创建新用户；填写完成后，点击![保存按钮](https://github.com/cosog-chentr/apmd/blob/master/Image/PNG/016.png?raw=true)，完成创建。  
>- 单位名称：选择已创建的单位组织，确定组织的用户登录后，只能看到该组织及该组织的下属单位对应的信息；  
>- 角色：包括数据管理、数据分析、系统管理等，不同的角色拥有不同的权限;  
>- 用户名称、用户账号、用户密码：按实际填写;
>- 用户电话、内部邮箱：可不填写;  
>- 快捷登录：在登录界面是否可以免密登录，一般用于数据查询人员。

![创建用户](https://github.com/cosog-chentr/apmd/blob/master/Image/GIF/004.gif?raw=true)

### 2.7.3 角色管理

&emsp;&emsp;进入**角色管理**模块，创建不同的角色，通过权限授予为不同的角色设置模块访问权限。系统内置多个角色，如数据管理、数据分析、系统管理（系统管理员用户，不可修改）等。  
1. 点击![创建按钮](https://github.com/cosog-chentr/apmd/blob/master/Image/PNG/015.png?raw=true)，创建新角色。  
>- 角色名称：自定义，便于识别角色；  
>- 角色编码：自定义，用于开发人员识别，用户不会用到；  
>- 角色描述：角色具体功能描述。

2. 在右侧权限角色授予界面为新角色配置可访问的模块，点击![保存按钮](https://github.com/cosog-chentr/apmd/blob/master/Image/PNG/033.png?raw=true)，完成权限授予。 

## 2.8 数据配置

&emsp;&emsp;配置采集和计算所需的数据，包括井名信息、生产数据，可从编辑好的Excel中粘贴过来。

### 2.8.1 井名信息

#### 2.8.1.1 数据收集

>- 单位名称：井所属单位，单位管理中创建的单位名称；  
>- 区块名称：井所属区块；  
>- 井名；  
>- 举升类型：包括抽油机、螺杆泵；  
>- 驱动名称：包括A11协议、四化协议等，根据实际协议选择；  
>- 采控类型：根据该井的实际采集控制数据，选择采控配置模块中创建的类型；  
>- 设备地址：网关的MAC地址或SIM卡号码；  
>- 设备编号：网关只连接一口井时，填写01；对于丛式井，网关连接多口井时，按网关中配置的设备ID填写，如01、02、03......；  
>- 功图采集间隔：现场功图采集的时间间隔；  
>- 状态：时间是否已同步至前端设备，包括等待下发、已同步；  
>- 离散采集间隔：离散数据的采集间隔，如电流、电压等；  
>- 数据保存间隔：数据保存进数据库的时间间隔；  
>- 时率来源：DI信号（连接DI线）、电参计算（采集电参数据）、转速计算（螺杆泵井有转速数据可选择转速计算）、人工录入；  
>- 视频路径：监控视频的URL路径；  
>- 排序编号：井名在系统显示时的排序。

#### 2.8.1.2 数据录入

&emsp;&emsp;在Excel中编辑好后粘贴至井名信息模块中，可先点击导出按钮导出Excel模板。  
**注意：**  
**（1）录入时需要先在组织导航中选择录入井所在的组织，如四矿；否则会提示“请先选择组织节点”。**  
**（2）复制时序号列不要复制。**

![井名信息录入](https://github.com/cosog-chentr/apmd/blob/master/Image/GIF/005.gif?raw=true)

#### 2.8.1.3 修改井名

&emsp;&emsp;在列表中修改井名，完成后点击![修改井名按钮](https://github.com/cosog-chentr/apmd/blob/master/Image/PNG/012.png?raw=true)。  
**注意：**  
**（1）不要删除修改井，再重新录入新井，会导致历史数据丢失；**  
**（2）修改完成后，点击“修改井名”按钮，不要点击“保存”按钮。**

![修改井名](https://github.com/cosog-chentr/apmd/blob/master/Image/GIF/006.gif?raw=true)

#### 2.8.1.4 删除数据

&emsp;&emsp;选中一行或多行，右键，选择删除行，然后点击![保存按钮](https://github.com/cosog-chentr/apmd/blob/master/Image/PNG/033.png?raw=true)。

![删除数据](https://github.com/cosog-chentr/apmd/blob/master/Image/GIF/007.gif?raw=true)

### 2.8.2 生产数据

#### 2.8.2.1 数据收集

>- 生产时间：井名信息模块中**时率来源**为人工录入时填写，全天工作填写24，间抽按间抽时间填写，停井填写0；  
>- 原油密度、水密度、天然气相对密度、饱和压力、油层中部深度、油层中部温度如果没有单井数据，可以参考所在区块数据；  
>- 油压：未测油压数据可填写回压；  
>- 泵级别：1、2、3；  
>- 泵径：国标：28、32、38、44、51、57、63、70、83、95；API标准：26.99、31.8、38.1、44.5、45.2、50.8、57.2、63.5、69.9、95.3；  
>- 套管内径：生产套管内径；  
>- 抽油杆数据:  
>（1）抽油杆数据不包括光杆、泵上拉杆；  
>（2）对于某些井最后一级会有几十米的加重杆，例如外径28mm，长度50m，需收集；  
>（3）从井口到泵依次为一级杆、二级杆......，除加重杆，外径逐级减小；  
>（4）杆的总长度应接近泵挂深度；  
>（5）杆级别：包括A、B、C、D、K、KD、HL、HY；  
>（6）杆内径：空心杆填写；
>- 锚定状态：包括锚定和未锚定；抽油机井默认是未锚定；  
>- 净毛比：用于产量标定，净毛比=实际产量/软件计算产量，默认为1，一般情况不修改。对于计产疑难井（油管漏、游动凡尔漏失、固定凡尔漏失），产量差距较大时，可以调整。例如：实际产量：20t/d，软件计算产量：40t/d，净毛比可设置在0.5左右。

#### 2.8.2.2 数据录入

&emsp;&emsp;收集完成后，复制粘贴到模块中。粘贴时无需按照模块列表中井顺序调整Excel表，直接粘贴保存即可。

![生产数据录入](https://github.com/cosog-chentr/apmd/blob/master/Image/GIF/008.gif?raw=true)

### 2.8.3 采控配置

&emsp;&emsp;针对不同的设备安装情况设置不同的采集项和控制项，  
**采集项包括：**  
>- 运行状态；  
>- 生产数据：包括油压、套压、回压、井口油温、动液面、含水率；  
>- 电参数据：A/B/C相电流、A/B/C相电压、有功功耗、无功功耗、有功功率、无功功率、反向功率、功率因数；  
>- 变频数据：变频运行频率；  
>- 功图数据：采集时间、功图点数、冲次、冲程、曲线位移值、曲线载荷值、曲线电流值、曲线功率值、功图采集间隔、功图采集设置点数；  
>- 螺杆泵特有数据：转速、转矩；  
>- 平衡调节：远程调节状态。

**控制项包括：**  
>- 启停抽；  
>- 变频设备频率；  
>- 数字抽油机参数：远程调节触发控制、平衡计算方式、重心远离支点调节时间、重心接近支点调节时间、参与平衡计算冲程次数、平衡调节上限、平衡调节下限、重心远离支点每拍调节时间、重心接近支点每拍调节时间。

&emsp;&emsp;点击![创建按钮](https://github.com/cosog-chentr/apmd/blob/master/Image/PNG/015.png?raw=true)创建采控类型，如类型名称“类型一”，类型编码“type1”，类型描述“抽油机全部数据”，创建完成后，在右侧列表中勾选实际采集项和控制项，点击![保存按钮](https://github.com/cosog-chentr/apmd/blob/master/Image/PNG/033.png?raw=true)完成配置。后续在**井名信息**模块数据录入时按照单井实际采控项选择不同的采控类型。

![采控配置](https://github.com/cosog-chentr/apmd/blob/master/Image/PNG/017.png?raw=true)

### 2.8.4 计算维护

&emsp;&emsp;计算维护模块主要应用场景包括：  
>- 针对系统部署初期或现场设备安装初期，各井的生产数据并未收集或收集的不完整，在进行功图诊断及产量计算时采用了模拟数据，待后续生产数据收集完整后，需要对历史数据进行重新计算。  
>- 生产数据收集的部分数据有误，更正后需要重新计算。  
>- 在使用过程中，现场作业后并未及时更新生产数据。  
>- 其他需要对历史数据进行重新计算的情况。

**注意：**  
&emsp;&emsp;**在“生产数据”模块中修改参数只对后续的计算起作用，对已经计算完成的历史数据并不生效。如果想要对历史结果重新计算，需要在“计算维护”模块中进行。**  
&emsp;&emsp;**历史结果会被重新计算的结果覆盖。**  

&emsp;&emsp;对历史结果进行重新计算有两种方法，根据实际情况选择较为便捷的方法：  
**1. 修改数据计算**  
&emsp;&emsp;选择目标井，找到需要修改的某条记录或某个时间段的多条记录，修改完生产数据后，点击“修改数据计算”按钮进行重新计算。  
&emsp;&emsp;例如：修改S68112井，2019年2月24号全部功图采集时间的泵径数据并重新计算。  
&emsp;&emsp;操作：井名中选择S68112，时间范围选择2019-02-24至2019-02-24，列表中将泵径38mm修改为44mm，点击“修改数据计算”按钮。

![修改数据计算](https://github.com/cosog-chentr/apmd/blob/master/Image/PNG/018.png?raw=true)

**2. 关联数据计算**  
&emsp;&emsp;利用生产数据表中的最新生产数据对某口井或所有井某个时间段内的所有历史结果进行重新计算。  
（1） 单井关联数据计算  
&emsp;&emsp;例如：修改S68112井，2019年1月24日至2019年2月24日内的所有历史结果。  
&emsp;&emsp;操作：“生产数据”模块中已录入最新生产数据，“计算维护”模块中井名选择S68112，时间范围2019-01-24至2019-02-24，点击“关联数据计算”。弹出操作确认对话框，确认无误后点击“是”。这时，S68112井2019年1月24日至2019年2月24日的所有历史数据将按最新的生产数据进行重新计算。

![单井关联数据计算](https://github.com/cosog-chentr/apmd/blob/master/Image/PNG/019.png?raw=true)

（2） 所有井关联数据计算  
&emsp;&emsp;例如：单位组织下所有井，2019年1月24日至2019年2月24日内的所有历史结果。  
&emsp;&emsp;操作：“生产数据”模块中已录入最新生产数据，“计算维护”模块中井名不选择或选择全部，时间范围2019-01-24至2019-02-24，点击“关联数据计算”。弹出操作确认对话框，确认无误后点击“是”。这时，所有井2019年1月24日至2019年2月24日的所有历史数据将按最新的生产数据进行重新计算。

![所有井关联数据计算](https://github.com/cosog-chentr/apmd/blob/master/Image/PNG/020.png?raw=true)

## 2.9 系统配置

### 2.9.1 模块配置

&emsp;&emsp;对模块进行编辑，生成功能导航，控制功能模块显示、隐藏等。

![系统配置](https://github.com/cosog-chentr/apmd/blob/master/Image/PNG/021.png?raw=true)

### 2.9.2 字典配置

&emsp;&emsp;对各模块显示的字段进行管理，主要修改字段名称、显示顺序、是否显示等。

![字典配置](https://github.com/cosog-chentr/apmd/blob/master/Image/PNG/022.png?raw=true)

### 2.9.3 统计配置

&emsp;&emsp;配置各项参数的统计级别。

![统计配置](https://github.com/cosog-chentr/apmd/blob/master/Image/PNG/023.png?raw=true)

### 2.9.4 报警配置

&emsp;&emsp;设置工况类型的报警类型、报警项、级别、开关、颜色等。

![报警配置](https://github.com/cosog-chentr/apmd/blob/master/Image/PNG/024.png?raw=true)