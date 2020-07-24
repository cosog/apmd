:link:[**用户手册**](.././README.md):link:  

# 《敏捷生产V7.3》数据库手册  

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
	 - [1.3.27 tbl_pcp_productiondata_latest 螺杆泵生产数据实时表](README.md#1327-tbl_pcp_productiondata_latest-螺杆泵生产数据实时表)
	 - [1.3.28 tbl_pcp_productiondata_hist 螺杆泵生产数据历史表](README.md#1328-tbl_pcp_productiondata_hist-螺杆泵生产数据历史表)
	 - [1.3.29 tbl_pcp_discrete_latest 螺杆泵离散数据实时表](README.md#1329-tbl_pcp_discrete_latest-螺杆泵离散数据实时表)
	 - [1.3.30 tbl_pcp_discrete_hist 螺杆泵离散数据历史表](README.md#1330-tbl_pcp_discrete_hist-螺杆泵离散数据历史表)
	 - [1.3.31 tbl_pcp_rpm_latest 螺杆泵曲线数据实时表](README.md#1331-tbl_pcp_rpm_latest-螺杆泵曲线数据实时表)
	 - [1.3.32 tbl_pcp_rpm_hist 螺杆泵曲线数据历史表](README.md#1332-tbl_pcp_rpm_hist-螺杆泵曲线数据历史表)
	 - [1.3.33 tbl_pcp_total_day 螺杆泵日累计数据表](README.md#1333-tbl_pcp_total_day-螺杆泵日累计数据表)
- [二、视图](README.md#二视图) 
   - [2.1 视图概览](README.md#21-视图概览)
   - [2.2 详述](README.md#22-详述)
     - [2.2.1 viw_wellinformation 井名信息视图](README.md#221-viw_wellinformation-井名信息视图)
	 - [2.2.2 viw_wellboretrajectory 井身轨迹视图](README.md#222-viw_wellboretrajectory-井身轨迹视图)
     - [2.2.3 viw_rpc_productiondata_latest 抽油机生产数据实时视图](README.md#223-viw_rpc_productiondata_latest-抽油机生产数据实时视图)  
     - [2.2.4 viw_rpc_productiondata_hist 抽油机生产数据历史视图](README.md#224-viw_rpc_productiondata_hist-抽油机生产数据历史视图)
     - [2.2.5 viw_commstatus 通信状态视图](README.md#225-viw_commstatus-通信状态视图)
     - [2.2.6 viw_rpc_diagram_latest 抽油机曲线数据实时视图](README.md#226-viw_rpc_diagram_latest-抽油机曲线数据实时视图)
     - [2.2.7 viw_rpc_diagram_hist 抽油机曲线数据历史视图](README.md#227-viw_rpc_diagram_hist-抽油机曲线数据历史视图)
     - [2.2.8 viw_rpc_discrete_latest 抽油机电参数据实时视图](README.md#228-viw_rpc_discrete_latest-抽油机电参数据实时视图)
     - [2.2.9 viw_rpc_discrete_hist 抽油机电参数据历史视图](README.md#229-viw_rpc_discrete_hist-抽油机电参数据历史视图)
     - [2.2.10 viw_rpc_comprehensive_latest 抽油机综合数据实时视图](README.md#2210-viw_rpc_comprehensive_latest-抽油机综合数据实时视图)
     - [2.2.11 viw_rpc_comprehensive_hist 抽油机综合数据历史视图](README.md#2211-viw_rpc_comprehensive_hist-抽油机综合数据历史视图)
     - [2.2.12 viw_rpc_diagramquery_latest 抽油机图形查询实时视图](README.md#2212-viw_rpc_diagramquery_latest-抽油机图形查询实时视图)
     - [2.2.13 viw_rpc_diagramquery_hist 抽油机图形查询历史视图](README.md#2213-viw_rpc_diagramquery_hist-抽油机图形查询历史视图)
     - [2.2.14 viw_rpc_total_day 抽油机日累计数据视图](README.md#2214-viw_rpc_total_day-抽油机日累计数据视图)
     - [2.1.15 viw_rpc_calculatemain 抽油机计算结果管理视图](README.md#2115-viw_rpc_calculatemain-抽油机计算结果管理视图)
	 - [2.1.16 viw_pcp_productiondata_latest 螺杆泵生产数据实时视图](README.md#2116-viw_pcp_productiondata_latest-螺杆泵生产数据实时视图)
	 - [2.1.17 viw_pcp_productiondata_hist 螺杆泵生产数据历史视图](README.md#2117-viw_pcp_productiondata_hist-螺杆泵生产数据历史视图)
	 - [2.1.18 viw_pcp_rpm_latest 螺杆泵曲线数据实时视图](README.md#2118-viw_pcp_rpm_latest-螺杆泵曲线数据实时视图)
	 - [2.1.19 viw_pcp_rpm_hist 螺杆泵曲线数据历史视图](README.md#2119-viw_pcp_rpm_hist-螺杆泵曲线数据历史视图)
	 - [2.1.20 viw_pcp_discrete_latest 螺杆泵离散数据实时视图](README.md#2120-viw_pcp_discrete_latest-螺杆泵离散数据实时视图)
	 - [2.1.21 viw_pcp_discrete_hist 螺杆泵离散数据历史视图](README.md#2121-viw_pcp_discrete_hist-螺杆泵离散数据历史视图)
	 - [2.1.22 viw_pcp_comprehensive_latest 螺杆泵综合数据实时视图](README.md#2122-viw_pcp_comprehensive_latest-螺杆泵综合数据实时视图)
	 - [2.1.23 viw_pcp_comprehensive_hist 螺杆泵综合数据历史视图](README.md#2123-viw_pcp_comprehensive_hist-螺杆泵综合数据历史视图)
	 - [2.1.24 viw_pcp_total_day 螺杆泵日累计数据视图](README.md#2124-viw_pcp_total_day-螺杆泵日累计数据视图)
- [三、存储过程](README.md#三存储过程)
- [四、触发器](README.md#四触发器)  

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
| 27       | tbl_pcp_productiondata_latest | 螺杆泵生产数据实时表     |
| 28       | tbl_pcp_productiondata_hist   | 螺杆泵生产数据历史表     |
| 29       | tbl_pcp_discrete_latest       | 螺杆泵离散数据实时表     |
| 30       | tbl_pcp_discrete_hist         | 螺杆泵离散数据历史表     |
| 31       | tbl_pcp_rpm_latest            | 螺杆泵曲线数据实时表     |
| 32       | tbl_pcp_rpm_hist              | 螺杆泵曲线数据历史表     |
| 33       | tbl_pcp_total_day             | 螺杆泵日累计数据表       |

## 1.2 逻辑结构

![逻辑结构](.././images/PNG/051.png?raw=true)

## 1.3 详述  

### 1.3.1 tbl_org 组织数据表

| **序号** | **代码**     | **名称**     | **类型**   | **单位**    | **为空**     | **键** |
|----------|--------------|--------------|-------------|-------------|--------------|--------|
| 1&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;  | org_id       | 单位序号     | NUMBER(10) |      | N&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; | 主键   |
| 2        | org_code     | 单位编码     | VARCHAR2(20)   |          | Y            |        |
| 3        | org_name     | 单位名称     | VARCHAR2(100)  |          | N            |        |
| 4        | org_memo     | 单位说明     | VARCHAR2(4000) |          | Y            |        |
| 5        | org_parent   | 父级单位编号 | NUMBER(10)     |          | N            |        |
| 6        | org_seq      | 单位排序     | NUMBER(10)     |          | Y            |        |
| 7        | org_flag     | 单位标志     | CHAR(1)        |          | Y            |        |
| 8        | org_realid   | 单位当前编号 | NUMBER(10)     |          | Y            |        |
| 9        | org_level    | 单位级别     | NUMBER(1)      |          | Y            |        |
| 10       | org_type     | 单位类型     | NUMBER(1)      |          | Y            |        |
| 11       | org_coordx   | 纬度         | NUMBER(10,6)   |          | Y            |        |
| 12       | org_coordy   | 经度         | NUMBER(10,6)   |          | Y            |        |
| 13       | show_level   | 地图显示级别 | NUMBER(2)      |          | Y            |        |

### 1.3.2 tbl_user 用户数据表

| **序号** | **代码**        | **名称**     | **类型**      | **单位** | **为空**     | **键** |
|----------|-----------------|--------------|---------------|----------|--------------|--------|
| 1&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;     | user_no         | 用户序号     | NUMBER(10) |         | N&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; | 主键   |
| 2        | user_id         | 用户账号     | VARCHAR2(20)  |          | N            |        |
| 3        | user_pwd        | 用户密码     | VARCHAR2(20)  |          | Y            |        |
| 4        | user_name       | 用户姓名     | VARCHAR2(40)  |          | N            |        |
| 5        | user_in_email   | 内部邮箱     | VARCHAR2(40)  |          | Y            |        |
| 6        | user_out_email  | 外部邮箱     | VARCHAR2(100) |          | Y            |        |
| 7        | user_phone      | 用户电话     | VARCHAR2(40)  |          | Y            |        |
| 8        | user_mobile     | 手机号       | VARCHAR2(40)  |          | Y            |        |
| 9        | user_address    | 地址         | VARCHAR2(200) |          | Y            |        |
| 10       | user_postcode   | 邮编         | CHAR(6)       |          | Y            |        |
| 11       | user_title      | 用户职称     | VARCHAR2(100) |          | Y            |        |
| 12       | user_type       | 用户类型     | NUMBER(10)    |          | Y            | 外键   |
| 13       | user_orgid      | 用户所属组织 | NUMBER(10)    |          | N            | 外键   |
| 14       | user_isleader   | 是否领导     | CHAR(1)       |          | Y            |        |
| 15       | user_regtime    | 用户注册时间 | DATE          |          | Y            |        |
| 16       | user_style      | 显示风格     | VARCHAR2(20)  |          | Y            |        |
| 17       | user_quicklogin | 是否快捷登录 | NUMBER(1)     |          | Y            |        |

### 1.3.3 tbl_role 角色数据表

| **序号** | **代码**     | **名称**   | **类型**       | **单位** | **为空**     | **键** |
|----------|--------------|------------|----------------|----------|--------------|--------|
| 1&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;        | role_id      | 角色序号   | NUMBER(10)    |      | N&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;            | 主键   |
| 2        | role_code    | 角色编码   | VARCHAR2(50)   |          | N            |        |
| 3        | role_name    | 角色名称   | VARCHAR2(40)   |          | N            |        |
| 4        | role_flag    | 控制权限   | NUMBER(10)     |          | Y            |        |
| 5        | remark       | 角色描述   | VARCHAR2(2000) |          | Y            |        |

### 1.3.4 tbl_module 模块数据表

| **序号** | **代码**     | **名称**     | **类型**      | **单位** | **为空**     | **键** |
|----------|--------------|--------------|---------------|----------|--------------|--------|
| 1&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;        | md_id        | 模块序号     | NUMBER(10)  |          | N&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;            | 主键   |
| 2        | md_parentid  | 父级模块序号 | NUMBER(10)    |          | N            |        |
| 3        | md_name      | 模块名称     | VARCHAR2(100) |          | N            |        |
| 4        | md_showname  | 模块简介     | VARCHAR2(100) |          | Y            |        |
| 5        | md_url       | 模块URL      | VARCHAR2(200) |          | Y            |        |
| 6        | md_code      | 模块编码     | VARCHAR2(200) |          | Y            |        |
| 7        | md_seq       | 模块排序     | NUMBER(20)    |          | Y            |        |
| 8        | md_level     | 模块级别     | NUMBER(10)    |          | Y            |        |
| 9        | md_flag      | 模块标志     | NUMBER(10)    |          | Y            |        |
| 10       | md_icon      | 模块图标     | VARCHAR2(100) |          | Y            |        |
| 11       | md_type      | 模块类型     | NUMBER(1)     |          | Y            |        |
| 12       | md_control   | 模块控制器   | VARCHAR2(100) |          | Y            |        |

### 1.3.5 tbl_module2role 模块角色关系表

| **序号** | **代码**     | **名称**   | **类型**     | **单位** | **为空**     | **键** |
|----------|--------------|------------|--------------|----------|--------------|--------|
| 1&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;        | rm_id        | 序号       | NUMBER(10)   |        | N&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;            | 主键   |
| 2        | rm_roleid    | 角色编号   | NUMBER(10)   |          | N            | 外键   |
| 3        | rm_moduleid  | 模块序号   | NUMBER(10)   |          | N            | 外键   |
| 4        | rm_matrix    | 权限矩阵   | VARCHAR2(8)  |          | N            |        |

### 1.3.6 tbl_dist_name 字典名称表

| **序号** | **代码**     | **名称**   | **类型**     | **单位** | **为空**     | **键** |
|----------|--------------|------------|--------------|----------|--------------|--------|
| 1&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;        | sysdataid    | 字典编码   | VARCHAR2(32)  |        | N&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;            | 主键   |
| 2        | tenantid     | 组织编号   | VARCHAR2(50) |          | Y            |        |
| 3        | cname        | 中文名称   | VARCHAR2(50) |          | Y            |        |
| 4        | ename        | 英文名称   | VARCHAR2(50) |          | Y            |        |
| 5        | sorts        | 排序       | NUMBER       |          | Y            |        |
| 6        | status       | 显示状态   | NUMBER       |          | Y            |        |
| 7        | creator      | 创建人     | VARCHAR2(50) |          | Y            |        |
| 8        | updateuser   | 修改人     | VARCHAR2(50) |          | Y            |        |
| 9        | createdate   | 创建时间   | DATE         |          | Y            |        |
| 10       | updatetime   | 修改时间   | DATE         |          | N            |        |

### 1.3.7 tbl_dist_item 字典数据项表

| **序号** | **代码**     | **名称**   | **类型**      | **单位** | **为空**     | **键** |
|----------|--------------|------------|---------------|----------|--------------|--------|
| 1&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;        | dataitemid   | 数据项编码 | VARCHAR2(32)   |        | N&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;            | 主键   |
| 2        | tenantid     | 组织编号   | VARCHAR2(50)  |          | Y            |        |
| 3        | sysdataid    | 字典编码   | VARCHAR2(50)  |          | Y            | 外键   |
| 4        | cname        | 中文名称   | VARCHAR2(50)  |          | Y            |        |
| 5        | ename        | 英文名称   | VARCHAR2(200) |          | Y            |        |
| 6        | datavalue    | 数据项值   | VARCHAR2(200) |          | Y            |        |
| 7        | sorts        | 排序       | NUMBER        |          | Y            |        |
| 8        | status       | 显示状态   | NUMBER        |          | Y            |        |
| 9        | creator      | 创建人     | VARCHAR2(50)  |          | Y            |        |
| 10       | updateuser   | 修改人     | VARCHAR2(50)  |          | Y            |        |
| 11       | createdate   | 创建时间   | DATE          |          | Y            |        |
| 12       | updatetime   | 修改时间   | DATE          |          | Y            |        |

### 1.3.8 tbl_code 代码表

| **序号** | **代码**     | **名称**   | **类型**      | **单位** | **为空**     | **键** |
|----------|--------------|------------|---------------|----------|--------------|--------|
| 1&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;        | id           | 记录编号   | NUMBER(10)   |          | N&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;            | 主键   |
| 2        | tablecode    | 数据表代码 | VARCHAR2(200) |          | Y            |        |
| 3        | itemcode     | 数据项代码 | VARCHAR2(200) |          | Y            |        |
| 4        | itemvalue    | 代码       | VARCHAR2(20)  |          | Y            |        |
| 5        | itemname     | 名称       | VARCHAR2(200) |          | Y            |        |
| 6        | remark       | 备注       | VARCHAR2(200) |          | Y            |        |
| 7        | state        | 状态       | NUMBER(10)    |          | Y            |        |

### 1.3.9 tbl_acq_group_conf 采控组名称表

| **序号** | **代码**     | **名称**   | **类型**       | **单位** | **为空**     | **键** |
|----------|--------------|------------|----------------|----------|--------------|--------|
| 1&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;        | id           | 记录编号   | NUMBER(10)    |        | N&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;            | 主键   |
| 2        | unit_code    | 单元代码   | VARCHAR2(50)   |          | N            |        |
| 3        | unit_name    | 单元名称   | VARCHAR2(50)   |          | Y            |        |
| 4        | remark       | 单元描述   | VARCHAR2(2000) |          | Y            |        |

### 1.3.10 tbl_acq_item_conf 采控项名称表

| **序号** | **代码**      | **名称**   | **类型**      | **单位** | **为空**     | **键** |
|----------|---------------|------------|---------------|----------|--------------|--------|
| 1&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;        | id            | 记录编号   | NUMBER(10)   |     | N&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;            | 主键   |
| 2        | parentid      | 父级编号   | NUMBER(10)    |          | Y            |        |
| 3        | itemname      | 采集项名称 | VARCHAR2(100) |          | Y            |        |
| 4        | itemcode      | 采集项代码 | VARCHAR2(100) |          | Y            |        |
| 5        | address       | 寄存器地址 | NUMBER(10)    |          | Y            |        |
| 6        | length        | 寄存器个数 | NUMBER(10)    |          | Y            |        |
| 7        | datatype      | 数据类型   | NUMBER(5)     |          | Y            |        |
| 8        | zoom          | 量程变换   | NUMBER(10,3)  |          | Y            |        |
| 9        | seq           | 排序编号   | NUMBER(10)    |          | Y            |        |
| 10       | operationtype | 操作类型   | NUMBER(2)     |          | Y            |        |

### 1.3.11 tbl_acq_item2group_conf 采控组项关系表

| **序号** | **代码**     | **名称**     | **类型**     | **单位** | **为空**     | **键** |
|----------|--------------|--------------|--------------|----------|--------------|--------|
| 1&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;        | id           | 记录编号     | NUMBER(10)  |    | N&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;            | 主键   |
| 2        | unitid       | 采集类型编号 | NUMBER(10)   |          | N            | 外键   |
| 3        | itemid       | 采集项编号   | NUMBER(10)   |          | N            | 外键   |
| 4        | matrix       | 阵列         | VARCHAR2(8)  |          | N            |        |

### 1.3.12 tbl_wellinformation 井名基本信息表

| **序号** | **代码**                   | **名称**             | **类型**      | **单位** | **为空**     | **键** |
|----------|----------------------------|----------------------|---------------|----------|--------------|--------|
| 1&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; | id                   | 记录编号 | NUMBER(10)    |     | N&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;| 主键   |
| 2        | orgid                      | 单位编号             | NUMBER(10)    |          | Y            | 外键   |
| 3        | resname                    | 油气藏名称           | VARCHAR2(200) |          | Y            |        |
| 4        | wellname                   | 井名                 | VARCHAR2(200) |          | N            |        |
| 5        | liftingtype                | 举升类型             | NUMBER(10)    |          | Y            |        |
| 6        | driveraddr                 | 设备地址             | VARCHAR2(200) |          | Y            |        |
| 7        | driverid                   | 设备编号             | VARCHAR2(200) |          | Y            |        |
| 8        | acqcycle_diagram           | 曲线采集间隔         | NUMBER(10)    | min      | Y            |        |
| 9        | acqcycle_discrete          | 离散读取间隔         | NUMBER(10)    | min      | Y            |        |
| 10       | savecycle_discrete         | 离散保存间隔         | NUMBER(10)    | min      | Y            |        |
| 11       | drivercode                 | 驱动编码             | VARCHAR2(50)  |          | Y            |        |
| 12       | unitcode                   | 采集单元编码         | VARCHAR2(50)  |          | Y            |        |
| 13       | runtimeefficiencysource    | 时率来源             | NUMBER(2)     |          | Y            |        |
| 14       | videourl                   | 视频url              | VARCHAR2(400) |          | Y            |        |
| 15       | sortnum                    | 排序编号             | NUMBER(10)    |          | Y            |        |
| 16       | acqcyclesetstatus_diagram  | 曲线采集间隔设置状态 | NUMBER(2)     |          | Y            |        |
| 17       | acqcyclesetstatus_discrete | 离散采集间隔设置状态 | NUMBER(2)     |          | Y            |        |

### 1.3.13 tbl_trajectory 井身轨迹表

| **序号** | **代码**        | **名称**   | **类型**     | **单位** | **为空**     | **键** |
|----------|-----------------|------------|--------------|----------|--------------|--------|
| 1        | id              | 记录编号   | NUMBER(10)   |          | N            | 主键   |
| 2        | wellid          | 井编号     | NUMBER(10)   |          | N            | 外键   |
| 3        | measuringdepth  | 测量深度   | CLOB         | m        | Y            |        |
| 4        | verticaldepth   | 垂直深度   | CLOB         | m        | Y            |        |
| 5        | deviationangle  | 井斜角     | CLOB         | 度       | Y            |        |
| 6        | azimuthangle    | 方位角     | CLOB         | 度       | Y            |        |
| 7        | x               | 直角坐标X  | CLOB         | m        | Y            |        |
| 8        | y               | 直角坐标Y  | CLOB         | m        | Y            |        |
| 9        | z               | 直角坐标Z  | CLOB         | m        | Y            |        |
| 10       | savetime        | 入库时间   | DATE         |          | Y            |        |
| 11       | resultstatus    | 计算标志   | NUMBER(4)    |          | Y            |        |


### 1.3.14 tbl_rpc_productiondata_latest 抽油机生产数据实时表

| **序号** | **代码**                   | **名称**        | **类型**      | **单位** | **为空**     | **键** |
|----------|----------------------------|-----------------|---------------|----------|--------------|--------|
| 1&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; | id              | 记录编号 | NUMBER(10)    |     | N&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;            | 主键   |
| 2        | wellid                     | 井编号          | NUMBER(10)    |         | N            | 外键   |  
| 3        | acquisitiontime            | 采集时间        | DATE          |         | Y            |        |  
| 4        | liftingtype                | 举升类型        | NUMBER(10)    |         | Y            |        |  
| 5        | displacementtype           | 驱替类型        | NUMBER(1)     |         | Y            |        |  
| 6        | runtime                    | 生产时间        | NUMBER(8,2)   | h       | Y            |        |  
| 7        | crudeoildensity            | 原油密度        | NUMBER(16,2)  | g/cm^3  | Y            |        |  
| 8        | waterdensity               | 水密度          | NUMBER(16,2)  | g/cm^3  | Y            |        |  
| 9        | naturalgasrelativedensity  | 天然气相对密度  | NUMBER(16,2)  |         | Y            |        |  
| 10       | saturationpressure         | 饱和压力        | NUMBER(16,2)  | MPa     | Y            |        |  
| 11       | reservoirdepth             | 油层中部深度    | NUMBER(16,2)  | m       | Y            |        |  
| 12       | reservoirtemperature       | 油层中部温度    | NUMBER(16,2)  | ℃       | Y            |        |  
| 13       | watercut                   | 体积含水率      | NUMBER(8,2)   | %       | Y            |        |  
| 14       | watercut_w                 | 重量含水率      | NUMBER(8,2)   | %       | Y            |        |  
| 15       | tubingpressure             | 油压            | NUMBER(8,2)   | MPa     | Y            |        |  
| 16       | casingpressure             | 套压            | NUMBER(8,2)   | MPa     | Y            |        |  
| 17       | backpressure               | 回压            | NUMBER(8,2)   | MPa     | Y            |        |  
| 18       | wellheadfluidtemperature   | 井口流温        | NUMBER(8,2)   | ℃       | Y            |        |  
| 19       | producingfluidlevel        | 动液面          | NUMBER(8,2)   | m       | Y            |        |  
| 20       | pumpsettingdepth           | 泵挂            | NUMBER(8,2)   | m       | Y            |        |  
| 21       | productiongasoilratio      | 生产气油比      | NUMBER(8,2)   | m^3/t   | Y            |        |  
| 22       | tubingstringinsidediameter | 油管内径        | NUMBER(8,2)   | mm      | Y            |        |  
| 23       | casingstringinsidediameter | 油层套管内径    | NUMBER(8,2)   | mm      | Y            |        |  
| 24       | rodstring                  | 抽油杆参数      | VARCHAR2(200) |         | Y            |        |  
| 25       | pumpgrade                  | 泵级别          | NUMBER(1)     |         | Y            |        |  
| 26       | pumpborediameter           | 泵径            | NUMBER(8,2)   | mm      | Y            |        |  
| 27       | plungerlength              | 柱塞长          | NUMBER(8,2)   | m       | Y            |        |  
| 28       | pumptype                   | 泵类型          | VARCHAR2(20)  |         | Y            |        |  
| 29       | barreltype                 | 泵筒类型        | VARCHAR2(20)  |         | Y            |        |  
| 30       | barrellength               | 泵筒长          | NUMBER(8,2)   | m       | Y            |        |  
| 31       | barrelseries               | 泵级数          | NUMBER(8,2)   |         | Y            |        |  
| 32       | rotordiameter              | 转子截面直径    | NUMBER(8,2)   | mm      | Y            |        |  
| 33       | qpr                        | 公称排量        | NUMBER(8,2)   |         | Y            |        |  
| 34       | manualintervention         | 人工干预        | NUMBER(4)     |         | Y            |        |  
| 35       | netgrossratio              | 净毛比          | NUMBER(8,2)   |         | Y            |        |  
| 36       | anchoringstate             | 锚定状态        | NUMBER(1)     |         | Y            |        |  
| 37       | remark                     | 备注            | VARCHAR2(200) |         | Y            |        |  

### 1.3.15 tbl_rpc_productiondata_hist 抽油机生产数据历史表

同tbl_rpc_productiondata_latest

### 1.3.16 tbl_rpc_discrete_latest 抽油机离散数据实时表

| **序号** | **代码**                  | **名称**                      | **类型**       | **单位** | **为空**     | **键** |
|----------|---------------------------|-------------------------------|----------------|----------|--------------|--------|
| 1&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;| id    | 记录编号     | NUMBER(10)       |      | N&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;  | 主键    |
| 2        | wellid                    | 井编号                        | NUMBER(10)     |         | N            | 外键   | 
| 3        | acquisitiontime           | 采集时间                      | DATE           |         | Y            |        | 
| 4        | commstatus                | 通信状态                      | NUMBER(2)      |         | Y            |        | 
| 5        | commtime                  | 在线时间                      | NUMBER(8,2)    | h       | Y            |        | 
| 6        | commtimeefficiency        | 在线时率                      | NUMBER(10,4)   |         | Y            |        | 
| 7        | commrange                 | 在线区间                      | VARCHAR2(2000) |         | Y            |        | 
| 8        | runstatus                 | 运行状态                      | NUMBER(2)      |         | Y            |        | 
| 9        | runtimeefficiency         | 运行时率                      | NUMBER(10,4)   |         | Y            |        | 
| 10       | runtime                   | 运行时间                      | NUMBER(8,2)    | h       | Y            |        | 
| 11       | runrange                  | 运行区间                      | VARCHAR2(2000) |         | Y            |        | 
| 12       | ia                        | A相电流                       | NUMBER(8,2)    | A       | Y            |        | 
| 13       | ib                        | B相电流                       | NUMBER(8,2)    | A       | Y            |        | 
| 14       | ic                        | C相电流                       | NUMBER(8,2)    | A       | Y            |        | 
| 15       | va                        | A相电压                       | NUMBER(8,2)    | V       | Y            |        | 
| 16       | vb                        | B相电压                       | NUMBER(8,2)    | V       | Y            |        | 
| 17       | vc                        | C相电压                       | NUMBER(8,2)    | V       | Y            |        | 
| 18       | totalwattenergy           | 累计有功功耗                  | NUMBER(10,2)   | kW·h    | Y            |        | 
| 19       | totalvarenergy            | 累计无功功耗                  | NUMBER(10,2)   | kVar·h  | Y            |        | 
| 20       | wattsum                   | 三相总有功功率                | NUMBER(8,2)    | kW      | Y            |        | 
| 21       | varsum                    | 三相总无功功率                | NUMBER(8,2)    | kVar    | Y            |        | 
| 22       | reversepower              | 反向功率                      | NUMBER(8,2)    |         | Y            |        | 
| 23       | pfsum                     | 三相综合功率因数              | NUMBER(8,2)    |         | Y            |        | 
| 24       | acqcycle_diagram          | 功图采集间隔                  | NUMBER(6)      | min     | Y            |        | 
| 25       | frequencysetvalue         | 变频设置频率                  | NUMBER(8,2)    | HZ      | Y            |        | 
| 26       | frequencyrunvalue         | 变频运行频率                  | NUMBER(8,2)    | HZ      | Y            |        | 
| 27       | tubingpressure            | 油压                          | NUMBER(8,2)    | MPa     | Y            |        | 
| 28       | casingpressure            | 套压                          | NUMBER(8,2)    | MPa     | Y            |        | 
| 29       | backpressure              | 回压                          | NUMBER(8,2)    | MPa     | Y            |        | 
| 30       | wellheadfluidtemperature  | 井口油温                      | NUMBER(8,2)    | ℃       | Y            |        | 
| 31       | totaywattenergy           | 日有功功耗                    | NUMBER(10,2)   | kW·h    | Y            |        | 
| 32       | workingconditioncode      | 电参工况代码                  | NUMBER(4)      |         | Y            |        | 
| 33       | iaalarm                   | A相电流报警项                 | VARCHAR2(20)   |         | Y            |        | 
| 34       | ibalarm                   | B相电流报警项                 | VARCHAR2(20)   |         | Y            |        | 
| 35       | icalarm                   | C相电流报警项                 | VARCHAR2(20)   |         | Y            |        | 
| 36       | vaalarm                   | A相电压报警项                 | VARCHAR2(20)   |         | Y            |        | 
| 37       | vbalarm                   | B相电压报警项                 | VARCHAR2(20)   |         | Y            |        | 
| 38       | vcalarm                   | C相电压报警项                 | VARCHAR2(20)   |         | Y            |        | 
| 39       | workingconditionstring    | 电参工况字符串                | VARCHAR2(4000) |         | Y            |        | 
| 40       | iauplimit                 | A相电流上限                   | NUMBER(10,2)   | A       | Y            |        | 
| 41       | iadownlimit               | A相电流下限                   | NUMBER(10,2)   | A       | Y            |        | 
| 42       | iazero                    | A相电流零值                   | NUMBER(8,2)    | A       | Y            |        | 
| 43       | ibuplimit                 | B相电流上限                   | NUMBER(10,2)   | A       | Y            |        | 
| 44       | ibdownlimit               | B相电流下限                   | NUMBER(10,2)   | A       | Y            |        | 
| 45       | ibzero                    | B相电流零值                   | NUMBER(8,2)    | A       | Y            |        | 
| 46       | icuplimit                 | C相电流上限                   | NUMBER(10,2)   | A       | Y            |        | 
| 47       | icdownlimit               | C相电流下限                   | NUMBER(10,2)   | A       | Y            |        | 
| 48       | iczero                    | C相电流零值                   | NUMBER(8,2)    | A       | Y            |        | 
| 49       | vauplimit                 | A相电压上限                   | NUMBER(10,2)   | V       | Y            |        | 
| 50       | vadownlimit               | A相电压下限                   | NUMBER(10,2)   | V       | Y            |        | 
| 51       | vazero                    | A相电压零值                   | NUMBER(8,2)    | V       | Y            |        | 
| 52       | vbuplimit                 | B相电压上限                   | NUMBER(10,2)   | V       | Y            |        | 
| 53       | vbdownlimit               | B相电压下限                   | NUMBER(10,2)   | V       | Y            |        | 
| 54       | vbzero                    | B相电压零值                   | NUMBER(8,2)    | V       | Y            |        | 
| 55       | vcuplimit                 | C相电压上限                   | NUMBER(10,2)   | V       | Y            |        | 
| 56       | vcdownlimit               | C相电压下限                   | NUMBER(10,2)   | V       | Y            |        | 
| 57       | vczero                    | C相电压零值                   | NUMBER(8,2)    | V       | Y            |        | 
| 58       | totalpwattenergy          | 累计正向有功功耗              | NUMBER(10,2)   | kW·h    | Y            |        | 
| 59       | totalnwattenergy          | 累计反向有功功耗              | NUMBER(10,2)   | kW·h    | Y            |        | 
| 60       | totalpvarenergy           | 累计正向无功功耗              | NUMBER(10,2)   | kVar·h  | Y            |        | 
| 61       | totalnvarenergy           | 累计反向无功功耗              | NUMBER(10,2)   | kVar·h  | Y            |        | 
| 62       | totalvaenergy             | 累计视在功耗                  | NUMBER(10,2)   | kVA·h   | Y            |        | 
| 63       | todaypwattenergy          | 日正向有功功耗                | NUMBER(10,2)   | kW·h    | Y            |        | 
| 64       | todaynwattenergy          | 日反向有功功耗                | NUMBER(10,2)   | kW·h    | Y            |        | 
| 65       | todayvarenergy            | 日无功功耗                    | NUMBER(10,2)   | kVar·h  | Y            |        | 
| 66       | todaypvarenergy           | 日正向无功功耗                | NUMBER(10,2)   | kVar·h  | Y            |        | 
| 67       | todaynvarenergy           | 日反向无功功耗                | NUMBER(10,2)   | kVar·h  | Y            |        | 
| 68       | todayvaenergy             | 日视在功耗                    | NUMBER(10,2)   | kVA·h   | Y            |        | 
| 69       | vasum                     | 视在功率                      | NUMBER(8,2)    | kVA     | Y            |        | 
| 70       | signal                    | 信号强度                      | NUMBER(8,2)    |         | Y            |        | 
| 71       | interval                  | 传输间隔                      | NUMBER(10)     | min     | Y            |        | 
| 72       | devicever                 | 设备版本信息                  | VARCHAR2(50)   |         | Y            |        | 
| 73       | vavg                      | 三相电压平均值                | NUMBER(8,2)    | V       | Y            |        | 
| 74       | iavg                      | 三相电流平均值                | NUMBER(8,2)    | A       | Y            |        | 
| 75       | watta                     | A相有功功率                   | NUMBER(8,2)    | kW      | Y            |        | 
| 76       | wattb                     | B相有功功率                   | NUMBER(8,2)    | kW      | Y            |        | 
| 77       | wattc                     | C相有功功率                   | NUMBER(8,2)    | kW      | Y            |        | 
| 78       | vara                      | A相无功功率                   | NUMBER(8,2)    | kVar    | Y            |        | 
| 79       | varb                      | B相无功功率                   | NUMBER(8,2)    | kVar    | Y            |        | 
| 80       | varc                      | C相无功功率                   | NUMBER(8,2)    | kVar    | Y            |        | 
| 81       | vaa                       | A相视在功率                   | NUMBER(8,2)    | kVA     | Y            |        | 
| 82       | vab                       | B相视在功率                   | NUMBER(8,2)    | kVA     | Y            |        | 
| 83       | vac                       | C相视在功率                   | NUMBER(8,2)    | kVA     | Y            |        | 
| 84       | pfa                       | A相功率因数                   | NUMBER(8,2)    |         | Y            |        | 
| 85       | pfb                       | B相功率因数                   | NUMBER(8,2)    |         | Y            |        | 
| 86       | pfc                       | C相功率因数                   | NUMBER(8,2)    |         | Y            |        | 
| 87       | balancecontrolmode        | 平衡远程调节远程触发控制      | NUMBER(10)     |         | Y            |        | 
| 88       | balancecalculatemode      | 平衡计算方式                  | NUMBER(10)     |         | Y            |        | 
| 89       | balanceawaytime           | 重心远离支点调节时间          | NUMBER(10)     | ms      | Y            |        | 
| 90       | balanceclosetime          | 重心接近支点调节时间          | NUMBER(10)     | ms      | Y            |        | 
| 91       | balancestrokecount        | 参与平衡度计算的冲程测量次数  | NUMBER(10)     |         | Y            |        | 
| 92       | balanceoperationuplimit   | 平衡调节上限                  | NUMBER(10)     | %       | Y            |        | 
| 93       | balanceoperationdownlimit | 平衡调节下限                  | NUMBER(10)     | %       | Y            |        | 
| 94       | balanceautocontrol        | 平衡远程自动调节              | NUMBER(1)      |         | Y            |        | 
| 95       | balancefrontlimit         | 平衡前限位                    | NUMBER(1)      |         | Y            |        | 
| 96       | balanceafterlimit         | 平衡后限位                    | NUMBER(1)      |         | Y            |        | 
| 97       | spmautocontrol            | 冲次远程自动调节              | NUMBER(1)      |         | Y            |        | 
| 98       | balanceawaytimeperbeat    | 重心远离支点每拍调节时间      | NUMBER(10)     | ms      | Y            |        | 
| 99       | balanceclosetimeperbeat   | 重心接近支点每拍调节时间      | NUMBER(10)     | ms      | Y            |        |
| 100      | acqcycle_discrete         | 离散数据采集间隔              | NUMBER(8,2)    | min     | Y            |        | 
| 101      | wattuplimit               | 有功功率上限                  | NUMBER(8,2)    | kW      | Y            |        | 
| 102      | wattdownlimit             | 有功功率下限                  | NUMBER(8,2)    | kW      | Y            |        | 
| 103      | iamax                     | A相电流最大值                 | NUMBER(8,2)    | A       | Y            |        | 
| 104      | ibmax                     | B相电流最大值                 | NUMBER(8,2)    | A       | Y            |        | 
| 105      | iamin                     | A相电流最小值                 | NUMBER(8,2)    | A       | Y            |        | 
| 106      | ibmin                     | B相电流最小值                 | NUMBER(8,2)    | A       | Y            |        | 
| 107      | icmax                     | C相电流最大值                 | NUMBER(8,2)    | A       | Y            |        | 
| 108      | icmin                     | C相电流最小值                 | NUMBER(8,2)    | A       | Y            |        |

### 1.3.17 tbl_rpc_discrete_hist 抽油机离散数据历史表

同tbl_rpc_discrete_latest

### 1.3.18 tbl_rpc_diagram_latest 抽油机曲线数据实时表

| **序号** | **代码**                     | **名称**              | **类型**      | **单位**    | **为空**     | **键** |
|----------|------------------------------|-----------------------|---------------|-------------|--------------|--------|
| 1&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;   | id    | 记录编号      | NUMBER(10)    |     | N&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;  | 主键   | 
| 2        | wellid                       | 井编号                | NUMBER(10)    |            | N            | 外键   | 
| 3        | acquisitiontime              | 采集时间              | DATE          |            | Y            |        | 
| 4        | stroke                       | 冲程                  | NUMBER(8,2)   | m          | Y            |        | 
| 5        | spm                          | 冲次                  | NUMBER(8,2)   | 次/min     | Y            |        | 
| 6        | fmax                         | 最大载荷              | NUMBER(8,2)   | kN         | Y            |        | 
| 7        | fmin                         | 最小载荷              | NUMBER(8,2)   | kN         | Y            |        | 
| 8        | position_curve               | 位移曲线              | CLOB          | m          | Y            |        | 
| 9        | angle_curve                  | 角度曲线              | CLOB          | °          | Y            |        | 
| 10       | load_curve                   | 载荷曲线              | CLOB          | kN         | Y            |        | 
| 11       | power_curve                  | 功率曲线              | CLOB          | kW         | Y            |        | 
| 12       | current_curve                | 电流曲线              | CLOB          | A          | Y            |        | 
| 13       | rpm_curve                    | 电机转速曲线          | CLOB          | r/min      | Y            |        | 
| 14       | rawpower_curve               | 功率原始曲线          | CLOB          | kW         | Y            |        | 
| 15       | rawcurrent_curve             | 电流原始曲线          | CLOB          | A          | Y            |        | 
| 16       | rawrpm_curve                 | 电机转速原始曲线      | CLOB          | r/min      | Y            |        | 
| 17       | upstrokeimax                 | 上冲程最大电流        | NUMBER(8,2)   | A          | Y            |        | 
| 18       | downstrokeimax               | 下冲程最大电流        | NUMBER(8,2)   | A          | Y            |        | 
| 19       | upstrokewattmax              | 上冲程最大功率        | NUMBER(8,2)   | kW         | Y            |        | 
| 20       | downstrokewattmax            | 下冲程最大功率        | NUMBER(8,2)   | kW         | Y            |        | 
| 21       | idegreebalance               | 电流平衡度            | NUMBER(8,2)   | %          | Y            |        | 
| 22       | wattdegreebalance            | 功率平衡度            | NUMBER(8,2)   | %          | Y            |        | 
| 23       | datasource                   | 功图来源              | NUMBER(1)     |            | Y            |        | 
| 24       | workingconditioncode         | 功图工况代码          | NUMBER(4)     |            | Y            |        | 
| 25       | fullnesscoefficient          | 功图充满系数          | NUMBER(12,3)  | 小数       | Y            |        | 
| 26       | upperloadline                | 理论上载荷            | NUMBER(8,2)   | kN         | Y            |        | 
| 27       | upperloadlineofexact         | 真实理论上载荷        | NUMBER(8,2)   | kN         | Y            |        | 
| 28       | lowerloadline                | 理论下载荷            | NUMBER(8,2)   | kN         | Y            |        | 
| 29       | pumpfsdiagram                | 泵功图                | CLOB          |            | Y            |        | 
| 30       | theoreticalproduction        | 理论排量              | NUMBER(8,2)   | m^3/d      | Y            |        | 
| 31       | liquidvolumetricproduction   | 产液量方              | NUMBER(8,2)   | m^3/d      | Y            |        | 
| 32       | oilvolumetricproduction      | 产油量方              | NUMBER(8,2)   | m^3/d      | Y            |        | 
| 33       | watervolumetricproduction    | 产水量方              | NUMBER(8,2)   | m^3/d      | Y            |        | 
| 34       | availableplungerstrokeprod_v | 柱塞有效冲程产量方    | NUMBER(8,2)   | m^3/d      | Y            |        | 
| 35       | pumpclearanceleakprod_v      | 泵间隙漏失量方        | NUMBER(8,2)   | m^3/d      | Y            |        | 
| 36       | tvleakvolumetricproduction   | 游动凡尔漏失量方      | NUMBER(8,2)   | m^3/d      | Y            |        | 
| 37       | svleakvolumetricproduction   | 固定凡尔漏失量方      | NUMBER(8,2)   | m^3/d      | Y            |        | 
| 38       | gasinfluenceprod_v           | 气影响方              | NUMBER(8,2)   | m^3/d      | Y            |        | 
| 39       | liquidweightproduction       | 产液量吨              | NUMBER(8,2)   | t/d        | Y            |        | 
| 40       | oilweightproduction          | 产油量吨              | NUMBER(8,2)   | t/d        | Y            |        | 
| 41       | waterweightproduction        | 产水量吨              | NUMBER(8,2)   | t/d        | Y            |        | 
| 42       | availableplungerstrokeprod_w | 柱塞有效冲程产量吨    | NUMBER(8,2)   | t/d        | Y            |        | 
| 43       | pumpclearanceleakprod_w      | 泵间隙漏失量吨        | NUMBER(8,2)   | t/d        | Y            |        | 
| 44       | tvleakweightproduction       | 游动凡尔漏失量吨      | NUMBER(8,2)   | t/d        | Y            |        | 
| 45       | svleakweightproduction       | 固定凡尔漏失量吨      | NUMBER(8,2)   | t/d        | Y            |        | 
| 46       | gasinfluenceprod_w           | 气影响吨              | NUMBER(8,2)   | t/d        | Y            |        | 
| 47       | motorinputactivepower        | 有功功率              | NUMBER(8,2)   | kW         | Y            |        | 
| 48       | polishrodpower               | 光杆功率              | NUMBER(8,2)   | kW         | Y            |        | 
| 49       | waterpower                   | 水功率                | NUMBER(8,2)   | kW         | Y            |        | 
| 50       | surfacesystemefficiency      | 地面系统效率          | NUMBER(12,3)  | 小数       | Y            |        | 
| 51       | welldownsystemefficiency     | 井下系统效率          | NUMBER(12,3)  | 小数       | Y            |        | 
| 52       | systemefficiency             | 系统效率              | NUMBER(12,3)  | 小数       | Y            |        | 
| 53       | powerconsumptionperthm       | 吨液百米耗电量        | NUMBER(8,2)   | kW·h/100m·t| Y            |        | 
| 54       | fsdiagramarea                | 功图面积              | NUMBER(8,2)   |            | Y            |        | 
| 55       | rodflexlength                | 抽油杆伸长量          | NUMBER(8,2)   | m          | Y            |        | 
| 56       | tubingflexlength             | 油管伸缩量            | NUMBER(8,2)   | m          | Y            |        | 
| 57       | inertialength                | 惯性增量              | NUMBER(8,2)   | m          | Y            |        | 
| 58       | pumpeff1                     | 冲程损失系数          | NUMBER(12,3)  | 小数       | Y            |        | 
| 59       | pumpeff2                     | 充满系数              | NUMBER(12,3)  | 小数       | Y            |        | 
| 60       | pumpeff3                     | 间隙漏失系数          | NUMBER(12,3)  | 小数       | Y            |        | 
| 61       | pumpeff4                     | 液体收缩系数          | NUMBER(12,3)  | 小数       | Y            |        | 
| 62       | pumpeff                      | 总泵效                | NUMBER(12,3)  | 小数       | Y            |        | 
| 63       | pumpintakep                  | 泵入口压力            | NUMBER(8,2)   | MPa        | Y            |        | 
| 64       | pumpintaket                  | 泵入口温度            | NUMBER(8,2)   | ℃          | Y            |        | 
| 65       | pumpintakegol                | 泵入口就地气液比      | NUMBER(8,2)   | m^3/m^3    | Y            |        | 
| 66       | pumpintakevisl               | 泵入口液体粘度        | NUMBER(8,2)   | mPa·s      | Y            |        | 
| 67       | pumpintakebo                 | 泵入口原油体积系数    | NUMBER(8,2)   | 小数       | Y            |        | 
| 68       | pumpoutletp                  | 泵出口压力            | NUMBER(8,2)   | MPa        | Y            |        | 
| 69       | pumpoutlett                  | 泵出口温度            | NUMBER(8,2)   | ℃          | Y            |        | 
| 70       | pumpoutletgol                | 泵出口就地气液比      | NUMBER(8,2)   | m^3/m^3    | Y            |        | 
| 71       | pumpoutletvisl               | 泵出口液体粘度        | NUMBER(8,2)   | mPa·s      | Y            |        | 
| 72       | pumpoutletbo                 | 泵出口原油体积系数    | NUMBER(8,2)   | 小数       | Y            |        | 
| 73       | rodstring                    | 抽油杆柱分析数据      | VARCHAR2(200) |            | Y            |        |
| 74       | savetime                     | 入库时间              | DATE          |            | Y            |        | 
| 75       | productiondataid             | 生产数据编号          | NUMBER(10)    |            | Y            |        | 
| 76       | resultstatus                 | 计算标志              | NUMBER(2)     |            | Y            |        | 
| 77       | inverresultstatus            | 功图反演状态          | NUMBER(2)     |            | Y            |        | 
| 78       | remark                       | 备注                  | VARCHAR2(200) |            | Y            |        | 
| 79       | position360_curve            | 360度均分位移曲线     | CLOB          | m          | Y            |        | 
| 80       | angle360_curve               | 360度均分角度曲线     | CLOB          | °          | Y            |        | 
| 81       | load360_curve                | 360度均分载荷曲线     | CLOB          | kN         | Y            |        | 
| 82       | signal                       | 信号强度              | NUMBER(8,2)   |            | Y            |        | 
| 83       | interval                     | 传输间隔              | NUMBER(10)    | min        | Y            |        | 
| 84       | devicever                    | 设备版本信息          | VARCHAR2(50)  |            | Y            |        | 
| 85       | discretedataid               | 离散数据编号          | NUMBER(10)    |            | Y            |        |
| 86       | plungerstroke                | 柱塞冲程              | NUMBER(8,2)   | m          | Y            |        |
| 87       | availableplungerstroke       | 柱塞有效冲程          | NUMBER(8,2)   | m          | Y            |        |
| 88       | ia_curve                     | A相电流曲线           | CLOB          |            | Y            |        | 
| 89       | ib_curve                     | B相电流曲线           | CLOB          |            | Y            |        |
| 90       | ic_curve                     | C相电流曲线           | CLOB          |            | Y            |        |
| 91       | deltaradius                  | 曲柄平衡移动距离      | NUMBER(8,2)   | cm         | Y            |        |
| 92       | crankangle                   | 曲柄转角曲线          | CLOB          |            | Y            |        |
| 93       | polishrodv                   | 速度曲线              | CLOB          |            | Y            |        |
| 94       | polishroda                   | 加速度曲线            | CLOB          |            | Y            |        |
| 95       | pr                           | 位置因数曲线          | CLOB          |            | Y            |        |
| 96       | tf                           | 扭矩因数曲线          | CLOB          |            | Y            |        |
| 97       | loadtorque                   | 载荷扭矩曲线          | CLOB          |            | Y            |        |
| 98       | cranktorque                  | 曲柄扭矩曲线          | CLOB          |            | Y            |        |
| 99       | currentbalancetorque         | 目前平衡块扭矩曲线    | CLOB          |            | Y            |        |
| 100      | currentnettorque             | 目前净扭矩曲线        | CLOB          |            | Y            |        |
| 101      | expectedbalancetorque        | 预期平衡块扭矩曲线    | CLOB          |            | Y            |        |
| 102      | expectednettorque            | 预期净扭矩曲线        | CLOB          |            | Y            |        |
| 103      | wellboreslice                | 井身切片曲线          | CLOB          |            | Y            |        |
| 104      | levelcorrectvalue            | 液面反演校正值        | NUMBER(8,2)   | MPa        | Y            |        |
| 105      | inverproducingfluidlevel     | 液面反演结果值        | NUMBER(8,2)   | m          | Y            |        |
| 106      | noliquidfullnesscoefficient  | 抽空充满系数          | NUMBER(10,4)  | 小数       | Y            |        |
| 107      | noliquidavailableplungerstroke  | 抽空柱塞有效冲程   | NUMBER(10,4)  | m          | Y            |        |

### 1.3.19 tbl_rpc_diagram_hist 抽油机曲线数据历史表

同tbl_rpc_diagram_latest

### 1.3.20 tbl_rpc_worktype 抽油机工况类型表

| **序号** | **代码**                    | **名称**   | **类型**      | **单位** | **为空**     | **键** |
|----------|-----------------------------|------------|---------------|----------|--------------|--------|
| 1&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;  | id         | 记录编号 | NUMBER(10)    |     | N&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;| 主键   |
| 2        | workingconditioncode        | 工况类型   | NUMBER(4)     |          | N            |        |
| 3        | workingconditionname        | 工况名称   | VARCHAR2(200) |          | N            |        |
| 4        | workingconditiondescription | 工况说明   | VARCHAR2(200) |          | Y            |        |
| 5        | workingconditiontemplate    | 工况模板   | BLOB          |          | Y            |        |
| 6        | optimizationsuggestion      | 优化建议   | VARCHAR2(200) |          | Y            |        |
| 7        | remark                      | 备注       | VARCHAR2(200) |          | Y            |        |

### 1.3.21 tbl_rpc_alarmtype_conf 抽油机报警类型表

| **序号** | **代码**             | **名称**   | **类型**      | **单位** | **为空**     | **键** |
|----------|----------------------|------------|---------------|----------|--------------|--------|
| 1&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; | id   | 记录编号   | NUMBER(10)  |     | N&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;            | 主键   |
| 2        | workingconditioncode | 工况类型   | NUMBER(10)    |          | N            |        |
| 3        | alarmtype            | 报警类型   | NUMBER(3)     |          | N            |        |
| 4        | alarmlevel           | 报警级别   | NUMBER(3)     |          | N            |        |
| 5        | alarmsign            | 报警标志   | NUMBER(1)     |          | Y            |        |
| 6        | remark               | 备注       | VARCHAR2(200) |          | Y            |        |

### 1.3.22 tbl_rpc_total_day 抽油机日累计数据表

| **序号** | **代码**                      | **名称**                          | **类型**       | **单位**    | **为空**     | **&nbsp;&nbsp;键&nbsp;&nbsp;** |
|----------|-------------------------------|-----------------------------------|----------------|-------------|--------------|--------|
| 1&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;    | id    | 记录编号                  | NUMBER(10)     |             | N&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; | 主键 |
| 2        | wellid                        | 井编号                            | NUMBER(10)     |            | Y            | 外键   | 
| 3        | calculatedate                 | 计算时间                          | DATE           |            | Y            |        | 
| 4        | commstatus                    | 通信状态                          | NUMBER(2)      |            | Y            |        | 
| 5        | runstatus                     | 运行状态                          | NUMBER(2)      |            | Y            |        | 
| 6        | commtime                      | 在线时间                          | NUMBER(8,2)    | h          | Y            |        | 
| 7        | commtimeefficiency            | 在线时率                          | NUMBER(12,3)   |            | Y            |        | 
| 8        | commrange                     | 在线区间                          | VARCHAR2(4000) |            | Y            |        | 
| 9        | runtime                       | 运行时间                          | NUMBER(8,2)    | h          | Y            |        | 
| 10       | runrange                      | 运行区间                          | VARCHAR2(4000) |            | Y            |        | 
| 11       | runtimeefficiency             | 运行时率                          | NUMBER(12,3)   | 小数       | Y            |        | 
| 12       | workingconditioncode          | 功图工况代码                      | NUMBER(4)      |            | Y            |        | 
| 13       | workingconditionstring        | 功图工况字符串                    | VARCHAR2(4000) |            | Y            |        | 
| 14       | workingconditioncode_e        | 电参工况代码                      | NUMBER(4)      |            | Y            |        | 
| 15       | workingconditionstring_e      | 电参工况字符串                    | VARCHAR2(4000) |            | Y            |        | 
| 16       | fullnesscoefficient           | 功图充满系数                      | NUMBER(10,4)   | 小数       | Y            |        | 
| 17       | fullnesscoefficientmax        | 功图充满系数最大值                | NUMBER(10,4)   | 小数       | Y            |        | 
| 18       | fullnesscoefficientmin        | 功图充满系数最小值                | NUMBER(10,4)   | 小数       | Y            |        | 
| 19       | stroke                        | 冲程                              | NUMBER(8,2)    | m          | Y            |        | 
| 20       | strokemax                     | 冲程最大值                        | NUMBER(8,2)    | m          | Y            |        | 
| 21       | strokemin                     | 冲程最小值                        | NUMBER(8,2)    | m          | Y            |        | 
| 22       | spm                           | 冲次                              | NUMBER(8,2)    | 次/min     | Y            |        | 
| 23       | spmmax                        | 冲次最大值                        | NUMBER(8,2)    | 次/min     | Y            |        | 
| 24       | spmmin                        | 冲次最小值                        | NUMBER(8,2)    | 次/min     | Y            |        | 
| 25       | liquidvolumetricproduction    | 产液量方                          | NUMBER(8,2)    | m^3/d      | Y            |        | 
| 26       | oilvolumetricproduction       | 产油量方                          | NUMBER(8,2)    | m^3/d      | Y            |        | 
| 27       | watervolumetricproduction     | 产水量方                          | NUMBER(8,2)    | m^3/d      | Y            |        | 
| 28       | liquidweightproduction        | 产液量吨                          | NUMBER(8,2)    | t/d        | Y            |        | 
| 29       | oilweightproduction           | 产油量吨                          | NUMBER(8,2)    | t/d        | Y            |        | 
| 30       | waterweightproduction         | 产水量吨                          | NUMBER(8,2)    | t/d        | Y            |        | 
| 31       | liquidvolumetricproductionmax | 产液量最大值方                    | NUMBER(8,2)    | m^3/d      | Y            |        | 
| 32       | liquidvolumetricproductionmin | 产液量最小值方                    | NUMBER(8,2)    | m^3/d      | Y            |        | 
| 33       | oilvolumetricproductionmax    | 产油量最大值方                    | NUMBER(8,2)    | m^3/d      | Y            |        | 
| 34       | oilvolumetricproductionmin    | 产油量最小值方                    | NUMBER(8,2)    | m^3/d      | Y            |        | 
| 35       | watervolumetricproductionmax  | 产水量最大值方                    | NUMBER(8,2)    | m^3/d      | Y            |        | 
| 36       | watervolumetricproductionmin  | 产水量最小值方                    | NUMBER(8,2)    | m^3/d      | Y            |        | 
| 37       | liquidweightproductionmax     | 产液量最大值吨                    | NUMBER(8,2)    | t/d        | Y            |        | 
| 38       | liquidweightproductionmin     | 产液量最小值吨                    | NUMBER(8,2)    | t/d        | Y            |        | 
| 39       | oilweightproductionmax        | 产油量最大值吨                    | NUMBER(8,2)    | t/d        | Y            |        | 
| 40       | oilweightproductionmin        | 产油量最小值吨                    | NUMBER(8,2)    | t/d        | Y            |        | 
| 41       | waterweightproductionmax      | 产水量最大值吨                    | NUMBER(8,2)    | t/d        | Y            |        | 
| 42       | waterweightproductionmin      | 产水量最小值吨                    | NUMBER(8,2)    | t/d        | Y            |        | 
| 43       | wattdegreebalance             | 功率平衡度                        | NUMBER(8,2)    | %          | Y            |        | 
| 44       | idegreebalance                | 电流平衡度                        | NUMBER(8,2)    | %          | Y            |        | 
| 45       | wattdegreebalancemax          | 功率平衡度最大值                  | NUMBER(8,2)    | %          | Y            |        | 
| 46       | wattdegreebalancemin          | 功率平衡度最小值                  | NUMBER(8,2)    | %          | Y            |        | 
| 47       | idegreebalancemax             | 电流平衡度最大值                  | NUMBER(8,2)    | %          | Y            |        | 
| 48       | idegreebalancemin             | 电流平衡度最小值                  | NUMBER(8,2)    | %          | Y            |        | 
| 49       | deltaradius                   | 曲柄平衡移动距离                  | NUMBER(8,2)    | m          | Y            |        | 
| 50       | deltaradiusmax                | 移动距离最大值                    | NUMBER(8,2)    | m          | Y            |        | 
| 51       | deltaradiusmin                | 移动距离最小值                    | NUMBER(8,2)    | m          | Y            |        | 
| 52       | watercut                      | 体积含水率                        | NUMBER(10,4)   | %          | Y            |        | 
| 53       | watercut_w                    | 重量含水率                        | NUMBER(10,4)   | %          | Y            |        | 
| 54       | watercutmax                   | 体积含水率最大值                  | NUMBER(10,4)   | %          | Y            |        | 
| 55       | watercutmin                   | 体积含水率最小值                  | NUMBER(10,4)   | %          | Y            |        | 
| 56       | watercutmax_w                 | 重量含水率最大值                  | NUMBER(10,4)   | %          | Y            |        | 
| 57       | watercutmin_w                 | 重量含水率最小值                  | NUMBER(10,4)   | %          | Y            |        | 
| 58       | tubingpressure                | 油压                              | NUMBER(8,2)    | MPa        | Y            |        | 
| 59       | tubingpressuremax             | 油压最大值                        | NUMBER(8,2)    | MPa        | Y            |        | 
| 60       | tubingpressuremin             | 油压最小值                        | NUMBER(8,2)    | MPa        | Y            |        | 
| 61       | casingpressure                | 套压                              | NUMBER(8,2)    | MPa        | Y            |        | 
| 62       | casingpressuremax             | 套压最大值                        | NUMBER(8,2)    | MPa        | Y            |        | 
| 63       | casingpressuremin             | 套压最小值                        | NUMBER(8,2)    | MPa        | Y            |        | 
| 64       | wellheadfluidtemperature      | 井口油温                          | NUMBER(8,2)    | ℃          | Y            |        | 
| 65       | wellheadfluidtemperaturemax   | 井口油温最大值                    | NUMBER(8,2)    | ℃          | Y            |        | 
| 66       | wellheadfluidtemperaturemin   | 井口油温最小值                    | NUMBER(8,2)    | ℃          | Y            |        | 
| 67       | productiongasoilratio         | 生产气油比                        | NUMBER(8,2)    | m^3/t      | Y            |        | 
| 68       | productiongasoilratiomax      | 生产气油比最大值                  | NUMBER(8,2)    | m^3/t      | Y            |        | 
| 69       | productiongasoilratiomin      | 生产气油比最小值                  | NUMBER(8,2)    | m^3/t      | Y            |        | 
| 70       | producingfluidlevel           | 动液面                            | NUMBER(8,2)    | m          | Y            |        | 
| 71       | producingfluidlevelmax        | 动液面最大值                      | NUMBER(8,2)    | m          | Y            |        | 
| 72       | producingfluidlevelmin        | 动液面最小值                      | NUMBER(8,2)    | m          | Y            |        | 
| 73       | pumpsettingdepth              | 泵挂                              | NUMBER(8,2)    | m          | Y            |        | 
| 74       | pumpsettingdepthmax           | 泵挂最大值                        | NUMBER(8,2)    | m          | Y            |        | 
| 75       | pumpsettingdepthmin           | 泵挂最小值                        | NUMBER(8,2)    | m          | Y            |        | 
| 76       | submergence                   | 沉没度                            | NUMBER(8,2)    | m          | Y            |        | 
| 77       | submergencemax                | 沉没度最大值                      | NUMBER(8,2)    | m          | Y            |        | 
| 78       | submergencemin                | 沉没度最小值                      | NUMBER(8,2)    | m          | Y            |        | 
| 79       | pumpborediameter              | 泵径                              | NUMBER(8,2)    | mm         | Y            |        | 
| 80       | pumpborediametermax           | 泵径最大值                        | NUMBER(8,2)    | mm         | Y            |        | 
| 81       | pumpborediametermin           | 泵径最小值                        | NUMBER(8,2)    | mm         | Y            |        | 
| 82       | systemefficiency              | 系统效率                          | NUMBER(10,4)   | 小数       | Y            |        | 
| 83       | systemefficiencymax           | 系统效率最大值                    | NUMBER(10,4)   | 小数       | Y            |        | 
| 84       | systemefficiencymin           | 系统效率最小值                    | NUMBER(10,4)   | 小数       | Y            |        | 
| 85       | surfacesystemefficiency       | 地面效率                          | NUMBER(10,4)   | 小数       | Y            |        | 
| 86       | surfacesystemefficiencymax    | 地面效率最大值                    | NUMBER(10,4)   | 小数       | Y            |        | 
| 87       | surfacesystemefficiencymin    | 地面效率最小值                    | NUMBER(10,4)   | 小数       | Y            |        | 
| 88       | welldownsystemefficiency      | 井下效率                          | NUMBER(10,4)   | 小数       | Y            |        | 
| 89       | welldownsystemefficiencymax   | 井下效率最大值                    | NUMBER(10,4)   | 小数       | Y            |        | 
| 90       | welldownsystemefficiencymin   | 井下效率最小值                    | NUMBER(10,4)   | 小数       | Y            |        | 
| 91       | powerconsumptionperthm        | 吨液百米耗电量                    | NUMBER(8,2)    | kW·h/100m·t| Y            |        | 
| 92       | powerconsumptionperthmmax     | 吨液百米耗电量最大值              | NUMBER(8,2)    | kW·h/100m·t| Y            |        | 
| 93       | powerconsumptionperthmmin     | 吨液百米耗电量最小值              | NUMBER(8,2)    | kW·h/100m·t| Y            |        | 
| 94       | pumpeff                       | 总泵效                            | NUMBER(10,4)   | 小数       | Y            |        | 
| 95       | pumpeffmax                    | 总泵效最大值                      | NUMBER(10,4)   | 小数       | Y            |        | 
| 96       | pumpeffmin                    | 总泵效最小值                      | NUMBER(10,4)   | 小数       | Y            |        | 
| 97       | ia                            | A相电流                           | NUMBER(8,2)    | A          | Y            |        | 
| 98       | iamax                         | A相电流最大值                     | NUMBER(8,2)    | A          | Y            |        | 
| 99       | iamin                         | A相电流最小值                     | NUMBER(8,2)    | A          | Y            |        | 
| 100      | ib                            | B相电流                           | NUMBER(8,2)    | A          | Y            |        | 
| 101      | ibmax                         | B相电流最大值                     | NUMBER(8,2)    | A          | Y            |        | 
| 102      | ibmin                         | B相电流最小值                     | NUMBER(8,2)    | A          | Y            |        | 
| 103      | ic                            | C相电流                           | NUMBER(8,2)    | A          | Y            |        | 
| 104      | icmax                         | C相电流最大值                     | NUMBER(8,2)    | A          | Y            |        | 
| 105      | icmin                         | C相电流最小值                     | NUMBER(8,2)    | A          | Y            |        | 
| 106      | va                            | A相电压                           | NUMBER(8,2)    | V          | Y            |        | 
| 107      | vamax                         | A相电压最大值                     | NUMBER(8,2)    | V          | Y            |        | 
| 108      | vamin                         | A相电压最小值                     | NUMBER(8,2)    | V          | Y            |        | 
| 109      | vb                            | B相电压                           | NUMBER(8,2)    | V          | Y            |        | 
| 110      | vbmax                         | B相电压最大值                     | NUMBER(8,2)    | V          | Y            |        | 
| 111      | vbmin                         | B相电压最小值                     | NUMBER(8,2)    | V          | Y            |        | 
| 112      | vc                            | C相电压                           | NUMBER(8,2)    | V          | Y            |        | 
| 113      | vcmax                         | C相电压最大值                     | NUMBER(8,2)    | V          | Y            |        | 
| 114      | vcmin                         | C相电压最小值                     | NUMBER(8,2)    | V          | Y            |        | 
| 115      | wattsum                       | 有功功率                          | NUMBER(8,2)    | kW         | Y            |        | 
| 116      | wattsummax                    | 有功功率最大值                    | NUMBER(8,2)    | kW         | Y            |        | 
| 117      | wattsummin                    | 有功功率最小值                    | NUMBER(8,2)    | kW         | Y            |        | 
| 118      | varsum                        | 无功功率                          | NUMBER(8,2)    | kVar       | Y            |        | 
| 119      | varsummax                     | 无功功率最大值                    | NUMBER(8,2)    | kVar       | Y            |        | 
| 120      | varsummin                     | 无功功率最小值                    | NUMBER(8,2)    | kVar       | Y            |        | 
| 121      | pfsum                         | 功率因数                          | NUMBER(8,2)    |            | Y            |        | 
| 122      | pfsummax                      | 功率因数最大值                    | NUMBER(8,2)    |            | Y            |        | 
| 123      | pfsummin                      | 功率因数最小值                    | NUMBER(8,2)    |            | Y            |        | 
| 124      | frequency                     | 运行频率                          | NUMBER(8,2)    | HZ         | Y            |        | 
| 125      | frequencymax                  | 运行频率最大值                    | NUMBER(8,2)    | HZ         | Y            |        | 
| 126      | frequencymin                  | 运行频率最小值                    | NUMBER(8,2)    | HZ         | Y            |        | 
| 127      | todaywattenergy               | 日有功功耗                        | NUMBER(10,2)   | kW·h       | Y            |        | 
| 128      | todaypwattenergy              | 日正向有功功耗                    | NUMBER(10,2)   | kW·h       | Y            |        | 
| 129      | todaynwattenergy              | 日反向有功功耗                    | NUMBER(10,2)   | kW·h       | Y            |        | 
| 130      | todayvarenergy                | 日无功功耗                        | NUMBER(10,2)   | kVar·h     | Y            |        | 
| 131      | todaypvarenergy               | 日正向无功功耗                    | NUMBER(10,2)   | kVar·h     | Y            |        | 
| 132      | todaynvarenergy               | 日反向无功功耗                    | NUMBER(10,2)   | kVar·h     | Y            |        | 
| 133      | todayvaenergy                 | 日视在功耗                        | NUMBER(10,2)   | kVA·h      | Y            |        | 
| 134      | totalwattenergy               | 累计有功功耗                      | NUMBER(10,2)   | kW·h       | Y            |        | 
| 135      | totalpwattenergy              | 累计正向有功功耗                  | NUMBER(10,2)   | kW·h       | Y            |        | 
| 136      | totalnwattenergy              | 累计反向有功功耗                  | NUMBER(10,2)   | kW·h       | Y            |        | 
| 137      | totalvarenergy                | 累计无功功耗                      | NUMBER(10,2)   | kVar·h     | Y            |        | 
| 138      | totalpvarenergy               | 累计正向无功功耗                  | NUMBER(10,2)   | kVar·h     | Y            |        | 
| 139      | totalnvarenergy               | 累计反向无功功耗                  | NUMBER(10,2)   | kVar·h     | Y            |        | 
| 140      | totalvaenergy                 | 累计视在功耗                      | NUMBER(10,2)   | kVA·h      | Y            |        | 
| 141      | rpm                           | 螺杆泵转速                        | NUMBER(8,2)    | r/min      | Y            |        | 
| 142      | rpmmax                        | 螺杆泵转速最大值                  | NUMBER(8,2)    | r/min      | Y            |        | 
| 143      | rpmmin                        | 螺杆泵转速最小值                  | NUMBER(8,2)    | r/min      | Y            |        | 
| 144      | extendeddays                  | 延用天数                          | NUMBER(5)      |            | Y            |        | 
| 145      | resultstatus                  | 计算标志                          | NUMBER(2)      |            | Y            |        | 
| 146      | signal                        | 信号强度                          | NUMBER(8,2)    |            | Y            |        | 
| 147      | signalmax                     | 信号强度最大值                    | NUMBER(8,2)    |            | Y            |        | 
| 148      | signalmin                     | 信号强度最小值                    | NUMBER(8,2)    |            | Y            |        | 
| 149      | f                             | 载荷                              | NUMBER(8,2)    | kN         | Y            |        | 
| 150      | fmax                          | 载荷最大值                        | NUMBER(8,2)    | kN         | Y            |        | 
| 151      | fmin                          | 载荷最小值                        | NUMBER(8,2)    | kN         | Y            |        | 
| 152      | savetime                      | 存储时间                          | DATE           |            | Y            |        |
| 153      | upperloadline                 | 理论上载荷线值                    | NUMBER(8,2)    | kN         | Y            |        |
| 154      | upperloadlinemax              | 理论上载荷线最大值                | NUMBER(8,2)    | kN         | Y            |        |
| 155      | upperloadlinemin              | 理论上载荷线最小值                | NUMBER(8,2)    | kN         | Y            |        |
| 156      | lowerloadline                 | 理论下载荷线值                    | NUMBER(8,2)    | kN         | Y            |        |
| 157      | lowerloadlinemax              | 理论下载荷线最大值                | NUMBER(8,2)    | kN         | Y            |        |
| 158      | lowerloadlinemin              | 理论下载荷线最小值                | NUMBER(8,2)    | kN         | Y            |        |
| 159      | upperloadlineofexact          | 考虑沉没压力的上载荷线值          | NUMBER(8,2)    | kN         | Y            |        |
| 160      | upperloadlineofexactmax       | 考虑沉没压力的上载荷线最大值      | NUMBER(8,2)    | kN         | Y            |        |
| 161      | upperloadlineofexactmin       | 考虑沉没压力的上载荷线最小值      | NUMBER(8,2)    | kN         | Y            |        |
| 162      | deltaloadline                 | 理论液柱载荷值                    | NUMBER(8,2)    | kN         | Y            |        |
| 163      | deltaloadlinemax              | 理论液柱载荷最大值                | NUMBER(8,2)    | kN         | Y            |        |
| 164      | deltaloadlinemin              | 理论液柱载荷最小值                | NUMBER(8,2)    | kN         | Y            |        |
| 165      | deltaloadlineofexact          | 考虑沉没压力的理论液柱载荷值      | NUMBER(8,2)    | kN         | Y            |        |
| 166      | deltaloadlineofexactmax       | 考虑沉没压力的理论液柱载荷最大值  | NUMBER(8,2)    | kN         | Y            |        |
| 167      | deltaloadlineofexactmin       | 考虑沉没压力的理论液柱载荷最小值  | NUMBER(8,2)    | kN         | Y            |        |
| 168      | fmax_avg                      | 最大载荷值                        | NUMBER(8,2)    | kN         | Y            |        |
| 169      | fmax_max                      | 最大载荷最大值                    | NUMBER(8,2)    | kN         | Y            |        |
| 170      | fmax_min                      | 最大载荷最小值                    | NUMBER(8,2)    | kN         | Y            |        |
| 171      | fmin_avg                      | 最小载荷值                        | NUMBER(8,2)    | kN         | Y            |        |
| 172      | fmin_max                      | 最小载荷最大值                    | NUMBER(8,2)    | kN         | Y            |        |
| 173      | fmin_min                      | 最小载荷最小值                    | NUMBER(8,2)    | kN         | Y            |        |
| 174      | deltaf                        | 载荷差                            | NUMBER(8,2)    | kN         | Y            |        |
| 175      | deltafmax                     | 载荷差最大值                      | NUMBER(8,2)    | kN         | Y            |        |
| 176      | deltafmin                     | 载荷差最小值                      | NUMBER(8,2)    | kN         | Y            |        |
| 177      | area                          | 功图面积                          | NUMBER(8,2)    | kN·m       | Y            |        |
| 178      | areamax                       | 功图面积最大值                    | NUMBER(8,2)    | kN·m       | Y            |        |
| 179      | areamin                       | 功图面积最小值                    | NUMBER(8,2)    | kN·m       | Y            |        |
| 180      | plungerstroke                 | 柱塞冲程                          | NUMBER(8,2)    | m          | Y            |        |
| 181      | plungerstrokemax              | 柱塞冲程最大值                    | NUMBER(8,2)    | m          | Y            |        |
| 182      | plungerstrokemin              | 柱塞冲程最小值                    | NUMBER(8,2)    | m          | Y            |        |
| 183      | availableplungerstroke        | 柱塞有效冲程                      | NUMBER(8,2)    | m          | Y            |        |
| 184      | availableplungerstrokemax     | 柱塞有效冲程最大值                | NUMBER(8,2)    | m          | Y            |        |
| 185      | availableplungerstrokemin     | 柱塞有效冲程最小值                | NUMBER(8,2)    | m          | Y            |        |
| 186      | theoreticalproduction         | 理论排量                          | NUMBER(8,2)    | m\^3/d     | Y            |        |
| 187      | theoreticalproductionmax      | 理论排量最大值                    | NUMBER(8,2)    | m\^3/d     | Y            |        |
| 188      | theoreticalproductionmin      | 理论排量最小值                    | NUMBER(8,2)    | m\^3/d     | Y            |        |
| 189      | availablestrokeprod_v         | 柱塞有效冲程计算产量方            | NUMBER(8,2)    | m\^3/d     | Y            |        |
| 190      | availablestrokeprod_v_max     | 柱塞有效冲程计算产量方最大值      | NUMBER(8,2)    | m\^3/d     | Y            |        |
| 191      | availablestrokeprod_v_min     | 柱塞有效冲程计算产量方最小值      | NUMBER(8,2)    | m\^3/d     | Y            |        |
| 192      | pumpclearanceleakprod_v       | 泵间隙漏失量方                    | NUMBER(8,2)    | m\^3/d     | Y            |        |
| 193      | pumpclearanceleakprod_v_max   | 泵间隙漏失量方最大值              | NUMBER(8,2)    | m\^3/d     | Y            |        |
| 194      | pumpclearanceleakprod_v_min   | 泵间隙漏失量方最小值              | NUMBER(8,2)    | m\^3/d     | Y            |        |
| 195      | tvleakvolumetricproduction    | 游动凡尔漏失量方                  | NUMBER(8,2)    | m\^3/d     | Y            |        |
| 196      | tvleakvolumetricproductionmax | 游动凡尔漏失量方最大值            | NUMBER(8,2)    | m\^3/d     | Y            |        |
| 197      | tvleakvolumetricproductionmin | 游动凡尔漏失量方最小值            | NUMBER(8,2)    | m\^3/d     | Y            |        |
| 198      | svleakvolumetricproduction    | 固定凡尔漏失量方                  | NUMBER(8,2)    | m\^3/d     | Y            |        |
| 199      | svleakvolumetricproductionmax | 固定凡尔漏失量方最大值            | NUMBER(8,2)    | m\^3/d     | Y            |        |
| 200      | svleakvolumetricproductionmin | 固定凡尔漏失量方最小值            | NUMBER(8,2)    | m\^3/d     | Y            |        |
| 201      | gasinfluenceprod_v            | 气影响方                          | NUMBER(8,2)    | m\^3/d     | Y            |        |
| 202      | gasinfluenceprod_v_max        | 气影响方最大值                    | NUMBER(8,2)    | m\^3/d     | Y            |        |
| 203      | gasinfluenceprod_v_min        | 气影响方最小值                    | NUMBER(8,2)    | m\^3/d     | Y            |        |
| 204      | availablestrokeprod_w         | 柱塞有效冲程计算产量吨            | NUMBER(8,2)    | t/d        | Y            |        |
| 205      | availablestrokeprod_w_max     | 柱塞有效冲程计算产量吨最大值      | NUMBER(8,2)    | t/d        | Y            |        |
| 206      | availablestrokeprod_w_min     | 柱塞有效冲程计算产量吨最小值      | NUMBER(8,2)    | t/d        | Y            |        |
| 207      | pumpclearanceleakprod_w       | 泵间隙漏失量吨                    | NUMBER(8,2)    | t/d        | Y            |        |
| 208      | pumpclearanceleakprod_w_max   | 泵间隙漏失量吨最大值              | NUMBER(8,2)    | t/d        | Y            |        |
| 209      | pumpclearanceleakprod_w_min   | 泵间隙漏失量吨最小值              | NUMBER(8,2)    | t/d        | Y            |        |
| 210      | tvleakweightproduction        | 游动凡尔漏失量吨                  | NUMBER(8,2)    | t/d        | Y            |        |
| 211      | tvleakweightproductionmax     | 游动凡尔漏失量吨最大值            | NUMBER(8,2)    | t/d        | Y            |        |
| 212      | tvleakweightproductionmin     | 游动凡尔漏失量吨最小值            | NUMBER(8,2)    | t/d        | Y            |        |
| 213      | svleakweightproduction        | 固定凡尔漏失量吨                  | NUMBER(8,2)    | t/d        | Y            |        |
| 214      | svleakweightproductionmax     | 固定凡尔漏失量吨最大值            | NUMBER(8,2)    | t/d        | Y            |        |
| 215      | svleakweightproductionmin     | 固定凡尔漏失量吨最小值            | NUMBER(8,2)    | t/d        | Y            |        |
| 216      | gasinfluenceprod_w            | 气影响吨                          | NUMBER(8,2)    | t/d        | Y            |        |
| 217      | gasinfluenceprod_w_max        | 气影响吨最大值                    | NUMBER(8,2)    | t/d        | Y            |        |
| 218      | gasinfluenceprod_w_min        | 气影响吨最小值                    | NUMBER(8,2)    | t/d        | Y            |        |
| 219      | pumpeff1                      | 冲程损失系数                      | NUMBER(10,4)   | 小数       | Y            |        |
| 220      | pumpeff1max                   | 冲程损失系数最大值                | NUMBER(10,4)   | 小数       | Y            |        |
| 221      | pumpeff1min                   | 冲程损失系数最小值                | NUMBER(10,4)   | 小数       | Y            |        |
| 222      | pumpeff2                      | 充满系数                          | NUMBER(10,4)   | 小数       | Y            |        |
| 223      | pumpeff2max                   | 充满系数最大值                    | NUMBER(10,4)   | 小数       | Y            |        |
| 224      | pumpeff2min                   | 充满系数最小值                    | NUMBER(10,4)   | 小数       | Y            |        |
| 225      | pumpeff3                      | 间隙漏失系数                      | NUMBER(10,4)   | 小数       | Y            |        |
| 226      | pumpeff3max                   | 间隙漏失系数最大值                | NUMBER(10,4)   | 小数       | Y            |        |
| 227      | pumpeff3min                   | 间隙漏失系数最小值                | NUMBER(10,4)   | 小数       | Y            |        |
| 228      | pumpeff4                      | 液体收缩系数                      | NUMBER(10,4)   | 小数       | Y            |        |
| 229      | pumpeff4max                   | 液体收缩系数最大值                | NUMBER(10,4)   | 小数       | Y            |        |
| 230      | pumpeff4min                   | 液体收缩系数最小值                | NUMBER(10,4)   | 小数       | Y            |        |
| 231      | rodflexlength                 | 抽油杆伸长量                      | NUMBER(8,2)    | m          | Y            |        |
| 232      | rodflexlengthmax              | 抽油杆伸长量最大值                | NUMBER(8,2)    | m          | Y            |        |
| 233      | rodflexlengthmin              | 抽油杆伸长量最小值                | NUMBER(8,2)    | m          | Y            |        |
| 234      | tubingflexlength              | 计算油管伸缩值                    | NUMBER(8,2)    | m          | Y            |        |
| 235      | tubingflexlengthmax           | 计算油管伸缩值最大值              | NUMBER(8,2)    | m          | Y            |        |
| 236      | tubingflexlengthmin           | 计算油管伸缩值最小值              | NUMBER(8,2)    | m          | Y            |        |
| 237      | inertialength                 | 惯性载荷增量                      | NUMBER(8,2)    | m          | Y            |        |
| 238      | inertialengthmax              | 惯性载荷增量最大值                | NUMBER(8,2)    | m          | Y            |        |
| 239      | inertialengthmin              | 惯性载荷增量最小值                | NUMBER(8,2)    | m          | Y            |        |
| 240      | pumpintakep                   | 泵入口压力                        | NUMBER(8,2)    | MPa        | Y            |        |
| 241      | pumpintakepmax                | 泵入口压力最大值                  | NUMBER(8,2)    | MPa        | Y            |        |
| 242      | pumpintakepmin                | 泵入口压力最小值                  | NUMBER(8,2)    | MPa        | Y            |        |
| 243      | pumpintaket                   | 泵入口温度                        | NUMBER(8,2)    | ℃          | Y            |        |
| 244      | pumpintaketmax                | 泵入口温度最大值                  | NUMBER(8,2)    | ℃          | Y            |        |
| 245      | pumpintaketmin                | 泵入口温度最小值                  | NUMBER(8,2)    | ℃          | Y            |        |
| 246      | pumpintakegol                 | 泵入口就地气液比                  | NUMBER(8,2)    | m^3/m^3    | Y            |        |
| 247      | pumpintakegolmax              | 泵入口就地气液比最大值            | NUMBER(8,2)    | m^3/m^3    | Y            |        |
| 248      | pumpintakegolmin              | 泵入口就地气液比最小值            | NUMBER(8,2)    | m^3/m^3    | Y            |        |
| 249      | pumpintakevisl                | 泵入口粘度                        | NUMBER(8,2)    | mPa·s      | Y            |        |
| 250      | pumpintakevislmax             | 泵入口粘度最大值                  | NUMBER(8,2)    | mPa·s      | Y            |        |
| 251      | pumpintakevislmin             | 泵入口粘度最小值                  | NUMBER(8,2)    | mPa·s      | Y            |        |
| 252      | pumpintakebo                  | 泵入口原油体积系数                | NUMBER(8,2)    |            | Y            |        |
| 253      | pumpintakebomax               | 泵入口原油体积系数最大值          | NUMBER(8,2)    |            | Y            |        |
| 254      | pumpintakebomin               | 泵入口原油体积系数最小值          | NUMBER(8,2)    |            | Y            |        |
| 255      | pumpoutletp                   | 泵出口压力                        | NUMBER(8,2)    | MPa        | Y            |        |
| 256      | pumpoutletpmax                | 泵出口压力最大值                  | NUMBER(8,2)    | MPa        | Y            |        |
| 257      | pumpoutletpmin                | 泵出口压力最小值                  | NUMBER(8,2)    | MPa        | Y            |        |
| 258      | pumpoutlett                   | 泵出口温度                        | NUMBER(8,2)    | ℃          | Y            |        |
| 259      | pumpoutlettmax                | 泵出口温度最大值                  | NUMBER(8,2)    | ℃          | Y            |        |
| 260      | pumpoutlettmin                | 泵出口温度最小值                  | NUMBER(8,2)    | ℃          | Y            |        |
| 261      | pumpoutletgol                 | 泵出口就地气液比                  | NUMBER(8,2)    | m^3/m^3    | Y            |        |
| 262      | pumpoutletgolmax              | 泵出口就地气液比最大值            | NUMBER(8,2)    | m^3/m^3    | Y            |        |
| 263      | pumpoutletgolmin              | 泵出口就地气液比最小值            | NUMBER(8,2)    | m^3/m^3    | Y            |        |
| 264      | pumpoutletvisl                | 泵出口粘度                        | NUMBER(8,2)    | mPa·s      | Y            |        |
| 265      | pumpoutletvislmax             | 泵出口粘度最大值                  | NUMBER(8,2)    | mPa·s      | Y            |        |
| 266      | pumpoutletvislmin             | 泵出口粘度最小值                  | NUMBER(8,2)    | mPa·s      | Y            |        |
| 267      | pumpoutletbo                  | 泵出口原油体积系数                | NUMBER(8,2)    |            | Y            |        |
| 268      | pumpoutletbomax               | 泵出口原油体积系数最大值          | NUMBER(8,2)    |            | Y            |        |
| 269      | pumpoutletbomin               | 泵出口原油体积系数最小值          | NUMBER(8,2)    |            | Y            |        |
| 270      | upstrokewattmax_avg           | 上冲程功率最大值                  | NUMBER(8,2)    | kW         | Y            |        |
| 271      | upstrokewattmax_max           | 上冲程功率最大值的最大值          | NUMBER(8,2)    | kW         | Y            |        |
| 272      | upstrokewattmax_min           | 上冲程功率最大值的最小值          | NUMBER(8,2)    | kW         | Y            |        |
| 273      | upstrokeimax_avg              | 上冲程电流最大值                  | NUMBER(8,2)    | A          | Y            |        |
| 274      | upstrokeimax_max              | 上冲程电流最大值的最大值          | NUMBER(8,2)    | A          | Y            |        |
| 275      | upstrokeimax_min              | 上冲程电流最大值的最小值          | NUMBER(8,2)    | A          | Y            |        |
| 276      | avgwatt                       | 平均有功功率                      | NUMBER(8,2)    | kW         | Y            |        |
| 277      | avgwattmax                    | 平均有功功率最大值                | NUMBER(8,2)    | kW         | Y            |        |
| 278      | avgwattmin                    | 平均有功功率最小值                | NUMBER(8,2)    | kW         | Y            |        |
| 279      | polishrodpower                | 光杆功率                          | NUMBER(8,2)    | kW         | Y            |        |
| 280      | polishrodpowermax             | 光杆功率最大值                    | NUMBER(8,2)    | kW         | Y            |        |
| 281      | polishrodpowermin             | 光杆功率最小值                    | NUMBER(8,2)    | kW         | Y            |        |
| 282      | waterpower                    | 水功率                            | NUMBER(8,2)    | kW         | Y            |        |
| 283      | waterpowermax                 | 水功率最大值                      | NUMBER(8,2)    | kW         | Y            |        |
| 284      | waterpowermin                 | 水功率最小值                      | NUMBER(8,2)    | kW         | Y            |        |
| 285      | vasum                         | 视在功率                          | NUMBER(8,2)    | kVA        | Y            |        |
| 286      | vasummax                      | 视在功率最大值                    | NUMBER(8,2)    | kVA        | Y            |        |
| 287      | vasummin                      | 视在功率最小值                    | NUMBER(8,2)    | kVA        | Y            |        |
| 288      | downstrokewattmax_avg         | 下冲程功率最大值                  | NUMBER(8,2)    | kW         | Y            |        |
| 289      | downstrokewattmax_max         | 下冲程功率最大值的最大值          | NUMBER(8,2)    | kW         | Y            |        |
| 290      | downstrokewattmax_min         | 下冲程功率最大值的最小值          | NUMBER(8,2)    | kW         | Y            |        |
| 291      | downstrokeimax_avg            | 下冲程电流最大值                  | NUMBER(8,2)    | A          | Y            |        |
| 292      | downstrokeimax_max            | 下冲程电流最大值的最大值          | NUMBER(8,2)    | A          | Y            |        |
| 293      | downstrokeimax_min            | 下冲程电流最大值的最小值          | NUMBER(8,2)    | A          | Y            |        |
| 294      | levelcorrectvalue             | 液面反演校正值                    | NUMBER(8,2)    | MPa        | Y            |        |
| 295      | levelcorrectvaluemax          | 液面反演校正最大值                | NUMBER(8,2)    | MPa        | Y            |        |
| 296      | levelcorrectvaluemin          | 液面反演校正最小值                | NUMBER(8,2)    | MPa        | Y            |        |
| 297      | noliquidfullnesscoefficient   | 抽空充满系数                      | NUMBER(10,4)   | 小数       | Y            |        |
| 298      | noliquidfullnesscoefficientmax| 抽空充满系数最大值                | NUMBER(10,4)   | 小数       | Y            |        |
| 299      | noliquidfullnesscoefficientmin| 抽空充满系数最小值                | NUMBER(10,4)   | 小数       | Y            |        |
| 300      | noliquidavailablestroke       | 抽空柱塞有效冲程                  | NUMBER(10,4)   | m          | Y            |        |
| 301      | noliquidavailablestrokemax    | 抽空柱塞有效冲程最大值            | NUMBER(10,4)   | m          | Y            |        |
| 302      | noliquidavailablestrokemin    | 抽空柱塞有效冲程最小值            | NUMBER(10,4)   | m          | Y            |        |

### 1.3.23 tbl_rpc_statistics_conf 抽油机统计配置表

| **序号** | **代码**     | **名称**   | **类型**     | **单位** | **为空**     | **键** |
|----------|--------------|------------|--------------|----------|--------------|--------|
| 1&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;        | id           | 记录编号   | NUMBER（10）|  | N&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;            | 主键   |
| 2        | s_level      | 级别       | VARCHAR2(50) |          | Y            |        |
| 3        | s_code       | 代码       | NUMBER(4)    |          | Y            |        |
| 4        | s_min        | 范围最小值 | NUMBER(11,3) |          | Y            |        |
| 5        | s_max        | 范围最大值 | NUMBER(11,3) |          | Y            |        |
| 6        | s_type       | 统计类型   | VARCHAR2(20) |          | Y            |        |

### 1.3.24 tbl_rpcinformation 抽油机设备表

| **序号** | **代码**                      | **名称**         | **类型**      | **单位** | **为空**     | **键** |
|----------|-------------------------------|------------------|---------------|----------|--------------|--------|
| 1&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;    | id               | 记录编号 | NUMBER(10)    |     | N&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; | 主键   |  
| 2        | wellid                        | 井编号           | NUMBER(10)    |          | Y            |        |
| 3        | manufacturer                  | 抽油机厂家       | VARCHAR2(200) |          | Y            |        |
| 4        | model                         | 抽油机型号       | VARCHAR2(200) |          | Y            |        |
| 5        | stroke                        | 冲程             | NUMBER(8,2)   | m        | Y            |        |
| 6        | crankrotationdirection        | 旋转方向         | VARCHAR2(200) |          | Y            |        |
| 7        | offsetangleofcrank            | 曲柄偏置角       | NUMBER(8,2)   | 度       | Y            |        |
| 8        | crankgravityradius            | 曲柄重心半径     | NUMBER(10,4)  | m        | Y            |        |
| 9        | singlecrankweight             | 单块曲柄重量     | NUMBER(8,2)   | kN       | Y            |        |
| 10       | structuralunbalance           | 结构不平衡重     | NUMBER(8,2)   | kN       | Y            |        |
| 11       | gearreducerratio              | 减速箱传动比     | NUMBER(10,4)  | %        | Y            |        |
| 12       | gearreducerbeltpulleydiameter | 减速箱皮带轮直径 | NUMBER(10,4)  | m        | Y            |        |
| 13       | balanceposition               | 平衡块位置       | VARCHAR2(200) | m        | Y            |        |
| 14       | balanceweight                 | 平衡块重量       | VARCHAR2(200) | kN       | Y            |        |
| 15       | prtf                          | 位置扭矩因数     | CLOB          |          | Y            |        |

### 1.3.25 tbl_rpc_motor 抽油机电机数据表

| **序号** | **代码**           | **名称**   | **类型**      | **单位** | **为空**     | **键** |
|----------|--------------------|------------|---------------|----------|--------------|--------|
| 1&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;      | id       | 记录编号   | NUMBER(10)      |     | N&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;   | 主键   |
| 2        | wellid             | 井编号     | NUMBER(10)    |          | N            | 外键   |
| 3        | manufacturer       | 电机厂家   | VARCHAR2(200) |          | N            |        |
| 4        | model              | 电机型号   | VARCHAR2(200) |          | N            |        |
| 5        | synchrospeed       | 同步转速   | NUMBER(8,2)   | r/min    | Y            |        |
| 6        | beltpulleydiameter | 皮带轮直径 | NUMBER(10,4)  | m        | Y            |        |
| 7        | performancecurver  | 特性曲线   | CLOB          |          | Y            |        |

### 1.3.26 tbl_rpc_inver_opt 抽油机电参反演参数优化表

| **序号** | **代码**                | **名称**             | **类型**     | **单位** | **为空**     | **键** |
|----------|-------------------------|----------------------|--------------|----------|--------------|--------|
| 1&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;  | id        | 记录编号        | NUMBER(10)   |    | N&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;| 主键   |
| 2        | wellid                  | 井编号               | NUMBER(10)   |          | Y            | 外键   |
| 3        | offsetangleofcrankps    | 曲柄位置开关偏置角   | NUMBER(8,2)  | 度       | Y            |        |
| 4        | surfacesystemefficiency | 地面效率             | NUMBER(8,2)  | 小数     | Y            |        |
| 5        | fs_leftpercent          | 功图左侧截取百分比   | NUMBER(8,2)  | %        | Y            |        |
| 6        | fs_rightpercent         | 功图右侧截取百分比   | NUMBER(8,2)  | %        | Y            |        |
| 7        | filtertime_watt         | 功率曲线滤波次数     | NUMBER(3)    |          | Y            |        |
| 8        | filtertime_i            | 电流曲线滤波次数     | NUMBER(3)    |          | Y            |        |
| 9        | filtertime_fsdiagram    | 地面功图滤波次数     | NUMBER(3)    |          | Y            |        |
| 10       | filtertime_rpm          | 转速曲线滤波次数     | NUMBER(3)    |          | Y            |        |
| 11       | filtertime_fsdiagram_l  | 地面功图左侧滤波次数 | NUMBER(3)    |          | Y            |        |
| 12       | filtertime_fsdiagram_r  | 地面功图右侧滤波次数 | NUMBER(3)    |          | Y            |        |
| 13       | wattangle               | 功率滤波角度         | NUMBER(8,2)  | 度       | Y            |        |

### 1.3.27 tbl_pcp_productiondata_latest 螺杆泵生产数据实时表

| **序号** | **代码**                   | **名称**        | **类型**      | **单位** | **为空** | **键** |
|----------|----------------------------|-----------------|---------------|----------|----------|--------|
| 1        | id                         | 记录编号        | NUMBER(10)    |         | N        | 主键   | 
| 2        | wellid                     | 井编号          | NUMBER(10)    |         | N        | 外键   | 
| 3        | acquisitiontime            | 采集时间        | DATE          |         | Y        |        | 
| 4        | liftingtype                | 举升类型        | NUMBER(10)    |         | Y        |        | 
| 5        | displacementtype           | 驱替类型        | NUMBER(1)     |         | Y        |        | 
| 6        | runtime                    | 生产时间        | NUMBER(8,2)   | h       | Y        |        | 
| 7        | crudeoildensity            | 原油密度        | NUMBER(16,2)  | g/cm^3  | Y        |        | 
| 8        | waterdensity               | 水密度          | NUMBER(16,2)  | g/cm^3  | Y        |        | 
| 9        | naturalgasrelativedensity  | 天然气相对密度  | NUMBER(16,2)  |         | Y        |        | 
| 10       | saturationpressure         | 饱和压力        | NUMBER(16,2)  | MPa     | Y        |        | 
| 11       | reservoirdepth             | 油层深度        | NUMBER(16,2)  | m       | Y        |        | 
| 12       | reservoirtemperature       | 油层温度        | NUMBER(16,2)  | ℃       | Y        |        |
| 13       | watercut                   | 体积含水率      | NUMBER(8,2)   | %       | Y        |        | 
| 14       | watercut_w                 | 重量含水率      | NUMBER(8,2)   | %       | Y        |        | 
| 15       | tubingpressure             | 油压            | NUMBER(8,2)   | MPa     | Y        |        | 
| 16       | casingpressure             | 套压            | NUMBER(8,2)   | MPa     | Y        |        | 
| 17       | backpressure               | 回压            | NUMBER(8,2)   | MPa     | Y        |        | 
| 18       | wellheadfluidtemperature   | 井口流温        | NUMBER(8,2)   | ℃       | Y        |        |
| 19       | producingfluidlevel        | 动液面          | NUMBER(8,2)   | m       | Y        |        | 
| 20       | pumpsettingdepth           | 泵挂            | NUMBER(8,2)   | m       | Y        |        | 
| 21       | productiongasoilratio      | 生产气油比      | NUMBER(8,2)   | m^3/t   | Y        |        | 
| 22       | tubingstringinsidediameter | 油管内径        | NUMBER(8,2)   | mm      | Y        |        | 
| 23       | casingstringinsidediameter | 油层套管内径    | NUMBER(8,2)   | mm      | Y        |        | 
| 24       | rodstring                  | 抽油杆参数      | VARCHAR2(200) |         | Y        |        | 
| 25       | pumptype                   | 泵类型          | VARCHAR2(20)  |         | Y        |        | 
| 26       | barreltype                 | 泵筒类型        | VARCHAR2(20)  |         | Y        |        | 
| 27       | barrellength               | 泵筒长          | NUMBER(8,2)   | m       | Y        |        | 
| 28       | barrelseries               | 泵级数          | NUMBER(8,2)   |         | Y        |        | 
| 29       | rotordiameter              | 转子截面直径    | NUMBER(8,2)   | mm      | Y        |        | 
| 30       | qpr                        | 公称排量        | NUMBER(8,2)   | m^3/r   | Y        |        | 
| 31       | manualintervention         | 人工干预        | NUMBER(4)     |         | Y        |        | 
| 32       | netgrossratio              | 净毛比          | NUMBER(8,2)   |         | Y        |        | 
| 33       | anchoringstate             | 锚定状态        | NUMBER(1)     |         | Y        |        | 
| 34       | remark                     | 备注            | VARCHAR2(200) |         | Y        |        | 
| 35       | pumpgrade                  | 泵级别          | NUMBER(1)     |         | Y        |        | 
| 36       | pumpborediameter           | 泵径            | NUMBER(8,2)   |         | Y        |        | 
| 37       | plungerlength              | 柱塞长          | NUMBER(8,2)   |         | Y        |        | 

### 1.3.28 tbl_pcp_productiondata_hist 螺杆泵生产数据历史表

同tbl_pcp_productiondata_latest

### 1.3.29 tbl_pcp_discrete_latest 螺杆泵离散数据实时表

| **序号** | **代码**                 | **名称**        | **类型**       | **单位** | **为空** | **键** |
|----------|--------------------------|-----------------|----------------|----------|----------|--------|
| 1        | id                       | 记录编号        | NUMBER(10)     |         | N        | 主键   | 
| 2        | wellid                   | 井编号          | NUMBER(10)     |         | N        | 外键   | 
| 3        | acquisitiontime          | 采集时间        | DATE           |         | Y        |        | 
| 4        | commstatus               | 通信状态        | NUMBER(2)      |         | Y        |        | 
| 5        | commtime                 | 在线时间        | NUMBER(8,2)    | h       | Y        |        | 
| 6        | commtimeefficiency       | 在线时率        | NUMBER(10,4)   |         | Y        |        | 
| 7        | commrange                | 在线区间        | VARCHAR2(2000) |         | Y        |        | 
| 8        | runstatus                | 运行状态        | NUMBER(2)      |         | Y        |        | 
| 9        | runtimeefficiency        | 运行时率        | NUMBER(10,4)   |         | Y        |        | 
| 10       | runtime                  | 运行时间        | NUMBER(8,2)    | h       | Y        |        | 
| 11       | runrange                 | 运行区间        | VARCHAR2(2000) |         | Y        |        | 
| 12       | ia                       | A相电流         | NUMBER(8,2)    | A       | Y        |        | 
| 13       | ib                       | B相电流         | NUMBER(8,2)    | A       | Y        |        | 
| 14       | ic                       | C相电流         | NUMBER(8,2)    | A       | Y        |        | 
| 15       | va                       | A相电压         | NUMBER(8,2)    | V       | Y        |        | 
| 16       | vb                       | B相电压         | NUMBER(8,2)    | V       | Y        |        | 
| 17       | vc                       | C相电压         | NUMBER(8,2)    | V       | Y        |        | 
| 18       | totalwattenergy          | 有功功耗        | NUMBER(8,2)    | kW·h    | Y        |        | 
| 19       | totalvarenergy           | 无功功耗        | NUMBER(8,2)    | kVar·h  | Y        |        | 
| 20       | wattsum                  | 有功功率        | NUMBER(8,2)    | kW      | Y        |        | 
| 21       | varsum                   | 无功功率        | NUMBER(8,2)    | kVar    | Y        |        | 
| 22       | reversepower             | 反向功率        | NUMBER(8,2)    |         | Y        |        | 
| 23       | pfsum                    | 功率因数        | NUMBER(8,2)    |         | Y        |        | 
| 24       | frequencysetvalue        | 变频设置频率    | NUMBER(8,2)    | HZ      | Y        |        | 
| 25       | frequencyrunvalue        | 变频运行频率    | NUMBER(8,2)    | HZ      | Y        |        | 
| 26       | tubingpressure           | 油压            | NUMBER(8,2)    | MPa     | Y        |        | 
| 27       | casingpressure           | 套压            | NUMBER(8,2)    | MPa     | Y        |        | 
| 28       | backpressure             | 回压            | NUMBER(8,2)    | MPa     | Y        |        | 
| 29       | wellheadfluidtemperature | 井口油温        | NUMBER(8,2)    | ℃       | Y        |        |
| 30       | todaywattenergy          | 日有功功耗      | NUMBER(8,2)    | kW·h    | Y        |        | 
| 31       | workingconditioncode     | 电参工况类型    | NUMBER(4)      |         | Y        |        | 
| 32       | iaalarm                  | A相电流报警项   | VARCHAR2(20)   |         | Y        |        | 
| 33       | ibalarm                  | B相电流报警项   | VARCHAR2(20)   |         | Y        |        | 
| 34       | icalarm                  | C相电流报警项   | VARCHAR2(20)   |         | Y        |        | 
| 35       | vaalarm                  | A相电压报警项   | VARCHAR2(20)   |         | Y        |        | 
| 36       | vbalarm                  | B相电压报警项   | VARCHAR2(20)   |         | Y        |        | 
| 37       | vcalarm                  | C相电压报警项   | VARCHAR2(20)   |         | Y        |        | 
| 38       | workingconditionstring   | 电参工况字符串  | VARCHAR2(4000) |         | Y        |        | 
| 39       | iauplimit                | A相电流上限     | NUMBER(8,2)    | A       | Y        |        | 
| 40       | iadownlimit              | A相电流下限     | NUMBER(8,2)    | A       | Y        |        | 
| 41       | ibuplimit                | B相电流上限     | NUMBER(8,2)    | A       | Y        |        | 
| 42       | ibdownlimit              | B相电流下限     | NUMBER(8,2)    | A       | Y        |        | 
| 43       | icuplimit                | C相电流上限     | NUMBER(8,2)    | A       | Y        |        | 
| 44       | icdownlimit              | C相电流下限     | NUMBER(8,2)    | A       | Y        |        | 
| 45       | vauplimit                | A相电压上限     | NUMBER(8,2)    | V       | Y        |        | 
| 46       | vadownlimit              | A相电压下限     | NUMBER(8,2)    | V       | Y        |        | 
| 47       | vbuplimit                | B相电压上限     | NUMBER(8,2)    | V       | Y        |        | 
| 48       | vbdownlimit              | B相电压下限     | NUMBER(8,2)    | V       | Y        |        | 
| 49       | vcuplimit                | C相电压上限     | NUMBER(8,2)    | V       | Y        |        | 
| 50       | vcdownlimit              | C相电压下限     | NUMBER(8,2)    | V       | Y        |        | 
| 51       | iazero                   | A相电流零值     | NUMBER(8,2)    | A       | Y        |        | 
| 52       | ibzero                   | B相电流零值     | NUMBER(8,2)    | A       | Y        |        | 
| 53       | iczero                   | C相电流零值     | NUMBER(8,2)    | A       | Y        |        | 
| 54       | vazero                   | A相电压零值     | NUMBER(8,2)    | V       | Y        |        | 
| 55       | vbzero                   | B相电压零值     | NUMBER(8,2)    | V       | Y        |        | 
| 56       | vczero                   | C相电压零值     | NUMBER(8,2)    | V       | Y        |        | 
| 57       | totalpwattenergy         | 正向有功功耗    | NUMBER(8,2)    | kW·h    | Y        |        | 
| 58       | totalnwattenergy         | 反向有功功耗    | NUMBER(8,2)    | kW·h    | Y        |        | 
| 59       | totalpvarenergy          | 正向无功功耗    | NUMBER(8,2)    | kVar·h  | Y        |        | 
| 60       | totalnvarenergy          | 反向无功功耗    | NUMBER(8,2)    | kVar·h  | Y        |        | 
| 61       | totalvaenergy            | 视在功耗        | NUMBER(8,2)    | kVA·h   | Y        |        | 
| 62       | todaypwattenergy         | 日正向有功功耗  | NUMBER(8,2)    | kW·h    | Y        |        | 
| 63       | todaynwattenergy         | 日反向有功功耗  | NUMBER(8,2)    | kW·h    | Y        |        | 
| 64       | todayvarenergy           | 日无功功耗      | NUMBER(8,2)    | kVar·h  | Y        |        | 
| 65       | todaypvarenergy          | 日正向无功功耗  | NUMBER(8,2)    | kVar·h  | Y        |        | 
| 66       | todaynvarenergy          | 日反向无功功耗  | NUMBER(8,2)    | kVar·h  | Y        |        | 
| 67       | todayvaenergy            | 日视在功耗      | NUMBER(8,2)    | kVA·h   | Y        |        | 
| 68       | vasum                    | 视在功率        | NUMBER(8,2)    | kVA     | Y        |        | 
| 69       | signal                   | 信号强度        | NUMBER(8,2)    |         | Y        |        | 
| 70       | interval                 | 传输间隔        | NUMBER(10)     | min     | Y        |        | 
| 71       | devicever                | 设备版本信息    | VARCHAR2(50)   |         | Y        |        | 
| 72       | vavg                     | 三相电压平均值  | NUMBER(8,2)    | V       | Y        |        | 
| 73       | iavg                     | 三相电流平均值  | NUMBER(8,2)    | A       | Y        |        | 
| 74       | watta                    | A相有功功率     | NUMBER(8,2)    | kW      | Y        |        | 
| 75       | wattb                    | B相有功功率     | NUMBER(8,2)    | kW      | Y        |        | 
| 76       | wattc                    | C相有功功率     | NUMBER(8,2)    | kW      | Y        |        | 
| 77       | vara                     | A相无功功率     | NUMBER(8,2)    | kVar    | Y        |        | 
| 78       | varb                     | B相无功功率     | NUMBER(8,2)    | kVar    | Y        |        | 
| 79       | varc                     | C相无功功率     | NUMBER(8,2)    | kVar    | Y        |        | 
| 80       | vaa                      | A相视在功率     | NUMBER(8,2)    | kVA     | Y        |        | 
| 81       | vab                      | B相视在功率     | NUMBER(8,2)    | kVA     | Y        |        | 
| 82       | vac                      | C相视在功率     | NUMBER(8,2)    | kVA     | Y        |        | 
| 83       | pfa                      | A相功率因数     | NUMBER(8,2)    |         | Y        |        | 
| 84       | pfb                      | B相功率因数     | NUMBER(8,2)    |         | Y        |        | 
| 85       | pfc                      | C相功率因数     | NUMBER(8,2)    |         | Y        |        | 

### 1.3.30 tbl_pcp_discrete_hist 螺杆泵离散数据历史表

同tbl_pcp_discrete_latest

### 1.3.31 tbl_pcp_rpm_latest 螺杆泵曲线数据实时表

| **序号** | **代码**                   | **名称**            | **类型**      | **单位**    | **为空** | **键** |
|----------|----------------------------|---------------------|---------------|-------------|----------|--------|
| 1        | id                         | 记录编号            | NUMBER(10)    |            | N        | 主键   | 
| 2        | wellid                     | 井编号              | NUMBER(10)    |            | N        | 外键   | 
| 3        | acquisitiontime            | 采集时间            | DATE          |            | Y        |        | 
| 4        | rpm                        | 转速                | NUMBER(8,2)   | r/min      | Y        |        | 
| 5        | torque                     | 扭矩                | NUMBER(8,2)   | kN·m       | Y        |        | 
| 6        | theoreticalproduction      | 理论排量            | NUMBER(8,2)   | m^3/d      | Y        |        | 
| 7        | liquidvolumetricproduction | 产液量方            | NUMBER(8,2)   | m^3/d      | Y        |        | 
| 8        | oilvolumetricproduction    | 产油量方            | NUMBER(8,2)   | m^3/d      | Y        |        | 
| 9        | watervolumetricproduction  | 产水量方            | NUMBER(8,2)   | m^3/d      | Y        |        | 
| 10       | liquidweightproduction     | 产液量吨            | NUMBER(8,2)   | t/d        | Y        |        | 
| 11       | oilweightproduction        | 产油量吨            | NUMBER(8,2)   | t/d        | Y        |        | 
| 12       | waterweightproduction      | 产水量吨            | NUMBER(8,2)   | t/d        | Y        |        | 
| 13       | motorinputactivepower      | 电机输入有功功率    | NUMBER(8,2)   | kW         | Y        |        | 
| 14       | waterpower                 | 水功率              | NUMBER(8,2)   | kW         | Y        |        | 
| 15       | systemefficiency           | 系统效率            | NUMBER(12,3)  | 小数       | Y        |        | 
| 16       | powerconsumptionperthm     | 吨液百米耗电量      | NUMBER(8,2)   | kW·h/100m·t| Y        |        | 
| 17       | pumpeff1                   | 容积效率            | NUMBER(12,3)  | 小数       | Y        |        | 
| 18       | pumpeff2                   | 液体收缩系数        | NUMBER(12,3)  | 小数       | Y        |        | 
| 19       | pumpeff                    | 泵效                | NUMBER(12,3)  | 小数       | Y        |        | 
| 20       | pumpintakep                | 泵入口压力          | NUMBER(8,2)   | MPa        | Y        |        | 
| 21       | pumpintaket                | 泵入口温度          | NUMBER(8,2)   | ℃         | Y        |        | 
| 22       | pumpintakegol              | 泵入口就地气液比    | NUMBER(8,2)   | m^3/m^3    | Y        |        | 
| 23       | pumpintakevisl             | 泵入口粘度          | NUMBER(8,2)   | mPa·s      | Y        |        | 
| 24       | pumpintakebo               | 泵入口原油体积系数  | NUMBER(8,2)   | 小数       | Y        |        | 
| 25       | pumpoutletp                | 泵出口压力          | NUMBER(8,2)   | MPa        | Y        |        | 
| 26       | pumpoutlett                | 泵出口温度          | NUMBER(8,2)   | ℃         | Y        |        | 
| 27       | pumpoutletgol              | 泵出口就地气液比    | NUMBER(8,2)   | m^3/m^3    | Y        |        | 
| 28       | pumpoutletvisl             | 泵出口粘度          | NUMBER(8,2)   | mPa·s      | Y        |        | 
| 29       | pumpoutletbo               | 泵出口原油体积系数  | NUMBER(8,2)   | 小数       | Y        |        | 
| 30       | rodstring                  | 抽油杆柱分析数据    | VARCHAR2(200) |            | Y        |        | 
| 31       | savetime                   | 入库时间            | DATE          |            | Y        |        | 
| 32       | productiondataid           | 生产数据编号        | NUMBER(10)    |            | Y        |        | 
| 33       | resultstatus               | 计算标志            | NUMBER(2)     |            | Y        |        | 
| 34       | discretedataid             | 离散数据编号        | NUMBER(10)    |            | Y        |        | 
| 35       | remark                     | 备注                | VARCHAR2(200) |            | Y        |        | 
| 36       | workingconditioncode       | 工况类型            | NUMBER(4)     |            | Y        |        | 

### 1.3.32 tbl_pcp_rpm_hist 螺杆泵曲线数据历史表

同tbl_pcp_rpm_latest

### 1.3.33 tbl_pcp_total_day 螺杆泵日累计数据表 

| **序号** | **代码**                      | **名称**                  | **类型**       | **单位**     | **为空** | **键** | 
|----------|-------------------------------|---------------------------|----------------|--------------|----------|--------|
| 1        | id                            | 记录编号                  | NUMBER(10)     |              | N        | 主键   | 
| 2        | wellid                        | 井编号                    | NUMBER(10)     |              | Y        | 外键   | 
| 3        | calculatedate                 | 计算时间                  | DATE           |              | Y        |        | 
| 4        | commstatus                    | 通信状态                  | NUMBER(2)      |              | Y        |        | 
| 5        | runstatus                     | 运行状态                  | NUMBER(2)      |              | Y        |        | 
| 6        | commtime                      | 在线时间                  | NUMBER(8,2)    | h            | Y        |        | 
| 7        | commtimeefficiency            | 在线时率                  | NUMBER(12,3)   |              | Y        |        | 
| 8        | commrange                     | 在线区间                  | VARCHAR2(4000) |              | Y        |        | 
| 9        | runtime                       | 运行时间                  | NUMBER(8,2)    | h            | Y        |        | 
| 10       | runrange                      | 运行区间                  | VARCHAR2(4000) |              | Y        |        | 
| 11       | runtimeefficiency             | 生产时率                  | NUMBER(12,3)   | 小数         | Y        |        | 
| 12       | workingconditioncode          | 工况代码                  | NUMBER(4)      |              | Y        |        | 
| 13       | workingconditionstring        | 工况字符串                | VARCHAR2(4000) |              | Y        |        | 
| 14       | rpm                           | 转速                      | NUMBER(4)      | r/min        | Y        |        | 
| 15       | rpmmax                        | 转速最大值                | VARCHAR2(4000) | r/min        | Y        |        | 
| 16       | rpmmin                        | 转速最小值                | NUMBER(10,4)   | r/min        | Y        |        | 
| 17       | torque                        | 扭矩                      | NUMBER(10,4)   | kN·m         | Y        |        | 
| 18       | torquemax                     | 扭矩最大值                | NUMBER(10,4)   | kN·m         | Y        |        | 
| 19       | torquemin                     | 扭矩最小值                | NUMBER(8,2)    | kN·m         | Y        |        | 
| 20       | liquidvolumetricproduction    | 产液量方                  | NUMBER(8,2)    | m^3/d        | Y        |        | 
| 21       | oilvolumetricproduction       | 产油量方                  | NUMBER(8,2)    | m^3/d        | Y        |        | 
| 22       | watervolumetricproduction     | 产水量方                  | NUMBER(8,2)    | m^3/d        | Y        |        | 
| 23       | liquidweightproduction        | 产液量吨                  | NUMBER(8,2)    | t/d          | Y        |        | 
| 24       | oilweightproduction           | 产油量吨                  | NUMBER(8,2)    | t/d          | Y        |        | 
| 25       | waterweightproduction         | 产水量吨                  | NUMBER(8,2)    | t/d          | Y        |        | 
| 26       | liquidvolumetricproductionmax | 产液量最大值方            | NUMBER(8,2)    | m^3/d        | Y        |        | 
| 27       | liquidvolumetricproductionmin | 产液量最小值方            | NUMBER(8,2)    | m^3/d        | Y        |        | 
| 28       | oilvolumetricproductionmax    | 产油量最大值方            | NUMBER(8,2)    | m^3/d        | Y        |        | 
| 29       | oilvolumetricproductionmin    | 产油量最小值方            | NUMBER(8,2)    | m^3/d        | Y        |        | 
| 30       | watervolumetricproductionmax  | 产水量最大值方            | NUMBER(8,2)    | m^3/d        | Y        |        | 
| 31       | watervolumetricproductionmin  | 产水量最小值方            | NUMBER(8,2)    | m^3/d        | Y        |        | 
| 32       | liquidweightproductionmax     | 产液量最大值吨            | NUMBER(8,2)    | t/d          | Y        |        | 
| 33       | liquidweightproductionmin     | 产液量最小值吨            | NUMBER(8,2)    | t/d          | Y        |        | 
| 34       | oilweightproductionmax        | 产油量最大值吨            | NUMBER(8,2)    | t/d          | Y        |        | 
| 35       | oilweightproductionmin        | 产油量最小值吨            | NUMBER(8,2)    | t/d          | Y        |        | 
| 36       | waterweightproductionmax      | 产水量最大值吨            | NUMBER(8,2)    | t/d          | Y        |        | 
| 37       | waterweightproductionmin      | 产水量最小值吨            | NUMBER(8,2)    | t/d          | Y        |        | 
| 38       | watercut                      | 体积含水率                | NUMBER(8,2)    | %            | Y        |        | 
| 39       | watercut_w                    | 重量含水率                | NUMBER(8,2)    | %            | Y        |        | 
| 40       | watercutmax                   | 体积含水率最大值          | NUMBER(8,2)    | %            | Y        |        | 
| 41       | watercutmin                   | 体积含水率最小值          | NUMBER(8,2)    | %            | Y        |        | 
| 42       | watercutmax_w                 | 重量含水率最大值          | NUMBER(8,2)    | %            | Y        |        | 
| 43       | watercutmin_w                 | 重量含水率最小值          | NUMBER(8,2)    | %            | Y        |        | 
| 44       | tubingpressure                | 油压                      | NUMBER(8,2)    | MPa          | Y        |        | 
| 45       | tubingpressuremax             | 油压最大值                | NUMBER(8,2)    | MPa          | Y        |        | 
| 46       | tubingpressuremin             | 油压最小值                | NUMBER(8,2)    | MPa          | Y        |        | 
| 47       | casingpressure                | 套压                      | NUMBER(8,2)    | MPa          | Y        |        | 
| 48       | casingpressuremax             | 套压最大值                | NUMBER(8,2)    | MPa          | Y        |        | 
| 49       | casingpressuremin             | 套压最小值                | NUMBER(8,2)    | MPa          | Y        |        | 
| 50       | wellheadfluidtemperature      | 井口油温                  | NUMBER(8,2)    | ℃            | Y        |        | 
| 51       | wellheadfluidtemperaturemax   | 井口油温最大值            | NUMBER(8,2)    | ℃            | Y        |        | 
| 52       | wellheadfluidtemperaturemin   | 井口油温最小值            | NUMBER(10,4)   | ℃            | Y        |        | 
| 53       | productiongasoilratio         | 生产气油比                | NUMBER(10,4)   | m^3/t        | Y        |        | 
| 54       | productiongasoilratiomax      | 生产气油比最大值          | NUMBER(10,4)   | m^3/t        | Y        |        | 
| 55       | productiongasoilratiomin      | 生产气油比最小值          | NUMBER(10,4)   | m^3/t        | Y        |        | 
| 56       | producingfluidlevel           | 动液面                    | NUMBER(10,4)   | m            | Y        |        | 
| 57       | producingfluidlevelmax        | 动液面最大值              | NUMBER(10,4)   | m            | Y        |        | 
| 58       | producingfluidlevelmin        | 动液面最小值              | NUMBER(8,2)    | m            | Y        |        | 
| 59       | pumpsettingdepth              | 泵挂                      | NUMBER(8,2)    | m            | Y        |        | 
| 60       | pumpsettingdepthmax           | 泵挂最大值                | NUMBER(8,2)    | m            | Y        |        | 
| 61       | pumpsettingdepthmin           | 泵挂最小值                | NUMBER(8,2)    | m            | Y        |        | 
| 62       | submergence                   | 沉没度                    | NUMBER(8,2)    | m            | Y        |        | 
| 63       | submergencemax                | 沉没度最大值              | NUMBER(8,2)    | m            | Y        |        | 
| 64       | submergencemin                | 沉没度最小值              | NUMBER(8,2)    | m            | Y        |        | 
| 65       | pumpborediameter              | 泵径                      | NUMBER(8,2)    | mm           | Y        |        | 
| 66       | pumpborediametermax           | 泵径最大值                | NUMBER(8,2)    | mm           | Y        |        | 
| 67       | pumpborediametermin           | 泵径最小值                | NUMBER(8,2)    | mm           | Y        |        | 
| 68       | systemefficiency              | 系统效率                  | NUMBER(8,2)    | 小数         | Y        |        | 
| 69       | systemefficiencymax           | 系统效率最大值            | NUMBER(8,2)    | 小数         | Y        |        | 
| 70       | systemefficiencymin           | 系统效率最小值            | NUMBER(8,2)    | 小数         | Y        |        | 
| 71       | surfacesystemefficiency       | 地面效率                  | NUMBER(8,2)    | 小数         | Y        |        | 
| 72       | surfacesystemefficiencymax    | 地面效率最大值            | NUMBER(8,2)    | 小数         | Y        |        | 
| 73       | surfacesystemefficiencymin    | 地面效率最小值            | NUMBER(8,2)    | 小数         | Y        |        | 
| 74       | welldownsystemefficiency      | 井下效率                  | NUMBER(8,2)    | 小数         | Y        |        | 
| 75       | welldownsystemefficiencymax   | 井下效率最大值            | NUMBER(8,2)    | 小数         | Y        |        | 
| 76       | welldownsystemefficiencymin   | 井下效率最小值            | NUMBER(8,2)    | 小数         | Y        |        | 
| 77       | powerconsumptionperthm        | 吨液百米耗电量            | NUMBER(8,2)    | kW·h/100m·t  | Y        |        | 
| 78       | powerconsumptionperthmmax     | 吨液百米耗电量最大值      | NUMBER(8,2)    | kW·h/100m·t  | Y        |        | 
| 79       | powerconsumptionperthmmin     | 吨液百米耗电量最小值      | NUMBER(8,2)    | kW·h/100m·t  | Y        |        | 
| 80       | pumpeff                       | 总泵效                    | NUMBER(8,2)    | 小数         | Y        |        | 
| 81       | pumpeffmax                    | 总泵效最大值              | NUMBER(8,2)    | 小数         | Y        |        | 
| 82       | pumpeffmin                    | 总泵效最小值              | NUMBER(10,4)   | 小数         | Y        |        | 
| 83       | ia                            | A相电流                   | NUMBER(10,4)   | A            | Y        |        | 
| 84       | iamax                         | A相电流最大值             | NUMBER(10,4)   | A            | Y        |        | 
| 85       | iamin                         | A相电流最小值             | NUMBER(10,4)   | A            | Y        |        | 
| 86       | ib                            | B相电流                   | NUMBER(10,4)   | A            | Y        |        | 
| 87       | ibmax                         | B相电流最大值             | NUMBER(10,4)   | A            | Y        |        | 
| 88       | ibmin                         | B相电流最小值             | NUMBER(10,4)   | A            | Y        |        | 
| 89       | ic                            | C相电流                   | NUMBER(10,4)   | A            | Y        |        | 
| 90       | icmax                         | C相电流最大值             | NUMBER(10,4)   | A            | Y        |        | 
| 91       | icmin                         | C相电流最小值             | NUMBER(8,2)    | A            | Y        |        | 
| 92       | va                            | A相电压                   | NUMBER(8,2)    | V            | Y        |        | 
| 93       | vamax                         | A相电压最大值             | NUMBER(8,2)    | V            | Y        |        | 
| 94       | vamin                         | A相电压最小值             | NUMBER(10,4)   | V            | Y        |        | 
| 95       | vb                            | B相电压                   | NUMBER(10,4)   | V            | Y        |        | 
| 96       | vbmax                         | B相电压最大值             | NUMBER(10,4)   | V            | Y        |        | 
| 97       | vbmin                         | B相电压最小值             | NUMBER(8,2)    | V            | Y        |        | 
| 98       | vc                            | C相电压                   | NUMBER(8,2)    | V            | Y        |        | 
| 99       | vcmax                         | C相电压最大值             | NUMBER(8,2)    | V            | Y        |        | 
| 100      | vcmin                         | C相电压最小值             | NUMBER(8,2)    | V            | Y        |        | 
| 101      | wattsum                       | 有功功率                  | NUMBER(8,2)    | kW           | Y        |        | 
| 102      | wattsummax                    | 有功功率最大值            | NUMBER(8,2)    | kW           | Y        |        | 
| 103      | wattsummin                    | 有功功率最小值            | NUMBER(8,2)    | kW           | Y        |        | 
| 104      | varsum                        | 无功功率                  | NUMBER(8,2)    | kVar         | Y        |        | 
| 105      | varsummax                     | 无功功率最大值            | NUMBER(8,2)    | kVar         | Y        |        | 
| 106      | varsummin                     | 无功功率最小值            | NUMBER(8,2)    | kVar         | Y        |        | 
| 107      | pfsum                         | 功率因数                  | NUMBER(8,2)    |              | Y        |        | 
| 108      | pfsummax                      | 功率因数最大值            | NUMBER(8,2)    |              | Y        |        | 
| 109      | pfsummin                      | 功率因数最小值            | NUMBER(8,2)    |              | Y        |        | 
| 110      | frequency                     | 运行频率                  | NUMBER(8,2)    | HZ           | Y        |        | 
| 111      | frequencymax                  | 运行频率最大值            | NUMBER(8,2)    | HZ           | Y        |        | 
| 112      | frequencymin                  | 运行频率最小值            | NUMBER(8,2)    | HZ           | Y        |        | 
| 113      | todaywattenergy               | 日有功功耗                | NUMBER(8,2)    | kW·h         | Y        |        | 
| 114      | todaypwattenergy              | 日正向有功功耗            | NUMBER(8,2)    | kW·h         | Y        |        | 
| 115      | todaynwattenergy              | 日反向有功功耗            | NUMBER(8,2)    | kW·h         | Y        |        | 
| 116      | todayvarenergy                | 日无功功耗                | NUMBER(8,2)    | kVar·h       | Y        |        | 
| 117      | todaypvarenergy               | 日正向无功功耗            | NUMBER(8,2)    | kVar·h       | Y        |        | 
| 118      | todaynvarenergy               | 日反向无功功耗            | NUMBER(8,2)    | kVar·h       | Y        |        | 
| 119      | todayvaenergy                 | 日视在功耗                | NUMBER(8,2)    | kVA·h        | Y        |        | 
| 120      | totalwattenergy               | 累计有功功耗              | NUMBER(8,2)    | kW·h         | Y        |        | 
| 121      | totalpwattenergy              | 累计正向有功功耗          | NUMBER(8,2)    | kW·h         | Y        |        | 
| 122      | totalnwattenergy              | 累计反向有功功耗          | NUMBER(8,2)    | kW·h         | Y        |        | 
| 123      | totalvarenergy                | 累计无功功耗              | NUMBER(8,2)    | kVar·h       | Y        |        | 
| 124      | totalpvarenergy               | 累计正向无功功耗          | NUMBER(8,2)    | kVar·h       | Y        |        | 
| 125      | totalnvarenergy               | 累计反向无功功耗          | NUMBER(8,2)    | kVar·h       | Y        |        | 
| 126      | totalvaenergy                 | 累计视在功耗              | NUMBER(8,2)    | kVA·h        | Y        |        | 
| 127      | extendeddays                  | 延用天数                  | NUMBER(8,2)    |              | Y        |        | 
| 128      | resultstatus                  | 计算标志                  | NUMBER(8,2)    |              | Y        |        | 
| 129      | signal                        | 信号强度                  | NUMBER(8,2)    |              | Y        |        | 
| 130      | signalmax                     | 信号强度最大值            | NUMBER(8,2)    |              | Y        |        | 
| 131      | signalmin                     | 信号强度最小值            | NUMBER(8,2)    |              | Y        |        | 
| 132      | savetime                      | 存储时间                  | NUMBER(8,2)    |              | Y        |        |
| 133      | theoreticalproduction         | 理论排量                  | NUMBER(8,2)    | m^3/d        | Y        |        | 
| 134      | theoreticalproductionmax      | 理论排量最大值            | NUMBER(8,2)    | m^3/d        | Y        |        | 
| 135      | theoreticalproductionmin      | 理论排量最小值            | NUMBER(8,2)    | m^3/d        | Y        |        | 
| 136      | avgwatt                       | 平均有功功率              | NUMBER(8,2)    | kW           | Y        |        | 
| 137      | avgwattmax                    | 平均有功功率最大值        | NUMBER(8,2)    | kW           | Y        |        | 
| 138      | avgwattmin                    | 平均有功功率最小值        | NUMBER(8,2)    | kW           | Y        |        | 
| 139      | waterpower                    | 水功率                    | NUMBER(8,2)    | kW           | Y        |        | 
| 140      | waterpowermax                 | 水功率最大值              | NUMBER(8,2)    | kW           | Y        |        | 
| 141      | waterpowermin                 | 水功率最小值              | NUMBER(8,2)    | kW           | Y        |        | 
| 142      | pumpeff1                      | 容积效率                  | NUMBER(10,4)   | 小数         | Y        |        | 
| 143      | pumpeff1max                   | 容积效率最大值            | NUMBER(10,4)   | 小数         | Y        |        | 
| 144      | pumpeff1min                   | 容积效率最小值            | NUMBER(10,4)   | 小数         | Y        |        | 
| 145      | pumpeff2                      | 液体收缩系数              | NUMBER(10,4)   | 小数         | Y        |        | 
| 146      | pumpeff2max                   | 液体收缩系数最大值        | NUMBER(10,4)   | 小数         | Y        |        | 
| 147      | pumpeff2min                   | 液体收缩系数最小值        | NUMBER(10,4)   | 小数         | Y        |        | 
| 148      | vasum                         | 视在功率                  | NUMBER(8,2)    | kVA          | Y        |        | 
| 149      | vasummax                      | 视在功率最大值            | NUMBER(8,2)    | kVA          | Y        |        | 
| 150      | vasummin                      | 视在功率最小值            | NUMBER(8,2)    | kVA          | Y        |        | 


# 二、视图

## 2.1 视图概览

| **序号** | **名称**                      | **描述**               |
|----------|-------------------------------|------------------------|
| 1        | viw_wellinformation           | 井名信息视图           |
| 2        | viw_wellboretrajectory        | 井身轨迹视图           |
| 3        | viw_rpc_productiondata_latest | 抽油机生产数据实时视图 |
| 4        | viw_rpc_productiondata_hist   | 抽油机生产数据历史视图 |
| 5        | viw_commstatus                | 通信状态视图           |
| 6        | viw_rpc_diagram_latest        | 抽油机曲线数据实时视图 |
| 7        | viw_rpc_diagram_hist          | 抽油机曲线数据历史视图 |
| 8        | viw_rpc_discrete_latest       | 抽油机离散数据实时视图 |
| 9        | viw_rpc_discrete_hist         | 抽油机离散数据历史视图 |
| 10       | viw_rpc_comprehensive_latest  | 抽油机综合数据实时视图 |
| 11       | viw_rpc_comprehensive_hist    | 抽油机综合数据历史视图 |
| 12       | viw_rpc_diagramquery_latest   | 抽油机图形查询实时视图 |
| 13       | viw_rpc_diagramquery_hist     | 抽油机图形查询历史视图 |
| 14       | viw_rpc_total_day             | 抽油机日累计数据视图   |
| 15       | viw_rpc_calculatemain         | 抽油机计算结果管理视图 |
| 16       | viw_pcp_productiondata_latest | 螺杆泵生产数据实时视图 |
| 17       | viw_pcp_productiondata_hist   | 螺杆泵生产数据历史视图 |
| 18       | viw_pcp_rpm_latest            | 螺杆泵曲线数据实时视图 |
| 19       | viw_pcp_rpm_hist              | 螺杆泵曲线数据历史视图 |
| 20       | viw_pcp_discrete_latest       | 螺杆泵离散数据实时视图 |
| 21       | viw_pcp_discrete_hist         | 螺杆泵离散数据历史视图 |
| 22       | viw_pcp_comprehensive_latest  | 螺杆泵综合数据实时视图 |
| 23       | viw_pcp_comprehensive_hist    | 螺杆泵综合数据历史视图 |
| 24       | viw_pcp_total_day             | 螺杆泵日累计数据视图   |

## 2.2 详述

### 2.2.1 viw_wellinformation 井名信息视图

| **序号** | **代码**                   | **名称**             | **类型**      | **单位** |
|----------|----------------------------|----------------------|---------------|----------|
| 1        | id                         | 记录编号             | NUMBER(10)    |          |
| 2        | orgname                    | 组织名称             | VARCHAR2(100) |          |
| 3        | orgid                      | 组织编号             | NUMBER(10)    |          |
| 4        | resname                    | 油气藏名称           | VARCHAR2(200) |          |
| 5        | wellname                   | 井名                 | VARCHAR2(200) |          |
| 6        | liftingtype                | 举升方式             | NUMBER(10)    |          |
| 7        | driveraddr                 | 设备地址             | VARCHAR2(200) |          |
| 8        | driverid                   | 设备编号             | VARCHAR2(200) |          |
| 9        | acqcycle_diagram           | 曲线采集间隔         | NUMBER(10)    | min      |
| 10       | acqcyclesetstatus_diagram  | 曲线采集间隔设置状态 | NUMBER(2)     |          |
| 11       | acqcycle_discrete          | 离散采集间隔         | NUMBER(10)    | min      |
| 12       | acqcyclesetstatus_discrete | 离散采集间隔设置状态 | NUMBER(2)     |          |
| 13       | savecycle_discrete         | 离散保存间隔         | NUMBER(10)    | min      |
| 14       | runtimeefficiencysource    | 时率来源             | VARCHAR2(200) |          |
| 15       | videourl                   | 视频路径             | VARCHAR2(400) |          |
| 16       | liftingtypename            | 举升方式名称         | VARCHAR2(200) |          |
| 17       | drivercode                 | 驱动编码             | VARCHAR2(50)  |          |
| 18       | acquisitionunit            | 采集组编码           | VARCHAR2(50)  |          |
| 19       | sortnum                    | 排序编号             | NUMBER(10)    |          |

### 2.2.2 viw_wellboretrajectory 井身轨迹视图

| **序号** | **代码**       | **名称**  | **类型**      | **单位** |
|----------|----------------|-----------|---------------|----------|
| 1        | id             | 记录编号  | NUMBER(10)    |          |
| 2        | orgname        | 单位名称  | VARCHAR2(100) |          |
| 3        | orgid          | 单位序号  | NUMBER(10)    |          |
| 4        | wellname       | 井名      | VARCHAR2(200) |          |
| 5        | measuringdepth | 测量深度  | CLOB          | m        |
| 6        | verticaldepth  | 垂直深度  | CLOB          | m        |
| 7        | deviationangle | 井斜角    | CLOB          | 度       |
| 8        | azimuthangle   | 方位角    | CLOB          | 度       |
| 9        | x              | 直角坐标x | CLOB          |          |
| 10       | y              | 直角坐标y | CLOB          |          |
| 11       | z              | 直角坐标z | CLOB          |          |
| 12       | savetime       | 入库时间  | DATE          |          |
| 13       | resultstatus   | 计算标志  | NUMBER(4)     |          |
| 14       | sortnum        | 排序编号  | NUMBER(10)    |          |

### 2.2.3 viw_rpc_productiondata_latest 抽油机生产数据实时视图

| **序号** | **代码**                   | **名称**       | **类型**      | **单位** |
|----------|----------------------------|----------------|---------------|----------|
| 1        | id                         | 记录编号       | NUMBER(10)    |          |
| 2        | wellname                   | 井名           | VARCHAR2(200) |          |
| 3        | wellid                     | 井编号         | NUMBER(10)    |          |
| 4        | liftingtype                | 举升类型       | NUMBER(10)    |          |
| 5        | acquisitiontime            | 采集时间       | DATE          |          |
| 6        | runtime                    | 运行时间       | NUMBER(8,2)   | h        |
| 7        | crudeoildensity            | 原油密度       | NUMBER(16,2)  | g/cm^3   |
| 8        | waterdensity               | 水密度         | NUMBER(16,2)  | g/cm^3   |
| 9        | naturalgasrelativedensity  | 天然气相对密度 | NUMBER(16,2)  |          |
| 10       | saturationpressure         | 饱和压力       | NUMBER(16,2)  | MPa      |
| 11       | reservoirdepth             | 油层中部深度   | NUMBER(16,2)  | m        |
| 12       | reservoirtemperature       | 油层中部温度   | NUMBER(16,2)  | ℃       |
| 13       | watercut_w                 | 重量含水率     | NUMBER(8,2)   | %        |
| 14       | watercut                   | 体积含水率     | NUMBER(8,2)   | %        |
| 15       | tubingpressure             | 油压           | NUMBER(8,2)   | MPa      |
| 16       | casingpressure             | 套压           | NUMBER(8,2)   | MPa      |
| 17       | backpressure               | 回压           | NUMBER(8,2)   | MPa      |
| 18       | wellheadfluidtemperature   | 井口油温       | NUMBER(8,2)   | ℃       |
| 19       | producingfluidlevel        | 动液面         | NUMBER(8,2)   | m        |
| 20       | pumpsettingdepth           | 泵挂           | NUMBER(8,2)   | m        |
| 21       | productiongasoilratio      | 生产气油比     | NUMBER(8,2)   | m^3/t    |
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

### 2.2.4 viw_rpc_productiondata_hist 抽油机生产数据历史视图

同viw_rpc_productiondata_latest

### 2.2.5 viw_commstatus 通信状态视图 

| **序号** | **代码**   | **名称** | **类型**      | **单位** |
|----------|------------|----------|---------------|----------|
| 1        | id         | 编号     | NUMBER(10)    |          |
| 2        | wellname   | 井名     | VARCHAR2(200) |          |
| 3        | commstatus | 通信状态 | NUMBER(1)     |          |

### 2.2.6 viw_rpc_diagram_latest 抽油机曲线数据实时视图

| **序号** | **代码**                      | **名称**           | **类型**      | **单位**    |
|----------|-------------------------------|--------------------|---------------|-------------|
| 1        | id                            | 记录编号           | NUMBER(10)    |             |
| 2        | wellname                      | 井名               | VARCHAR2(200) |             |
| 3        | wellid                        | 井编号             | NUMBER(10)    |             |
| 4        | liftingtype                   | 举升类型           | NUMBER(10)    |             |
| 5        | driveraddr                    | 设备地址           | VARCHAR2(200) |             |
| 6        | acquisitiontime               | 采集时间           | DATE          |             |
| 7        | commstatus                    | 通信状态           | NUMBER(1)     |             |
| 8        | commstatusname                | 通信状态名称       | VARCHAR2      |             |
| 9        | commalarmlevel                | 通信状态报警级别   | NUMBER(3)     |             |
| 10       | workingconditioncode          | 功图工况代码       | NUMBER(4)     |             |
| 11       | workingconditionname          | 功图工况名称       | VARCHAR2(200) |             |
| 12       | optimizationsuggestion        | 优化建议           | VARCHAR2(200) |             |
| 13       | workingconditionrunalarmlevel | 功图工况报警级别   | NUMBER(3)     |             |
| 14       | theoreticalproduction         | 理论排量           | NUMBER(8,2)   | m^3/d       |
| 15       | liquidweightproduction        | 产液量吨           | NUMBER(8,2)   | t/d         |
| 16       | oilweightproduction           | 产油量吨           | NUMBER(8,2)   | t/d         |
| 17       | waterweightproduction         | 产水量吨           | NUMBER(8,2)   | t/d         |
| 18       | watercut_w                    | 重量含水率         | NUMBER(8,2)   | %           |
| 19       | liquidweightproductionlevel   | 产液级别吨         | VARCHAR2(50)  |             |
| 20       | liquidvolumetricproduction    | 产液量方           | NUMBER(8,2)   | m^3/d       |
| 21       | oilvolumetricproduction       | 产油量方           | NUMBER(8,2)   | m^3/d       |
| 22       | watervolumetricproduction     | 产水量方           | NUMBER(8,2)   | m^3/d       |
| 23       | watercut                      | 体积含水率         | NUMBER(8,2)   | %           |
| 24       | liquidvolumeproductionlevel   | 产液级别方         | VARCHAR2(50)  |             |
| 25       | productiongasoilratio         | 生产气油比         | NUMBER(8,2)   | m^3/t       |
| 26       | tubingpressure                | 油压               | NUMBER(8,2)   | MPa         |
| 27       | casingpressure                | 套压               | NUMBER(8,2)   | MPa         |
| 28       | wellheadfluidtemperature      | 井口油温           | NUMBER(8,2)   | ℃           |
| 29       | producingfluidlevel           | 动液面             | NUMBER(8,2)   | m           |
| 30       | levelcorrectvalue             | 液面反演校正值             | NUMBER(8,2)   | MPa           |
| 31       | pumpsettingdepth              | 泵挂               | NUMBER(8,2)   | m           |
| 32       | submergence                   | 沉没度             | NUMBER(8,2)   | m           |
| 33       | pumpborediameter              | 泵径               | NUMBER(8,2)   | mm          |
| 34       | crudeoildensity               | 原油密度           | NUMBER(16,2)  | g/cm^3      |
| 35       | netgrossratio                 | 净毛比             | NUMBER(8,2)   |             |
| 36       | availableplungerstrokeprod    | 柱塞有效冲程产量吨 | NUMBER(8,2)   | t/d         |
| 37       | pumpclearanceleakprod         | 泵间隙漏失量吨     | NUMBER(8,2)   | t/d         |
| 38       | tvleakweightproduction        | 游动凡尔漏失量吨   | NUMBER(8,2)   | t/d         |
| 39       | svleakweightproduction        | 固定凡尔漏失量吨   | NUMBER(8,2)   | t/d         |
| 40       | gasinfluenceprod              | 气影响吨           | NUMBER(8,2)   | t/d         |
| 41       | availableplungerstrokeprod_v  | 柱塞有效冲程产量方 | NUMBER(8,2)   | m^3/d       |
| 42       | pumpclearanceleakprod_v       | 泵间隙漏失量方     | NUMBER(8,2)   | m^3/d       |
| 43       | tvleakvolumetricproduction    | 游动凡尔漏失量方   | NUMBER(8,2)   | m^3/d       |
| 44       | svleakvolumetricproduction    | 固定凡尔漏失量方   | NUMBER(8,2)   | m^3/d       |
| 45       | gasinfluenceprod_v            | 气影响方           | NUMBER(8,2)   | m^3/d       |
| 46       | rodstring                     | 抽油杆数据         | VARCHAR2(200) |             |
| 47       | stroke                        | 冲程               | NUMBER(8,2)   | m           |
| 48       | spm                           | 冲次               | NUMBER(8,2)   | 次/min      |
| 49       | upperloadline                 | 理论上载荷         | NUMBER(8,2)   | kN          |
| 50       | upperloadlineofexact          | 真实理论上载荷     | NUMBER(8,2)   | kN          |
| 51       | lowerloadline                 | 理论下载荷         | NUMBER(8,2)   | kN          |
| 52       | upperloadline                 | 理论液柱载荷       | NUMBER(8,2)   | kN          |
| 53       | fmax                          | 最大载荷           | NUMBER(8,2)   | kN          |
| 54       | fmin                          | 最小载荷           | NUMBER(8,2)   | kN          |
| 55       | deltaf                        | 载荷差             | NUMBER(8,2)   | kN          |
| 56       | fullnesscoefficient           | 充满系数           | NUMBER(8,2)   | 小数        |
| 57       | noliquidfullnesscoefficient   | 抽空充满系数       | NUMBER(10,4)  | 小数        |
| 58       | plungerstroke                 | 柱塞冲程           | NUMBER(8,2)   | m           |
| 59       | availableplungerstroke        | 柱塞有效冲程       | NUMBER(8,2)   | m           |
| 60       | noliquidavailableplungerstroke| 抽空柱塞有效冲程   | NUMBER(10,4)  | m           |
| 61       | motorinputactivepower         | 电机输入有功功率   | NUMBER(8,2)   | kW          |
| 62       | polishrodpower                | 光杆功率           | NUMBER(8,2)   | kW          |
| 63       | waterpower                    | 水功率             | NUMBER(8,2)   | kW          |
| 64       | systemefficiency              | 系统效率           | NUMBER(12,3)  | 小数        |
| 65       | systemefficiencylevel         | 系统效率级别       | VARCHAR2(50)  |             |
| 66       | surfacesystemefficiency       | 地面效率           | NUMBER(12,3)  | 小数        |
| 67       | surfacesystemefficiencylevel  | 地面效率级别       | VARCHAR2(50)  |             |
| 68       | welldownsystemefficiency      | 井下效率           | NUMBER(12,3)  | 小数        |
| 69       | welldownsystemefficiencylevel | 井下效率级别       | VARCHAR2(50)  |             |
| 70       | fsdiagramarea                 | 功图面积           | NUMBER(8,2)   |             |
| 71       | powerconsumptionperthm        | 吨液百米耗电量     | NUMBER(8,2)   | kW·h/100m·t |
| 72       | idegreebalance                | 电流平衡度         | NUMBER(8,2)   | %           |
| 73       | idegreebalancename            | 电流平衡状态       | VARCHAR2(200) |             |
| 74       | upstrokeimax                  | 上冲程最大电流     | NUMBER(8,2)   | A           |
| 75       | downstrokeimax                | 下冲程最大电流     | NUMBER(8,2)   | A           |
| 76       | iratio                        | 电流比             | NUMBER(8,2)   |             |
| 77       | idegreebalancealarmlevel      | 电流平衡报警级别   | NUMBER(3)     |             |
| 78       | wattdegreebalance             | 功率平衡度         | NUMBER(8,2)   | %           |
| 79       | wattdegreebalancename         | 功率平衡状态       | VARCHAR2(200) |             |
| 80       | upstrokewattmax               | 上冲程最大功率     | NUMBER(8,2)   | kW          |
| 81       | downstrokewattmax             | 下冲程最大功率     | NUMBER(8,2)   | kW          |
| 82       | wattratio                     | 功率比             | NUMBER(8,2)   |             |
| 83       | wattdegreebalancealarmlevel   | 功率平衡报警级别   | NUMBER(3)     |             |
| 84       | deltaradius                   | 曲柄平衡移动距离   | NUMBER(8,2)   | cm          |
| 85       | pumpeff1                      | 冲程损失系数       | NUMBER(12,3)  | 小数        |
| 86       | pumpeff2                      | 充满系数           | NUMBER(12,3)  | 小数        |
| 87       | pumpeff3                      | 间隙漏失系数       | NUMBER(12,3)  | 小数        |
| 88       | pumpeff4                      | 液体收缩系数       | NUMBER(12,3)  | 小数        |
| 89       | pumpeff                       | 总泵效             | NUMBER(12,3)  | 小数        |
| 90       | rodflexlength                 | 抽油杆伸长量       | NUMBER(8,2)   | m           |
| 91       | tubingflexlength              | 油管伸缩值         | NUMBER(8,2)   | m           |
| 92       | inertialength                 | 惯性载荷增量       | NUMBER(8,2)   | m           |
| 93       | pumpintakep                   | 泵入口压力         | NUMBER(8,2)   | MPa         |
| 94       | pumpintaket                   | 泵入口温度         | NUMBER(8,2)   | ℃           |
| 95       | pumpintakegol                 | 泵入口就地气液比   | NUMBER(8,2)   | m^3/m^3     |
| 96       | pumpintakevisl                | 泵入口粘度         | NUMBER(8,2)   | mPa·s       |
| 97       | pumpintakebo                  | 泵入口原油体积系数 | NUMBER(8,2)   | 小数        |
| 98       | pumpoutletp                   | 泵出口压力         | NUMBER(8,2)   | MPa         |
| 99       | pumpoutlett                   | 泵出口温度         | NUMBER(8,2)   | ℃           |
| 100      | pumpoutletgol                 | 泵出口就地气液比   | NUMBER(8,2)   | m^3/m^3     |
| 101      | pumpoutletvisl                | 泵出口粘度         | NUMBER(8,2)   | mPa·s       |
| 102      | pumpoutletbo                  | 泵出口原油体积系数 | NUMBER(8,2)   | 小数        |
| 103      | videourl                      | 视频路径           | VARCHAR2(400) |             |
| 104      | org_id                        | 组织标号           | NUMBER(10)    |             |
| 105      | org_code                      | 组织代码           | VARCHAR2(20)  |             |
| 106      | sortnum                       | 排序编号           | NUMBER(10)    |             |

### 2.2.7 viw_rpc_diagram_hist 抽油机曲线数据历史视图

同viw_rpc_diagram_latest

### 2.2.8 viw_rpc_discrete_latest 抽油机离散数据实时视图

| **序号** | **代码**                    | **名称**           | **类型**       | **单位** |
|----------|-----------------------------|--------------------|----------------|----------|
| 1        | id                          | 记录编号           | NUMBER(10)     |          |
| 2        | wellname                    | 井名               | VARCHAR2(200)  |          |
| 3        | liftingtype                 | 举升类型           | NUMBER(10)     |          |
| 4        | liftingtypename             | 举升类型名称       | VARCHAR2(200)  |          |
| 5        | wellid                      | 井编号             | NUMBER(10)     |          |
| 6        | driveraddr                  | 设备地址           | VARCHAR2(200)  |          |
| 7        | commstatus                  | 通信状态           | NUMBER(1)      |          |
| 8        | commstatusname              | 通信状态名称       | VARCHAR2       |          |
| 9        | commalarmlevel              | 通信状态报警级别   | NUMBER(4)      |          |
| 10       | runstatus                   | 运行状态           | NUMBER(1)      |          |
| 11       | runstatusname               | 运行状态名称       | VARCHAR2       |          |
| 12       | runalarmlevel               | 运行状态报警级别   | NUMBER(3)      |          |
| 13       | commtime                    | 在线时间           | NUMBER(8,2)    | h        |
| 14       | commrange                   | 在线区间           | VARCHAR2(2000) |          |
| 15       | commtimeefficiency          | 在线时率           | NUMBER(10,4)   |          |
| 16       | commtimeefficiencylevel     | 在线时率级别       | VARCHAR2(50)   |          |
| 17       | runtime                     | 运行时间           | NUMBER(8,2)    | h        |
| 18       | runrange                    | 运行区间           | VARCHAR2(2000) |          |
| 19       | runtimeefficiency           | 运行时率           | NUMBER(10,4)   |          |
| 20       | runtimeefficiencylevel      | 运行时率级别       | VARCHAR2(50)   |          |
| 21       | acquisitiontime             | 采集时间           | DATE           |          |
| 22       | acqcycle_diagram            | 功图采集间隔       | NUMBER(6)      | min      |
| 23       | acqcycle_discrete           | 离散数据采集间隔   | NUMBER(10)     | min      |
| 24       | workingconditioncode_elec   | 电参工况代码       | NUMBER(4)      |          |
| 25       | workingconditionstring_elec | 电参工况累计字符串 | VARCHAR2(4000) |          |
| 26       | workingconditionname_elec   | 电参工况名称       | VARCHAR2(200)  |          |
| 27       | optimizationsuggestion_elec | 电参工况优化建议   | VARCHAR2(200)  |          |
| 28       | workingconditionalarmlevel  | 电参工况报警级别   | NUMBER(3)      |          |
| 29       | todaywattenergy             | 日有功功耗         | NUMBER(10,2)   | kW·h     |
| 30       | todaywattenergylevel        | 日有功功耗级别     | VARCHAR2(50)   |          |
| 31       | todaypwattenergy            | 日正向有功功耗     | NUMBER(10,2)   | kW·h     |
| 32       | todaynwattenergy            | 日反向有功功耗     | NUMBER(10,2)   | kW·h     |
| 33       | todayvarenergy              | 日无功功耗         | NUMBER(10,2)   | kVar·h   |
| 34       | todaypvarenergy             | 日正向无功功耗     | NUMBER(10,2)   | kVar·h   |
| 35       | todaynvarenergy             | 日反向无功功耗     | NUMBER(10,2)   | kVar·h   |
| 36       | todayvaenergy               | 日视在功耗         | NUMBER(10,2)   | kVA·h    |
| 37       | ia                          | A相电流            | NUMBER(8,2)    | A        |
| 38       | ib                          | B相电流            | NUMBER(8,2)    | A        |
| 39       | ic                          | C相电流            | NUMBER(8,2)    | A        |
| 40       | iavg                        | 三相平均电流       | NUMBER(8,2)    | A        |
| 41       | istr                        | 电流字符串         | VARCHAR2       |          |
| 42       | iauplimit                   | A相电流上限        | NUMBER(10,2)   | A        |
| 43       | iadownlimit                 | A相电流下限        | NUMBER(10,2)   | A        |
| 44       | iazero                      | A相电流零值        | NUMBER(8,2)    | A        |
| 45       | ibuplimit                   | B相电流上限        | NUMBER(10,2)   | A        |
| 46       | ibdownlimit                 | B相电流下限        | NUMBER(10,2)   | A        |
| 47       | ibzero                      | B相电流零值        | NUMBER(8,2)    | A        |
| 48       | icuplimit                   | C相电流上限        | NUMBER(10,2)   | A        |
| 49       | icdownlimit                 | C相电流下限        | NUMBER(10,2)   | A        |
| 50       | iczero                      | C相电流零值        | NUMBER(8,2)    | A        |
| 51       | wattuplimit                 | 有功功率上限       | NUMBER(8,2)    | kW       |
| 52       | wattdownlimit               | 有功功率下限       | NUMBER(8,2)    | kW       |
| 53       | iamax                       | A相电流最大值      | NUMBER(8,2)    | A        |
| 54       | iamin                       | A相电流最小值      | NUMBER(8,2)    | A        |
| 55       | ibmax                       | B相电流最大值      | NUMBER(8,2)    | A        |
| 56       | ibmin                       | B相电流最小值      | NUMBER(8,2)    | A        |
| 57       | icmax                       | C相电流最大值      | NUMBER(8,2)    | A        |
| 58       | icmin                       | C相电流最小值      | NUMBER(8,2)    | A        |
| 59       | va                          | A相电压            | NUMBER(8,2)    | V        |
| 60       | vb                          | B相电压            | NUMBER(8,2)    | V        |
| 61       | vc                          | C相电压            | NUMBER(8,2)    | V        |
| 62       | vavg                        | 三相平均电压       | NUMBER(8,2)    | V        |
| 63       | vstr                        | 电压字符串         | VARCHAR2       |          |
| 64       | vauplimit                   | A相电压上限        | NUMBER(10,2)   | V        |
| 65       | vadownlimit                 | A相电压下限        | NUMBER(10,2)   | V        |
| 66       | vazero                      | A相电压零值        | NUMBER(8,2)    | V        |
| 67       | vbuplimit                   | B相电压上限        | NUMBER(10,2)   | V        |
| 68       | vbdownlimit                 | B相电压下限        | NUMBER(10,2)   | V        |
| 69       | vbzero                      | B相电压零值        | NUMBER(8,2)    | V        |
| 70       | vcuplimit                   | C相电压上限        | NUMBER(10,2)   | V        |
| 71       | vcdownlimit                 | C相电压下限        | NUMBER(10,2)   | V        |
| 72       | vczero                      | C相电压零值        | NUMBER(8,2)    | V        |
| 73       | totalwattenergy             | 累计有功功耗       | NUMBER(10,2)   | kW·h     |
| 74       | totalpwattenergy            | 累计正向有功功耗   | NUMBER(10,2)   | kW·h     |
| 75       | totalnwattenergy            | 累计反向有功功耗   | NUMBER(10,2)   | kW·h     |
| 76       | totalvarenergy              | 累计无功功耗       | NUMBER(10,2)   | kVar·h   |
| 77       | totalpvarenergy             | 累计正向无功功耗   | NUMBER(10,2)   | kVar·h   |
| 78       | totalnvarenergy             | 累计反向无功功耗   | NUMBER(10,2)   | kVar·h   |
| 79       | totalvaenergy               | 累计视在功耗       | NUMBER(10,2)   | kVA·h    |
| 80       | watta                       | A相有功功率        | NUMBER(8,2)    | kW       |
| 81       | wattb                       | B相有功功率        | NUMBER(8,2)    | kW       |
| 82       | wattc                       | C相有功功率        | NUMBER(8,2)    | kW       |
| 83       | wattsum                     | 三相总有功功率     | NUMBER(8,2)    | kW       |
| 84       | wattstr                     | 有功功率字符串     | VARCHAR2       |          |
| 85       | vara                        | A相无功功率        | NUMBER(8,2)    | kVar     |
| 86       | varb                        | B相无功功率        | NUMBER(8,2)    | kVar     |
| 87       | varc                        | C相无功功率        | NUMBER(8,2)    | kVar     |
| 88       | varsum                      | 三相总无功功率     | NUMBER(8,2)    | kVar     |
| 89       | varstr                      | 无功功率字符串     | VARCHAR2       |          |
| 90       | reversepower                | 反向功率           | NUMBER(8,2)    |          |
| 91       | vaa                         | A相视在功率        | NUMBER(8,2)    | kVA      |
| 92       | vab                         | B相视在功率        | NUMBER(8,2)    | kVA      |
| 93       | vac                         | C相视在功率        | NUMBER(8,2)    | kVA      |
| 94       | vasum                       | 三相总视在功率     | NUMBER(8,2)    | kVA      |
| 95       | vastr                       | 视在功率字符串     | VARCHAR2       |          |
| 96       | pfa                         | A相功率因数        | NUMBER(8,2)    |          |
| 97       | pfb                         | B相功率因数        | NUMBER(8,2)    |          |
| 98       | pfc                         | C相功率因数        | NUMBER(8,2)    |          |
| 99       | pfsum                       | 三相综合功率因数   | NUMBER(8,2)    |          |
| 100      | pfstr                       | 功率因数字符串     | VARCHAR2       |          |
| 101      | frequencysetvalue           | 设置频率           | NUMBER(8,2)    | HZ       |
| 102      | frequencyrunvalue           | 运行频率           | NUMBER(8,2)    | HZ       |
| 103      | tubingpressure              | 油压               | NUMBER(8,2)    | MPa      |
| 104      | casingpressure              | 套压               | NUMBER(8,2)    | MPa      |
| 105      | backpressure                | 回压               | NUMBER(8,2)    | MPa      |
| 106      | wellheadfluidtemperature    | 井口油温           | NUMBER(8,2)    | ℃       |
| 107      | signal                      | 信号强度           | NUMBER(8,2)    |          |
| 108      | interval                    | 传输间隔           | NUMBER(10)     |          |
| 109      | devicever                   | 设备版本           | VARCHAR2(50)   |          |
| 110      | videourl                    | 视频路径           | VARCHAR2(400)  |          |
| 111      | sortnum                     | 排序编号           | NUMBER(10)     |          |
| 112      | org_code                    | 组织代码           | VARCHAR2(20)   |          |
| 113      | org_id                      | 组织编号           | NUMBER(10)     |          |

### 2.2.9 viw_rpc_discrete_hist 抽油机离散数据历史视图

同 viw_rpc_discrete_latest

### 2.2.10 viw_rpc_comprehensive_latest 抽油机综合数据实时视图

| **序号** | **代码**                      | **名称**                     | **类型**       | **单位**    |
|----------|-------------------------------|------------------------------|----------------|-------------|
| 1        | id                            | 记录编号                     | NUMBER(10)     |             |
| 2        | wellname                      | 井名                         | VARCHAR2(200)  |             |
| 3        | wellid                        | 井编号                       | NUMBER(10)     |             |
| 4        | liftingtype                   | 举升类型                     | NUMBER(10)     |             |
| 5        | acquisitiontime               | 采集时间                     | DATE           |             |
| 6        | acquisitiontime_d             | 离散数据采集时间             | DATE           |             |
| 7        | commstatus                    | 通信状态                     | NUMBER(2)      |             |
| 8        | commstatusname                | 通信状态名称                 | VARCHAR2       |             |
| 9        | commalarmlevel                | 通信状态报警级别             | NUMBER(3)      |             |
| 10       | runstatus                     | 运行状态                     | NUMBER(1)      |             |
| 11       | runstatusname                 | 运行状态名称                 | VARCHAR2       |             |
| 12       | runalarmlevel                 | 运行状态报警级别             | NUMBER(3)      |             |
| 13       | commtime                      | 在线时间                     | NUMBER(8,2)    | h           |
| 14       | commrange                     | 在线区间                     | VARCHAR2(2000) |             |
| 15       | commtimeefficiency            | 在线时率                     | NUMBER(10,4)   |             |
| 16       | commtimeefficiencylevel       | 在线时率级别                 | VARCHAR2(50)   |             |
| 17       | runtime                       | 运行时间                     | NUMBER(8,2)    | h           |
| 18       | runrange                      | 运行区间                     | VARCHAR2(2000) |             |
| 19       | runtimeefficiency             | 运行时率                     | NUMBER(10,4)   |             |
| 20       | runtimeefficiencylevel        | 运行时率级别                 | VARCHAR2(50)   |             |
| 21       | workingconditioncode          | 功图工况代码                 | NUMBER(4)      |             |
| 22       | workingconditionname          | 功图工况名称                 | VARCHAR2(200)  |             |
| 23       | optimizationsuggestion        | 优化建议                     | VARCHAR2(200)  |             |
| 24       | workingconditionalarmlevel    | 功图工况报警级别             | VARCHAR2       |             |
| 25       | workingconditioncode_e        | 电参工况代码                 | NUMBER(4)      |             |
| 26       | workingconditionstring_e      | 电参工况字符串               | VARCHAR2(4000) |             |
| 27       | workingconditionname_e        | 电参工况名称                 | VARCHAR2(200)  |             |
| 28       | workingconditionalarmlevel_e  | 电参工况报警级别             | NUMBER(3)      |             |
| 29       | theoreticalproduction         | 理论排量                     | NUMBER(8,2)    | m^3/d       |
| 30       | liquidweightproduction        | 产液量吨                     | NUMBER(8,2)    | t/d         |
| 31       | oilweightproduction           | 产油量吨                     | NUMBER(8,2)    | t/d         |
| 32       | waterweightproduction         | 产水量吨                     | NUMBER(8,2)    | t/d         |
| 33       | watercut_w                    | 重量含水率                   | NUMBER(8,2)    | %           |
| 34       | liquidweightproductionlevel   | 产液级别吨                   | VARCHAR2(50)   |             |
| 35       | liquidvolumetricproduction    | 产液量方                     | NUMBER(8,2)    | m^3/d       |
| 36       | oilvolumetricproduction       | 产油量方                     | NUMBER(8,2)    | m^3/d       |
| 37       | watervolumetricproduction     | 产水量方                     | NUMBER(8,2)    | m^3/d       |
| 38       | watercut                      | 体积含水率                   | NUMBER(8,2)    | %           |
| 39       | liquidvolumeproductionlevel   | 产液级别方                   | VARCHAR2(50)   |             |
| 40       | productiongasoilratio         | 生产气油比                   | NUMBER(8,2)    | m^3/t       |
| 41       | tubingpressure                | 油压                         | NUMBER(8,2)    | MPa         |
| 42       | casingpressure                | 套压                         | NUMBER(8,2)    | MPa         |
| 43       | wellheadfluidtemperature      | 井口油温                     | NUMBER(8,2)    | ℃           |
| 44       | producingfluidlevel           | 动液面                       | NUMBER(8,2)    | m           |
| 45       | levelcorrectvalue             | 液面反演校正值               | NUMBER(8,2)    | m           |
| 46       | pumpsettingdepth              | 泵挂                         | NUMBER(8,2)    | m           |
| 47       | submergence                   | 沉没度                       | NUMBER(8,2)    | m           |
| 48       | pumpborediameter              | 泵径                         | NUMBER(8,2)    | mm          |
| 49       | crudeoildensity               | 原油密度                     | NUMBER(16,2)   | g/cm^3      |
| 50       | netgrossratio                 | 净毛比                       | NUMBER(8,2)    |             |
| 51       | availableplungerstrokeprod    | 柱塞有效冲程产量吨           | NUMBER(8,2)    | t/d         |
| 52       | pumpclearanceleakprod         | 泵间隙漏失量吨               | NUMBER(8,2)    | t/d         |
| 53       | tvleakweightproduction        | 游动凡尔漏失量吨             | NUMBER(8,2)    | t/d         |
| 54       | svleakweightproduction        | 固定凡尔漏失量吨             | NUMBER(8,2)    | t/d         |
| 55       | gasinfluenceprod              | 气影响吨                     | NUMBER(8,2)    | t/d         |
| 56       | availableplungerstrokeprod_v  | 柱塞有效冲程产量方           | NUMBER(8,2)    | m^3/d       |
| 57       | pumpclearanceleakprod_v       | 泵间隙漏失量方               | NUMBER(8,2)    | m^3/d       |
| 58       | tvleakvolumetricproduction    | 游动凡尔漏失量方             | NUMBER(8,2)    | m^3/d       |
| 59       | svleakvolumetricproduction    | 固定凡尔漏失量方             | NUMBER(8,2)    | m^3/d       |
| 60       | gasinfluenceprod_v            | 气影响方                     | NUMBER(8,2)    | m^3/d       |
| 61       | rodstring                     | 抽油杆数据                   | VARCHAR2(200)  |             |
| 62       | stroke                        | 冲程                         | NUMBER(8,2)    | m           |
| 63       | spm                           | 冲次                         | NUMBER(8,2)    | 次/min      |
| 64       | upperloadline                 | 理论上载荷                   | NUMBER(8,2)    | kN          |
| 65       | upperloadlineofexact          | 真实理论上载荷               | NUMBER(8,2)    | kN          |
| 66       | lowerloadline                 | 理论下载荷                   | NUMBER(8,2)    | kN          |
| 67       | deltaloadline                 | 理论液柱载荷                 | NUMBER(8,2)    | kN          |
| 68       | fmax                          | 最大载荷                     | NUMBER(8,2)    | kN          |
| 69       | fmin                          | 最小载荷                     | NUMBER(8,2)    | kN          |
| 70       | deltaf                        | 载荷差                       | NUMBER(8,2)    | kN          |
| 71       | fullnesscoefficient           | 充满系数                     | NUMBER(8,2)    | 小数        |
| 72       | noliquidfullnesscoefficient   | 抽空充满系数                 | NUMBER(10,4)   | 小数        |
| 73       | plungerstroke                 | 柱塞冲程                     | NUMBER(8,2)    | m           |
| 74       | availableplungerstroke        | 柱塞有效冲程                 | NUMBER(8,2)    | m           |
| 75       | noliquidavailableplungerstroke| 抽空柱塞有效冲程             | NUMBER(10,4)   | m           |
| 76       | motorinputactivepower         | 电机输入有功功率             | NUMBER(8,2)    | kW          |
| 77       | polishrodpower                | 光杆功率                     | NUMBER(8,2)    | kW          |
| 78       | waterpower                    | 水功率                       | NUMBER(8,2)    | kW          |
| 79       | systemefficiency              | 系统效率                     | NUMBER(12,3)   | 小数        |
| 80       | systemefficiencylevel         | 系统效率级别                 | VARCHAR2(50)   |             |
| 81       | surfacesystemefficiency       | 地面效率                     | NUMBER(12,3)   | 小数        |
| 82       | surfacesystemefficiencylevel  | 地面效率级别                 | VARCHAR2(50)   |             |
| 83       | welldownsystemefficiency      | 井下效率                     | NUMBER(12,3)   | 小数        |
| 84       | welldownsystemefficiencylevel | 井下效率级别                 | VARCHAR2(50)   |             |
| 85       | fsdiagramarea                 | 功图面积                     | NUMBER(8,2)    |             |
| 86       | powerconsumptionperthm        | 吨液百米耗电量               | NUMBER(8,2)    | kW·h/100m·t |
| 87       | idegreebalance                | 电流平衡度                   | NUMBER(8,2)    | %           |
| 88       | idegreebalancename            | 电流平衡状态                 | VARCHAR2(200)  |             |
| 89       | upstrokeimax                  | 上冲程最大电流               | NUMBER(8,2)    | A           |
| 90       | downstrokeimax                | 下冲程最大电流               | NUMBER(8,2)    | A           |
| 91       | iratio                        | 电流比                       | VARCHAR2       |             |
| 92       | idegreebalancealarmlevel      | 电流平衡报警级别             | NUMBER(4)      |             |
| 93       | wattdegreebalance             | 功率平衡度                   | NUMBER(8,2)    | %           |
| 94       | wattdegreebalancename         | 功率平衡状态                 | VARCHAR2(200)  |             |
| 95       | upstrokewattmax               | 上冲程最大功率               | NUMBER(8,2)    | kW          |
| 96       | downstrokewattmax             | 下冲程最大功率               | NUMBER(8,2)    | kW          |
| 97       | wattratio                     | 功率比                       | VARCHAR2       |             |
| 98       | wattdegreebalancealarmlevel   | 功率平衡报警级别             | NUMBER(4)      |             |
| 99       | deltaradius                   | 曲柄平衡移动距离             | NUMBER(8,2)    | cm          |
| 100      | pumpeff1                      | 冲程损失系数                 | NUMBER(8,2)    | 小数        |
| 101      | pumpeff2                      | 充满系数                     | NUMBER(8,2)    | 小数        |
| 102      | pumpeff3                      | 间隙漏失系数                 | NUMBER(8,2)    | 小数        |
| 103      | pumpeff4                      | 液体收缩系数                 | NUMBER(8,2)    | 小数        |
| 104      | pumpeff                       | 总泵效                       | NUMBER(8,2)    | 小数        |
| 105      | rodflexlength                 | 抽油杆伸长量                 | NUMBER(8,2)    | m           |
| 106      | tubingflexlength              | 油管伸缩值                   | NUMBER(8,2)    | m           |
| 107      | inertialength                 | 惯性载荷增量                 | NUMBER(8,2)    | m           |
| 108      | pumpintakep                   | 泵入口压力                   | NUMBER(8,2)    | MPa         |
| 109      | pumpintaket                   | 泵入口温度                   | NUMBER(8,2)    | ℃           |
| 110      | pumpintakegol                 | 泵入口就地气液比             | NUMBER(8,2)    | m^3/m^3     |
| 111      | pumpintakevisl                | 泵入口粘度                   | NUMBER(8,2)    | mPa·s       |
| 112      | pumpintakebo                  | 泵入口原油体积系数           | NUMBER(8,2)    | 小数        |
| 113      | pumpoutletp                   | 泵出口压力                   | NUMBER(8,2)    | MPa         |
| 114      | pumpoutlett                   | 泵出口温度                   | NUMBER(8,2)    | ℃           |
| 115      | pumpoutletgol                 | 泵出口就地气液比             | NUMBER(8,2)    | m^3/m^3     |
| 116      | pumpoutletvisl                | 泵出口粘度                   | NUMBER(8,2)    | mPa·s       |
| 117      | pumpoutletbo                  | 泵出口原油体积系数           | NUMBER(8,2)    | 小数        |
| 118      | acqcycle_diagram              | 功图采集间隔                 | NUMBER(6)      | min         |
| 119      | acqcycle_discrete             | 离散数据采集间隔             | NUMBER(10)     | min         |
| 120      | todaywattenergy               | 日有功功耗                   | NUMBER(10,2)   | kW·h        |
| 121      | todaywattenergylevel          | 日有功功耗级别               | VARCHAR2(50)   |             |
| 122      | todaypwattenergy              | 日正向有功功耗               | NUMBER(10,2)   | kW·h        |
| 123      | todaynwattenergy              | 日反向有功功耗               | NUMBER(10,2)   | kW·h        |
| 124      | todayvarenergy                | 日无功功耗                   | NUMBER(10,2)   | kVar·h      |
| 125      | todaypvarenergy               | 日正向无功功耗               | NUMBER(10,2)   | kVar·h      |
| 126      | todaynvarenergy               | 日反向无功功耗               | NUMBER(10,2)   | kVar·h      |
| 127      | todayvaenergy                 | 日视在功耗                   | NUMBER(10,2)   | kVA·h       |
| 128      | ia                            | A相电流                      | NUMBER(8,2)    | A           |
| 129      | ib                            | B相电流                      | NUMBER(8,2)    | A           |
| 130      | ic                            | C相电流                      | NUMBER(8,2)    | A           |
| 131      | iavg                          | 三相平均电流                 | NUMBER(8,2)    | A           |
| 132      | istr                          | 电流字符串                   | VARCHAR2       |             |
| 133      | iauplimit                     | A相电流上限                  | NUMBER(10,2)   | A           |
| 134      | iadownlimit                   | A相电流下限                  | NUMBER(10,2)   | A           |
| 135      | iazero                        | A相电流零值                  | NUMBER(8,2)    | A           |
| 136      | ibuplimit                     | B相电流上限                  | NUMBER(10,2)   | A           |
| 137      | ibdownlimit                   | B相电流下限                  | NUMBER(10,2)   | A           |
| 138      | ibzero                        | B相电流零值                  | NUMBER(8,2)    | A           |
| 139      | icuplimit                     | C相电流上限                  | NUMBER(10,2)   | A           |
| 140      | icdownlimit                   | C相电流下限                  | NUMBER(10,2)   | A           |
| 141      | iczero                        | C相电流零值                  | NUMBER(8,2)    | A           |
| 142      | wattuplimit                   | 有功功率上限                 | NUMBER(8,2)    | kW          |
| 143      | wattdownlimit                 | 有功功率下限                 | NUMBER(8,2)    | kW          |
| 144      | iamax                         | A相电流最大值                | NUMBER(8,2)    | A           |
| 145      | iamin                         | A相电流最小值                | NUMBER(8,2)    | A           |
| 146      | ibmax                         | B相电流最大值                | NUMBER(8,2)    | A           |
| 147      | ibmin                         | B相电流最小值                | NUMBER(8,2)    | A           |
| 148      | icmax                         | C相电流最大值                | NUMBER(8,2)    | A           |
| 149      | icmin                         | C相电流最小值                | NUMBER(8,2)    | A           |
| 150      | va                            | A相电压                      | NUMBER(8,2)    | V           |
| 151      | vb                            | B相电压                      | NUMBER(8,2)    | V           |
| 152      | vc                            | C相电压                      | NUMBER(8,2)    | V           |
| 153      | vavg                          | 三相平均电压                 | NUMBER(8,2)    | V           |
| 154      | vstr                          | 电压字符串                   | VARCHAR2       |             |
| 155      | vauplimit                     | A相电压上限                  | NUMBER(10,2)   | V           |
| 156      | vadownlimit                   | A相电压下限                  | NUMBER(10,2)   | V           |
| 157      | vazero                        | A相电压零值                  | NUMBER(8,2)    | V           |
| 158      | vbuplimit                     | B相电压上限                  | NUMBER(10,2)   | V           |
| 159      | vbdownlimit                   | B相电压下限                  | NUMBER(10,2)   | V           |
| 160      | vbzero                        | B相电压零值                  | NUMBER(8,2)    | V           |
| 161      | vcuplimit                     | C相电压上限                  | NUMBER(10,2)   | V           |
| 162      | vcdownlimit                   | C相电压下限                  | NUMBER(10,2)   | V           |
| 163      | vczero                        | C相电压零值                  | NUMBER(8,2)    | V           |
| 164      | totalwattenergy               | 累计有功功耗                 | NUMBER(10,2)   | kW·h        |
| 165      | totalpwattenergy              | 累计正向有功功耗             | NUMBER(10,2)   | kW·h        |
| 166      | totalnwattenergy              | 累计反向有功功耗             | NUMBER(10,2)   | kW·h        |
| 167      | totalvarenergy                | 累计无功功耗                 | NUMBER(10,2)   | kVar·h      |
| 168      | totalpvarenergy               | 累计正向无功功耗             | NUMBER(10,2)   | kVar·h      |
| 169      | totalnvarenergy               | 累计反向无功功耗             | NUMBER(10,2)   | kVar·h      |
| 170      | totalvaenergy                 | 累计视在功耗                 | NUMBER(10,2)   | kVA·h       |
| 171      | watta                         | A相有功功率                  | NUMBER(8,2)    | kW          |
| 172      | wattb                         | B相有功功率                  | NUMBER(8,2)    | kW          |
| 173      | wattc                         | C相有功功率                  | NUMBER(8,2)    | kW          |
| 174      | wattsum                       | 三相总有功功率               | NUMBER(8,2)    | kW          |
| 175      | wattstr                       | 有功功率字符串               | VARCHAR2       |             |
| 176      | vara                          | A相无功功率                  | NUMBER(8,2)    | kVar        |
| 177      | varb                          | B相无功功率                  | NUMBER(8,2)    | kVar        |
| 178      | varc                          | C相无功功率                  | NUMBER(8,2)    | kVar        |
| 179      | varsum                        | 三相总无功功率               | NUMBER(8,2)    | kVar        |
| 180      | varstr                        | 无功功率字符串               | VARCHAR2       |             |
| 181      | reversepower                  | 反向功率                     | NUMBER(8,2)    |             |
| 182      | vaa                           | A相视在功率                  | NUMBER(8,2)    | kVA         |
| 183      | vab                           | B相视在功率                  | NUMBER(8,2)    | kVA         |
| 184      | vac                           | C相视在功率                  | NUMBER(8,2)    | kVA         |
| 185      | vasum                         | 三相总视在功率               | NUMBER(8,2)    | kVA         |
| 186      | vastr                         | 视在功率字符串               | VARCHAR2       |             |
| 187      | pfa                           | A相功率因数                  | NUMBER(8,2)    |             |
| 188      | pfb                           | B相功率因数                  | NUMBER(8,2)    |             |
| 189      | pfc                           | C相功率因数                  | NUMBER(8,2)    |             |
| 190      | pfsum                         | 三相综合功率因数             | NUMBER(8,2)    |             |
| 191      | pfstr                         | 功率因数字符串               | VARCHAR2       |             |
| 192      | frequencysetvalue             | 设置频率                     | NUMBER(8,2)    | HZ          |
| 193      | frequencyrunvalue             | 运行频率                     | NUMBER(8,2)    | HZ          |
| 194      | signal                        | 信号强度                     | NUMBER(8,2)    |             |
| 195      | interval                      | 传输间隔                     | NUMBER(10)     |             |
| 196      | devicever                     | 设备版本                     | VARCHAR2(50)   |             |
| 197      | balancecontrolmode            | 平衡远程调节远程触发控制     | NUMBER(10)     |             |
| 198      | balancecalculatemode          | 平衡计算方式                 | NUMBER(10)     |             |
| 199      | balanceawaytime               | 重心远离支点调节时间         | NUMBER(10)     | ms          |
| 200      | balanceclosetime              | 重心接近支点调节时间         | NUMBER(10)     | ms          |
| 201      | balanceawaytimeperbeat        | 重心远离支点每拍调节时间     | NUMBER(10)     | ms          |
| 202      | balanceclosetimeperbeat       | 重心接近支点每拍调节时间     | NUMBER(10)     | ms          |
| 203      | balancestrokecount            | 参与平衡度计算的冲程测量次数 | NUMBER(10)     |             |
| 204      | balanceoperationuplimit       | 平衡调节上限                 | NUMBER(10)     | %           |
| 205      | balanceoperationdownlimit     | 平衡调节下限                 | NUMBER(10)     | %           |
| 206      | balanceautocontrol            | 平衡远程自动调节             | NUMBER(1)      |             |
| 207      | spmautocontrol                | 冲次远程自动调节             | NUMBER(1)      |             |
| 208      | balancefrontlimit             | 平衡前限位                   | NUMBER(1)      |             |
| 209      | balanceafterlimit             | 平衡后限位                   | NUMBER(1)      |             |
| 210      | videourl                      | 视频路径                     | VARCHAR2(400)  |             |
| 211      | org_id                        | 组织编号                     | NUMBER(10)     |             |
| 212      | org_code                      | 组织代码                     | VARCHAR2(20)   |             |
| 213      | sortnum                       | 排序编号                     | NUMBER(10)     |             |

### 2.2.11 viw_rpc_comprehensive_hist 抽油机综合数据历史视图

同 viw_rpc_comprehensive_latest

### 2.2.12 viw_rpc_diagramquery_latest 抽油机图形查询实时视图

| **序号** | **代码**                    | **名称**         | **类型**      | **单位** |
|----------|-----------------------------|------------------|---------------|----------|
| 1        | id                          | 记录编号         | NUMBER(10)    |          |
| 2        | wellname                    | 井名             | VARCHAR2(200) |          |
| 3        | acquisitiontime             | 采集时间         | DATE          |          |
| 4        | stroke                      | 冲程             | NUMBER(8,2)   | m        |
| 5        | spm                         | 冲次             | NUMBER(8,2)   | 次/min   |
| 6        | fmax                        | 最大载荷         | NUMBER(8,2)   | kN       |
| 7        | fmin                        | 最小载荷         | NUMBER(8,2)   | kN       |
| 8        | position_curve              | 位移曲线         | CLOB          |          |
| 9        | load_curve                  | 载荷曲线         | CLOB          |          |
| 10       | power_curve                 | 功率曲线         | CLOB          |          |
| 11       | current_curve               | 电流曲线         | CLOB          |          |
| 12       | rpm_curve                   | 电机转速曲线     | CLOB          |          |
| 13       | rawpower_curve              | 功率原始曲线     | CLOB          |          |
| 14       | rawcurrent_curve            | 电流原始曲线     | CLOB          |          |
| 15       | rawrpm_curve                | 电机转速原始曲线 | CLOB          |          |
| 16       | workingconditioncode        | 功图工况代码     | NUMBER(4)     |          |
| 17       | workingconditionname        | 功图工况名称     | VARCHAR2(200) |          |
| 18       | workingconditionalarmlevel  | 功图工况报警级别 |               |          |
| 19       | upstrokeimax                | 上冲程最大电流   | VARCHAR2(200) | A        |
| 20       | downstrokeimax              | 下冲程最大电流   | NUMBER(8,2)   | A        |
| 21       | idegreebalance              | 电流平衡度       | NUMBER(8,2)   | %        |
| 22       | idegreebalancelevel         | 电流平衡级别     | NUMBER(8,2)   |          |
| 23       | idegreebalancealarmlevel    | 电流平衡报警级别 | VARCHAR2(200) |          |
| 24       | upstrokewattmax             | 上冲程最大功率   | NUMBER(8,2)   | kW       |
| 25       | downstrokewattmax           | 下冲程最大功率   | NUMBER(8,2)   | kW       |
| 26       | wattdegreebalance           | 功率平衡度       | NUMBER(8,2)   | %        |
| 27       | wattdegreebalancelevel      | 功率平衡级别     | NUMBER(8,2)   |          |
| 28       | wattdegreebalancealarmlevel | 功率平衡报警级别 | VARCHAR2(200) |          |
| 29       | datasource                  | 数据来源         | NUMBER(1)     |          |
| 30       | upperloadline               | 理论上载荷线     | NUMBER(8,2)   | kN       |
| 31       | lowerloadline               | 理论下载荷线     | NUMBER(8,2)   | kN       |
| 32       | liquidweightproduction      | 产液量吨         | NUMBER(8,2)   | t/d      |
| 33       | liquidvolumetricproduction  | 产液量方         | NUMBER(8,2)   | m^3/d    |
| 34       | signal                      | 信号强度         | NUMBER(8,2)   |          |
| 35       | devicever                   | 设备版本         | VARCHAR2(50)  |          |
| 36       | interval                    | 传输间隔         | NUMBER(10)    |          |
| 37       | orgid                       | 组织编号         | NUMBER(10)    |          |
| 38       | sortnum                     | 排序编号         | NUMBER(10)    |          |

### 2.2.13 viw_rpc_diagramquery_hist 抽油机图形查询历史视图

同 viw_rpc_diagramquery_latest

### 2.2.14 viw_rpc_total_day 抽油机日累计数据视图

| **序号** | **代码**                      | **名称**           | **类型**       | **单位**    |
|----------|-------------------------------|--------------------|----------------|-------------|
| 1        | id                            | 记录编号           | NUMBER(10)     |             |
| 2        | wellname                      | 井名               | VARCHAR2(200)  |             |
| 3        | liftingtype                   | 举升类型           | NUMBER(10)     |             |
| 4        | liftingtypename               | 举升类型名称       | VARCHAR2(200)  |             |
| 5        | wellid                        | 井编号             | NUMBER(10)     |             |
| 6        | driveraddr                    | 设备地址           | VARCHAR2(200)  |             |
| 7        | calculatedate                 | 汇总日期           | DATE           |             |
| 8        | acquisitiondate               | 采集日期           | DATE           |             |
| 9        | commstatus                    | 通信状态           |                |             |
| 10       | commstatusname                | 通信名称           |                |             |
| 11       | commalarmlevel                | 通信状态报警级别   |                |             |
| 12       | runstatus                     | 运行状态           | NUMBER(2)      |             |
| 13       | runstatusname                 | 运行状态名称       |                |             |
| 14       | runalarmlevel                 | 运行状态报警级别   |                |             |
| 15       | commtime                      | 在线时间           | NUMBER(8,2)    | h           |
| 16       | commrange                     | 在线区间           | VARCHAR2(4000) |             |
| 17       | commtimeefficiency            | 在线时率           | NUMBER(12,3)   |             |
| 18       | commtimeefficiencylevel       | 在线时率级别       | VARCHAR2(50)   |             |
| 19       | runtime                       | 运行时间           | NUMBER(8,2)    | h           |
| 20       | runrange                      | 运行区间           | VARCHAR2(4000) |             |
| 21       | runtimeefficiency             | 运行时率           | NUMBER(12,3)   |             |
| 22       | runtimeefficiencylevel        | 运行时率级别       | VARCHAR2(50)   |             |
| 23       | workingconditioncode          | 功图工况代码       | NUMBER(4)      |             |
| 24       | workingconditionname          | 功图工况名称       | VARCHAR2(200)  |             |
| 25       | workingconditionstring        | 工况累计字符串     | VARCHAR2(4000) |             |
| 26       | optimizationsuggestion        | 优化建议           | VARCHAR2(200)  |             |
| 27       | workingconditionalarmlevel    | 功图工况报警级别   | NUMBER(3)      |             |
| 28       | workingconditioncode_e        | 电参工况代码       | NUMBER(4)      |             |
| 29       | workingconditionname_e        | 电参工况名称       | VARCHAR2(200)  |             |
| 30       | workingconditionstring_e      | 电参工况字符串     | VARCHAR2(4000) |             |
| 31       | workingconditionalarmlevel_e  | 电参工况报警级别   | NUMBER(3)      |             |
| 32       | liquidweightproduction        | 产液量吨           | NUMBER(8,2)    | t/d         |
| 33       | oilweightproduction           | 产油量吨           | NUMBER(8,2)    | t/d         |
| 34       | waterweightproduction         | 产水量吨           | NUMBER(8,2)    | t/d         |
| 35       | watercut_w                    | 重量含水率         | NUMBER(10,4)   | %           |
| 36       | liquidweightproductionlevel   | 产液级别吨         | VARCHAR2(50)   |             |
| 37       | liquidvolumetricproduction    | 产液量方           | NUMBER(8,2)    | m^3/d       |
| 38       | oilvolumetricproduction       | 产油量方           | NUMBER(8,2)    | m^3/d       |
| 39       | watervolumetricproduction     | 产水量方           | NUMBER(8,2)    | m^3/d       |
| 40       | watercut                      | 体积含水率         | NUMBER(8,2)    | %           |
| 41       | liquidvolumeproductionlevel   | 产液级别方         | VARCHAR2(50)   |             |
| 42       | extendeddays                  | 延用天数           | NUMBER(5)      |             |
| 43       | productiongasoilratio         | 生产气油比         | NUMBER(8,2)    | m^3/t       |
| 44       | tubingpressure                | 油压               | NUMBER(8,2)    | MPa         |
| 45       | casingpressure                | 套压               | NUMBER(8,2)    | MPa         |
| 46       | wellheadfluidtemperature      | 井口油温           | NUMBER(8,2)    | ℃          |
| 47       | stroke                        | 冲程               | NUMBER(8,2)    | m           |
| 48       | strokemax                     | 冲程最大值         | NUMBER(8,2)    | m           |
| 49       | strokemin                     | 冲程最小值         | NUMBER(8,2)    | m           |
| 50       | strokestr                     | 冲程字符串         | VARCHAR2       |             |
| 51       | spm                           | 冲次               | NUMBER(8,2)    | 次/min      |
| 52       | spmmax                        | 冲次最大值         | NUMBER(8,2)    | 次/min      |
| 53       | spmmin                        | 冲次最小值         | NUMBER(8,2)    | 次/min      |
| 54       | spmstr                        | 冲次字符串         | VARCHAR2       |             |
| 55       | f                             | 载荷               | NUMBER(8,2)    | kN          |
| 56       | fmax                          | 载荷最大值         | NUMBER(8,2)    | kN          |
| 57       | fmin                          | 载荷最小值         | NUMBER(8,2)    | kN          |
| 58       | fstr                          | 载荷字符串         | VARCHAR2       |             |
| 59       | plungerstroke                 | 柱塞冲程           | NUMBER(8,2)    | m           |
| 60       | availableplungerstroke        | 柱塞有效冲程       | NUMBER(8,2)    | m           |
| 61       | noliquidavailablestroke       | 抽空柱塞有效冲程   | NUMBER(10,4)   | m           |
| 62       | fullnesscoefficient           | 充满系数           | NUMBER(10,4)   | 小数        |
| 63       | noliquidfullnesscoefficient   | 抽空充满系数       | NUMBER(10,4)   | 小数        |
| 64       | pumpeff                       | 总泵效             | NUMBER(10,4)   | 小数        |
| 65       | pumpborediameter              | 泵径               | NUMBER(8,2)    | mm          |
| 66       | pumpsettingdepth              | 泵挂               | NUMBER(8,2)    | m           |
| 67       | producingfluidlevel           | 动液面             | NUMBER(8,2)    | m           |
| 68       | levelcorrectvalue             | 液面反演校正值     | NUMBER(8,2)    | MPa         |
| 69       | submergence                   | 沉没度             | NUMBER(8,2)    | m           |
| 70       | rpm                           | 转速               | NUMBER(8,2)    | r/min       |
| 71       | rpmmax                        | 转速最大值         | NUMBER(8,2)    | r/min       |
| 72       | rpmmin                        | 转速最小值         | NUMBER(8,2)    | r/min       |
| 73       | systemefficiency              | 系统效率           | NUMBER(10,4)   | 小数        |
| 74       | systemefficiencylevel         | 系统效率级别       | VARCHAR2(50)   |             |
| 75       | surfacesystemefficiency       | 地面效率           | NUMBER(10,4)   | 小数        |
| 76       | surfacesystemefficiencylevel  | 地面效率级别       | VARCHAR2(50)   |             |
| 77       | welldownsystemefficiency      | 井下效率           | NUMBER(10,4)   | 小数        |
| 78       | welldownsystemefficiencylevel | 井下效率级别       | VARCHAR2(50)   |             |
| 79       | powerconsumptionperthm        | 吨液百米耗电量     | NUMBER(8,2)    | kW·h/100m·t |
| 80       | todaywattenergy               | 日有功功耗         | NUMBER(10,2)   | kW·h        |
| 81       | todaywattenergylevel          | 日有功功耗级别     | VARCHAR2(50)   |             |
| 82       | todaypwattenergy              | 日正向有功功耗     | NUMBER(10,2)   | kW·h        |
| 83       | todaynwattenergy              | 日反向有功功耗     | NUMBER(10,2)   | kW·h        |
| 84       | todayvarenergy                | 日无功功耗         | NUMBER(10,2)   | kVar·h      |
| 85       | todaypvarenergy               | 日正向无功功耗     | NUMBER(10,2)   | kVar·h      |
| 86       | todaynvarenergy               | 日反向无功功耗     | NUMBER(10,2)   | kVar·h      |
| 87       | todayvaenergy                 | 日视在功耗         | NUMBER(10,2)   | kVA·h       |
| 88       | idegreebalance                | 电流平衡度         | NUMBER(8,2)    | %           |
| 89       | idegreebalancemax             | 电流平衡度最大值   | NUMBER(8,2)    | %           |
| 90       | idegreebalancemin             | 电流平衡度最小值   | NUMBER(8,2)    | %           |
| 91       | idegreebalancestr             | 电流平衡度字符串   | VARCHAR2       |             |
| 92       | idegreebalancelevel           | 电流平衡统计级别   | VARCHAR2(200)  |             |
| 93       | idegreebalancealarmlevel      | 电流平衡报警级别   | NUMBER(3)      |             |
| 94       | wattdegreebalance             | 功率平衡度         | NUMBER(8,2)    | %           |
| 95       | wattdegreebalancemax          | 功率平衡度最大值   | NUMBER(8,2)    | %           |
| 96       | wattdegreebalancemin          | 功率平衡度最小值   | NUMBER(8,2)    | %           |
| 97       | wattdegreebalancestr          | 功率平衡度字符串   | VARCHAR2       |             |
| 98       | wattdegreebalancelevel        | 功率平衡统计级别   | VARCHAR2(200)  |             |
| 99       | wattdegreebalancealarmlevel   | 功率平衡报警级别   | NUMBER(3)      |             |
| 100      | deltaradius                   | 曲柄平衡移动距离   | NUMBER(8,2)    | m           |
| 101      | deltaradiusmax                | 移动距离最大值     | NUMBER(8,2)    | m           |
| 102      | deltaradiusmin                | 移动距离最小值     | NUMBER(8,2)    | m           |
| 103      | ia                            | A相电流            | NUMBER(8,2)    | A           |
| 104      | iamax                         | A相电流最大值      | NUMBER(8,2)    | A           |
| 105      | iamin                         | A相电流最小值      | NUMBER(8,2)    | A           |
| 106      | iastr                         | A相电流字符串      | NUMBER(8,2)    |             |
| 107      | ib                            | B相电流            | NUMBER(8,2)    | A           |
| 108      | ibmax                         | B相电流最大值      | NUMBER(8,2)    | A           |
| 109      | ibmin                         | B相电流最小值      | NUMBER(8,2)    | A           |
| 110      | ibstr                         | B相电流字符串      | VARCHAR2       |             |
| 111      | ic                            | C相电流            | NUMBER(8,2)    | A           |
| 112      | icmax                         | C相电流最大值      | NUMBER(8,2)    | A           |
| 113      | icmin                         | C相电流最小值      | NUMBER(8,2)    | A           |
| 114      | icstr                         | C相电流字符串      | VARCHAR2       |             |
| 115      | va                            | A相电压            | NUMBER(8,2)    | V           |
| 116      | vamax                         | A相电压最大值      | NUMBER(8,2)    | V           |
| 117      | vamin                         | A相电压最小值      | NUMBER(8,2)    | V           |
| 118      | vastr                         | A相电压字符串      | VARCHAR2       |             |
| 119      | vb                            | B相电压            | NUMBER(8,2)    | V           |
| 120      | vbmax                         | B相电压最大值      | NUMBER(8,2)    | V           |
| 121      | vbmin                         | B相电压最小值      | NUMBER(8,2)    | V           |
| 122      | vbstr                         | B相电压字符串      | VARCHAR2       |             |
| 123      | vc                            | C相电压            | NUMBER(8,2)    | V           |
| 124      | vcmax                         | C相电压最大值      | NUMBER(8,2)    | V           |
| 125      | vcmin                         | C相电压最小值      | NUMBER(8,2)    | V           |
| 126      | vcstr                         | C相电压字符串      | VARCHAR2       |             |
| 127      | signal                        | 信号强度           | NUMBER(8,2)    |             |
| 128      | signalmax                     | 信号强度最大值     | NUMBER(8,2)    |             |
| 129      | signalmin                     | 信号强度最小值     | NUMBER(8,2)    |             |
| 130      | signalstr                     | 信号强度字符串     | VARCHAR2       |             |
| 131      | videourl                      | 视频路径           | VARCHAR2(400)  |             |
| 132      | sortnum                       | 排序编号           | NUMBER(10)     |             |
| 133      | org_code                      | 组织代码           | VARCHAR2(20)   |             |
| 134      | org_id                        | 组织编号           | NUMBER(10)     |             |
| 135      | remark                        | 备注               | VARCHAR2       |             |

### 2.1.15 viw_rpc_calculatemain 抽油机计算结果管理视图

| **序号** | **代码**                   | **名称**       | **类型**      | **单位** |
|----------|----------------------------|----------------|---------------|----------|
| 1        | id                         | 记录编号       | NUMBER(10)    |          |
| 2        | wellname                   | 井名           | VARCHAR2(200) |          |
| 3        | liftingtype                | 举升方式       | NUMBER(10)    |          |
| 4        | acquisitiontime            | 采集时间       | DATE          |          |
| 5        | workingconditionname       | 工况名称       | VARCHAR2(200) |          |
| 6        | liquidweightproduction     | 产液量吨       | NUMBER(8,2)   | t/d      |
| 7        | oilweightproduction        | 产油量吨       | NUMBER(8,2)   | t/d      |
| 8        | liquidvolumetricproduction | 产液量方       | NUMBER(8,2)   | m^3/d    |
| 9        | oilvolumetricproduction    | 产油量方       | NUMBER(8,2)   | m^3/d    |
| 10       | crudeoildensity            | 原油密度       | NUMBER(16,2)  | g/cm^3   |
| 11       | waterdensity               | 水密度         | NUMBER(16,2)  | g/cm^3   |
| 12       | naturalgasrelativedensity  | 天然气相对密度 | NUMBER(16,2)  |          |
| 13       | saturationpressure         | 饱和压力       | NUMBER(16,2)  | MPa      |
| 14       | reservoirdepth             | 油层中部深度   | NUMBER(16,2)  | m        |
| 15       | reservoirtemperature       | 油层中部温度   | NUMBER(16,2)  | ℃       |
| 16       | tubingpressure             | 油压           | NUMBER(8,2)   | MPa      |
| 17       | casingpressure             | 套压           | NUMBER(8,2)   | MPa      |
| 18       | wellheadfluidtemperature   | 井口温油       | NUMBER(8,2)   | ℃       |
| 19       | watercut                   | 体积含水率     | NUMBER(8,2)   | %        |
| 20       | productiongasoilratio      | 生产气油比     | NUMBER(8,2)   | m^3/t    |
| 21       | producingfluidlevel        | 动液面         | NUMBER(8,2)   | m        |
| 22       | pumpsettingdepth           | 泵挂           | NUMBER(8,2)   | m        |
| 23       | pumpgrade                  | 泵级别         | NUMBER(1)     |          |
| 24       | pumpborediameter           | 泵径           | NUMBER(8,2)   | mm       |
| 25       | plungerlength              | 柱塞长         | NUMBER(8,2)   | m        |
| 26       | tubingstringinsidediameter | 油管内径       | NUMBER(8,2)   | mm       |
| 27       | casingstringinsidediameter | 套管内径       | NUMBER(8,2)   | mm       |
| 28       | rodstring                  | 杆数据         | VARCHAR2(200) |          |
| 29       | anchoringstatename         | 锚定状态       | VARCHAR2(200) |          |
| 30       | netgrossratio              | 净毛比         | NUMBER(8,2)   |          |
| 31       | resultstatus               | 计算结果       | NUMBER(2)     |          |
| 32       | orgid                      | 组织编号       | NUMBER(10)    |          |

### 2.1.16 viw_pcp_productiondata_latest 螺杆泵生产数据实时视图 

| **序号** | **代码**                   | **名称**       | **类型**      | **单位** | 
|----------|----------------------------|----------------|---------------|----------|
| 1        | id                         | 记录编号       | NUMBER(10)    |          | 
| 2        | wellname                   | 井名           | VARCHAR2(200) |          | 
| 3        | wellid                     | 井编号         | NUMBER(10)    |          | 
| 4        | liftingtype                | 举升类型       | NUMBER(10)    |          | 
| 5        | acquisitiontime            | 采集时间       | DATE          |          | 
| 6        | runtime                    | 运行时间       | NUMBER(8,2)   | h        | 
| 7        | crudeoildensity            | 原油密度       | NUMBER(16,2)  | g/cm^3   | 
| 8        | waterdensity               | 水密度         | NUMBER(16,2)  | g/cm^3   | 
| 9        | naturalgasrelativedensity  | 天然气相对密度 | NUMBER(16,2)  |          | 
| 10       | saturationpressure         | 饱和压力       | NUMBER(16,2)  | MPa      | 
| 11       | reservoirdepth             | 油层中部深度   | NUMBER(16,2)  | m        | 
| 12       | reservoirtemperature       | 油层中部温度   | NUMBER(16,2)  | ℃       | 
| 13       | watercut_w                 | 重量含水率     | NUMBER(8,2)   | %        | 
| 14       | watercut                   | 体积含水率     | NUMBER(8,2)   | %        | 
| 15       | tubingpressure             | 油压           | NUMBER(8,2)   | MPa      | 
| 16       | casingpressure             | 套压           | NUMBER(8,2)   | MPa      | 
| 17       | backpressure               | 回压           | NUMBER(8,2)   | MPa      | 
| 18       | wellheadfluidtemperature   | 井口油温       | NUMBER(8,2)   | ℃       | 
| 19       | producingfluidlevel        | 动液面         | NUMBER(8,2)   | m        | 
| 20       | pumpsettingdepth           | 泵挂           | NUMBER(8,2)   | m        | 
| 21       | productiongasoilratio      | 生产气油比     | NUMBER(8,2)   | m^3/t    | 
| 22       | pumpborediameter           | 泵径           | NUMBER(8,2)   | mm       | 
| 23       | pumptype                   | 泵类型         | VARCHAR2(20)  |          |
| 24       | pumpgrade                  | 泵级别         | NUMBER(1)     |          | 
| 25       | plungerlength              | 柱塞长         | NUMBER(8,2)   | m        | 
| 26       | barreltype                 | 泵筒类型       | VARCHAR2(20)  |          |
| 27       | barrellength               | 泵筒长         | NUMBER(8,2)   | m        | 
| 28       | barrelseries               | 泵级数         | NUMBER(8,2)   |          | 
| 29       | rotordiameter              | 转子截面直径   | NUMBER(8,2)   | mm       | 
| 30       | qpr                        | 转速           | NUMBER(8,2)   | r/min    | 
| 31       | tubingstringinsidediameter | 油管内径       | NUMBER(8,2)   | mm       | 
| 32       | casingstringinsidediameter | 套管内径       | NUMBER(8,2)   | mm       | 
| 33       | rodstring                  | 杆数据         | VARCHAR2(200) |          | 
| 34       | anchoringstate             | 锚定状态       | NUMBER(1)     |          | 
| 35       | anchoringstatename         | 锚定状态名称   | VARCHAR2(200) |          | 
| 36       | netgrossratio              | 净毛比         | NUMBER(8,2)   |          | 
| 37       | manualintervention         | 人工干预代码   | NUMBER(4)     |          | 
| 38       | sortnum                    | 排序编号       | NUMBER(10)    |          | 
| 39       | org_id                     | 组织编号       | NUMBER(10)    |          | 
### 2.1.17 viw_pcp_productiondata_hist 螺杆泵生产数据历史视图

同viw_pcp_productiondata_latest

### 2.1.18 viw_pcp_rpm_latest 螺杆泵曲线数据实时视图 

| **序号** | **代码**                      | **名称**           | **类型**      | **单位**    | 
|----------|-------------------------------|--------------------|---------------|-------------|
| 1        | id                            | 记录编号           | NUMBER(10)    |             | 
| 2        | wellname                      | 井名               | VARCHAR2(200) |             | 
| 3        | wellid                        | 井编号             | NUMBER(10)    |             | 
| 4        | liftingtype                   | 举升类型           | NUMBER(10)    |             | 
| 5        | acquisitiontime               | 采集时间           | DATE          |             | 
| 6        | rpm                           | 转速               | NUMBER(8,2)   | r/min       | 
| 7        | torque                        | 扭矩               | NUMBER(8,2)   | kN·m        | 
| 8        | workingconditioncode          | 工况代码           | NUMBER(4)     |             | 
| 9        | workingconditionname          | 工况名称           | VARCHAR2(200) |             | 
| 10       | optimizationsuggestion        | 优化建议           | VARCHAR2(200) |             | 
| 11       | workingconditionrunalarmlevel | 工况报警级别       | NUMBER(3)     |             | 
| 12       | theoreticalproduction         | 理论排量           | NUMBER(8,2)   | m^3/d       | 
| 13       | liquidweightproduction        | 产液量吨           | NUMBER(8,2)   | t/d         |
| 14       | oilweightproduction           | 产油量吨           | NUMBER(8,2)   | t/d         |
| 15       | waterweightproduction         | 产水量吨           | NUMBER(8,2)   | t/d         |
| 16       | watercut_w                    | 重量含水率         | NUMBER(8,2)   | %           |
| 17       | liquidweightproductionlevel   | 产液级别吨         | VARCHAR2(50)  |             |
| 18       | liquidvolumetricproduction    | 产液量方           | NUMBER(8,2)   | m^3/d       |
| 19       | oilvolumetricproduction       | 产油量方           | NUMBER(8,2)   | m^3/d       |
| 20       | watervolumetricproduction     | 产水量方           | NUMBER(8,2)   | m^3/d       |
| 21       | watercut                      | 体积含水率         | NUMBER(8,2)   | %           |
| 22       | liquidvolumeproductionlevel   | 产液级别方         | VARCHAR2(50)  |             | 
| 23       | productiongasoilratio         | 生产气油比         | NUMBER(8,2)   | m^3/t       | 
| 24       | tubingpressure                | 油压               | NUMBER(8,2)   | MPa         | 
| 25       | casingpressure                | 套压               | NUMBER(8,2)   | MPa         | 
| 26       | wellheadfluidtemperature      | 井口油温           | NUMBER(8,2)   | ℃          | 
| 27       | qpr                           | 公称排量           | NUMBER(8,2)   | m^3/r       | 
| 28       | barrellength                  | 泵筒长             | NUMBER(8,2)   | m           | 
| 29       | barrelseries                  | 泵级数             | NUMBER(8,2)   |             | 
| 30       | rotordiameter                 | 转子截面直径       | NUMBER(8,2)   | mm          | 
| 31       | producingfluidlevel           | 动液面             | NUMBER(8,2)   | m           | 
| 32       | pumpsettingdepth              | 泵挂               | NUMBER(8,2)   | m           | 
| 33       | submergence                   | 沉没度             | NUMBER(8,2)   | m           | 
| 34       | pumpborediameter              | 泵径               | NUMBER(8,2)   | mm          | 
| 35       | crudeoildensity               | 原油密度           | NUMBER(16,2)  | g/cm^3      | 
| 36       | netgrossratio                 | 净毛比             | NUMBER(8,2)   |             | 
| 37       | rodstring                     | 抽油杆柱分析数据   | VARCHAR2(200) |             | 
| 38       | motorinputactivepower         | 电机输入有功功率   | NUMBER(8,2)   | kW          | 
| 39       | waterpower                    | 水功率             | NUMBER(8,2)   | kW          | 
| 40       | systemefficiency              | 系统效率           | NUMBER(12,3)  | 小数        | 
| 41       | systemefficiencylevel         | 系统效率级别       | VARCHAR2(50)  |             | 
| 42       | powerconsumptionperthm        | 吨液百米耗电量     | NUMBER(8,2)   | kW·h/100m·t | 
| 43       | pumpeff1                      | 容积效率           | NUMBER(12,3)  | 小数        | 
| 44       | pumpeff2                      | 液体收缩系数       | NUMBER(12,3)  | 小数        | 
| 45       | pumpeff                       | 泵效               | NUMBER(12,3)  | 小数        | 
| 46       | pumpintakep                   | 泵入口压力         | NUMBER(8,2)   | MPa         | 
| 47       | pumpintaket                   | 泵入口温度         | NUMBER(8,2)   | ℃          | 
| 48       | pumpintakegol                 | 泵入口就地气液比   | NUMBER(8,2)   | m^3/m^3     | 
| 49       | pumpintakevisl                | 泵入口粘度         | NUMBER(8,2)   | mPa·s       | 
| 50       | pumpintakebo                  | 泵入口原油体积系数 | NUMBER(8,2)   | 小数        | 
| 51       | pumpoutletp                   | 泵出口压力         | NUMBER(8,2)   | MPa         | 
| 52       | pumpoutlett                   | 泵出口温度         | NUMBER(8,2)   | ℃          | 
| 53       | pumpoutletgol                 | 泵出口就地气液比   | NUMBER(8,2)   | m^3/m^3     | 
| 54       | pumpoutletvisl                | 泵出口粘度         | NUMBER(8,2)   | mPa·s       | 
| 55       | pumpoutletbo                  | 泵出口原油体积系数 | NUMBER(8,2)   | 小数        | 
| 56       | videourl                      | 视频路径           | VARCHAR2(400) |             | 
| 57       | org_id                        | 组织标号           | NUMBER(10)    |             | 
| 58       | org_code                      | 组织代码           | VARCHAR2(20)  |             | 
| 59       | sortnum                       | 排序编号           | NUMBER(10)    |             | 

### 2.1.19 viw_pcp_rpm_hist 螺杆泵曲线数据历史视图

同viw_pcp_rpm_latest

### 2.1.20 viw_pcp_discrete_latest 螺杆泵离散数据实时视图

| **序号** | **代码**                    | **名称**           | **类型**       | **单位** | 
|----------|-----------------------------|--------------------|----------------|----------|
| 1        | id                          | 记录编号           | NUMBER(10)     |          | 
| 2        | wellname                    | 井名               | VARCHAR2(200)  |          | 
| 3        | liftingtype                 | 举升类型           | NUMBER(10)     |          | 
| 4        | liftingtypename             | 举升类型名称       | VARCHAR2(200)  |          | 
| 5        | wellid                      | 井编号             | NUMBER(10)     |          | 
| 6        | commstatus                  | 通信状态           | NUMBER(1)      |          | 
| 7        | commstatusname              | 通信状态名称       | VARCHAR2       |          | 
| 8        | commalarmlevel              | 通信状态报警级别   | NUMBER(4)      |          | 
| 9        | runstatus                   | 运行状态           | NUMBER(1)      |          | 
| 10       | runstatusname               | 运行状态名称       | VARCHAR2       |          | 
| 11       | runalarmlevel               | 运行状态报警级别   | NUMBER(3)      |          | 
| 12       | commtime                    | 在线时间           | NUMBER(8,2)    | h        | 
| 13       | commrange                   | 在线区间           | VARCHAR2(2000) |          | 
| 14       | commtimeefficiency          | 在线时率           | NUMBER(10,4)   |          | 
| 15       | commtimeefficiencylevel     | 在线时率级别       | VARCHAR2(50)   |          | 
| 16       | runtime                     | 运行时间           | NUMBER(8,2)    | h        | 
| 17       | runrange                    | 运行区间           | VARCHAR2(2000) |          | 
| 18       | runtimeefficiency           | 生产时率           | NUMBER(10,4)   |          | 
| 19       | runtimeefficiencylevel      | 生产时率级别       | VARCHAR2(50)   |          | 
| 20       | acquisitiontime             | 采集时间           | DATE           |          | 
| 21       | workingconditioncode_elec   | 电参工况代码       | NUMBER(4)      |          | 
| 22       | workingconditionstring_elec | 电参工况累计字符串 | VARCHAR2(4000) |          | 
| 23       | workingconditionname_elec   | 电参工况名称       | VARCHAR2(200)  |          | 
| 24       | optimizationsuggestion_elec | 电参工况优化建议   | VARCHAR2(200)  |          | 
| 25       | workingconditionalarmlevel  | 电参工况报警级别   | NUMBER(3)      |          | 
| 26       | todaywattenergy             | 日有功功耗         | NUMBER(8,2)    | kW·h     | 
| 27       | todaywattenergylevel        | 日耗电量级别       | VARCHAR2(50)   |          | 
| 28       | todaypwattenergy            | 日正向有功功耗     | NUMBER(8,2)    | kW·h     | 
| 29       | todaynwattenergy            | 日反向有功功耗     | NUMBER(8,2)    | kW·h     | 
| 30       | todayvarenergy              | 日无功功耗         | NUMBER(8,2)    | kVar·h   | 
| 31       | todaypvarenergy             | 日正向无功功耗     | NUMBER(8,2)    | kVar·h   | 
| 32       | todaynvarenergy             | 日反向无功功耗     | NUMBER(8,2)    | kVar·h   | 
| 33       | todayvaenergy               | 日视在功耗         | NUMBER(8,2)    | kVA·h    | 
| 34       | ia                          | A相电流            | NUMBER(8,2)    | A        | 
| 35       | ib                          | B相电流            | NUMBER(8,2)    | A        | 
| 36       | ic                          | C相电流            | NUMBER(8,2)    | A        | 
| 37       | iavg                        | 三项平均电流       | NUMBER(8,2)    | A        | 
| 38       | istr                        | 电流字符串         | VARCHAR2       |          | 
| 39       | iauplimit                   | A相电流上限        | NUMBER(8,2)    | A        | 
| 40       | iadownlimit                 | A相电流下限        | NUMBER(8,2)    | A        | 
| 41       | iazero                      | A相电流零值        | NUMBER(8,2)    | A        | 
| 42       | ibuplimit                   | B相电流上限        | NUMBER(8,2)    | A        | 
| 43       | ibdownlimit                 | B相电流下限        | NUMBER(8,2)    | A        | 
| 44       | ibzero                      | B相电流零值        | NUMBER(8,2)    | A        | 
| 45       | icuplimit                   | C相电流上限        | NUMBER(8,2)    | A        | 
| 46       | icdownlimit                 | C相电流下限        | NUMBER(8,2)    | A        | 
| 47       | iczero                      | C相电流零值        | NUMBER(8,2)    | A        | 
| 48       | va                          | A相电压            | NUMBER(8,2)    | V        | 
| 49       | vb                          | B相电压            | NUMBER(8,2)    | V        | 
| 50       | vc                          | C相电压            | NUMBER(8,2)    | V        | 
| 51       | vavg                        | 三项平均电压       | NUMBER(8,2)    | V        | 
| 52       | vstr                        | 电压字符串         | VARCHAR2       |          | 
| 53       | vauplimit                   | A相电压上限        | NUMBER(8,2)    | V        | 
| 54       | vadownlimit                 | A相电压下限        | NUMBER(8,2)    | V        | 
| 55       | vazero                      | A相电压零值        | NUMBER(8,2)    | V        | 
| 56       | vbuplimit                   | B相电压上限        | NUMBER(8,2)    | V        | 
| 57       | vbdownlimit                 | B相电压下限        | NUMBER(8,2)    | V        | 
| 58       | vbzero                      | B相电压零值        | NUMBER(8,2)    | V        | 
| 59       | vcuplimit                   | C相电压上限        | NUMBER(8,2)    | V        | 
| 60       | vcdownlimit                 | C相电压下限        | NUMBER(8,2)    | V        | 
| 61       | vczero                      | C相电压零值        | NUMBER(8,2)    | V        | 
| 62       | totalwattenergy             | 累计有功功耗       | NUMBER(8,2)    | kW·h     | 
| 63       | totalpwattenergy            | 累计正向有功功耗   | NUMBER(8,2)    | kW·h     | 
| 64       | totalnwattenergy            | 累计反向有功功耗   | NUMBER(8,2)    | kW·h     | 
| 65       | totalvarenergy              | 累计无功功耗       | NUMBER(8,2)    | kVar·h   | 
| 66       | totalpvarenergy             | 累计正向无功功耗   | NUMBER(8,2)    | kVar·h   | 
| 67       | totalnvarenergy             | 累计反向无功功耗   | NUMBER(8,2)    | kVar·h   | 
| 68       | totalvaenergy               | 累计视在功耗       | NUMBER(8,2)    | kVA·h    | 
| 69       | watta                       | A相有功功率        | NUMBER(8,2)    | kW       | 
| 70       | wattb                       | B相有功功率        | NUMBER(8,2)    | kW       | 
| 71       | wattc                       | C相有功功率        | NUMBER(8,2)    | kW       | 
| 72       | wattsum                     | 三相总有功功率     | NUMBER(8,2)    | kW       | 
| 73       | wattstr                     | 有功功率字符串     | VARCHAR2       |          | 
| 74       | vara                        | A相无功功率        | NUMBER(8,2)    | kVar     | 
| 75       | varb                        | B相无功功率        | NUMBER(8,2)    | kVar     | 
| 76       | varc                        | C相无功功率        | NUMBER(8,2)    | kVar     | 
| 77       | varsum                      | 三相总无功功率     | NUMBER(8,2)    | kVar     | 
| 78       | varstr                      | 无功功率字符串     | VARCHAR2       |          | 
| 79       | reversepower                | 反向功率           | NUMBER(8,2)    |          |
| 80       | vaa                         | A相视在功率        | NUMBER(8,2)    | kVA      |
| 81       | vab                         | B相视在功率        | NUMBER(8,2)    | kVA      |
| 82       | vac                         | C相视在功率        | NUMBER(8,2)    | kVA      |
| 83       | vasum                       | 三相总视在功率     | NUMBER(8,2)    | kVA      |
| 84       | vastr                       | 视在功率字符串     | VARCHAR2       |          | 
| 85       | pfa                         | A相功率因数        | NUMBER(8,2)    |          | 
| 86       | pfb                         | B相功率因数        | NUMBER(8,2)    |          | 
| 87       | pfc                         | C相功率因数        | NUMBER(8,2)    |          | 
| 88       | pfsum                       | 三相综合功率因数   | NUMBER(8,2)    |          | 
| 89       | pfstr                       | 功率因数字符串     | VARCHAR2       |          | 
| 90       | frequencysetvalue           | 设置频率           | NUMBER(8,2)    | HZ       | 
| 91       | frequencyrunvalue           | 运行频率           | NUMBER(8,2)    | HZ       | 
| 92       | tubingpressure              | 油压               | NUMBER(8,2)    | MPa      | 
| 93       | casingpressure              | 套压               | NUMBER(8,2)    | MPa      | 
| 94       | backpressure                | 回压               | NUMBER(8,2)    | MPa      | 
| 95       | wellheadfluidtemperature    | 井口油温           | NUMBER(8,2)    | ℃       | 
| 96       | signal                      | 信号强度           | NUMBER(8,2)    |          | 
| 97       | interval                    | 传输间隔           | NUMBER(10)     |          | 
| 98       | devicever                   | 设备版本           | VARCHAR2(50)   |          | 
| 99       | videourl                    | 视频路径           | VARCHAR2(400)  |          | 
| 100      | sortnum                     | 排序编号           | NUMBER(10)     |          | 
| 101      | org_code                    | 组织代码           | VARCHAR2(20)   |          | 
| 102      | org_id                      | 组织编号           | NUMBER(10)     |          | 

### 2.1.21 viw_pcp_discrete_hist 螺杆泵离散数据历史视图

同viw_pcp_discrete_latest

### 2.1.22 viw_pcp_comprehensive_latest 螺杆泵综合数据实时视图 

| **序号** | **代码**                     | **名称**           | **类型**       | **单位**    | 
|----------|------------------------------|--------------------|----------------|-------------|
| 1        | id                           | 记录编号           | NUMBER(10)     |             | 
| 2        | wellname                     | 井名               | VARCHAR2(200)  |             | 
| 3        | wellid                       | 井编号             | NUMBER(10)     |             | 
| 4        | liftingtype                  | 举升类型           | NUMBER(10)     |             | 
| 5        | acquisitiontime              | 采集时间           | DATE           |             | 
| 6        | acquisitiontime_d            | 离散数据采集时间   | DATE           |             | 
| 7        | commstatus                   | 通信状态           | NUMBER(2)      |             | 
| 8        | commstatusname               | 通信状态名称       | VARCHAR2       |             | 
| 9        | commalarmlevel               | 通信状态报警级别   | NUMBER(3)      |             | 
| 10       | runstatus                    | 运行状态           | NUMBER(1)      |             | 
| 11       | runstatusname                | 运行状态名称       | VARCHAR2       |             | 
| 12       | runalarmlevel                | 运行状态报警级别   | NUMBER(3)      |             | 
| 13       | commtime                     | 在线时间           | NUMBER(8,2)    | h           | 
| 14       | commrange                    | 在线区间           | VARCHAR2(2000) |             | 
| 15       | commtimeefficiency           | 在线时率           | NUMBER(10,4)   |             | 
| 16       | commtimeefficiencylevel      | 在线时率级别       | VARCHAR2(50)   |             | 
| 17       | runtime                      | 运行时间           | NUMBER(8,2)    | h           | 
| 18       | runrange                     | 运行区间           | VARCHAR2(2000) |             | 
| 19       | runtimeefficiency            | 生产时率           | NUMBER(10,4)   |             | 
| 20       | runtimeefficiencylevel       | 生产时率级别       | VARCHAR2(50)   |             | 
| 21       | workingconditioncode         | 工况代码           | NUMBER(4)      |             | 
| 22       | workingconditionname         | 工况名称           | VARCHAR2(200)  |             | 
| 23       | optimizationsuggestion       | 优化建议           | VARCHAR2(200)  |             | 
| 24       | workingconditionalarmlevel   | 工况报警级别       | VARCHAR2       |             | 
| 25       | workingconditioncode_e       | 电参工况代码       | NUMBER(4)      |             | 
| 26       | workingconditionstring_e     | 电参工况字符串     | VARCHAR2(4000) |             | 
| 27       | workingconditionname_e       | 电参工况名称       | VARCHAR2(200)  |             | 
| 28       | optimizationsuggestion_e     | 电参工况优化建议   | VARCHAR2(200)  |             | 
| 29       | workingconditionalarmlevel_e | 电参工况报警级别   | NUMBER(3)      |             | 
| 30       | rpm                          | 转速               | NUMBER(8,2)    | r/min       | 
| 31       | torque                       | 扭矩               | NUMBER(8,2)    | kN·m        | 
| 32       | theoreticalproduction        | 理论排量           | NUMBER(8,2)    | m^3/d       | 
| 33       | liquidweightproduction       | 产液量吨           | NUMBER(8,2)    | t/d         |
| 34       | oilweightproduction          | 产油量吨           | NUMBER(8,2)    | t/d         |
| 35       | waterweightproduction        | 产水量吨           | NUMBER(8,2)    | t/d         |
| 36       | watercut_w                   | 重量含水率         | NUMBER(8,2)    | %           |
| 37       | liquidweightproductionlevel  | 产液级别吨         | VARCHAR2(50)   |             |
| 38       | liquidvolumetricproduction   | 产液量方           | NUMBER(8,2)    | m^3/d       |
| 39       | oilvolumetricproduction      | 产油量方           | NUMBER(8,2)    | m^3/d       |
| 40       | watervolumetricproduction    | 产水量方           | NUMBER(8,2)    | m^3/d       |
| 41       | watercut                     | 体积含水率         | NUMBER(8,2)    | %           |
| 42       | liquidvolumeproductionlevel  | 产液级别方         | VARCHAR2(50)   |             | 
| 43       | productiongasoilratio        | 生产气油比         | NUMBER(8,2)    | m^3/t       | 
| 44       | tubingpressure               | 油压               | NUMBER(8,2)    | MPa         | 
| 45       | casingpressure               | 套压               | NUMBER(8,2)    | MPa         | 
| 46       | wellheadfluidtemperature     | 井口油温           | NUMBER(8,2)    | ℃          | 
| 47       | qpr                          | 公称排量           | NUMBER(8,2)    | m^3/r       | 
| 48       | barrellength                 | 泵筒长             | NUMBER(8,2)    | m           | 
| 49       | barrelseries                 | 泵级数             | NUMBER(8,2)    |             | 
| 50       | rotordiameter                | 转子截面直径       | NUMBER(8,2)    | mm          | 
| 51       | producingfluidlevel          | 动液面             | NUMBER(8,2)    | m           | 
| 52       | pumpsettingdepth             | 泵挂               | NUMBER(8,2)    | m           | 
| 53       | submergence                  | 沉没度             | NUMBER(8,2)    | m           | 
| 54       | pumpborediameter             | 泵径               | NUMBER(8,2)    | mm          | 
| 55       | crudeoildensity              | 原油密度           | NUMBER(16,2)   | g/cm^3      | 
| 56       | netgrossratio                | 净毛比             | NUMBER(8,2)    |             | 
| 57       | rodstring                    | 抽油杆数据         | VARCHAR2(200)  |             | 
| 58       | motorinputactivepower        | 电机输入有功功率   | NUMBER(8,2)    | kW          | 
| 59       | waterpower                   | 水功率             | NUMBER(8,2)    | kW          | 
| 60       | systemefficiency             | 系统效率           | NUMBER(12,3)   | 小数        | 
| 61       | systemefficiencylevel        | 系统效率级别       | VARCHAR2(50)   |             | 
| 62       | powerconsumptionperthm       | 吨液百米耗电量     | NUMBER(8,2)    | kW·h/100m·t | 
| 63       | pumpeff1                     | 容积效率           | NUMBER(12,3)   | 小数        | 
| 64       | pumpeff2                     | 液体收缩系数       | NUMBER(12,3)   | 小数        | 
| 65       | pumpeff                      | 泵效               | NUMBER(12,3)   | 小数        | 
| 66       | pumpintakep                  | 泵入口压力         | NUMBER(8,2)    | MPa         | 
| 67       | pumpintaket                  | 泵入口温度         | NUMBER(8,2)    | ℃          | 
| 68       | pumpintakegol                | 泵入口就地气液比   | NUMBER(8,2)    | m^3/m^3     | 
| 69       | pumpintakevisl               | 泵入口粘度         | NUMBER(8,2)    | mPa·s       | 
| 70       | pumpintakebo                 | 泵入口原油体积系数 | NUMBER(8,2)    | 小数        | 
| 71       | pumpoutletp                  | 泵出口压力         | NUMBER(8,2)    | MPa         | 
| 72       | pumpoutlett                  | 泵出口温度         | NUMBER(8,2)    | ℃          | 
| 73       | pumpoutletgol                | 泵出口就地气液比   | NUMBER(8,2)    | m^3/m^3     | 
| 74       | pumpoutletvisl               | 泵出口粘度         | NUMBER(8,2)    | mPa·s       | 
| 75       | pumpoutletbo                 | 泵出口原油体积系数 | NUMBER(8,2)    | 小数        | 
| 76       | todaywattenergy              | 日有功功耗         | NUMBER(8,2)    | kW·h        | 
| 77       | todaywattenergylevel         | 日有功功耗级别     | VARCHAR2(50)   |             | 
| 78       | todaypwattenergy             | 日正向有功功耗     | NUMBER(8,2)    | kW·h        | 
| 79       | todaynwattenergy             | 日反向有功功耗     | NUMBER(8,2)    | kW·h        | 
| 80       | todayvarenergy               | 日无功功耗         | NUMBER(8,2)    | kVar·h      | 
| 81       | todaypvarenergy              | 日正向无功功耗     | NUMBER(8,2)    | kVar·h      | 
| 82       | todaynvarenergy              | 日反向无功功耗     | NUMBER(8,2)    | kVar·h      | 
| 83       | todayvaenergy                | 日视在功耗         | NUMBER(8,2)    | kVA·h       | 
| 84       | ia                           | A相电流            | NUMBER(8,2)    | A           | 
| 85       | ib                           | B相电流            | NUMBER(8,2)    | A           | 
| 86       | ic                           | C相电流            | NUMBER(8,2)    | A           | 
| 87       | iavg                         | 三相平均电流       | NUMBER(8,2)    | A           | 
| 88       | istr                         | 电流字符串         | VARCHAR2       |             | 
| 89       | iauplimit                    | A相电流上限        | NUMBER(8,2)    | A           | 
| 90       | iadownlimit                  | A相电流下限        | NUMBER(8,2)    | A           | 
| 91       | iazero                       | A相电流零值        | NUMBER(8,2)    | A           | 
| 92       | ibuplimit                    | B相电流上限        | NUMBER(8,2)    | A           | 
| 93       | ibdownlimit                  | B相电流下限        | NUMBER(8,2)    | A           | 
| 94       | ibzero                       | B相电流零值        | NUMBER(8,2)    | A           | 
| 95       | icuplimit                    | C相电流上限        | NUMBER(8,2)    | A           | 
| 96       | icdownlimit                  | C相电流下限        | NUMBER(8,2)    | A           | 
| 97       | iczero                       | C相电流零值        | NUMBER(8,2)    | A           | 
| 98       | va                           | A相电压            | NUMBER(8,2)    | V           | 
| 99       | vb                           | B相电压            | NUMBER(8,2)    | V           | 
| 100      | vc                           | C相电压            | NUMBER(8,2)    | V           | 
| 101      | vavg                         | 三相平均电压       | NUMBER(8,2)    | V           | 
| 102      | vstr                         | 电压字符串         | VARCHAR2       |             | 
| 103      | vauplimit                    | A相电压上限        | NUMBER(8,2)    | V           | 
| 104      | vadownlimit                  | A相电压下限        | NUMBER(8,2)    | V           | 
| 105      | vazero                       | A相电压零值        | NUMBER(8,2)    | V           | 
| 106      | vbuplimit                    | B相电压上限        | NUMBER(8,2)    | V           | 
| 107      | vbdownlimit                  | B相电压下限        | NUMBER(8,2)    | V           | 
| 108      | vbzero                       | B相电压零值        | NUMBER(8,2)    | V           | 
| 109      | vcuplimit                    | C相电压上限        | NUMBER(8,2)    | V           | 
| 110      | vcdownlimit                  | C相电压下限        | NUMBER(8,2)    | V           | 
| 111      | vczero                       | C相电压零值        | NUMBER(8,2)    | V           | 
| 112      | totalwattenergy              | 累计有功功耗       | NUMBER(8,2)    | kW·h        | 
| 113      | totalpwattenergy             | 累计正向有功功耗   | NUMBER(8,2)    | kW·h        | 
| 114      | totalnwattenergy             | 累计反向有功功耗   | NUMBER(8,2)    | kW·h        | 
| 115      | totalvarenergy               | 累计无功功耗       | NUMBER(8,2)    | kVar·h      | 
| 116      | totalpvarenergy              | 累计正向无功功耗   | NUMBER(8,2)    | kVar·h      | 
| 117      | totalnvarenergy              | 累计反向无功功耗   | NUMBER(8,2)    | kVar·h      | 
| 118      | totalvaenergy                | 累计视在功耗       | NUMBER(8,2)    | kVA·h       | 
| 119      | watta                        | A相有功功率        | NUMBER(8,2)    | kW          | 
| 120      | wattb                        | B相有功功率        | NUMBER(8,2)    | kW          | 
| 121      | wattc                        | C相有功功率        | NUMBER(8,2)    | kW          | 
| 122      | wattsum                      | 三相总有功功率     | NUMBER(8,2)    | kW          | 
| 123      | wattstr                      | 有功功率字符串     | VARCHAR2       |             | 
| 124      | vara                         | A相无功功率        | NUMBER(8,2)    | kVar        | 
| 125      | varb                         | B相无功功率        | NUMBER(8,2)    | kVar        | 
| 126      | varc                         | C相无功功率        | NUMBER(8,2)    | kVar        | 
| 127      | varsum                       | 三相总无功功率     | NUMBER(8,2)    | kVar        | 
| 128      | varstr                       | 无功功率字符串     | VARCHAR2       |             | 
| 129      | reversepower                 | 反向功率           | NUMBER(8,2)    |             |
| 130      | vaa                          | A相视在功率        | NUMBER(8,2)    | kVA         |
| 131      | vab                          | B相视在功率        | NUMBER(8,2)    | kVA         |
| 132      | vac                          | C相视在功率        | NUMBER(8,2)    | kVA         |
| 133      | vasum                        | 三相总视在功率     | NUMBER(8,2)    | kVA         |
| 134      | vastr                        | 视在功率字符串     | VARCHAR2       |             | 
| 135      | pfa                          | A相功率因数        | NUMBER(8,2)    |             | 
| 136      | pfb                          | B相功率因数        | NUMBER(8,2)    |             | 
| 137      | pfc                          | C相功率因数        | NUMBER(8,2)    |             | 
| 138      | pfsum                        | 三相综合功率因数   | NUMBER(8,2)    |             | 
| 139      | pfstr                        | 功率因数字符串     | VARCHAR2       |             | 
| 140      | frequencysetvalue            | 设置频率           | NUMBER(8,2)    | HZ          | 
| 141      | frequencyrunvalue            | 运行频率           | NUMBER(8,2)    | HZ          | 
| 142      | signal                       | 信号强度           | NUMBER(8,2)    |             | 
| 143      | interval                     | 传输间隔           | NUMBER(10)     |             | 
| 144      | devicever                    | 设备版本           | VARCHAR2(50)   |             | 
| 145      | videourl                     | 视频路径           | VARCHAR2(400)  |             | 
| 146      | org_id                       | 组织编号           | NUMBER(10)     |             | 
| 147      | org_code                     | 组织代码           | VARCHAR2(20)   |             | 
| 148      | sortnum                      | 排序编号           | NUMBER(10)     |             | 

### 2.1.23 viw_pcp_comprehensive_hist 螺杆泵综合数据历史视图

同viw_pcp_comprehensive_latest

### 2.1.24 viw_pcp_total_day 螺杆泵日累计数据视图

| **序号** | **代码**                    | **名称**         | **类型**       | **单位**    | 
|----------|-----------------------------|------------------|----------------|-------------|
| 1        | id                          | 记录编号         | NUMBER(10)     |             | 
| 2        | wellname                    | 井名             | VARCHAR2(200)  |             | 
| 3        | liftingtype                 | 举升类型         | NUMBER(10)     |             | 
| 4        | liftingtypename             | 举升类型名称     | VARCHAR2(200)  |             | 
| 5        | wellid                      | 井编号           | NUMBER(10)     |             | 
| 6        | calculatedate               | 日期             | DATE           |             | 
| 7        | commstatus                  | 通信状态         |                |             | 
| 8        | commstatusname              | 通信状态名称     |                |             | 
| 9        | commalarmlevel              | 通信状态报警级别 |                |             | 
| 10       | runstatus                   | 运行状态         | NUMBER(2)      |             | 
| 11       | runstatusname               | 运行状态名称     |                |             | 
| 12       | runalarmlevel               | 运行状态报警级别 |                |             | 
| 13       | commtime                    | 在线时间         | NUMBER(8,2)    | h           | 
| 14       | commrange                   | 在线区间         | VARCHAR2(4000) |             | 
| 15       | commtimeefficiency          | 在线时率         | NUMBER(12,3)   |             | 
| 16       | commtimeefficiencylevel     | 在线时率级别     | VARCHAR2(50)   |             | 
| 17       | runtime                     | 运行时间         | NUMBER(8,2)    | h           | 
| 18       | runrange                    | 运行区间         | VARCHAR2(4000) |             | 
| 19       | runtimeefficiency           | 运行时率         | NUMBER(12,3)   |             | 
| 20       | runtimeefficiencylevel      | 运行时率级别     | VARCHAR2(50)   |             | 
| 21       | workingconditioncode        | 工况代码         | NUMBER(4)      |             | 
| 22       | workingconditionname        | 工况名称         | VARCHAR2(200)  |             | 
| 23       | workingconditionstring      | 工况累计字符串   | VARCHAR2(4000) |             | 
| 24       | optimizationsuggestion      | 优化建议         | VARCHAR2(200)  |             | 
| 25       | workingconditionalarmlevel  | 工况报警级别     | NUMBER(3)      |             | 
| 26       | liquidweightproduction      | 产液量吨         | NUMBER(8,2)    | t/d         |
| 27       | oilweightproduction         | 产油量吨         | NUMBER(8,2)    | t/d         |
| 28       | waterweightproduction       | 产水量吨         | NUMBER(8,2)    | t/d         |
| 29       | watercut_w                  | 重量含水率       | NUMBER(8,2)    | %           |
| 30       | liquidweightproductionlevel | 产液级别吨       | VARCHAR2(50)   |             |
| 31       | liquidvolumetricproduction  | 产液量方         | NUMBER(8,2)    | m^3/d       |
| 32       | oilvolumetricproduction     | 产油量方         | NUMBER(8,2)    | m^3/d       |
| 33       | watervolumetricproduction   | 产水量方         | NUMBER(8,2)    | m^3/d       |
| 34       | watercut                    | 体积含水率       | NUMBER(8,2)    | %           |
| 35       | liquidvolumeproductionlevel | 产液级别方       | VARCHAR2(50)   |             | 
| 36       | productiongasoilratio       | 生产气油比       | NUMBER(8,2)    | m^3/t       | 
| 37       | tubingpressure              | 油压             | NUMBER(8,2)    | MPa         | 
| 38       | casingpressure              | 套压             | NUMBER(8,2)    | MPa         | 
| 39       | wellheadfluidtemperature    | 井口油温         | NUMBER(8,2)    | ℃          | 
| 40       | pumpeff                     | 总泵效           | NUMBER(10,4)   | 小数        | 
| 41       | pumpborediameter            | 泵径             | NUMBER(8,2)    | mm          | 
| 42       | pumpsettingdepth            | 泵挂             | NUMBER(8,2)    | m           | 
| 43       | producingfluidlevel         | 动液面           | NUMBER(8,2)    | m           | 
| 44       | submergence                 | 沉没度           | NUMBER(8,2)    | m           | 
| 45       | rpm                         | 转速             | NUMBER(8,2)    | r/min       | 
| 46       | rpmmax                      | 转速最大值       | NUMBER(8,2)    | r/min       | 
| 47       | rpmmin                      | 转速最小值       | NUMBER(8,2)    | r/min       | 
| 48       | systemefficiency            | 系统效率         | NUMBER(10,4)   | 小数        | 
| 49       | systemefficiencylevel       | 系统效率级别     | VARCHAR2(50)   |             | 
| 50       | powerconsumptionperthm      | 吨液百米耗电量   | NUMBER(8,2)    | kW·h/100m·t | 
| 51       | todaywattenergy             | 日有功功耗       | NUMBER(8,2)    | kW·h        | 
| 52       | todaywattenergylevel        | 日有功功耗级别   | VARCHAR2(50)   |             | 
| 53       | todaypwattenergy            | 日正向有功功耗   | NUMBER(8,2)    | kW·h        | 
| 54       | todaynwattenergy            | 日反向有功功耗   | NUMBER(8,2)    | kW·h        | 
| 55       | todayvarenergy              | 日无功功耗       | NUMBER(8,2)    | kVar·h      | 
| 56       | todaypvarenergy             | 日正向无功功耗   | NUMBER(8,2)    | kVar·h      | 
| 57       | todaynvarenergy             | 日反向无功功耗   | NUMBER(8,2)    | kVar·h      | 
| 58       | todayvaenergy               | 日视在功耗       | NUMBER(8,2)    | kVA·h       | 
| 59       | ia                          | A相电流          | NUMBER(8,2)    | A           | 
| 60       | iamax                       | A相电流最大值    | NUMBER(8,2)    | A           | 
| 61       | iamin                       | A相电流最小值    | NUMBER(8,2)    | A           | 
| 62       | iastr                       | A相电流字符串    | NUMBER(8,2)    |             | 
| 63       | ib                          | B相电流          | NUMBER(8,2)    | A           | 
| 64       | ibmax                       | B相电流最大值    | NUMBER(8,2)    | A           | 
| 65       | ibmin                       | B相电流最小值    | NUMBER(8,2)    | A           | 
| 66       | ibstr                       | B相电流字符串    | VARCHAR2       |             | 
| 67       | ic                          | C相电流          | NUMBER(8,2)    | A           | 
| 68       | icmax                       | C相电流最大值    | NUMBER(8,2)    | A           | 
| 69       | icmin                       | C相电流最小值    | NUMBER(8,2)    | A           | 
| 70       | icstr                       | C相电流字符串    | VARCHAR2       |             | 
| 71       | va                          | A相电压          | NUMBER(8,2)    | V           | 
| 72       | vamax                       | A相电压最大值    | NUMBER(8,2)    | V           | 
| 73       | vamin                       | A相电压最小值    | NUMBER(8,2)    | V           | 
| 74       | vastr                       | A相电压字符串    | VARCHAR2       |             | 
| 75       | vb                          | B相电压          | NUMBER(8,2)    | V           | 
| 76       | vbmax                       | B相电压最大值    | NUMBER(8,2)    | V           | 
| 77       | vbmin                       | B相电压最小值    | NUMBER(8,2)    | V           | 
| 78       | vbstr                       | B相电压字符串    | VARCHAR2       |             | 
| 79       | vc                          | C相电压          | NUMBER(8,2)    | V           | 
| 80       | vcmax                       | C相电压最大值    | NUMBER(8,2)    | V           | 
| 81       | vcmin                       | C相电压最小值    | NUMBER(8,2)    | V           | 
| 82       | vcstr                       | C相电压字符串    | VARCHAR2       |             | 
| 83       | signal                      | 信号强度         | NUMBER(8,2)    |             | 
| 84       | signalmax                   | 信号强度最大值   | NUMBER(8,2)    |             | 
| 85       | signalmin                   | 信号强度最小值   | NUMBER(8,2)    |             | 
| 86       | signalstr                   | 信号强度字符串   | VARCHAR2       |             | 
| 87       | videourl                    | 视频路径         | VARCHAR2(400)  |             | 
| 88       | sortnum                     | 排序编号         | NUMBER(10)     |             | 
| 89       | org_code                    | 组织代码         | VARCHAR2(20)   |             | 
| 90       | org_id                      | 组织编号         | NUMBER(10)     |             | 
| 91       | remark                      | 备注             | VARCHAR2       |             |

# 三、存储过程

| **序号** | **名称**                      | **描述**                      | **备注**             |
|----------|-------------------------------|-------------------------------|----------------------|
| 1        | prd_clear_data                | 清理数据并重置序列            |                      |
| 2        | prd_reset_sequence            | 重置序列                      |                      |
| 3        | prd_save_wellinformation      | 保存井信息数据                |                      |
| 4        | prd_change_wellname           | 修改井名                      |                      |
| 5        | prd_save_wellboretrajectory   | 保存井身轨迹数据              |                      |
| 6        | prd_save_rpc_productiondata   | 保存生产数据                  |                      |
| 7        | prd_save_rpc_diagram          | 保存功图采集和计算数据        |                      |
| 8        | prd_save_rpc_uploaddiagram    | 保存上传的功图数据            |                      |
| 9        | prd_save_rpc_diagramresult    | 保存功图计算结果              |                      |
| 10       | prd_save_rpc_recalculateparam | 保存功图重新计算参数          |                      |
| 11       | prd_save_rpc_reinverdiagram   | 保存重新反演曲线数据          |                      |
| 12       | prd_init_rpc_daily            | 初始化日汇总数据              | 每天凌晨一点定时执行 |
| 13       | prd_save_rpc_diagramdaily     | 保存功图日汇总数据            |                      |
| 14       | prd_save_rpc_discretedaily    | 保存离散数据日汇总结果        |                      |
| 15       | prd_save_rpc_inver_daily      | 保存反演上传的日汇总数据      |                      |
| 16       | prd_save_rpc_motor            | 保存反演电机数据              |                      |
| 17       | prd_save_rpcinformation       | 保存反演抽油机数据            |                      |
| 18       | prd_save_rpc_inver_opt        | 保存反演优化参数              |                      |
| 19       | prd_save_alarmcolor           | 保存报警级别颜色              |                      |
| 20       | prd_save_pcp_productiondata   | 保存生产数据_螺杆泵           |                      |
| 21       | prd_save_pcp_discretedaily    | 保存离散数据日汇总结果_螺杆泵 |                      |
| 22       | prd_save_pcp_rpm              | 保存曲线采集和计算数据_螺杆泵 |                      |
| 23       | prd_save_pcp_rpmdaily         | 保存曲线日汇总数据_螺杆泵     |                      |

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
| 28       | trg_b_pcp_discrete_latest_i   | 螺杆泵离散数据实时表插入数据前触发       |
| 29       | trg_b_pcp_discrete_hist_i     | 螺杆泵离散数据历史表插入数据前触发       |
| 30       | trg_b_pcp_proddata_latest_i   | 螺杆泵生产数据实时表插入数据前触发       |
| 31       | trg_b_pcp_proddata_hist_i     | 螺杆泵生产数据历史表插入数据前触发       |
| 32       | trg_b_pcp_rpm_latest_i        | 螺杆泵曲线数据实时表插入数据前触发       |
| 33       | trg_b_pcp_rpm_hist_i          | 螺杆泵曲线数据历史表插入数据前触发       |
| 34       | trg_a_pcp_rpm_hist_i_u        | 螺杆泵曲线数据历史表插入、更新数据后触发 |
| 35       | trg_b_pcp_total_day_i         | 螺杆泵日累计数据表插入数据前触发         |
| 36       | trg_b_wellboretrajectory_i    | 井身轨迹表插入数据前出发                 |
