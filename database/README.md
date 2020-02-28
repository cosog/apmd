----:link:[**转至用户手册**](.././README.md):link:----  

# 《油气生产敏捷计算分析系统V7.1》 数据库手册

# 一、表

## 1.1 表概览

| **序号** | **名称**                      | **描述**                 |
|----------|-------------------------------|--------------------------|
| 1        | tbl_org                       | 组织数据表               |
| 2        | tbl_user                      | 用户数据表               |
| 3        | tbl_role                      | 角色数据表               |
| 4        | tbl_module                    | 模块数据表               |
| 5        | tbl_module2role               | 模块角色关系表           |
| 6        | tbl_dist_name                 | 字典名称表               |
| 7        | tbl_dist_item                 | 字典数据项表             |
| 8        | tbl_code                      | 代码表                   |
| 9        | tbl_acq_group_conf            | 采控组名称表             |
| 10       | tbl_acq_item_conf             | 采控项名称表             |
| 11       | tbl_acq_item2group_conf       | 采控组项关系表           |
| 12       | tbl_wellinformation           | 井名基本信息表           |
| 13       | tbl_trajectory                | 井身轨迹表               |
| 14       | tbl_rpc_productiondata_latest | 抽油机生产数据实时表     |
| 15       | tbl_rpc_productiondata_hist   | 抽油机生产数据历史表     |
| 16       | tbl_rpc_discrete_latest       | 抽油机离散数据实时表     |
| 17       | tbl_rpc_discrete_hist         | 抽油机离散数据历史表     |
| 18       | tbl_rpc_diagram_latest        | 抽油机曲线数据实时表     |
| 19       | tbl_rpc_diagram_hist          | 抽油机曲线数据历史表     |
| 20       | tbl_rpc_worktype              | 抽油机工况类型表         |
| 21       | tbl_rpc_alarmtype_conf        | 抽油机报警类型表         |
| 22       | tbl_rpc_total_day             | 抽油机日累计数据表       |
| 23       | tbl_rpc_statistics_conf       | 抽油机统计配置表         |
| 24       | tbl_rpcinformation            | 抽油机设备表             |
| 25       | tbl_rpc_motor                 | 抽油机电机数据表         |
| 26       | tbl_rpc_inver_opt             | 抽油机电参反演参数优化表 |

## 1.2 逻辑结构

![逻辑结构](https://github.com/cosog-chentr/apmd/blob/master/Image/PNG/035.png?raw=true)

## 1.3 详述  

### 1.3.1 tbl_org 组织数据表

| **序号** | **字段代码** | **字段名**   | **单位** | **字段类型**   | **是否为空** | **键** | **备注** |
|----------|--------------|--------------|----------|----------------|--------------|--------|----------|
| 1        | org_id       | 单位序号     |          | NUMBER（10）   | N            | 主键   |          |
| 2        | org_code     | 单位编码     |          | VARCHAR2(20)   | Y            |        |          |
| 3        | org_name     | 单位名称     |          | VARCHAR2(100)  | N            |        |          |
| 4        | org_memo     | 单位说明     |          | VARCHAR2(4000) | Y            |        |          |
| 5        | org_parent   | 父级单位编号 |          | NUMBER（10）   | N            |        |          |
| 6        | org_seq      | 单位排序     |          | NUMBER（10）   | Y            |        |          |
| 7        | org_flag     | 单位标志     |          | CHAR(1)        | Y            |        |          |
| 8        | org_realid   | 单位当前编号 |          | NUMBER（10）   | Y            |        |          |
| 9        | org_level    | 单位级别     |          | NUMBER(1)      | Y            |        |          |
| 10       | org_type     | 单位类型     |          | NUMBER(1)      | Y            |        |          |
| 11       | org_coordx   | 纬度         |          | NUMBER(10,6)   | Y            |        |          |
| 12       | org_coordy   | 经度         |          | NUMBER(10,6)   | Y            |        |          |
| 13       | show_level   | 地图显示级别 |          | NUMBER(2)      | Y            |        |          |

### 1.3.2 tbl_user 用户数据表

| **序号** | **字段代码**    | **字段名**   | **单位** | **字段类型**  | **是否为空** | **键** | **备注**                    |
|----------|-----------------|--------------|----------|---------------|--------------|--------|-----------------------------|
| 1        | user_no         | 用户序号     |          | NUMBER（10）  | N            | 主键   |                             |
| 2        | user_id         | 用户账号     |          | VARCHAR2(20)  | N            |        |                             |
| 3        | user_pwd        | 用户密码     |          | VARCHAR2(20)  | Y            |        |                             |
| 4        | user_name       | 用户姓名     |          | VARCHAR2(40)  | N            |        |                             |
| 5        | user_in_email   | 内部邮箱     |          | VARCHAR2(40)  | Y            |        |                             |
| 6        | user_out_email  | 外部邮箱     |          | VARCHAR2(100) | Y            |        |                             |
| 7        | user_phone      | 用户电话     |          | VARCHAR2(40)  | Y            |        |                             |
| 8        | user_mobile     | 手机号       |          | VARCHAR2(40)  | Y            |        |                             |
| 9        | user_address    | 地址         |          | VARCHAR2(200) | Y            |        |                             |
| 10       | user_postcode   | 邮编         |          | CHAR(6)       | Y            |        |                             |
| 11       | user_title      | 用户职称     |          | VARCHAR2(100) | Y            |        |                             |
| 12       | user_type       | 用户类型     |          | NUMBER（10）  | Y            | 外键   | 对应tbl_role表中role_id字段 |
| 13       | user_orgid      | 用户所属组织 |          | NUMBER（10）  | N            | 外键   |                             |
| 14       | user_isleader   | 是否领导     |          | CHAR(1)       | Y            |        | 0-不是，1-是                |
| 15       | user_regtime    | 用户注册时间 |          | DATE          | Y            |        |                             |
| 16       | user_style      | 显示风格     |          | VARCHAR2(20)  | Y            |        |                             |
| 17       | user_quicklogin | 是否快捷登录 |          | NUMBER(1)     | Y            |        | 是否快捷登录 0-不是 1-是    |

### 1.3.3 tbl_role 角色数据表

| **序号** | **字段代码** | **字段名** | **单位** | **字段类型**   | **是否为空** | **键** | **备注**   |
|----------|--------------|------------|----------|----------------|--------------|--------|------------|
| 1        | role_id      | 角色序号   |          | NUMBER（10）   | N            | 主键   |            |
| 2        | role_code    | 角色编码   |          | VARCHAR2(50)   | N            |        |            |
| 3        | role_name    | 角色名称   |          | VARCHAR2(40)   | N            |        |            |
| 4        | role_flag    | 控制权限   |          | NUMBER(10)     | Y            |        | 0-无，1-是 |
| 5        | remark       | 角色描述   |          | VARCHAR2(2000) | Y            |        |            |

### 1.3.4 tbl_module 模块数据表

| **序号** | **字段代码** | **字段名**   | **单位** | **字段类型**  | **是否为空** | **键** | **备注**               |
|----------|--------------|--------------|----------|---------------|--------------|--------|------------------------|
| 1        | md_id        | 模块序号     |          | NUMBER（10）  | N            | 主键   |                        |
| 2        | md_parentid  | 父级模块序号 |          | NUMBER（10）  | N            |        |                        |
| 3        | md_name      | 模块名称     |          | VARCHAR2(100) | N            |        |                        |
| 4        | md_showname  | 模块简介     |          | VARCHAR2(100) | Y            |        |                        |
| 5        | md_url       | 模块URL      |          | VARCHAR2(200) | Y            |        |                        |
| 6        | md_code      | 模块编码     |          | VARCHAR2(200) | Y            |        |                        |
| 7        | md_seq       | 模块排序     |          | NUMBER(20)    | Y            |        |                        |
| 8        | md_level     | 模块级别     |          | NUMBER（10）  | Y            |        |                        |
| 9        | md_flag      | 模块标志     |          | NUMBER（10）  | Y            |        |                        |
| 10       | md_icon      | 模块图标     |          | VARCHAR2(100) | Y            |        |                        |
| 11       | md_type      | 模块类型     |          | NUMBER(1)     | Y            |        | 0-启用模块，2-备用模块 |
| 12       | md_control   | 模块控制器   |          | VARCHAR2(100) | Y            |        |                        |

### 1.3.5 tbl_module2role 模块角色关系表

| **序号** | **字段代码** | **字段名** | **单位** | **字段类型** | **是否为空** | **键** | **备注** |
|----------|--------------|------------|----------|--------------|--------------|--------|----------|
| 1        | rm_id        | 序号       |          | NUMBER（10） | N            | 主键   |          |
| 2        | rm_roleid    | 角色编号   |          | NUMBER（10） | N            | 外键   |          |
| 3        | rm_moduleid  | 模块序号   |          | NUMBER（10） | N            | 外键   |          |
| 4        | rm_matrix    | 权限矩阵   |          | VARCHAR2(8)  | N            |        |          |

### 1.3.6 tbl_dist_name 字典名称表

| **序号** | **字段代码** | **字段名** | **单位** | **字段类型** | **是否为空** | **键** | **备注**       |
|----------|--------------|------------|----------|--------------|--------------|--------|----------------|
| 1        | sysdataid    | 字典编码   |          | VARCHAR2(32) | N            | 主键   |                |
| 2        | tenantid     | 组织编号   |          | VARCHAR2(50) | Y            |        |                |
| 3        | cname        | 中文名称   |          | VARCHAR2(50) | Y            |        |                |
| 4        | ename        | 英文名称   |          | VARCHAR2(50) | Y            |        |                |
| 5        | sorts        | 排序       |          | NUMBER       | Y            |        |                |
| 6        | status       | 显示状态   |          | NUMBER       | Y            |        | 0-显示，1-隐藏 |
| 7        | creator      | 创建人     |          | VARCHAR2(50) | Y            |        |                |
| 8        | updateuser   | 修改人     |          | VARCHAR2(50) | Y            |        |                |
| 9        | createdate   | 创建时间   |          | DATE         | Y            |        | SYSDATE        |
| 10       | updatetime   | 修改时间   |          | DATE         | N            |        | SYSDATE        |

### 1.3.7 tbl_dist_item 字典数据项表

| **序号** | **字段代码** | **字段名** | **单位** | **字段类型**  | **是否为空** | **键** | **备注**       |
|----------|--------------|------------|----------|---------------|--------------|--------|----------------|
| 1        | dataitemid   | 数据项编码 |          | VARCHAR2(32)  | N            | 主键   |                |
| 2        | tenantid     | 组织编号   |          | VARCHAR2(50)  | Y            |        |                |
| 3        | sysdataid    | 字典编码   |          | VARCHAR2(50)  | Y            | 外键   |                |
| 4        | cname        | 中文名称   |          | VARCHAR2(50)  | Y            |        |                |
| 5        | ename        | 英文名称   |          | VARCHAR2(200) | Y            |        |                |
| 6        | datavalue    | 数据项值   |          | VARCHAR2(200) | Y            |        |                |
| 7        | sorts        | 排序       |          | NUMBER        | Y            |        |                |
| 8        | status       | 显示状态   |          | NUMBER        | Y            |        | 0-显示，1-隐藏 |
| 9        | creator      | 创建人     |          | VARCHAR2(50)  | Y            |        |                |
| 10       | updateuser   | 修改人     |          | VARCHAR2(50)  | Y            |        |                |
| 11       | createdate   | 创建时间   |          | DATE          | Y            |        | SYSDATE        |
| 12       | updatetime   | 修改时间   |          | DATE          | Y            |        | SYSDATE        |

### 1.3.8 tbl_code 代码表

| **序号** | **字段代码** | **字段名** | **单位** | **字段类型**  | **是否为空** | **键** | **备注** |
|----------|--------------|------------|----------|---------------|--------------|--------|----------|
| 1        | id           | 记录编号   |          | NUMBER（10）  | N            | 主键   |          |
| 2        | tablecode    | 数据表代码 |          | VARCHAR2(200) | Y            |        |          |
| 3        | itemcode     | 数据项代码 |          | VARCHAR2(200) | Y            |        |          |
| 4        | itemvalue    | 代码       |          | VARCHAR2(20)  | Y            |        |          |
| 5        | itemname     | 名称       |          | VARCHAR2(200) | Y            |        |          |
| 6        | remark       | 备注       |          | VARCHAR2(200) | Y            |        |          |
| 7        | state        | 状态       |          | NUMBER(10)    | Y            |        |          |

### 1.3.9 tbl_acq_group_conf 采控组名称表

| **序号** | **字段代码** | **字段名** | **单位** | **字段类型**   | **是否为空** | **键** | **备注** |
|----------|--------------|------------|----------|----------------|--------------|--------|----------|
| 1        | id           | 记录编号   |          | NUMBER(10)     | N            | 主键   |          |
| 2        | unit_code    | 单元代码   |          | VARCHAR2(50)   | N            |        |          |
| 3        | unit_name    | 单元名称   |          | VARCHAR2(50)   | Y            |        |          |
| 4        | remark       | 单元描述   |          | VARCHAR2(2000) | Y            |        |          |

### 1.3.10 tbl_acq_item_conf 采控项名称表

| **序号** | **字段代码**  | **字段名** | **单位** | **字段类型**  | **是否为空** | **键** | **备注**      |
|----------|---------------|------------|----------|---------------|--------------|--------|---------------|
| 1        | id            | 记录编号   |          | NUMBER(10)    | N            | 主键   |               |
| 2        | parentid      | 父级编号   |          | NUMBER(10)    | Y            |        |               |
| 3        | itemname      | 采集项名称 |          | VARCHAR2(100) | Y            |        |               |
| 4        | itemcode      | 采集项代码 |          | VARCHAR2(100) | Y            |        |               |
| 5        | address       | 寄存器地址 |          | NUMBER(10)    | Y            |        |               |
| 6        | length        | 寄存器个数 |          | NUMBER(10)    | Y            |        |               |
| 7        | datatype      | 数据类型   |          | NUMBER(5)     | Y            |        |               |
| 8        | zoom          | 量程变换   |          | NUMBER(10,3)  | Y            |        |               |
| 9        | seq           | 排序编号   |          | NUMBER(10)    | Y            |        |               |
| 10       | operationtype | 操作类型   |          | NUMBER(2)     | Y            |        | 1-只读 2-读写 |

### 1.3.11 tbl_acq_item2group_conf 采控组项关系表

| **序号** | **字段代码** | **字段名**   | **单位** | **字段类型** | **是否为空** | **键** | **备注** |
|----------|--------------|--------------|----------|--------------|--------------|--------|----------|
| 1        | id           | 记录编号     |          | NUMBER(10)   | N            | 主键   |          |
| 2        | unitid       | 采集类型编号 |          | NUMBER(10)   | N            | 外键   |          |
| 3        | itemid       | 采集项编号   |          | NUMBER(10)   | N            | 外键   |          |
| 4        | matrix       | 阵列         |          | VARCHAR2(8)  | N            |        |          |

### 1.3.12 tbl_wellinformation 井名基本信息表

| **序号** | **字段代码**               | **字段名**       | **单位** | **字段类型**  | **是否为空** | **键** | **备注**                                  |
|----------|----------------------------|------------------|----------|---------------|--------------|--------|-------------------------------------------|
| 1        | id                         | 记录编号         |          | NUMBER(10)    | N            | 主键   |                                           |
| 2        | orgid                      | 单位编号         |          | NUMBER(10)    | Y            | 外键   |                                           |
| 3        | resname                    | 油气藏名称       |          | VARCHAR2(200) | Y            |        |                                           |
| 4        | wellname                   | 井名             |          | VARCHAR2(200) | N            |        |                                           |
| 5        | liftingtype                | 举升类型         |          | NUMBER(10)    | Y            |        |                                           |
| 6        | driveraddr                 | 设备地址         |          | VARCHAR2(200) | Y            |        |                                           |
| 7        | driverid                   | 设备编号         |          | VARCHAR2(200) | Y            |        |                                           |
| 8        | acqcycle_diagram           | 功图采集间隔     | min      | NUMBER(10)    | Y            |        |                                           |
| 9        | acqcycle_discrete          | 离散数据读取间隔 | min      | NUMBER(10)    | Y            |        |                                           |
| 10       | savecycle_discrete         | 离散数据保存间隔 | min      | NUMBER(10)    | Y            |        |                                           |
| 11       | drivercode                 | 驱动编码         |          | VARCHAR2(50)  | Y            |        |                                           |
| 12       | unitcode                   | 采集单元编码     |          | VARCHAR2(50)  | Y            |        |                                           |
| 13       | runtimeefficiencysource    | 时率来源         |          | NUMBER(2)     | Y            |        | 0-人工录入 1-DI信号 2-电参计算 3-转速计算 |
| 14       | videourl                   | 视频url          |          | VARCHAR2(400) | Y            |        |                                           |
| 15       | sortnum                    | 排序编号         |          | NUMBER(10)    | Y            |        |                                           |
| 16       | acqcyclesetstatus_diagram  | 曲线采集间隔状态 |          | NUMBER(2)     | Y            |        | 0-等待下发 1-已下发 2-已同步              |
| 17       | acqcyclesetstatus_discrete | 离散采集间隔状态 |          | NUMBER(2)     | Y            |        | 0-等待下发 1-已下发 2-已同步              |
| 18       | groupid                    | 采控组编号       |          | NUMBER(10)    | Y            | 外键   |                                           |

### 1.3.13 tbl_trajectory 井身轨迹表

| **序号** | **字段代码** | **字段名** | **单位** | **字段类型** | **是否为空** | **键** | **备注** |
|----------|--------------|------------|----------|--------------|--------------|--------|----------|
| 1        |              |            |          |              |              |        |          |
| 2        |              |            |          |              |              |        |          |
| 3        |              |            |          |              |              |        |          |

### 1.3.14 tbl_rpc_productiondata_latest 抽油机生产数据实时表

| **序号** | **字段代码**               | **字段名**     | **单位** | **字段类型**  | **是否为空** | **键** | **备注** |
|----------|----------------------------|----------------|----------|---------------|--------------|--------|----------|
| 1        | id                         | 记录编号       |          | NUMBER(10)    | N            | 主键   |          |
| 2        | wellid                     | 井编号         |          | NUMBER(10)    | N            | 外键   |          |
| 3        | acquisitiontime            | 采集时间       |          | DATE          | Y            |        |          |
| 4        | liftingtype                | 举升类型       |          | NUMBER(10)    | Y            |        |          |
| 5        | displacementtype           | 驱替类型       |          | NUMBER(1)     | Y            |        |          |
| 6        | runtime                    | 生产时间       | h        | NUMBER(8,2)   | Y            |        |          |
| 7        | crudeoildensity            | 原油密度       | g/cm\^3  | NUMBER(16,2)  | Y            |        |          |
| 8        | waterdensity               | 水密度         | g/cm\^3  | NUMBER(16,2)  | Y            |        |          |
| 9        | naturalgasrelativedensity  | 天然气相对密度 |          | NUMBER(16,2)  | Y            |        |          |
| 10       | saturationpressure         | 饱和压力       | MPa      | NUMBER(16,2)  | Y            |        |          |
| 11       | reservoirdepth             | 油层中部深度   | m        | NUMBER(16,2)  | Y            |        |          |
| 12       | reservoirtemperature       | 油层中部温度   | ℃        | NUMBER(16,2)  | Y            |        |          |
| 13       | watercut                   | 体积含水率     | %        | NUMBER(8,2)   | Y            |        |          |
| 14       | watercut_w                 | 重量含水率     | %        | NUMBER(8,2)   | Y            |        |          |
| 15       | tubingpressure             | 油压           | MPa      | NUMBER(8,2)   | Y            |        |          |
| 16       | casingpressure             | 套压           | MPa      | NUMBER(8,2)   | Y            |        |          |
| 17       | backpressure               | 回压           | MPa      | NUMBER(8,2)   | Y            |        |          |
| 18       | wellheadfluidtemperature   | 井口流温       | ℃        | NUMBER(8,2)   | Y            |        |          |
| 19       | producingfluidlevel        | 动液面         | m        | NUMBER(8,2)   | Y            |        |          |
| 20       | pumpsettingdepth           | 泵挂           | m        | NUMBER(8,2)   | Y            |        |          |
| 21       | productiongasoilratio      | 生产气油比     | m\^3/t   | NUMBER(8,2)   | Y            |        |          |
| 22       | tubingstringinsidediameter | 油管内径       | mm       | NUMBER(8,2)   | Y            |        |          |
| 23       | casingstringinsidediameter | 油层套管内径   | mm       | NUMBER(8,2)   | Y            |        |          |
| 24       | rodstring                  | 抽油杆参数     |          | VARCHAR2(200) | Y            |        |          |
| 25       | pumpgrade                  | 泵级别         |          | NUMBER(1)     | Y            |        |          |
| 26       | pumpborediameter           | 泵径           | mm       | NUMBER(8,2)   | Y            |        |          |
| 27       | plungerlength              | 柱塞长         | m        | NUMBER(8,2)   | Y            |        |          |
| 28       | pumptype                   | 泵类型         |          | VARCHAR2(20)  | Y            |        |          |
| 29       | barreltype                 | 泵筒类型       |          | VARCHAR2(20)  | Y            |        |          |
| 30       | barrellength               | 泵筒长         | m        | NUMBER(8,2)   | Y            |        |          |
| 31       | barrelseries               | 泵级数         |          | NUMBER(8,2)   | Y            |        |          |
| 32       | rotordiameter              | 转子截面直径   | mm       | NUMBER(8,2)   | Y            |        |          |
| 33       | qpr                        | 公称排量       |          | NUMBER(8,2)   | Y            |        |          |
| 34       | manualintervention         | 人工干预       |          | NUMBER(4)     | Y            |        |          |
| 35       | netgrossratio              | 净毛比         |          | NUMBER(8,2)   | Y            |        |          |
| 36       | anchoringstate             | 锚定状态       |          | NUMBER(1)     | Y            |        |          |
| 37       | remark                     | 备注           |          | VARCHAR2(200) | Y            |        |          |

### 1.3.15 tbl_rpc_productiondata_hist 抽油机生产数据历史表

同tbl_rpc_productiondata_latest

### 1.3.16 tbl_rpc_discrete_latest 抽油机离散数据实时表

| **序号** | **字段代码**              | **字段名**                   | **单位** | **字段类型**   | **是否为空** | **键** | **备注**                |
|----------|---------------------------|------------------------------|----------|----------------|--------------|--------|-------------------------|
| 1        | id                        | 记录编号                     |          | NUMBER(10)     | N            | 主键   |                         |
| 2        | wellid                    | 井编号                       |          | NUMBER(10)     | N            | 外键   |                         |
| 3        | acquisitiontime           | 采集时间                     |          | DATE           | Y            |        |                         |
| 4        | commstatus                | 通信状态                     |          | NUMBER(2)      | Y            |        | 0-离线 1-在线           |
| 5        | commtime                  | 在线时间                     |          | NUMBER(8,2)    | Y            |        |                         |
| 6        | commtimeefficiency        | 在线时率                     |          | NUMBER(10,4)   | Y            |        |                         |
| 7        | commrange                 | 在线区间                     |          | VARCHAR2(2000) | Y            |        |                         |
| 8        | runstatus                 | 运行状态                     |          | NUMBER(2)      | Y            |        | 0-停抽 1-运行           |
| 9        | runtimeefficiency         | 运行时率                     |          | NUMBER(10,4)   | Y            |        |                         |
| 10       | runtime                   | 运行时间                     |          | NUMBER(8,2)    | Y            |        |                         |
| 11       | runrange                  | 运行区间                     |          | VARCHAR2(2000) | Y            |        |                         |
| 12       | ia                        | A相电流                      | A        | NUMBER(8,2)    | Y            |        |                         |
| 13       | ib                        | B相电流                      | A        | NUMBER(8,2)    | Y            |        |                         |
| 14       | ic                        | C相电流                      | A        | NUMBER(8,2)    | Y            |        |                         |
| 15       | va                        | A相电压                      | V        | NUMBER(8,2)    | Y            |        |                         |
| 16       | vb                        | B相电压                      | V        | NUMBER(8,2)    | Y            |        |                         |
| 17       | vc                        | C相电压                      | V        | NUMBER(8,2)    | Y            |        |                         |
| 18       | totalwattenergy           | 累计有功电能                 | kW·h     | NUMBER(8,2)    | Y            |        |                         |
| 19       | totalvarenergy            | 累计无功电能                 | kVar·h   | NUMBER(8,2)    | Y            |        |                         |
| 20       | wattsum                   | 三相总有功功率               | kW       | NUMBER(8,2)    | Y            |        |                         |
| 21       | varsum                    | 三相总无功功率               | kVar     | NUMBER(8,2)    | Y            |        |                         |
| 22       | reversepower              | 反向功率                     |          | NUMBER(8,2)    | Y            |        |                         |
| 23       | pfsum                     | 三相综合功率因数             |          | NUMBER(8,2)    | Y            |        |                         |
| 24       | acqcycle_diagram          | 功图采集周期                 | min      | NUMBER(6)      | Y            |        |                         |
| 25       | frequencysetvalue         | 变频设置频率                 | HZ       | NUMBER(8,2)    | Y            |        |                         |
| 26       | frequencyrunvalue         | 变频运行频率                 | HZ       | NUMBER(8,2)    | Y            |        |                         |
| 27       | tubingpressure            | 油压                         | MPa      | NUMBER(8,2)    | Y            |        |                         |
| 28       | casingpressure            | 套压                         | MPa      | NUMBER(8,2)    | Y            |        |                         |
| 29       | backpressure              | 回压                         | MPa      | NUMBER(8,2)    | Y            |        |                         |
| 30       | wellheadfluidtemperature  | 井口油温                     | ℃        | NUMBER(8,2)    | Y            |        |                         |
| 31       | totaywattenergy           | 日有功电能                   | kW·h     | NUMBER(8,2)    | Y            |        | 日用电量                |
| 32       | workingconditioncode      | 电参工况                     |          | NUMBER(4)      | Y            |        |                         |
| 33       | iaalarm                   | A相电流报警项                |          | VARCHAR2(20)   | Y            |        | 高报/低报/零值/均衡报警 |
| 34       | ibalarm                   | B相电流报警项                |          | VARCHAR2(20)   | Y            |        | 高报/低报/零值/均衡报警 |
| 35       | icalarm                   | C相电流报警项                |          | VARCHAR2(20)   | Y            |        | 高报/低报/零值/均衡报警 |
| 36       | vaalarm                   | A相电压报警项                |          | VARCHAR2(20)   | Y            |        | 高报/低报/零值/均衡报警 |
| 37       | vbalarm                   | B相电压报警项                |          | VARCHAR2(20)   | Y            |        | 高报/低报/零值/均衡报警 |
| 38       | vcalarm                   | C相电压报警项                |          | VARCHAR2(20)   | Y            |        | 高报/低报/零值/均衡报警 |
| 39       | workingconditionstring    | 电参工况字符串               |          | VARCHAR2(4000) | Y            |        |                         |
| 40       | iauplimit                 | A相电流上限                  | A        | NUMBER(8,2)    | Y            |        |                         |
| 41       | iadownlimit               | A相电流下限                  | A        | NUMBER(8,2)    | Y            |        |                         |
| 42       | iazero                    | A相电流零值                  | A        | NUMBER(8,2)    | Y            |        |                         |
| 43       | ibuplimit                 | B相电流上限                  | A        | NUMBER(8,2)    | Y            |        |                         |
| 44       | ibdownlimit               | B相电流下限                  | A        | NUMBER(8,2)    | Y            |        |                         |
| 45       | ibzero                    | B相电流零值                  | A        | NUMBER(8,2)    | Y            |        |                         |
| 46       | icuplimit                 | C相电流上限                  | A        | NUMBER(8,2)    | Y            |        |                         |
| 47       | icdownlimit               | C相电流下限                  | A        | NUMBER(8,2)    | Y            |        |                         |
| 48       | iczero                    | C相电流零值                  | A        | NUMBER(8,2)    | Y            |        |                         |
| 49       | vauplimit                 | A相电压上限                  | V        | NUMBER(8,2)    | Y            |        |                         |
| 50       | vadownlimit               | A相电压下限                  | V        | NUMBER(8,2)    | Y            |        |                         |
| 51       | vazero                    | A相电压零值                  | V        | NUMBER(8,2)    | Y            |        |                         |
| 52       | vbuplimit                 | B相电压上限                  | V        | NUMBER(8,2)    | Y            |        |                         |
| 53       | vbdownlimit               | B相电压下限                  | V        | NUMBER(8,2)    | Y            |        |                         |
| 54       | vbzero                    | B相电压零值                  | V        | NUMBER(8,2)    | Y            |        |                         |
| 55       | vcuplimit                 | C相电压上限                  | V        | NUMBER(8,2)    | Y            |        |                         |
| 56       | vcdownlimit               | C相电压下限                  | V        | NUMBER(8,2)    | Y            |        |                         |
| 57       | vczero                    | C相电压零值                  | V        | NUMBER(8,2)    | Y            |        |                         |
| 58       | totalpwattenergy          | 累计正向有功电能             | kW·h     | NUMBER(8,2)    | Y            |        |                         |
| 59       | totalnwattenergy          | 累计反向有功电能             | kW·h     | NUMBER(8,2)    | Y            |        |                         |
| 60       | totalpvarenergy           | 累计正向无功电能             | kVar·h   | NUMBER(8,2)    | Y            |        |                         |
| 61       | totalnvarenergy           | 累计反向无功电能             | kVar·h   | NUMBER(8,2)    | Y            |        |                         |
| 62       | totalvaenergy             | 累计视在电能                 | kVA·h    | NUMBER(8,2)    | Y            |        |                         |
| 63       | todaypwattenergy          | 日正向有功电能               | kW·h     | NUMBER(8,2)    | Y            |        |                         |
| 64       | todaynwattenergy          | 日反向有功电能               | kW·h     | NUMBER(8,2)    | Y            |        |                         |
| 65       | todayvarenergy            | 日无功电能                   | kVar·h   | NUMBER(8,2)    | Y            |        |                         |
| 66       | todaypvarenergy           | 日正向无功电能               | kVar·h   | NUMBER(8,2)    | Y            |        |                         |
| 67       | todaynvarenergy           | 日反向无功电能               | kVar·h   | NUMBER(8,2)    | Y            |        |                         |
| 68       | todayvaenergy             | 日视在电能                   | kVA·h    | NUMBER(8,2)    | Y            |        |                         |
| 69       | vasum                     | 视在功率                     | kVA      | NUMBER(8,2)    | Y            |        |                         |
| 70       | signal                    | 信号强度                     |          | NUMBER(8,2)    | Y            |        |                         |
| 71       | interval                  | 传输间隔                     | min      | NUMBER(10)     | Y            |        |                         |
| 72       | devicever                 | 设备版本信息                 |          | VARCHAR2(50)   | Y            |        |                         |
| 73       | vavg                      | 三相电压平均值               | V        | NUMBER(8,2)    | Y            |        |                         |
| 74       | iavg                      | 三相电流平均值               | A        | NUMBER(8,2)    | Y            |        |                         |
| 75       | watta                     | A相有功功率                  | kW       | NUMBER(8,2)    | Y            |        |                         |
| 76       | wattb                     | B相有功功率                  | kW       | NUMBER(8,2)    | Y            |        |                         |
| 77       | wattc                     | C相有功功率                  | kW       | NUMBER(8,2)    | Y            |        |                         |
| 78       | vara                      | A相无功功率                  | kVar     | NUMBER(8,2)    | Y            |        |                         |
| 79       | varb                      | B相无功功率                  | kVar     | NUMBER(8,2)    | Y            |        |                         |
| 80       | varc                      | C相无功功率                  | kVar     | NUMBER(8,2)    | Y            |        |                         |
| 81       | vaa                       | A相视在功率                  | kVA      | NUMBER(8,2)    | Y            |        |                         |
| 82       | vab                       | B相视在功率                  | kVA      | NUMBER(8,2)    | Y            |        |                         |
| 83       | vac                       | C相视在功率                  | kVA      | NUMBER(8,2)    | Y            |        |                         |
| 84       | pfa                       | A相功率因数                  |          | NUMBER(8,2)    | Y            |        |                         |
| 85       | pfb                       | B相功率因数                  |          | NUMBER(8,2)    | Y            |        |                         |
| 86       | pfc                       | C相功率因数                  |          | NUMBER(8,2)    | Y            |        |                         |
| 87       | balancecontrolmode        | 平衡远程调节远程触发控制     |          | NUMBER(10)     | Y            |        | 0-无操作执行 1-正在调节 |
| 88       | balancecalculatemode      | 平衡计算方式                 |          | NUMBER(10)     | Y            |        | 1-下/上 2-上/下         |
| 89       | balanceawaytime           | 重心远离支点调节时间         | ms       | NUMBER(10)     | Y            |        |                         |
| 90       | balanceclosetime          | 重心接近支点调节时间         | ms       | NUMBER(10)     | Y            |        |                         |
| 91       | balancestrokecount        | 参与平衡度计算的冲程测量次数 |          | NUMBER(10)     | Y            |        |                         |
| 92       | balanceoperationuplimit   | 平衡调节上限                 | %        | NUMBER(10)     | Y            |        |                         |
| 93       | balanceoperationdownlimit | 平衡调节下限                 | %        | NUMBER(10)     | Y            |        |                         |
| 94       | balanceautocontrol        | 平衡远程自动调节             |          | NUMBER(1)      | Y            |        | 0-允许 1-禁止           |
| 95       | balancefrontlimit         | 平衡前限位                   |          | NUMBER(1)      | Y            |        | 0-限位 1-未限位         |
| 96       | balanceafterlimit         | 平衡后限位                   |          | NUMBER(1)      | Y            |        | 0-限位 1-未限位         |
| 97       | spmautocontrol            | 冲次远程自动调节             |          | NUMBER(1)      | Y            |        | 0-允许 1-禁止           |
| 98       | balanceawaytimeperbeat    | 重心远离支点每拍调节时间     | ms       | NUMBER(10)     | Y            |        |                         |
| 99       | balanceclosetimeperbeat   | 重心接近支点每拍调节时间     | ms       | NUMBER(10)     | Y            |        |                         |

### 1.3.17 tbl_rpc_discrete_hist 抽油机离散数据历史表

同tbl_rpc_discrete_latest

### 1.3.18 tbl_rpc_diagram_latest 抽油机曲线数据实时表

| **序号** | **字段代码**                 | **字段名**           | **单位**    | **字段类型**  | **是否为空** | **键** | **备注**                                                                                       |
|----------|------------------------------|----------------------|-------------|---------------|--------------|--------|------------------------------------------------------------------------------------------------|
| 1        | id                           | 记录编号             |             | NUMBER(10)    | N            | 主键   |                                                                                                |
| 2        | wellid                       | 井编号               |             | NUMBER（10）  | N            | 外键   |                                                                                                |
| 3        | acquisitiontime              | 测试时间             |             | DATE          | Y            |        |                                                                                                |
| 4        | stroke                       | 冲程                 | m           | NUMBER(8,2)   | Y            |        |                                                                                                |
| 5        | spm                          | 冲次                 | 次/min      | NUMBER(8,2)   | Y            |        |                                                                                                |
| 6        | fmax                         | 最大载荷             | kN          | NUMBER(8,2)   | Y            |        |                                                                                                |
| 7        | fmin                         | 最小载荷             | kN          | NUMBER(8,2)   | Y            |        |                                                                                                |
| 8        | position_curve               | 位移曲线             | m           | CLOB          | Y            |        | 位移1,位移2…                                                                                   |
| 9        | angle_curve                  | 角度曲线             | °           | CLOB          | Y            |        | 角度1,角度2…                                                                                   |
| 10       | load_curve                   | 载荷曲线             | kN          | CLOB          | Y            |        | 载荷1,载荷2…                                                                                   |
| 11       | power_curve                  | 功率曲线             | kW          | CLOB          | Y            |        | 功率1,功率2…                                                                                   |
| 12       | current_curve                | 电流曲线             | A           | CLOB          | Y            |        | 电流1,电流2…                                                                                   |
| 13       | rpm_curve                    | 电机转速曲线         | r/min       | CLOB          | Y            |        | 转速1,转速2…                                                                                   |
| 14       | rawpower_curve               | 功率原始曲线         | kW          | CLOB          | Y            |        | 功率1,功率2…                                                                                   |
| 15       | rawcurrent_curve             | 电流原始曲线         | A           | CLOB          | Y            |        | 电流1,电流2…                                                                                   |
| 16       | rawrpm_curve                 | 电机转速原始曲线     | r/min       | CLOB          | Y            |        | 转速1,转速2…                                                                                   |
| 17       | upstrokeimax                 | 上冲程最大电流       | A           | NUMBER(8,2)   | Y            |        |                                                                                                |
| 18       | downstrokeimax               | 下冲程最大电流       | A           | NUMBER(8,2)   | Y            |        |                                                                                                |
| 19       | upstrokewattmax              | 上冲程最大功率       | kW          | NUMBER(8,2)   | Y            |        |                                                                                                |
| 20       | downstrokewattmax            | 下冲程最大功率       | kW          | NUMBER(8,2)   | Y            |        |                                                                                                |
| 21       | idegreebalance               | 电流平衡度           | %           | NUMBER(8,2)   | Y            |        |                                                                                                |
| 22       | wattdegreebalance            | 功率平衡度           | %           | NUMBER(8,2)   | Y            |        |                                                                                                |
| 23       | datasource                   | 功图来源             |             | NUMBER(1)     | Y            |        | 0-采集 1-电参反演 2-人工上传                                                                   |
| 24       | workingconditioncode         | 工况类型             |             | NUMBER(4)     | Y            |        |                                                                                                |
| 25       | fullnesscoefficient          | 功图充满系数         | 小数        | NUMBER(12,3)  | Y            |        |                                                                                                |
| 26       | upperloadline                | 理论上载荷           | kN          | NUMBER(8,2)   | Y            |        |                                                                                                |
| 27       | upperloadlineofexact         | 真实理论上载荷       | kN          | NUMBER(8,2)   | Y            |        |                                                                                                |
| 28       | lowerloadline                | 理论下载荷           | kN          | NUMBER(8,2)   | Y            |        |                                                                                                |
| 29       | pumpfsdiagram                | 泵功图               |             | CLOB          | Y            |        |                                                                                                |
| 30       | theoreticalproduction        | 理论排量             | m\^3/d      | NUMBER(8,2)   | Y            |        |                                                                                                |
| 31       | liquidvolumetricproduction   | 计算单井日产液量方   | m\^3/d      | NUMBER(8,2)   | Y            |        |                                                                                                |
| 32       | oilvolumetricproduction      | 计算单井日产油量方   | m\^3/d      | NUMBER(8,2)   | Y            |        |                                                                                                |
| 33       | watervolumetricproduction    | 计算单井日产水量方   | m\^3/d      | NUMBER(8,2)   | Y            |        |                                                                                                |
| 34       | availableplungerstrokeprod_v | 泵有效冲程计算产量方 | m\^3/d      | NUMBER(8,2)   | Y            |        |                                                                                                |
| 35       | pumpclearanceleakprod_v      | 泵间隙漏失量方       | m\^3/d      | NUMBER(8,2)   | Y            |        |                                                                                                |
| 36       | tvleakvolumetricproduction   | 游动凡尔漏失量方     | m\^3/d      | NUMBER(8,2)   | Y            |        |                                                                                                |
| 37       | svleakvolumetricproduction   | 固定凡尔漏失量方     | m\^3/d      | NUMBER(8,2)   | Y            |        |                                                                                                |
| 38       | gasinfluenceprod_v           | 气影响方             | m\^3/d      | NUMBER(8,2)   | Y            |        |                                                                                                |
| 39       | liquidweightproduction       | 计算单井日产液量吨   | t/d         | NUMBER(8,2)   | Y            |        |                                                                                                |
| 40       | oilweightproduction          | 计算单井日产油量吨   | t/d         | NUMBER(8,2)   | Y            |        |                                                                                                |
| 41       | waterweightproduction        | 计算单井日产水量吨   | t/d         | NUMBER(8,2)   | Y            |        |                                                                                                |
| 42       | availableplungerstrokeprod_w | 泵有效冲程计算产量吨 | t/d         | NUMBER(8,2)   | Y            |        |                                                                                                |
| 43       | pumpclearanceleakprod_w      | 泵间隙漏失量吨       | t/d         | NUMBER(8,2)   | Y            |        |                                                                                                |
| 44       | tvleakweightproduction       | 游动凡尔漏失量吨     | t/d         | NUMBER(8,2)   | Y            |        |                                                                                                |
| 45       | svleakweightproduction       | 固定凡尔漏失量吨     | t/d         | NUMBER(8,2)   | Y            |        |                                                                                                |
| 46       | gasinfluenceprod_w           | 气影响吨             | t/d         | NUMBER(8,2)   | Y            |        |                                                                                                |
| 47       | motorinputactivepower        | 有功功率             | kW          | NUMBER(8,2)   | Y            |        |                                                                                                |
| 48       | polishrodpower               | 光杆功率             | kW          | NUMBER(8,2)   | Y            |        |                                                                                                |
| 49       | waterpower                   | 水功率               | kW          | NUMBER(8,2)   | Y            |        |                                                                                                |
| 50       | surfacesystemefficiency      | 地面系统效率         | 小数        | NUMBER(12,3)  | Y            |        |                                                                                                |
| 51       | welldownsystemefficiency     | 井下系统效率         | 小数        | NUMBER(12,3)  | Y            |        |                                                                                                |
| 52       | systemefficiency             | 系统效率             | 小数        | NUMBER(12,3)  | Y            |        |                                                                                                |
| 53       | powerconsumptionperthm       | 吨液百米耗电量       | kW·h/100m·t | NUMBER(8,2)   | Y            |        |                                                                                                |
| 54       | fsdiagramarea                | 功图面积             |             | NUMBER(8,2)   | Y            |        |                                                                                                |
| 55       | rodflexlength                | 抽油杆伸长量         | m           | NUMBER(8,2)   | Y            |        |                                                                                                |
| 56       | tubingflexlength             | 油管伸缩量           | m           | NUMBER(8,2)   | Y            |        |                                                                                                |
| 57       | inertialength                | 惯性增量             | m           | NUMBER(8,2)   | Y            |        |                                                                                                |
| 58       | pumpeff1                     | 冲程损失系数         | 小数        | NUMBER(12,3)  | Y            |        |                                                                                                |
| 59       | pumpeff2                     | 充满系数             | 小数        | NUMBER(12,3)  | Y            |        |                                                                                                |
| 60       | pumpeff3                     | 间隙漏失系数         | 小数        | NUMBER(12,3)  | Y            |        |                                                                                                |
| 61       | pumpeff4                     | 液体收缩系数         | 小数        | NUMBER(12,3)  | Y            |        |                                                                                                |
| 62       | pumpeff                      | 总泵效               | 小数        | NUMBER(12,3)  | Y            |        |                                                                                                |
| 63       | pumpintakep                  | 泵入口压力           | MPa         | NUMBER(8,2)   | Y            |        |                                                                                                |
| 64       | pumpintaket                  | 泵入口温度           | ℃           | NUMBER(8,2)   | Y            |        |                                                                                                |
| 65       | pumpintakegol                | 泵入口就地气液比     |             | NUMBER(8,2)   | Y            |        |                                                                                                |
| 66       | pumpinletvisl                | 泵入口液体粘度       | mPa·s       | NUMBER(8,2)   | Y            |        |                                                                                                |
| 67       | pumpinletbo                  | 泵入口原油体积系数   | 小数        | NUMBER(8,2)   | Y            |        |                                                                                                |
| 68       | pumpoutletp                  | 泵出口压力           | MPa         | NUMBER(8,2)   | Y            |        |                                                                                                |
| 69       | pumpoutlett                  | 泵出口温度           | ℃           | NUMBER(8,2)   | Y            |        |                                                                                                |
| 70       | pumpoutletgol                | 泵出口就地气液比     |             | NUMBER(8,2)   | Y            |        |                                                                                                |
| 71       | pumpoutletvisl               | 泵出口液体粘度       | mPa·s       | NUMBER(8,2)   | Y            |        |                                                                                                |
| 72       | pumpoutletbo                 | 泵出口原油体积系数   | 小数        | NUMBER(8,2)   | Y            |        |                                                                                                |
| 73       | rodstring                    | 抽油杆柱分析数据     |             | VARCHAR2(200) | Y            |        | 格式：杆数,总杆长,总杆重,总浮力;一级杆最大应力,一级杆最小应力,一级杆许用应力,一级杆应力范围比… |
| 74       | savetime                     | 入库时间             |             | DATE          | Y            |        | SYSDATE                                                                                        |
| 75       | productiondataid             | 生产数据编号         |             | NUMBER(10)    | Y            |        | 关联生产数据历史表                                                                             |
| 76       | resultstatus                 | 计算标志             |             | NUMBER(2)     | Y            |        |                                                                                                |
| 77       | inverresultstatus            | 功图反演状态         |             | NUMBER(2)     | Y            |        |                                                                                                |
| 78       | remark                       | 备注                 |             | VARCHAR2(200) | Y            |        |                                                                                                |
| 79       | position360_curve            | 360度均分位移曲线    | m           | CLOB          | Y            |        | 360度均分位移曲线                                                                              |
| 80       | angle360_curve               | 360度均分角度曲线    | °           | CLOB          | Y            |        | 360度均分角度曲线                                                                              |
| 81       | load360_curve                | 360度均分载荷曲线    | kN          | CLOB          | Y            |        | 360度均分载荷曲线                                                                              |
| 82       | signal                       | 信号强度             |             | NUMBER(8,2)   | Y            |        |                                                                                                |
| 83       | interval                     | 传输间隔             | min         | NUMBER(10)    | Y            |        |                                                                                                |
| 84       | devicever                    | 设备版本信息         |             | VARCHAR2(50)  | Y            |        |                                                                                                |
| 85       | discretedataid               | 离散数据编号         |             | NUMBER(10)    | Y            |        |                                                                                                |

### 1.3.19 tbl_rpc_diagram_hist 抽油机曲线数据历史表

同tbl_rpc_diagram_latest

### 1.3.20 tbl_rpc_worktype 抽油机工况类型表

| **序号** | **字段代码**                | **字段名** | **单位** | **字段类型**  | **是否为空** | **键** | **备注** |
|----------|-----------------------------|------------|----------|---------------|--------------|--------|----------|
| 1        | id                          | 记录编号   |          | NUMBER（10）  | N            | 主键   |          |
| 2        | workingconditioncode        | 工况类型   |          | NUMBER(4)     | N            |        |          |
| 3        | workingconditionname        | 工况名称   |          | VARCHAR2(200) | N            |        |          |
| 4        | workingconditiondescription | 工况说明   |          | VARCHAR2(200) | Y            |        |          |
| 5        | workingconditiontemplate    | 工况模板   |          | BLOB          | Y            |        |          |
| 6        | optimizationsuggestion      | 优化建议   |          | VARCHAR2(200) | Y            |        |          |
| 7        | remark                      | 备注       |          | VARCHAR2(200) | Y            |        |          |

### 1.3.21 tbl_rpc_alarmtype_conf 抽油机报警类型表

| **序号** | **字段代码**         | **字段名** | **单位** | **字段类型**  | **是否为空** | **键** | **备注**                                                                                                                                                                    |
|----------|----------------------|------------|----------|---------------|--------------|--------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 1        | id                   | 记录编号   |          | NUMBER(10)    | N            | 主键   |                                                                                                                                                                             |
| 2        | workingconditioncode | 工况类型   |          | NUMBER(10)    | N            |        |                                                                                                                                                                             |
| 3        | alarmtype            | 报警类型   |          | NUMBER(3)     | N            |        | 100-通信报警，200-测试报警，300-视频和RFID报警，301-视频，302-RFID报警，400-工况报警，500-平衡报警，600-设备报警，601-载荷传感器报警，602-压力传感器报警，603-温度传感器报警 |
| 4        | alarmlevel           | 报警级别   |          | NUMBER(3)     | N            |        | 100-一级报警，200-二级报警，300-三级报警，400-四级报警                                                                                                                      |
| 5        | alarmsign            | 报警标志   |          | NUMBER(1)     | Y            |        | 0-正常，1-报警                                                                                                                                                              |
| 6        | remark               | 备注       |          | VARCHAR2(200) | Y            |        |                                                                                                                                                                             |

### 1.3.22 tbl_rpc_total_day 抽油机日累计数据表

| **序号** | **字段代码**                  | **字段名**               | **单位**    | **字段类型**   | **是否为空** | **键** | **备注**      |
|----------|-------------------------------|--------------------------|-------------|----------------|--------------|--------|---------------|
| 1        | id                            | 记录编号                 |             | NUMBER(10)     | N            | 主键   |               |
| 2        | wellid                        | 井编号                   |             | NUMBER(10)     | Y            | 外键   |               |
| 3        | calculatedate                 | 计算时间                 |             | DATE           | Y            |        |               |
| 4        | commstatus                    | 通信状态                 |             | NUMBER(2)      | Y            |        | 0-离线 1-在线 |
| 5        | runstatus                     | 运行状态                 |             | NUMBER(2)      | Y            |        | 0-停止 1-运行 |
| 6        | commtime                      | 通信时间                 |             | NUMBER(8,2)    | Y            |        |               |
| 7        | commtimeefficiency            | 通信时率                 |             | NUMBER(12,3)   | Y            |        |               |
| 8        | commrange                     | 通信区间                 |             | VARCHAR2(4000) | Y            |        |               |
| 9        | runtime                       | 运行时间                 |             | NUMBER(8,2)    | Y            |        |               |
| 10       | runrange                      | 运行区间                 |             | VARCHAR2(4000) | Y            |        |               |
| 11       | runtimeefficiency             | 生产时率                 | 小数        | NUMBER(12,3)   | Y            |        |               |
| 12       | workingconditioncode          | 工况类型                 |             | NUMBER(4)      | Y            |        |               |
| 13       | workingconditionstring        | 功图工况字符串           |             | VARCHAR2(4000) | Y            |        |               |
| 14       | workingconditioncode_e        | 电参工况类型             |             | NUMBER(4)      | Y            |        |               |
| 15       | workingconditionstring_e      | 电参工况字符串           |             | VARCHAR2(4000) | Y            |        |               |
| 16       | fullnesscoefficient           | 功图充满系数             | 小数        | NUMBER(10,4)   | Y            |        |               |
| 17       | fullnesscoefficientmax        | 功图充满系数最大值       | 小数        | NUMBER(10,4)   | Y            |        |               |
| 18       | fullnesscoefficientmin        | 功图充满系数最小值       | 小数        | NUMBER(10,4)   | Y            |        |               |
| 19       | stroke                        | 冲程                     | m           | NUMBER(8,2)    | Y            |        |               |
| 20       | strokemax                     | 冲程最大值               | m           | NUMBER(8,2)    | Y            |        |               |
| 21       | strokemin                     | 冲程最小值               | m           | NUMBER(8,2)    | Y            |        |               |
| 22       | spm                           | 冲次                     | 次/min      | NUMBER(8,2)    | Y            |        |               |
| 23       | spmmax                        | 冲次最大值               | 次/min      | NUMBER(8,2)    | Y            |        |               |
| 24       | spmmin                        | 冲次最小值               | 次/min      | NUMBER(8,2)    | Y            |        |               |
| 25       | liquidvolumetricproduction    | 计算单井日产液量方       | m\^3/d      | NUMBER(8,2)    | Y            |        |               |
| 26       | oilvolumetricproduction       | 计算单井日产油量方       | m\^3/d      | NUMBER(8,2)    | Y            |        |               |
| 27       | watervolumetricproduction     | 计算单井日产水量方       | m\^3/d      | NUMBER(8,2)    | Y            |        |               |
| 28       | liquidweightproduction        | 计算单井日产液量吨       | t/d         | NUMBER(8,2)    | Y            |        |               |
| 29       | oilweightproduction           | 计算单井日产油量吨       | t/d         | NUMBER(8,2)    | Y            |        |               |
| 30       | waterweightproduction         | 计算单井日产水量吨       | t/d         | NUMBER(8,2)    | Y            |        |               |
| 31       | liquidvolumetricproductionmax | 计算单井日产液量最大值方 | m\^3/d      | NUMBER(8,2)    | Y            |        |               |
| 32       | liquidvolumetricproductionmin | 计算单井日产液量最小值方 | m\^3/d      | NUMBER(8,2)    | Y            |        |               |
| 33       | oilvolumetricproductionmax    | 计算单井日产油量最大值方 | m\^3/d      | NUMBER(8,2)    | Y            |        |               |
| 34       | oilvolumetricproductionmin    | 计算单井日产油量最小值方 | m\^3/d      | NUMBER(8,2)    | Y            |        |               |
| 35       | watervolumetricproductionmax  | 计算单井日产水量最大值方 | m\^3/d      | NUMBER(8,2)    | Y            |        |               |
| 36       | watervolumetricproductionmin  | 计算单井日产水量最小值方 | m\^3/d      | NUMBER(8,2)    | Y            |        |               |
| 37       | liquidweightproductionmax     | 计算单井日产液量最大值吨 | t/d         | NUMBER(8,2)    | Y            |        |               |
| 38       | liquidweightproductionmin     | 计算单井日产液量最小值吨 | t/d         | NUMBER(8,2)    | Y            |        |               |
| 39       | oilweightproductionmax        | 计算单井日产油量最大值吨 | t/d         | NUMBER(8,2)    | Y            |        |               |
| 40       | oilweightproductionmin        | 计算单井日产油量最小值吨 | t/d         | NUMBER(8,2)    | Y            |        |               |
| 41       | waterweightproductionmax      | 计算单井日产水量最大值吨 | t/d         | NUMBER(8,2)    | Y            |        |               |
| 42       | waterweightproductionmin      | 计算单井日产水量最小值吨 | t/d         | NUMBER(8,2)    | Y            |        |               |
| 43       | wattdegreebalance             | 功率平衡度               | %           | NUMBER(8,2)    | Y            |        |               |
| 44       | idegreebalance                | 电流平衡度               | %           | NUMBER(8,2)    | Y            |        |               |
| 45       | wattdegreebalancemax          | 功率平衡度最大值         | %           | NUMBER(8,2)    | Y            |        |               |
| 46       | wattdegreebalancemin          | 功率平衡度最小值         | %           | NUMBER(8,2)    | Y            |        |               |
| 47       | idegreebalancemax             | 电流平衡度最大值         | %           | NUMBER(8,2)    | Y            |        |               |
| 48       | idegreebalancemin             | 电流平衡度最小值         | %           | NUMBER(8,2)    | Y            |        |               |
| 49       | deltaradius                   | 移动距离                 | m           | NUMBER(8,2)    | Y            |        |               |
| 50       | deltaradiusmax                | 移动距离最大值           | m           | NUMBER(8,2)    | Y            |        |               |
| 51       | deltaradiusmin                | 移动距离最小值           | m           | NUMBER(8,2)    | Y            |        |               |
| 52       | watercut                      | 体积含水率               | %           | NUMBER(10,4)   | Y            |        |               |
| 53       | watercut_w                    | 重量含水率               | %           | NUMBER(10,4)   | Y            |        |               |
| 54       | watercutmax                   | 体积含水率最大值         | %           | NUMBER(10,4)   | Y            |        |               |
| 55       | watercutmin                   | 体积含水率最小值         | %           | NUMBER(10,4)   | Y            |        |               |
| 56       | watercutmax_w                 | 重量含水率最大值         | %           | NUMBER(10,4)   | Y            |        |               |
| 57       | watercutmin_w                 | 重量含水率最小值         | %           | NUMBER(10,4)   | Y            |        |               |
| 58       | tubingpressure                | 油压                     | MPa         | NUMBER(8,2)    | Y            |        |               |
| 59       | tubingpressuremax             | 油压最大值               | MPa         | NUMBER(8,2)    | Y            |        |               |
| 60       | tubingpressuremin             | 油压最小值               | MPa         | NUMBER(8,2)    | Y            |        |               |
| 61       | casingpressure                | 套压                     | MPa         | NUMBER(8,2)    | Y            |        |               |
| 62       | casingpressuremax             | 套压最大值               | MPa         | NUMBER(8,2)    | Y            |        |               |
| 63       | casingpressuremin             | 套压最小值               | MPa         | NUMBER(8,2)    | Y            |        |               |
| 64       | wellheadfluidtemperature      | 井口油温                 | ℃           | NUMBER(8,2)    | Y            |        |               |
| 65       | wellheadfluidtemperaturemax   | 井口油温最大值           | ℃           | NUMBER(8,2)    | Y            |        |               |
| 66       | wellheadfluidtemperaturemin   | 井口油温最小值           | ℃           | NUMBER(8,2)    | Y            |        |               |
| 67       | productiongasoilratio         | 生产气油比               |             | NUMBER(8,2)    | Y            |        |               |
| 68       | productiongasoilratiomax      | 生产气油比最大值         |             | NUMBER(8,2)    | Y            |        |               |
| 69       | productiongasoilratiomin      | 生产气油比最小值         |             | NUMBER(8,2)    | Y            |        |               |
| 70       | producingfluidlevel           | 动液面                   | m           | NUMBER(8,2)    | Y            |        |               |
| 71       | producingfluidlevelmax        | 动液面最大值             | m           | NUMBER(8,2)    | Y            |        |               |
| 72       | producingfluidlevelmin        | 动液面最小值             | m           | NUMBER(8,2)    | Y            |        |               |
| 73       | pumpsettingdepth              | 泵挂                     | m           | NUMBER(8,2)    | Y            |        |               |
| 74       | pumpsettingdepthmax           | 泵挂最大值               | m           | NUMBER(8,2)    | Y            |        |               |
| 75       | pumpsettingdepthmin           | 泵挂最小值               | m           | NUMBER(8,2)    | Y            |        |               |
| 76       | submergence                   | 沉没度                   | m           | NUMBER(8,2)    | Y            |        |               |
| 77       | submergencemax                | 沉没度最大值             | m           | NUMBER(8,2)    | Y            |        |               |
| 78       | submergencemin                | 沉没度最小值             | m           | NUMBER(8,2)    | Y            |        |               |
| 79       | pumpborediameter              | 泵径                     | mm          | NUMBER(8,2)    | Y            |        |               |
| 80       | pumpborediametermax           | 泵径最大值               | mm          | NUMBER(8,2)    | Y            |        |               |
| 81       | pumpborediametermin           | 泵径最小值               | mm          | NUMBER(8,2)    | Y            |        |               |
| 82       | systemefficiency              | 系统效率                 | 小数        | NUMBER(10,4)   | Y            |        |               |
| 83       | systemefficiencymax           | 系统效率最大值           | 小数        | NUMBER(10,4)   | Y            |        |               |
| 84       | systemefficiencymin           | 系统效率最小值           | 小数        | NUMBER(10,4)   | Y            |        |               |
| 85       | surfacesystemefficiency       | 地面效率                 | 小数        | NUMBER(10,4)   | Y            |        |               |
| 86       | surfacesystemefficiencymax    | 地面效率最大值           | 小数        | NUMBER(10,4)   | Y            |        |               |
| 87       | surfacesystemefficiencymin    | 地面效率最小值           | 小数        | NUMBER(10,4)   | Y            |        |               |
| 88       | welldownsystemefficiency      | 井下效率                 | 小数        | NUMBER(10,4)   | Y            |        |               |
| 89       | welldownsystemefficiencymax   | 井下效率最大值           | 小数        | NUMBER(10,4)   | Y            |        |               |
| 90       | welldownsystemefficiencymin   | 井下效率最小值           | 小数        | NUMBER(10,4)   | Y            |        |               |
| 91       | powerconsumptionperthm        | 吨液百米耗电量           | kW·h/100m·t | NUMBER(8,2)    | Y            |        |               |
| 92       | powerconsumptionperthmmax     | 吨液百米耗电量最大值     | kW·h/100m·t | NUMBER(8,2)    | Y            |        |               |
| 93       | powerconsumptionperthmmin     | 吨液百米耗电量最小值     | kW·h/100m·t | NUMBER(8,2)    | Y            |        |               |
| 94       | pumpeff                       | 总泵效                   | 小数        | NUMBER(10,4)   | Y            |        |               |
| 95       | pumpeffmax                    | 总泵效最大值             | 小数        | NUMBER(10,4)   | Y            |        |               |
| 96       | pumpeffmin                    | 总泵效最小值             | 小数        | NUMBER(10,4)   | Y            |        |               |
| 97       | ia                            | A相电流                  | A           | NUMBER(8,2)    | Y            |        |               |
| 98       | iamax                         | A相电流最大值            | A           | NUMBER(8,2)    | Y            |        |               |
| 99       | iamin                         | A相电流最小值            | A           | NUMBER(8,2)    | Y            |        |               |
| 100      | ib                            | B相电流                  | A           | NUMBER(8,2)    | Y            |        |               |
| 101      | ibmax                         | B相电流最大值            | A           | NUMBER(8,2)    | Y            |        |               |
| 102      | ibmin                         | B相电流最小值            | A           | NUMBER(8,2)    | Y            |        |               |
| 103      | ic                            | C相电流                  | A           | NUMBER(8,2)    | Y            |        |               |
| 104      | icmax                         | C相电流最大值            | A           | NUMBER(8,2)    | Y            |        |               |
| 105      | icmin                         | C相电流最小值            | A           | NUMBER(8,2)    | Y            |        |               |
| 106      | va                            | A相电压                  | V           | NUMBER(8,2)    | Y            |        |               |
| 107      | vamax                         | A相电压最大值            | V           | NUMBER(8,2)    | Y            |        |               |
| 108      | vamin                         | A相电压最小值            | V           | NUMBER(8,2)    | Y            |        |               |
| 109      | vb                            | B相电压                  | V           | NUMBER(8,2)    | Y            |        |               |
| 110      | vbmax                         | B相电压最大值            | V           | NUMBER(8,2)    | Y            |        |               |
| 111      | vbmin                         | B相电压最小值            | V           | NUMBER(8,2)    | Y            |        |               |
| 112      | vc                            | C相电压                  | V           | NUMBER(8,2)    | Y            |        |               |
| 113      | vcmax                         | C相电压最大值            | V           | NUMBER(8,2)    | Y            |        |               |
| 114      | vcmin                         | C相电压最小值            | V           | NUMBER(8,2)    | Y            |        |               |
| 115      | wattsum                       | 有功功率                 | kW          | NUMBER(8,2)    | Y            |        |               |
| 116      | wattsummax                    | 有功功率最大值           | kW          | NUMBER(8,2)    | Y            |        |               |
| 117      | wattsummin                    | 有功功率最小值           | kW          | NUMBER(8,2)    | Y            |        |               |
| 118      | varsum                        | 无功功率                 | kVar        | NUMBER(8,2)    | Y            |        |               |
| 119      | varsummax                     | 无功功率最大值           | kVar        | NUMBER(8,2)    | Y            |        |               |
| 120      | varsummin                     | 无功功率最小值           | kVar        | NUMBER(8,2)    | Y            |        |               |
| 121      | pfsum                         | 功率因数                 |             | NUMBER(8,2)    | Y            |        |               |
| 122      | pfsummax                      | 功率因数最大值           |             | NUMBER(8,2)    | Y            |        |               |
| 123      | pfsummin                      | 功率因数最小值           |             | NUMBER(8,2)    | Y            |        |               |
| 124      | frequency                     | 运行频率                 | HZ          | NUMBER(8,2)    | Y            |        |               |
| 125      | frequencymax                  | 运行频率最大值           | HZ          | NUMBER(8,2)    | Y            |        |               |
| 126      | frequencymin                  | 运行频率最小值           | HZ          | NUMBER(8,2)    | Y            |        |               |
| 127      | todaywattenergy               | 日有功电能               | kW·h        | NUMBER(8,2)    | Y            |        |               |
| 128      | todaypwattenergy              | 日正向有功电能           | kW·h        | NUMBER(8,2)    | Y            |        |               |
| 129      | todaynwattenergy              | 日反向有功电能           | kW·h        | NUMBER(8,2)    | Y            |        |               |
| 130      | todayvarenergy                | 日无功电能               | kVar·h      | NUMBER(8,2)    | Y            |        |               |
| 131      | todaypvarenergy               | 日正向无功电能           | kVar·h      | NUMBER(8,2)    | Y            |        |               |
| 132      | todaynvarenergy               | 日反向无功电能           | kVar·h      | NUMBER(8,2)    | Y            |        |               |
| 133      | todayvaenergy                 | 日视在电能               | kVA·h       | NUMBER(8,2)    | Y            |        |               |
| 134      | totalwattenergy               | 累计有功电能             | kW·h        | NUMBER(8,2)    | Y            |        |               |
| 135      | totalpwattenergy              | 累计正向有功电能         | kW·h        | NUMBER(8,2)    | Y            |        |               |
| 136      | totalnwattenergy              | 累计反向有功电能         | kW·h        | NUMBER(8,2)    | Y            |        |               |
| 137      | totalvarenergy                | 累计无功电能             | kVar·h      | NUMBER(8,2)    | Y            |        |               |
| 138      | totalpvarenergy               | 累计正向无功电能         | kVar·h      | NUMBER(8,2)    | Y            |        |               |
| 139      | totalnvarenergy               | 累计反向无功电能         | kVar·h      | NUMBER(8,2)    | Y            |        |               |
| 140      | totalvaenergy                 | 累计视在电能             | kVA·h       | NUMBER(8,2)    | Y            |        |               |
| 141      | rpm                           | 螺杆泵转速               | r/min       | NUMBER(8,2)    | Y            |        |               |
| 142      | rpmmax                        | 螺杆泵转速最大值         | r/min       | NUMBER(8,2)    | Y            |        |               |
| 143      | rpmmin                        | 螺杆泵转速最小值         | r/min       | NUMBER(8,2)    | Y            |        |               |
| 144      | extendeddays                  | 延用天数                 |             | NUMBER(5)      | Y            |        |               |
| 145      | resultstatus                  | 计算标志                 |             | NUMBER(2)      | Y            |        |               |
| 146      | signal                        | 信号强度                 |             | NUMBER(8,2)    | Y            |        |               |
| 147      | signalmax                     | 信号强度最大值           |             | NUMBER(8,2)    | Y            |        |               |
| 148      | signalmin                     | 信号强度最小值           |             | NUMBER(8,2)    | Y            |        |               |
| 149      | f                             | 载荷                     | kN          | NUMBER(8,2)    | Y            |        |               |
| 150      | fmax                          | 载荷最大值               | kN          | NUMBER(8,2)    | Y            |        |               |
| 151      | fmin                          | 载荷最小值               | kN          | NUMBER(8,2)    | Y            |        |               |
| 152      | savetime                      | 存储时间                 |             | DATE           | Y            |        | SYSDATE       |

### 1.3.23 tbl_rpc_statistics_conf 抽油机统计配置表

| **序号** | **字段代码** | **字段名** | **单位** | **字段类型** | **是否为空** | **键** | **备注** |
|----------|--------------|------------|----------|--------------|--------------|--------|----------|
| 1        | id           | 记录编号   |          | NUMBER（10） | N            | 主键   |          |
| 2        | s_level      | 级别       |          | VARCHAR2(50) | Y            |        |          |
| 3        | s_code       | 代码       |          | NUMBER(4)    | Y            |        |          |
| 4        | s_min        | 范围最小值 |          | NUMBER(11,3) | Y            |        |          |
| 5        | s_max        | 范围最大值 |          | NUMBER(11,3) | Y            |        |          |
| 6        | s_type       | 统计类型   |          | VARCHAR2(20) | Y            |        |          |

### 1.3.24 tbl_rpcinformation 抽油机设备表

| **序号** | **字段代码**                  | **字段名**       | **单位** | **字段类型**  | **是否为空** | **键** | **备注**                             |
|----------|-------------------------------|------------------|----------|---------------|--------------|--------|--------------------------------------|
| 1        | id                            | 记录编号         |          | NUMBER(10)    | N            | 主键   |                                      |
| 2        | wellid                        | 井编号           |          | NUMBER(10)    | Y            | 外键   |                                      |
| 3        | manufacturer                  | 抽油机厂家       |          | VARCHAR2(200) | Y            |        |                                      |
| 4        | model                         | 抽油机型号       |          | VARCHAR2(200) | Y            |        |                                      |
| 5        | stroke                        | 冲程             | m        | NUMBER(8,2)   | N            |        |                                      |
| 6        | crankrotationdirection        | 旋转方向         |          | VARCHAR2(200) | N            |        | Clockwise-顺时针Anticlockwise-逆时针 |
| 7        | offsetangleofcrank            | 曲柄偏置角       | °        | NUMBER(8,2)   | N            |        |                                      |
| 8        | crankgravityradius            | 曲柄重心半径     | m        | NUMBER(10,4)  | N            |        |                                      |
| 9        | singlecrankweight             | 单块曲柄重量     | kN       | NUMBER(8,2)   | N            |        |                                      |
| 10       | structuralunbalance           | 结构不平衡重     | kN       | NUMBER(8,2)   | N            |        |                                      |
| 11       | gearreducerratio              | 减速箱传动比     |          | NUMBER(10,4)  | N            |        |                                      |
| 12       | gearreducerbeltpulleydiameter | 减速箱皮带轮直径 | m        | NUMBER(10,4)  | N            |        |                                      |
| 13       | balanceposition               | 平衡块位置       | m        | VARCHAR2(200) | N            |        |                                      |
| 14       | balanceweight                 | 平衡块重量       | kN       | VARCHAR2(200) | N            |        |                                      |
| 15       | prtf                          | 位置扭矩因数     |          | CLOB          | Y            |        |                                      |

### 1.3.25 tbl_rpc_motor 抽油机电机数据表

| **序号** | **字段代码**       | **字段名** | **单位** | **字段类型**  | **是否为空** | **键** | **备注** |
|----------|--------------------|------------|----------|---------------|--------------|--------|----------|
| 1        | id                 | 记录编号   |          | NUMBER(10)    | N            | 主键   |          |
| 2        | wellid             | 井编号     |          | NUMBER(10)    | N            | 外键   |          |
| 3        | manufacturer       | 电机厂家   |          | VARCHAR2(200) | N            |        |          |
| 4        | model              | 电机型号   |          | VARCHAR2(200) | N            |        |          |
| 5        | synchrospeed       | 同步转速   | r/min    | NUMBER(8,2)   | Y            |        |          |
| 6        | beltpulleydiameter | 皮带轮直径 | m        | NUMBER(10,4)  | Y            |        |          |
| 7        | performancecurver  | 特性曲线   |          | CLOB          |              |        |          |

### 1.3.26 tbl_rpc_inver_opt 抽油机电参反演参数优化表

| **序号** | **字段代码**            | **字段名**           | **单位** | **字段类型** | **是否为空** | **键** | **备注** |
|----------|-------------------------|----------------------|----------|--------------|--------------|--------|----------|
| 1        | id                      | 记录编号             |          | NUMBER(10)   | N            | 主键   |          |
| 2        | wellid                  | 井编号               |          | NUMBER(10)   | Y            | 外键   |          |
| 3        | offsetangleofcrankps    | 曲柄位置开关偏置角   | °        | NUMBER(8,2)  | Y            |        |          |
| 4        | surfacesystemefficiency | 地面效率             | 小数     | NUMBER(8,2)  | Y            |        |          |
| 5        | fs_leftpercent          | 功图左侧截取百分比   | %        | NUMBER(8,2)  | Y            |        |          |
| 6        | fs_rightpercent         | 功图又侧截取百分比   | %        | NUMBER(8,2)  | Y            |        |          |
| 7        | filtertime_watt         | 功率曲线滤波次数     |          | NUMBER(3)    | Y            |        |          |
| 8        | filtertime_i            | 电流曲线滤波次数     |          | NUMBER(3)    | Y            |        |          |
| 9        | filtertime_fsdiagram    | 地面功图滤波次数     |          | NUMBER(3)    | Y            |        |          |
| 10       | filtertime_rpm          | 转速曲线滤波次数     |          | NUMBER(3)    | Y            |        |          |
| 11       | filtertime_fsdiagram_l  | 地面功图左侧滤波次数 |          | NUMBER(3)    | Y            |        |          |
| 12       | filtertime_fsdiagram_r  | 地面功图右侧滤波次数 |          | NUMBER(3)    | Y            |        |          |
| 13       | wattangle               | 功率滤波角度         | °        | NUMBER(8,2)  | Y            |        |          |

# 二、视图

## 2.1 视图概览

| **序号** | **名称**                                                                        | **描述**               |
|----------|---------------------------------------------------------------------------------|------------------------|
| 1        | [viw_wellinformation](database/View-20200226.xlsx#油井信息数据!A1)              | 油井信息视图           |
| 2        | [viw_rpc_productiondata_latest](database/View-20200226.xlsx#生产数据实时!A1)    | 抽油机生产数据实时视图 |
| 3        | viw_rpc_productiondata_hist                                                     | 抽油机生产数据历史视图 |
| 4        | [viw_commstatus](database/View-20200226.xlsx#通信状态!A1)                       | 通信状态视图           |
| 5        | [viw_rpc_diagram_latest](database/View-20200226.xlsx#曲线分析实时数据!A1)       | 抽油机曲线数据实时视图 |
| 6        | [viw_rpc_diagram_hist](database/View-20200226.xlsx#曲线分析历史数据!A1)         | 抽油机曲线数据历史视图 |
| 7        | [viw_rpc_discrete_latest](database/View-20200226.xlsx#电参分析实时数据!A1)      | 抽油机电参数据实时视图 |
| 8        | [viw_rpc_discrete_hist](database/View-20200226.xlsx#电参分析历史数据!A1)        | 抽油机电参数据历史视图 |
| 9        | [viw_rpc_comprehensive_latest](database/View-20200226.xlsx#综合分析实时数据!A1) | 抽油机综合数据实时视图 |
| 10       | [viw_rpc_comprehensive_hist](database/View-20200226.xlsx#综合分析历史数据!A1)   | 抽油机综合数据历史视图 |
| 11       | [viw_rpc_diagramquery_latest](database/View-20200226.xlsx#图形查询实时数据!A1)  | 抽油机图形查询实时视图 |
| 12       | [viw_rpc_diagramquery_hist](database/View-20200226.xlsx#图形查询历史数据!A1)    | 抽油机图形查询历史视图 |
| 13       | [viw_rpc_total_day](database/View-20200226.xlsx#全天评价数据!A1)                | 抽油机日累计数据视图   |
| 14       | [viw_rpc_calculatemain](database/View-20200226.xlsx#计算结果管理!A1)            | 抽油机计算结果管理视图 |

## 2.2 详述

### 2.2.1 viw_wellinformation 油井信息视图

| **序号** | **字段名**               | **字段代码**               | **字段类型**  | **单位** | **备注** |
|----------|--------------------------|----------------------------|---------------|----------|----------|
| 1        | 编号                     | id                         | NUMBER(10)    |          |          |
| 2        | 组织名称                 | orgname                    | VARCHAR2(100) |          |          |
| 3        | 组织编号                 | orgid                      | NUMBER(10)    |          |          |
| 4        | 油藏名称                 | resname                    | VARCHAR2(200) |          |          |
| 5        | 井名                     | wellname                   | VARCHAR2(200) |          |          |
| 6        | 举升方式                 | liftingtype                | NUMBER(10)    |          |          |
| 7        | 设备地址                 | driveraddr                 | VARCHAR2(200) |          |          |
| 8        | 设备编号                 | driverid                   | VARCHAR2(200) |          |          |
| 9        | 曲线数据采集周期         | acqcycle_diagram           | NUMBER(10)    |          |          |
| 10       | 曲线数据采集周期设置状态 | acqcyclesetstatus_diagram  | NUMBER(2)     |          |          |
| 11       | 离散数据采集周期         | acqcycle_discrete          | NUMBER(10)    |          |          |
| 12       | 离散数据采集周期设置状态 | acqcyclesetstatus_discrete | NUMBER(2)     |          |          |
| 13       | 离散数据保存周期         | savecycle_discrete         | NUMBER(10)    |          |          |
| 14       | 时率来源                 | runtimeefficiencysource    | VARCHAR2(200) |          |          |
| 15       | 视频路径                 | videourl                   | VARCHAR2(400) |          |          |
| 16       | 举升方式名称             | liftingtypename            | VARCHAR2(200) |          |          |
| 17       | 驱动代码                 | drivercode                 | VARCHAR2(50)  |          |          |
| 18       | 采集组代码               | acquisitionunit            | VARCHAR2(50)  |          |          |
| 19       | 排序编号                 | sortnum                    | NUMBER(10)    |          |          |

### 2.2.2 viw_rpc_productiondata_latest 抽油机生产数据实时视图

| **序号** | **字段名**     | **字段代码**               | **字段类型**  | **单位** | **备注** |
|----------|----------------|----------------------------|---------------|----------|----------|
| 1        | 编号           | id                         | NUMBER(10)    |          |          |
| 2        | 井名           | wellname                   | VARCHAR2(200) |          |          |
| 3        | 井编号         | wellid                     | NUMBER(10)    |          |          |
| 4        | 举升类型       | liftingtype                | NUMBER(10)    |          |          |
| 5        | 采集时间       | acquisitiontime            | DATE          |          |          |
| 6        | 运行时间       | runtime                    | NUMBER(8,2)   |          |          |
| 7        | 原油密度       | crudeoildensity            | NUMBER(16,2)  |          |          |
| 8        | 水密度         | waterdensity               | NUMBER(16,2)  |          |          |
| 9        | 天然气相对密度 | naturalgasrelativedensity  | NUMBER(16,2)  |          |          |
| 10       | 饱和压力       | saturationpressure         | NUMBER(16,2)  |          |          |
| 11       | 油藏深度       | reservoirdepth             | NUMBER(16,2)  |          |          |
| 12       | 油藏温度       | reservoirtemperature       | NUMBER(16,2)  |          |          |
| 13       | 重量含水率     | watercut_w                 | NUMBER(8,2)   |          |          |
| 14       | 体积含水率     | watercut                   | NUMBER(8,2)   |          |          |
| 15       | 油压           | tubingpressure             | NUMBER(8,2)   |          |          |
| 16       | 套压           | casingpressure             | NUMBER(8,2)   |          |          |
| 17       | 回压           | backpressure               | NUMBER(8,2)   |          |          |
| 18       | 井口油温       | wellheadfluidtemperature   | NUMBER(8,2)   |          |          |
| 19       | 动液面         | producingfluidlevel        | NUMBER(8,2)   |          |          |
| 20       | 泵挂           | pumpsettingdepth           | NUMBER(8,2)   |          |          |
| 21       | 生产汽油比     | productiongasoilratio      | NUMBER(8,2)   |          |          |
| 22       | 泵径           | pumpborediameter           | NUMBER(8,2)   |          |          |
| 23       | 泵类型         | pumptype                   | VARCHAR2(20)  |          |          |
| 24       | 泵类型名称     | pumptypename               | VARCHAR2(200) |          |          |
| 25       | 泵级别         | pumpgrade                  | NUMBER(1)     |          |          |
| 26       | 柱塞长         | plungerlength              | NUMBER(8,2)   |          |          |
| 27       | 泵筒类型       | barreltype                 | VARCHAR2(20)  |          |          |
| 28       | 泵筒类型名称   | barreltypename             | VARCHAR2(200) |          |          |
| 29       | 泵筒长         | barrellength               | NUMBER(8,2)   |          |          |
| 30       | 泵级数         | barrelseries               | NUMBER(8,2)   |          |          |
| 31       | 转子截面直径   | rotordiameter              | NUMBER(8,2)   |          |          |
| 32       | 转速           | qpr                        | NUMBER(8,2)   |          |          |
| 33       | 油管内径       | tubingstringinsidediameter | NUMBER(8,2)   |          |          |
| 34       | 套管内径       | casingstringinsidediameter | NUMBER(8,2)   |          |          |
| 35       | 杆数据         | rodstring                  | VARCHAR2(200) |          |          |
| 36       | 锚定状态       | anchoringstate             | NUMBER(1)     |          |          |
| 37       | 锚定状态名称   | anchoringstatename         | VARCHAR2(200) |          |          |
| 38       | 净毛比         | netgrossratio              | NUMBER(8,2)   |          |          |
| 39       | 人工干预代码   | manualintervention         | NUMBER(4)     |          |          |
| 40       | 井排序编号     | sortnum                    | NUMBER(10)    |          |          |
| 41       | 组织编号       | org_id                     | NUMBER(10)    |          |          |

### 2.2.3 viw_rpc_productiondata_hist 抽油机生产数据历史视图

同viw_rpc_productiondata_latest

### 2.2.4 viw_commstatus 通信状态视图 

| **序号** | **字段名** | **字段代码** | **字段类型**  | **单位** | **备注** |
|----------|------------|--------------|---------------|----------|----------|
| 1        | 编号       | id           | NUMBER(10)    |          |          |
| 2        | 井名       | wellname     | VARCHAR2(200) |          |          |
| 3        | 通信状态   | commstatus   | NUMBER(1)     |          |          |

### 2.2.5 viw_rpc_diagram_latest 抽油机曲线数据实时视图

| **序号** | **字段名**           | **字段代码**                  | **字段类型**  | **单位** | **备注** |
|----------|----------------------|-------------------------------|---------------|----------|----------|
| 1        | 编号                 | id                            | NUMBER(10)    |          |          |
| 2        | 井名                 | wellname                      | VARCHAR2(200) |          |          |
| 3        | 井编号               | wellid                        | NUMBER(10)    |          |          |
| 4        | 举升类型             | liftingtype                   | NUMBER(10)    |          |          |
| 5        | 采集时间             | acquisitiontime               | DATE          |          |          |
| 6        | 通信状态             | commstatus                    | NUMBER(1)     |          |          |
| 7        | 通信状态名称         | commstatusname                | VARCHAR2      |          |          |
| 8        | 通信报警级别         | commalarmlevel                | NUMBER(3)     |          |          |
| 9        | 工况代码             | workingconditioncode          | NUMBER(4)     |          |          |
| 10       | 工况名称             | workingconditionname          | VARCHAR2(200) |          |          |
| 11       | 优化建议             | optimizationsuggestion        | VARCHAR2(200) |          |          |
| 12       | 工况报警级别         | workingconditionrunalarmlevel | NUMBER(3)     |          |          |
| 13       | 理论排量             | theoreticalproduction         | NUMBER(8,2)   |          |          |
| 14       | 产液量               | liquidweightproduction        | NUMBER(8,2)   |          |          |
| 15       | 产油量               | oilweightproduction           | NUMBER(8,2)   |          |          |
| 16       | 产水量               | waterweightproduction         | NUMBER(8,2)   |          |          |
| 17       | 含水率               | watercut_w                    | NUMBER(8,2)   |          |          |
| 18       | 产液级别             | liquidweightproductionlevel   | VARCHAR2(50)  |          |          |
| 19       | 生产汽油比           | productiongasoilratio         | NUMBER(8,2)   |          |          |
| 20       | 油压                 | tubingpressure                | NUMBER(8,2)   |          |          |
| 21       | 套压                 | casingpressure                | NUMBER(8,2)   |          |          |
| 22       | 井口油温             | wellheadfluidtemperature      | NUMBER(8,2)   |          |          |
| 23       | 动液面               | producingfluidlevel           | NUMBER(8,2)   |          |          |
| 24       | 泵挂                 | pumpsettingdepth              | NUMBER(8,2)   |          |          |
| 25       | 沉没度               | submergence                   | NUMBER(8,2)   |          |          |
| 26       | 泵径                 | pumpborediameter              | NUMBER(8,2)   |          |          |
| 27       | 原油密度             | crudeoildensity               | NUMBER(16,2)  |          |          |
| 28       | 净毛比               | netgrossratio                 | NUMBER(8,2)   |          |          |
| 29       | 柱塞有效冲程计算产量 | availableplungerstrokeprod    | NUMBER(8,2)   |          |          |
| 30       | 泵间隙漏失量         | pumpclearanceleakprod         | NUMBER(8,2)   |          |          |
| 31       | 游动凡尔漏失量       | tvleakweightproduction        | NUMBER(8,2)   |          |          |
| 32       | 固定凡尔漏失量       | svleakweightproduction        | NUMBER(8,2)   |          |          |
| 33       | 气影响               | gasinfluenceprod              | NUMBER(8,2)   |          |          |
| 34       | 抽油杆数据           | rodstring                     | VARCHAR2(200) |          |          |
| 35       | 冲程                 | stroke                        | NUMBER(8,2)   |          |          |
| 36       | 冲次                 | spm                           | NUMBER(8,2)   |          |          |
| 37       | 理论上载荷           | upperloadline                 | NUMBER(8,2)   |          |          |
| 38       | 真实理论上载荷       | upperloadlineofexact          | NUMBER(8,2)   |          |          |
| 39       | 理论下载荷           | lowerloadline                 | NUMBER(8,2)   |          |          |
| 40       | 最大载荷             | fmax                          | NUMBER(8,2)   |          |          |
| 41       | 最小载荷             | fmin                          | NUMBER(8,2)   |          |          |
| 42       | 电机输入有功功率     | motorinputactivepower         | NUMBER(8,2)   |          |          |
| 43       | 光杆功率             | polishrodpower                | NUMBER(8,2)   |          |          |
| 44       | 水功率               | waterpower                    | NUMBER(8,2)   |          |          |
| 45       | 系统效率             | systemefficiency              | NUMBER(12,3)  |          |          |
| 46       | 系统效率级别         | systemefficiencylevel         | VARCHAR2(50)  |          |          |
| 47       | 地面效率             | surfacesystemefficiency       | NUMBER(12,3)  |          |          |
| 48       | 地面效率级别         | surfacesystemefficiencylevel  | VARCHAR2(50)  |          |          |
| 49       | 井下效率             | welldownsystemefficiency      | NUMBER(12,3)  |          |          |
| 50       | 井下效率级别         | welldownsystemefficiencylevel | VARCHAR2(50)  |          |          |
| 51       | 功图面积             | fsdiagramarea                 | NUMBER(8,2)   |          |          |
| 52       | 吨液百米耗电量       | powerconsumptionperthm        | NUMBER(8,2)   |          |          |
| 53       | 电流平衡度           | idegreebalance                | NUMBER(8,2)   |          |          |
| 54       | 电流平衡状态         | idegreebalancename            | VARCHAR2(200) |          |          |
| 55       | 上冲程最大电流       | upstrokeimax                  | NUMBER(8,2)   |          |          |
| 56       | 下冲程最大电流       | downstrokeimax                | NUMBER(8,2)   |          |          |
| 57       | 电流平衡报警级别     | idegreebalancealarmlevel      | NUMBER(3)     |          |          |
| 58       | 功率平衡度           | wattdegreebalance             | NUMBER(8,2)   |          |          |
| 59       | 功率平衡状态         | wattdegreebalancename         | VARCHAR2(200) |          |          |
| 60       | 上冲程最大功率       | upstrokewattmax               | NUMBER(8,2)   |          |          |
| 61       | 下冲程最大功率       | downstrokewattmax             | NUMBER(8,2)   |          |          |
| 62       | 功率平衡报警级别     | wattdegreebalancealarmlevel   | NUMBER(3)     |          |          |
| 63       | 冲程损失系数         | pumpeff1                      | NUMBER(12,3)  |          |          |
| 64       | 充满系数             | pumpeff2                      | NUMBER(12,3)  |          |          |
| 65       | 间隙漏失系数         | pumpeff3                      | NUMBER(12,3)  |          |          |
| 66       | 液体收缩系数         | pumpeff4                      | NUMBER(12,3)  |          |          |
| 67       | 总泵效               | pumpeff                       | NUMBER(12,3)  |          |          |
| 68       | 抽油杆伸长量         | rodflexlength                 | NUMBER(8,2)   |          |          |
| 69       | 油管伸缩值           | tubingflexlength              | NUMBER(8,2)   |          |          |
| 70       | 惯性载荷增量         | inertialength                 | NUMBER(8,2)   |          |          |
| 71       | 泵入口压力           | pumpintakep                   | NUMBER(8,2)   |          |          |
| 72       | 泵入口温度           | pumpintaket                   | NUMBER(8,2)   |          |          |
| 73       | 泵入口就地气液比     | pumpintakegol                 | NUMBER(8,2)   |          |          |
| 74       | 泵入口粘度           | pumpinletvisl                 | NUMBER(8,2)   |          |          |
| 75       | 泵入口原油体积系数   | pumpinletbo                   | NUMBER(8,2)   |          |          |
| 76       | 泵出口压力           | pumpoutletp                   | NUMBER(8,2)   |          |          |
| 77       | 泵出口温度           | pumpoutlett                   | NUMBER(8,2)   |          |          |
| 78       | 泵出口就地气液比     | pumpoutletgol                 | NUMBER(8,2)   |          |          |
| 79       | 泵出口粘度           | pumpoutletvisl                | NUMBER(8,2)   |          |          |
| 80       | 泵出口原油体积系数   | pumpoutletbo                  | NUMBER(8,2)   |          |          |
| 81       | 视频路径             | videourl                      | VARCHAR2(400) |          |          |
| 82       | 组织标号             | org_id                        | NUMBER(10)    |          |          |
| 83       | 组织代码             | org_code                      | VARCHAR2(20)  |          |          |
| 84       | 井排序编号           | sortnum                       | NUMBER(10)    |          |          |

### 2.2.6 viw_rpc_diagram_hist 抽油机曲线数据历史视图

同viw_rpc_diagram_latest

### 2.2.7 viw_rpc_discrete_latest 抽油机电参数据实时视图

| **序号** | **字段名**       | **字段代码**                | **字段类型**   | **单位** | **备注** |
|----------|------------------|-----------------------------|----------------|----------|----------|
| 1        | 编号             | id                          | NUMBER(10)     |          |          |
| 2        | 井名             | wellname                    | VARCHAR2(200)  |          |          |
| 3        | 举升类型         | liftingtype                 | NUMBER(10)     |          |          |
| 4        | 举升类型名称     | liftingtypename             | VARCHAR2(200)  |          |          |
| 5        | 井编号           | wellid                      | NUMBER(10)     |          |          |
| 6        | 通信状态         | commstatus                  | NUMBER(1)      |          |          |
| 7        | 通信状态名称     | commstatusname              | VARCHAR2       |          |          |
| 8        | 通信报警级别     | commalarmlevel              | NUMBER(4)      |          |          |
| 9        | 运行状态         | runstatus                   | NUMBER(1)      |          |          |
| 10       | 运行状态名称     | runstatusname               | VARCHAR2       |          |          |
| 11       | 运行状态报警级别 | runalarmlevel               | NUMBER(3)      |          |          |
| 12       | 通信时间         | commtime                    | NUMBER(8,2)    |          |          |
| 13       | 通信区间         | commrange                   | VARCHAR2(2000) |          |          |
| 14       | 通信时率         | commtimeefficiency          | NUMBER(10,4)   |          |          |
| 15       | 通信时率级别     | commtimeefficiencylevel     | VARCHAR2(50)   |          |          |
| 16       | 运行时间         | runtime                     | NUMBER(8,2)    |          |          |
| 17       | 运行区间         | runrange                    | VARCHAR2(2000) |          |          |
| 18       | 生产时率         | runtimeefficiency           | NUMBER(10,4)   |          |          |
| 19       | 生产时率等级     | runtimeefficiencylevel      | VARCHAR2(50)   |          |          |
| 20       | 采集时间         | acquisitiontime             | DATE           |          |          |
| 21       | 工况代码         | workingconditioncode_elec   | NUMBER(4)      |          |          |
| 22       | 工况累计字符串   | workingconditionstring_elec | VARCHAR2(4000) |          |          |
| 23       | 工况名称         | workingconditionname_elec   | VARCHAR2(200)  |          |          |
| 24       | 优化建议         | optimizationsuggestion_elec | VARCHAR2(200)  |          |          |
| 25       | 工况报警等级     | workingconditionalarmlevel  | NUMBER(3)      |          |          |
| 26       | 日有功功耗       | todaywattenergy             | NUMBER(8,2)    |          |          |
| 27       | 日耗电量等级     | todaywattenergylevel        | VARCHAR2(50)   |          |          |
| 28       | 日正向有功功耗   | todaypwattenergy            | NUMBER(8,2)    |          |          |
| 29       | 日反向有功功耗   | todaynwattenergy            | NUMBER(8,2)    |          |          |
| 30       | 日无功功耗       | todayvarenergy              | NUMBER(8,2)    |          |          |
| 31       | 日正向无功功耗   | todaypvarenergy             | NUMBER(8,2)    |          |          |
| 32       | 日反向无功功耗   | todaynvarenergy             | NUMBER(8,2)    |          |          |
| 33       | 日视在功耗       | todayvaenergy               | NUMBER(8,2)    |          |          |
| 34       | A相电流          | ia                          | NUMBER(8,2)    |          |          |
| 35       | B相电流          | ib                          | NUMBER(8,2)    |          |          |
| 36       | C相电流          | ic                          | NUMBER(8,2)    |          |          |
| 37       | 三项平均电流     | iavg                        | NUMBER(8,2)    |          |          |
| 38       | 电流字符串       | istr                        | VARCHAR2       |          |          |
| 39       | A相电流上限      | iauplimit                   | NUMBER(8,2)    |          |          |
| 40       | A相电流下限      | iadownlimit                 | NUMBER(8,2)    |          |          |
| 41       | A相电流零值      | iazero                      | NUMBER(8,2)    |          |          |
| 42       | B相电流上限      | ibuplimit                   | NUMBER(8,2)    |          |          |
| 43       | B相电流下限      | ibdownlimit                 | NUMBER(8,2)    |          |          |
| 44       | B相电流零值      | ibzero                      | NUMBER(8,2)    |          |          |
| 45       | C相电流上限      | icuplimit                   | NUMBER(8,2)    |          |          |
| 46       | C相电流下限      | icdownlimit                 | NUMBER(8,2)    |          |          |
| 47       | C相电流零值      | iczero                      | NUMBER(8,2)    |          |          |
| 48       | A相电压          | va                          | NUMBER(8,2)    |          |          |
| 49       | B相电压          | vb                          | NUMBER(8,2)    |          |          |
| 50       | C相电压          | vc                          | NUMBER(8,2)    |          |          |
| 51       | 三项平均电压     | vavg                        | NUMBER(8,2)    |          |          |
| 52       | 电压字符串       | vstr                        | VARCHAR2       |          |          |
| 53       | A相电压上限      | vauplimit                   | NUMBER(8,2)    |          |          |
| 54       | A相电压下限      | vadownlimit                 | NUMBER(8,2)    |          |          |
| 55       | A相电压零值      | vazero                      | NUMBER(8,2)    |          |          |
| 56       | B相电压上限      | vbuplimit                   | NUMBER(8,2)    |          |          |
| 57       | B相电压下限      | vbdownlimit                 | NUMBER(8,2)    |          |          |
| 58       | B相电压零值      | vbzero                      | NUMBER(8,2)    |          |          |
| 59       | C相电压上限      | vcuplimit                   | NUMBER(8,2)    |          |          |
| 60       | C相电压下限      | vcdownlimit                 | NUMBER(8,2)    |          |          |
| 61       | C相电压零值      | vczero                      | NUMBER(8,2)    |          |          |
| 62       | 累计有功功耗     | totalwattenergy             | NUMBER(8,2)    |          |          |
| 63       | 累计正向有功功耗 | totalpwattenergy            | NUMBER(8,2)    |          |          |
| 64       | 累计反向有功功耗 | totalnwattenergy            | NUMBER(8,2)    |          |          |
| 65       | 累计无功功耗     | totalvarenergy              | NUMBER(8,2)    |          |          |
| 66       | 累计正向无功功耗 | totalpvarenergy             | NUMBER(8,2)    |          |          |
| 67       | 累计反向无功功耗 | totalnvarenergy             | NUMBER(8,2)    |          |          |
| 68       | 累计视在功耗     | totalvaenergy               | NUMBER(8,2)    |          |          |
| 69       | A相有功功率      | watta                       | NUMBER(8,2)    |          |          |
| 70       | B相有功功率      | wattb                       | NUMBER(8,2)    |          |          |
| 71       | C相有功功率      | wattc                       | NUMBER(8,2)    |          |          |
| 72       | 三相总有功功率   | wattsum                     | NUMBER(8,2)    |          |          |
| 73       | 有功功率字符串   | wattstr                     | VARCHAR2       |          |          |
| 74       | A相无功功率      | vara                        | NUMBER(8,2)    |          |          |
| 75       | B相无功功率      | varb                        | NUMBER(8,2)    |          |          |
| 76       | C相无功功率      | varc                        | NUMBER(8,2)    |          |          |
| 77       | 三相总无功功率   | varsum                      | NUMBER(8,2)    |          |          |
| 78       | 无功功率字符串   | varstr                      | VARCHAR2       |          |          |
| 79       | 反向功率         | reversepower                | NUMBER(8,2)    |          |          |
| 80       | A相功率因数      | pfa                         | NUMBER(8,2)    |          |          |
| 81       | B相功率因数      | pfb                         | NUMBER(8,2)    |          |          |
| 82       | C相功率因数      | pfc                         | NUMBER(8,2)    |          |          |
| 83       | 三项综合功率因数 | pfsum                       | NUMBER(8,2)    |          |          |
| 84       | 功率因数字符串   | pfstr                       | VARCHAR2       |          |          |
| 85       | 设置频率         | frequencysetvalue           | NUMBER(8,2)    |          |          |
| 86       | 运行频率         | frequencyrunvalue           | NUMBER(8,2)    |          |          |
| 87       | 油压             | tubingpressure              | NUMBER(8,2)    |          |          |
| 88       | 套压             | casingpressure              | NUMBER(8,2)    |          |          |
| 89       | 回压             | backpressure                | NUMBER(8,2)    |          |          |
| 90       | 井口油温         | wellheadfluidtemperature    | NUMBER(8,2)    |          |          |
| 91       | 信号强度         | signal                      | NUMBER(8,2)    |          |          |
| 92       | 传输间隔         | interval                    | NUMBER(10)     |          |          |
| 93       | 设备版本         | devicever                   | VARCHAR2(50)   |          |          |
| 94       | 视频路径         | videourl                    | VARCHAR2(400)  |          |          |
| 95       | 井排序编号       | sortnum                     | NUMBER(10)     |          |          |
| 96       | 组织代码         | org_code                    | VARCHAR2(20)   |          |          |
| 97       | 组织编号         | org_id                      | NUMBER(10)     |          |          |

### 2.2.8 viw_rpc_discrete_hist 抽油机电参数据历史视图

同 viw_rpc_discrete_latest

### 2.2.9 viw_rpc_comprehensive_latest 抽油机综合数据实时视图

| **序号** | **字段名**                   | **字段代码**                  | **字段类型**   | **单位** | **备注** |
|----------|------------------------------|-------------------------------|----------------|----------|----------|
| 1        | 编号                         | id                            | NUMBER(10)     |          |          |
| 2        | 井名                         | wellname                      | VARCHAR2(200)  |          |          |
| 3        | 井编号                       | wellid                        | NUMBER(10)     |          |          |
| 4        | 举升类型                     | liftingtype                   | NUMBER(10)     |          |          |
| 5        | 采集时间                     | acquisitiontime               | DATE           |          |          |
| 6        | 通信状态                     | commstatus                    | NUMBER(2)      |          |          |
| 7        | 通信状态名称                 | commstatusname                | VARCHAR2       |          |          |
| 8        | 通信报警级别                 | commalarmlevel                | NUMBER(3)      |          |          |
| 9        | 运行状态                     | runstatus                     | NUMBER(1)      |          |          |
| 10       | 运行状态名称                 | runstatusname                 | VARCHAR2       |          |          |
| 11       | 运行状态报警级别             | runalarmlevel                 | NUMBER(3)      |          |          |
| 12       | 通信时间                     | commtime                      | NUMBER(8,2)    |          |          |
| 13       | 通信区间                     | commrange                     | VARCHAR2(2000) |          |          |
| 14       | 通信时率                     | commtimeefficiency            | NUMBER(10,4)   |          |          |
| 15       | 通信时率级别                 | commtimeefficiencylevel       | VARCHAR2(50)   |          |          |
| 16       | 运行时间                     | runtime                       | NUMBER(8,2)    |          |          |
| 17       | 运行区间                     | runrange                      | VARCHAR2(2000) |          |          |
| 18       | 生产时率                     | runtimeefficiency             | NUMBER(10,4)   |          |          |
| 19       | 生产时率等级                 | runtimeefficiencylevel        | VARCHAR2(50)   |          |          |
| 20       | 工况代码                     | workingconditioncode          | NUMBER(4)      |          |          |
| 21       | 工况名称                     | workingconditionname          | VARCHAR2(200)  |          |          |
| 22       | 优化建议                     | optimizationsuggestion        | VARCHAR2(200)  |          |          |
| 23       | 工况报警级别                 | workingconditionalarmlevel    | VARCHAR2       |          |          |
| 24       | 电参工况代码                 | workingconditioncode_e        | NUMBER(4)      |          |          |
| 25       | 电参功率字符串               | workingconditionstring_e      | VARCHAR2(4000) |          |          |
| 26       | 电参工况名称                 | workingconditionname_e        | VARCHAR2(200)  |          |          |
| 27       | 电参工况优化建议             | optimizationsuggestion_e      | VARCHAR2(200)  |          |          |
| 28       | 电参工况报警级别             | workingconditionalarmlevel_e  | NUMBER(3)      |          |          |
| 29       | 理论排量                     | theoreticalproduction         | NUMBER(8,2)    |          |          |
| 30       | 产液量                       | liquidweightproduction        | NUMBER(8,2)    |          |          |
| 31       | 产油量                       | oilweightproduction           | NUMBER(8,2)    |          |          |
| 32       | 产水量                       | waterweightproduction         | NUMBER(8,2)    |          |          |
| 33       | 含水率                       | watercut                      | NUMBER(8,2)    |          |          |
| 34       | 产液级别                     | liquidweightproductionlevel   | VARCHAR2(50)   |          |          |
| 35       | 生产汽油比                   | productiongasoilratio         | NUMBER(8,2)    |          |          |
| 36       | 油压                         | tubingpressure                | NUMBER(8,2)    |          |          |
| 37       | 套压                         | casingpressure                | NUMBER(8,2)    |          |          |
| 38       | 井口油温                     | wellheadfluidtemperature      | NUMBER(8,2)    |          |          |
| 39       | 动液面                       | producingfluidlevel           | NUMBER(8,2)    |          |          |
| 40       | 泵挂                         | pumpsettingdepth              | NUMBER(8,2)    |          |          |
| 41       | 沉没度                       | submergence                   | NUMBER(8,2)    |          |          |
| 42       | 泵径                         | pumpborediameter              | NUMBER(8,2)    |          |          |
| 43       | 原油密度                     | crudeoildensity               | NUMBER(16,2)   |          |          |
| 44       | 净毛比                       | netgrossratio                 | NUMBER(8,2)    |          |          |
| 45       | 柱塞有效冲程计算产量         | availableplungerstrokeprod    | NUMBER(8,2)    |          |          |
| 46       | 泵间隙漏失量                 | pumpclearanceleakprod         | NUMBER(8,2)    |          |          |
| 47       | 游动凡尔漏失量               | tvleakweightproduction        | NUMBER(8,2)    |          |          |
| 48       | 固定凡尔漏失量               | svleakweightproduction        | NUMBER(8,2)    |          |          |
| 49       | 气影响                       | gasinfluenceprod              | NUMBER(8,2)    |          |          |
| 50       | 抽油杆数据                   | rodstring                     | VARCHAR2(200)  |          |          |
| 51       | 冲程                         | stroke                        | NUMBER(8,2)    |          |          |
| 52       | 冲次                         | spm                           | NUMBER(8,2)    |          |          |
| 53       | 理论上载荷                   | upperloadline                 | NUMBER(8,2)    |          |          |
| 54       | 真实理论上载荷               | upperloadlineofexact          | NUMBER(8,2)    |          |          |
| 55       | 理论下载荷                   | lowerloadline                 | NUMBER(8,2)    |          |          |
| 56       | 最大载荷                     | fmax                          | NUMBER(8,2)    |          |          |
| 57       | 最小载荷                     | fmin                          | NUMBER(8,2)    |          |          |
| 58       | 功图充满系数                 | fullnesscoefficient           | NUMBER(8,2)    |          |          |
| 59       | 电机输入有功功率             | motorinputactivepower         | NUMBER(8,2)    |          |          |
| 60       | 光杆功率                     | polishrodpower                | NUMBER(8,2)    |          |          |
| 61       | 水功率                       | waterpower                    | NUMBER(8,2)    |          |          |
| 62       | 系统效率                     | systemefficiency              | NUMBER(12,3)   |          |          |
| 63       | 系统效率级别                 | systemefficiencylevel         | VARCHAR2(50)   |          |          |
| 64       | 地面效率                     | surfacesystemefficiency       | NUMBER(12,3)   |          |          |
| 65       | 地面效率级别                 | surfacesystemefficiencylevel  | VARCHAR2(50)   |          |          |
| 66       | 井下效率                     | welldownsystemefficiency      | NUMBER(12,3)   |          |          |
| 67       | 井下效率级别                 | welldownsystemefficiencylevel | VARCHAR2(50)   |          |          |
| 68       | 功图面积                     | fsdiagramarea                 | NUMBER(8,2)    |          |          |
| 69       | 吨液百米耗电量               | powerconsumptionperthm        | NUMBER(8,2)    |          |          |
| 70       | 电流平衡度                   | idegreebalance                | NUMBER(8,2)    |          |          |
| 71       | 电流平衡状态                 | idegreebalancename            | VARCHAR2(200)  |          |          |
| 72       | 上冲程最大电流               | upstrokeimax                  | NUMBER(8,2)    |          |          |
| 73       | 下冲程最大电流               | downstrokeimax                | NUMBER(8,2)    |          |          |
| 74       | 电流比                       | iratio                        | VARCHAR2       |          |          |
| 75       | 电流平衡报警级别             | idegreebalancealarmlevel      | NUMBER(4)      |          |          |
| 76       | 功率平衡度                   | wattdegreebalance             | NUMBER(8,2)    |          |          |
| 77       | 功率平衡状态                 | wattdegreebalancename         | VARCHAR2(200)  |          |          |
| 78       | 上冲程最大功率               | upstrokewattmax               | NUMBER(8,2)    |          |          |
| 79       | 下冲程最大功率               | downstrokewattmax             | NUMBER(8,2)    |          |          |
| 80       | 功率比                       | wattratio                     | VARCHAR2       |          |          |
| 81       | 功率平衡报警级别             | wattdegreebalancealarmlevel   | NUMBER(4)      |          |          |
| 82       | 冲程损失系数                 | pumpeff1                      | NUMBER(8,2)    |          |          |
| 83       | 充满系数                     | pumpeff2                      | NUMBER(8,2)    |          |          |
| 84       | 间隙漏失系数                 | pumpeff3                      | NUMBER(8,2)    |          |          |
| 85       | 液体收缩系数                 | pumpeff4                      | NUMBER(8,2)    |          |          |
| 86       | 总泵效                       | pumpeff                       | NUMBER(8,2)    |          |          |
| 87       | 抽油杆伸长量                 | rodflexlength                 | NUMBER(8,2)    |          |          |
| 88       | 油管伸缩值                   | tubingflexlength              | NUMBER(8,2)    |          |          |
| 89       | 惯性载荷增量                 | inertialength                 | NUMBER(8,2)    |          |          |
| 90       | 泵入口压力                   | pumpintakep                   | NUMBER(8,2)    |          |          |
| 91       | 泵入口温度                   | pumpintaket                   | NUMBER(8,2)    |          |          |
| 92       | 泵入口就地气液比             | pumpintakegol                 | NUMBER(8,2)    |          |          |
| 93       | 泵入口粘度                   | pumpinletvisl                 | NUMBER(8,2)    |          |          |
| 94       | 泵入口原油体积系数           | pumpinletbo                   | NUMBER(8,2)    |          |          |
| 95       | 泵出口压力                   | pumpoutletp                   | NUMBER(8,2)    |          |          |
| 96       | 泵出口温度                   | pumpoutlett                   | NUMBER(8,2)    |          |          |
| 97       | 泵出口就地气液比             | pumpoutletgol                 | NUMBER(8,2)    |          |          |
| 98       | 泵出口粘度                   | pumpoutletvisl                | NUMBER(8,2)    |          |          |
| 99       | 泵出口原油体积系数           | pumpoutletbo                  | NUMBER(8,2)    |          |          |
| 100      | 日有功功耗                   | todaywattenergy               | NUMBER(8,2)    |          |          |
| 101      | 日耗电量等级                 | todaywattenergylevel          | VARCHAR2(50)   |          |          |
| 102      | 日正向有功功耗               | todaypwattenergy              | NUMBER(8,2)    |          |          |
| 103      | 日反向有功功耗               | todaynwattenergy              | NUMBER(8,2)    |          |          |
| 104      | 日无功功耗                   | todayvarenergy                | NUMBER(8,2)    |          |          |
| 105      | 日正向无功功耗               | todaypvarenergy               | NUMBER(8,2)    |          |          |
| 106      | 日反向无功功耗               | todaynvarenergy               | NUMBER(8,2)    |          |          |
| 107      | 日视在功耗                   | todayvaenergy                 | NUMBER(8,2)    |          |          |
| 108      | A相电流                      | ia                            | NUMBER(8,2)    |          |          |
| 109      | B相电流                      | ib                            | NUMBER(8,2)    |          |          |
| 110      | C相电流                      | ic                            | NUMBER(8,2)    |          |          |
| 111      | 三项平均电流                 | iavg                          | NUMBER(8,2)    |          |          |
| 112      | 电流字符串                   | istr                          | VARCHAR2       |          |          |
| 113      | A相电流上限                  | iauplimit                     | NUMBER(8,2)    |          |          |
| 114      | A相电流下限                  | iadownlimit                   | NUMBER(8,2)    |          |          |
| 115      | A相电流零值                  | iazero                        | NUMBER(8,2)    |          |          |
| 116      | B相电流上限                  | ibuplimit                     | NUMBER(8,2)    |          |          |
| 117      | B相电流下限                  | ibdownlimit                   | NUMBER(8,2)    |          |          |
| 118      | B相电流零值                  | ibzero                        | NUMBER(8,2)    |          |          |
| 119      | C相电流上限                  | icuplimit                     | NUMBER(8,2)    |          |          |
| 120      | C相电流下限                  | icdownlimit                   | NUMBER(8,2)    |          |          |
| 121      | C相电流零值                  | iczero                        | NUMBER(8,2)    |          |          |
| 122      | A相电压                      | va                            | NUMBER(8,2)    |          |          |
| 123      | B相电压                      | vb                            | NUMBER(8,2)    |          |          |
| 124      | C相电压                      | vc                            | NUMBER(8,2)    |          |          |
| 125      | 三项平均电压                 | vavg                          | NUMBER(8,2)    |          |          |
| 126      | 电压字符串                   | vstr                          | VARCHAR2       |          |          |
| 127      | A相电压上限                  | vauplimit                     | NUMBER(8,2)    |          |          |
| 128      | A相电压下限                  | vadownlimit                   | NUMBER(8,2)    |          |          |
| 129      | A相电压零值                  | vazero                        | NUMBER(8,2)    |          |          |
| 130      | B相电压上限                  | vbuplimit                     | NUMBER(8,2)    |          |          |
| 131      | B相电压下限                  | vbdownlimit                   | NUMBER(8,2)    |          |          |
| 132      | B相电压零值                  | vbzero                        | NUMBER(8,2)    |          |          |
| 133      | C相电压上限                  | vcuplimit                     | NUMBER(8,2)    |          |          |
| 134      | C相电压下限                  | vcdownlimit                   | NUMBER(8,2)    |          |          |
| 135      | C相电压零值                  | vczero                        | NUMBER(8,2)    |          |          |
| 136      | 累计有功功耗                 | totalwattenergy               | NUMBER(8,2)    |          |          |
| 137      | 累计正向有功功耗             | totalpwattenergy              | NUMBER(8,2)    |          |          |
| 138      | 累计反向有功功耗             | totalnwattenergy              | NUMBER(8,2)    |          |          |
| 139      | 累计无功功耗                 | totalvarenergy                | NUMBER(8,2)    |          |          |
| 140      | 累计正向无功功耗             | totalpvarenergy               | NUMBER(8,2)    |          |          |
| 141      | 累计反向无功功耗             | totalnvarenergy               | NUMBER(8,2)    |          |          |
| 142      | 累计视在功耗                 | totalvaenergy                 | NUMBER(8,2)    |          |          |
| 143      | A相有功功率                  | watta                         | NUMBER(8,2)    |          |          |
| 144      | B相有功功率                  | wattb                         | NUMBER(8,2)    |          |          |
| 145      | C相有功功率                  | wattc                         | NUMBER(8,2)    |          |          |
| 146      | 三相总有功功率               | wattsum                       | NUMBER(8,2)    |          |          |
| 147      | 有功功率字符串               | wattstr                       | VARCHAR2       |          |          |
| 148      | A相无功功率                  | vara                          | NUMBER(8,2)    |          |          |
| 149      | B相无功功率                  | varb                          | NUMBER(8,2)    |          |          |
| 150      | C相无功功率                  | varc                          | NUMBER(8,2)    |          |          |
| 151      | 三相总无功功率               | varsum                        | NUMBER(8,2)    |          |          |
| 152      | 无功功率字符串               | varstr                        | VARCHAR2       |          |          |
| 153      | 反向功率                     | reversepower                  | NUMBER(8,2)    |          |          |
| 154      | A相功率因数                  | pfa                           | NUMBER(8,2)    |          |          |
| 155      | B相功率因数                  | pfb                           | NUMBER(8,2)    |          |          |
| 156      | C相功率因数                  | pfc                           | NUMBER(8,2)    |          |          |
| 157      | 三项综合功率因数             | pfsum                         | NUMBER(8,2)    |          |          |
| 158      | 功率因数字符串               | pfstr                         | VARCHAR2       |          |          |
| 159      | 设置频率                     | frequencysetvalue             | NUMBER(8,2)    |          |          |
| 160      | 运行频率                     | frequencyrunvalue             | NUMBER(8,2)    |          |          |
| 161      | 信号强度                     | signal                        | NUMBER(8,2)    |          |          |
| 162      | 传输间隔                     | interval                      | NUMBER(10)     |          |          |
| 163      | 设备版本                     | devicever                     | VARCHAR2(50)   |          |          |
| 164      | 平衡远程调节远程触发控制     | balancecontrolmode            | NUMBER(10)     |          |          |
| 165      | 平衡计算方式                 | balancecalculatemode          | NUMBER(10)     |          |          |
| 166      | 重心远离支点调节时间         | balanceawaytime               | NUMBER(10)     |          |          |
| 167      | 重心接近支点调节时间         | balanceclosetime              | NUMBER(10)     |          |          |
| 168      | 重心远离支点每拍调节时间     | balanceawaytimeperbeat        | NUMBER(10)     |          |          |
| 169      | 重心接近支点每拍调节时间     | balanceclosetimeperbeat       | NUMBER(10)     |          |          |
| 170      | 参与平衡度计算的冲程测量次数 | balancestrokecount            | NUMBER(10)     |          |          |
| 171      | 平衡调节上限                 | balanceoperationuplimit       | NUMBER(10)     |          |          |
| 172      | 平衡调节下限                 | balanceoperationdownlimit     | NUMBER(10)     |          |          |
| 173      | 平衡远程自动调节             | balanceautocontrol            | NUMBER(1)      |          |          |
| 174      | 冲次远程自动调节             | spmautocontrol                | NUMBER(1)      |          |          |
| 175      | 平衡前限位                   | balancefrontlimit             | NUMBER(1)      |          |          |
| 176      | 平衡后限位                   | balanceafterlimit             | NUMBER(1)      |          |          |
| 177      | 视频路径                     | videourl                      | VARCHAR2(400)  |          |          |
| 178      | 组织编号                     | org_id                        | NUMBER(10)     |          |          |
| 179      | 组织代码                     | org_code                      | VARCHAR2(20)   |          |          |
| 180      | 井排序编号                   | sortnum                       | NUMBER(10)     |          |          |

### 2.2.10 viw_rpc_comprehensive_hist 抽油机综合数据历史视图

同 viw_rpc_comprehensive_latest

### 2.2.11 viw_rpc_diagramquery_latest 抽油机图形查询实时视图

| **序号** | **字段名**         | **字段代码**                | **字段类型**  | **单位** | **备注** |
|----------|--------------------|-----------------------------|---------------|----------|----------|
| 1        | 编号               | id                          | NUMBER(10)    |          |          |
| 2        | 井名               | wellname                    | VARCHAR2(200) |          |          |
| 3        | 采集时间           | acquisitiontime             | DATE          |          |          |
| 4        | 冲程               | stroke                      | NUMBER(8,2)   |          |          |
| 5        | 冲次               | spm                         | NUMBER(8,2)   |          |          |
| 6        | 最大载荷           | fmax                        | NUMBER(8,2)   |          |          |
| 7        | 最小载荷           | fmin                        | NUMBER(8,2)   |          |          |
| 8        | 位移曲线           | position_curve              | CLOB          |          |          |
| 9        | 载荷曲线           | load_curve                  | CLOB          |          |          |
| 10       | 功率曲线           | power_curve                 | CLOB          |          |          |
| 11       | 电流曲线           | current_curve               | CLOB          |          |          |
| 12       | 电机转速曲线       | rpm_curve                   | CLOB          |          |          |
| 13       | 过滤前功率曲线     | rawpower_curve              | CLOB          |          |          |
| 14       | 过滤前电流曲线     | rawcurrent_curve            | CLOB          |          |          |
| 15       | 过滤前电机转速曲线 | rawrpm_curve                | CLOB          |          |          |
| 16       | 上冲程最大电流     | upstrokeimax                | VARCHAR2(200) |          |          |
| 17       | 下冲程最大电流     | downstrokeimax              | NUMBER(8,2)   |          |          |
| 18       | 电流平衡度         | idegreebalance              | NUMBER(8,2)   |          |          |
| 19       | 电流平衡级别       | idegreebalancelevel         | NUMBER(8,2)   |          |          |
| 20       | 电流平衡报警级别   | idegreebalancealarmlevel    | VARCHAR2(200) |          |          |
| 21       | 上冲程最大功率     | upstrokewattmax             | NUMBER(8,2)   |          |          |
| 22       | 下冲程最大功率     | downstrokewattmax           | NUMBER(8,2)   |          |          |
| 23       | 功率平衡度         | wattdegreebalance           | NUMBER(8,2)   |          |          |
| 24       | 功率平衡级别       | wattdegreebalancelevel      | NUMBER(8,2)   |          |          |
| 25       | 功率平衡报警级别   | wattdegreebalancealarmlevel | VARCHAR2(200) |          |          |
| 26       | 数据来源           | datasource                  | NUMBER(1)     |          |          |
| 27       | 工况名称           | workingconditionname        | VARCHAR2      |          |          |
| 28       | 理论上载荷线       | upperloadline               | NUMBER(8,2)   |          |          |
| 29       | 理论下载荷线       | lowerloadline               | NUMBER(8,2)   |          |          |
| 30       | 产液量             | liquidweightproduction      | NUMBER(8,2)   |          |          |
| 31       | 信号强度           | signal                      | NUMBER(8,2)   |          |          |
| 32       | 设备版本           | devicever                   | VARCHAR2(50)  |          |          |
| 33       | 传输间隔           | interval                    | NUMBER(10)    |          |          |
| 34       | 组织编号           | orgid                       | NUMBER(10)    |          |          |
| 35       | 排序编号           | sortnum                     | NUMBER(10)    |          |          |

### 2.2.12 viw_rpc_diagramquery_hist 抽油机图形查询历史视图

同 viw_rpc_diagramquery_latest

### 2.2.13 viw_rpc_total_day 抽油机日累计数据视图

| **序号** | **字段名**         | **字段代码**                  | **字段类型**   | **单位** | **备注** |
|----------|--------------------|-------------------------------|----------------|----------|----------|
| 1        | 编号               | id                            | NUMBER(10)     |          |          |
| 2        | 井名               | wellname                      | VARCHAR2(200)  |          |          |
| 3        | 举升类型           | liftingtype                   | NUMBER(10)     |          |          |
| 4        | 举升类型名称       | liftingtypename               | VARCHAR2(200)  |          |          |
| 5        | 井编号             | wellid                        | NUMBER(10)     |          |          |
| 6        | 日期               | calculatedate                 | DATE           |          |          |
| 7        | 通信状态           | commstatus                    |                |          |          |
| 8        | 通信名称           | commstatusname                |                |          |          |
| 9        | 通信报警级别       | commalarmlevel                |                |          |          |
| 10       | 运行状态           | runstatus                     | NUMBER(2)      |          |          |
| 11       | 运行状态名称       | runstatusname                 |                |          |          |
| 12       | 运行状态报警级别   | runalarmlevel                 |                |          |          |
| 13       | 通信时间           | commtime                      | NUMBER(8,2)    |          |          |
| 14       | 通信区间           | commrange                     | VARCHAR2(4000) |          |          |
| 15       | 通信时率           | commtimeefficiency            | NUMBER(12,3)   |          |          |
| 16       | 通信时率级别       | commtimeefficiencylevel       | VARCHAR2(50)   |          |          |
| 17       | 运行时间           | runtime                       | NUMBER(8,2)    |          |          |
| 18       | 运行区间           | runrange                      | VARCHAR2(4000) |          |          |
| 19       | 运行时率           | runtimeefficiency             | NUMBER(12,3)   |          |          |
| 20       | 运行时率级别       | runtimeefficiencylevel        | VARCHAR2(50)   |          |          |
| 21       | 工况代码           | workingconditioncode          | NUMBER(4)      |          |          |
| 22       | 工况名称           | workingconditionname          | VARCHAR2(200)  |          |          |
| 23       | 工况累计字符串     | workingconditionstring        | VARCHAR2(4000) |          |          |
| 24       | 优化建议           | optimizationsuggestion        | VARCHAR2(200)  |          |          |
| 25       | 工况报警级别       | workingconditionalarmlevel    | NUMBER(3)      |          |          |
| 26       | 电参工况代码       | workingconditioncode_e        | NUMBER(4)      |          |          |
| 27       | 电参工况名称       | workingconditionname_e        | VARCHAR2(200)  |          |          |
| 28       | 累计电参工况字符串 | workingconditionstring_e      | VARCHAR2(4000) |          |          |
| 29       | 电参工况报警级别   | workingconditionalarmlevel_e  | NUMBER(3)      |          |          |
| 30       | 产液量             | liquidweightproduction        | NUMBER(8,2)    |          |          |
| 31       | 产液量统计级别     | liquidweightproductionlevel   | VARCHAR2(50)   |          |          |
| 32       | 产油量             | oilweightproduction           | NUMBER(8,2)    |          |          |
| 33       | 产水量             | waterweightproduction         | NUMBER(8,2)    |          |          |
| 34       | 含水率             | watercut                      | NUMBER(10,4)   |          |          |
| 35       | 生产汽油比         | productiongasoilratio         | NUMBER(8,2)    |          |          |
| 36       | 油压               | tubingpressure                | NUMBER(8,2)    |          |          |
| 37       | 套压               | casingpressure                | NUMBER(8,2)    |          |          |
| 38       | 井口油温           | wellheadfluidtemperature      | NUMBER(8,2)    |          |          |
| 39       | 冲程               | stroke                        | NUMBER(8,2)    |          |          |
| 40       | 冲程最大值         | strokemax                     | NUMBER(8,2)    |          |          |
| 41       | 冲程最小值         | strokemin                     | NUMBER(8,2)    |          |          |
| 42       | 冲程字符串         | strokestr                     | VARCHAR2       |          |          |
| 43       | 冲次               | spm                           | NUMBER(8,2)    |          |          |
| 44       | 冲次最大值         | spmmax                        | NUMBER(8,2)    |          |          |
| 45       | 冲次最小值         | spmmin                        | NUMBER(8,2)    |          |          |
| 46       | 冲次字符串         | spmstr                        | VARCHAR2       |          |          |
| 47       | 载荷               | f                             | NUMBER(8,2)    |          |          |
| 48       | 载荷最大值         | fmax                          | NUMBER(8,2)    |          |          |
| 49       | 载荷最小值         | fmin                          | NUMBER(8,2)    |          |          |
| 50       | 载荷字符串         | fstr                          | VARCHAR2       |          |          |
| 51       | 充满系数           | fullnesscoefficient           | NUMBER(10,4)   |          |          |
| 52       | 总泵效             | pumpeff                       | NUMBER(10,4)   |          |          |
| 53       | 泵径               | pumpborediameter              | NUMBER(8,2)    |          |          |
| 54       | 泵挂               | pumpsettingdepth              | NUMBER(8,2)    |          |          |
| 55       | 动液面             | producingfluidlevel           | NUMBER(8,2)    |          |          |
| 56       | 沉没度             | submergence                   | NUMBER(8,2)    |          |          |
| 57       | 转速               | rpm                           | NUMBER(8,2)    |          |          |
| 58       | 转速最大值         | rpmmax                        | NUMBER(8,2)    |          |          |
| 59       | 转速最小值         | rpmmin                        | NUMBER(8,2)    |          |          |
| 60       | 系统效率           | systemefficiency              | NUMBER(10,4)   |          |          |
| 61       | 系统效率统计等级   | systemefficiencylevel         | VARCHAR2(50)   |          |          |
| 62       | 地面效率           | surfacesystemefficiency       | NUMBER(10,4)   |          |          |
| 63       | 地面效率级别       | surfacesystemefficiencylevel  | VARCHAR2(50)   |          |          |
| 64       | 井下效率           | welldownsystemefficiency      | NUMBER(10,4)   |          |          |
| 65       | 井下效率级别       | welldownsystemefficiencylevel | VARCHAR2(50)   |          |          |
| 66       | 吨液百米耗电量     | powerconsumptionperthm        | NUMBER(8,2)    |          |          |
| 67       | 日有功功耗         | todaywattenergy               | NUMBER(8,2)    |          |          |
| 68       | 日耗电量统计级别   | todaywattenergylevel          | VARCHAR2(50)   |          |          |
| 69       | 日正向有功功耗     | todaypwattenergy              | NUMBER(8,2)    |          |          |
| 70       | 日反向有功功耗     | todaynwattenergy              | NUMBER(8,2)    |          |          |
| 71       | 日无功功耗         | todayvarenergy                | NUMBER(8,2)    |          |          |
| 72       | 日正向无功功耗     | todaypvarenergy               | NUMBER(8,2)    |          |          |
| 73       | 日反向无功功耗     | todaynvarenergy               | NUMBER(8,2)    |          |          |
| 74       | 日视在功耗         | todayvaenergy                 | NUMBER(8,2)    |          |          |
| 75       | 电流平衡度         | idegreebalance                | NUMBER(8,2)    |          |          |
| 76       | 电流平衡度最大值   | idegreebalancemax             | NUMBER(8,2)    |          |          |
| 77       | 电流平衡度最小值   | idegreebalancemin             | NUMBER(8,2)    |          |          |
| 78       | 电流平衡度字符串   | idegreebalancestr             | VARCHAR2       |          |          |
| 79       | 电流平衡统计级别   | idegreebalancelevel           | VARCHAR2(200)  |          |          |
| 80       | 电流平衡报警级别   | idegreebalancealarmlevel      | NUMBER(3)      |          |          |
| 81       | 功率平衡度         | wattdegreebalance             | NUMBER(8,2)    |          |          |
| 82       | 功率平衡度最大值   | wattdegreebalancemax          | NUMBER(8,2)    |          |          |
| 83       | 功率平衡度最小值   | wattdegreebalancemin          | NUMBER(8,2)    |          |          |
| 84       | 功率平衡度字符串   | wattdegreebalancestr          | VARCHAR2       |          |          |
| 85       | 功率平衡统计级别   | wattdegreebalancelevel        | VARCHAR2(200)  |          |          |
| 86       | 功率平衡报警级别   | wattdegreebalancealarmlevel   | NUMBER(3)      |          |          |
| 87       | 移动距离           | deltaradius                   | NUMBER(8,2)    |          |          |
| 88       | A相电流            | ia                            | NUMBER(8,2)    |          |          |
| 89       | A相电流最大值      | iamax                         | NUMBER(8,2)    |          |          |
| 90       | A相电流最小值      | iamin                         | NUMBER(8,2)    |          |          |
| 91       | A相电流字符串      | iastr                         | NUMBER(8,2)    |          |          |
| 92       | B相电流            | ib                            | NUMBER(8,2)    |          |          |
| 93       | B相电流最大值      | ibmax                         | NUMBER(8,2)    |          |          |
| 94       | B相电流最小值      | ibmin                         | NUMBER(8,2)    |          |          |
| 95       | B相电流字符串      | ibstr                         | VARCHAR2       |          |          |
| 96       | C相电流            | ic                            | NUMBER(8,2)    |          |          |
| 97       | C相电流最大值      | icmax                         | NUMBER(8,2)    |          |          |
| 98       | C相电流最小值      | icmin                         | NUMBER(8,2)    |          |          |
| 99       | C相电流字符串      | icstr                         | VARCHAR2       |          |          |
| 100      | A相电压            | va                            | NUMBER(8,2)    |          |          |
| 101      | A相电压最大值      | vamax                         | NUMBER(8,2)    |          |          |
| 102      | A相电压最小值      | vamin                         | NUMBER(8,2)    |          |          |
| 103      | A相电压字符串      | vastr                         | VARCHAR2       |          |          |
| 104      | B相电压            | vb                            | NUMBER(8,2)    |          |          |
| 105      | B相电压最大值      | vbmax                         | NUMBER(8,2)    |          |          |
| 106      | B相电压最小值      | vbmin                         | NUMBER(8,2)    |          |          |
| 107      | B相电压字符串      | vbstr                         | VARCHAR2       |          |          |
| 108      | C相电压            | vc                            | NUMBER(8,2)    |          |          |
| 109      | C相电压最大值      | vcmax                         | NUMBER(8,2)    |          |          |
| 110      | C相电压最小值      | vcmin                         | NUMBER(8,2)    |          |          |
| 111      | C相电压字符串      | vcstr                         | VARCHAR2       |          |          |
| 112      | 信号强度           | signal                        | NUMBER(8,2)    |          |          |
| 113      | 信号强度最大值     | signalmax                     | NUMBER(8,2)    |          |          |
| 114      | 信号强度最小值     | signalmin                     | NUMBER(8,2)    |          |          |
| 115      | 信号强度字符串     | signalstr                     | VARCHAR2       |          |          |
| 116      | 视频路径           | videourl                      | VARCHAR2(400)  |          |          |
| 117      | 井排序编号         | sortnum                       | NUMBER(10)     |          |          |
| 118      | 组织代码           | org_code                      | VARCHAR2(20)   |          |          |
| 119      | 组织编号           | org_id                        | NUMBER(10)     |          |          |
| 120      | 备注               | remark                        | VARCHAR2       |          |          |

### 2.1.14 viw_rpc_calculatemain 抽油机计算结果管理视图

| **序号** | **字段名**     | **字段代码**               | **字段类型**  | **单位** | **备注** |
|----------|----------------|----------------------------|---------------|----------|----------|
| 1        | 编号           | id                         | NUMBER(10)    |          |          |
| 2        | 井名           | wellname                   | VARCHAR2(200) |          |          |
| 3        | 举升方式       | liftingtype                | NUMBER(10)    |          |          |
| 4        | 采集时间       | acquisitiontime            | DATE          |          |          |
| 5        | 工况名称       | workingconditionname       | VARCHAR2(200) |          |          |
| 6        | 产液量         | liquidproduction           | NUMBER(8,2)   |          |          |
| 7        | 产油量         | oilproduction              | NUMBER(8,2)   |          |          |
| 8        | 原油密度       | crudeoildensity            | NUMBER(16,2)  |          |          |
| 9        | 水密度         | waterdensity               | NUMBER(16,2)  |          |          |
| 10       | 天然气相对密度 | naturalgasrelativedensity  | NUMBER(16,2)  |          |          |
| 11       | 饱和压力       | saturationpressure         | NUMBER(16,2)  |          |          |
| 12       | 油藏深度       | reservoirdepth             | NUMBER(16,2)  |          |          |
| 13       | 油藏温度       | reservoirtemperature       | NUMBER(16,2)  |          |          |
| 14       | 油压           | tubingpressure             | NUMBER(8,2)   |          |          |
| 15       | 套压           | casingpressure             | NUMBER(8,2)   |          |          |
| 16       | 井口温油       | wellheadfluidtemperature   | NUMBER(8,2)   |          |          |
| 17       | 含水率         | watercut                   | NUMBER(8,2)   |          |          |
| 18       | 生产气油比     | productiongasoilratio      | NUMBER(8,2)   |          |          |
| 19       | 动液面         | producingfluidlevel        | NUMBER(8,2)   |          |          |
| 20       | 泵挂           | pumpsettingdepth           | NUMBER(8,2)   |          |          |
| 21       | 泵级别         | pumpgrade                  | NUMBER(1)     |          |          |
| 22       | 泵径           | pumpborediameter           | NUMBER(8,2)   |          |          |
| 23       | 柱塞长         | plungerlength              | NUMBER(8,2)   |          |          |
| 24       | 油管内径       | tubingstringinsidediameter | NUMBER(8,2)   |          |          |
| 25       | 套管内径       | casingstringinsidediameter | NUMBER(8,2)   |          |          |
| 26       | 杆数据         | rodstring                  | VARCHAR2(200) |          |          |
| 27       | 锚定状态       | anchoringstatename         | VARCHAR2(200) |          |          |
| 28       | 净毛比         | netgrossratio              | NUMBER(8,2)   |          |          |
| 29       | 计算结果       | resultstatus               | NUMBER(2)     |          |          |
| 30       | 组织编号       | orgid                      | NUMBER(10)    |          |          |

# 三、存储过程

| **序号** | **名称**                      | **描述**                 | **备注**               |
|----------|-------------------------------|--------------------------|------------------------|
| 1        | prd_clear_data                | 清理数据并重置序列       |                        |
| 2        | prd_reset_sequence            | 重置序列                 |                        |
| 3        | prd_save_wellinformation      | 保存井信息数据           |                        |
| 4        | prd_change_wellname           | 修改井名                 |                        |
| 5        | prd_save_rpc_productiondata   | 保存生产数据             |                        |
| 6        | prd_save_rpc_diagram          | 保存功图采集和计算数据   |                        |
| 7        | prd_save_rpc_uploaddiagram    | 保存上传的功图数据       |                        |
| 8        | prd_save_rpc_diagramresult    | 保存功图计算结果         |                        |
| 9        | pro_save_rpc_recalculateparam | 保存功图重新计算参数     |                        |
| 10       | prd_save_rpc_reinverdiagram   | 保存重新反演曲线数据     |                        |
| 11       | prd_init_rpc_daily            | 初始化日汇总数据         | 每天凌晨一点钟定时执行 |
| 12       | prd_save_rpc_diagramdaily     | 保存功图日汇总数据       |                        |
| 13       | prd_save_rpc_discretedaily    | 保存离散数据日汇总结果   |                        |
| 14       | prd_save_rpc_inver_daily      | 保存反演上传的日汇总数据 |                        |
| 15       | prd_save_rpc_motor            | 保存反演电机数据         |                        |
| 16       | prd_save_rpcinformation       | 保存反演抽油机数据       |                        |
| 17       | prd_save_rpc_inver_opt        | 保存反演优化参数         |                        |
| 18       | prd_save_alarmcolor           | 保存报警级别颜色         |                        |

# 四、触发器

| **序号** | **名称**                      | **描述**                                 |
|----------|-------------------------------|------------------------------------------|
| 1        | trg_b_org_i_u                 | 组织表插入、修改数据前触发               |
| 2        | trg_b_user_i                  | 用户表插入数据前触发                     |
| 3        | trg_b_role_i                  | 角色表插入数据前触发                     |
| 4        | trg_b_module_i                | 模块表插入数据前触发                     |
| 5        | trg_b_code_i                  | 代码表插入数据前触发                     |
| 6        | trg_b_acq_group_conf_i        | 采控组表插入数据前触发                   |
| 7        | trg_b_acq_item_conf_i         | 采控项表插入数据前触发                   |
| 8        | trg_b_acq_item2group_conf_i   | 采控组项关系表插入数据前触发             |
| 9        | trg_b_wellinformation_i       | 井信息表插入数据前触发                   |
| 10       | trg_a_wellinformation_i       | 井信息表插入数据后触发                   |
| 11       | trg_a_wellinformation_u       | 井信息表更新数据后触发                   |
| 12       | trg_b_rpc_proddata_latest_i   | 抽油机生产数据实时表插入数据前触发       |
| 13       | trg_a_rpc_proddata_latest_i_u | 抽油机生产数据实时表插入、更新数据后触发 |
| 14       | trg_b_rpc_proddata_hist_i     | 抽油机生产数据历史表插入数据前触发       |
| 15       | trg_b_rpc_discrete_latest_i   | 抽油机离散数据实时表插入数据前触发       |
| 16       | trg_a_rpc_discrete_latest_i_u | 抽油机离散数据实时表插入、更新数据后触发 |
| 17       | trg_b_rpc_discrete_hist_i     | 抽油机离散数据历史表插入数据前触发       |
| 18       | trg_b_rpc_diagram_latest_i    | 抽油机曲线数据实时表插入数据前触发       |
| 19       | trg_b_rpc_diagram_hist_i      | 抽油机曲线数据历史表插入数据前触发       |
| 20       | trg_a_rpc_diagram_hist_i_u    | 抽油机曲线数据历史表插入、更新数据后触发 |
| 21       | trg_b_rpc_worktype_i          | 抽油机工况类型表插入数据前触发           |
| 22       | trg_b_rpc_alarmtype_conf_i    | 抽油机工况报警配置表插入数据前触发       |
| 23       | trg_b_rpc_total_day_i         | 抽油机日累计数据表插入数据前触发         |
| 24       | trg_b_rpc_statistics_conf_i   | 抽油机统计配置表插入数据前触发           |
| 25       | trg_b_rpcinformation_i        | 抽油机设备表插入数据前触发               |
| 26       | trg_b_rpc_motor_i             | 抽油机电机数据表插入数据前触发           |
| 27       | trg_b_rpc_inver_opt_i         | 抽油机电参反演参数优化表插入数据前触发   |

# 五、序列  


# 六、数据库创建

## 6.1 自建用户

需要自建用户及表空间，并给用户授权。

**步骤1、**修改“1创建表空间和用户.sql”中的oracle数据库路径；文件在“创建数据库sql”文件夹中。

（1）找到部署服务器中的oracle数据库实例路径，如：F:\app\Administrator\oradata\orcl

（2）将“1创建表空间和用户.sql”文件中的路径修改为实际路径，修改位置包括：

TEMPFILE
'D:\app\Oracle11g\oradata\orcl\agile_temp.dbf'中的D:\app\Oracle11g\oradata\orcl

DATAFILE
'D:\app\Oracle11g\oradata\orcl\agile_data.dbf'中的D:\app\Oracle11g\oradata\orcl

保存。

**步骤2、**修改autorun.bat中内容，主要是修改密码和全局数据库名。

（1）右键编辑autorun.bat（不要双击打开，会执行该文件）

（2）修改该句内容 sqlplus sys/orcl\@orcl as sysdba
\@1创建表空间和用户.sql\>log.txt

其中：

sys：系统管理员，不用修改

orcl：系统管理员密码，安装Oracle时输入的管理口令，根据实际修改

\@orcl：全局数据库名，若安装时没有修改，默认是orcl

**步骤3、**执行autorun.bat文件，等待执行完成

**步骤4、**执行完成后，查看log.txt（日志文件）是否有报错。

## 6.2 已有用户

部署方提供了用户名、密码，创建表空间，并为用户授权。授权有两种形式：

（1）grant connect,resource,dba to agile; //agile为用户名

（2）grant connect,resource,create view,debug any procedure, debug connect
session to agile

**步骤1、**修改creatAndInitDB.bat中内容，主要是修改用户名、密码和全局数据库名。

sqlplus agile/agile\@orcl \@createAndInitDB.sql\>log.txt

sys：用户名，部署方提供

orcl：密码，部署方提供

orcl：全局数据库名，部署方提供

**步骤2、**修改完成后，执行该文件。

**步骤3、**执行完成后，查看log.txt（日志文件）是否有报错信息。
