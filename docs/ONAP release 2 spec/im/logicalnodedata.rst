.. Copyright 2018 (China Mobile)
.. This file is licensed under the CREATIVE COMMONS ATTRIBUTION 4.0 INTERNATIONAL LICENSE
.. Full license text at https://creativecommons.org/licenses/by/4.0/legalcode

.. contents::
   :depth: 3
..

Class: LogicalNodeData/LogicalNodeDesc
======================================

+--------------------+-------------+------------------+-----------------+--------------------------+
| **Attribute Name** | **Type**    | **Multiplicity** | **Description** | **Applied Stereotypes**  |
+====================+=============+==================+=================+==========================+
| logicalNode        | KeyValuePai | 0..N             | The logical     | support:                 |
| Requirement        | r/NameValue |                  | node-level      | MANDATORY                |
| s                  | Pair        |                  | compute,        |                          |
|                    |             |                  | memory and      |                          |
|                    |             |                  | I/O             |                          |
|                    |             |                  | requirement     |                          |
|                    |             |                  | s.              |                          |
|                    |             |                  | An array of     |                          |
|                    |             |                  | key-value       |                          |
|                    |             |                  | pairs that      |                          |
|                    |             |                  | articulate      |                          |
|                    |             |                  | the             |                          |
|                    |             |                  | deployment      |                          |
|                    |             |                  | requirement     |                          |
|                    |             |                  | s.              |                          |
|                    |             |                  |                 |                          |
|                    |             |                  | This could      |                          |
|                    |             |                  | include the     |                          |
|                    |             |                  | number of       |                          |
|                    |             |                  | CPU cores       |                          |
|                    |             |                  | on this         |                          |
|                    |             |                  | logical         |                          |
|                    |             |                  | node, a         |                          |
|                    |             |                  | memory          |                          |
|                    |             |                  | configurati     |                          |
|                    |             |                  | on              |                          |
|                    |             |                  | specific to     |                          |
|                    |             |                  | a logical       |                          |
|                    |             |                  | node (e.g.      |                          |
|                    |             |                  | such as         |                          |
|                    |             |                  | available       |                          |
|                    |             |                  | in the          |                          |
|                    |             |                  | Linux           |                          |
|                    |             |                  | kernel via      |                          |
|                    |             |                  | the libnuma     |                          |
|                    |             |                  | library) or     |                          |
|                    |             |                  | a               |                          |
|                    |             |                  | requirement     |                          |
|                    |             |                  | related to      |                          |
|                    |             |                  | the             |                          |
|                    |             |                  | association     |                          |
|                    |             |                  | of an I/O       |                          |
|                    |             |                  | device with     |                          |
|                    |             |                  | the logical     |                          |
|                    |             |                  | node.           |                          |
+--------------------+-------------+------------------+-----------------+--------------------------+
