## XRv-11 (.1): 
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

## XRv-12 (.2): 
```


RP/0/RP0/CPU0:cisco-kudo-12#

RP/0/RP0/CPU0:cisco-kudo-12#show route

Sun Dec 27 04:37:53.779 UTC

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

i L1 100.64.0.1/32 [115/10] via 192.168.12.1, 2d03h, GigabitEthernet0/0/0/0.12
                   [115/20] via 192.168.23.3, 2d03h, GigabitEthernet0/0/0/0.23 (!)
L    100.64.0.2/32 is directly connected, 2d03h, Loopback2
i L1 100.64.0.3/32 [115/20] via 192.168.12.1, 2d03h, GigabitEthernet0/0/0/0.12 (!)
                   [115/10] via 192.168.23.3, 2d03h, GigabitEthernet0/0/0/0.23
C    192.168.12.0/24 is directly connected, 2d03h, GigabitEthernet0/0/0/0.12
L    192.168.12.2/32 is directly connected, 2d03h, GigabitEthernet0/0/0/0.12
i L1 192.168.13.0/24 [115/20] via 192.168.12.1, 2d03h, GigabitEthernet0/0/0/0.12
                     [115/20] via 192.168.23.3, 2d03h, GigabitEthernet0/0/0/0.23
C    192.168.23.0/24 is directly connected, 2d03h, GigabitEthernet0/0/0/0.23
L    192.168.23.2/32 is directly connected, 2d03h, GigabitEthernet0/0/0/0.23
RP/0/RP0/CPU0:cisco-kudo-12#

RP/0/RP0/CPU0:cisco-kudo-12#

RP/0/RP0/CPU0:cisco-kudo-12#show route vrf all

Sun Dec 27 04:37:55.867 UTC

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
L    10.10.0.42/32 is directly connected, 2d03h, MgmtEth0/RP0/CPU0/0

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

B    100.64.10.1/32 [200/0] via 100.64.0.1 (nexthop in vrf default), 2d03h
L    100.64.10.2/32 is directly connected, 2d03h, Loopback10
B    100.64.10.3/32 [200/0] via 100.64.0.3 (nexthop in vrf default), 1d22h
B    100.64.10.4/32 [200/0] via 100.64.0.3 (nexthop in vrf default), 02:50:50
B    100.64.10.5/32 [200/0] via 100.64.0.3 (nexthop in vrf default), 02:50:50
B    100.64.10.6/32 [200/0] via 100.64.0.3 (nexthop in vrf default), 02:50:50
B    100.64.10.18/32 [200/0] via 100.64.0.1 (nexthop in vrf default), 2d03h
B    100.64.10.19/32 [200/0] via 100.64.0.3 (nexthop in vrf default), 01:08:55
B    100.64.10.28/32 [20/0] via 172.24.28.8, 2d03h
B    100.64.10.29/32 [200/0] via 100.64.0.3 (nexthop in vrf default), 01:08:25
B    172.24.18.0/24 [200/0] via 100.64.0.1 (nexthop in vrf default), 2d03h
B    172.24.19.0/24 [200/0] via 100.64.0.3 (nexthop in vrf default), 02:50:50
C    172.24.28.0/24 is directly connected, 2d03h, GigabitEthernet0/0/0/0.28
L    172.24.28.2/32 is directly connected, 2d03h, GigabitEthernet0/0/0/0.28
B    172.24.29.0/24 [200/0] via 100.64.0.3 (nexthop in vrf default), 02:50:50

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

B    100.64.20.1/32 [200/0] via 100.64.0.1 (nexthop in vrf default), 2d03h
L    100.64.20.2/32 is directly connected, 2d03h, Loopback20
B    100.64.20.3/32 [200/0] via 100.64.0.3 (nexthop in vrf default), 1d22h
B    100.64.20.4/32 [200/0] via 100.64.0.3 (nexthop in vrf default), 02:50:50
B    100.64.20.5/32 [200/0] via 100.64.0.3 (nexthop in vrf default), 02:50:50
B    100.64.20.6/32 [200/0] via 100.64.0.3 (nexthop in vrf default), 02:50:50
B    100.64.20.38/32 [200/0] via 100.64.0.1 (nexthop in vrf default), 2d03h
B    100.64.20.39/32 [200/0] via 100.64.0.3 (nexthop in vrf default), 01:08:55
B    100.64.20.48/32 [20/0] via 172.24.48.8, 2d03h
B    100.64.20.49/32 [200/0] via 100.64.0.3 (nexthop in vrf default), 01:08:25
B    172.24.38.0/24 [200/0] via 100.64.0.1 (nexthop in vrf default), 2d03h
B    172.24.39.0/24 [200/0] via 100.64.0.3 (nexthop in vrf default), 02:50:50
C    172.24.48.0/24 is directly connected, 2d03h, GigabitEthernet0/0/0/0.48
L    172.24.48.2/32 is directly connected, 2d03h, GigabitEthernet0/0/0/0.48
B    172.24.49.0/24 [200/0] via 100.64.0.3 (nexthop in vrf default), 02:50:50
RP/0/RP0/CPU0:cisco-kudo-12#

RP/0/RP0/CPU0:cisco-kudo-12#

RP/0/RP0/CPU0:cisco-kudo-12#show mpls ldp bindings

Sun Dec 27 04:37:58.976 UTC

100.64.0.1/32, rev 11
	Local binding: label: 24008
	Remote bindings: (2 peers)
	    Peer                Label    
	    -----------------   ---------
	    100.64.0.1:0        ImpNull 
	    100.64.0.3:0        24008   
100.64.0.2/32, rev 8
	Local binding: label: ImpNull
	Remote bindings: (2 peers)
	    Peer                Label    
	    -----------------   ---------
	    100.64.0.1:0        24008   
	    100.64.0.3:0        24010   
100.64.0.3/32, rev 13
	Local binding: label: 24010
	Remote bindings: (2 peers)
	    Peer                Label    
	    -----------------   ---------
	    100.64.0.1:0        24010   
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
	    100.64.0.1:0        ImpNull 
	    100.64.0.3:0        24009   
192.168.13.0/24, rev 12
	Local binding: label: 24009
	Remote bindings: (2 peers)
	    Peer                Label    
	    -----------------   ---------
	    100.64.0.1:0        ImpNull 
	    100.64.0.3:0        ImpNull 
192.168.23.0/24, rev 9
	Local binding: label: ImpNull
	Remote bindings: (2 peers)
	    Peer                Label    
	    -----------------   ---------
	    100.64.0.1:0        24009   
	    100.64.0.3:0        ImpNull 

RP/0/RP0/CPU0:cisco-kudo-12#

RP/0/RP0/CPU0:cisco-kudo-12#

RP/0/RP0/CPU0:cisco-kudo-12#show cef vrf all

Sun Dec 27 04:38:01.008 UTC

VRF: MGMT
_____________

Prefix              Next Hop            Interface
------------------- ------------------- ------------------
0.0.0.0/0           drop                default handler 
0.0.0.0/32          broadcast
10.10.0.0/24        attached            MgmtEth0/RP0/CPU0/0
10.10.0.0/32        broadcast           MgmtEth0/RP0/CPU0/0
10.10.0.1/32        10.10.0.1/32        MgmtEth0/RP0/CPU0/0
10.10.0.30/32       10.10.0.30/32       MgmtEth0/RP0/CPU0/0
10.10.0.38/32       10.10.0.38/32       MgmtEth0/RP0/CPU0/0
10.10.0.39/32       10.10.0.39/32       MgmtEth0/RP0/CPU0/0
10.10.0.41/32       10.10.0.41/32       MgmtEth0/RP0/CPU0/0
10.10.0.42/32       receive             MgmtEth0/RP0/CPU0/0
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
100.64.10.1/32      100.64.0.1/32       <recursive>
100.64.10.2/32      receive             Loopback10
100.64.10.3/32      100.64.0.3/32       <recursive>
100.64.10.4/32      100.64.0.3/32       <recursive>
100.64.10.5/32      100.64.0.3/32       <recursive>
100.64.10.6/32      100.64.0.3/32       <recursive>
100.64.10.18/32     100.64.0.1/32       <recursive>
100.64.10.19/32     100.64.0.3/32       <recursive>
100.64.10.28/32     172.24.28.8/32      <recursive>
100.64.10.29/32     100.64.0.3/32       <recursive>
172.24.18.0/24      100.64.0.1/32       <recursive>
172.24.19.0/24      100.64.0.3/32       <recursive>
172.24.28.0/24      attached            GigabitEthernet0/0/0/0.28
172.24.28.0/32      broadcast           GigabitEthernet0/0/0/0.28
172.24.28.2/32      receive             GigabitEthernet0/0/0/0.28
172.24.28.8/32      172.24.28.8/32      GigabitEthernet0/0/0/0.28
172.24.28.255/32    broadcast           GigabitEthernet0/0/0/0.28
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
100.64.20.1/32      100.64.0.1/32       <recursive>
100.64.20.2/32      receive             Loopback20
100.64.20.3/32      100.64.0.3/32       <recursive>
100.64.20.4/32      100.64.0.3/32       <recursive>
100.64.20.5/32      100.64.0.3/32       <recursive>
100.64.20.6/32      100.64.0.3/32       <recursive>
100.64.20.38/32     100.64.0.1/32       <recursive>
100.64.20.39/32     100.64.0.3/32       <recursive>
100.64.20.48/32     172.24.48.8/32      <recursive>
100.64.20.49/32     100.64.0.3/32       <recursive>
172.24.38.0/24      100.64.0.1/32       <recursive>
172.24.39.0/24      100.64.0.3/32       <recursive>
172.24.48.0/24      attached            GigabitEthernet0/0/0/0.48
172.24.48.0/32      broadcast           GigabitEthernet0/0/0/0.48
172.24.48.2/32      receive             GigabitEthernet0/0/0/0.48
172.24.48.8/32      172.24.48.8/32      GigabitEthernet0/0/0/0.48
172.24.48.255/32    broadcast           GigabitEthernet0/0/0/0.48
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
100.64.0.1/32       192.168.12.1/32     GigabitEthernet0/0/0/0.12
                    192.168.23.3/32     GigabitEthernet0/0/0/0.23 (!)
100.64.0.2/32       receive             Loopback2
100.64.0.3/32       192.168.12.1/32     GigabitEthernet0/0/0/0.12 (!)
                    192.168.23.3/32     GigabitEthernet0/0/0/0.23
192.168.12.0/24     attached            GigabitEthernet0/0/0/0.12
192.168.12.0/32     broadcast           GigabitEthernet0/0/0/0.12
192.168.12.2/32     receive             GigabitEthernet0/0/0/0.12
192.168.12.255/32   broadcast           GigabitEthernet0/0/0/0.12
192.168.13.0/24     192.168.12.1/32     GigabitEthernet0/0/0/0.12
                    192.168.23.3/32     GigabitEthernet0/0/0/0.23
192.168.23.0/24     attached            GigabitEthernet0/0/0/0.23
192.168.23.0/32     broadcast           GigabitEthernet0/0/0/0.23
192.168.23.2/32     receive             GigabitEthernet0/0/0/0.23
192.168.23.255/32   broadcast           GigabitEthernet0/0/0/0.23
224.0.0.0/4         0.0.0.0/32          
224.0.0.0/24        receive
255.255.255.255/32  broadcast
RP/0/RP0/CPU0:cisco-kudo-12#

RP/0/RP0/CPU0:cisco-kudo-12#

RP/0/RP0/CPU0:cisco-kudo-12#show mpls forwarding

Sun Dec 27 04:38:04.165 UTC
Local  Outgoing    Prefix             Outgoing     Next Hop        Bytes       
Label  Label       or ID              Interface                    Switched    
------ ----------- ------------------ ------------ --------------- ------------
15012  Pop         SRLB (idx 12)      Gi0/0/0/0.12 192.168.12.1    0           
15023  Pop         SRLB (idx 23)      Gi0/0/0/0.23 192.168.23.3    0           
17001  Pop         SR Pfx (idx 1001)  Gi0/0/0/0.12 192.168.12.1    15817       
       17001       SR Pfx (idx 1001)  Gi0/0/0/0.23 192.168.23.3    0            (!)
17003  Pop         SR Pfx (idx 1003)  Gi0/0/0/0.23 192.168.23.3    15976       
       17003       SR Pfx (idx 1003)  Gi0/0/0/0.12 192.168.12.1    0            (!)
24000  Pop         SR Adj (idx 0)     Gi0/0/0/0.23 192.168.23.3    0           
       17003       SR Adj (idx 0)     Gi0/0/0/0.12 192.168.12.1    0            (!)
24001  Pop         SR Adj (idx 2)     Gi0/0/0/0.23 192.168.23.3    0           
24002  Pop         SR Adj (idx 1)     Gi0/0/0/0.23 192.168.23.3    0           
       17003       SR Adj (idx 1)     Gi0/0/0/0.12 192.168.12.1    0            (!)
24003  Pop         SR Adj (idx 3)     Gi0/0/0/0.23 192.168.23.3    0           
24004  Pop         SR Adj (idx 0)     Gi0/0/0/0.12 192.168.12.1    0           
       17001       SR Adj (idx 0)     Gi0/0/0/0.23 192.168.23.3    0            (!)
24005  Pop         SR Adj (idx 2)     Gi0/0/0/0.12 192.168.12.1    0           
24006  Pop         SR Adj (idx 1)     Gi0/0/0/0.12 192.168.12.1    0           
       17001       SR Adj (idx 1)     Gi0/0/0/0.23 192.168.23.3    0            (!)
24007  Pop         SR Adj (idx 3)     Gi0/0/0/0.12 192.168.12.1    0           
24008  Pop         100.64.0.1/32      Gi0/0/0/0.12 192.168.12.1    1569044     
       24008       100.64.0.1/32      Gi0/0/0/0.23 192.168.23.3    0            (!)
24009  Pop         192.168.13.0/24    Gi0/0/0/0.12 192.168.12.1    0           
       Pop         192.168.13.0/24    Gi0/0/0/0.23 192.168.23.3    0           
24010  Pop         100.64.0.3/32      Gi0/0/0/0.23 192.168.23.3    1569555     
       24010       100.64.0.3/32      Gi0/0/0/0.12 192.168.12.1    0            (!)
24011  Aggregate   UG-A: Per-VRF Aggr[V]   \
                                      UG-A                         2040        
24012  24011       100.64.10.3/32[V]               100.64.0.3      520         
24013  Aggregate   UG-B: Per-VRF Aggr[V]   \
                                      UG-B                         0           
24014  24011       100.64.10.1/32[V]               100.64.0.1      520         
24015  24011       172.24.18.0/24[V]               100.64.0.1      0           
24016  Unlabelled  100.64.10.28/32[V] Gi0/0/0/0.28 172.24.28.8     0           
24017  Unlabelled  100.64.20.48/32[V] Gi0/0/0/0.48 172.24.48.8     0           
24018  24016       100.64.10.18/32[V]              100.64.0.1      0           
24019  24039       100.64.10.4/32[V]               100.64.0.3      0           
24020  24040       100.64.10.5/32[V]               100.64.0.3      0           
24021  24043       100.64.10.6/32[V]               100.64.0.3      0           
24022  24041       100.64.10.19/32[V]              100.64.0.3      0           
24023  24044       100.64.10.29/32[V]              100.64.0.3      0           
24024  24042       172.24.19.0/24[V]               100.64.0.3      0           
24025  24045       172.24.29.0/24[V]               100.64.0.3      0           
RP/0/RP0/CPU0:cisco-kudo-12#
```


## XRv-13 (.3): 
```


RP/0/RP0/CPU0:cisco-kudo-13#

RP/0/RP0/CPU0:cisco-kudo-13#show route

Sun Dec 27 04:37:58.326 UTC

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

i L1 100.64.0.1/32 [115/10] via 192.168.13.1, 2d03h, GigabitEthernet0/0/0/0.13
                   [115/20] via 192.168.23.2, 2d03h, GigabitEthernet0/0/0/0.23 (!)
i L1 100.64.0.2/32 [115/20] via 192.168.13.1, 2d03h, GigabitEthernet0/0/0/0.13 (!)
                   [115/10] via 192.168.23.2, 2d03h, GigabitEthernet0/0/0/0.23
L    100.64.0.3/32 is directly connected, 2d03h, Loopback3
C    172.24.34.0/24 is directly connected, 2d03h, GigabitEthernet0/0/0/0.34
L    172.24.34.3/32 is directly connected, 2d03h, GigabitEthernet0/0/0/0.34
S    172.24.34.4/32 is directly connected, 00:52:48, GigabitEthernet0/0/0/0.34
i L1 192.168.12.0/24 [115/20] via 192.168.13.1, 2d03h, GigabitEthernet0/0/0/0.13
                     [115/20] via 192.168.23.2, 2d03h, GigabitEthernet0/0/0/0.23
C    192.168.13.0/24 is directly connected, 2d03h, GigabitEthernet0/0/0/0.13
L    192.168.13.3/32 is directly connected, 2d03h, GigabitEthernet0/0/0/0.13
C    192.168.23.0/24 is directly connected, 2d03h, GigabitEthernet0/0/0/0.23
L    192.168.23.3/32 is directly connected, 2d03h, GigabitEthernet0/0/0/0.23
RP/0/RP0/CPU0:cisco-kudo-13#

RP/0/RP0/CPU0:cisco-kudo-13#

RP/0/RP0/CPU0:cisco-kudo-13#show route vrf all

Sun Dec 27 04:38:00.292 UTC

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
L    10.10.0.43/32 is directly connected, 2d03h, MgmtEth0/RP0/CPU0/0

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

B    100.64.10.1/32 [200/0] via 100.64.0.1 (nexthop in vrf default), 1d22h
B    100.64.10.2/32 [200/0] via 100.64.0.2 (nexthop in vrf default), 1d22h
L    100.64.10.3/32 is directly connected, 2d03h, Loopback10
B    100.64.10.4/32 [20/0] via 172.24.34.4 (nexthop in vrf default), 02:50:55
B    100.64.10.5/32 [20/0] via 172.24.34.4 (nexthop in vrf default), 02:50:55
B    100.64.10.6/32 [20/0] via 172.24.34.4 (nexthop in vrf default), 02:50:55
B    100.64.10.18/32 [200/0] via 100.64.0.1 (nexthop in vrf default), 1d22h
B    100.64.10.19/32 [20/0] via 172.24.34.4 (nexthop in vrf default), 01:09:00
B    100.64.10.28/32 [200/0] via 100.64.0.2 (nexthop in vrf default), 1d22h
B    100.64.10.29/32 [20/0] via 172.24.34.4 (nexthop in vrf default), 01:08:30
B    172.24.18.0/24 [200/0] via 100.64.0.1 (nexthop in vrf default), 1d22h
B    172.24.19.0/24 [20/0] via 172.24.34.4 (nexthop in vrf default), 02:50:55
B    172.24.28.0/24 [200/0] via 100.64.0.2 (nexthop in vrf default), 1d22h
B    172.24.29.0/24 [20/0] via 172.24.34.4 (nexthop in vrf default), 02:50:55

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

B    100.64.20.1/32 [200/0] via 100.64.0.1 (nexthop in vrf default), 1d22h
B    100.64.20.2/32 [200/0] via 100.64.0.2 (nexthop in vrf default), 1d22h
L    100.64.20.3/32 is directly connected, 2d03h, Loopback20
B    100.64.20.4/32 [20/0] via 172.24.34.4 (nexthop in vrf default), 02:50:55
B    100.64.20.5/32 [20/0] via 172.24.34.4 (nexthop in vrf default), 02:50:55
B    100.64.20.6/32 [20/0] via 172.24.34.4 (nexthop in vrf default), 02:50:55
B    100.64.20.38/32 [200/0] via 100.64.0.1 (nexthop in vrf default), 1d22h
B    100.64.20.39/32 [20/0] via 172.24.34.4 (nexthop in vrf default), 01:09:00
B    100.64.20.48/32 [200/0] via 100.64.0.2 (nexthop in vrf default), 1d22h
B    100.64.20.49/32 [20/0] via 172.24.34.4 (nexthop in vrf default), 01:08:31
B    172.24.38.0/24 [200/0] via 100.64.0.1 (nexthop in vrf default), 1d22h
B    172.24.39.0/24 [20/0] via 172.24.34.4 (nexthop in vrf default), 02:50:55
B    172.24.48.0/24 [200/0] via 100.64.0.2 (nexthop in vrf default), 1d22h
B    172.24.49.0/24 [20/0] via 172.24.34.4 (nexthop in vrf default), 02:50:55
RP/0/RP0/CPU0:cisco-kudo-13#

RP/0/RP0/CPU0:cisco-kudo-13#

RP/0/RP0/CPU0:cisco-kudo-13#show mpls ldp bindings

Sun Dec 27 04:38:03.402 UTC

100.64.0.1/32, rev 12
	Local binding: label: 24008
	Remote bindings: (2 peers)
	    Peer                Label    
	    -----------------   ---------
	    100.64.0.1:0        ImpNull 
	    100.64.0.2:0        24008   
100.64.0.2/32, rev 14
	Local binding: label: 24010
	Remote bindings: (2 peers)
	    Peer                Label    
	    -----------------   ---------
	    100.64.0.1:0        24008   
	    100.64.0.2:0        ImpNull 
100.64.0.3/32, rev 2
	Local binding: label: ImpNull
	Remote bindings: (2 peers)
	    Peer                Label    
	    -----------------   ---------
	    100.64.0.1:0        24010   
	    100.64.0.2:0        24010   
172.24.34.0/24, rev 4
	Local binding: label: ImpNull
	No remote bindings
172.24.34.4/32, rev 16
	Local binding: label: 24053
	No remote bindings
192.168.12.0/24, rev 13
	Local binding: label: 24009
	Remote bindings: (2 peers)
	    Peer                Label    
	    -----------------   ---------
	    100.64.0.1:0        ImpNull 
	    100.64.0.2:0        ImpNull 
192.168.13.0/24, rev 8
	Local binding: label: ImpNull
	Remote bindings: (2 peers)
	    Peer                Label    
	    -----------------   ---------
	    100.64.0.1:0        ImpNull 
	    100.64.0.2:0        24009   
192.168.23.0/24, rev 6
	Local binding: label: ImpNull
	Remote bindings: (2 peers)
	    Peer                Label    
	    -----------------   ---------
	    100.64.0.1:0        24009   
	    100.64.0.2:0        ImpNull 

RP/0/RP0/CPU0:cisco-kudo-13#

RP/0/RP0/CPU0:cisco-kudo-13#

RP/0/RP0/CPU0:cisco-kudo-13#show cef vrf all

Sun Dec 27 04:38:05.561 UTC

VRF: MGMT
_____________

Prefix              Next Hop            Interface
------------------- ------------------- ------------------
0.0.0.0/0           drop                default handler 
0.0.0.0/32          broadcast
10.10.0.0/24        attached            MgmtEth0/RP0/CPU0/0
10.10.0.0/32        broadcast           MgmtEth0/RP0/CPU0/0
10.10.0.1/32        10.10.0.1/32        MgmtEth0/RP0/CPU0/0
10.10.0.30/32       10.10.0.30/32       MgmtEth0/RP0/CPU0/0
10.10.0.31/32       10.10.0.31/32       MgmtEth0/RP0/CPU0/0
10.10.0.38/32       10.10.0.38/32       MgmtEth0/RP0/CPU0/0
10.10.0.39/32       10.10.0.39/32       MgmtEth0/RP0/CPU0/0
10.10.0.41/32       10.10.0.41/32       MgmtEth0/RP0/CPU0/0
10.10.0.42/32       10.10.0.42/32       MgmtEth0/RP0/CPU0/0
10.10.0.43/32       receive             MgmtEth0/RP0/CPU0/0
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
100.64.10.1/32      100.64.0.1/32       <recursive>
100.64.10.2/32      100.64.0.2/32       <recursive>
100.64.10.3/32      receive             Loopback10
100.64.10.4/32      172.24.34.4/32      <recursive>
100.64.10.5/32      172.24.34.4/32      <recursive>
100.64.10.6/32      172.24.34.4/32      <recursive>
100.64.10.18/32     100.64.0.1/32       <recursive>
100.64.10.19/32     172.24.34.4/32      <recursive>
100.64.10.28/32     100.64.0.2/32       <recursive>
100.64.10.29/32     172.24.34.4/32      <recursive>
172.24.18.0/24      100.64.0.1/32       <recursive>
172.24.19.0/24      172.24.34.4/32      <recursive>
172.24.28.0/24      100.64.0.2/32       <recursive>
172.24.29.0/24      172.24.34.4/32      <recursive>
224.0.0.0/4         0.0.0.0/32          
224.0.0.0/24        receive
255.255.255.255/32  broadcast

VRF: UG-B
_____________

Prefix              Next Hop            Interface
------------------- ------------------- ------------------
0.0.0.0/0           drop                default handler 
0.0.0.0/32          broadcast
100.64.20.1/32      100.64.0.1/32       <recursive>
100.64.20.2/32      100.64.0.2/32       <recursive>
100.64.20.3/32      receive             Loopback20
100.64.20.4/32      172.24.34.4/32      <recursive>
100.64.20.5/32      172.24.34.4/32      <recursive>
100.64.20.6/32      172.24.34.4/32      <recursive>
100.64.20.38/32     100.64.0.1/32       <recursive>
100.64.20.39/32     172.24.34.4/32      <recursive>
100.64.20.48/32     100.64.0.2/32       <recursive>
100.64.20.49/32     172.24.34.4/32      <recursive>
172.24.38.0/24      100.64.0.1/32       <recursive>
172.24.39.0/24      172.24.34.4/32      <recursive>
172.24.48.0/24      100.64.0.2/32       <recursive>
172.24.49.0/24      172.24.34.4/32      <recursive>
224.0.0.0/4         0.0.0.0/32          
224.0.0.0/24        receive
255.255.255.255/32  broadcast

VRF: default
_____________

Prefix              Next Hop            Interface
------------------- ------------------- ------------------
0.0.0.0/0           drop                default handler 
0.0.0.0/32          broadcast
100.64.0.1/32       192.168.13.1/32     GigabitEthernet0/0/0/0.13
                    192.168.23.2/32     GigabitEthernet0/0/0/0.23 (!)
100.64.0.2/32       192.168.13.1/32     GigabitEthernet0/0/0/0.13 (!)
                    192.168.23.2/32     GigabitEthernet0/0/0/0.23
100.64.0.3/32       receive             Loopback3
172.24.34.0/24      attached            GigabitEthernet0/0/0/0.34
172.24.34.0/32      broadcast           GigabitEthernet0/0/0/0.34
172.24.34.3/32      receive             GigabitEthernet0/0/0/0.34
172.24.34.4/32      attached            GigabitEthernet0/0/0/0.34
172.24.34.255/32    broadcast           GigabitEthernet0/0/0/0.34
192.168.12.0/24     192.168.13.1/32     GigabitEthernet0/0/0/0.13
                    192.168.23.2/32     GigabitEthernet0/0/0/0.23
192.168.13.0/24     attached            GigabitEthernet0/0/0/0.13
192.168.13.0/32     broadcast           GigabitEthernet0/0/0/0.13
192.168.13.3/32     receive             GigabitEthernet0/0/0/0.13
192.168.13.255/32   broadcast           GigabitEthernet0/0/0/0.13
192.168.23.0/24     attached            GigabitEthernet0/0/0/0.23
192.168.23.0/32     broadcast           GigabitEthernet0/0/0/0.23
192.168.23.3/32     receive             GigabitEthernet0/0/0/0.23
192.168.23.255/32   broadcast           GigabitEthernet0/0/0/0.23
224.0.0.0/4         0.0.0.0/32          
224.0.0.0/24        receive
255.255.255.255/32  broadcast
RP/0/RP0/CPU0:cisco-kudo-13#

RP/0/RP0/CPU0:cisco-kudo-13#

RP/0/RP0/CPU0:cisco-kudo-13#show mpls forwarding

Sun Dec 27 04:38:08.534 UTC
Local  Outgoing    Prefix             Outgoing     Next Hop        Bytes       
Label  Label       or ID              Interface                    Switched    
------ ----------- ------------------ ------------ --------------- ------------
15013  Pop         SRLB (idx 13)      Gi0/0/0/0.13 192.168.13.1    0           
15023  Pop         SRLB (idx 23)      Gi0/0/0/0.23 192.168.23.2    0           
17001  Pop         SR Pfx (idx 1001)  Gi0/0/0/0.13 192.168.13.1    16898       
       17001       SR Pfx (idx 1001)  Gi0/0/0/0.23 192.168.23.2    0            (!)
17002  Pop         SR Pfx (idx 1002)  Gi0/0/0/0.23 192.168.23.2    16758       
       17002       SR Pfx (idx 1002)  Gi0/0/0/0.13 192.168.13.1    0            (!)
24000  Pop         SR Adj (idx 0)     Gi0/0/0/0.23 192.168.23.2    0           
       17002       SR Adj (idx 0)     Gi0/0/0/0.13 192.168.13.1    0            (!)
24001  Pop         SR Adj (idx 2)     Gi0/0/0/0.23 192.168.23.2    0           
24002  Pop         SR Adj (idx 1)     Gi0/0/0/0.23 192.168.23.2    0           
       17002       SR Adj (idx 1)     Gi0/0/0/0.13 192.168.13.1    0            (!)
24003  Pop         SR Adj (idx 3)     Gi0/0/0/0.23 192.168.23.2    0           
24004  Pop         SR Adj (idx 0)     Gi0/0/0/0.13 192.168.13.1    0           
       17001       SR Adj (idx 0)     Gi0/0/0/0.23 192.168.23.2    0            (!)
24005  Pop         SR Adj (idx 2)     Gi0/0/0/0.13 192.168.13.1    0           
24006  Pop         SR Adj (idx 1)     Gi0/0/0/0.13 192.168.13.1    0           
       17001       SR Adj (idx 1)     Gi0/0/0/0.23 192.168.23.2    0            (!)
24007  Pop         SR Adj (idx 3)     Gi0/0/0/0.13 192.168.13.1    0           
24008  Pop         100.64.0.1/32      Gi0/0/0/0.13 192.168.13.1    1577083     
       24008       100.64.0.1/32      Gi0/0/0/0.23 192.168.23.2    0            (!)
24009  Pop         192.168.12.0/24    Gi0/0/0/0.13 192.168.13.1    0           
       Pop         192.168.12.0/24    Gi0/0/0/0.23 192.168.23.2    0           
24010  Pop         100.64.0.2/32      Gi0/0/0/0.23 192.168.23.2    1577580     
       24008       100.64.0.2/32      Gi0/0/0/0.13 192.168.13.1    0            (!)
24011  Aggregate   UG-A: Per-VRF Aggr[V]   \
                                      UG-A                         4040        
24013  Aggregate   UG-B: Per-VRF Aggr[V]   \
                                      UG-B                         1312        
24014  24013       100.64.10.4/32[V]  Gi0/0/0/0.34 172.24.34.4     1560        
24015  24017       100.64.10.5/32[V]  Gi0/0/0/0.34 172.24.34.4     0           
24016  24018       100.64.10.19/32[V] Gi0/0/0/0.34 172.24.34.4     0           
24017  24019       172.24.19.0/24[V]  Gi0/0/0/0.34 172.24.34.4     0           
24018  24011       100.64.10.2:10:100.64.10.2/32   \
                                                   100.64.0.2      0           
24019  24011       100.64.10.2:10:172.24.28.0/24   \
                                                   100.64.0.2      0           
24020  24013       100.64.20.2:20:100.64.20.2/32   \
                                                   100.64.0.2      0           
24021  24013       100.64.20.2:20:172.24.48.0/24   \
                                                   100.64.0.2      0           
24022  24011       100.64.10.2/32[V]               100.64.0.2      520         
24023  24011       172.24.28.0/24[V]               100.64.0.2      0           
24024  24011       100.64.10.1:10:100.64.10.1/32   \
                                                   100.64.0.1      0           
24025  24011       100.64.10.1:10:172.24.18.0/24   \
                                                   100.64.0.1      0           
24026  24015       100.64.20.1:20:100.64.20.1/32   \
                                                   100.64.0.1      0           
24027  24015       100.64.20.1:20:172.24.38.0/24   \
                                                   100.64.0.1      0           
24028  24011       100.64.10.1/32[V]               100.64.0.1      1040        
24029  24011       172.24.18.0/24[V]               100.64.0.1      0           
24030  24016       100.64.10.2:10:100.64.10.28/32   \
                                                   100.64.0.2      0           
24031  24017       100.64.20.2:20:100.64.20.48/32   \
                                                   100.64.0.2      0           
24032  24016       100.64.10.28/32[V]              100.64.0.2      0           
24033  24016       100.64.10.1:10:100.64.10.18/32   \
                                                   100.64.0.1      0           
24034  24017       100.64.20.1:20:100.64.20.38/32   \
                                                   100.64.0.1      0           
24035  24016       100.64.10.18/32[V]              100.64.0.1      0           
24036  24030       100.64.10.6/32[V]  Gi0/0/0/0.34 172.24.34.4     0           
24037  24031       100.64.10.29/32[V] Gi0/0/0/0.34 172.24.34.4     0           
24038  24032       172.24.29.0/24[V]  Gi0/0/0/0.34 172.24.34.4     0           
24039  24013       100.64.10.4:10:100.64.10.4/32   \
                                      Gi0/0/0/0.34 172.24.34.4     0           
24040  24017       100.64.10.5:10:100.64.10.5/32   \
                                      Gi0/0/0/0.34 172.24.34.4     0           
24041  24018       100.64.10.5:10:100.64.10.19/32   \
                                      Gi0/0/0/0.34 172.24.34.4     0           
24042  24019       100.64.10.5:10:172.24.19.0/24   \
                                      Gi0/0/0/0.34 172.24.34.4     0           
24043  24030       100.64.10.6:10:100.64.10.6/32   \
                                      Gi0/0/0/0.34 172.24.34.4     0           
24044  24031       100.64.10.6:10:100.64.10.29/32   \
                                      Gi0/0/0/0.34 172.24.34.4     0           
24045  24032       100.64.10.6:10:172.24.29.0/24   \
                                      Gi0/0/0/0.34 172.24.34.4     0           
24046  24020       100.64.20.4:20:100.64.20.4/32   \
                                      Gi0/0/0/0.34 172.24.34.4     0           
24047  24021       100.64.20.5:20:100.64.20.5/32   \
                                      Gi0/0/0/0.34 172.24.34.4     0           
24048  24022       100.64.20.5:20:100.64.20.39/32   \
                                      Gi0/0/0/0.34 172.24.34.4     0           
24049  24023       100.64.20.5:20:172.24.39.0/24   \
                                      Gi0/0/0/0.34 172.24.34.4     0           
24050  24033       100.64.20.6:20:100.64.20.6/32   \
                                      Gi0/0/0/0.34 172.24.34.4     0           
24051  24034       100.64.20.6:20:100.64.20.49/32   \
                                      Gi0/0/0/0.34 172.24.34.4     0           
24052  24035       100.64.20.6:20:172.24.49.0/24   \
                                      Gi0/0/0/0.34 172.24.34.4     0           
24053  Pop         172.24.34.4/32     Gi0/0/0/0.34 172.24.34.4     21231       
RP/0/RP0/CPU0:cisco-kudo-13#
```


## XRv-01 (.4): 
```


RP/0/RP0/CPU0:cisco-kudo-01#

RP/0/RP0/CPU0:cisco-kudo-01#show route

Sun Dec 27 04:38:00.074 UTC

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

L    100.64.0.4/32 is directly connected, 2d03h, Loopback4
i L1 100.64.0.5/32 [115/10] via 192.168.45.5, 2d03h, GigabitEthernet0/0/0/0.45
                   [115/20] via 192.168.46.6, 2d03h, GigabitEthernet0/0/0/0.46 (!)
i L1 100.64.0.6/32 [115/20] via 192.168.45.5, 2d03h, GigabitEthernet0/0/0/0.45 (!)
                   [115/10] via 192.168.46.6, 2d03h, GigabitEthernet0/0/0/0.46
C    172.24.34.0/24 is directly connected, 2d03h, GigabitEthernet0/0/0/0.34
S    172.24.34.3/32 is directly connected, 00:52:51, GigabitEthernet0/0/0/0.34
L    172.24.34.4/32 is directly connected, 2d03h, GigabitEthernet0/0/0/0.34
C    192.168.45.0/24 is directly connected, 2d03h, GigabitEthernet0/0/0/0.45
L    192.168.45.4/32 is directly connected, 2d03h, GigabitEthernet0/0/0/0.45
C    192.168.46.0/24 is directly connected, 2d03h, GigabitEthernet0/0/0/0.46
L    192.168.46.4/32 is directly connected, 2d03h, GigabitEthernet0/0/0/0.46
i L1 192.168.56.0/24 [115/20] via 192.168.45.5, 2d03h, GigabitEthernet0/0/0/0.45
                     [115/20] via 192.168.46.6, 2d03h, GigabitEthernet0/0/0/0.46
RP/0/RP0/CPU0:cisco-kudo-01#

RP/0/RP0/CPU0:cisco-kudo-01#

RP/0/RP0/CPU0:cisco-kudo-01#show route vrf all

Sun Dec 27 04:38:02.117 UTC

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
L    10.10.0.30/32 is directly connected, 2d03h, MgmtEth0/RP0/CPU0/0

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

B    100.64.10.1/32 [20/0] via 172.24.34.3 (nexthop in vrf default), 02:50:56
B    100.64.10.2/32 [20/0] via 172.24.34.3 (nexthop in vrf default), 02:50:56
B    100.64.10.3/32 [20/0] via 172.24.34.3 (nexthop in vrf default), 02:50:56
L    100.64.10.4/32 is directly connected, 2d03h, Loopback10
B    100.64.10.5/32 [200/0] via 100.64.0.5 (nexthop in vrf default), 1d22h
B    100.64.10.6/32 [200/0] via 100.64.0.6 (nexthop in vrf default), 1d22h
B    100.64.10.18/32 [20/0] via 172.24.34.3 (nexthop in vrf default), 02:50:56
B    100.64.10.19/32 [200/0] via 100.64.0.5 (nexthop in vrf default), 01:09:01
B    100.64.10.28/32 [20/0] via 172.24.34.3 (nexthop in vrf default), 02:50:56
B    100.64.10.29/32 [200/0] via 100.64.0.6 (nexthop in vrf default), 01:09:01
B    172.24.18.0/24 [20/0] via 172.24.34.3 (nexthop in vrf default), 02:50:56
B    172.24.19.0/24 [200/0] via 100.64.0.5 (nexthop in vrf default), 1d22h
B    172.24.28.0/24 [20/0] via 172.24.34.3 (nexthop in vrf default), 02:50:56
B    172.24.29.0/24 [200/0] via 100.64.0.6 (nexthop in vrf default), 1d22h

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

B    100.64.20.1/32 [20/0] via 172.24.34.3 (nexthop in vrf default), 02:50:56
B    100.64.20.2/32 [20/0] via 172.24.34.3 (nexthop in vrf default), 02:50:56
B    100.64.20.3/32 [20/0] via 172.24.34.3 (nexthop in vrf default), 02:50:56
L    100.64.20.4/32 is directly connected, 2d03h, Loopback20
B    100.64.20.5/32 [200/0] via 100.64.0.5 (nexthop in vrf default), 1d22h
B    100.64.20.6/32 [200/0] via 100.64.0.6 (nexthop in vrf default), 1d22h
B    100.64.20.38/32 [20/0] via 172.24.34.3 (nexthop in vrf default), 02:50:56
B    100.64.20.39/32 [200/0] via 100.64.0.5 (nexthop in vrf default), 01:09:01
B    100.64.20.48/32 [20/0] via 172.24.34.3 (nexthop in vrf default), 02:50:56
B    100.64.20.49/32 [200/0] via 100.64.0.6 (nexthop in vrf default), 01:09:01
B    172.24.38.0/24 [20/0] via 172.24.34.3 (nexthop in vrf default), 02:50:56
B    172.24.39.0/24 [200/0] via 100.64.0.5 (nexthop in vrf default), 1d22h
B    172.24.48.0/24 [20/0] via 172.24.34.3 (nexthop in vrf default), 02:50:56
B    172.24.49.0/24 [200/0] via 100.64.0.6 (nexthop in vrf default), 1d22h
RP/0/RP0/CPU0:cisco-kudo-01#

RP/0/RP0/CPU0:cisco-kudo-01#

RP/0/RP0/CPU0:cisco-kudo-01#show mpls ldp bindings

Sun Dec 27 04:38:05.214 UTC

100.64.0.4/32, rev 7
	Local binding: label: ImpNull
	Remote bindings: (2 peers)
	    Peer                Label    
	    -----------------   ---------
	    100.64.0.5:0        24010   
	    100.64.0.6:0        24008   
100.64.0.5/32, rev 14
	Local binding: label: 24010
	Remote bindings: (2 peers)
	    Peer                Label    
	    -----------------   ---------
	    100.64.0.5:0        ImpNull 
	    100.64.0.6:0        24010   
100.64.0.6/32, rev 13
	Local binding: label: 24009
	Remote bindings: (2 peers)
	    Peer                Label    
	    -----------------   ---------
	    100.64.0.5:0        24008   
	    100.64.0.6:0        ImpNull 
172.24.34.0/24, rev 9
	Local binding: label: ImpNull
	No remote bindings
172.24.34.3/32, rev 16
	Local binding: label: 24053
	No remote bindings
192.168.45.0/24, rev 11
	Local binding: label: ImpNull
	Remote bindings: (2 peers)
	    Peer                Label    
	    -----------------   ---------
	    100.64.0.5:0        ImpNull 
	    100.64.0.6:0        24009   
192.168.46.0/24, rev 10
	Local binding: label: ImpNull
	Remote bindings: (2 peers)
	    Peer                Label    
	    -----------------   ---------
	    100.64.0.5:0        24009   
	    100.64.0.6:0        ImpNull 
192.168.56.0/24, rev 12
	Local binding: label: 24008
	Remote bindings: (2 peers)
	    Peer                Label    
	    -----------------   ---------
	    100.64.0.5:0        ImpNull 
	    100.64.0.6:0        ImpNull 

RP/0/RP0/CPU0:cisco-kudo-01#

RP/0/RP0/CPU0:cisco-kudo-01#

RP/0/RP0/CPU0:cisco-kudo-01#show cef vrf all

Sun Dec 27 04:38:07.306 UTC

VRF: MGMT
_____________

Prefix              Next Hop            Interface
------------------- ------------------- ------------------
0.0.0.0/0           drop                default handler 
0.0.0.0/32          broadcast
10.10.0.0/24        attached            MgmtEth0/RP0/CPU0/0
10.10.0.0/32        broadcast           MgmtEth0/RP0/CPU0/0
10.10.0.1/32        10.10.0.1/32        MgmtEth0/RP0/CPU0/0
10.10.0.30/32       receive             MgmtEth0/RP0/CPU0/0
10.10.0.38/32       10.10.0.38/32       MgmtEth0/RP0/CPU0/0
10.10.0.39/32       10.10.0.39/32       MgmtEth0/RP0/CPU0/0
10.10.0.41/32       10.10.0.41/32       MgmtEth0/RP0/CPU0/0
10.10.0.42/32       10.10.0.42/32       MgmtEth0/RP0/CPU0/0
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
100.64.10.1/32      172.24.34.3/32      <recursive>
100.64.10.2/32      172.24.34.3/32      <recursive>
100.64.10.3/32      172.24.34.3/32      <recursive>
100.64.10.4/32      receive             Loopback10
100.64.10.5/32      100.64.0.5/32       <recursive>
100.64.10.6/32      100.64.0.6/32       <recursive>
100.64.10.18/32     172.24.34.3/32      <recursive>
100.64.10.19/32     100.64.0.5/32       <recursive>
100.64.10.28/32     172.24.34.3/32      <recursive>
100.64.10.29/32     100.64.0.6/32       <recursive>
172.24.18.0/24      172.24.34.3/32      <recursive>
172.24.19.0/24      100.64.0.5/32       <recursive>
172.24.28.0/24      172.24.34.3/32      <recursive>
172.24.29.0/24      100.64.0.6/32       <recursive>
224.0.0.0/4         0.0.0.0/32          
224.0.0.0/24        receive
255.255.255.255/32  broadcast

VRF: UG-B
_____________

Prefix              Next Hop            Interface
------------------- ------------------- ------------------
0.0.0.0/0           drop                default handler 
0.0.0.0/32          broadcast
100.64.20.1/32      172.24.34.3/32      <recursive>
100.64.20.2/32      172.24.34.3/32      <recursive>
100.64.20.3/32      172.24.34.3/32      <recursive>
100.64.20.4/32      receive             Loopback20
100.64.20.5/32      100.64.0.5/32       <recursive>
100.64.20.6/32      100.64.0.6/32       <recursive>
100.64.20.38/32     172.24.34.3/32      <recursive>
100.64.20.39/32     100.64.0.5/32       <recursive>
100.64.20.48/32     172.24.34.3/32      <recursive>
100.64.20.49/32     100.64.0.6/32       <recursive>
172.24.38.0/24      172.24.34.3/32      <recursive>
172.24.39.0/24      100.64.0.5/32       <recursive>
172.24.48.0/24      172.24.34.3/32      <recursive>
172.24.49.0/24      100.64.0.6/32       <recursive>
224.0.0.0/4         0.0.0.0/32          
224.0.0.0/24        receive
255.255.255.255/32  broadcast

VRF: default
_____________

Prefix              Next Hop            Interface
------------------- ------------------- ------------------
0.0.0.0/0           drop                default handler 
0.0.0.0/32          broadcast
100.64.0.4/32       receive             Loopback4
100.64.0.5/32       192.168.45.5/32     GigabitEthernet0/0/0/0.45
                    192.168.46.6/32     GigabitEthernet0/0/0/0.46 (!)
100.64.0.6/32       192.168.45.5/32     GigabitEthernet0/0/0/0.45 (!)
                    192.168.46.6/32     GigabitEthernet0/0/0/0.46
172.24.34.0/24      attached            GigabitEthernet0/0/0/0.34
172.24.34.0/32      broadcast           GigabitEthernet0/0/0/0.34
172.24.34.3/32      attached            GigabitEthernet0/0/0/0.34
172.24.34.4/32      receive             GigabitEthernet0/0/0/0.34
172.24.34.255/32    broadcast           GigabitEthernet0/0/0/0.34
192.168.45.0/24     attached            GigabitEthernet0/0/0/0.45
192.168.45.0/32     broadcast           GigabitEthernet0/0/0/0.45
192.168.45.4/32     receive             GigabitEthernet0/0/0/0.45
192.168.45.255/32   broadcast           GigabitEthernet0/0/0/0.45
192.168.46.0/24     attached            GigabitEthernet0/0/0/0.46
192.168.46.0/32     broadcast           GigabitEthernet0/0/0/0.46
192.168.46.4/32     receive             GigabitEthernet0/0/0/0.46
192.168.46.255/32   broadcast           GigabitEthernet0/0/0/0.46
192.168.56.0/24     192.168.45.5/32     GigabitEthernet0/0/0/0.45
                    192.168.46.6/32     GigabitEthernet0/0/0/0.46
224.0.0.0/4         0.0.0.0/32          
224.0.0.0/24        receive
255.255.255.255/32  broadcast
RP/0/RP0/CPU0:cisco-kudo-01#

RP/0/RP0/CPU0:cisco-kudo-01#

RP/0/RP0/CPU0:cisco-kudo-01#show mpls forwarding

Sun Dec 27 04:38:10.413 UTC
Local  Outgoing    Prefix             Outgoing     Next Hop        Bytes       
Label  Label       or ID              Interface                    Switched    
------ ----------- ------------------ ------------ --------------- ------------
15045  Pop         SRLB (idx 45)      Gi0/0/0/0.45 192.168.45.5    0           
15046  Pop         SRLB (idx 46)      Gi0/0/0/0.46 192.168.46.6    0           
17005  Pop         SR Pfx (idx 1005)  Gi0/0/0/0.45 192.168.45.5    16114       
       17005       SR Pfx (idx 1005)  Gi0/0/0/0.46 192.168.46.6    0            (!)
17006  Pop         SR Pfx (idx 1006)  Gi0/0/0/0.46 192.168.46.6    16271       
       17006       SR Pfx (idx 1006)  Gi0/0/0/0.45 192.168.45.5    0            (!)
24000  Pop         SR Adj (idx 0)     Gi0/0/0/0.45 192.168.45.5    0           
       17005       SR Adj (idx 0)     Gi0/0/0/0.46 192.168.46.6    0            (!)
24001  Pop         SR Adj (idx 2)     Gi0/0/0/0.45 192.168.45.5    0           
24002  Pop         SR Adj (idx 1)     Gi0/0/0/0.45 192.168.45.5    0           
       17005       SR Adj (idx 1)     Gi0/0/0/0.46 192.168.46.6    0            (!)
24003  Pop         SR Adj (idx 3)     Gi0/0/0/0.45 192.168.45.5    0           
24004  Pop         SR Adj (idx 0)     Gi0/0/0/0.46 192.168.46.6    0           
       17006       SR Adj (idx 0)     Gi0/0/0/0.45 192.168.45.5    0            (!)
24005  Pop         SR Adj (idx 2)     Gi0/0/0/0.46 192.168.46.6    0           
24006  Pop         SR Adj (idx 1)     Gi0/0/0/0.46 192.168.46.6    0           
       17006       SR Adj (idx 1)     Gi0/0/0/0.45 192.168.45.5    0            (!)
24007  Pop         SR Adj (idx 3)     Gi0/0/0/0.46 192.168.46.6    0           
24008  Pop         192.168.56.0/24    Gi0/0/0/0.45 192.168.45.5    0           
       Pop         192.168.56.0/24    Gi0/0/0/0.46 192.168.46.6    0           
24009  Pop         100.64.0.6/32      Gi0/0/0/0.46 192.168.46.6    1578425     
       24008       100.64.0.6/32      Gi0/0/0/0.45 192.168.45.5    0            (!)
24010  Pop         100.64.0.5/32      Gi0/0/0/0.45 192.168.45.5    1576949     
       24010       100.64.0.5/32      Gi0/0/0/0.46 192.168.46.6    0            (!)
24012  24011       100.64.10.3/32[V]  Gi0/0/0/0.34 172.24.34.3     1560        
24013  Aggregate   UG-A: Per-VRF Aggr[V]   \
                                      UG-A                         3540        
24014  24011       100.64.10.5/32[V]               100.64.0.5      520         
24015  24012       100.64.10.19/32[V]              100.64.0.5      0           
24016  24011       172.24.19.0/24[V]               100.64.0.5      0           
24017  24011       100.64.10.5:10:100.64.10.5/32   \
                                                   100.64.0.5      0           
24018  24012       100.64.10.5:10:100.64.10.19/32   \
                                                   100.64.0.5      0           
24019  24011       100.64.10.5:10:172.24.19.0/24   \
                                                   100.64.0.5      0           
24020  Aggregate   UG-B: Per-VRF Aggr[V]   \
                                      UG-B                         500         
24021  24013       100.64.20.5:20:100.64.20.5/32   \
                                                   100.64.0.5      0           
24022  24014       100.64.20.5:20:100.64.20.39/32   \
                                                   100.64.0.5      0           
24023  24013       100.64.20.5:20:172.24.39.0/24   \
                                                   100.64.0.5      0           
24024  24024       100.64.10.1/32[V]  Gi0/0/0/0.34 172.24.34.3     0           
24025  24018       100.64.10.2/32[V]  Gi0/0/0/0.34 172.24.34.3     0           
24026  24033       100.64.10.18/32[V] Gi0/0/0/0.34 172.24.34.3     0           
24027  24030       100.64.10.28/32[V] Gi0/0/0/0.34 172.24.34.3     0           
24028  24025       172.24.18.0/24[V]  Gi0/0/0/0.34 172.24.34.3     0           
24029  24019       172.24.28.0/24[V]  Gi0/0/0/0.34 172.24.34.3     0           
24030  24013       100.64.10.6:10:100.64.10.6/32   \
                                                   100.64.0.6      0           
24031  24015       100.64.10.6:10:100.64.10.29/32   \
                                                   100.64.0.6      0           
24032  24013       100.64.10.6:10:172.24.29.0/24   \
                                                   100.64.0.6      0           
24033  24017       100.64.20.6:20:100.64.20.6/32   \
                                                   100.64.0.6      0           
24034  24018       100.64.20.6:20:100.64.20.49/32   \
                                                   100.64.0.6      0           
24035  24017       100.64.20.6:20:172.24.49.0/24   \
                                                   100.64.0.6      0           
24036  24013       100.64.10.6/32[V]               100.64.0.6      520         
24037  24015       100.64.10.29/32[V]              100.64.0.6      0           
24038  24013       172.24.29.0/24[V]               100.64.0.6      0           
24039  24024       100.64.10.1:10:100.64.10.1/32   \
                                      Gi0/0/0/0.34 172.24.34.3     0           
24040  24033       100.64.10.1:10:100.64.10.18/32   \
                                      Gi0/0/0/0.34 172.24.34.3     0           
24041  24025       100.64.10.1:10:172.24.18.0/24   \
                                      Gi0/0/0/0.34 172.24.34.3     0           
24042  24018       100.64.10.2:10:100.64.10.2/32   \
                                      Gi0/0/0/0.34 172.24.34.3     0           
24043  24030       100.64.10.2:10:100.64.10.28/32   \
                                      Gi0/0/0/0.34 172.24.34.3     0           
24044  24019       100.64.10.2:10:172.24.28.0/24   \
                                      Gi0/0/0/0.34 172.24.34.3     0           
24045  24011       100.64.10.3:10:100.64.10.3/32   \
                                      Gi0/0/0/0.34 172.24.34.3     0           
24046  24026       100.64.20.1:20:100.64.20.1/32   \
                                      Gi0/0/0/0.34 172.24.34.3     0           
24047  24034       100.64.20.1:20:100.64.20.38/32   \
                                      Gi0/0/0/0.34 172.24.34.3     0           
24048  24027       100.64.20.1:20:172.24.38.0/24   \
                                      Gi0/0/0/0.34 172.24.34.3     0           
24049  24020       100.64.20.2:20:100.64.20.2/32   \
                                      Gi0/0/0/0.34 172.24.34.3     0           
24050  24031       100.64.20.2:20:100.64.20.48/32   \
                                      Gi0/0/0/0.34 172.24.34.3     0           
24051  24021       100.64.20.2:20:172.24.48.0/24   \
                                      Gi0/0/0/0.34 172.24.34.3     0           
24052  24013       100.64.20.3:20:100.64.20.3/32   \
                                      Gi0/0/0/0.34 172.24.34.3     0           
24053  Pop         172.24.34.3/32     Gi0/0/0/0.34 172.24.34.3     21153       
RP/0/RP0/CPU0:cisco-kudo-01#
```


## XRv-02 (.5): 
```


RP/0/RP0/CPU0:cisco-kudo-02#

RP/0/RP0/CPU0:cisco-kudo-02#show route

Sun Dec 27 04:37:59.516 UTC

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

i L1 100.64.0.4/32 [115/10] via 192.168.45.4, 2d03h, GigabitEthernet0/0/0/0.45
                   [115/20] via 192.168.56.6, 2d03h, GigabitEthernet0/0/0/0.56 (!)
L    100.64.0.5/32 is directly connected, 2d03h, Loopback5
i L1 100.64.0.6/32 [115/20] via 192.168.45.4, 2d03h, GigabitEthernet0/0/0/0.45 (!)
                   [115/10] via 192.168.56.6, 2d03h, GigabitEthernet0/0/0/0.56
C    192.168.45.0/24 is directly connected, 2d03h, GigabitEthernet0/0/0/0.45
L    192.168.45.5/32 is directly connected, 2d03h, GigabitEthernet0/0/0/0.45
i L1 192.168.46.0/24 [115/20] via 192.168.45.4, 2d03h, GigabitEthernet0/0/0/0.45
                     [115/20] via 192.168.56.6, 2d03h, GigabitEthernet0/0/0/0.56
C    192.168.56.0/24 is directly connected, 2d03h, GigabitEthernet0/0/0/0.56
L    192.168.56.5/32 is directly connected, 2d03h, GigabitEthernet0/0/0/0.56
RP/0/RP0/CPU0:cisco-kudo-02#

RP/0/RP0/CPU0:cisco-kudo-02#

RP/0/RP0/CPU0:cisco-kudo-02#show route vrf all

Sun Dec 27 04:38:01.619 UTC

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
L    10.10.0.31/32 is directly connected, 2d03h, MgmtEth0/RP0/CPU0/0

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

B    100.64.10.1/32 [200/0] via 100.64.0.4 (nexthop in vrf default), 02:50:56
B    100.64.10.2/32 [200/0] via 100.64.0.4 (nexthop in vrf default), 02:50:56
B    100.64.10.3/32 [200/0] via 100.64.0.4 (nexthop in vrf default), 02:50:56
B    100.64.10.4/32 [200/0] via 100.64.0.4 (nexthop in vrf default), 1d22h
L    100.64.10.5/32 is directly connected, 2d03h, Loopback10
B    100.64.10.6/32 [200/0] via 100.64.0.6 (nexthop in vrf default), 2d03h
B    100.64.10.18/32 [200/0] via 100.64.0.4 (nexthop in vrf default), 02:50:56
B    100.64.10.19/32 [20/0] via 172.24.19.9, 01:09:01
B    100.64.10.28/32 [200/0] via 100.64.0.4 (nexthop in vrf default), 02:50:56
B    100.64.10.29/32 [200/0] via 100.64.0.6 (nexthop in vrf default), 01:09:01
B    172.24.18.0/24 [200/0] via 100.64.0.4 (nexthop in vrf default), 02:50:56
C    172.24.19.0/24 is directly connected, 2d03h, GigabitEthernet0/0/0/0.19
L    172.24.19.5/32 is directly connected, 2d03h, GigabitEthernet0/0/0/0.19
B    172.24.28.0/24 [200/0] via 100.64.0.4 (nexthop in vrf default), 02:50:56
B    172.24.29.0/24 [200/0] via 100.64.0.6 (nexthop in vrf default), 2d03h

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

B    100.64.20.1/32 [200/0] via 100.64.0.4 (nexthop in vrf default), 02:50:56
B    100.64.20.2/32 [200/0] via 100.64.0.4 (nexthop in vrf default), 02:50:56
B    100.64.20.3/32 [200/0] via 100.64.0.4 (nexthop in vrf default), 02:50:56
B    100.64.20.4/32 [200/0] via 100.64.0.4 (nexthop in vrf default), 1d22h
L    100.64.20.5/32 is directly connected, 2d03h, Loopback20
B    100.64.20.6/32 [200/0] via 100.64.0.6 (nexthop in vrf default), 2d03h
B    100.64.20.38/32 [200/0] via 100.64.0.4 (nexthop in vrf default), 02:50:56
B    100.64.20.39/32 [20/0] via 172.24.39.9, 01:09:01
B    100.64.20.48/32 [200/0] via 100.64.0.4 (nexthop in vrf default), 02:50:56
B    100.64.20.49/32 [200/0] via 100.64.0.6 (nexthop in vrf default), 01:09:01
B    172.24.38.0/24 [200/0] via 100.64.0.4 (nexthop in vrf default), 02:50:56
C    172.24.39.0/24 is directly connected, 2d03h, GigabitEthernet0/0/0/0.39
L    172.24.39.5/32 is directly connected, 2d03h, GigabitEthernet0/0/0/0.39
B    172.24.48.0/24 [200/0] via 100.64.0.4 (nexthop in vrf default), 02:50:56
B    172.24.49.0/24 [200/0] via 100.64.0.6 (nexthop in vrf default), 2d03h
RP/0/RP0/CPU0:cisco-kudo-02#

RP/0/RP0/CPU0:cisco-kudo-02#

RP/0/RP0/CPU0:cisco-kudo-02#show mpls ldp bindings

Sun Dec 27 04:38:04.658 UTC

100.64.0.4/32, rev 12
	Local binding: label: 24010
	Remote bindings: (2 peers)
	    Peer                Label    
	    -----------------   ---------
	    100.64.0.4:0        ImpNull 
	    100.64.0.6:0        24008   
100.64.0.5/32, rev 2
	Local binding: label: ImpNull
	Remote bindings: (2 peers)
	    Peer                Label    
	    -----------------   ---------
	    100.64.0.4:0        24010   
	    100.64.0.6:0        24010   
100.64.0.6/32, rev 10
	Local binding: label: 24008
	Remote bindings: (2 peers)
	    Peer                Label    
	    -----------------   ---------
	    100.64.0.4:0        24009   
	    100.64.0.6:0        ImpNull 
172.24.34.0/24, rev 0
	No local binding 
	Remote bindings: (1 peers)
	    Peer                Label    
	    -----------------   ---------
	    100.64.0.4:0        ImpNull 
172.24.34.3/32, rev 0
	No local binding 
	Remote bindings: (1 peers)
	    Peer                Label    
	    -----------------   ---------
	    100.64.0.4:0        24053   
192.168.45.0/24, rev 6
	Local binding: label: ImpNull
	Remote bindings: (2 peers)
	    Peer                Label    
	    -----------------   ---------
	    100.64.0.4:0        ImpNull 
	    100.64.0.6:0        24009   
192.168.46.0/24, rev 11
	Local binding: label: 24009
	Remote bindings: (2 peers)
	    Peer                Label    
	    -----------------   ---------
	    100.64.0.4:0        ImpNull 
	    100.64.0.6:0        ImpNull 
192.168.56.0/24, rev 4
	Local binding: label: ImpNull
	Remote bindings: (2 peers)
	    Peer                Label    
	    -----------------   ---------
	    100.64.0.4:0        24008   
	    100.64.0.6:0        ImpNull 

RP/0/RP0/CPU0:cisco-kudo-02#

RP/0/RP0/CPU0:cisco-kudo-02#

RP/0/RP0/CPU0:cisco-kudo-02#show cef vrf all

Sun Dec 27 04:38:06.761 UTC

VRF: MGMT
_____________

Prefix              Next Hop            Interface
------------------- ------------------- ------------------
0.0.0.0/0           drop                default handler 
0.0.0.0/32          broadcast
10.10.0.0/24        attached            MgmtEth0/RP0/CPU0/0
10.10.0.0/32        broadcast           MgmtEth0/RP0/CPU0/0
10.10.0.1/32        10.10.0.1/32        MgmtEth0/RP0/CPU0/0
10.10.0.30/32       10.10.0.30/32       MgmtEth0/RP0/CPU0/0
10.10.0.31/32       receive             MgmtEth0/RP0/CPU0/0
10.10.0.38/32       10.10.0.38/32       MgmtEth0/RP0/CPU0/0
10.10.0.39/32       10.10.0.39/32       MgmtEth0/RP0/CPU0/0
10.10.0.41/32       10.10.0.41/32       MgmtEth0/RP0/CPU0/0
10.10.0.42/32       10.10.0.42/32       MgmtEth0/RP0/CPU0/0
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
100.64.10.1/32      100.64.0.4/32       <recursive>
100.64.10.2/32      100.64.0.4/32       <recursive>
100.64.10.3/32      100.64.0.4/32       <recursive>
100.64.10.4/32      100.64.0.4/32       <recursive>
100.64.10.5/32      receive             Loopback10
100.64.10.6/32      100.64.0.6/32       <recursive>
100.64.10.18/32     100.64.0.4/32       <recursive>
100.64.10.19/32     172.24.19.9/32      <recursive>
100.64.10.28/32     100.64.0.4/32       <recursive>
100.64.10.29/32     100.64.0.6/32       <recursive>
172.24.18.0/24      100.64.0.4/32       <recursive>
172.24.19.0/24      attached            GigabitEthernet0/0/0/0.19
172.24.19.0/32      broadcast           GigabitEthernet0/0/0/0.19
172.24.19.5/32      receive             GigabitEthernet0/0/0/0.19
172.24.19.9/32      172.24.19.9/32      GigabitEthernet0/0/0/0.19
172.24.19.255/32    broadcast           GigabitEthernet0/0/0/0.19
172.24.28.0/24      100.64.0.4/32       <recursive>
172.24.29.0/24      100.64.0.6/32       <recursive>
224.0.0.0/4         0.0.0.0/32          
224.0.0.0/24        receive
255.255.255.255/32  broadcast

VRF: UG-B
_____________

Prefix              Next Hop            Interface
------------------- ------------------- ------------------
0.0.0.0/0           drop                default handler 
0.0.0.0/32          broadcast
100.64.20.1/32      100.64.0.4/32       <recursive>
100.64.20.2/32      100.64.0.4/32       <recursive>
100.64.20.3/32      100.64.0.4/32       <recursive>
100.64.20.4/32      100.64.0.4/32       <recursive>
100.64.20.5/32      receive             Loopback20
100.64.20.6/32      100.64.0.6/32       <recursive>
100.64.20.38/32     100.64.0.4/32       <recursive>
100.64.20.39/32     172.24.39.9/32      <recursive>
100.64.20.48/32     100.64.0.4/32       <recursive>
100.64.20.49/32     100.64.0.6/32       <recursive>
172.24.38.0/24      100.64.0.4/32       <recursive>
172.24.39.0/24      attached            GigabitEthernet0/0/0/0.39
172.24.39.0/32      broadcast           GigabitEthernet0/0/0/0.39
172.24.39.5/32      receive             GigabitEthernet0/0/0/0.39
172.24.39.9/32      172.24.39.9/32      GigabitEthernet0/0/0/0.39
172.24.39.255/32    broadcast           GigabitEthernet0/0/0/0.39
172.24.48.0/24      100.64.0.4/32       <recursive>
172.24.49.0/24      100.64.0.6/32       <recursive>
224.0.0.0/4         0.0.0.0/32          
224.0.0.0/24        receive
255.255.255.255/32  broadcast

VRF: default
_____________

Prefix              Next Hop            Interface
------------------- ------------------- ------------------
0.0.0.0/0           drop                default handler 
0.0.0.0/32          broadcast
100.64.0.4/32       192.168.45.4/32     GigabitEthernet0/0/0/0.45
                    192.168.56.6/32     GigabitEthernet0/0/0/0.56 (!)
100.64.0.5/32       receive             Loopback5
100.64.0.6/32       192.168.45.4/32     GigabitEthernet0/0/0/0.45 (!)
                    192.168.56.6/32     GigabitEthernet0/0/0/0.56
192.168.45.0/24     attached            GigabitEthernet0/0/0/0.45
192.168.45.0/32     broadcast           GigabitEthernet0/0/0/0.45
192.168.45.5/32     receive             GigabitEthernet0/0/0/0.45
192.168.45.255/32   broadcast           GigabitEthernet0/0/0/0.45
192.168.46.0/24     192.168.45.4/32     GigabitEthernet0/0/0/0.45
                    192.168.56.6/32     GigabitEthernet0/0/0/0.56
192.168.56.0/24     attached            GigabitEthernet0/0/0/0.56
192.168.56.0/32     broadcast           GigabitEthernet0/0/0/0.56
192.168.56.5/32     receive             GigabitEthernet0/0/0/0.56
192.168.56.255/32   broadcast           GigabitEthernet0/0/0/0.56
224.0.0.0/4         0.0.0.0/32          
224.0.0.0/24        receive
255.255.255.255/32  broadcast
RP/0/RP0/CPU0:cisco-kudo-02#

RP/0/RP0/CPU0:cisco-kudo-02#

RP/0/RP0/CPU0:cisco-kudo-02#show mpls forwarding

Sun Dec 27 04:38:09.813 UTC
Local  Outgoing    Prefix             Outgoing     Next Hop        Bytes       
Label  Label       or ID              Interface                    Switched    
------ ----------- ------------------ ------------ --------------- ------------
15045  Pop         SRLB (idx 45)      Gi0/0/0/0.45 192.168.45.4    0           
15056  Pop         SRLB (idx 56)      Gi0/0/0/0.56 192.168.56.6    0           
17004  Pop         SR Pfx (idx 1004)  Gi0/0/0/0.45 192.168.45.4    15522       
       17004       SR Pfx (idx 1004)  Gi0/0/0/0.56 192.168.56.6    0            (!)
17006  Pop         SR Pfx (idx 1006)  Gi0/0/0/0.56 192.168.56.6    15679       
       17006       SR Pfx (idx 1006)  Gi0/0/0/0.45 192.168.45.4    0            (!)
24000  Pop         SR Adj (idx 0)     Gi0/0/0/0.45 192.168.45.4    0           
       17004       SR Adj (idx 0)     Gi0/0/0/0.56 192.168.56.6    0            (!)
24001  Pop         SR Adj (idx 2)     Gi0/0/0/0.45 192.168.45.4    0           
24002  Pop         SR Adj (idx 1)     Gi0/0/0/0.45 192.168.45.4    0           
       17004       SR Adj (idx 1)     Gi0/0/0/0.56 192.168.56.6    0            (!)
24003  Pop         SR Adj (idx 3)     Gi0/0/0/0.45 192.168.45.4    0           
24004  Pop         SR Adj (idx 0)     Gi0/0/0/0.56 192.168.56.6    0           
       17006       SR Adj (idx 0)     Gi0/0/0/0.45 192.168.45.4    0            (!)
24005  Pop         SR Adj (idx 2)     Gi0/0/0/0.56 192.168.56.6    0           
24006  Pop         SR Adj (idx 1)     Gi0/0/0/0.56 192.168.56.6    0           
       17006       SR Adj (idx 1)     Gi0/0/0/0.45 192.168.45.4    0            (!)
24007  Pop         SR Adj (idx 3)     Gi0/0/0/0.56 192.168.56.6    0           
24008  Pop         100.64.0.6/32      Gi0/0/0/0.56 192.168.56.6    1561029     
       24009       100.64.0.6/32      Gi0/0/0/0.45 192.168.45.4    0            (!)
24009  Pop         192.168.46.0/24    Gi0/0/0/0.45 192.168.45.4    0           
       Pop         192.168.46.0/24    Gi0/0/0/0.56 192.168.56.6    0           
24010  Pop         100.64.0.4/32      Gi0/0/0/0.45 192.168.45.4    1571411     
       24008       100.64.0.4/32      Gi0/0/0/0.56 192.168.56.6    0            (!)
24011  Aggregate   UG-A: Per-VRF Aggr[V]   \
                                      UG-A                         1020        
24012  Unlabelled  100.64.10.19/32[V] Gi0/0/0/0.19 172.24.19.9     0           
24013  Aggregate   UG-B: Per-VRF Aggr[V]   \
                                      UG-B                         0           
24014  Unlabelled  100.64.20.39/32[V] Gi0/0/0/0.39 172.24.39.9     0           
24015  24013       100.64.10.4/32[V]               100.64.0.4      520         
24016  24013       100.64.10.6/32[V]               100.64.0.6      0           
24017  24015       100.64.10.29/32[V]              100.64.0.6      0           
24018  24013       172.24.29.0/24[V]               100.64.0.6      0           
24019  24039       100.64.10.1/32[V]               100.64.0.4      0           
24020  24042       100.64.10.2/32[V]               100.64.0.4      0           
24021  24045       100.64.10.3/32[V]               100.64.0.4      0           
24022  24040       100.64.10.18/32[V]              100.64.0.4      0           
24023  24043       100.64.10.28/32[V]              100.64.0.4      0           
24024  24041       172.24.18.0/24[V]               100.64.0.4      0           
24025  24044       172.24.28.0/24[V]               100.64.0.4      0           
RP/0/RP0/CPU0:cisco-kudo-02#
```


## XRv-08 (.6): 
```


RP/0/RP0/CPU0:cisco-kudo-08#

RP/0/RP0/CPU0:cisco-kudo-08#show route

Sun Dec 27 04:38:01.335 UTC

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

i L1 100.64.0.4/32 [115/10] via 192.168.46.4, 2d03h, GigabitEthernet0/0/0/0.46
                   [115/20] via 192.168.56.5, 2d03h, GigabitEthernet0/0/0/0.56 (!)
i L1 100.64.0.5/32 [115/20] via 192.168.46.4, 2d03h, GigabitEthernet0/0/0/0.46 (!)
                   [115/10] via 192.168.56.5, 2d03h, GigabitEthernet0/0/0/0.56
L    100.64.0.6/32 is directly connected, 2d03h, Loopback6
i L1 192.168.45.0/24 [115/20] via 192.168.46.4, 2d03h, GigabitEthernet0/0/0/0.46
                     [115/20] via 192.168.56.5, 2d03h, GigabitEthernet0/0/0/0.56
C    192.168.46.0/24 is directly connected, 2d03h, GigabitEthernet0/0/0/0.46
L    192.168.46.6/32 is directly connected, 2d03h, GigabitEthernet0/0/0/0.46
C    192.168.56.0/24 is directly connected, 2d03h, GigabitEthernet0/0/0/0.56
L    192.168.56.6/32 is directly connected, 2d03h, GigabitEthernet0/0/0/0.56
RP/0/RP0/CPU0:cisco-kudo-08#

RP/0/RP0/CPU0:cisco-kudo-08#

RP/0/RP0/CPU0:cisco-kudo-08#show route vrf all

Sun Dec 27 04:38:03.408 UTC

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
L    10.10.0.38/32 is directly connected, 2d03h, MgmtEth0/RP0/CPU0/0

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

B    100.64.10.1/32 [200/0] via 100.64.0.4 (nexthop in vrf default), 02:50:57
B    100.64.10.2/32 [200/0] via 100.64.0.4 (nexthop in vrf default), 02:50:57
B    100.64.10.3/32 [200/0] via 100.64.0.4 (nexthop in vrf default), 02:50:57
B    100.64.10.4/32 [200/0] via 100.64.0.4 (nexthop in vrf default), 1d22h
B    100.64.10.5/32 [200/0] via 100.64.0.5 (nexthop in vrf default), 2d03h
L    100.64.10.6/32 is directly connected, 2d03h, Loopback10
B    100.64.10.18/32 [200/0] via 100.64.0.4 (nexthop in vrf default), 02:50:57
B    100.64.10.19/32 [200/0] via 100.64.0.5 (nexthop in vrf default), 01:09:02
B    100.64.10.28/32 [200/0] via 100.64.0.4 (nexthop in vrf default), 02:50:57
B    100.64.10.29/32 [20/0] via 172.24.29.9, 01:09:02
B    172.24.18.0/24 [200/0] via 100.64.0.4 (nexthop in vrf default), 02:50:57
B    172.24.19.0/24 [200/0] via 100.64.0.5 (nexthop in vrf default), 2d03h
B    172.24.28.0/24 [200/0] via 100.64.0.4 (nexthop in vrf default), 02:50:57
C    172.24.29.0/24 is directly connected, 2d03h, GigabitEthernet0/0/0/0.29
L    172.24.29.6/32 is directly connected, 2d03h, GigabitEthernet0/0/0/0.29

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

B    100.64.20.1/32 [200/0] via 100.64.0.4 (nexthop in vrf default), 02:50:57
B    100.64.20.2/32 [200/0] via 100.64.0.4 (nexthop in vrf default), 02:50:57
B    100.64.20.3/32 [200/0] via 100.64.0.4 (nexthop in vrf default), 02:50:57
B    100.64.20.4/32 [200/0] via 100.64.0.4 (nexthop in vrf default), 1d22h
B    100.64.20.5/32 [200/0] via 100.64.0.5 (nexthop in vrf default), 2d03h
L    100.64.20.6/32 is directly connected, 2d03h, Loopback20
B    100.64.20.38/32 [200/0] via 100.64.0.4 (nexthop in vrf default), 02:50:57
B    100.64.20.39/32 [200/0] via 100.64.0.5 (nexthop in vrf default), 01:09:02
B    100.64.20.48/32 [200/0] via 100.64.0.4 (nexthop in vrf default), 02:50:57
B    100.64.20.49/32 [20/0] via 172.24.49.9, 01:09:02
B    172.24.38.0/24 [200/0] via 100.64.0.4 (nexthop in vrf default), 02:50:57
B    172.24.39.0/24 [200/0] via 100.64.0.5 (nexthop in vrf default), 2d03h
B    172.24.48.0/24 [200/0] via 100.64.0.4 (nexthop in vrf default), 02:50:57
C    172.24.49.0/24 is directly connected, 2d03h, GigabitEthernet0/0/0/0.49
L    172.24.49.6/32 is directly connected, 2d03h, GigabitEthernet0/0/0/0.49
RP/0/RP0/CPU0:cisco-kudo-08#

RP/0/RP0/CPU0:cisco-kudo-08#

RP/0/RP0/CPU0:cisco-kudo-08#show mpls ldp bindings

Sun Dec 27 04:38:06.515 UTC

100.64.0.4/32, rev 11
	Local binding: label: 24008
	Remote bindings: (2 peers)
	    Peer                Label    
	    -----------------   ---------
	    100.64.0.4:0        ImpNull 
	    100.64.0.5:0        24010   
100.64.0.5/32, rev 13
	Local binding: label: 24010
	Remote bindings: (2 peers)
	    Peer                Label    
	    -----------------   ---------
	    100.64.0.4:0        24010   
	    100.64.0.5:0        ImpNull 
100.64.0.6/32, rev 8
	Local binding: label: ImpNull
	Remote bindings: (2 peers)
	    Peer                Label    
	    -----------------   ---------
	    100.64.0.4:0        24009   
	    100.64.0.5:0        24008   
172.24.34.0/24, rev 0
	No local binding 
	Remote bindings: (1 peers)
	    Peer                Label    
	    -----------------   ---------
	    100.64.0.4:0        ImpNull 
172.24.34.3/32, rev 0
	No local binding 
	Remote bindings: (1 peers)
	    Peer                Label    
	    -----------------   ---------
	    100.64.0.4:0        24053   
192.168.45.0/24, rev 12
	Local binding: label: 24009
	Remote bindings: (2 peers)
	    Peer                Label    
	    -----------------   ---------
	    100.64.0.4:0        ImpNull 
	    100.64.0.5:0        ImpNull 
192.168.46.0/24, rev 10
	Local binding: label: ImpNull
	Remote bindings: (2 peers)
	    Peer                Label    
	    -----------------   ---------
	    100.64.0.4:0        ImpNull 
	    100.64.0.5:0        24009   
192.168.56.0/24, rev 9
	Local binding: label: ImpNull
	Remote bindings: (2 peers)
	    Peer                Label    
	    -----------------   ---------
	    100.64.0.4:0        24008   
	    100.64.0.5:0        ImpNull 

RP/0/RP0/CPU0:cisco-kudo-08#

RP/0/RP0/CPU0:cisco-kudo-08#

RP/0/RP0/CPU0:cisco-kudo-08#show cef vrf all

Sun Dec 27 04:38:08.499 UTC

VRF: MGMT
_____________

Prefix              Next Hop            Interface
------------------- ------------------- ------------------
0.0.0.0/0           drop                default handler 
0.0.0.0/32          broadcast
10.10.0.0/24        attached            MgmtEth0/RP0/CPU0/0
10.10.0.0/32        broadcast           MgmtEth0/RP0/CPU0/0
10.10.0.1/32        10.10.0.1/32        MgmtEth0/RP0/CPU0/0
10.10.0.38/32       receive             MgmtEth0/RP0/CPU0/0
10.10.0.39/32       10.10.0.39/32       MgmtEth0/RP0/CPU0/0
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
100.64.10.1/32      100.64.0.4/32       <recursive>
100.64.10.2/32      100.64.0.4/32       <recursive>
100.64.10.3/32      100.64.0.4/32       <recursive>
100.64.10.4/32      100.64.0.4/32       <recursive>
100.64.10.5/32      100.64.0.5/32       <recursive>
100.64.10.6/32      receive             Loopback10
100.64.10.18/32     100.64.0.4/32       <recursive>
100.64.10.19/32     100.64.0.5/32       <recursive>
100.64.10.28/32     100.64.0.4/32       <recursive>
100.64.10.29/32     172.24.29.9/32      <recursive>
172.24.18.0/24      100.64.0.4/32       <recursive>
172.24.19.0/24      100.64.0.5/32       <recursive>
172.24.28.0/24      100.64.0.4/32       <recursive>
172.24.29.0/24      attached            GigabitEthernet0/0/0/0.29
172.24.29.0/32      broadcast           GigabitEthernet0/0/0/0.29
172.24.29.6/32      receive             GigabitEthernet0/0/0/0.29
172.24.29.9/32      172.24.29.9/32      GigabitEthernet0/0/0/0.29
172.24.29.255/32    broadcast           GigabitEthernet0/0/0/0.29
224.0.0.0/4         0.0.0.0/32          
224.0.0.0/24        receive
255.255.255.255/32  broadcast

VRF: UG-B
_____________

Prefix              Next Hop            Interface
------------------- ------------------- ------------------
0.0.0.0/0           drop                default handler 
0.0.0.0/32          broadcast
100.64.20.1/32      100.64.0.4/32       <recursive>
100.64.20.2/32      100.64.0.4/32       <recursive>
100.64.20.3/32      100.64.0.4/32       <recursive>
100.64.20.4/32      100.64.0.4/32       <recursive>
100.64.20.5/32      100.64.0.5/32       <recursive>
100.64.20.6/32      receive             Loopback20
100.64.20.38/32     100.64.0.4/32       <recursive>
100.64.20.39/32     100.64.0.5/32       <recursive>
100.64.20.48/32     100.64.0.4/32       <recursive>
100.64.20.49/32     172.24.49.9/32      <recursive>
172.24.38.0/24      100.64.0.4/32       <recursive>
172.24.39.0/24      100.64.0.5/32       <recursive>
172.24.48.0/24      100.64.0.4/32       <recursive>
172.24.49.0/24      attached            GigabitEthernet0/0/0/0.49
172.24.49.0/32      broadcast           GigabitEthernet0/0/0/0.49
172.24.49.6/32      receive             GigabitEthernet0/0/0/0.49
172.24.49.9/32      172.24.49.9/32      GigabitEthernet0/0/0/0.49
172.24.49.255/32    broadcast           GigabitEthernet0/0/0/0.49
224.0.0.0/4         0.0.0.0/32          
224.0.0.0/24        receive
255.255.255.255/32  broadcast

VRF: default
_____________

Prefix              Next Hop            Interface
------------------- ------------------- ------------------
0.0.0.0/0           drop                default handler 
0.0.0.0/32          broadcast
100.64.0.4/32       192.168.46.4/32     GigabitEthernet0/0/0/0.46
                    192.168.56.5/32     GigabitEthernet0/0/0/0.56 (!)
100.64.0.5/32       192.168.46.4/32     GigabitEthernet0/0/0/0.46 (!)
                    192.168.56.5/32     GigabitEthernet0/0/0/0.56
100.64.0.6/32       receive             Loopback6
192.168.45.0/24     192.168.46.4/32     GigabitEthernet0/0/0/0.46
                    192.168.56.5/32     GigabitEthernet0/0/0/0.56
192.168.46.0/24     attached            GigabitEthernet0/0/0/0.46
192.168.46.0/32     broadcast           GigabitEthernet0/0/0/0.46
192.168.46.6/32     receive             GigabitEthernet0/0/0/0.46
192.168.46.255/32   broadcast           GigabitEthernet0/0/0/0.46
192.168.56.0/24     attached            GigabitEthernet0/0/0/0.56
192.168.56.0/32     broadcast           GigabitEthernet0/0/0/0.56
192.168.56.6/32     receive             GigabitEthernet0/0/0/0.56
192.168.56.255/32   broadcast           GigabitEthernet0/0/0/0.56
224.0.0.0/4         0.0.0.0/32          
224.0.0.0/24        receive
255.255.255.255/32  broadcast
RP/0/RP0/CPU0:cisco-kudo-08#

RP/0/RP0/CPU0:cisco-kudo-08#

RP/0/RP0/CPU0:cisco-kudo-08#show mpls forwarding

Sun Dec 27 04:38:11.540 UTC
Local  Outgoing    Prefix             Outgoing     Next Hop        Bytes       
Label  Label       or ID              Interface                    Switched    
------ ----------- ------------------ ------------ --------------- ------------
15046  Pop         SRLB (idx 46)      Gi0/0/0/0.46 192.168.46.4    0           
15056  Pop         SRLB (idx 56)      Gi0/0/0/0.56 192.168.56.5    0           
17004  Pop         SR Pfx (idx 1004)  Gi0/0/0/0.46 192.168.46.4    15343       
       17004       SR Pfx (idx 1004)  Gi0/0/0/0.56 192.168.56.5    0            (!)
17005  Pop         SR Pfx (idx 1005)  Gi0/0/0/0.56 192.168.56.5    15263       
       17005       SR Pfx (idx 1005)  Gi0/0/0/0.46 192.168.46.4    0            (!)
24000  Pop         SR Adj (idx 1)     Gi0/0/0/0.46 192.168.46.4    0           
       17004       SR Adj (idx 1)     Gi0/0/0/0.56 192.168.56.5    0            (!)
24001  Pop         SR Adj (idx 3)     Gi0/0/0/0.46 192.168.46.4    0           
24002  Pop         SR Adj (idx 1)     Gi0/0/0/0.56 192.168.56.5    0           
       17005       SR Adj (idx 1)     Gi0/0/0/0.46 192.168.46.4    0            (!)
24003  Pop         SR Adj (idx 3)     Gi0/0/0/0.56 192.168.56.5    0           
24004  Pop         SR Adj (idx 0)     Gi0/0/0/0.46 192.168.46.4    0           
       17004       SR Adj (idx 0)     Gi0/0/0/0.56 192.168.56.5    0            (!)
24005  Pop         SR Adj (idx 2)     Gi0/0/0/0.46 192.168.46.4    0           
24006  Pop         SR Adj (idx 0)     Gi0/0/0/0.56 192.168.56.5    0           
       17005       SR Adj (idx 0)     Gi0/0/0/0.46 192.168.46.4    0            (!)
24007  Pop         SR Adj (idx 2)     Gi0/0/0/0.56 192.168.56.5    0           
24008  Pop         100.64.0.4/32      Gi0/0/0/0.46 192.168.46.4    1571461     
       24010       100.64.0.4/32      Gi0/0/0/0.56 192.168.56.5    0            (!)
24009  Pop         192.168.45.0/24    Gi0/0/0/0.46 192.168.46.4    0           
       Pop         192.168.45.0/24    Gi0/0/0/0.56 192.168.56.5    0           
24010  Pop         100.64.0.5/32      Gi0/0/0/0.56 192.168.56.5    1384693     
       24010       100.64.0.5/32      Gi0/0/0/0.46 192.168.46.4    0            (!)
24011  24013       100.64.10.4/32[V]               100.64.0.4      520         
24012  24011       100.64.10.5/32[V]               100.64.0.5      0           
24013  Aggregate   UG-A: Per-VRF Aggr[V]   \
                                      UG-A                         1020        
24014  24012       100.64.10.19/32[V]              100.64.0.5      0           
24015  Unlabelled  100.64.10.29/32[V] Gi0/0/0/0.29 172.24.29.9     0           
24016  24011       172.24.19.0/24[V]               100.64.0.5      0           
24017  Aggregate   UG-B: Per-VRF Aggr[V]   \
                                      UG-B                         0           
24018  Unlabelled  100.64.20.49/32[V] Gi0/0/0/0.49 172.24.49.9     0           
24019  24039       100.64.10.1/32[V]               100.64.0.4      0           
24020  24042       100.64.10.2/32[V]               100.64.0.4      0           
24021  24045       100.64.10.3/32[V]               100.64.0.4      0           
24022  24040       100.64.10.18/32[V]              100.64.0.4      0           
24023  24043       100.64.10.28/32[V]              100.64.0.4      0           
24024  24041       172.24.18.0/24[V]               100.64.0.4      0           
24025  24044       172.24.28.0/24[V]               100.64.0.4      0           
RP/0/RP0/CPU0:cisco-kudo-08#
```
