.. Copyright 2018 (China Mobile)
.. This file is licensed under the CREATIVE COMMONS ATTRIBUTION 4.0 INTERNATIONAL LICENSE
.. Full license text at https://creativecommons.org/licenses/by/4.0/legalcode

.. contents::
   :depth: 3
..

Class: VirtualComputeDesc/VirtualCompute
========================================

+-------------------+-------------+------------------+-----------------+--------------------------+
| **Attribute Name**| **Type**    | **Multiplicity** | **Description** | **Applied Stereotypes**  |
+===================+=============+==================+=================+==========================+
| virtualComp       | Identifier  | 1                | Unique          | support:                 |
| uteDescId         |             |                  | identifier      | MANDATORY                |
|                   |             |                  | of this         |                          |
|                   |             |                  | VirtualComp     |                          |
|                   |             |                  | uteDesc         |                          |
|                   |             |                  | in the          |                          |
|                   |             |                  | VNFD.           |                          |
+-------------------+-------------+------------------+-----------------+--------------------------+
| logicalNode       | LogicalNode | 1..N             | The logical     | support:                 |
|  (logical_n       | Data/Logici |                  | Node            | MANDATORY                |
| ode_id            | alNodeDesc  |                  | requirement     |                          |
| in SOL001)        |             |                  | s.              |                          |
+-------------------+-------------+------------------+-----------------+--------------------------+
| requestAddi       | RequestedAd | 0..N             | Specifies       | support:                 |
| tionalCapab       | ditionalCap |                  | requirement     | MANDATORY                |
| ilities           | abilityData |                  | s               |                          |
|                   |             |                  | for             |                          |
|                   |             |                  | additional      |                          |
|                   |             |                  | capabilitie     |                          |
|                   |             |                  | s.              |                          |
|                   |             |                  | These may       |                          |
|                   |             |                  | be for a        |                          |
|                   |             |                  | range of        |                          |
|                   |             |                  | purposes.       |                          |
|                   |             |                  | One example     |                          |
|                   |             |                  | is              |                          |
|                   |             |                  | acceleratio     |                          |
|                   |             |                  | n               |                          |
|                   |             |                  | related         |                          |
|                   |             |                  | capabilitie     |                          |
|                   |             |                  | s.              |                          |
+-------------------+-------------+------------------+-----------------+--------------------------+
| computeRequ       | KeyValuePai | 0..N             | Specifies       | support:                 |
| irements          | r/NameValue |                  | compute         | MANDATORY                |
|                   | Pair        |                  | requirement     |                          |
|                   |             |                  | s.              |                          |
+-------------------+-------------+------------------+-----------------+--------------------------+
| virtualMemo       | VirtualMemo | 1                | The virtual     | support:                 |
| ry                | ryData/Virt |                  | memory of       | MANDATORY                |
|                   | ualMemoryDe |                  | the             |                          |
|                   | sc          |                  | virtualised     |                          |
|                   |             |                  | compute.        |                          |
|                   | (VirtualMem |                  |                 |                          |
|                   | ory)        |                  |                 |                          |
+-------------------+-------------+------------------+-----------------+--------------------------+
| virtualCpu        | VirtualCpuD | 1                | The virtual     | support:                 |
|                   | ata/Virtual |                  | CPU(s) of       | MANDATORY                |
|                   | CPUDesc     |                  | the             |                          |
|                   |             |                  | virtualised     |                          |
|                   | (VirtualCpu |                  | compute.        |                          |
|                   | )           |                  |                 |                          |
+-------------------+-------------+------------------+-----------------+--------------------------+
                                                                                                  