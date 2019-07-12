---
title: irf 配置
date: 2019-07-09 02:59:46
tags:
---
#irf 配置
irf 英文全称为：Intelligent Resilient Framework，中文全称为：智能弹性架构。它的思想是将多台设备通过irf物理端口连接在一起，进行必要的irf配置后，多台设备整体虚拟化成一台irf设备，可以统一管理和不间断维护多台设备。
要想配好irf，需要理解以下几个概念：
- irf 物理端口
- irf端口
- 成员编号
- 成员设备优先级 

&#8195;&#8195;**irf物理端口：** 设备上的物理端口。
&#8195;&#8195;**irf端口：** 一种逻辑端口，配置irf需要物理端口关闭后加入irf的逻辑端口，端口号取值只能为1或2。成员设备的irf端口号不能相同。
&#8195;&#8195;**成员编号：** 用于标识成员设备的号码。
&#8195;&#8195;**成员设备优先级：** 成员优先级高的成员设备成为master设备。
配置irf的过程为：
1. 配置成员编号和成员优先级
2. 配置irf端口
3. 保存当前配置文件
4. 切换设备的运行模式


**相关命令为：**
irf member member-id：配置成员编号
irf priority priority：配置成员设备优先级
irf-port port-number：创建irf端口
port group interface interface-type interface-number [ mode { enhanced | normal } ]：将物理端口加入irf端口，物理端口需要先关闭
chassis convert mode irf：转换设备的运行模式为irf模式

