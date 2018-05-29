.. Copyright 2018 (China Mobile)
.. This file is licensed under the CREATIVE COMMONS ATTRIBUTION 4.0 INTERNATIONAL LICENSE
.. Full license text at https://creativecommons.org/licenses/by/4.0/legalcode

Class: VnfdElementGroup
=======================

+--------------------+---------------------+------------------+--------------------+---------------+
| **Attribute        | **Type**            | **Multiplicity** | **Description**    | **Applied     |
| Name**             |                     |                  |                    | Stereotypes** |
+====================+=====================+==================+====================+===============+
| vnfdElementGroupId | Identifier          | 1                | Unique             | support:      |
|                    |                     |                  | identifier         | MANDATORY     |
|                    |                     |                  | of this            |               |
|                    |                     |                  | group in           |               |
|                    |                     |                  | the VNFD.          |               |
+--------------------+---------------------+------------------+--------------------+---------------+
| description        | String              | 1                | Human              | support:      |
|                    |                     |                  | readable           | MANDATORY     |
|                    |                     |                  | description        |               |
|                    |                     |                  | of the             |               |
|                    |                     |                  | group.             |               |
+--------------------+---------------------+------------------+--------------------+---------------+
| vdu                | Identifier          | 0..N             | References         | support:      |
|                    | (Reference          |                  | to Vdus            | MANDATORY     |
|                    | to Vdu)             |                  | that are           |               |
|                    |                     |                  | part of            |               |
|                    |                     |                  | this group.        |               |
+--------------------+---------------------+------------------+--------------------+---------------+
| virtualLinkDesc    | Identifier          | 0..N             | References         | support:      |
|                    | (Reference          |                  | to                 | MANDATORY     |
|                    | to                  |                  | VnfVirtualLinkDesc |               |
|                    | VnfVirtualLinkDesc) |                  | that are part of   |               |
|                    |                     |                  | this group.        |               |
+--------------------+---------------------+------------------+--------------------+---------------+
