.. Copyright 2018 (China Mobile)
.. This file is licensed under the CREATIVE COMMONS ATTRIBUTION 4.0 INTERNATIONAL LICENSE
.. Full license text at https://creativecommons.org/licenses/by/4.0/legalcode

Class: VirtualMemoryData
========================

+----------------------------------+-------------------+------------------+-----------------+-------------------------+
| **Attribute Name**               | **Type**          | **Multiplicity** | **Description** | **Applied Stereotypes** |
+==================================+===================+==================+=================+=========================+
| virtualMemSize                   | Number            | 1                | Amount of       | support:                |
|                                  | (recommended      |                  | virtual         | MANDATORY               |
|                                  | DM type:          |                  | Memory          |                         |
|                                  | Scalar-Unit-Size) |                  | (e.g. in        |                         |
|                                  |                   |                  | MB).            |                         |
+----------------------------------+-------------------+------------------+-----------------+-------------------------+
| virtualMemOversubscriptionPolicy | String            | 0..1             | The memory      | support:                |
|                                  |                   |                  | core            | MANDATORY               |
|                                  |                   |                  | oversubscription|                         |
|                                  |                   |                  | policy in       |                         |
|                                  |                   |                  | terms of        |                         |
|                                  |                   |                  | virtual         |                         |
|                                  |                   |                  | memory to       |                         |
|                                  |                   |                  | physical        |                         |
|                                  |                   |                  | memory on       |                         |
|                                  |                   |                  | the             |                         |
|                                  |                   |                  | platform.       |                         |
|                                  |                   |                  | The             |                         |
|                                  |                   |                  | cardinality     |                         |
|                                  |                   |                  | can be 0        |                         |
|                                  |                   |                  | during the      |                         |
|                                  |                   |                  | allocation      |                         |
|                                  |                   |                  | request, if     |                         |
|                                  |                   |                  | no              |                         |
|                                  |                   |                  | particular      |                         |
|                                  |                   |                  | value is        |                         |
|                                  |                   |                  | requested.      |                         |
+----------------------------------+-------------------+------------------+-----------------+-------------------------+
| vduMemRequirements               | KeyValuePair      | 0..N             | Array of        | support:                |
|                                  |                   |                  | key-value       | MANDATORY               |
|                                  |                   |                  | pair            |                         |
|                                  |                   |                  | requirements    |                         |
|                                  |                   |                  | on the          |                         |
|                                  |                   |                  | memory for      |                         |
|                                  |                   |                  | the VDU.        |                         |
+----------------------------------+-------------------+------------------+-----------------+-------------------------+
| numaEnabled                      | Boolean           | 0..1             | It              | support:                |
|                                  |                   |                  | specifies       | MANDATORY               |
|                                  |                   |                  | the memory      |                         |
|                                  |                   |                  | allocation      |                         |
|                                  |                   |                  | to be           |                         |
|                                  |                   |                  | cognisant       |                         |
|                                  |                   |                  | of the          |                         |
|                                  |                   |                  | relevant        |                         |
|                                  |                   |                  | process/core    |                         |
|                                  |                   |                  | allocation.     |                         |
|                                  |                   |                  | The             |                         |
|                                  |                   |                  | cardinality     |                         |
|                                  |                   |                  | can be 0        |                         |
|                                  |                   |                  | during the      |                         |
|                                  |                   |                  | allocation      |                         |
|                                  |                   |                  | request, if     |                         |
|                                  |                   |                  | no              |                         |
|                                  |                   |                  | particular      |                         |
|                                  |                   |                  | value is        |                         |
|                                  |                   |                  | requested.      |                         |
+----------------------------------+-------------------+------------------+-----------------+-------------------------+
                                                                        