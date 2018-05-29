.. Copyright 2018 (China Mobile)
.. This file is licensed under the CREATIVE COMMONS ATTRIBUTION 4.0 INTERNATIONAL LICENSE
.. Full license text at https://creativecommons.org/licenses/by/4.0/legalcode

Class: VnfExtCpd
================

+-------------------------------------+-------------------------------------+------------------+-------------------------------------+--------------------------+
| **Attribute Name**                  | **Type**                            | **Multiplicity** | **Description**                     | **Applied Stereotypes**  |
+=====================================+=====================================+==================+=====================================+==========================+
| intCpd                              | Identifier                          | 0..1             | Reference                           | support:                 |
|                                     | (Reference                          |                  | to the                              | MANDATORY                |
|                                     | to VduCpd)                          |                  | internal                            |                          |
|                                     |                                     |                  | VDU CPD                             |                          |
|                                     |                                     |                  | which is                            |                          |
|                                     |                                     |                  | used to                             |                          |
|                                     |                                     |                  | instantiate                         |                          |
|                                     |                                     |                  | internal                            |                          |
|                                     |                                     |                  | CPs. These                          |                          |
|                                     |                                     |                  | internal                            |                          |
|                                     |                                     |                  | CPs are, in                         |                          |
|                                     |                                     |                  | turn,                               |                          |
|                                     |                                     |                  | exposed as                          |                          |
|                                     |                                     |                  | external                            |                          |
|                                     |                                     |                  | CPs defined                         |                          |
|                                     |                                     |                  | by this                             |                          |
|                                     |                                     |                  | external                            |                          |
|                                     |                                     |                  | CPD.                                |                          |
+-------------------------------------+-------------------------------------+------------------+-------------------------------------+--------------------------+
| virtualNetworkInterfaceRequirements | VirtualNetworkInterfaceRequirements | 0..N             | Specifies                           | support:                 |
|                                     |                                     |                  | requirements                        | MANDATORY                |
|                                     |                                     |                  | on a                                |                          |
|                                     |                                     |                  | virtual                             |                          |
|                                     |                                     |                  | network                             |                          |
|                                     |                                     |                  | interface                           |                          |
|                                     |                                     |                  | realising                           |                          |
|                                     |                                     |                  | the CPs                             |                          |
|                                     |                                     |                  | instantiated                        |                          |
|                                     |                                     |                  | from this                           |                          |
|                                     |                                     |                  | CPD.                                |                          |
|                                     |                                     |                  |                                     |                          |
|                                     |                                     |                  | NOTE: In                            |                          |
|                                     |                                     |                  | case of                             |                          |
|                                     |                                     |                  | referencing                         |                          |
|                                     |                                     |                  | an intCpd                           |                          |
|                                     |                                     |                  | via its                             |                          |
|                                     |                                     |                  | identifier,                         |                          |
|                                     |                                     |                  | the                                 |                          |
|                                     |                                     |                  | virtualNetworkInterfaceRequirements |                          |
|                                     |                                     |                  | attribute                           |                          |
|                                     |                                     |                  | of the                              |                          |
|                                     |                                     |                  | referenced                          |                          |
|                                     |                                     |                  | intCpd                              |                          |
|                                     |                                     |                  | applies.                            |                          |
+-------------------------------------+-------------------------------------+------------------+-------------------------------------+--------------------------+
| (inherited                          |                                     |                  | All                                 |                          |
| attributes)                         |                                     |                  | attributes                          |                          |
|                                     |                                     |                  | inherited                           |                          |
|                                     |                                     |                  | from Cpd.                           |                          |
+-------------------------------------+-------------------------------------+------------------+-------------------------------------+--------------------------+
                                                                       