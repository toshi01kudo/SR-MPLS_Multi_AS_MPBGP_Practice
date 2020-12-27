## XRv-11: 
```
RP/0/RP0/CPU0:cisco-kudo-11#show ip route
Sun Dec 27 04:25:24.454 UTC

Codes: C - connected, S - static, R - RIP, B - BGP, (>) - Diversion path
       D - EIGRP, EX - EIGRP external, O - OSPF, IA - OSPF inter area
       N1 - OSPF NSSA external type 1, N2 - OSPF NSSA external type 2
       E1 - OSPF external type 1, E2 - OSPF external type 2, E - EGP
       i - ISIS, L1 - IS-IS level-1, L2 - IS-IS level-2
       ia - IS-IS inter area, su - IS-IS summary null, * - candidate default
       U - per-user static route, o - ODR, L - local, G  - DAGR, l - LISP
       A - access/subscriber, a - Application route
       M - mobile route, r - RPL, t - Traffic Engineering, (!) - FRR Backup path

Gateway of last resort is not set

L    100.64.0.1/32 is directly connected, 2d03h, Loopback1
i L1 100.64.0.2/32 [115/10] via 192.168.12.2, 2d03h, GigabitEthernet0/0/0/0.12
                   [115/20] via 192.168.13.3, 2d03h, GigabitEthernet0/0/0/0.13 (!)
i L1 100.64.0.3/32 [115/20] via 192.168.12.2, 2d03h, GigabitEthernet0/0/0/0.12 (!)
                   [115/10] via 192.168.13.3, 2d03h, GigabitEthernet0/0/0/0.13
C    192.168.12.0/24 is directly connected, 2d03h, GigabitEthernet0/0/0/0.12
L    192.168.12.1/32 is directly connected, 2d03h, GigabitEthernet0/0/0/0.12
C    192.168.13.0/24 is directly connected, 2d03h, GigabitEthernet0/0/0/0.13
L    192.168.13.1/32 is directly connected, 2d03h, GigabitEthernet0/0/0/0.13
i L1 192.168.23.0/24 [115/20] via 192.168.12.2, 2d03h, GigabitEthernet0/0/0/0.12
                     [115/20] via 192.168.13.3, 2d03h, GigabitEthernet0/0/0/0.13

RP/0/RP0/CPU0:cisco-kudo-11#show route vrf all
Sun Dec 27 04:26:03.129 UTC

VRF: MGMT


Codes: C - connected, S - static, R - RIP, B - BGP, (>) - Diversion path
       D - EIGRP, EX - EIGRP external, O - OSPF, IA - OSPF inter area
       N1 - OSPF NSSA external type 1, N2 - OSPF NSSA external type 2
       E1 - OSPF external type 1, E2 - OSPF external type 2, E - EGP
       i - ISIS, L1 - IS-IS level-1, L2 - IS-IS level-2
       ia - IS-IS inter area, su - IS-IS summary null, * - candidate default
       U - per-user static route, o - ODR, L - local, G  - DAGR, l - LISP
       A - access/subscriber, a - Application route
       M - mobile route, r - RPL, t - Traffic Engineering, (!) - FRR Backup path

Gateway of last resort is not set

C    10.10.0.0/24 is directly connected, 2d03h, MgmtEth0/RP0/CPU0/0
L    10.10.0.41/32 is directly connected, 2d03h, MgmtEth0/RP0/CPU0/0

VRF: UG-A


Codes: C - connected, S - static, R - RIP, B - BGP, (>) - Diversion path
       D - EIGRP, EX - EIGRP external, O - OSPF, IA - OSPF inter area
       N1 - OSPF NSSA external type 1, N2 - OSPF NSSA external type 2
       E1 - OSPF external type 1, E2 - OSPF external type 2, E - EGP
       i - ISIS, L1 - IS-IS level-1, L2 - IS-IS level-2
       ia - IS-IS inter area, su - IS-IS summary null, * - candidate default
       U - per-user static route, o - ODR, L - local, G  - DAGR, l - LISP
       A - access/subscriber, a - Application route
       M - mobile route, r - RPL, t - Traffic Engineering, (!) - FRR Backup path

Gateway of last resort is not set

L    100.64.10.1/32 is directly connected, 2d03h, Loopback10
B    100.64.10.2/32 [200/0] via 100.64.0.2 (nexthop in vrf default), 2d03h
B    100.64.10.3/32 [200/0] via 100.64.0.3 (nexthop in vrf default), 1d22h
B    100.64.10.4/32 [200/0] via 100.64.0.3 (nexthop in vrf default), 02:38:58
B    100.64.10.5/32 [200/0] via 100.64.0.3 (nexthop in vrf default), 02:38:58
B    100.64.10.6/32 [200/0] via 100.64.0.3 (nexthop in vrf default), 02:38:58
B    100.64.10.18/32 [20/0] via 172.24.18.8, 2d03h
B    100.64.10.19/32 [200/0] via 100.64.0.3 (nexthop in vrf default), 00:57:03
B    100.64.10.28/32 [200/0] via 100.64.0.2 (nexthop in vrf default), 2d03h
B    100.64.10.29/32 [200/0] via 100.64.0.3 (nexthop in vrf default), 00:56:33
C    172.24.18.0/24 is directly connected, 2d03h, GigabitEthernet0/0/0/0.18
L    172.24.18.1/32 is directly connected, 2d03h, GigabitEthernet0/0/0/0.18
B    172.24.19.0/24 [200/0] via 100.64.0.3 (nexthop in vrf default), 02:38:58
B    172.24.28.0/24 [200/0] via 100.64.0.2 (nexthop in vrf default), 2d03h
B    172.24.29.0/24 [200/0] via 100.64.0.3 (nexthop in vrf default), 02:38:58

VRF: UG-B


Codes: C - connected, S - static, R - RIP, B - BGP, (>) - Diversion path
       D - EIGRP, EX - EIGRP external, O - OSPF, IA - OSPF inter area
       N1 - OSPF NSSA external type 1, N2 - OSPF NSSA external type 2
       E1 - OSPF external type 1, E2 - OSPF external type 2, E - EGP
       i - ISIS, L1 - IS-IS level-1, L2 - IS-IS level-2
       ia - IS-IS inter area, su - IS-IS summary null, * - candidate default
       U - per-user static route, o - ODR, L - local, G  - DAGR, l - LISP
       A - access/subscriber, a - Application route
       M - mobile route, r - RPL, t - Traffic Engineering, (!) - FRR Backup path

Gateway of last resort is not set

L    100.64.20.1/32 is directly connected, 2d03h, Loopback20
B    100.64.20.2/32 [200/0] via 100.64.0.2 (nexthop in vrf default), 2d03h
B    100.64.20.3/32 [200/0] via 100.64.0.3 (nexthop in vrf default), 1d22h
B    100.64.20.4/32 [200/0] via 100.64.0.3 (nexthop in vrf default), 02:38:58
B    100.64.20.5/32 [200/0] via 100.64.0.3 (nexthop in vrf default), 02:38:58
B    100.64.20.6/32 [200/0] via 100.64.0.3 (nexthop in vrf default), 02:38:58
B    100.64.20.38/32 [20/0] via 172.24.38.8, 2d03h
B    100.64.20.39/32 [200/0] via 100.64.0.3 (nexthop in vrf default), 00:57:03
B    100.64.20.48/32 [200/0] via 100.64.0.2 (nexthop in vrf default), 2d03h
B    100.64.20.49/32 [200/0] via 100.64.0.3 (nexthop in vrf default), 00:56:33
C    172.24.38.0/24 is directly connected, 2d03h, GigabitEthernet0/0/0/0.38
L    172.24.38.1/32 is directly connected, 2d03h, GigabitEthernet0/0/0/0.38
B    172.24.39.0/24 [200/0] via 100.64.0.3 (nexthop in vrf default), 02:38:58
B    172.24.48.0/24 [200/0] via 100.64.0.2 (nexthop in vrf default), 2d03h
B    172.24.49.0/24 [200/0] via 100.64.0.3 (nexthop in vrf default), 02:38:58
RP/0/RP0/CPU0:cisco-kudo-11#
RP/0/RP0/CPU0:cisco-kudo-11#
RP/0/RP0/CPU0:cisco-kudo-11#
RP/0/RP0/CPU0:cisco-kudo-11#show mpls ldp bindings
Sun Dec 27 04:27:41.741 UTC

100.64.0.1/32, rev 8
        Local binding: label: ImpNull
        Remote bindings: (2 peers)
            Peer                Label
            -----------------   ---------
            100.64.0.2:0        24008
            100.64.0.3:0        24008
100.64.0.2/32, rev 11
        Local binding: label: 24008
        Remote bindings: (2 peers)
            Peer                Label
            -----------------   ---------
            100.64.0.2:0        ImpNull
            100.64.0.3:0        24010
100.64.0.3/32, rev 13
        Local binding: label: 24010
        Remote bindings: (2 peers)
            Peer                Label
            -----------------   ---------
            100.64.0.2:0        24010
            100.64.0.3:0        ImpNull
172.24.34.0/24, rev 0
        No local binding
        Remote bindings: (1 peers)
            Peer                Label
            -----------------   ---------
            100.64.0.3:0        ImpNull
172.24.34.4/32, rev 0
        No local binding
        Remote bindings: (1 peers)
            Peer                Label
            -----------------   ---------
            100.64.0.3:0        24053
192.168.12.0/24, rev 10
        Local binding: label: ImpNull
        Remote bindings: (2 peers)
            Peer                Label
            -----------------   ---------
            100.64.0.2:0        ImpNull
            100.64.0.3:0        24009
192.168.13.0/24, rev 9
        Local binding: label: ImpNull
        Remote bindings: (2 peers)
            Peer                Label
            -----------------   ---------
            100.64.0.2:0        24009
            100.64.0.3:0        ImpNull
192.168.23.0/24, rev 12
        Local binding: label: 24009
        Remote bindings: (2 peers)
            Peer                Label
            -----------------   ---------
            100.64.0.2:0        ImpNull
            100.64.0.3:0        ImpNull

RP/0/RP0/CPU0:cisco-kudo-11#
RP/0/RP0/CPU0:cisco-kudo-11#
RP/0/RP0/CPU0:cisco-kudo-11#
RP/0/RP0/CPU0:cisco-kudo-11#show cef vrf all
Sun Dec 27 04:30:03.641 UTC

VRF: MGMT
_____________

Prefix              Next Hop            Interface
------------------- ------------------- ------------------
0.0.0.0/0           drop                default handler
0.0.0.0/32          broadcast
10.10.0.0/24        attached            MgmtEth0/RP0/CPU0/0
10.10.0.0/32        broadcast           MgmtEth0/RP0/CPU0/0
10.10.0.1/32        10.10.0.1/32        MgmtEth0/RP0/CPU0/0
10.10.0.38/32       10.10.0.38/32       MgmtEth0/RP0/CPU0/0
10.10.0.39/32       10.10.0.39/32       MgmtEth0/RP0/CPU0/0
10.10.0.41/32       receive             MgmtEth0/RP0/CPU0/0
10.10.0.45/32       10.10.0.45/32       MgmtEth0/RP0/CPU0/0
10.10.0.255/32      broadcast           MgmtEth0/RP0/CPU0/0
224.0.0.0/4         0.0.0.0/32
224.0.0.0/24        receive
255.255.255.255/32  broadcast

VRF: UG-A
_____________

Prefix              Next Hop            Interface
------------------- ------------------- ------------------
0.0.0.0/0           drop                default handler
0.0.0.0/32          broadcast
100.64.10.1/32      receive             Loopback10
100.64.10.2/32      100.64.0.2/32       <recursive>
100.64.10.3/32      100.64.0.3/32       <recursive>
100.64.10.4/32      100.64.0.3/32       <recursive>
100.64.10.5/32      100.64.0.3/32       <recursive>
100.64.10.6/32      100.64.0.3/32       <recursive>
100.64.10.18/32     172.24.18.8/32      <recursive>
100.64.10.19/32     100.64.0.3/32       <recursive>
100.64.10.28/32     100.64.0.2/32       <recursive>
100.64.10.29/32     100.64.0.3/32       <recursive>
172.24.18.0/24      attached            GigabitEthernet0/0/0/0.18
172.24.18.0/32      broadcast           GigabitEthernet0/0/0/0.18
172.24.18.1/32      receive             GigabitEthernet0/0/0/0.18
172.24.18.8/32      172.24.18.8/32      GigabitEthernet0/0/0/0.18
172.24.18.255/32    broadcast           GigabitEthernet0/0/0/0.18
172.24.19.0/24      100.64.0.3/32       <recursive>
172.24.28.0/24      100.64.0.2/32       <recursive>
172.24.29.0/24      100.64.0.3/32       <recursive>
224.0.0.0/4         0.0.0.0/32
224.0.0.0/24        receive
255.255.255.255/32  broadcast

VRF: UG-B
_____________

Prefix              Next Hop            Interface
------------------- ------------------- ------------------
0.0.0.0/0           drop                default handler
0.0.0.0/32          broadcast
100.64.20.1/32      receive             Loopback20
100.64.20.2/32      100.64.0.2/32       <recursive>
100.64.20.3/32      100.64.0.3/32       <recursive>
100.64.20.4/32      100.64.0.3/32       <recursive>
100.64.20.5/32      100.64.0.3/32       <recursive>
100.64.20.6/32      100.64.0.3/32       <recursive>
100.64.20.38/32     172.24.38.8/32      <recursive>
100.64.20.39/32     100.64.0.3/32       <recursive>
100.64.20.48/32     100.64.0.2/32       <recursive>
100.64.20.49/32     100.64.0.3/32       <recursive>
172.24.38.0/24      attached            GigabitEthernet0/0/0/0.38
172.24.38.0/32      broadcast           GigabitEthernet0/0/0/0.38
172.24.38.1/32      receive             GigabitEthernet0/0/0/0.38
172.24.38.8/32      172.24.38.8/32      GigabitEthernet0/0/0/0.38
172.24.38.255/32    broadcast           GigabitEthernet0/0/0/0.38
172.24.39.0/24      100.64.0.3/32       <recursive>
172.24.48.0/24      100.64.0.2/32       <recursive>
172.24.49.0/24      100.64.0.3/32       <recursive>
224.0.0.0/4         0.0.0.0/32
224.0.0.0/24        receive
255.255.255.255/32  broadcast

VRF: default
_____________

Prefix              Next Hop            Interface
------------------- ------------------- ------------------
0.0.0.0/0           drop                default handler
0.0.0.0/32          broadcast
100.64.0.1/32       receive             Loopback1
100.64.0.2/32       192.168.12.2/32     GigabitEthernet0/0/0/0.12
                    192.168.13.3/32     GigabitEthernet0/0/0/0.13 (!)
100.64.0.3/32       192.168.12.2/32     GigabitEthernet0/0/0/0.12 (!)
                    192.168.13.3/32     GigabitEthernet0/0/0/0.13
192.168.12.0/24     attached            GigabitEthernet0/0/0/0.12
192.168.12.0/32     broadcast           GigabitEthernet0/0/0/0.12
192.168.12.1/32     receive             GigabitEthernet0/0/0/0.12
192.168.12.255/32   broadcast           GigabitEthernet0/0/0/0.12
192.168.13.0/24     attached            GigabitEthernet0/0/0/0.13
192.168.13.0/32     broadcast           GigabitEthernet0/0/0/0.13
192.168.13.1/32     receive             GigabitEthernet0/0/0/0.13
192.168.13.255/32   broadcast           GigabitEthernet0/0/0/0.13
192.168.23.0/24     192.168.12.2/32     GigabitEthernet0/0/0/0.12
                    192.168.13.3/32     GigabitEthernet0/0/0/0.13
224.0.0.0/4         0.0.0.0/32
224.0.0.0/24        receive
255.255.255.255/32  broadcast
RP/0/RP0/CPU0:cisco-kudo-11#
RP/0/RP0/CPU0:cisco-kudo-11#
RP/0/RP0/CPU0:cisco-kudo-11#
RP/0/RP0/CPU0:cisco-kudo-11#show mpls forwarding
Sun Dec 27 04:30:37.536 UTC
Local  Outgoing    Prefix             Outgoing     Next Hop        Bytes
Label  Label       or ID              Interface                    Switched
------ ----------- ------------------ ------------ --------------- ------------
15012  Pop         SRLB (idx 12)      Gi0/0/0/0.12 192.168.12.2    0
15013  Pop         SRLB (idx 13)      Gi0/0/0/0.13 192.168.13.3    0
17002  Pop         SR Pfx (idx 1002)  Gi0/0/0/0.12 192.168.12.2    15679
       17002       SR Pfx (idx 1002)  Gi0/0/0/0.13 192.168.13.3    0            (!)
17003  Pop         SR Pfx (idx 1003)  Gi0/0/0/0.13 192.168.13.3    15679
       17003       SR Pfx (idx 1003)  Gi0/0/0/0.12 192.168.12.2    0            (!)
24000  Pop         SR Adj (idx 0)     Gi0/0/0/0.12 192.168.12.2    0
       17002       SR Adj (idx 0)     Gi0/0/0/0.13 192.168.13.3    0            (!)
24001  Pop         SR Adj (idx 2)     Gi0/0/0/0.12 192.168.12.2    0
24002  Pop         SR Adj (idx 1)     Gi0/0/0/0.12 192.168.12.2    0
       17002       SR Adj (idx 1)     Gi0/0/0/0.13 192.168.13.3    0            (!)
24003  Pop         SR Adj (idx 3)     Gi0/0/0/0.12 192.168.12.2    0
24004  Pop         SR Adj (idx 0)     Gi0/0/0/0.13 192.168.13.3    0
       17003       SR Adj (idx 0)     Gi0/0/0/0.12 192.168.12.2    0            (!)
24005  Pop         SR Adj (idx 2)     Gi0/0/0/0.13 192.168.13.3    0
24006  Pop         SR Adj (idx 1)     Gi0/0/0/0.13 192.168.13.3    0
       17003       SR Adj (idx 1)     Gi0/0/0/0.12 192.168.12.2    0            (!)
24007  Pop         SR Adj (idx 3)     Gi0/0/0/0.13 192.168.13.3    0
24008  Pop         100.64.0.2/32      Gi0/0/0/0.12 192.168.12.2    1565116
       24010       100.64.0.2/32      Gi0/0/0/0.13 192.168.13.3    0            (!)
24009  Pop         192.168.23.0/24    Gi0/0/0/0.12 192.168.12.2    0
       Pop         192.168.23.0/24    Gi0/0/0/0.13 192.168.13.3    0
24010  Pop         100.64.0.3/32      Gi0/0/0/0.13 192.168.13.3    1570887
       24010       100.64.0.3/32      Gi0/0/0/0.12 192.168.12.2    0            (!)
24011  Aggregate   UG-A: Per-VRF Aggr[V]   \
                                      UG-A                         2520
24012  24011       100.64.10.2/32[V]               100.64.0.2      520
24013  24011       100.64.10.3/32[V]               100.64.0.3      1040
24014  24011       172.24.28.0/24[V]               100.64.0.2      0
24015  Aggregate   UG-B: Per-VRF Aggr[V]   \
                                      UG-B                         96
24016  Unlabelled  100.64.10.18/32[V] Gi0/0/0/0.18 172.24.18.8     0
24017  Unlabelled  100.64.20.38/32[V] Gi0/0/0/0.38 172.24.38.8     0
24018  24016       100.64.10.28/32[V]              100.64.0.2      0
24019  24039       100.64.10.4/32[V]               100.64.0.3      0
24020  24040       100.64.10.5/32[V]               100.64.0.3      0
24021  24043       100.64.10.6/32[V]               100.64.0.3      0
24022  24041       100.64.10.19/32[V]              100.64.0.3      0
24023  24044       100.64.10.29/32[V]              100.64.0.3      0
24024  24042       172.24.19.0/24[V]               100.64.0.3      0
24025  24045       172.24.29.0/24[V]               100.64.0.3      0
RP/0/RP0/CPU0:cisco-kudo-11#
RP/0/RP0/CPU0:cisco-kudo-11#
RP/0/RP0/CPU0:cisco-kudo-11#
```


