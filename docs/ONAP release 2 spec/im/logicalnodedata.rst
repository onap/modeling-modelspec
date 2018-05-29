.. Copyright 2018 (China Mobile)
.. This file is licensed under the CREATIVE COMMONS ATTRIBUTION 4.0 INTERNATIONAL LICENSE
.. Full license text at https://creativecommons.org/licenses/by/4.0/legalcode

Class: LogicalNodeData
======================

+-------------------------+-------------+------------------+-----------------+--------------------------+
| **Attribute Name**      | **Type**    | **Multiplicity** | **Description** | **Applied Stereotypes**  |
+=========================+=============+==================+=================+==========================+
| logicalNodeRequirements | KeyValuePair| 0..N             | The logical     | support:                 |
|                         |             |                  | node-level      | MANDATORY                |
|                         |             |                  | compute,        |                          |
|                         |             |                  | memory and      |                          |
|                         |             |                  | I/O             |                          |
|                         |             |                  | requirements.   |                          |
|                         |             |                  | An array of     |                          |
|                         |             |                  | key-value       |                          |
|                         |             |                  | pairs that      |                          |
|                         |             |                  | articulate      |                          |
|                         |             |                  | the             |                          |
|                         |             |                  | deployment      |                          |
|                         |             |                  | requirements.   |                          |
|                         |             |                  |                 |                          |
|                         |             |                  | This could      |                          |
|                         |             |                  | include the     |                          |
|                         |             |                  | number of       |                          |
|                         |             |                  | CPU cores       |                          |
|                         |             |                  | on this         |                          |
|                         |             |                  | logical         |                          |
|                         |             |                  | node, a         |                          |
|                         |             |                  | memory          |                          |
|                         |             |                  | configuration   |                          |
|                         |             |                  | specific to     |                          |
|                         |             |                  | a logical       |                          |
|                         |             |                  | node (e.g.      |                          |
|                         |             |                  | such as         |                          |
|                         |             |                  | available       |                          |
|                         |             |                  | in the          |                          |
|                         |             |                  | Linux           |                          |
|                         |             |                  | kernel via      |                          |
|                         |             |                  | the libnuma     |                          |
|                         |             |                  | library) or     |                          |
|                         |             |                  | a               |                          |
|                         |             |                  | requirement     |                          |
|                         |             |                  | related to      |                          |
|                         |             |                  | the             |                          |
|                         |             |                  | association     |                          |
|                         |             |                  | of an I/O       |                          |
|                         |             |                  | device with     |                          |
|                         |             |                  | the logical     |                          |
|                         |             |                  | node.           |                          |
+-------------------------+-------------+------------------+-----------------+--------------------------+
