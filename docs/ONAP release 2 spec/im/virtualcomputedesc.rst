.. Copyright 2018 (China Mobile)
.. This file is licensed under the CREATIVE COMMONS ATTRIBUTION 4.0 INTERNATIONAL LICENSE
.. Full license text at https://creativecommons.org/licenses/by/4.0/legalcode

Class: VirtualComputeDesc
=========================

+-------------------------------+-----------------------------------+------------------+-------------------+--------------------------+
| **Attribute Name**            | **Type**                          | **Multiplicity** | **Description**   | **Applied Stereotypes**  |
+===============================+===================================+==================+===================+==========================+
| virtualComputeDescId          | Identifier                        | 1                | Unique            | support:                 |
|                               |                                   |                  | identifier        | MANDATORY                |
|                               |                                   |                  | of this           |                          |
|                               |                                   |                  | VirtualComputeDesc|                          |
|                               |                                   |                  | in the            |                          |
|                               |                                   |                  | VNFD.             |                          |
+-------------------------------+-----------------------------------+------------------+-------------------+--------------------------+
| logicalNode                   | LogicalNodeData                   | 1..N             | The logical       | support:                 |
|                               |                                   |                  | Node              | MANDATORY                |
|                               |                                   |                  | requirements.     |                          |
+-------------------------------+-----------------------------------+------------------+-------------------+--------------------------+
| requestAdditionalCapabilities | RequestedAdditionalCapabilityData | 0..N             | Specifies         | support:                 |
|                               |                                   |                  | requirements      | MANDATORY                |
|                               |                                   |                  | for               |                          |
|                               |                                   |                  | additional        |                          |
|                               |                                   |                  | capabilities.     |                          |
|                               |                                   |                  | These may         |                          |
|                               |                                   |                  | be for a          |                          |
|                               |                                   |                  | range of          |                          |
|                               |                                   |                  | purposes.         |                          |
|                               |                                   |                  | One example       |                          |
|                               |                                   |                  | is                |                          |
|                               |                                   |                  | acceleration      |                          |
|                               |                                   |                  | related           |                          |
|                               |                                   |                  | capabilities.     |                          |
+-------------------------------+-----------------------------------+------------------+-------------------+--------------------------+
| computeRequirements           | KeyValuePair                      | 0..N             | Specifies         | support:                 |
|                               |                                   |                  | compute           | MANDATORY                |
|                               |                                   |                  | requirements.     |                          |
+-------------------------------+-----------------------------------+------------------+-------------------+--------------------------+
| virtualMemory                 | VirtualMemoryData                 | 1                | The virtual       | support:                 |
|                               |                                   |                  | memory of         | MANDATORY                |
|                               |                                   |                  | the               |                          |
|                               |                                   |                  | virtualised       |                          |
|                               |                                   |                  | compute.          |                          |
|                               |                                   |                  |                   |                          |
|                               |                                   |                  |                   |                          |
+-------------------------------+-----------------------------------+------------------+-------------------+--------------------------+
| virtualCpu                    | VirtualCpuData                    | 1                | The virtual       | support:                 |
|                               |                                   |                  | CPU(s) of         | MANDATORY                |
|                               |                                   |                  | the               |                          |
|                               |                                   |                  | virtualised       |                          |
|                               |                                   |                  | compute.          |                          |
|                               |                                   |                  |                   |                          |
+-------------------------------+-----------------------------------+------------------+-------------------+--------------------------+
                                                                                                  