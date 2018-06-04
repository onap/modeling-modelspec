.. Copyright 2018 (China Mobile)
.. This file is licensed under the CREATIVE COMMONS ATTRIBUTION 4.0 INTERNATIONAL LICENSE
.. Full license text at https://creativecommons.org/licenses/by/4.0/legalcode

Class: VirtualNetworkInterfaceRequirements
==========================================

+------------------------------+------------------+------------------+-----------------+--------------------------+
| **Attribute Name**           | **Type**         | **Multiplicity** | **Description** | **Applied  Stereotypes** |
+==============================+==================+==================+=================+==========================+
| name                         | String           | 0..1             | Provides a      | support:                 |
|                              |                  |                  | human           | MANDATORY                |
|                              |                  |                  | readable        |                          |
|                              |                  |                  | name for        |                          |
|                              |                  |                  | the             |                          |
|                              |                  |                  | requirement.    |                          |
+------------------------------+------------------+------------------+-----------------+--------------------------+
| description                  | String           | 0..1             | Provides a      | support:                 |
|                              |                  |                  | human           | MANDATORY                |
|                              |                  |                  | readable        |                          |
|                              |                  |                  | description     |                          |
|                              |                  |                  | of the          |                          |
|                              |                  |                  | requirement.    |                          |
+------------------------------+------------------+------------------+-----------------+--------------------------+
| supportMandatory             | Boolean          | 1                | Indicates       | support:                 |
|                              |                  |                  | whether         | MANDATORY                |
|                              |                  |                  | fulfilling      |                          |
|                              |                  |                  | the             |                          |
|                              |                  |                  | constraint      |                          |
|                              |                  |                  | is              |                          |
|                              |                  |                  | mandatory       |                          |
|                              |                  |                  | (TRUE) for      |                          |
|                              |                  |                  | successful      |                          |
|                              |                  |                  | operation       |                          |
|                              |                  |                  | or              |                          |
|                              |                  |                  | desirable       |                          |
|                              |                  |                  | (FALSE).        |                          |
+------------------------------+------------------+------------------+-----------------+--------------------------+
| networkInterfaceRequirements | KeyValuePair     | 0..N             | The network     | support:                 |
|                              |                  |                  | interface       | MANDATORY                |
|                              |                  |                  | requirements.   |                          |
|                              |                  |                  | An element      |                          |
|                              |                  |                  | from an         |                          |
|                              |                  |                  | array of        |                          |
|                              |                  |                  | key-value       |                          |
|                              |                  |                  | pairs that      |                          |
|                              |                  |                  | articulate      |                          |
|                              |                  |                  | the network     |                          |
|                              |                  |                  | interface       |                          |
|                              |                  |                  | deployment      |                          |
|                              |                  |                  | requirements.   |                          |
+------------------------------+------------------+------------------+-----------------+--------------------------+
| nicIoRequirements            | Identifier       | 0..1             | This            | support:                 |
|                              | (reference       |                  | references      | MANDATORY                |
|                              | to               |                  | (couples)       |                          |
|                              | logicalNodeData) |                  | the CPD         |                          |
|                              |                  |                  | with any        |                          |
|                              |                  |                  | logical         |                          |
|                              |                  |                  | node I/O        |                          |
|                              |                  |                  | requirements    |                          |
|                              |                  |                  | (for            |                          |
|                              |                  |                  | network         |                          |
|                              |                  |                  | devices)        |                          |
|                              |                  |                  | that may        |                          |
|                              |                  |                  | have been       |                          |
|                              |                  |                  | created.        |                          |
|                              |                  |                  | Linking         |                          |
|                              |                  |                  | these           |                          |
|                              |                  |                  | attributes      |                          |
|                              |                  |                  | is              |                          |
|                              |                  |                  | necessary       |                          |
|                              |                  |                  | so that so      |                          |
|                              |                  |                  | that I/O        |                          |
|                              |                  |                  | requirements    |                          |
|                              |                  |                  | that need       |                          |
|                              |                  |                  | to be           |                          |
|                              |                  |                  | articulated     |                          |
|                              |                  |                  | at the          |                          |
|                              |                  |                  | logical         |                          |
|                              |                  |                  | node level      |                          |
|                              |                  |                  | can be          |                          |
|                              |                  |                  | associated      |                          |
|                              |                  |                  | with the        |                          |
|                              |                  |                  | network         |                          |
|                              |                  |                  | interface       |                          |
|                              |                  |                  | requirements    |                          |
|                              |                  |                  | associated      |                          |
|                              |                  |                  | with the        |                          |
|                              |                  |                  | CPD.            |                          |
+------------------------------+------------------+------------------+-----------------+--------------------------+
