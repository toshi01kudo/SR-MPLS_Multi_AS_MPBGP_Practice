# SR-MPLS Multi AS MP-BGP Practice
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

### Layer 1 Physical port assignment
リソース節約のため、単一物理ネットワーク上に構築する。\
L1レベルではすべて同じスイッチに所属しているように見える。

![L1NWD](./L1NWD_SRMPLS.PNG)

## 設計詳細

* 参考URL: [IOS および IOS XR を使用したレイヤ 3 MPLS VPN INTER-AS オプション B の設定と検証](https://www.cisco.com/c/ja_jp/support/docs/multiprotocol-label-switching-mpls/mpls/200557-Configuration-and-Verification-of-Layer.html)
* 参考URL: [MPLS網にSegment Routingを適用してみよう](https://www.netone.co.jp/knowledge-center/blog-column/knowledge_takumi_175/)
* 参考URL: [Segment Routing Configuration Guide for Cisco ASR 9000 Series Routers, IOS XR](https://www.cisco.com/c/en/us/td/docs/routers/asr9000/software/segment-routing/configuration/guide/b-seg-routing-cg-asr9k.html)
* 参考URL: [SR IGP Flex Algo - Segment Routing](https://www.segment-routing.net/images/sr-igp-flex-algo-rev4b-km1.pdf)
* 参考URL: [Segment Routingでよく聞かれること](https://note.com/ka_summary/n/n6ba56050774f)


### Segment Routing のとは？

### Segment Routing のメリット

### SR-MPLS の基本設定とIGP
* 参考URL: [MPLS網にSegment Routingを適用してみよう](https://www.netone.co.jp/knowledge-center/blog-column/knowledge_takumi_175/)
* 参考URL: [Segment Routing Configuration Guide for Cisco ASR 9000 Series Routers, IOS XR](https://www.cisco.com/c/en/us/td/docs/routers/asr9000/software/segment-routing/configuration/guide/b-seg-routing-cg-asr9k.html)

#### IGPの選択
IS-ISとOSPFが対応。本環境ではFlex-Algo利用を視野に入れていることもあり、Segment Routingが早期から導入されてきたIS-ISを利用する。\
IS-ISのため、NSAPアドレスの設定が必要なので、忘れずに設定する。\
本環境ではNSAPアドレスはLoopbackアドレス、アドレスファミリーはIPv4を用いる。

```
router isis core
 net 49.0001.1000.6400.0001.00
 address-family ipv4 unicast
  segment-routing mpls
```

#### SRGBの設定
マルチベンダー環境の場合、Segment Routing Global Block (SRGB) の規定値が異なる場合があるので、念のためで設定を投入することが推奨。\
SRGBはルータ内でPrefix-sid / Node-sid 等のGlobal SID付与に使用されるラベル番号の範囲のこと。\
Ciscoのデフォルトは```16000 - 23999```

```
router isis core
 segment-routing global-block 16000 23999
```

#### Node SID設定
SRGBの範囲内で機器にNode Segment IDを付与。Node-sidはルータ自身を示すSIDであり同一SR Domain内でユニーク（一意）である必要あり。\
通常、Loopback インターフェースにてIS-ISを動作させ、Node SIDを割り当てている。\
指定方法にはindex指定と絶対値(absolute)指定の2種類存在。index指定が一般的。\
indexはSRGBの開始値に加算した値がNode-SIDとなる。

```
router isis core
 interface Loopback1
  passive
  address-family ipv4 unicast
   prefix-sid index 1001
```

(参考) SRGBの開始値が16000の時、下記2つの設定は同一。
```
   prefix-sid index 1001
   prefix-sid absolute 17001
```

#### Adjacency-SID設定
Adj-sidはユーザが設定する必要は無く自動的に付与されるが、自身で設定する場合には下記\
Cisco デフォルトの SRLB は ```15000 - 15999``` のため、index指定の場合はSRGB同様、SRLB開始値に加算される。

```
router isis core
 segment-routing global-block 16000 23999
 !
 interface GigabitEthernet0/0/0/0.12
  point-to-point
  address-family ipv4 unicast
   adjacency-sid index 12
  !
 !
 interface GigabitEthernet0/0/0/0.13
  point-to-point
  address-family ipv4 unicast
   adjacency-sid index 13
  !
segment-routing
 global-block 16000 23999
 adjacency-sid
  interface GigabitEthernet0/0/0/0.12
   address-family ipv4 unicast
    l2-adjacency-sid absolute 15012 next-hop 192.168.12.2
   !
  !
  interface GigabitEthernet0/0/0/0.13
   address-family ipv4 unicast
    l2-adjacency-sid absolute 15013 next-hop 192.168.13.3
```

#### TI-LFA設定
SR環境でFRR（Fast ReRoute : 高速迂回）を実現するための機能であるTI-LFA（Topology Independent Loop Free Alternate）の設定を実施。\
TI-LFAを使用するとルータは最適pathとは異なる迂回用のpathをprefix毎に計算し、それを保持。\
最適pathの障害時には保持している迂回用pathに通信を切り替えることで高速迂回を実現。


```
router isis core
 interface GigabitEthernet0/0/0/0.12
  address-family ipv4 unicast
   fast-reroute per-prefix
   fast-reroute per-prefix ti-lfa
  !
 !
 interface GigabitEthernet0/0/0/0.13
  address-family ipv4 unicast
   fast-reroute per-prefix
   fast-reroute per-prefix ti-lfa
```


### Segment Routing 環境での Inter AS MP-BGP


### SRv6 の基本設定


