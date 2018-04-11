.. Copyright 2018 (China Mobile)
.. This file is licensed under the CREATIVE COMMONS ATTRIBUTION 4.0 INTERNATIONAL LICENSE
.. Full license text at https://creativecommons.org/licenses/by/4.0/legalcode

.. contents::
   :depth: 3
..

Class: VirtualNetworkInterfaceRequirements
==========================================

+--------------------+-------------+------------------+-----------------+--------------------------+
| **Attribute Name** | **Type**    | **Multiplicity** | **Description** | **Applied  Stereotypes** |
+====================+=============+==================+=================+==========================+
| name               | String      | 0..1             | Provides a      | support:                 |
|                    |             |                  | human           | MANDATORY                |
|                    |             |                  | readable        |                          |
|                    |             |                  | name for        |                          |
|                    |             |                  | the             |                          |
|                    |             |                  | requirement     |                          |
|                    |             |                  | .               |                          |
+--------------------+-------------+------------------+-----------------+--------------------------+
| description        | String      | 0..1             | Provides a      | support:                 |
|                    |             |                  | human           | MANDATORY                |
|                    |             |                  | readable        |                          |
|                    |             |                  | description     |                          |
|                    |             |                  | of the          |                          |
|                    |             |                  | requirement     |                          |
|                    |             |                  | .               |                          |
+--------------------+-------------+------------------+-----------------+--------------------------+
| supportMand        | Boolean     | 1                | Indicates       | support:                 |
| atory              |             |                  | whether         | MANDATORY                |
|                    |             |                  | fulfilling      |                          |
|                    |             |                  | the             |                          |
|                    |             |                  | constraint      |                          |
|                    |             |                  | is              |                          |
|                    |             |                  | mandatory       |                          |
|                    |             |                  | (TRUE) for      |                          |
|                    |             |                  | successful      |                          |
|                    |             |                  | operation       |                          |
|                    |             |                  | or              |                          |
|                    |             |                  | desirable       |                          |
|                    |             |                  | (FALSE).        |                          |
+--------------------+-------------+------------------+-----------------+--------------------------+
| networkInte        | KeyValuePai | 0..N             | The network     | support:                 |
| rfaceRequir        | r/NameValue |                  | interface       | MANDATORY                |
| ements             | Pair        |                  | requirement     |                          |
|                    |             |                  | s.              |                          |
|                    |             |                  | An element      |                          |
|                    |             |                  | from an         |                          |
|                    |             |                  | array of        |                          |
|                    |             |                  | key-value       |                          |
|                    |             |                  | pairs that      |                          |
|                    |             |                  | articulate      |                          |
|                    |             |                  | the network     |                          |
|                    |             |                  | interface       |                          |
|                    |             |                  | deployment      |                          |
|                    |             |                  | requirement     |                          |
|                    |             |                  | s.              |                          |
+--------------------+-------------+------------------+-----------------+--------------------------+
| nicIoRequir        | Identifier  | 0..1             | This            | support:                 |
| ements             | (reference  |                  | references      | MANDATORY                |
|                    | to          |                  | (couples)       |                          |
|                    | logicalNode |                  | the CPD         |                          |
|                    | Data)       |                  | with any        |                          |
|                    |             |                  | logical         |                          |
|                    |             |                  | node I/O        |                          |
|                    |             |                  | requirement     |                          |
|                    |             |                  | s               |                          |
|                    |             |                  | (for            |                          |
|                    |             |                  | network         |                          |
|                    |             |                  | devices)        |                          |
|                    |             |                  | that may        |                          |
|                    |             |                  | have been       |                          |
|                    |             |                  | created.        |                          |
|                    |             |                  | Linking         |                          |
|                    |             |                  | these           |                          |
|                    |             |                  | attributes      |                          |
|                    |             |                  | is              |                          |
|                    |             |                  | necessary       |                          |
|                    |             |                  | so that so      |                          |
|                    |             |                  | that I/O        |                          |
|                    |             |                  | requirement     |                          |
|                    |             |                  | s               |                          |
|                    |             |                  | that need       |                          |
|                    |             |                  | to be           |                          |
|                    |             |                  | articulated     |                          |
|                    |             |                  | at the          |                          |
|                    |             |                  | logical         |                          |
|                    |             |                  | node level      |                          |
|                    |             |                  | can be          |                          |
|                    |             |                  | associated      |                          |
|                    |             |                  | with the        |                          |
|                    |             |                  | network         |                          |
|                    |             |                  | interface       |                          |
|                    |             |                  | requirement     |                          |
|                    |             |                  | s               |                          |
|                    |             |                  | associated      |                          |
|                    |             |                  | with the        |                          |
|                    |             |                  | CPD.            |                          |
+--------------------+-------------+------------------+-----------------+--------------------------+
