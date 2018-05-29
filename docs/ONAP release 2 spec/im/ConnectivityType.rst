.. Copyright 2018 (China Mobile)
.. This file is licensed under the CREATIVE COMMONS ATTRIBUTION 4.0 INTERNATIONAL LICENSE
.. Full license text at https://creativecommons.org/licenses/by/4.0/legalcode

Class: ConnectivityType
=======================

+---------------+-------------+------------------+-----------------+---------------+
| **Attribute   | **Type**    | **Multiplicity** | **Description** | **Applied     |
| Name**        |             |                  |                 | Stereotypes** |
+===============+=============+==================+=================+===============+
| layerProtocol | Enum        | 1                | Identifies      | support:      |
|               |             |                  | the protocol    | MANDATORY     |
|               |             |                  | this VL gives   |               |
|               |             |                  | access to       |               |
|               |             |                  | (Ethernet,      |               |
|               |             |                  | MPLS, ODU2,     |               |
|               |             |                  | IPV4, IPV6,     |               |
|               |             |                  | Pseudo-Wire).   |               |
+---------------+-------------+------------------+-----------------+---------------+
| flowPattern   | String      | 0..1             | Identifies      | support:      |
|               |             |                  | the flow        | MANDATORY     |
|               |             |                  | pattern of the  |               |
|               |             |                  | the connectivity|               |
|               |             |                  | (Line, Tree,    |               |
|               |             |                  | Mesh).          |               |
+---------------+-------------+------------------+-----------------+---------------+
