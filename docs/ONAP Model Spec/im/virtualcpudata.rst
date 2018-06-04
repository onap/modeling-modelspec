.. Copyright 2018 (China Mobile)
.. This file is licensed under the CREATIVE COMMONS ATTRIBUTION 4.0 INTERNATIONAL LICENSE
.. Full license text at https://creativecommons.org/licenses/by/4.0/legalcode

Class: VirtualCpuData
=====================

+----------------------------------+-----------------------+------------------+-----------------+-------------------------+
| **Attribute Name**               | **Type**              | **Multiplicity** | **Description** | **Applied Stereotypes** |
+==================================+=======================+==================+=================+=========================+
| cpuArchitecture                  | String                | 0..1             | CPU             | support:                |
|                                  |                       |                  | architecture    | MANDATORY               |
|                                  |                       |                  | type.           |                         |
|                                  |                       |                  | Examples        |                         |
|                                  |                       |                  | are x86,        |                         |
|                                  |                       |                  | ARM. The        |                         |
|                                  |                       |                  | cardinality     |                         |
|                                  |                       |                  | can be 0        |                         |
|                                  |                       |                  | during the      |                         |
|                                  |                       |                  | allocation      |                         |
|                                  |                       |                  | request, if     |                         |
|                                  |                       |                  | no              |                         |
|                                  |                       |                  | particular      |                         |
|                                  |                       |                  | CPU             |                         |
|                                  |                       |                  | architecture    |                         |
|                                  |                       |                  | type is         |                         |
|                                  |                       |                  | requested.      |                         |
+----------------------------------+-----------------------+------------------+-----------------+-------------------------+
| numVirtualCpu                    | Integer               | 1                | Number of       | support:                |
|                                  |                       |                  | virtual         | MANDATORY               |
|                                  |                       |                  | CPUs.           |                         |
+----------------------------------+-----------------------+------------------+-----------------+-------------------------+
| virtualCpuClock                  | Number                | 0..1             | Minimum         | support:                |
|                                  | (recommended          |                  | virtual CPU     | MANDATORY               |
|                                  | DM type:              |                  | clock rate      |                         |
|                                  | Scalar-Unit-Freq)     |                  | (e.g. in        |                         |
|                                  |                       |                  | MHz). The       |                         |
|                                  |                       |                  | cardinality     |                         |
|                                  |                       |                  | can be 0        |                         |
|                                  |                       |                  | during the      |                         |
|                                  |                       |                  | allocation      |                         |
|                                  |                       |                  | request, if     |                         |
|                                  |                       |                  | no              |                         |
|                                  |                       |                  | particular      |                         |
|                                  |                       |                  | value is        |                         |
|                                  |                       |                  | requested.      |                         |
+----------------------------------+-----------------------+------------------+-----------------+-------------------------+
| virtualCpuOversubscriptionPolicy | String                | 0..1             | The CPU         | support:                |
|                                  |                       |                  | core            | MANDATORY               |
|                                  |                       |                  | oversubscription|                         |
|                                  |                       |                  | policy e.g.     |                         |
|                                  |                       |                  | the             |                         |
|                                  |                       |                  | relation of     |                         |
|                                  |                       |                  | virtual CPU     |                         |
|                                  |                       |                  | cores to        |                         |
|                                  |                       |                  | physical        |                         |
|                                  |                       |                  | CPU             |                         |
|                                  |                       |                  | cores/threads.  |                         |
|                                  |                       |                  | The             |                         |
|                                  |                       |                  | cardinality     |                         |
|                                  |                       |                  | can be 0        |                         |
|                                  |                       |                  | during the      |                         |
|                                  |                       |                  | allocation      |                         |
|                                  |                       |                  | request, if     |                         |
|                                  |                       |                  | no              |                         |
|                                  |                       |                  | particular      |                         |
|                                  |                       |                  | value is        |                         |
|                                  |                       |                  | requested.      |                         |
+----------------------------------+-----------------------+------------------+-----------------+-------------------------+
| vduCpuRequirements               | KeyValuePair          | 0..N             | Array of        | support:                |
|                                  |                       |                  | key-value       | MANDATORY               |
|                                  |                       |                  | pair            |                         |
|                                  |                       |                  | requirements    |                         |
|                                  |                       |                  | on the          |                         |
|                                  |                       |                  | Compute         |                         |
|                                  |                       |                  | (CPU) for       |                         |
|                                  |                       |                  | the VDU.        |                         |
+----------------------------------+-----------------------+------------------+-----------------+-------------------------+
| virtualCpuPinning                | VirtualCpuPinningData | 0..1             | The virtual     | support:                |
|                                  |                       |                  | CPU pinning     | MANDATORY               |
|                                  |                       |                  | configuration   |                         |
|                                  |                       |                  | for the         |                         |
|                                  |                       |                  | virtualised     |                         |
|                                  |                       |                  | compute         |                         |
|                                  |                       |                  | resource.       |                         |
+----------------------------------+-----------------------+------------------+-----------------+-------------------------+
