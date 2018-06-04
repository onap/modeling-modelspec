.. Copyright 2018 (China Mobile)
.. This file is licensed under the CREATIVE COMMONS ATTRIBUTION 4.0 INTERNATIONAL LICENSE
.. Full license text at https://creativecommons.org/licenses/by/4.0/legalcode

Class: VduCpd
=============

+------------------------------------+------------------------------------+------------------+------------------+--------------------------+
| **Attribute Name**                 | **Type**                           | **Multiplicity** | **Description**  | **Applied Stereotypes**  |
+====================================+====================================+==================+==================+==========================+
| bitrateRequirement                 | Number                             | 0..1             | Bitrate          | support:                 |
|                                    | (recommended                       |                  | requirement      | MANDATORY                |
|                                    | DM type: Scalar-Unit-Rate)         |                  | on this CP.      |                          |
+------------------------------------+------------------------------------+------------------+------------------+--------------------------+
| vnicName                           | String                             | 0..1             | Describes        | support:                 |
|                                    |                                    |                  | the name of      | MANDATORY                |
|                                    |                                    |                  | the vNIC         |                          |
|                                    |                                    |                  | this CP          |                          |
|                                    |                                    |                  | attaches         |                          |
|                                    |                                    |                  | to, e.g.         |                          |
|                                    |                                    |                  | eth0. It         |                          |
|                                    |                                    |                  | will be          |                          |
|                                    |                                    |                  | configured       |                          |
|                                    |                                    |                  | during the       |                          |
|                                    |                                    |                  | Vdu booting      |                          |
|                                    |                                    |                  | process.         |                          |
+------------------------------------+------------------------------------+------------------+------------------+--------------------------+
| vnicOrder                          | Integer                            | 0..1             | Describes        | support:                 |
|                                    |                                    |                  | the order        | MANDATORY                |
|                                    |                                    |                  | to create        |                          |
|                                    |                                    |                  | the vNIC         |                          |
|                                    |                                    |                  | within the       |                          |
|                                    |                                    |                  | scope of         |                          |
|                                    |                                    |                  | this Vdu.        |                          |
+------------------------------------+------------------------------------+------------------+------------------+--------------------------+
| vnicType                           | Enum                               | 0..1             | Describes        | support:                 |
|                                    |                                    |                  | the type of      | MANDATORY                |
|                                    |                                    |                  | the vNIC         |                          |
|                                    |                                    |                  | this CP          | valueRange:              |
|                                    |                                    |                  | attaches         | normal,                  |
|                                    |                                    |                  | to.              | macvtap,                 |
|                                    |                                    |                  |                  | direct,                  |
|                                    |                                    |                  |                  | baremetal,               |
|                                    |                                    |                  |                  | direct-physical          |
|                                    |                                    |                  |                  | and                      |
|                                    |                                    |                  |                  | virtio-forwarder         |
+------------------------------------+------------------------------------+------------------+------------------+--------------------------+
| virtualNetworkInterfaceRequirements| VirtualNetworkInterfaceRequirements| 0..N             | Specifies        | support:                 |
|                                    |                                    |                  | requirements     | MANDATORY                |
|                                    |                                    |                  | on a             |                          |
|                                    |                                    |                  | virtual          |                          |
|                                    |                                    |                  | network          |                          |
|                                    |                                    |                  | interface        |                          |
|                                    |                                    |                  | realising        |                          |
|                                    |                                    |                  | the CPs          |                          |
|                                    |                                    |                  | instantiated     |                          |
|                                    |                                    |                  | from this        |                          |
|                                    |                                    |                  | CPD.             |                          |
+------------------------------------+------------------------------------+------------------+------------------+--------------------------+
| (inherited                         |                                    |                  | All              |                          |
| attributes)                        |                                    |                  | attributes       |                          |
|                                    |                                    |                  | inherited        |                          |
|                                    |                                    |                  | from Cpd.        |                          |
+------------------------------------+------------------------------------+------------------+------------------+--------------------------+
