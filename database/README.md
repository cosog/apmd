----:link:[**转至用户手册**](.././README.md):link:----  

# 《油气生产敏捷计算分析系统V7.1》 数据库手册  

- [一、表](README.md#一表)
   - [1.1 表概览](README.md#11-表概览)
   - [1.2 逻辑结构](README.md#12-逻辑结构)
   - [1.3 详述](README.md#13-详述)
     - [1.3.1 tbl_org 组织数据表](README.md#131-tbl_org-组织数据表)
     - [1.3.2 tbl_user 用户数据表](README.md#132-tbl_user-用户数据表)
     - [1.3.3 tbl_role 角色数据表](README.md#133-tbl_role-角色数据表)
     - [1.3.4 tbl_module 模块数据表](README.md#134-tbl_module-模块数据表)
     - [1.3.5 tbl_module2role 模块角色关系表](README.md#135-tbl_module2role-模块角色关系表)
     - [1.3.6 tbl_dist_name 字典名称表](README.md#136-tbl_dist_name-字典名称表)
     - [1.3.7 tbl_dist_item 字典数据项表](README.md#137-tbl_dist_item-字典数据项表)
     - [1.3.8 tbl_code 代码表](README.md#138-tbl_code-代码表)
     - [1.3.9 tbl_acq_group_conf 采控组名称表](README.md#139-tbl_acq_group_conf-采控组名称表)
     - [1.3.10 tbl_acq_item_conf 采控项名称表](README.md#1310-tbl_acq_item_conf-采控项名称表)
     - [1.3.11 tbl_acq_item2group_conf 采控组项关系表](README.md#1311-tbl_acq_item2group_conf-采控组项关系表)
     - [1.3.12 tbl_wellinformation 井名基本信息表](README.md#1312-tbl_wellinformation-井名基本信息表)
     - [1.3.13 tbl_trajectory 井身轨迹表](README.md#1313-tbl_trajectory-井身轨迹表)
     - [1.3.14 tbl_rpc_productiondata_latest 抽油机生产数据实时表](README.md#1314-tbl_rpc_productiondata_latest-抽油机生产数据实时表)
     - [1.3.15 tbl_rpc_productiondata_hist 抽油机生产数据历史表](README.md#1315-tbl_rpc_productiondata_hist-抽油机生产数据历史表)
     - [1.3.16 tbl_rpc_discrete_latest 抽油机离散数据实时表](README.md#1316-tbl_rpc_discrete_latest-抽油机离散数据实时表)
     - [1.3.17 tbl_rpc_discrete_hist 抽油机离散数据历史表](README.md#1317-tbl_rpc_discrete_hist-抽油机离散数据历史表)
     - [1.3.18 tbl_rpc_diagram_latest 抽油机曲线数据实时表](README.md#1318-tbl_rpc_diagram_latest-抽油机曲线数据实时表)
     - [1.3.19 tbl_rpc_diagram_hist 抽油机曲线数据历史表](README.md#1319-tbl_rpc_diagram_hist-抽油机曲线数据历史表)
     - [1.3.20 tbl_rpc_worktype 抽油机工况类型表](README.md#1320-tbl_rpc_worktype-抽油机工况类型表)
     - [1.3.21 tbl_rpc_alarmtype_conf 抽油机报警类型表](README.md#1321-tbl_rpc_alarmtype_conf-抽油机报警类型表)
     - [1.3.22 tbl_rpc_total_day 抽油机日累计数据表](README.md#1322-tbl_rpc_total_day-抽油机日累计数据表)
     - [1.3.23 tbl_rpc_statistics_conf 抽油机统计配置表](README.md#1323-tbl_rpc_statistics_conf-抽油机统计配置表)
     - [1.3.24 tbl_rpcinformation 抽油机设备表](README.md#1324-tbl_rpcinformation-抽油机设备表)
     - [1.3.25 tbl_rpc_motor 抽油机电机数据表](README.md#1325-tbl_rpc_motor-抽油机电机数据表)
     - [1.3.26 tbl_rpc_inver_opt 抽油机电参反演参数优化表](README.md#1326-tbl_rpc_inver_opt-抽油机电参反演参数优化表)
- [二、视图](README.md#二视图) 
   - [2.1 视图概览](README.md#21-视图概览)
   - [2.2 详述](README.md#22-详述)
     - [2.2.1 viw_wellinformation 井名信息视图](README.md#221-viw_wellinformation-井名信息视图)
     - [2.2.2 viw_rpc_productiondata_latest 抽油机生产数据实时视图](README.md#222-viw_rpc_productiondata_latest-抽油机生产数据实时视图)  
     - [2.2.3 viw_rpc_productiondata_hist 抽油机生产数据历史视图](README.md#223-viw_rpc_productiondata_hist-抽油机生产数据历史视图)
     - [2.2.4 viw_commstatus 通信状态视图](README.md#224-viw_commstatus-通信状态视图)
     - [2.2.5 viw_rpc_diagram_latest 抽油机曲线数据实时视图](README.md#225-viw_rpc_diagram_latest-抽油机曲线数据实时视图)
     - [2.2.6 viw_rpc_diagram_hist 抽油机曲线数据历史视图](README.md#226-viw_rpc_diagram_hist-抽油机曲线数据历史视图)
     - [2.2.7 viw_rpc_discrete_latest 抽油机电参数据实时视图](README.md#227-viw_rpc_discrete_latest-抽油机电参数据实时视图)
     - [2.2.8 viw_rpc_discrete_hist 抽油机电参数据历史视图](README.md#228-viw_rpc_discrete_hist-抽油机电参数据历史视图)
     - [2.2.9 viw_rpc_comprehensive_latest 抽油机综合数据实时视图](README.md#229-viw_rpc_comprehensive_latest-抽油机综合数据实时视图)
     - [2.2.10 viw_rpc_comprehensive_hist 抽油机综合数据历史视图](README.md#2210-viw_rpc_comprehensive_hist-抽油机综合数据历史视图)
     - [2.2.11 viw_rpc_diagramquery_latest 抽油机图形查询实时视图](README.md#2211-viw_rpc_diagramquery_latest-抽油机图形查询实时视图)
     - [2.2.12 viw_rpc_diagramquery_hist 抽油机图形查询历史视图](README.md#2212-viw_rpc_diagramquery_hist-抽油机图形查询历史视图)
     - [2.2.13 viw_rpc_total_day 抽油机日累计数据视图](README.md#2213-viw_rpc_total_day-抽油机日累计数据视图)
     - [2.1.14 viw_rpc_calculatemain 抽油机计算结果管理视图](README.md#2114-viw_rpc_calculatemain-抽油机计算结果管理视图)
- [三、存储过程](README.md#三存储过程)
- [四、触发器](README.md#四触发器)  
- [五、序列](README.md#五序列)  
- [六、数据库创建](README.md#六数据库创建)
   - [6.1 自建用户](README.md#61-自建用户)
   - [6.2 已有用户](README.md#62-已有用户)

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

![逻辑结构](.././Image/PNG/035.png?raw=true)

## 1.3 详述  

### 1.3.1 tbl_org 组织数据表

| **序号** | **代码**     | **名称**     | **单位** | **类型**       | **为空**     | **键** |
|----------|--------------|--------------|----------|----------------|--------------|--------|
| 1&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;  | org_id       | 单位序号     |          | NUMBER(10)     | N&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; | 主键   |
| 2        | org_code     | 单位编码     |          | VARCHAR2(20)   | Y            |        |
| 3        | org_name     | 单位名称     |          | VARCHAR2(100)  | N            |        |
| 4        | org_memo     | 单位说明     |          | VARCHAR2(4000) | Y            |        |
| 5        | org_parent   | 父级单位编号 |          | NUMBER(10)     | N            |        |
| 6        | org_seq      | 单位排序     |          | NUMBER(10)     | Y            |        |
| 7        | org_flag     | 单位标志     |          | CHAR(1)        | Y            |        |
| 8        | org_realid   | 单位当前编号 |          | NUMBER(10)     | Y            |        |
| 9        | org_level    | 单位级别     |          | NUMBER(1)      | Y            |        |
| 10       | org_type     | 单位类型     |          | NUMBER(1)      | Y            |        |
| 11       | org_coordx   | 纬度         |          | NUMBER(10,6)   | Y            |        |
| 12       | org_coordy   | 经度         |          | NUMBER(10,6)   | Y            |        |
| 13       | show_level   | 地图显示级别 |          | NUMBER(2)      | Y            |        |

### 1.3.2 tbl_user 用户数据表

| **序号** | **代码**        | **名称**     | **单位** | **类型**      | **为空**     | **键** |
|----------|-----------------|--------------|----------|---------------|--------------|--------|
| 1&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;     | user_no         | 用户序号     |          | NUMBER(10)    | N&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; | 主键   |
| 2        | user_id         | 用户账号     |          | VARCHAR2(20)  | N            |        |
| 3        | user_pwd        | 用户密码     |          | VARCHAR2(20)  | Y            |        |
| 4        | user_name       | 用户姓名     |          | VARCHAR2(40)  | N            |        |
| 5        | user_in_email   | 内部邮箱     |          | VARCHAR2(40)  | Y            |        |
| 6        | user_out_email  | 外部邮箱     |          | VARCHAR2(100) | Y            |        |
| 7        | user_phone      | 用户电话     |          | VARCHAR2(40)  | Y            |        |
| 8        | user_mobile     | 手机号       |          | VARCHAR2(40)  | Y            |        |
| 9        | user_address    | 地址         |          | VARCHAR2(200) | Y            |        |
| 10       | user_postcode   | 邮编         |          | CHAR(6)       | Y            |        |
| 11       | user_title      | 用户职称     |          | VARCHAR2(100) | Y            |        |
| 12       | user_type       | 用户类型     |          | NUMBER(10)    | Y            | 外键   |
| 13       | user_orgid      | 用户所属组织 |          | NUMBER(10)    | N            | 外键   |
| 14       | user_isleader   | 是否领导     |          | CHAR(1)       | Y            |        |
| 15       | user_regtime    | 用户注册时间 |          | DATE          | Y            |        |
| 16       | user_style      | 显示风格     |          | VARCHAR2(20)  | Y            |        |
| 17       | user_quicklogin | 是否快捷登录 |          | NUMBER(1)     | Y            |        |

### 1.3.3 tbl_role 角色数据表

| **序号** | **代码**     | **名称**   | **单位** | **类型**       | **为空**     | **键** |
|----------|--------------|------------|----------|----------------|--------------|--------|
| 1&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;        | role_id      | 角色序号   |          | NUMBER(10)     | N&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;            | 主键   |
| 2        | role_code    | 角色编码   |          | VARCHAR2(50)   | N            |        |
| 3        | role_name    | 角色名称   |          | VARCHAR2(40)   | N            |        |
| 4        | role_flag    | 控制权限   |          | NUMBER(10)     | Y            |        |
| 5        | remark       | 角色描述   |          | VARCHAR2(2000) | Y            |        |

### 1.3.4 tbl_module 模块数据表

| **序号** | **代码**     | **名称**     | **单位** | **类型**      | **为空**     | **键** |
|----------|--------------|--------------|----------|---------------|--------------|--------|
| 1&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;        | md_id        | 模块序号     |          | NUMBER(10)    | N&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;            | 主键   |
| 2        | md_parentid  | 父级模块序号 |          | NUMBER(10)    | N            |        |
| 3        | md_name      | 模块名称     |          | VARCHAR2(100) | N            |        |
| 4        | md_showname  | 模块简介     |          | VARCHAR2(100) | Y            |        |
| 5        | md_url       | 模块URL      |          | VARCHAR2(200) | Y            |        |
| 6        | md_code      | 模块编码     |          | VARCHAR2(200) | Y            |        |
| 7        | md_seq       | 模块排序     |          | NUMBER(20)    | Y            |        |
| 8        | md_level     | 模块级别     |          | NUMBER(10)    | Y            |        |
| 9        | md_flag      | 模块标志     |          | NUMBER(10)    | Y            |        |
| 10       | md_icon      | 模块图标     |          | VARCHAR2(100) | Y            |        |
| 11       | md_type      | 模块类型     |          | NUMBER(1)     | Y            |        |
| 12       | md_control   | 模块控制器   |          | VARCHAR2(100) | Y            |        |

### 1.3.5 tbl_module2role 模块角色关系表

| **序号** | **代码**     | **名称**   | **单位** | **类型**     | **为空**     | **键** |
|----------|--------------|------------|----------|--------------|--------------|--------|
| 1&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;        | rm_id        | 序号       |          | NUMBER(10)   | N&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;            | 主键   |
| 2        | rm_roleid    | 角色编号   |          | NUMBER(10)   | N            | 外键   |
| 3        | rm_moduleid  | 模块序号   |          | NUMBER(10)   | N            | 外键   |
| 4        | rm_matrix    | 权限矩阵   |          | VARCHAR2(8)  | N            |        |

### 1.3.6 tbl_dist_name 字典名称表

| **序号** | **代码**     | **名称**   | **单位** | **类型**     | **为空**     | **键** |
|----------|--------------|------------|----------|--------------|--------------|--------|
| 1&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;        | sysdataid    | 字典编码   |          | VARCHAR2(32) | N&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;            | 主键   |
| 2        | tenantid     | 组织编号   |          | VARCHAR2(50) | Y            |        |
| 3        | cname        | 中文名称   |          | VARCHAR2(50) | Y            |        |
| 4        | ename        | 英文名称   |          | VARCHAR2(50) | Y            |        |
| 5        | sorts        | 排序       |          | NUMBER       | Y            |        |
| 6        | status       | 显示状态   |          | NUMBER       | Y            |        |
| 7        | creator      | 创建人     |          | VARCHAR2(50) | Y            |        |
| 8        | updateuser   | 修改人     |          | VARCHAR2(50) | Y            |        |
| 9        | createdate   | 创建时间   |          | DATE         | Y            |        |
| 10       | updatetime   | 修改时间   |          | DATE         | N            |        |

### 1.3.7 tbl_dist_item 字典数据项表

| **序号** | **代码**     | **名称**   | **单位** | **类型**      | **为空**     | **键** |
|----------|--------------|------------|----------|---------------|--------------|--------|
| 1&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;        | dataitemid   | 数据项编码 |          | VARCHAR2(32)  | N&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;            | 主键   |
| 2        | tenantid     | 组织编号   |          | VARCHAR2(50)  | Y            |        |
| 3        | sysdataid    | 字典编码   |          | VARCHAR2(50)  | Y            | 外键   |
| 4        | cname        | 中文名称   |          | VARCHAR2(50)  | Y            |        |
| 5        | ename        | 英文名称   |          | VARCHAR2(200) | Y            |        |
| 6        | datavalue    | 数据项值   |          | VARCHAR2(200) | Y            |        |
| 7        | sorts        | 排序       |          | NUMBER        | Y            |        |
| 8        | status       | 显示状态   |          | NUMBER        | Y            |        |
| 9        | creator      | 创建人     |          | VARCHAR2(50)  | Y            |        |
| 10       | updateuser   | 修改人     |          | VARCHAR2(50)  | Y            |        |
| 11       | createdate   | 创建时间   |          | DATE          | Y            |        |
| 12       | updatetime   | 修改时间   |          | DATE          | Y            |        |

### 1.3.8 tbl_code 代码表

| **序号** | **代码**     | **名称**   | **单位** | **类型**      | **为空**     | **键** |
|----------|--------------|------------|----------|---------------|--------------|--------|
| 1&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;        | id           | 记录编号   |          | NUMBER(10)    | N&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;            | 主键   |
| 2        | tablecode    | 数据表代码 |          | VARCHAR2(200) | Y            |        |
| 3        | itemcode     | 数据项代码 |          | VARCHAR2(200) | Y            |        |
| 4        | itemvalue    | 代码       |          | VARCHAR2(20)  | Y            |        |
| 5        | itemname     | 名称       |          | VARCHAR2(200) | Y            |        |
| 6        | remark       | 备注       |          | VARCHAR2(200) | Y            |        |
| 7        | state        | 状态       |          | NUMBER(10)    | Y            |        |

### 1.3.9 tbl_acq_group_conf 采控组名称表

| **序号** | **代码**     | **名称**   | **单位** | **类型**       | **为空**     | **键** |
|----------|--------------|------------|----------|----------------|--------------|--------|
| 1&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;        | id           | 记录编号   |          | NUMBER(10)     | N&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;            | 主键   |
| 2        | unit_code    | 单元代码   |          | VARCHAR2(50)   | N            |        |
| 3        | unit_name    | 单元名称   |          | VARCHAR2(50)   | Y            |        |
| 4        | remark       | 单元描述   |          | VARCHAR2(2000) | Y            |        |

### 1.3.10 tbl_acq_item_conf 采控项名称表

| **序号** | **代码**      | **名称**   | **单位** | **类型**      | **为空**     | **键** |
|----------|---------------|------------|----------|---------------|--------------|--------|
| 1&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;        | id            | 记录编号   |          | NUMBER(10)    | N&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;            | 主键   |
| 2        | parentid      | 父级编号   |          | NUMBER(10)    | Y            |        |
| 3        | itemname      | 采集项名称 |          | VARCHAR2(100) | Y            |        |
| 4        | itemcode      | 采集项代码 |          | VARCHAR2(100) | Y            |        |
| 5        | address       | 寄存器地址 |          | NUMBER(10)    | Y            |        |
| 6        | length        | 寄存器个数 |          | NUMBER(10)    | Y            |        |
| 7        | datatype      | 数据类型   |          | NUMBER(5)     | Y            |        |
| 8        | zoom          | 量程变换   |          | NUMBER(10,3)  | Y            |        |
| 9        | seq           | 排序编号   |          | NUMBER(10)    | Y            |        |
| 10       | operationtype | 操作类型   |          | NUMBER(2)     | Y            |        |

### 1.3.11 tbl_acq_item2group_conf 采控组项关系表

| **序号** | **代码**     | **名称**     | **单位** | **类型**     | **为空**     | **键** |
|----------|--------------|--------------|----------|--------------|--------------|--------|
| 1&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;        | id           | 记录编号     |          | NUMBER(10)   | N&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;            | 主键   |
| 2        | unitid       | 采集类型编号 |          | NUMBER(10)   | N            | 外键   |
| 3        | itemid       | 采集项编号   |          | NUMBER(10)   | N            | 外键   |
| 4        | matrix       | 阵列         |          | VARCHAR2(8)  | N            |        |

### 1.3.12 tbl_wellinformation 井名基本信息表

| **序号** | **代码**                   | **名称**         | **单位** | **类型**      | **为空**     | **键** |
|----------|----------------------------|------------------|----------|---------------|--------------|--------|
| 1&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; | id               | 记录编号 |          | NUMBER(10)    | N&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;| 主键   |
| 2        | orgid                      | 单位编号         |          | NUMBER(10)    | Y            | 外键   |
| 3        | resname                    | 油气藏名称       |          | VARCHAR2(200) | Y            |        |
| 4        | wellname                   | 井名             |          | VARCHAR2(200) | N            |        |
| 5        | liftingtype                | 举升类型         |          | NUMBER(10)    | Y            |        |
| 6        | driveraddr                 | 设备地址         |          | VARCHAR2(200) | Y            |        |
| 7        | driverid                   | 设备编号         |          | VARCHAR2(200) | Y            |        |
| 8        | acqcycle_diagram           | 曲线采集周期     | min      | NUMBER(10)    | Y            |        |
| 9        | acqcycle_discrete          | 离散读取周期 | min      | NUMBER(10)    | Y            |        |
| 10       | savecycle_discrete         | 离散保存周期 | min      | NUMBER(10)    | Y            |        |
| 11       | drivercode                 | 驱动编码         |          | VARCHAR2(50)  | Y            |        |
| 12       | unitcode                   | 采集单元编码     |          | VARCHAR2(50)  | Y            |        |
| 13       | runtimeefficiencysource    | 时率来源         |          | NUMBER(2)     | Y            |        |
| 14       | videourl                   | 视频url          |          | VARCHAR2(400) | Y            |        |
| 15       | sortnum                    | 排序编号         |          | NUMBER(10)    | Y            |        |
| 16       | acqcyclesetstatus_diagram  | 曲线采集周期设置状态 |          | NUMBER(2)     | Y            |        |
| 17       | acqcyclesetstatus_discrete | 离散采集周期设置状态 |          | NUMBER(2)     | Y            |        |
| 18       | groupid                    | 采控组编号       |          | NUMBER(10)    | Y            | 外键   |

### 1.3.13 tbl_trajectory 井身轨迹表

| **序号** | **代码**         | **名称**   | **单位** | **类型**     | **为空**     | **键** |
|----------|-----------------|------------|----------|--------------|--------------|--------|
| 1        | id              | 记录编号    |          | NUMBER(10)   | N            | 主键    |
| 2        | wellid          | 井编号     |          | NUMBER(10)    | N            | 外键   |
| 3        | measuringdepth  | 测量深度    | m        | CLOB         | Y            |        |
| 4        | verticaldepth   | 垂直深度    | m        | CLOB         | Y            |        |
| 5        | deviationangle  | 井斜角     | 度        | CLOB         | Y            |        |
| 6        | azimuthangle    | 方位角     | 度        | CLOB         | Y            |        |

### 1.3.14 tbl_rpc_productiondata_latest 抽油机生产数据实时表

| **序号** | **代码**                   | **名称**       | **单位** | **类型**      | **为空**     | **键** | **备注** |
|----------|----------------------------|----------------|----------|---------------|--------------|--------|----------|
| 1&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; | id             | 记录编号 |          | NUMBER(10)    | N&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;            | 主键   |
| 2        | wellid                     | 井编号         |          | NUMBER(10)    | N            | 外键   |  
| 3        | acquisitiontime            | 采集时间       |          | DATE          | Y            |        |  
| 4        | liftingtype                | 举升类型       |          | NUMBER(10)    | Y            |        |  
| 5        | displacementtype           | 驱替类型       |          | NUMBER(1)     | Y            |        |  
| 6        | runtime                    | 生产时间       | h        | NUMBER(8,2)   | Y            |        |  
| 7        | crudeoildensity            | 原油密度       | g/cm^3   | NUMBER(16,2)  | Y            |        |  
| 8        | waterdensity               | 水密度         | g/cm^3   | NUMBER(16,2)  | Y            |        |  
| 9        | naturalgasrelativedensity  | 天然气相对密度 |          | NUMBER(16,2)  | Y            |        |  
| 10       | saturationpressure         | 饱和压力       | MPa      | NUMBER(16,2)  | Y            |        |  
| 11       | reservoirdepth             | 油层中部深度   | m        | NUMBER(16,2)  | Y            |        |  
| 12       | reservoirtemperature       | 油层中部温度   | ℃        | NUMBER(16,2)  | Y            |        |  
| 13       | watercut                   | 体积含水率     | %        | NUMBER(8,2)   | Y            |        |  
| 14       | watercut_w                 | 重量含水率     | %        | NUMBER(8,2)   | Y            |        |  
| 15       | tubingpressure             | 油压           | MPa      | NUMBER(8,2)   | Y            |        |  
| 16       | casingpressure             | 套压           | MPa      | NUMBER(8,2)   | Y            |        |  
| 17       | backpressure               | 回压           | MPa      | NUMBER(8,2)   | Y            |        |  
| 18       | wellheadfluidtemperature   | 井口流温       | ℃        | NUMBER(8,2)   | Y            |        |  
| 19       | producingfluidlevel        | 动液面         | m        | NUMBER(8,2)   | Y            |        |  
| 20       | pumpsettingdepth           | 泵挂           | m        | NUMBER(8,2)   | Y            |        |  
| 21       | productiongasoilratio      | 生产气油比     | m^3/t    | NUMBER(8,2)   | Y            |        |  
| 22       | tubingstringinsidediameter | 油管内径       | mm       | NUMBER(8,2)   | Y            |        |  
| 23       | casingstringinsidediameter | 油层套管内径   | mm       | NUMBER(8,2)   | Y            |        |  
| 24       | rodstring                  | 抽油杆参数     |          | VARCHAR2(200) | Y            |        |  
| 25       | pumpgrade                  | 泵级别         |          | NUMBER(1)     | Y            |        |  
| 26       | pumpborediameter           | 泵径           | mm       | NUMBER(8,2)   | Y            |        |  
| 27       | plungerlength              | 柱塞长         | m        | NUMBER(8,2)   | Y            |        |  
| 28       | pumptype                   | 泵类型         |          | VARCHAR2(20)  | Y            |        |  
| 29       | barreltype                 | 泵筒类型       |          | VARCHAR2(20)  | Y            |        |  
| 30       | barrellength               | 泵筒长         | m        | NUMBER(8,2)   | Y            |        |  
| 31       | barrelseries               | 泵级数         |          | NUMBER(8,2)   | Y            |        |  
| 32       | rotordiameter              | 转子截面直径   | mm       | NUMBER(8,2)   | Y            |        |  
| 33       | qpr                        | 公称排量       |          | NUMBER(8,2)   | Y            |        |  
| 34       | manualintervention         | 人工干预       |          | NUMBER(4)     | Y            |        |  
| 35       | netgrossratio              | 净毛比         |          | NUMBER(8,2)   | Y            |        |  
| 36       | anchoringstate             | 锚定状态       |          | NUMBER(1)     | Y            |        |  
| 37       | remark                     | 备注           |          | VARCHAR2(200) | Y            |        |  

### 1.3.15 tbl_rpc_productiondata_hist 抽油机生产数据历史表

同tbl_rpc_productiondata_latest

### 1.3.16 tbl_rpc_discrete_latest 抽油机离散数据实时表

| **序号** | **代码**                  | **名称**                     | **单位** | **类型**       | **为空**     | **键** |
|----------|---------------------------|------------------------------|----------|----------------|--------------|--------|
| 1&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;| id    | 记录编号     |          | NUMBER(10)     | N&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;  | 主键   |
| 2        | wellid                    | 井编号                       |          | NUMBER(10)     | N            | 外键   | 
| 3        | acquisitiontime           | 采集时间                     |          | DATE           | Y            |        | 
| 4        | commstatus                | 通信状态                     |          | NUMBER(2)      | Y            |        | 
| 5        | commtime                  | 在线时间                     | h         | NUMBER(8,2)    | Y            |        | 
| 6        | commtimeefficiency        | 在线时率                     |          | NUMBER(10,4)   | Y            |        | 
| 7        | commrange                 | 在线区间                     |          | VARCHAR2(2000) | Y            |        | 
| 8        | runstatus                 | 运行状态                     |          | NUMBER(2)      | Y            |        | 
| 9        | runtimeefficiency         | 运行时率                     |          | NUMBER(10,4)   | Y            |        | 
| 10       | runtime                   | 运行时间                     | h         | NUMBER(8,2)    | Y            |        | 
| 11       | runrange                  | 运行区间                     |          | VARCHAR2(2000) | Y            |        | 
| 12       | ia                        | A相电流                      | A        | NUMBER(8,2)    | Y            |        | 
| 13       | ib                        | B相电流                      | A        | NUMBER(8,2)    | Y            |        | 
| 14       | ic                        | C相电流                      | A        | NUMBER(8,2)    | Y            |        | 
| 15       | va                        | A相电压                      | V        | NUMBER(8,2)    | Y            |        | 
| 16       | vb                        | B相电压                      | V        | NUMBER(8,2)    | Y            |        | 
| 17       | vc                        | C相电压                      | V        | NUMBER(8,2)    | Y            |        | 
| 18       | totalwattenergy           | 累计有功电能                 | kW·h     | NUMBER(8,2)    | Y            |        | 
| 19       | totalvarenergy            | 累计无功电能                 | kVar·h   | NUMBER(8,2)    | Y            |        | 
| 20       | wattsum                   | 三相总有功功率               | kW       | NUMBER(8,2)    | Y            |        | 
| 21       | varsum                    | 三相总无功功率               | kVar     | NUMBER(8,2)    | Y            |        | 
| 22       | reversepower              | 反向功率                     |          | NUMBER(8,2)    | Y            |        | 
| 23       | pfsum                     | 三相综合功率因数             |          | NUMBER(8,2)    | Y            |        | 
| 24       | acqcycle_diagram          | 功图采集周期                 | min      | NUMBER(6)      | Y            |        | 
| 25       | frequencysetvalue         | 变频设置频率                 | HZ       | NUMBER(8,2)    | Y            |        | 
| 26       | frequencyrunvalue         | 变频运行频率                 | HZ       | NUMBER(8,2)    | Y            |        | 
| 27       | tubingpressure            | 油压                         | MPa      | NUMBER(8,2)    | Y            |        | 
| 28       | casingpressure            | 套压                         | MPa      | NUMBER(8,2)    | Y            |        | 
| 29       | backpressure              | 回压                         | MPa      | NUMBER(8,2)    | Y            |        | 
| 30       | wellheadfluidtemperature  | 井口油温                     | ℃        | NUMBER(8,2)    | Y            |        | 
| 31       | totaywattenergy           | 日有功电能                   | kW·h     | NUMBER(8,2)    | Y            |        | 
| 32       | workingconditioncode      | 电参工况                     |          | NUMBER(4)      | Y            |        | 
| 33       | iaalarm                   | A相电流报警项                |          | VARCHAR2(20)   | Y            |        | 
| 34       | ibalarm                   | B相电流报警项                |          | VARCHAR2(20)   | Y            |        | 
| 35       | icalarm                   | C相电流报警项                |          | VARCHAR2(20)   | Y            |        | 
| 36       | vaalarm                   | A相电压报警项                |          | VARCHAR2(20)   | Y            |        | 
| 37       | vbalarm                   | B相电压报警项                |          | VARCHAR2(20)   | Y            |        | 
| 38       | vcalarm                   | C相电压报警项                |          | VARCHAR2(20)   | Y            |        | 
| 39       | workingconditionstring    | 电参工况字符串               |          | VARCHAR2(4000) | Y            |        | 
| 40       | iauplimit                 | A相电流上限                  | A        | NUMBER(8,2)    | Y            |        | 
| 41       | iadownlimit               | A相电流下限                  | A        | NUMBER(8,2)    | Y            |        | 
| 42       | iazero                    | A相电流零值                  | A        | NUMBER(8,2)    | Y            |        | 
| 43       | ibuplimit                 | B相电流上限                  | A        | NUMBER(8,2)    | Y            |        | 
| 44       | ibdownlimit               | B相电流下限                  | A        | NUMBER(8,2)    | Y            |        | 
| 45       | ibzero                    | B相电流零值                  | A        | NUMBER(8,2)    | Y            |        | 
| 46       | icuplimit                 | C相电流上限                  | A        | NUMBER(8,2)    | Y            |        | 
| 47       | icdownlimit               | C相电流下限                  | A        | NUMBER(8,2)    | Y            |        | 
| 48       | iczero                    | C相电流零值                  | A        | NUMBER(8,2)    | Y            |        | 
| 49       | vauplimit                 | A相电压上限                  | V        | NUMBER(8,2)    | Y            |        | 
| 50       | vadownlimit               | A相电压下限                  | V        | NUMBER(8,2)    | Y            |        | 
| 51       | vazero                    | A相电压零值                  | V        | NUMBER(8,2)    | Y            |        | 
| 52       | vbuplimit                 | B相电压上限                  | V        | NUMBER(8,2)    | Y            |        | 
| 53       | vbdownlimit               | B相电压下限                  | V        | NUMBER(8,2)    | Y            |        | 
| 54       | vbzero                    | B相电压零值                  | V        | NUMBER(8,2)    | Y            |        | 
| 55       | vcuplimit                 | C相电压上限                  | V        | NUMBER(8,2)    | Y            |        | 
| 56       | vcdownlimit               | C相电压下限                  | V        | NUMBER(8,2)    | Y            |        | 
| 57       | vczero                    | C相电压零值                  | V        | NUMBER(8,2)    | Y            |        | 
| 58       | totalpwattenergy          | 累计正向有功电能             | kW·h     | NUMBER(8,2)    | Y            |        | 
| 59       | totalnwattenergy          | 累计反向有功电能             | kW·h     | NUMBER(8,2)    | Y            |        | 
| 60       | totalpvarenergy           | 累计正向无功电能             | kVar·h   | NUMBER(8,2)    | Y            |        | 
| 61       | totalnvarenergy           | 累计反向无功电能             | kVar·h   | NUMBER(8,2)    | Y            |        | 
| 62       | totalvaenergy             | 累计视在电能                 | kVA·h    | NUMBER(8,2)    | Y            |        | 
| 63       | todaypwattenergy          | 日正向有功电能               | kW·h     | NUMBER(8,2)    | Y            |        | 
| 64       | todaynwattenergy          | 日反向有功电能               | kW·h     | NUMBER(8,2)    | Y            |        | 
| 65       | todayvarenergy            | 日无功电能                   | kVar·h   | NUMBER(8,2)    | Y            |        | 
| 66       | todaypvarenergy           | 日正向无功电能               | kVar·h   | NUMBER(8,2)    | Y            |        | 
| 67       | todaynvarenergy           | 日反向无功电能               | kVar·h   | NUMBER(8,2)    | Y            |        | 
| 68       | todayvaenergy             | 日视在电能                   | kVA·h    | NUMBER(8,2)    | Y            |        | 
| 69       | vasum                     | 视在功率                     | kVA      | NUMBER(8,2)    | Y            |        | 
| 70       | signal                    | 信号强度                     |          | NUMBER(8,2)    | Y            |        | 
| 71       | interval                  | 传输间隔                     | min      | NUMBER(10)     | Y            |        | 
| 72       | devicever                 | 设备版本信息                 |          | VARCHAR2(50)   | Y            |        | 
| 73       | vavg                      | 三相电压平均值               | V        | NUMBER(8,2)    | Y            |        | 
| 74       | iavg                      | 三相电流平均值               | A        | NUMBER(8,2)    | Y            |        | 
| 75       | watta                     | A相有功功率                  | kW       | NUMBER(8,2)    | Y            |        | 
| 76       | wattb                     | B相有功功率                  | kW       | NUMBER(8,2)    | Y            |        | 
| 77       | wattc                     | C相有功功率                  | kW       | NUMBER(8,2)    | Y            |        | 
| 78       | vara                      | A相无功功率                  | kVar     | NUMBER(8,2)    | Y            |        | 
| 79       | varb                      | B相无功功率                  | kVar     | NUMBER(8,2)    | Y            |        | 
| 80       | varc                      | C相无功功率                  | kVar     | NUMBER(8,2)    | Y            |        | 
| 81       | vaa                       | A相视在功率                  | kVA      | NUMBER(8,2)    | Y            |        | 
| 82       | vab                       | B相视在功率                  | kVA      | NUMBER(8,2)    | Y            |        | 
| 83       | vac                       | C相视在功率                  | kVA      | NUMBER(8,2)    | Y            |        | 
| 84       | pfa                       | A相功率因数                  |          | NUMBER(8,2)    | Y            |        | 
| 85       | pfb                       | B相功率因数                  |          | NUMBER(8,2)    | Y            |        | 
| 86       | pfc                       | C相功率因数                  |          | NUMBER(8,2)    | Y            |        | 
| 87       | balancecontrolmode        | 平衡远程调节远程触发控制     |          | NUMBER(10)     | Y            |        | 
| 88       | balancecalculatemode      | 平衡计算方式                 |          | NUMBER(10)     | Y            |        | 
| 89       | balanceawaytime           | 重心远离支点调节时间         | ms       | NUMBER(10)     | Y            |        | 
| 90       | balanceclosetime          | 重心接近支点调节时间         | ms       | NUMBER(10)     | Y            |        | 
| 91       | balancestrokecount        | 参与平衡度计算的冲程测量次数 |          | NUMBER(10)     | Y            |        | 
| 92       | balanceoperationuplimit   | 平衡调节上限                 | %        | NUMBER(10)     | Y            |        | 
| 93       | balanceoperationdownlimit | 平衡调节下限                 | %        | NUMBER(10)     | Y            |        | 
| 94       | balanceautocontrol        | 平衡远程自动调节             |          | NUMBER(1)      | Y            |        | 
| 95       | balancefrontlimit         | 平衡前限位                   |          | NUMBER(1)      | Y            |        | 
| 96       | balanceafterlimit         | 平衡后限位                   |          | NUMBER(1)      | Y            |        | 
| 97       | spmautocontrol            | 冲次远程自动调节             |          | NUMBER(1)      | Y            |        | 
| 98       | balanceawaytimeperbeat    | 重心远离支点每拍调节时间     | ms       | NUMBER(10)     | Y            |        | 
| 99       | balanceclosetimeperbeat   | 重心接近支点每拍调节时间     | ms       | NUMBER(10)     | Y            |        | 

### 1.3.17 tbl_rpc_discrete_hist 抽油机离散数据历史表

同tbl_rpc_discrete_latest

### 1.3.18 tbl_rpc_diagram_latest 抽油机曲线数据实时表

| **序号** | **代码**                     | **名称**             | **单位**    | **类型**      | **为空**     | **键** |
|----------|------------------------------|----------------------|-------------|---------------|--------------|--------|
| 1&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;   | id    | 记录编号     |             | NUMBER(10)    | N&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;  | 主键   | 
| 2        | wellid                       | 井编号               |             | NUMBER(10)    | N            | 外键   | 
| 3        | acquisitiontime              | 采集时间             |             | DATE          | Y            |        | 
| 4        | stroke                       | 冲程                 | m           | NUMBER(8,2)   | Y            |        | 
| 5        | spm                          | 冲次                 | 次/min      | NUMBER(8,2)   | Y            |        | 
| 6        | fmax                         | 最大载荷             | kN          | NUMBER(8,2)   | Y            |        | 
| 7        | fmin                         | 最小载荷             | kN          | NUMBER(8,2)   | Y            |        | 
| 8        | position_curve               | 位移曲线             | m           | CLOB          | Y            |        | 
| 9        | angle_curve                  | 角度曲线             | °           | CLOB          | Y            |        | 
| 10       | load_curve                   | 载荷曲线             | kN          | CLOB          | Y            |        | 
| 11       | power_curve                  | 功率曲线             | kW          | CLOB          | Y            |        | 
| 12       | current_curve                | 电流曲线             | A           | CLOB          | Y            |        | 
| 13       | rpm_curve                    | 电机转速曲线         | r/min       | CLOB          | Y            |        | 
| 14       | rawpower_curve               | 功率原始曲线         | kW          | CLOB          | Y            |        | 
| 15       | rawcurrent_curve             | 电流原始曲线         | A           | CLOB          | Y            |        | 
| 16       | rawrpm_curve                 | 电机转速原始曲线     | r/min       | CLOB          | Y            |        | 
| 17       | upstrokeimax                 | 上冲程最大电流       | A           | NUMBER(8,2)   | Y            |        | 
| 18       | downstrokeimax               | 下冲程最大电流       | A           | NUMBER(8,2)   | Y            |        | 
| 19       | upstrokewattmax              | 上冲程最大功率       | kW          | NUMBER(8,2)   | Y            |        | 
| 20       | downstrokewattmax            | 下冲程最大功率       | kW          | NUMBER(8,2)   | Y            |        | 
| 21       | idegreebalance               | 电流平衡度           | %           | NUMBER(8,2)   | Y            |        | 
| 22       | wattdegreebalance            | 功率平衡度           | %           | NUMBER(8,2)   | Y            |        | 
| 23       | datasource                   | 功图来源             |             | NUMBER(1)     | Y            |        | 
| 24       | workingconditioncode         | 工况类型             |             | NUMBER(4)     | Y            |        | 
| 25       | fullnesscoefficient          | 功图充满系数         | 小数        | NUMBER(12,3)  | Y            |        | 
| 26       | upperloadline                | 理论上载荷           | kN          | NUMBER(8,2)   | Y            |        | 
| 27       | upperloadlineofexact         | 真实理论上载荷       | kN          | NUMBER(8,2)   | Y            |        | 
| 28       | lowerloadline                | 理论下载荷           | kN          | NUMBER(8,2)   | Y            |        | 
| 29       | pumpfsdiagram                | 泵功图               |             | CLOB          | Y            |        | 
| 30       | theoreticalproduction        | 理论排量             | m^3/d       | NUMBER(8,2)   | Y            |        | 
| 31       | liquidvolumetricproduction   | 计算单井日产液量方   | m^3/d       | NUMBER(8,2)   | Y            |        | 
| 32       | oilvolumetricproduction      | 计算单井日产油量方   | m^3/d       | NUMBER(8,2)   | Y            |        | 
| 33       | watervolumetricproduction    | 计算单井日产水量方   | m^3/d       | NUMBER(8,2)   | Y            |        | 
| 34       | availableplungerstrokeprod_v | 泵有效冲程计算产量方 | m^3/d       | NUMBER(8,2)   | Y            |        | 
| 35       | pumpclearanceleakprod_v      | 泵间隙漏失量方       | m^3/d       | NUMBER(8,2)   | Y            |        | 
| 36       | tvleakvolumetricproduction   | 游动凡尔漏失量方     | m^3/d       | NUMBER(8,2)   | Y            |        | 
| 37       | svleakvolumetricproduction   | 固定凡尔漏失量方     | m^3/d       | NUMBER(8,2)   | Y            |        | 
| 38       | gasinfluenceprod_v           | 气影响方             | m^3/d       | NUMBER(8,2)   | Y            |        | 
| 39       | liquidweightproduction       | 计算单井日产液量吨   | t/d         | NUMBER(8,2)   | Y            |        | 
| 40       | oilweightproduction          | 计算单井日产油量吨   | t/d         | NUMBER(8,2)   | Y            |        | 
| 41       | waterweightproduction        | 计算单井日产水量吨   | t/d         | NUMBER(8,2)   | Y            |        | 
| 42       | availableplungerstrokeprod_w | 泵有效冲程计算产量吨 | t/d         | NUMBER(8,2)   | Y            |        | 
| 43       | pumpclearanceleakprod_w      | 泵间隙漏失量吨       | t/d         | NUMBER(8,2)   | Y            |        | 
| 44       | tvleakweightproduction       | 游动凡尔漏失量吨     | t/d         | NUMBER(8,2)   | Y            |        | 
| 45       | svleakweightproduction       | 固定凡尔漏失量吨     | t/d         | NUMBER(8,2)   | Y            |        | 
| 46       | gasinfluenceprod_w           | 气影响吨             | t/d         | NUMBER(8,2)   | Y            |        | 
| 47       | motorinputactivepower        | 有功功率             | kW          | NUMBER(8,2)   | Y            |        | 
| 48       | polishrodpower               | 光杆功率             | kW          | NUMBER(8,2)   | Y            |        | 
| 49       | waterpower                   | 水功率               | kW          | NUMBER(8,2)   | Y            |        | 
| 50       | surfacesystemefficiency      | 地面系统效率         | 小数        | NUMBER(12,3)  | Y            |        | 
| 51       | welldownsystemefficiency     | 井下系统效率         | 小数        | NUMBER(12,3)  | Y            |        | 
| 52       | systemefficiency             | 系统效率             | 小数        | NUMBER(12,3)  | Y            |        | 
| 53       | powerconsumptionperthm       | 吨液百米耗电量       | kW·h/100m·t | NUMBER(8,2)   | Y            |        | 
| 54       | fsdiagramarea                | 功图面积             |             | NUMBER(8,2)   | Y            |        | 
| 55       | rodflexlength                | 抽油杆伸长量         | m           | NUMBER(8,2)   | Y            |        | 
| 56       | tubingflexlength             | 油管伸缩量           | m           | NUMBER(8,2)   | Y            |        | 
| 57       | inertialength                | 惯性增量             | m           | NUMBER(8,2)   | Y            |        | 
| 58       | pumpeff1                     | 冲程损失系数         | 小数        | NUMBER(12,3)  | Y            |        | 
| 59       | pumpeff2                     | 充满系数             | 小数        | NUMBER(12,3)  | Y            |        | 
| 60       | pumpeff3                     | 间隙漏失系数         | 小数        | NUMBER(12,3)  | Y            |        | 
| 61       | pumpeff4                     | 液体收缩系数         | 小数        | NUMBER(12,3)  | Y            |        | 
| 62       | pumpeff                      | 总泵效               | 小数        | NUMBER(12,3)  | Y            |        | 
| 63       | pumpintakep                  | 泵入口压力           | MPa         | NUMBER(8,2)   | Y            |        | 
| 64       | pumpintaket                  | 泵入口温度           | ℃           | NUMBER(8,2)   | Y            |        | 
| 65       | pumpintakegol                | 泵入口就地气液比     | m^3/m^3     | NUMBER(8,2)   | Y            |        | 
| 66       | pumpinletvisl                | 泵入口液体粘度       | mPa·s       | NUMBER(8,2)   | Y            |        | 
| 67       | pumpinletbo                  | 泵入口原油体积系数   | 小数        | NUMBER(8,2)   | Y            |        | 
| 68       | pumpoutletp                  | 泵出口压力           | MPa         | NUMBER(8,2)   | Y            |        | 
| 69       | pumpoutlett                  | 泵出口温度           | ℃           | NUMBER(8,2)   | Y            |        | 
| 70       | pumpoutletgol                | 泵出口就地气液比     | m^3/m^3     | NUMBER(8,2)   | Y            |        | 
| 71       | pumpoutletvisl               | 泵出口液体粘度       | mPa·s       | NUMBER(8,2)   | Y            |        | 
| 72       | pumpoutletbo                 | 泵出口原油体积系数   | 小数        | NUMBER(8,2)   | Y            |        | 
| 73       | rodstring                    | 抽油杆柱分析数据     |             | VARCHAR2(200) | Y            |        |
| 74       | savetime                     | 入库时间             |             | DATE          | Y            |        | 
| 75       | productiondataid             | 生产数据编号         |             | NUMBER(10)    | Y            |        | 
| 76       | resultstatus                 | 计算标志             |             | NUMBER(2)     | Y            |        | 
| 77       | inverresultstatus            | 功图反演状态         |             | NUMBER(2)     | Y            |        | 
| 78       | remark                       | 备注                 |             | VARCHAR2(200) | Y            |        | 
| 79       | position360_curve            | 360度均分位移曲线    | m           | CLOB          | Y            |        | 
| 80       | angle360_curve               | 360度均分角度曲线    | °           | CLOB          | Y            |        | 
| 81       | load360_curve                | 360度均分载荷曲线    | kN          | CLOB          | Y            |        | 
| 82       | signal                       | 信号强度             |             | NUMBER(8,2)   | Y            |        | 
| 83       | interval                     | 传输间隔             | min         | NUMBER(10)    | Y            |        | 
| 84       | devicever                    | 设备版本信息         |             | VARCHAR2(50)  | Y            |        | 
| 85       | discretedataid               | 离散数据编号         |             | NUMBER(10)    | Y            |        | 

### 1.3.19 tbl_rpc_diagram_hist 抽油机曲线数据历史表

同tbl_rpc_diagram_latest

### 1.3.20 tbl_rpc_worktype 抽油机工况类型表

| **序号** | **代码**                    | **名称**   | **单位** | **类型**      | **为空**     | **键** |
|----------|-----------------------------|------------|----------|---------------|--------------|--------|
| 1&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;  | id         | 记录编号 |      | NUMBER(10)    | N&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;| 主键   |
| 2        | workingconditioncode        | 工况类型   |          | NUMBER(4)     | N            |        |
| 3        | workingconditionname        | 工况名称   |          | VARCHAR2(200) | N            |        |
| 4        | workingconditiondescription | 工况说明   |          | VARCHAR2(200) | Y            |        |
| 5        | workingconditiontemplate    | 工况模板   |          | BLOB          | Y            |        |
| 6        | optimizationsuggestion      | 优化建议   |          | VARCHAR2(200) | Y            |        |
| 7        | remark                      | 备注       |          | VARCHAR2(200) | Y            |        |

### 1.3.21 tbl_rpc_alarmtype_conf 抽油机报警类型表

| **序号** | **代码**             | **名称**   | **单位** | **类型**      | **为空**     | **键** |
|----------|----------------------|------------|----------|---------------|--------------|--------|
| 1&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; | id   | 记录编号   |          | NUMBER(10)    | N&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;            | 主键   |
| 2        | workingconditioncode | 工况类型   |          | NUMBER(10)    | N            |        |
| 3        | alarmtype            | 报警类型   |          | NUMBER(3)     | N            |        |
| 4        | alarmlevel           | 报警级别   |          | NUMBER(3)     | N            |        |
| 5        | alarmsign            | 报警标志   |          | NUMBER(1)     | Y            |        |
| 6        | remark               | 备注       |          | VARCHAR2(200) | Y            |        |

### 1.3.22 tbl_rpc_total_day 抽油机日累计数据表

| **序号** | **代码**                      | **名称**                 | **单位**    | **类型**       | **为空**     | **键** |
|----------|-------------------------------|--------------------------|-------------|----------------|--------------|--------|
| 1&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;    | id    | 记录编号         |             | NUMBER(10)     | N&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; | 主键   |
| 2        | wellid                        | 井编号                   |             | NUMBER(10)     | Y            | 外键   | 
| 3        | calculatedate                 | 计算时间                 |             | DATE           | Y            |        | 
| 4        | commstatus                    | 通信状态                 |             | NUMBER(2)      | Y            |        | 
| 5        | runstatus                     | 运行状态                 |             | NUMBER(2)      | Y            |        | 
| 6        | commtime                      | 通信时间                 | h            | NUMBER(8,2)    | Y            |        | 
| 7        | commtimeefficiency            | 通信时率                 |             | NUMBER(12,3)   | Y            |        | 
| 8        | commrange                     | 通信区间                 |             | VARCHAR2(4000) | Y            |        | 
| 9        | runtime                       | 运行时间                 | h            | NUMBER(8,2)    | Y            |        | 
| 10       | runrange                      | 运行区间                 |             | VARCHAR2(4000) | Y            |        | 
| 11       | runtimeefficiency             | 生产时率                 | 小数        | NUMBER(12,3)   | Y            |        | 
| 12       | workingconditioncode          | 工况类型                 |             | NUMBER(4)      | Y            |        | 
| 13       | workingconditionstring        | 功图工况字符串           |             | VARCHAR2(4000) | Y            |        | 
| 14       | workingconditioncode_e        | 电参工况类型             |             | NUMBER(4)      | Y            |        | 
| 15       | workingconditionstring_e      | 电参工况字符串           |             | VARCHAR2(4000) | Y            |        | 
| 16       | fullnesscoefficient           | 功图充满系数             | 小数        | NUMBER(10,4)   | Y            |        | 
| 17       | fullnesscoefficientmax        | 功图充满系数最大值       | 小数        | NUMBER(10,4)   | Y            |        | 
| 18       | fullnesscoefficientmin        | 功图充满系数最小值       | 小数        | NUMBER(10,4)   | Y            |        | 
| 19       | stroke                        | 冲程                     | m           | NUMBER(8,2)    | Y            |        | 
| 20       | strokemax                     | 冲程最大值               | m           | NUMBER(8,2)    | Y            |        | 
| 21       | strokemin                     | 冲程最小值               | m           | NUMBER(8,2)    | Y            |        | 
| 22       | spm                           | 冲次                     | 次/min      | NUMBER(8,2)    | Y            |        | 
| 23       | spmmax                        | 冲次最大值               | 次/min      | NUMBER(8,2)    | Y            |        | 
| 24       | spmmin                        | 冲次最小值               | 次/min      | NUMBER(8,2)    | Y            |        | 
| 25       | liquidvolumetricproduction    | 计算单井日产液量方       | m^3/d       | NUMBER(8,2)    | Y            |        | 
| 26       | oilvolumetricproduction       | 计算单井日产油量方       | m^3/d       | NUMBER(8,2)    | Y            |        | 
| 27       | watervolumetricproduction     | 计算单井日产水量方       | m^3/d       | NUMBER(8,2)    | Y            |        | 
| 28       | liquidweightproduction        | 计算单井日产液量吨       | t/d         | NUMBER(8,2)    | Y            |        | 
| 29       | oilweightproduction           | 计算单井日产油量吨       | t/d         | NUMBER(8,2)    | Y            |        | 
| 30       | waterweightproduction         | 计算单井日产水量吨       | t/d         | NUMBER(8,2)    | Y            |        | 
| 31       | liquidvolumetricproductionmax | 计算单井日产液量最大值方 | m^3/d      | NUMBER(8,2)    | Y            |        | 
| 32       | liquidvolumetricproductionmin | 计算单井日产液量最小值方 | m^3/d      | NUMBER(8,2)    | Y            |        | 
| 33       | oilvolumetricproductionmax    | 计算单井日产油量最大值方 | m^3/d      | NUMBER(8,2)    | Y            |        | 
| 34       | oilvolumetricproductionmin    | 计算单井日产油量最小值方 | m^3/d      | NUMBER(8,2)    | Y            |        | 
| 35       | watervolumetricproductionmax  | 计算单井日产水量最大值方 | m^3/d      | NUMBER(8,2)    | Y            |        | 
| 36       | watervolumetricproductionmin  | 计算单井日产水量最小值方 | m^3/d      | NUMBER(8,2)    | Y            |        | 
| 37       | liquidweightproductionmax     | 计算单井日产液量最大值吨 | t/d         | NUMBER(8,2)    | Y            |        | 
| 38       | liquidweightproductionmin     | 计算单井日产液量最小值吨 | t/d         | NUMBER(8,2)    | Y            |        | 
| 39       | oilweightproductionmax        | 计算单井日产油量最大值吨 | t/d         | NUMBER(8,2)    | Y            |        | 
| 40       | oilweightproductionmin        | 计算单井日产油量最小值吨 | t/d         | NUMBER(8,2)    | Y            |        | 
| 41       | waterweightproductionmax      | 计算单井日产水量最大值吨 | t/d         | NUMBER(8,2)    | Y            |        | 
| 42       | waterweightproductionmin      | 计算单井日产水量最小值吨 | t/d         | NUMBER(8,2)    | Y            |        | 
| 43       | wattdegreebalance             | 功率平衡度               | %           | NUMBER(8,2)    | Y            |        | 
| 44       | idegreebalance                | 电流平衡度               | %           | NUMBER(8,2)    | Y            |        | 
| 45       | wattdegreebalancemax          | 功率平衡度最大值         | %           | NUMBER(8,2)    | Y            |        | 
| 46       | wattdegreebalancemin          | 功率平衡度最小值         | %           | NUMBER(8,2)    | Y            |        | 
| 47       | idegreebalancemax             | 电流平衡度最大值         | %           | NUMBER(8,2)    | Y            |        | 
| 48       | idegreebalancemin             | 电流平衡度最小值         | %           | NUMBER(8,2)    | Y            |        | 
| 49       | deltaradius                   | 移动距离                 | m           | NUMBER(8,2)    | Y            |        | 
| 50       | deltaradiusmax                | 移动距离最大值           | m           | NUMBER(8,2)    | Y            |        | 
| 51       | deltaradiusmin                | 移动距离最小值           | m           | NUMBER(8,2)    | Y            |        | 
| 52       | watercut                      | 体积含水率               | %           | NUMBER(10,4)   | Y            |        | 
| 53       | watercut_w                    | 重量含水率               | %           | NUMBER(10,4)   | Y            |        | 
| 54       | watercutmax                   | 体积含水率最大值         | %           | NUMBER(10,4)   | Y            |        | 
| 55       | watercutmin                   | 体积含水率最小值         | %           | NUMBER(10,4)   | Y            |        | 
| 56       | watercutmax_w                 | 重量含水率最大值         | %           | NUMBER(10,4)   | Y            |        | 
| 57       | watercutmin_w                 | 重量含水率最小值         | %           | NUMBER(10,4)   | Y            |        | 
| 58       | tubingpressure                | 油压                     | MPa         | NUMBER(8,2)    | Y            |        | 
| 59       | tubingpressuremax             | 油压最大值               | MPa         | NUMBER(8,2)    | Y            |        | 
| 60       | tubingpressuremin             | 油压最小值               | MPa         | NUMBER(8,2)    | Y            |        | 
| 61       | casingpressure                | 套压                     | MPa         | NUMBER(8,2)    | Y            |        | 
| 62       | casingpressuremax             | 套压最大值               | MPa         | NUMBER(8,2)    | Y            |        | 
| 63       | casingpressuremin             | 套压最小值               | MPa         | NUMBER(8,2)    | Y            |        | 
| 64       | wellheadfluidtemperature      | 井口油温                 | ℃           | NUMBER(8,2)    | Y            |        | 
| 65       | wellheadfluidtemperaturemax   | 井口油温最大值           | ℃           | NUMBER(8,2)    | Y            |        | 
| 66       | wellheadfluidtemperaturemin   | 井口油温最小值           | ℃           | NUMBER(8,2)    | Y            |        | 
| 67       | productiongasoilratio         | 生产气油比               | m^3/t            | NUMBER(8,2)    | Y            |        | 
| 68       | productiongasoilratiomax      | 生产气油比最大值         | m^3/t            | NUMBER(8,2)    | Y            |        | 
| 69       | productiongasoilratiomin      | 生产气油比最小值         | m^3/t            | NUMBER(8,2)    | Y            |        | 
| 70       | producingfluidlevel           | 动液面                   | m           | NUMBER(8,2)    | Y            |        | 
| 71       | producingfluidlevelmax        | 动液面最大值             | m           | NUMBER(8,2)    | Y            |        | 
| 72       | producingfluidlevelmin        | 动液面最小值             | m           | NUMBER(8,2)    | Y            |        | 
| 73       | pumpsettingdepth              | 泵挂                     | m           | NUMBER(8,2)    | Y            |        | 
| 74       | pumpsettingdepthmax           | 泵挂最大值               | m           | NUMBER(8,2)    | Y            |        | 
| 75       | pumpsettingdepthmin           | 泵挂最小值               | m           | NUMBER(8,2)    | Y            |        | 
| 76       | submergence                   | 沉没度                   | m           | NUMBER(8,2)    | Y            |        | 
| 77       | submergencemax                | 沉没度最大值             | m           | NUMBER(8,2)    | Y            |        | 
| 78       | submergencemin                | 沉没度最小值             | m           | NUMBER(8,2)    | Y            |        | 
| 79       | pumpborediameter              | 泵径                     | mm          | NUMBER(8,2)    | Y            |        | 
| 80       | pumpborediametermax           | 泵径最大值               | mm          | NUMBER(8,2)    | Y            |        | 
| 81       | pumpborediametermin           | 泵径最小值               | mm          | NUMBER(8,2)    | Y            |        | 
| 82       | systemefficiency              | 系统效率                 | 小数        | NUMBER(10,4)   | Y            |        | 
| 83       | systemefficiencymax           | 系统效率最大值           | 小数        | NUMBER(10,4)   | Y            |        | 
| 84       | systemefficiencymin           | 系统效率最小值           | 小数        | NUMBER(10,4)   | Y            |        | 
| 85       | surfacesystemefficiency       | 地面效率                 | 小数        | NUMBER(10,4)   | Y            |        | 
| 86       | surfacesystemefficiencymax    | 地面效率最大值           | 小数        | NUMBER(10,4)   | Y            |        | 
| 87       | surfacesystemefficiencymin    | 地面效率最小值           | 小数        | NUMBER(10,4)   | Y            |        | 
| 88       | welldownsystemefficiency      | 井下效率                 | 小数        | NUMBER(10,4)   | Y            |        | 
| 89       | welldownsystemefficiencymax   | 井下效率最大值           | 小数        | NUMBER(10,4)   | Y            |        | 
| 90       | welldownsystemefficiencymin   | 井下效率最小值           | 小数        | NUMBER(10,4)   | Y            |        | 
| 91       | powerconsumptionperthm        | 吨液百米耗电量           | kW·h/100m·t | NUMBER(8,2)    | Y            |        | 
| 92       | powerconsumptionperthmmax     | 吨液百米耗电量最大值     | kW·h/100m·t | NUMBER(8,2)    | Y            |        | 
| 93       | powerconsumptionperthmmin     | 吨液百米耗电量最小值     | kW·h/100m·t | NUMBER(8,2)    | Y            |        | 
| 94       | pumpeff                       | 总泵效                   | 小数        | NUMBER(10,4)   | Y            |        | 
| 95       | pumpeffmax                    | 总泵效最大值             | 小数        | NUMBER(10,4)   | Y            |        | 
| 96       | pumpeffmin                    | 总泵效最小值             | 小数        | NUMBER(10,4)   | Y            |        | 
| 97       | ia                            | A相电流                  | A           | NUMBER(8,2)    | Y            |        | 
| 98       | iamax                         | A相电流最大值            | A           | NUMBER(8,2)    | Y            |        | 
| 99       | iamin                         | A相电流最小值            | A           | NUMBER(8,2)    | Y            |        | 
| 100      | ib                            | B相电流                  | A           | NUMBER(8,2)    | Y            |        | 
| 101      | ibmax                         | B相电流最大值            | A           | NUMBER(8,2)    | Y            |        | 
| 102      | ibmin                         | B相电流最小值            | A           | NUMBER(8,2)    | Y            |        | 
| 103      | ic                            | C相电流                  | A           | NUMBER(8,2)    | Y            |        | 
| 104      | icmax                         | C相电流最大值            | A           | NUMBER(8,2)    | Y            |        | 
| 105      | icmin                         | C相电流最小值            | A           | NUMBER(8,2)    | Y            |        | 
| 106      | va                            | A相电压                  | V           | NUMBER(8,2)    | Y            |        | 
| 107      | vamax                         | A相电压最大值            | V           | NUMBER(8,2)    | Y            |        | 
| 108      | vamin                         | A相电压最小值            | V           | NUMBER(8,2)    | Y            |        | 
| 109      | vb                            | B相电压                  | V           | NUMBER(8,2)    | Y            |        | 
| 110      | vbmax                         | B相电压最大值            | V           | NUMBER(8,2)    | Y            |        | 
| 111      | vbmin                         | B相电压最小值            | V           | NUMBER(8,2)    | Y            |        | 
| 112      | vc                            | C相电压                  | V           | NUMBER(8,2)    | Y            |        | 
| 113      | vcmax                         | C相电压最大值            | V           | NUMBER(8,2)    | Y            |        | 
| 114      | vcmin                         | C相电压最小值            | V           | NUMBER(8,2)    | Y            |        | 
| 115      | wattsum                       | 有功功率                 | kW          | NUMBER(8,2)    | Y            |        | 
| 116      | wattsummax                    | 有功功率最大值           | kW          | NUMBER(8,2)    | Y            |        | 
| 117      | wattsummin                    | 有功功率最小值           | kW          | NUMBER(8,2)    | Y            |        | 
| 118      | varsum                        | 无功功率                 | kVar        | NUMBER(8,2)    | Y            |        | 
| 119      | varsummax                     | 无功功率最大值           | kVar        | NUMBER(8,2)    | Y            |        | 
| 120      | varsummin                     | 无功功率最小值           | kVar        | NUMBER(8,2)    | Y            |        | 
| 121      | pfsum                         | 功率因数                 |             | NUMBER(8,2)    | Y            |        | 
| 122      | pfsummax                      | 功率因数最大值           |             | NUMBER(8,2)    | Y            |        | 
| 123      | pfsummin                      | 功率因数最小值           |             | NUMBER(8,2)    | Y            |        | 
| 124      | frequency                     | 运行频率                 | HZ          | NUMBER(8,2)    | Y            |        | 
| 125      | frequencymax                  | 运行频率最大值           | HZ          | NUMBER(8,2)    | Y            |        | 
| 126      | frequencymin                  | 运行频率最小值           | HZ          | NUMBER(8,2)    | Y            |        | 
| 127      | todaywattenergy               | 日有功电能               | kW·h        | NUMBER(8,2)    | Y            |        | 
| 128      | todaypwattenergy              | 日正向有功电能           | kW·h        | NUMBER(8,2)    | Y            |        | 
| 129      | todaynwattenergy              | 日反向有功电能           | kW·h        | NUMBER(8,2)    | Y            |        | 
| 130      | todayvarenergy                | 日无功电能               | kVar·h      | NUMBER(8,2)    | Y            |        | 
| 131      | todaypvarenergy               | 日正向无功电能           | kVar·h      | NUMBER(8,2)    | Y            |        | 
| 132      | todaynvarenergy               | 日反向无功电能           | kVar·h      | NUMBER(8,2)    | Y            |        | 
| 133      | todayvaenergy                 | 日视在电能               | kVA·h       | NUMBER(8,2)    | Y            |        | 
| 134      | totalwattenergy               | 累计有功电能             | kW·h        | NUMBER(8,2)    | Y            |        | 
| 135      | totalpwattenergy              | 累计正向有功电能         | kW·h        | NUMBER(8,2)    | Y            |        | 
| 136      | totalnwattenergy              | 累计反向有功电能         | kW·h        | NUMBER(8,2)    | Y            |        | 
| 137      | totalvarenergy                | 累计无功电能             | kVar·h      | NUMBER(8,2)    | Y            |        | 
| 138      | totalpvarenergy               | 累计正向无功电能         | kVar·h      | NUMBER(8,2)    | Y            |        | 
| 139      | totalnvarenergy               | 累计反向无功电能         | kVar·h      | NUMBER(8,2)    | Y            |        | 
| 140      | totalvaenergy                 | 累计视在电能             | kVA·h       | NUMBER(8,2)    | Y            |        | 
| 141      | rpm                           | 螺杆泵转速               | r/min       | NUMBER(8,2)    | Y            |        | 
| 142      | rpmmax                        | 螺杆泵转速最大值         | r/min       | NUMBER(8,2)    | Y            |        | 
| 143      | rpmmin                        | 螺杆泵转速最小值         | r/min       | NUMBER(8,2)    | Y            |        | 
| 144      | extendeddays                  | 延用天数                 |             | NUMBER(5)      | Y            |        | 
| 145      | resultstatus                  | 计算标志                 |             | NUMBER(2)      | Y            |        | 
| 146      | signal                        | 信号强度                 |             | NUMBER(8,2)    | Y            |        | 
| 147      | signalmax                     | 信号强度最大值           |             | NUMBER(8,2)    | Y            |        | 
| 148      | signalmin                     | 信号强度最小值           |             | NUMBER(8,2)    | Y            |        | 
| 149      | f                             | 载荷                     | kN          | NUMBER(8,2)    | Y            |        | 
| 150      | fmax                          | 载荷最大值               | kN          | NUMBER(8,2)    | Y            |        | 
| 151      | fmin                          | 载荷最小值               | kN          | NUMBER(8,2)    | Y            |        | 
| 152      | savetime                      | 存储时间                 |             | DATE           | Y            |        | 

### 1.3.23 tbl_rpc_statistics_conf 抽油机统计配置表

| **序号** | **代码**     | **名称**   | **单位** | **类型**     | **为空**     | **键** |
|----------|--------------|------------|----------|--------------|--------------|--------|
| 1&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;        | id           | 记录编号   |          | NUMBER（10） | N&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;            | 主键   |
| 2        | s_level      | 级别       |          | VARCHAR2(50) | Y            |        |
| 3        | s_code       | 代码       |          | NUMBER(4)    | Y            |        |
| 4        | s_min        | 范围最小值 |          | NUMBER(11,3) | Y            |        |
| 5        | s_max        | 范围最大值 |          | NUMBER(11,3) | Y            |        |
| 6        | s_type       | 统计类型   |          | VARCHAR2(20) | Y            |        |

### 1.3.24 tbl_rpcinformation 抽油机设备表

| **序号** | **代码**                      | **名称**         | **单位** | **类型**      | **为空**     | **键** |
|----------|-------------------------------|------------------|----------|---------------|--------------|--------|
| 1&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;    | id               | 记录编号 |      | NUMBER(10)    | N&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; | 主键   |  
| 2        | wellid                        | 井编号           |          | NUMBER(10)    | Y            |
| 3        | manufacturer                  | 抽油机厂家       |          | VARCHAR2(200) | Y            |
| 4        | model                         | 抽油机型号       |          | VARCHAR2(200) | Y            |
| 5        | stroke                        | 冲程             | m        | NUMBER(8,2)   | N            |
| 6        | crankrotationdirection        | 旋转方向         |          | VARCHAR2(200) | N            |
| 7        | offsetangleofcrank            | 曲柄偏置角       | 度        | NUMBER(8,2)   | N            |
| 8        | crankgravityradius            | 曲柄重心半径     | m        | NUMBER(10,4)  | N            |
| 9        | singlecrankweight             | 单块曲柄重量     | kN       | NUMBER(8,2)   | N            |
| 10       | structuralunbalance           | 结构不平衡重     | kN       | NUMBER(8,2)   | N            |
| 11       | gearreducerratio              | 减速箱传动比     | %         | NUMBER(10,4)  | N            |
| 12       | gearreducerbeltpulleydiameter | 减速箱皮带轮直径 | m        | NUMBER(10,4)  | N            |
| 13       | balanceposition               | 平衡块位置       | m        | VARCHAR2(200) | N            |
| 14       | balanceweight                 | 平衡块重量       | kN       | VARCHAR2(200) | N            |
| 15       | prtf                          | 位置扭矩因数     |          | CLOB          | Y            |

### 1.3.25 tbl_rpc_motor 抽油机电机数据表

| **序号** | **代码**           | **名称**   | **单位** | **类型**      | **为空**     | **键** |
|----------|--------------------|------------|----------|---------------|--------------|--------|
| 1&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;      | id       | 记录编号   |          | NUMBER(10)    | N&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;   | 主键   |
| 2        | wellid             | 井编号     |          | NUMBER(10)    | N            | 外键   |
| 3        | manufacturer       | 电机厂家   |          | VARCHAR2(200) | N            |        |
| 4        | model              | 电机型号   |          | VARCHAR2(200) | N            |        |
| 5        | synchrospeed       | 同步转速   | r/min    | NUMBER(8,2)   | Y            |        |
| 6        | beltpulleydiameter | 皮带轮直径 | m        | NUMBER(10,4)  | Y            |        |
| 7        | performancecurver  | 特性曲线   |          | CLOB          |              |        |

### 1.3.26 tbl_rpc_inver_opt 抽油机电参反演参数优化表

| **序号** | **代码**                | **名称**             | **单位** | **类型**     | **为空**     | **键** |
|----------|-------------------------|----------------------|----------|--------------|--------------|--------|
| 1&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;  | id        | 记录编号        |          | NUMBER(10)   | N&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;| 主键   |
| 2        | wellid                  | 井编号               |          | NUMBER(10)   | Y            | 外键   |
| 3        | offsetangleofcrankps    | 曲柄位置开关偏置角   | 度        | NUMBER(8,2)  | Y            |        |
| 4        | surfacesystemefficiency | 地面效率             | 小数     | NUMBER(8,2)  | Y            |        |
| 5        | fs_leftpercent          | 功图左侧截取百分比   | %        | NUMBER(8,2)  | Y            |        |
| 6        | fs_rightpercent         | 功图又侧截取百分比   | %        | NUMBER(8,2)  | Y            |        |
| 7        | filtertime_watt         | 功率曲线滤波次数     |          | NUMBER(3)    | Y            |        |
| 8        | filtertime_i            | 电流曲线滤波次数     |          | NUMBER(3)    | Y            |        |
| 9        | filtertime_fsdiagram    | 地面功图滤波次数     |          | NUMBER(3)    | Y            |        |
| 10       | filtertime_rpm          | 转速曲线滤波次数     |          | NUMBER(3)    | Y            |        |
| 11       | filtertime_fsdiagram_l  | 地面功图左侧滤波次数 |          | NUMBER(3)    | Y            |        |
| 12       | filtertime_fsdiagram_r  | 地面功图右侧滤波次数 |          | NUMBER(3)    | Y            |        |
| 13       | wattangle               | 功率滤波角度         | 度        | NUMBER(8,2)  | Y            |        |

# 二、视图

## 2.1 视图概览

| **序号** | **名称**                      | **描述**               |
|----------|-------------------------------|------------------------|
| 1        | viw_wellinformation           | 井名信息视图           |
| 2        | viw_rpc_productiondata_latest | 抽油机生产数据实时视图 |
| 3        | viw_rpc_productiondata_hist   | 抽油机生产数据历史视图 |
| 4        | viw_commstatus                | 通信状态视图           |
| 5        | viw_rpc_diagram_latest        | 抽油机曲线数据实时视图 |
| 6        | viw_rpc_diagram_hist          | 抽油机曲线数据历史视图 |
| 7        | viw_rpc_discrete_latest       | 抽油机电参数据实时视图 |
| 8        | viw_rpc_discrete_hist         | 抽油机电参数据历史视图 |
| 9        | viw_rpc_comprehensive_latest  | 抽油机综合数据实时视图 |
| 10       | viw_rpc_comprehensive_hist    | 抽油机综合数据历史视图 |
| 11       | viw_rpc_diagramquery_latest   | 抽油机图形查询实时视图 |
| 12       | viw_rpc_diagramquery_hist     | 抽油机图形查询历史视图 |
| 13       | viw_rpc_total_day             | 抽油机日累计数据视图   |
| 14       | viw_rpc_calculatemain         | 抽油机计算结果管理视图 |

## 2.2 详述

### 2.2.1 viw_wellinformation 井名信息视图

| **序号** | **代码**                   | **名称**             | **类型**      | **单位** |
|----------|----------------------------|----------------------|---------------|----------|
| 1        | id                         | 记录编号             | NUMBER(10)    |          |
| 2        | orgname                    | 组织名称             | VARCHAR2(100) |          |
| 3        | orgid                      | 组织编号             | NUMBER(10)    |          |
| 4        | resname                    | 油气藏名称             | VARCHAR2(200) |          |
| 5        | wellname                   | 井名                 | VARCHAR2(200) |          |
| 6        | liftingtype                | 举升方式             | NUMBER(10)    |          |
| 7        | driveraddr                 | 设备地址             | VARCHAR2(200) |          |
| 8        | driverid                   | 设备编号             | VARCHAR2(200) |          |
| 9        | acqcycle_diagram           | 曲线采集周期         | NUMBER(10)    | min      |
| 10       | acqcyclesetstatus_diagram  | 曲线采集周期设置状态 | NUMBER(2)     |          |
| 11       | acqcycle_discrete          | 离散采集周期         | NUMBER(10)    | min      |
| 12       | acqcyclesetstatus_discrete | 离散采集周期设置状态 | NUMBER(2)     |          |
| 13       | savecycle_discrete         | 离散保存周期         | NUMBER(10)    | min      |
| 14       | runtimeefficiencysource    | 时率来源             | VARCHAR2(200) |          |
| 15       | videourl                   | 视频路径             | VARCHAR2(400) |          |
| 16       | liftingtypename            | 举升方式名称         | VARCHAR2(200) |          |
| 17       | drivercode                 | 驱动编码             | VARCHAR2(50)  |          |
| 18       | acquisitionunit            | 采集组编码           | VARCHAR2(50)  |          |
| 19       | sortnum                    | 排序编号             | NUMBER(10)    |          |

### 2.2.2 viw_rpc_productiondata_latest 抽油机生产数据实时视图

| **序号** | **代码**                   | **名称**       | **类型**      | **单位** |
|----------|----------------------------|----------------|---------------|----------|
| 1        | id                         | 记录编号       | NUMBER(10)    |          |
| 2        | wellname                   | 井名           | VARCHAR2(200) |          |
| 3        | wellid                     | 井编号         | NUMBER(10)    |          |
| 4        | liftingtype                | 举升类型       | NUMBER(10)    |          |
| 5        | acquisitiontime            | 采集时间       | DATE          |          |
| 6        | runtime                    | 运行时间       | NUMBER(8,2)   | h         |
| 7        | crudeoildensity            | 原油密度       | NUMBER(16,2)  | g/cm^3  |
| 8        | waterdensity               | 水密度         | NUMBER(16,2)  | g/cm^3  |
| 9        | naturalgasrelativedensity  | 天然气相对密度 | NUMBER(16,2)  |          |
| 10       | saturationpressure         | 饱和压力       | NUMBER(16,2)  | MPa      |
| 11       | reservoirdepth             | 油层中部深度   | NUMBER(16,2)  | m        |
| 12       | reservoirtemperature       | 油层中部温度   | NUMBER(16,2)  | ℃        |
| 13       | watercut_w                 | 重量含水率     | NUMBER(8,2)   | %        |
| 14       | watercut                   | 体积含水率     | NUMBER(8,2)   | %        |
| 15       | tubingpressure             | 油压           | NUMBER(8,2)   | MPa      |
| 16       | casingpressure             | 套压           | NUMBER(8,2)   | MPa      |
| 17       | backpressure               | 回压           | NUMBER(8,2)   | MPa      |
| 18       | wellheadfluidtemperature   | 井口油温       | NUMBER(8,2)   | ℃        |
| 19       | producingfluidlevel        | 动液面         | NUMBER(8,2)   | m        |
| 20       | pumpsettingdepth           | 泵挂           | NUMBER(8,2)   | m        |
| 21       | productiongasoilratio      | 生产气油比     | NUMBER(8,2)   | m^3/t   |
| 22       | pumpborediameter           | 泵径           | NUMBER(8,2)   | mm       |
| 23       | pumptype                   | 泵类型         | VARCHAR2(20)  |          |
| 24       | pumptypename               | 泵类型名称     | VARCHAR2(200) |          |
| 25       | pumpgrade                  | 泵级别         | NUMBER(1)     |          |
| 26       | plungerlength              | 柱塞长         | NUMBER(8,2)   | m        |
| 27       | barreltype                 | 泵筒类型       | VARCHAR2(20)  |          |
| 28       | barreltypename             | 泵筒类型名称   | VARCHAR2(200) |          |
| 29       | barrellength               | 泵筒长         | NUMBER(8,2)   | m        |
| 30       | barrelseries               | 泵级数         | NUMBER(8,2)   |          |
| 31       | rotordiameter              | 转子截面直径   | NUMBER(8,2)   | mm       |
| 32       | qpr                        | 转速           | NUMBER(8,2)   | r/min    |
| 33       | tubingstringinsidediameter | 油管内径       | NUMBER(8,2)   | mm       |
| 34       | casingstringinsidediameter | 套管内径       | NUMBER(8,2)   | mm       |
| 35       | rodstring                  | 杆数据         | VARCHAR2(200) |          |
| 36       | anchoringstate             | 锚定状态       | NUMBER(1)     |          |
| 37       | anchoringstatename         | 锚定状态名称   | VARCHAR2(200) |          |
| 38       | netgrossratio              | 净毛比         | NUMBER(8,2)   |          |
| 39       | manualintervention         | 人工干预代码   | NUMBER(4)     |          |
| 40       | sortnum                    | 井排序编号     | NUMBER(10)    |          |
| 41       | org_id                     | 组织编号       | NUMBER(10)    |          |

### 2.2.3 viw_rpc_productiondata_hist 抽油机生产数据历史视图

同viw_rpc_productiondata_latest

### 2.2.4 viw_commstatus 通信状态视图 

| **序号** | **代码**   | **名称** | **类型**      | **单位** |
|----------|------------|----------|---------------|----------|
| 1        | id         | 编号     | NUMBER(10)    |          |
| 2        | wellname   | 井名     | VARCHAR2(200) |          |
| 3        | commstatus | 通信状态 | NUMBER(1)     |          |

### 2.2.5 viw_rpc_diagram_latest 抽油机曲线数据实时视图

| **序号** | **代码**                      | **名称**             | **类型**      | **单位**    |
|----------|-------------------------------|----------------------|---------------|-------------|
| 1        | id                            | 记录编号             | NUMBER(10)    |             |
| 2        | wellname                      | 井名                 | VARCHAR2(200) |             |
| 3        | wellid                        | 井编号               | NUMBER(10)    |             |
| 4        | liftingtype                   | 举升类型             | NUMBER(10)    |             |
| 5        | acquisitiontime               | 采集时间             | DATE          |             |
| 6        | commstatus                    | 通信状态             | NUMBER(1)     |             |
| 7        | commstatusname                | 通信状态名称         | VARCHAR2      |             |
| 8        | commalarmlevel                | 通信报警级别         | NUMBER(3)     |             |
| 9        | workingconditioncode          | 工况代码             | NUMBER(4)     |             |
| 10       | workingconditionname          | 工况名称             | VARCHAR2(200) |             |
| 11       | optimizationsuggestion        | 优化建议             | VARCHAR2(200) |             |
| 12       | workingconditionrunalarmlevel | 工况报警级别         | NUMBER(3)     |             |
| 13       | theoreticalproduction         | 理论排量             | NUMBER(8,2)   | m^3/d         |
| 14       | liquidweightproduction        | 产液量               | NUMBER(8,2)   | t/d         |
| 15       | oilweightproduction           | 产油量               | NUMBER(8,2)   | t/d         |
| 16       | waterweightproduction         | 产水量               | NUMBER(8,2)   | t/d         |
| 17       | watercut_w                    | 含水率               | NUMBER(8,2)   | %           |
| 18       | liquidweightproductionlevel   | 产液级别             | VARCHAR2(50)  |             |
| 19       | productiongasoilratio         | 生产气油比           | NUMBER(8,2)   | m^3/t      |
| 20       | tubingpressure                | 油压                 | NUMBER(8,2)   | MPa         |
| 21       | casingpressure                | 套压                 | NUMBER(8,2)   | MPa         |
| 22       | wellheadfluidtemperature      | 井口油温             | NUMBER(8,2)   | ℃           |
| 23       | producingfluidlevel           | 动液面               | NUMBER(8,2)   | m           |
| 24       | pumpsettingdepth              | 泵挂                 | NUMBER(8,2)   | m           |
| 25       | submergence                   | 沉没度               | NUMBER(8,2)   | m           |
| 26       | pumpborediameter              | 泵径                 | NUMBER(8,2)   | mm          |
| 27       | crudeoildensity               | 原油密度             | NUMBER(16,2)  | g/cm^3     |
| 28       | netgrossratio                 | 净毛比               | NUMBER(8,2)   |             |
| 29       | availableplungerstrokeprod    | 柱塞有效冲程计算产量 | NUMBER(8,2)   | t/d         |
| 30       | pumpclearanceleakprod         | 泵间隙漏失量         | NUMBER(8,2)   | t/d         |
| 31       | tvleakweightproduction        | 游动凡尔漏失量       | NUMBER(8,2)   | t/d         |
| 32       | svleakweightproduction        | 固定凡尔漏失量       | NUMBER(8,2)   | t/d         |
| 33       | gasinfluenceprod              | 气影响               | NUMBER(8,2)   | t/d         |
| 34       | rodstring                     | 抽油杆数据           | VARCHAR2(200) |             |
| 35       | stroke                        | 冲程                 | NUMBER(8,2)   | m           |
| 36       | spm                           | 冲次                 | NUMBER(8,2)   | 次/min      |
| 37       | upperloadline                 | 理论上载荷           | NUMBER(8,2)   | kN          |
| 38       | upperloadlineofexact          | 真实理论上载荷       | NUMBER(8,2)   | kN          |
| 39       | lowerloadline                 | 理论下载荷           | NUMBER(8,2)   | kN          |
| 40       | fmax                          | 最大载荷             | NUMBER(8,2)   | kN          |
| 41       | fmin                          | 最小载荷             | NUMBER(8,2)   | kN          |
| 42       | motorinputactivepower         | 电机输入有功功率     | NUMBER(8,2)   | kW          |
| 43       | polishrodpower                | 光杆功率             | NUMBER(8,2)   | kW          |
| 44       | waterpower                    | 水功率               | NUMBER(8,2)   | kW          |
| 45       | systemefficiency              | 系统效率             | NUMBER(12,3)  | 小数        |
| 46       | systemefficiencylevel         | 系统效率级别         | VARCHAR2(50)  |             |
| 47       | surfacesystemefficiency       | 地面效率             | NUMBER(12,3)  | 小数        |
| 48       | surfacesystemefficiencylevel  | 地面效率级别         | VARCHAR2(50)  |             |
| 49       | welldownsystemefficiency      | 井下效率             | NUMBER(12,3)  | 小数        |
| 50       | welldownsystemefficiencylevel | 井下效率级别         | VARCHAR2(50)  |             |
| 51       | fsdiagramarea                 | 功图面积             | NUMBER(8,2)   |             |
| 52       | powerconsumptionperthm        | 吨液百米耗电量       | NUMBER(8,2)   | kW·h/100m·t |
| 53       | idegreebalance                | 电流平衡度           | NUMBER(8,2)   | %           |
| 54       | idegreebalancename            | 电流平衡状态         | VARCHAR2(200) |             |
| 55       | upstrokeimax                  | 上冲程最大电流       | NUMBER(8,2)   | A           |
| 56       | downstrokeimax                | 下冲程最大电流       | NUMBER(8,2)   | A           |
| 57       | idegreebalancealarmlevel      | 电流平衡报警级别     | NUMBER(3)     |             |
| 58       | wattdegreebalance             | 功率平衡度           | NUMBER(8,2)   | %           |
| 59       | wattdegreebalancename         | 功率平衡状态         | VARCHAR2(200) |             |
| 60       | upstrokewattmax               | 上冲程最大功率       | NUMBER(8,2)   | kW          |
| 61       | downstrokewattmax             | 下冲程最大功率       | NUMBER(8,2)   | kW          |
| 62       | wattdegreebalancealarmlevel   | 功率平衡报警级别     | NUMBER(3)     |             |
| 63       | pumpeff1                      | 冲程损失系数         | NUMBER(12,3)  | 小数        |
| 64       | pumpeff2                      | 充满系数             | NUMBER(12,3)  | 小数        |
| 65       | pumpeff3                      | 间隙漏失系数         | NUMBER(12,3)  | 小数        |
| 66       | pumpeff4                      | 液体收缩系数         | NUMBER(12,3)  | 小数        |
| 67       | pumpeff                       | 总泵效               | NUMBER(12,3)  | 小数        |
| 68       | rodflexlength                 | 抽油杆伸长量         | NUMBER(8,2)   | m           |
| 69       | tubingflexlength              | 油管伸缩值           | NUMBER(8,2)   | m           |
| 70       | inertialength                 | 惯性载荷增量         | NUMBER(8,2)   | m           |
| 71       | pumpintakep                   | 泵入口压力           | NUMBER(8,2)   | MPa         |
| 72       | pumpintaket                   | 泵入口温度           | NUMBER(8,2)   | ℃           |
| 73       | pumpintakegol                 | 泵入口就地气液比     | NUMBER(8,2)   | m^3/m^3   |
| 74       | pumpinletvisl                 | 泵入口粘度           | NUMBER(8,2)   | mPa·s       |
| 75       | pumpinletbo                   | 泵入口原油体积系数   | NUMBER(8,2)   | 小数        |
| 76       | pumpoutletp                   | 泵出口压力           | NUMBER(8,2)   | MPa         |
| 77       | pumpoutlett                   | 泵出口温度           | NUMBER(8,2)   | ℃           |
| 78       | pumpoutletgol                 | 泵出口就地气液比     | NUMBER(8,2)   | m^3/m^3   |
| 79       | pumpoutletvisl                | 泵出口粘度           | NUMBER(8,2)   | mPa·s       |
| 80       | pumpoutletbo                  | 泵出口原油体积系数   | NUMBER(8,2)   | 小数        |
| 81       | videourl                      | 视频路径             | VARCHAR2(400) |             |
| 82       | org_id                        | 组织标号             | NUMBER(10)    |             |
| 83       | org_code                      | 组织代码             | VARCHAR2(20)  |             |
| 84       | sortnum                       | 井排序编号           | NUMBER(10)    |             |

### 2.2.6 viw_rpc_diagram_hist 抽油机曲线数据历史视图

同viw_rpc_diagram_latest

### 2.2.7 viw_rpc_discrete_latest 抽油机电参数据实时视图

| **序号** | **代码**                    | **名称**         | **类型**       | **单位** |
|----------|-----------------------------|------------------|----------------|----------|
| 1        | id                          | 记录编号         | NUMBER(10)     |          |
| 2        | wellname                    | 井名             | VARCHAR2(200)  |          |
| 3        | liftingtype                 | 举升类型         | NUMBER(10)     |          |
| 4        | liftingtypename             | 举升类型名称     | VARCHAR2(200)  |          |
| 5        | wellid                      | 井编号           | NUMBER(10)     |          |
| 6        | commstatus                  | 通信状态         | NUMBER(1)      |          |
| 7        | commstatusname              | 通信状态名称     | VARCHAR2       |          |
| 8        | commalarmlevel              | 通信报警级别     | NUMBER(4)      |          |
| 9        | runstatus                   | 运行状态         | NUMBER(1)      |          |
| 10       | runstatusname               | 运行状态名称     | VARCHAR2       |          |
| 11       | runalarmlevel               | 运行状态报警级别 | NUMBER(3)      |          |
| 12       | commtime                    | 通信时间         | NUMBER(8,2)    | h        |
| 13       | commrange                   | 通信区间         | VARCHAR2(2000) |          |
| 14       | commtimeefficiency          | 通信时率         | NUMBER(10,4)   |          |
| 15       | commtimeefficiencylevel     | 通信时率级别     | VARCHAR2(50)   |          |
| 16       | runtime                     | 运行时间         | NUMBER(8,2)    | h        |
| 17       | runrange                    | 运行区间         | VARCHAR2(2000) |          |
| 18       | runtimeefficiency           | 生产时率         | NUMBER(10,4)   |          |
| 19       | runtimeefficiencylevel      | 生产时率等级     | VARCHAR2(50)   |          |
| 20       | acquisitiontime             | 采集时间         | DATE           |          |
| 21       | workingconditioncode_elec   | 工况代码         | NUMBER(4)      |          |
| 22       | workingconditionstring_elec | 工况累计字符串   | VARCHAR2(4000) |          |
| 23       | workingconditionname_elec   | 工况名称         | VARCHAR2(200)  |          |
| 24       | optimizationsuggestion_elec | 优化建议         | VARCHAR2(200)  |          |
| 25       | workingconditionalarmlevel  | 工况报警等级     | NUMBER(3)      |          |
| 26       | todaywattenergy             | 日有功功耗       | NUMBER(8,2)    | kW·h     |
| 27       | todaywattenergylevel        | 日耗电量等级     | VARCHAR2(50)   |          |
| 28       | todaypwattenergy            | 日正向有功功耗   | NUMBER(8,2)    | kW·h     |
| 29       | todaynwattenergy            | 日反向有功功耗   | NUMBER(8,2)    | kW·h     |
| 30       | todayvarenergy              | 日无功功耗       | NUMBER(8,2)    | kVar·h   |
| 31       | todaypvarenergy             | 日正向无功功耗   | NUMBER(8,2)    | kVar·h   |
| 32       | todaynvarenergy             | 日反向无功功耗   | NUMBER(8,2)    | kVar·h   |
| 33       | todayvaenergy               | 日视在功耗       | NUMBER(8,2)    | kVA·h    |
| 34       | ia                          | A相电流          | NUMBER(8,2)    | A        |
| 35       | ib                          | B相电流          | NUMBER(8,2)    | A        |
| 36       | ic                          | C相电流          | NUMBER(8,2)    | A        |
| 37       | iavg                        | 三相平均电流     | NUMBER(8,2)    | A        |
| 38       | istr                        | 电流字符串       | VARCHAR2       |          |
| 39       | iauplimit                   | A相电流上限      | NUMBER(8,2)    | A        |
| 40       | iadownlimit                 | A相电流下限      | NUMBER(8,2)    | A        |
| 41       | iazero                      | A相电流零值      | NUMBER(8,2)    | A        |
| 42       | ibuplimit                   | B相电流上限      | NUMBER(8,2)    | A        |
| 43       | ibdownlimit                 | B相电流下限      | NUMBER(8,2)    | A        |
| 44       | ibzero                      | B相电流零值      | NUMBER(8,2)    | A        |
| 45       | icuplimit                   | C相电流上限      | NUMBER(8,2)    | A        |
| 46       | icdownlimit                 | C相电流下限      | NUMBER(8,2)    | A        |
| 47       | iczero                      | C相电流零值      | NUMBER(8,2)    | A        |
| 48       | va                          | A相电压          | NUMBER(8,2)    | V        |
| 49       | vb                          | B相电压          | NUMBER(8,2)    | V        |
| 50       | vc                          | C相电压          | NUMBER(8,2)    | V        |
| 51       | vavg                        | 三相平均电压     | NUMBER(8,2)    | V        |
| 52       | vstr                        | 电压字符串       | VARCHAR2       |          |
| 53       | vauplimit                   | A相电压上限      | NUMBER(8,2)    | V        |
| 54       | vadownlimit                 | A相电压下限      | NUMBER(8,2)    | V        |
| 55       | vazero                      | A相电压零值      | NUMBER(8,2)    | V        |
| 56       | vbuplimit                   | B相电压上限      | NUMBER(8,2)    | V        |
| 57       | vbdownlimit                 | B相电压下限      | NUMBER(8,2)    | V        |
| 58       | vbzero                      | B相电压零值      | NUMBER(8,2)    | V        |
| 59       | vcuplimit                   | C相电压上限      | NUMBER(8,2)    | V        |
| 60       | vcdownlimit                 | C相电压下限      | NUMBER(8,2)    | V        |
| 61       | vczero                      | C相电压零值      | NUMBER(8,2)    | V        |
| 62       | totalwattenergy             | 累计有功功耗     | NUMBER(8,2)    | kW·h     |
| 63       | totalpwattenergy            | 累计正向有功功耗 | NUMBER(8,2)    | kW·h     |
| 64       | totalnwattenergy            | 累计反向有功功耗 | NUMBER(8,2)    | kW·h     |
| 65       | totalvarenergy              | 累计无功功耗     | NUMBER(8,2)    | kVar·h   |
| 66       | totalpvarenergy             | 累计正向无功功耗 | NUMBER(8,2)    | kVar·h   |
| 67       | totalnvarenergy             | 累计反向无功功耗 | NUMBER(8,2)    | kVar·h   |
| 68       | totalvaenergy               | 累计视在功耗     | NUMBER(8,2)    | kVA·h    |
| 69       | watta                       | A相有功功率      | NUMBER(8,2)    | kW       |
| 70       | wattb                       | B相有功功率      | NUMBER(8,2)    | kW       |
| 71       | wattc                       | C相有功功率      | NUMBER(8,2)    | kW       |
| 72       | wattsum                     | 三相总有功功率   | NUMBER(8,2)    | kW       |
| 73       | wattstr                     | 有功功率字符串   | VARCHAR2       |          |
| 74       | vara                        | A相无功功率      | NUMBER(8,2)    | kVar     |
| 75       | varb                        | B相无功功率      | NUMBER(8,2)    | kVar     |
| 76       | varc                        | C相无功功率      | NUMBER(8,2)    | kVar     |
| 77       | varsum                      | 三相总无功功率   | NUMBER(8,2)    | kVar     |
| 78       | varstr                      | 无功功率字符串   | VARCHAR2       |          |
| 79       | reversepower                | 反向功率         | NUMBER(8,2)    |          |
| 80       | pfa                         | A相功率因数      | NUMBER(8,2)    |          |
| 81       | pfb                         | B相功率因数      | NUMBER(8,2)    |          |
| 82       | pfc                         | C相功率因数      | NUMBER(8,2)    |          |
| 83       | pfsum                       | 三相综合功率因数 | NUMBER(8,2)    |          |
| 84       | pfstr                       | 功率因数字符串   | VARCHAR2       |          |
| 85       | frequencysetvalue           | 设置频率         | NUMBER(8,2)    | HZ       |
| 86       | frequencyrunvalue           | 运行频率         | NUMBER(8,2)    | HZ       |
| 87       | tubingpressure              | 油压             | NUMBER(8,2)    | MPa      |
| 88       | casingpressure              | 套压             | NUMBER(8,2)    | MPa      |
| 89       | backpressure                | 回压             | NUMBER(8,2)    | MPa      |
| 90       | wellheadfluidtemperature    | 井口油温         | NUMBER(8,2)    | ℃        |
| 91       | signal                      | 信号强度         | NUMBER(8,2)    |          |
| 92       | interval                    | 传输间隔         | NUMBER(10)     |          |
| 93       | devicever                   | 设备版本         | VARCHAR2(50)   |          |
| 94       | videourl                    | 视频路径         | VARCHAR2(400)  |          |
| 95       | sortnum                     | 井排序编号       | NUMBER(10)     |          |
| 96       | org_code                    | 组织代码         | VARCHAR2(20)   |          |
| 97       | org_id                      | 组织编号         | NUMBER(10)     |          |

### 2.2.8 viw_rpc_discrete_hist 抽油机电参数据历史视图

同 viw_rpc_discrete_latest

### 2.2.9 viw_rpc_comprehensive_latest 抽油机综合数据实时视图

| **序号** | **代码**                      | **名称**                     | **类型**       | **单位**    |
|----------|-------------------------------|------------------------------|----------------|-------------|
| 1        | id                            | 记录编号                         | NUMBER(10)     |             |
| 2        | wellname                      | 井名                         | VARCHAR2(200)  |             |
| 3        | wellid                        | 井编号                       | NUMBER(10)     |             |
| 4        | liftingtype                   | 举升类型                     | NUMBER(10)     |             |
| 5        | acquisitiontime               | 采集时间                     | DATE           |             |
| 6        | commstatus                    | 通信状态                     | NUMBER(2)      |             |
| 7        | commstatusname                | 通信状态名称                 | VARCHAR2       |             |
| 8        | commalarmlevel                | 通信报警级别                 | NUMBER(3)      |             |
| 9        | runstatus                     | 运行状态                     | NUMBER(1)      |             |
| 10       | runstatusname                 | 运行状态名称                 | VARCHAR2       |             |
| 11       | runalarmlevel                 | 运行状态报警级别             | NUMBER(3)      |             |
| 12       | commtime                      | 通信时间                     | NUMBER(8,2)    | h           |
| 13       | commrange                     | 通信区间                     | VARCHAR2(2000) |             |
| 14       | commtimeefficiency            | 通信时率                     | NUMBER(10,4)   |             |
| 15       | commtimeefficiencylevel       | 通信时率级别                 | VARCHAR2(50)   |             |
| 16       | runtime                       | 运行时间                     | NUMBER(8,2)    | h           |
| 17       | runrange                      | 运行区间                     | VARCHAR2(2000) |             |
| 18       | runtimeefficiency             | 生产时率                     | NUMBER(10,4)   |             |
| 19       | runtimeefficiencylevel        | 生产时率等级                 | VARCHAR2(50)   |             |
| 20       | workingconditioncode          | 工况代码                     | NUMBER(4)      |             |
| 21       | workingconditionname          | 工况名称                     | VARCHAR2(200)  |             |
| 22       | optimizationsuggestion        | 优化建议                     | VARCHAR2(200)  |             |
| 23       | workingconditionalarmlevel    | 工况报警级别                 | VARCHAR2       |             |
| 24       | workingconditioncode_e        | 电参工况代码                 | NUMBER(4)      |             |
| 25       | workingconditionstring_e      | 电参功率字符串               | VARCHAR2(4000) |             |
| 26       | workingconditionname_e        | 电参工况名称                 | VARCHAR2(200)  |             |
| 27       | optimizationsuggestion_e      | 电参工况优化建议             | VARCHAR2(200)  |             |
| 28       | workingconditionalarmlevel_e  | 电参工况报警级别             | NUMBER(3)      |             |
| 29       | theoreticalproduction         | 理论排量                     | NUMBER(8,2)    | m^3/d      |
| 30       | liquidweightproduction        | 产液量                       | NUMBER(8,2)    | t/d         |
| 31       | oilweightproduction           | 产油量                       | NUMBER(8,2)    | t/d         |
| 32       | waterweightproduction         | 产水量                       | NUMBER(8,2)    | t/d         |
| 33       | watercut                      | 含水率                       | NUMBER(8,2)    | %           |
| 34       | liquidweightproductionlevel   | 产液级别                     | VARCHAR2(50)   |             |
| 35       | productiongasoilratio         | 生产气油比                   | NUMBER(8,2)    | m^3/t      |
| 36       | tubingpressure                | 油压                         | NUMBER(8,2)    | MPa         |
| 37       | casingpressure                | 套压                         | NUMBER(8,2)    | MPa         |
| 38       | wellheadfluidtemperature      | 井口油温                     | NUMBER(8,2)    | ℃           |
| 39       | producingfluidlevel           | 动液面                       | NUMBER(8,2)    | m           |
| 40       | pumpsettingdepth              | 泵挂                         | NUMBER(8,2)    | m           |
| 41       | submergence                   | 沉没度                       | NUMBER(8,2)    | m           |
| 42       | pumpborediameter              | 泵径                         | NUMBER(8,2)    | mm          |
| 43       | crudeoildensity               | 原油密度                     | NUMBER(16,2)   | g/cm^3     |
| 44       | netgrossratio                 | 净毛比                       | NUMBER(8,2)    |             |
| 45       | availableplungerstrokeprod    | 柱塞有效冲程计算产量         | NUMBER(8,2)    | t/d         |
| 46       | pumpclearanceleakprod         | 泵间隙漏失量                 | NUMBER(8,2)    | t/d         |
| 47       | tvleakweightproduction        | 游动凡尔漏失量               | NUMBER(8,2)    | t/d         |
| 48       | svleakweightproduction        | 固定凡尔漏失量               | NUMBER(8,2)    | t/d         |
| 49       | gasinfluenceprod              | 气影响                       | NUMBER(8,2)    | t/d         |
| 50       | rodstring                     | 抽油杆数据                   | VARCHAR2(200)  |             |
| 51       | stroke                        | 冲程                         | NUMBER(8,2)    | m           |
| 52       | spm                           | 冲次                         | NUMBER(8,2)    | 次/min      |
| 53       | upperloadline                 | 理论上载荷                   | NUMBER(8,2)    | kN          |
| 54       | upperloadlineofexact          | 真实理论上载荷               | NUMBER(8,2)    | kN          |
| 55       | lowerloadline                 | 理论下载荷                   | NUMBER(8,2)    | kN          |
| 56       | fmax                          | 最大载荷                     | NUMBER(8,2)    | kN          |
| 57       | fmin                          | 最小载荷                     | NUMBER(8,2)    | kN          |
| 58       | fullnesscoefficient           | 功图充满系数                 | NUMBER(8,2)    | 小数        |
| 59       | motorinputactivepower         | 电机输入有功功率             | NUMBER(8,2)    | kW          |
| 60       | polishrodpower                | 光杆功率                     | NUMBER(8,2)    | kW          |
| 61       | waterpower                    | 水功率                       | NUMBER(8,2)    | kW          |
| 62       | systemefficiency              | 系统效率                     | NUMBER(12,3)   | 小数        |
| 63       | systemefficiencylevel         | 系统效率级别                 | VARCHAR2(50)   |             |
| 64       | surfacesystemefficiency       | 地面效率                     | NUMBER(12,3)   | 小数        |
| 65       | surfacesystemefficiencylevel  | 地面效率级别                 | VARCHAR2(50)   |             |
| 66       | welldownsystemefficiency      | 井下效率                     | NUMBER(12,3)   | 小数        |
| 67       | welldownsystemefficiencylevel | 井下效率级别                 | VARCHAR2(50)   |             |
| 68       | fsdiagramarea                 | 功图面积                     | NUMBER(8,2)    |             |
| 69       | powerconsumptionperthm        | 吨液百米耗电量               | NUMBER(8,2)    | kW·h/100m·t |
| 70       | idegreebalance                | 电流平衡度                   | NUMBER(8,2)    | %           |
| 71       | idegreebalancename            | 电流平衡状态                 | VARCHAR2(200)  |             |
| 72       | upstrokeimax                  | 上冲程最大电流               | NUMBER(8,2)    | A           |
| 73       | downstrokeimax                | 下冲程最大电流               | NUMBER(8,2)    | A           |
| 74       | iratio                        | 电流比                       | VARCHAR2       |             |
| 75       | idegreebalancealarmlevel      | 电流平衡报警级别             | NUMBER(4)      |             |
| 76       | wattdegreebalance             | 功率平衡度                   | NUMBER(8,2)    | %           |
| 77       | wattdegreebalancename         | 功率平衡状态                 | VARCHAR2(200)  |             |
| 78       | upstrokewattmax               | 上冲程最大功率               | NUMBER(8,2)    | kW          |
| 79       | downstrokewattmax             | 下冲程最大功率               | NUMBER(8,2)    | kW          |
| 80       | wattratio                     | 功率比                       | VARCHAR2       |             |
| 81       | wattdegreebalancealarmlevel   | 功率平衡报警级别             | NUMBER(4)      |             |
| 82       | pumpeff1                      | 冲程损失系数                 | NUMBER(8,2)    | 小数        |
| 83       | pumpeff2                      | 充满系数                     | NUMBER(8,2)    | 小数        |
| 84       | pumpeff3                      | 间隙漏失系数                 | NUMBER(8,2)    | 小数        |
| 85       | pumpeff4                      | 液体收缩系数                 | NUMBER(8,2)    | 小数        |
| 86       | pumpeff                       | 总泵效                       | NUMBER(8,2)    | 小数        |
| 87       | rodflexlength                 | 抽油杆伸长量                 | NUMBER(8,2)    | m           |
| 88       | tubingflexlength              | 油管伸缩值                   | NUMBER(8,2)    | m           |
| 89       | inertialength                 | 惯性载荷增量                 | NUMBER(8,2)    | m           |
| 90       | pumpintakep                   | 泵入口压力                   | NUMBER(8,2)    | MPa         |
| 91       | pumpintaket                   | 泵入口温度                   | NUMBER(8,2)    | ℃           |
| 92       | pumpintakegol                 | 泵入口就地气液比             | NUMBER(8,2)    | m^3/m^3   |
| 93       | pumpinletvisl                 | 泵入口粘度                   | NUMBER(8,2)    | mPa·s       |
| 94       | pumpinletbo                   | 泵入口原油体积系数           | NUMBER(8,2)    | 小数        |
| 95       | pumpoutletp                   | 泵出口压力                   | NUMBER(8,2)    | MPa         |
| 96       | pumpoutlett                   | 泵出口温度                   | NUMBER(8,2)    | ℃           |
| 97       | pumpoutletgol                 | 泵出口就地气液比             | NUMBER(8,2)    | m^3/m^3   |
| 98       | pumpoutletvisl                | 泵出口粘度                   | NUMBER(8,2)    | mPa·s       |
| 99       | pumpoutletbo                  | 泵出口原油体积系数           | NUMBER(8,2)    | 小数        |
| 100      | todaywattenergy               | 日有功功耗                   | NUMBER(8,2)    | kW·h        |
| 101      | todaywattenergylevel          | 日耗电量等级                 | VARCHAR2(50)   |             |
| 102      | todaypwattenergy              | 日正向有功功耗               | NUMBER(8,2)    | kW·h        |
| 103      | todaynwattenergy              | 日反向有功功耗               | NUMBER(8,2)    | kW·h        |
| 104      | todayvarenergy                | 日无功功耗                   | NUMBER(8,2)    | kVar·h      |
| 105      | todaypvarenergy               | 日正向无功功耗               | NUMBER(8,2)    | kVar·h      |
| 106      | todaynvarenergy               | 日反向无功功耗               | NUMBER(8,2)    | kVar·h      |
| 107      | todayvaenergy                 | 日视在功耗                   | NUMBER(8,2)    | kVA·h       |
| 108      | ia                            | A相电流                      | NUMBER(8,2)    | A           |
| 109      | ib                            | B相电流                      | NUMBER(8,2)    | A           |
| 110      | ic                            | C相电流                      | NUMBER(8,2)    | A           |
| 111      | iavg                          | 三相平均电流                 | NUMBER(8,2)    | A           |
| 112      | istr                          | 电流字符串                   | VARCHAR2       |             |
| 113      | iauplimit                     | A相电流上限                  | NUMBER(8,2)    | A           |
| 114      | iadownlimit                   | A相电流下限                  | NUMBER(8,2)    | A           |
| 115      | iazero                        | A相电流零值                  | NUMBER(8,2)    | A           |
| 116      | ibuplimit                     | B相电流上限                  | NUMBER(8,2)    | A           |
| 117      | ibdownlimit                   | B相电流下限                  | NUMBER(8,2)    | A           |
| 118      | ibzero                        | B相电流零值                  | NUMBER(8,2)    | A           |
| 119      | icuplimit                     | C相电流上限                  | NUMBER(8,2)    | A           |
| 120      | icdownlimit                   | C相电流下限                  | NUMBER(8,2)    | A           |
| 121      | iczero                        | C相电流零值                  | NUMBER(8,2)    | A           |
| 122      | va                            | A相电压                      | NUMBER(8,2)    | V           |
| 123      | vb                            | B相电压                      | NUMBER(8,2)    | V           |
| 124      | vc                            | C相电压                      | NUMBER(8,2)    | V           |
| 125      | vavg                          | 三相平均电压                 | NUMBER(8,2)    | V           |
| 126      | vstr                          | 电压字符串                   | VARCHAR2       |             |
| 127      | vauplimit                     | A相电压上限                  | NUMBER(8,2)    | V           |
| 128      | vadownlimit                   | A相电压下限                  | NUMBER(8,2)    | V           |
| 129      | vazero                        | A相电压零值                  | NUMBER(8,2)    | V           |
| 130      | vbuplimit                     | B相电压上限                  | NUMBER(8,2)    | V           |
| 131      | vbdownlimit                   | B相电压下限                  | NUMBER(8,2)    | V           |
| 132      | vbzero                        | B相电压零值                  | NUMBER(8,2)    | V           |
| 133      | vcuplimit                     | C相电压上限                  | NUMBER(8,2)    | V           |
| 134      | vcdownlimit                   | C相电压下限                  | NUMBER(8,2)    | V           |
| 135      | vczero                        | C相电压零值                  | NUMBER(8,2)    | V           |
| 136      | totalwattenergy               | 累计有功功耗                 | NUMBER(8,2)    | kW·h        |
| 137      | totalpwattenergy              | 累计正向有功功耗             | NUMBER(8,2)    | kW·h        |
| 138      | totalnwattenergy              | 累计反向有功功耗             | NUMBER(8,2)    | kW·h        |
| 139      | totalvarenergy                | 累计无功功耗                 | NUMBER(8,2)    | kVar·h      |
| 140      | totalpvarenergy               | 累计正向无功功耗             | NUMBER(8,2)    | kVar·h      |
| 141      | totalnvarenergy               | 累计反向无功功耗             | NUMBER(8,2)    | kVar·h      |
| 142      | totalvaenergy                 | 累计视在功耗                 | NUMBER(8,2)    | kVA·h       |
| 143      | watta                         | A相有功功率                  | NUMBER(8,2)    | kW          |
| 144      | wattb                         | B相有功功率                  | NUMBER(8,2)    | kW          |
| 145      | wattc                         | C相有功功率                  | NUMBER(8,2)    | kW          |
| 146      | wattsum                       | 三相总有功功率               | NUMBER(8,2)    | kW          |
| 147      | wattstr                       | 有功功率字符串               | VARCHAR2       |             |
| 148      | vara                          | A相无功功率                  | NUMBER(8,2)    | kVar        |
| 149      | varb                          | B相无功功率                  | NUMBER(8,2)    | kVar        |
| 150      | varc                          | C相无功功率                  | NUMBER(8,2)    | kVar        |
| 151      | varsum                        | 三相总无功功率               | NUMBER(8,2)    | kVar        |
| 152      | varstr                        | 无功功率字符串               | VARCHAR2       |             |
| 153      | reversepower                  | 反向功率                     | NUMBER(8,2)    |             |
| 154      | pfa                           | A相功率因数                  | NUMBER(8,2)    |             |
| 155      | pfb                           | B相功率因数                  | NUMBER(8,2)    |             |
| 156      | pfc                           | C相功率因数                  | NUMBER(8,2)    |             |
| 157      | pfsum                         | 三相综合功率因数             | NUMBER(8,2)    |             |
| 158      | pfstr                         | 功率因数字符串               | VARCHAR2       |             |
| 159      | frequencysetvalue             | 设置频率                     | NUMBER(8,2)    | HZ          |
| 160      | frequencyrunvalue             | 运行频率                     | NUMBER(8,2)    | HZ          |
| 161      | signal                        | 信号强度                     | NUMBER(8,2)    |             |
| 162      | interval                      | 传输间隔                     | NUMBER(10)     |             |
| 163      | devicever                     | 设备版本                     | VARCHAR2(50)   |             |
| 164      | balancecontrolmode            | 平衡远程调节远程触发控制     | NUMBER(10)     |             |
| 165      | balancecalculatemode          | 平衡计算方式                 | NUMBER(10)     |             |
| 166      | balanceawaytime               | 重心远离支点调节时间         | NUMBER(10)     | ms          |
| 167      | balanceclosetime              | 重心接近支点调节时间         | NUMBER(10)     | ms          |
| 168      | balanceawaytimeperbeat        | 重心远离支点每拍调节时间     | NUMBER(10)     | ms          |
| 169      | balanceclosetimeperbeat       | 重心接近支点每拍调节时间     | NUMBER(10)     | ms          |
| 170      | balancestrokecount            | 参与平衡度计算的冲程测量次数 | NUMBER(10)     |             |
| 171      | balanceoperationuplimit       | 平衡调节上限                 | NUMBER(10)     | %           |
| 172      | balanceoperationdownlimit     | 平衡调节下限                 | NUMBER(10)     | %           |
| 173      | balanceautocontrol            | 平衡远程自动调节             | NUMBER(1)      |             |
| 174      | spmautocontrol                | 冲次远程自动调节             | NUMBER(1)      |             |
| 175      | balancefrontlimit             | 平衡前限位                   | NUMBER(1)      |             |
| 176      | balanceafterlimit             | 平衡后限位                   | NUMBER(1)      |             |
| 177      | videourl                      | 视频路径                     | VARCHAR2(400)  |             |
| 178      | org_id                        | 组织编号                     | NUMBER(10)     |             |
| 179      | org_code                      | 组织代码                     | VARCHAR2(20)   |             |
| 180      | sortnum                       | 井排序编号                   | NUMBER(10)     |             |

### 2.2.10 viw_rpc_comprehensive_hist 抽油机综合数据历史视图

同 viw_rpc_comprehensive_latest

### 2.2.11 viw_rpc_diagramquery_latest 抽油机图形查询实时视图

| **序号** | **代码**                    | **名称**           | **类型**      | **单位** |
|----------|-----------------------------|--------------------|---------------|----------|
| 1        | id                          | 记录编号               | NUMBER(10)    |          |
| 2        | wellname                    | 井名               | VARCHAR2(200) |          |
| 3        | acquisitiontime             | 采集时间           | DATE          |          |
| 4        | stroke                      | 冲程               | NUMBER(8,2)   | m        |
| 5        | spm                         | 冲次               | NUMBER(8,2)   | 次/min   |
| 6        | fmax                        | 最大载荷           | NUMBER(8,2)   | kN       |
| 7        | fmin                        | 最小载荷           | NUMBER(8,2)   | kN       |
| 8        | position_curve              | 位移曲线           | CLOB          |          |
| 9        | load_curve                  | 载荷曲线           | CLOB          |          |
| 10       | power_curve                 | 功率曲线           | CLOB          |          |
| 11       | current_curve               | 电流曲线           | CLOB          |          |
| 12       | rpm_curve                   | 电机转速曲线       | CLOB          |          |
| 13       | rawpower_curve              | 过滤前功率曲线     | CLOB          |          |
| 14       | rawcurrent_curve            | 过滤前电流曲线     | CLOB          |          |
| 15       | rawrpm_curve                | 过滤前电机转速曲线 | CLOB          |          |
| 16       | upstrokeimax                | 上冲程最大电流     | VARCHAR2(200) | A        |
| 17       | downstrokeimax              | 下冲程最大电流     | NUMBER(8,2)   | A        |
| 18       | idegreebalance              | 电流平衡度         | NUMBER(8,2)   | %        |
| 19       | idegreebalancelevel         | 电流平衡级别       | NUMBER(8,2)   |          |
| 20       | idegreebalancealarmlevel    | 电流平衡报警级别   | VARCHAR2(200) |          |
| 21       | upstrokewattmax             | 上冲程最大功率     | NUMBER(8,2)   | kW       |
| 22       | downstrokewattmax           | 下冲程最大功率     | NUMBER(8,2)   | kW       |
| 23       | wattdegreebalance           | 功率平衡度         | NUMBER(8,2)   | %        |
| 24       | wattdegreebalancelevel      | 功率平衡级别       | NUMBER(8,2)   |          |
| 25       | wattdegreebalancealarmlevel | 功率平衡报警级别   | VARCHAR2(200) |          |
| 26       | datasource                  | 数据来源           | NUMBER(1)     |          |
| 27       | workingconditionname        | 工况名称           | VARCHAR2      |          |
| 28       | upperloadline               | 理论上载荷线       | NUMBER(8,2)   | kN       |
| 29       | lowerloadline               | 理论下载荷线       | NUMBER(8,2)   | kN       |
| 30       | liquidweightproduction      | 产液量             | NUMBER(8,2)   | t/d      |
| 31       | signal                      | 信号强度           | NUMBER(8,2)   |          |
| 32       | devicever                   | 设备版本           | VARCHAR2(50)  |          |
| 33       | interval                    | 传输间隔           | NUMBER(10)    |          |
| 34       | orgid                       | 组织编号           | NUMBER(10)    |          |
| 35       | sortnum                     | 排序编号           | NUMBER(10)    |          |

### 2.2.12 viw_rpc_diagramquery_hist 抽油机图形查询历史视图

同 viw_rpc_diagramquery_latest

### 2.2.13 viw_rpc_total_day 抽油机日累计数据视图

| **序号** | **代码**                      | **名称**           | **类型**       | **单位**    |
|----------|-------------------------------|--------------------|----------------|-------------|
| 1        | id                            | 记录编号               | NUMBER(10)     |             |
| 2        | wellname                      | 井名               | VARCHAR2(200)  |             |
| 3        | liftingtype                   | 举升类型           | NUMBER(10)     |             |
| 4        | liftingtypename               | 举升类型名称       | VARCHAR2(200)  |             |
| 5        | wellid                        | 井编号             | NUMBER(10)     |             |
| 6        | calculatedate                 | 日期               | DATE           |             |
| 7        | commstatus                    | 通信状态           |                |             |
| 8        | commstatusname                | 通信名称           |                |             |
| 9        | commalarmlevel                | 通信报警级别       |                |             |
| 10       | runstatus                     | 运行状态           | NUMBER(2)      |             |
| 11       | runstatusname                 | 运行状态名称       |                |             |
| 12       | runalarmlevel                 | 运行状态报警级别   |                |             |
| 13       | commtime                      | 通信时间           | NUMBER(8,2)    | h           |
| 14       | commrange                     | 通信区间           | VARCHAR2(4000) |             |
| 15       | commtimeefficiency            | 通信时率           | NUMBER(12,3)   |             |
| 16       | commtimeefficiencylevel       | 通信时率级别       | VARCHAR2(50)   |             |
| 17       | runtime                       | 运行时间           | NUMBER(8,2)    | h           |
| 18       | runrange                      | 运行区间           | VARCHAR2(4000) |             |
| 19       | runtimeefficiency             | 运行时率           | NUMBER(12,3)   |             |
| 20       | runtimeefficiencylevel        | 运行时率级别       | VARCHAR2(50)   |             |
| 21       | workingconditioncode          | 工况代码           | NUMBER(4)      |             |
| 22       | workingconditionname          | 工况名称           | VARCHAR2(200)  |             |
| 23       | workingconditionstring        | 工况累计字符串     | VARCHAR2(4000) |             |
| 24       | optimizationsuggestion        | 优化建议           | VARCHAR2(200)  |             |
| 25       | workingconditionalarmlevel    | 工况报警级别       | NUMBER(3)      |             |
| 26       | workingconditioncode_e        | 电参工况代码       | NUMBER(4)      |             |
| 27       | workingconditionname_e        | 电参工况名称       | VARCHAR2(200)  |             |
| 28       | workingconditionstring_e      | 累计电参工况字符串 | VARCHAR2(4000) |             |
| 29       | workingconditionalarmlevel_e  | 电参工况报警级别   | NUMBER(3)      |             |
| 30       | liquidweightproduction        | 产液量             | NUMBER(8,2)    | t/d         |
| 31       | liquidweightproductionlevel   | 产液量统计级别     | VARCHAR2(50)   |             |
| 32       | oilweightproduction           | 产油量             | NUMBER(8,2)    | t/d         |
| 33       | waterweightproduction         | 产水量             | NUMBER(8,2)    | t/d         |
| 34       | watercut                      | 含水率             | NUMBER(10,4)   | %           |
| 35       | productiongasoilratio         | 生产气油比         | NUMBER(8,2)    | m^3/t      |
| 36       | tubingpressure                | 油压               | NUMBER(8,2)    | MPa         |
| 37       | casingpressure                | 套压               | NUMBER(8,2)    | MPa         |
| 38       | wellheadfluidtemperature      | 井口油温           | NUMBER(8,2)    | ℃           |
| 39       | stroke                        | 冲程               | NUMBER(8,2)    | m           |
| 40       | strokemax                     | 冲程最大值         | NUMBER(8,2)    | m           |
| 41       | strokemin                     | 冲程最小值         | NUMBER(8,2)    | m           |
| 42       | strokestr                     | 冲程字符串         | VARCHAR2       |             |
| 43       | spm                           | 冲次               | NUMBER(8,2)    | 次/min      |
| 44       | spmmax                        | 冲次最大值         | NUMBER(8,2)    | 次/min      |
| 45       | spmmin                        | 冲次最小值         | NUMBER(8,2)    | 次/min      |
| 46       | spmstr                        | 冲次字符串         | VARCHAR2       |             |
| 47       | f                             | 载荷               | NUMBER(8,2)    | kN          |
| 48       | fmax                          | 载荷最大值         | NUMBER(8,2)    | kN          |
| 49       | fmin                          | 载荷最小值         | NUMBER(8,2)    | kN          |
| 50       | fstr                          | 载荷字符串         | VARCHAR2       |             |
| 51       | fullnesscoefficient           | 充满系数           | NUMBER(10,4)   | 小数        |
| 52       | pumpeff                       | 总泵效             | NUMBER(10,4)   | 小数        |
| 53       | pumpborediameter              | 泵径               | NUMBER(8,2)    | mm          |
| 54       | pumpsettingdepth              | 泵挂               | NUMBER(8,2)    | m           |
| 55       | producingfluidlevel           | 动液面             | NUMBER(8,2)    | m           |
| 56       | submergence                   | 沉没度             | NUMBER(8,2)    | m           |
| 57       | rpm                           | 转速               | NUMBER(8,2)    | r/min       |
| 58       | rpmmax                        | 转速最大值         | NUMBER(8,2)    | r/min       |
| 59       | rpmmin                        | 转速最小值         | NUMBER(8,2)    | r/min       |
| 60       | systemefficiency              | 系统效率           | NUMBER(10,4)   | 小数        |
| 61       | systemefficiencylevel         | 系统效率统计等级   | VARCHAR2(50)   |             |
| 62       | surfacesystemefficiency       | 地面效率           | NUMBER(10,4)   | 小数        |
| 63       | surfacesystemefficiencylevel  | 地面效率级别       | VARCHAR2(50)   |             |
| 64       | welldownsystemefficiency      | 井下效率           | NUMBER(10,4)   | 小数        |
| 65       | welldownsystemefficiencylevel | 井下效率级别       | VARCHAR2(50)   |             |
| 66       | powerconsumptionperthm        | 吨液百米耗电量     | NUMBER(8,2)    | kW·h/100m·t |
| 67       | todaywattenergy               | 日有功功耗         | NUMBER(8,2)    | kW·h        |
| 68       | todaywattenergylevel          | 日耗电量统计级别   | VARCHAR2(50)   |             |
| 69       | todaypwattenergy              | 日正向有功功耗     | NUMBER(8,2)    | kW·h        |
| 70       | todaynwattenergy              | 日反向有功功耗     | NUMBER(8,2)    | kW·h        |
| 71       | todayvarenergy                | 日无功功耗         | NUMBER(8,2)    | kVar·h      |
| 72       | todaypvarenergy               | 日正向无功功耗     | NUMBER(8,2)    | kVar·h      |
| 73       | todaynvarenergy               | 日反向无功功耗     | NUMBER(8,2)    | kVar·h      |
| 74       | todayvaenergy                 | 日视在功耗         | NUMBER(8,2)    | kVA·h       |
| 75       | idegreebalance                | 电流平衡度         | NUMBER(8,2)    | %           |
| 76       | idegreebalancemax             | 电流平衡度最大值   | NUMBER(8,2)    | %           |
| 77       | idegreebalancemin             | 电流平衡度最小值   | NUMBER(8,2)    | %           |
| 78       | idegreebalancestr             | 电流平衡度字符串   | VARCHAR2       |             |
| 79       | idegreebalancelevel           | 电流平衡统计级别   | VARCHAR2(200)  |             |
| 80       | idegreebalancealarmlevel      | 电流平衡报警级别   | NUMBER(3)      |             |
| 81       | wattdegreebalance             | 功率平衡度         | NUMBER(8,2)    | %           |
| 82       | wattdegreebalancemax          | 功率平衡度最大值   | NUMBER(8,2)    | %           |
| 83       | wattdegreebalancemin          | 功率平衡度最小值   | NUMBER(8,2)    | %           |
| 84       | wattdegreebalancestr          | 功率平衡度字符串   | VARCHAR2       |             |
| 85       | wattdegreebalancelevel        | 功率平衡统计级别   | VARCHAR2(200)  |             |
| 86       | wattdegreebalancealarmlevel   | 功率平衡报警级别   | NUMBER(3)      |             |
| 87       | deltaradius                   | 移动距离           | NUMBER(8,2)    | m           |
| 88       | ia                            | A相电流            | NUMBER(8,2)    | A           |
| 89       | iamax                         | A相电流最大值      | NUMBER(8,2)    | A           |
| 90       | iamin                         | A相电流最小值      | NUMBER(8,2)    | A           |
| 91       | iastr                         | A相电流字符串      | NUMBER(8,2)    |             |
| 92       | ib                            | B相电流            | NUMBER(8,2)    | A           |
| 93       | ibmax                         | B相电流最大值      | NUMBER(8,2)    | A           |
| 94       | ibmin                         | B相电流最小值      | NUMBER(8,2)    | A           |
| 95       | ibstr                         | B相电流字符串      | VARCHAR2       |             |
| 96       | ic                            | C相电流            | NUMBER(8,2)    | A           |
| 97       | icmax                         | C相电流最大值      | NUMBER(8,2)    | A           |
| 98       | icmin                         | C相电流最小值      | NUMBER(8,2)    | A           |
| 99       | icstr                         | C相电流字符串      | VARCHAR2       |             |
| 100      | va                            | A相电压            | NUMBER(8,2)    | V           |
| 101      | vamax                         | A相电压最大值      | NUMBER(8,2)    | V           |
| 102      | vamin                         | A相电压最小值      | NUMBER(8,2)    | V           |
| 103      | vastr                         | A相电压字符串      | VARCHAR2       |             |
| 104      | vb                            | B相电压            | NUMBER(8,2)    | V           |
| 105      | vbmax                         | B相电压最大值      | NUMBER(8,2)    | V           |
| 106      | vbmin                         | B相电压最小值      | NUMBER(8,2)    | V           |
| 107      | vbstr                         | B相电压字符串      | VARCHAR2       |             |
| 108      | vc                            | C相电压            | NUMBER(8,2)    | V           |
| 109      | vcmax                         | C相电压最大值      | NUMBER(8,2)    | V           |
| 110      | vcmin                         | C相电压最小值      | NUMBER(8,2)    | V           |
| 111      | vcstr                         | C相电压字符串      | VARCHAR2       |             |
| 112      | signal                        | 信号强度           | NUMBER(8,2)    |             |
| 113      | signalmax                     | 信号强度最大值     | NUMBER(8,2)    |             |
| 114      | signalmin                     | 信号强度最小值     | NUMBER(8,2)    |             |
| 115      | signalstr                     | 信号强度字符串     | VARCHAR2       |             |
| 116      | videourl                      | 视频路径           | VARCHAR2(400)  |             |
| 117      | sortnum                       | 井排序编号         | NUMBER(10)     |             |
| 118      | org_code                      | 组织代码           | VARCHAR2(20)   |             |
| 119      | org_id                        | 组织编号           | NUMBER(10)     |             |
| 120      | remark                        | 备注               | VARCHAR2       |             |

### 2.1.14 viw_rpc_calculatemain 抽油机计算结果管理视图

| **序号** | **代码**                   | **名称**       | **类型**      | **单位** |
|----------|----------------------------|----------------|---------------|----------|
| 1        | id                         | 记录编号           | NUMBER(10)    |          |
| 2        | wellname                   | 井名           | VARCHAR2(200) |          |
| 3        | liftingtype                | 举升方式       | NUMBER(10)    |          |
| 4        | acquisitiontime            | 采集时间       | DATE          |          |
| 5        | workingconditionname       | 工况名称       | VARCHAR2(200) |          |
| 6        | liquidproduction           | 产液量         | NUMBER(8,2)   | t/d      |
| 7        | oilproduction              | 产油量         | NUMBER(8,2)   | t/d      |
| 8        | crudeoildensity            | 原油密度       | NUMBER(16,2)  | g/cm^3  |
| 9        | waterdensity               | 水密度         | NUMBER(16,2)  | g/cm^3  |
| 10       | naturalgasrelativedensity  | 天然气相对密度 | NUMBER(16,2)  |          |
| 11       | saturationpressure         | 饱和压力       | NUMBER(16,2)  | MPa      |
| 12       | reservoirdepth             | 油层中部深度       | NUMBER(16,2)  | m        |
| 13       | reservoirtemperature       | 油层中部温度       | NUMBER(16,2)  | ℃        |
| 14       | tubingpressure             | 油压           | NUMBER(8,2)   | MPa      |
| 15       | casingpressure             | 套压           | NUMBER(8,2)   | MPa      |
| 16       | wellheadfluidtemperature   | 井口温油       | NUMBER(8,2)   | ℃        |
| 17       | watercut                   | 含水率         | NUMBER(8,2)   | %        |
| 18       | productiongasoilratio      | 生产气油比     | NUMBER(8,2)   | m^3/t   |
| 19       | producingfluidlevel        | 动液面         | NUMBER(8,2)   | m        |
| 20       | pumpsettingdepth           | 泵挂           | NUMBER(8,2)   | m        |
| 21       | pumpgrade                  | 泵级别         | NUMBER(1)     |          |
| 22       | pumpborediameter           | 泵径           | NUMBER(8,2)   | mm       |
| 23       | plungerlength              | 柱塞长         | NUMBER(8,2)   | m        |
| 24       | tubingstringinsidediameter | 油管内径       | NUMBER(8,2)   | mm       |
| 25       | casingstringinsidediameter | 套管内径       | NUMBER(8,2)   | mm       |
| 26       | rodstring                  | 杆数据         | VARCHAR2(200) |          |
| 27       | anchoringstatename         | 锚定状态       | VARCHAR2(200) |          |
| 28       | netgrossratio              | 净毛比         | NUMBER(8,2)   |          |
| 29       | resultstatus               | 计算结果       | NUMBER(2)     |          |
| 30       | orgid                      | 组织编号       | NUMBER(10)    |          |

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
