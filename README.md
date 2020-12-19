# SR-MPLS_Multi_AS_MPBGP_Practice
Practice repository - Upload the config to work.

## Network diagram
### Layer 3 IP assignment
* Inner-AS: ```192.168.xx.xx/24```
* Inter-AS: ```172.24.xx.xx/24```
* Mgmt IP: ```100.64.x.x/32```
  * Octet 3: 
    * UG-A: 10
    * UG-B: 20
* UG AS: 650xx

![L3NWD](./L3NWD_SRMPLSv2.PNG)

### Layer 2 VLAN assignment
クラウド上に構築するため、リソース節約のため、単一物理ネットワーク上に構築する。\
ルータ間接続はVLANで接続し、他の通信が干渉しないようにする。

![L2NWD](./L2NWD_SRMPLSv2.PNG)
