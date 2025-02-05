腾讯云本地专用集群（Cloud Dedicated Cluster，CDC）是全新推出的托管型基础设施类产品，将腾讯云的计算、网络、存储等服务以整机柜的形式，扩展到用户 IDC，就近提供与云上一致的能力，支持通过公有云现有工具（控制台、API 等）实现 CDC 资源的统一管理。

CDC 融合了公有云与本地 IDC 的双重优势，用户可以以本地化的时延和数据安全来使用公有云的丰富能力，构建强大的分布式边缘云网络。
<img src="https://main.qcloudimg.com/raw/7820418a0b0b98fb98c2943fb137c7d3.png" width="60%" />

## 网络功能
CDC 目前支持的网络功能包括：
+ 支持单 VPC 多子网
+ 支持 VPC 默认路由表，也支持自定义路由表
+ 支持 CDC 子网内云服务器绑定安全组，控制实例的出入流量
+ 支持 CDC 子网关联网络 ACL，控制 CDC 子网的出入流量
+ 支持通过 CDC 本地网关与 IDC 通信
+ 支持 CDC 内云服务器绑定弹性 IP，并最终经过 IDC 本地 NAT 转换后与公网通信

![](https://main.qcloudimg.com/raw/0f6e2acdf223585ce7594725bca29f3b.png)

## 使用限制
+ 1个 CDC 只支持1个 VPC，1个 CDC 集群的1个 VPC 只能够创建1个 CDC 本地网关。
+ CDC 独占子网，子网支持更换路由表、ACL，不支持 IPv6、广播功能。
+ CDC 暂不支持内网 CLB、VPN、NAT 网关、专线接入等其他网络接入能力。
+ CDC 支持和云上关联的 VPC 内的所有子网服务进行通信，暂不支持跨 VPC 互访，也不支持和该 VPC 内的专线、SD-WAN Edge、黑石服务器、VPN 互访。
+ CDC 所关联的 VPC 网段不能与 IDC 网段重叠。
+ 弹性 IP 地址池：需要用户分配1个内网地址段（不能够和 IDC Underlay 其他已经使用网段重叠），且网段 CIDR 掩码要求大于等于/29。

## 网络通信场景
+ CDC 内云服务器互访
+ CDC 内云服务器访问公网
+ CDC 通过本地网关与本地 IDC 通信


