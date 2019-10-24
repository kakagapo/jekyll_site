---
layout: page
title: Service Fabric
permalink: /sf
---
Youtube videos:
===============
- [Inside Azure Service Fabric Playlist](https://www.youtube.com/watch?v=oIdkbdlnmbw&list=PLlrxD0HtieHh73JryJJ-GWcUtrqpcg2Pb)
    - [Inside Service Fabric Data Replication](https://www.youtube.com/watch?v=OlO7aSMGvJg)
    - [Inside Service Fabric Reconfiguration](https://www.youtube.com/watch?v=BvIWoMpj4vI)
    - [Inside Reliable Collections](https://www.youtube.com/watch?v=wcfewGJ6Tu8)
    - [Inside Service Fabric Health Manager](https://www.youtube.com/watch?v=EU9Wp3S9bCE)
    - [Inside the Failover Manager](https://www.youtube.com/watch?v=vM5x9kk6ZVY)
    - [Inside Service Fabric Hosting](https://www.youtube.com/watch?v=rRXu26YrcF8)

Heirarchy of components in a replica:
=====================================
- TStore/Reliable Collection
- ReliableStateManager
- Replicator
- Log
- Disk

Source code: 
============
[https://github.com/Microsoft/service-fabric](https://github.com/Microsoft/service-fabric)

Logging replicator:
===================
- Code @ src/prod/src/data/txnreplicator/loggingreplicator

Failover Manager(FM):
=====================
- Code @ src/prod/src/Reliability/Failover/fm
- Responsible for quorum management and failover

Logging Replicator:
==================
- ACID
- Write ahead logging used to do presumed abort
- Log mgmt, checkpoints
- Build new replicas

Notes:
======
- C++ co-routines used extensively in code
- ktl -> provides compartmentalization, does leak detection in debug mode
- Failover Manager(FM) is responsible for initiating the replica addition when we do ops like TargetReplicaSetSize increase say from 3 to 5.

