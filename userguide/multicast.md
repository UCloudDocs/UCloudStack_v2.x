# 29 组播

## 29.1 组播概述

作为一种与单播（Unicast）和广播（Broadcast）并列的通信方式，组播（Multicast）技术能够有效地解决单点发送、多点接收的问题，从而实现了网络中点到多点的高效数据传送，可以为企业节约网络带宽、降低网络负载，在ucloudstack 平台创建组播产品，支持 vpc 内组播通信。

## 29.2 创建组播

云平台用户可以通过指定VPC、组播组IP、组播组端口、发送方机器、接收方机器、项目组、组播名称等相关基础信息创建组播。

可通过导航栏进入【组播】资源控制台，通过 “**创建**” 进入向导页面，如下图所示：

![createFS](../images/userguide/createmulticast.png)

1、选择并配置组播的基础配置：

* 规则名称/备注：申请组播的名称和备注，申请时必须指定名称
* 组播组IP：组播IP仅支持224.0.0.0/4网段内的IP
* 组播组端口：组播组端口需要用户指定，端口默认范围为10000-64999
* vpc：创建组播时必须选择 VPC 网络，即选择要加入的网络
* 发送方：发送和接收方为相同VPC下的虚拟机，发送方为单一虚拟机
* 接收方：发送和接收方为相同VPC下的虚拟机，接收方可以为多个虚拟机
* 单个vpc可以添加的组播组规则限制为9个，一个组播组接收方数量限制为9个
## 29.3 组播列表

通过导航栏进入组播控制台，可查看组播资源列表。

组播列表可查看当前账户下所有组播资源的列表信息，包括名称、资源ID、状态、VPC、组播组IP、组播组端口、发送方、接收方、项目组、创建时间、更新时间及操作项，如下图所示：

![FSlist](../images/userguide/multicastlist.png)

- 名称：组播资源的名称；
- 资源 ID：组播的资源ID作为全局唯一标识符；
- 状态：组播资源的状态，包括可用、删除中等状态；
- 组播组IP：需要用户指定，组播IP仅支持224.0.0.0/4网段内的IP
- 组播组端口：需要用户指定，端口默认范围为10000-64999
- 发送方：同vpc下的发送机器，可以作为组播源发送组播消息
- 接收方：同vpc下的接收机器，可以接收组播消息
- VPC：组播创建时所指定的 VPC 网络；
- 项目组：组播创建时所绑定的项目组；
- 创建时间/更新时间：组播资源的创建时间和更新组播规则的时间；
- 操作：列表上的操作项是对单个组播的操作，包括更新、删除。

## 29.4 更新组播规则

更新组播的规则，添加或删除接收方的机器。可通过点击组播列表名称右侧的 “更新” 按钮进行修改，如下图所示：

![modifyFSname](../images/userguide/modifymulticast.png)

## 29.5 删除组播

用户可在控制台删除账户内组比，支持对组播进行批量删除操作。可通过组播列表操作项中的 “**删除**” 进行操作，如下图所示：

![FSrm](../images/userguide/multicastrm.png)



