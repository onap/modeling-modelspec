.. Copyright 2018 (China Mobile)
.. This file is licensed under the CREATIVE COMMONS ATTRIBUTION 4.0 INTERNATIONAL LICENSE
.. Full license text at https://creativecommons.org/licenses/by/4.0/legalcode

.. contents::
   :depth: 3
..

Class: VirtualMemoryData/VirtualMemoryDesc
==========================================

+--------------------+-------------+------------------+-----------------+-------------------------+
| **Attribute Name** | **Type**    | **Multiplicity** | **Description** | **Applied Stereotypes** |
+====================+=============+==================+=================+=========================+
| virtualMemS        | Number      | 1                | Amount of       | support:                |
| ize                | (recommende |                  | virtual         | MANDATORY               |
|                    | d           |                  | Memory          |                         |
|                    | DM type:    |                  | (e.g. in        |                         |
|                    | Scalar-Unit |                  | MB).            |                         |
|                    | -Size)      |                  |                 |                         |
+--------------------+-------------+------------------+-----------------+-------------------------+
| virtualMemO        | String      | 0..1             | The memory      | support:                |
| versubscrip        |             |                  | core            | MANDATORY               |
| tionPolicy         |             |                  | oversubscri     |                         |
|                    |             |                  | ption           |                         |
|                    |             |                  | policy in       |                         |
|                    |             |                  | terms of        |                         |
|                    |             |                  | virtual         |                         |
|                    |             |                  | memory to       |                         |
|                    |             |                  | physical        |                         |
|                    |             |                  | memory on       |                         |
|                    |             |                  | the             |                         |
|                    |             |                  | platform.       |                         |
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
| vduMemRequi        | KeyValuePai | 0..N             | Array of        | support:                |
| rements            | r/NameValue |                  | key-value       | MANDATORY               |
|                    | Pair        |                  | pair            |                         |
|                    |             |                  | requirement     |                         |
|                    |             |                  | s               |                         |
|                    |             |                  | on the          |                         |
|                    |             |                  | memory for      |                         |
|                    |             |                  | the VDU.        |                         |
+--------------------+-------------+------------------+-----------------+-------------------------+
| numaEnabled        | Boolean     | 0..1             | It              | support:                |
|                    |             |                  | specifies       | MANDATORY               |
|                    |             |                  | the memory      |                         |
|                    |             |                  | allocation      |                         |
|                    |             |                  | to be           |                         |
|                    |             |                  | cognisant       |                         |
|                    |             |                  | of the          |                         |
|                    |             |                  | relevant        |                         |
|                    |             |                  | process/cor     |                         |
|                    |             |                  | e               |                         |
|                    |             |                  | allocation.     |                         |
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
                                                                        