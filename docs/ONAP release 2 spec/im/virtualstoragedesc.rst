.. Copyright 2018 (China Mobile)
.. This file is licensed under the CREATIVE COMMONS ATTRIBUTION 4.0 INTERNATIONAL LICENSE
.. Full license text at https://creativecommons.org/licenses/by/4.0/legalcode

Class: VirtualStorageDesc
=========================

+------------------------+-------------------+------------------+---------------------+-------------------------+
| **Attribute Name**     | **Type**          | **Multiplicity** | **Description**     | **Applied Stereotypes** |
+========================+===================+==================+=====================+=========================+
| id                     | Identifier        | 1                | Unique              | support:                |
|                        |                   |                  | identifier          | MANDATORY               |
|                        |                   |                  | of this             |                         |
|                        |                   |                  | VirtualStorageDesc  |                         |
|                        |                   |                  | in the              |                         |
|                        |                   |                  | VNFD.               |                         |
+------------------------+-------------------+------------------+---------------------+-------------------------+
| typeOfStorage          | String            | 1                | Type of             | support:                |
|                        |                   |                  | virtualised         | MANDATORY               |
|                        |                   |                  | storage             |                         |
|                        |                   |                  | resource            |                         |
|                        |                   |                  | (e.g.               |                         |
|                        |                   |                  | volume,             |                         |
|                        |                   |                  | object).            |                         |
+------------------------+-------------------+------------------+---------------------+-------------------------+
| sizeOfStorage          | Number            | 1                | Size of             | support:                |
|                        | (recommended      |                  | virtualised         | MANDATORY               |
|                        | DM type:          |                  | storage             |                         |
|                        | Scalar-Unit-Size) |                  | resource            |                         |
|                        |                   |                  | (e.g. size          |                         |
|                        |                   |                  | of volume,          |                         |
|                        |                   |                  | in GB).             |                         |
+------------------------+-------------------+------------------+---------------------+-------------------------+
| vduStorageRequirements | KeyValuePair      | 0..N             | An array of         | support:                |
|                        |                   |                  | key-value           | MANDATORY               |
|                        |                   |                  | pairs that          |                         |
|                        |                   |                  | articulate          |                         |
|                        |                   |                  | the storage         |                         |
|                        |                   |                  | deployment          |                         |
|                        |                   |                  | requirements.       |                         |
+------------------------+-------------------+------------------+---------------------+-------------------------+
| rdmaEnabled            | Boolean           | 0..1             | Indicate if         | support:                |
|                        |                   |                  | the storage         | MANDATORY               |
|                        |                   |                  | support             |                         |
|                        |                   |                  | RDMA.               |                         |
+------------------------+-------------------+------------------+---------------------+-------------------------+
| swImageDesc            | Identifier        | 0..1             | Software            | support:                |
|                        | (Reference        |                  | image to be         | MANDATORY               |
|                        | to                |                  | loaded on           |                         |
|                        | SwImageDesc)      |                  | the                 |                         |
|                        |                   |                  | VirtualStorage      |                         |
|                        |                   |                  | resource            |                         |
|                        |                   |                  | created             |                         |
|                        |                   |                  | based on            |                         |
|                        |                   |                  | this                |                         |
|                        |                   |                  | VirtualStorageDesc. |                         |
+------------------------+-------------------+------------------+---------------------+-------------------------+
                                                                                                 