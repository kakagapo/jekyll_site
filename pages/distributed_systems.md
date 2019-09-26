---
layout: page
title: Distributed systems
permalink: /dist-sys
---
Partitioning schemes:
====================
1) Deterministic
    1.1) Range partitioning - eg: actor implementation in service fabric is based on stateful service using this scheme
    1.2) Hash partitioning
2) Non-deterministic - Input data is not used to determine the partition
    2.1) Round-robin
    2.2) Random

References:
===========
[1] Jingren Zhou , Nicolas Bruno , Wei Lin, Advanced partitioning techniques for massively distributed computation, Proceedings of the 2012 ACM SIGMOD International Conference on Management of Data, May 20-24, 2012, Scottsdale, Arizona, USA