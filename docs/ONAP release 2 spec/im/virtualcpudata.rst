.. Copyright 2018 (China Mobile)
.. This file is licensed under the CREATIVE COMMONS ATTRIBUTION 4.0 INTERNATIONAL LICENSE
.. Full license text at https://creativecommons.org/licenses/by/4.0/legalcode

.. contents::
   :depth: 3
..

Class: VirtualCpuData/VirtualCPUDesc
====================================

+--------------------+-------------+------------------+-----------------+-------------------------+
| **Attribute Name** | **Type**    | **Multiplicity** | **Description** | **Applied Stereotypes** |
+====================+=============+==================+=================+=========================+
| cpuArchitec        | String      | 0..1             | CPU             | support:                |
| ture               |             |                  | architectur     | MANDATORY               |
|                    |             |                  | e               |                         |
|                    |             |                  | type.           |                         |
|                    |             |                  | Examples        |                         |
|                    |             |                  | are x86,        |                         |
|                    |             |                  | ARM. The        |                         |
|                    |             |                  | cardinality     |                         |
|                    |             |                  | can be 0        |                         |
|                    |             |                  | during the      |                         |
|                    |             |                  | allocation      |                         |
|                    |             |                  | request, if     |                         |
|                    |             |                  | no              |                         |
|                    |             |                  | particular      |                         |
|                    |             |                  | CPU             |                         |
|                    |             |                  | architectur     |                         |
|                    |             |                  | e               |                         |
|                    |             |                  | type is         |                         |
|                    |             |                  | requested.      |                         |
+--------------------+-------------+------------------+-----------------+-------------------------+
| numVirtualC        | Integer     | 1                | Number of       | support:                |
| pu                 |             |                  | virtual         | MANDATORY               |
|                    |             |                  | CPUs.           |                         |
+--------------------+-------------+------------------+-----------------+-------------------------+
| virtualCpuC        | Number      | 0..1             | Minimum         | support:                |
| lock               | (recommende |                  | virtual CPU     | MANDATORY               |
|                    | d           |                  | clock rate      |                         |
|                    | DM type:    |                  | (e.g. in        |                         |
|                    | Scalar-Unit |                  | MHz). The       |                         |
|                    | -Freq)      |                  | cardinality     |                         |
|                    |             |                  | can be 0        |                         |
|                    |             |                  | during the      |                         |
|                    |             |                  | allocation      |                         |
|                    |             |                  | request, if     |                         |
|                    |             |                  | no              |                         |
|                    |             |                  | particular      |                         |
|                    |             |                  | value is        |                         |
|                    |             |                  | requested.      |                         |
+--------------------+-------------+------------------+-----------------+-------------------------+
| virtualCpuO        | String      | 0..1             | The CPU         | support:                |
| versubscrip        |             |                  | core            | MANDATORY               |
| tionPolicy         |             |                  | oversubscri     |                         |
|                    |             |                  | ption           |                         |
|                    |             |                  | policy e.g.     |                         |
|                    |             |                  | the             |                         |
|                    |             |                  | relation of     |                         |
|                    |             |                  | virtual CPU     |                         |
|                    |             |                  | cores to        |                         |
|                    |             |                  | physical        |                         |
|                    |             |                  | CPU             |                         |
|                    |             |                  | cores/threa     |                         |
|                    |             |                  | ds.             |                         |
|                    |             |                  | The             |                         |
|                    |             |                  | cardinality     |                         |
|                    |             |                  | can be 0        |                         |
|                    |             |                  | during the      |                         |
|                    |             |                  | allocation      |                         |
|                    |             |                  | request, if     |                         |
|                    |             |                  | no              |                         |
|                    |             |                  | particular      |                         |
|                    |             |                  | value is        |                         |
|                    |             |                  | requested.      |                         |
+--------------------+-------------+------------------+-----------------+-------------------------+
| vduCpuRequi        | KeyValuePai | 0..N             | Array of        | support:                |
| rements            | r/NameValue |                  | key-value       | MANDATORY               |
|                    | Pair        |                  | pair            |                         |
|                    |             |                  | requirement     |                         |
|                    |             |                  | s               |                         |
|                    |             |                  | on the          |                         |
|                    |             |                  | Compute         |                         |
|                    |             |                  | (CPU) for       |                         |
|                    |             |                  | the VDU.        |                         |
+--------------------+-------------+------------------+-----------------+-------------------------+
| virtualCpuP        | VirtualCpuP | 0..1             | The virtual     | support:                |
| inning             | inningData  |                  | CPU pinning     | MANDATORY               |
|                    |             |                  | configurati     |                         |
|                    |             |                  | on              | editor's                |
|                    |             |                  | for the         | note: need              |
|                    |             |                  | virtualised     | to check                |
|                    |             |                  | compute         | whether can             |
|                    |             |                  | resource.       | be optional             |
+--------------------+-------------+------------------+-----------------+-------------------------+
