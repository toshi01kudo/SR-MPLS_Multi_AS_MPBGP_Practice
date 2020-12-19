# SR-MPLS_Multi_AS_MPBGP_Practice
Practice repository - Upload the config to work.

## Network diagram
### Layer 3 IP assignment
* Inner-AS: ```192.168.xx.xx/24```
* Inter-AS: ```172.24.xx.xx/24```
* Mgmt IP: ```100.64.x.x/32```

### Layer 2 VLAN assignment
クラウド上に構築するため、リソース節約のため、単一物理ネットワーク上に構築する。\
ルータ間接続はVLANで接続し、他の通信が干渉しないようにする。
