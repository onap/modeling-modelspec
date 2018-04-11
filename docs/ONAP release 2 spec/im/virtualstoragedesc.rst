.. Copyright 2018 (China Mobile)
.. This file is licensed under the CREATIVE COMMONS ATTRIBUTION 4.0 INTERNATIONAL LICENSE
.. Full license text at https://creativecommons.org/licenses/by/4.0/legalcode

.. contents::
   :depth: 3
..

Class: VirtualStorageDesc
=========================

+-------------------+-------------+------------------+-----------------+-------------------------+
| **Attribute Name**| **Type**    | **Multiplicity** | **Description** | **Applied Stereotypes** |
+===================+=============+==================+=================+=========================+
| id                | Identifier  | 1                | Unique          | support:                |
|                   |             |                  | identifier      | MANDATORY               |
|                   |             |                  | of this         |                         |
|                   |             |                  | VirtualStor     |                         |
|                   |             |                  | ageDesc         |                         |
|                   |             |                  | in the          |                         |
|                   |             |                  | VNFD.           |                         |
+-------------------+-------------+------------------+-----------------+-------------------------+
| typeOfStora       | String      | 1                | Type of         | support:                |
| ge                |             |                  | virtualised     | MANDATORY               |
|                   |             |                  | storage         |                         |
|                   |             |                  | resource        |                         |
|                   |             |                  | (e.g.           |                         |
|                   |             |                  | volume,         |                         |
|                   |             |                  | object).        |                         |
+-------------------+-------------+------------------+-----------------+-------------------------+
| sizeOfStora       | Number      | 1                | Size of         | support:                |
| ge                | (recommende |                  | virtualised     | MANDATORY               |
|                   | d           |                  | storage         |                         |
|                   | DM type:    |                  | resource        |                         |
|                   | Scalar-Unit |                  | (e.g. size      |                         |
|                   | -Size)      |                  | of volume,      |                         |
|                   |             |                  | in GB).         |                         |
+-------------------+-------------+------------------+-----------------+-------------------------+
| vduStorageR       | KeyValuePai | 0..N             | An array of     | support:                |
| equirements       | r/NameValue |                  | key-value       | MANDATORY               |
|                   | Pair        |                  | pairs that      |                         |
|                   |             |                  | articulate      |                         |
|                   |             |                  | the storage     |                         |
|                   |             |                  | deployment      |                         |
|                   |             |                  | requirement     |                         |
|                   |             |                  | s.              |                         |
+-------------------+-------------+------------------+-----------------+-------------------------+
| rdmaEnabled       | Boolean     | 0..1             | Indicate if     | support:                |
|                   |             |                  | the storage     | MANDATORY               |
|                   |             |                  | support         |                         |
|                   |             |                  | RDMA.           |                         |
+-------------------+-------------+------------------+-----------------+-------------------------+
| swImageDesc       | Identifier  | 0..1             | Software        | support:                |
|                   | (Reference  |                  | image to be     | MANDATORY               |
|                   | to          |                  | loaded on       |                         |
|                   | SwImageDesc |                  | the             |                         |
|                   | )           |                  | VirtualStor     |                         |
|                   |             |                  | age             |                         |
|                   |             |                  | resource        |                         |
|                   |             |                  | created         |                         |
|                   |             |                  | based on        |                         |
|                   |             |                  | this            |                         |
|                   |             |                  | VirtualStor     |                         |
|                   |             |                  | ageDesc.        |                         |
+-------------------+-------------+------------------+-----------------+-------------------------+
                                                                                                 