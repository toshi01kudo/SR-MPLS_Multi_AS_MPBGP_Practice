# SR-MPLS_Multi_AS_MPBGP_Practice
Practice repository - Upload the config to work.\
This is Backbone network with SR-MPLS which has multi AS for MP-BGP, and CE routers will be pingable from each edge. 

SR-MPLS をベースにしたバックボーン環境を構築する。MP-BGPはマルチASとし、異なるASを接続した通信を実装する。

## 前提条件
Cisco 製品では、現時点でSRに対応しているのはCisco IOS XRのみ。\
VMの上の仮想環境で構築する。
* PE routers & P routers: Cisco XRv
* CE routers: Cisco CSR 1000v

## Network diagram
### Layer 3 IP assignment
* Inner-AS: ```192.168.xx.xx/24```
  * Octet 3: Link ID
* Inter-AS: ```172.24.xx.xx/24```
  * Octet 3: Link ID
* Mgmt IP: ```100.64.x.x/32```
  * Octet 3: 
    * UG-A: ```10```
    * UG-B: ```20```
* UG AS: ```650xx```

![L3NWD](./L3NWD_SRMPLSv2.PNG)

### Layer 2.8 Segment Routing ID assignment
* SRGB Range: ```16000 - 23999```
  * Segment ID: ```1600x```


### Layer 2 VLAN assignment
クラウド上に構築するため、リソース節約のため、単一物理ネットワーク上に構築する。\
ルータ間接続はVLANで接続し、他の通信が干渉しないようにする。

![L2NWD](./L2NWD_SRMPLSv2.PNG)

## 設計詳細

* 参考URL: [IOS および IOS XR を使用したレイヤ 3 MPLS VPN INTER-AS オプション B の設定と検証](https://www.cisco.com/c/ja_jp/support/docs/multiprotocol-label-switching-mpls/mpls/200557-Configuration-and-Verification-of-Layer.html)
* 参考URL: [MPLS網にSegment Routingを適用してみよう](https://www.netone.co.jp/knowledge-center/blog-column/knowledge_takumi_175/)
* 参考URL: [Segment Routing Configuration Guide for Cisco ASR 9000 Series Routers, IOS XR](https://www.cisco.com/c/en/us/td/docs/routers/asr9000/software/segment-routing/configuration/guide/b-seg-routing-cg-asr9k.html)


### Segment Routing のとは？

### Segment Routing のメリット

### Segment Routing の基本設定とIGP

### Segment Routing 環境での Inter AS MP-BGP


