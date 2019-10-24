---
layout: page
title: Distributed systems
permalink: /dist-sys
---
Partitioning schemes:
====================
- Deterministic
    - Range partitioning - eg: actor implementation in service fabric is based on stateful service using this scheme
    - Hash partitioning
- Non-deterministic - Input data is not used to determine the partition
    - Round-robin
    - Random

References:
===========
- Jingren Zhou , Nicolas Bruno , Wei Lin, Advanced partitioning techniques for massively distributed computation, Proceedings of the 2012 ACM SIGMOD International Conference on Management of Data, May 20-24, 2012, Scottsdale, Arizona, USA