.. Copyright 2018 (China Mobile)
.. This file is licensed under the CREATIVE COMMONS ATTRIBUTION 4.0 INTERNATIONAL LICENSE
.. Full license text at https://creativecommons.org/licenses/by/4.0/legalcode

Class: AffinityOrAntiAffinityGroup
==================================

+-------------+-------------+------------------+-----------------+-----------------+
| **Attribute | **Type**    | **Multiplicity** | **Description** | **Applied       |
| Name**      |             |                  |                 | Stereotypes**   |
+=============+=============+==================+=================+=================+
| groupId     | Identifier  | 1                | Identifies      | support:        |
|             |             |                  | an affinity or  | MANDATORY       |
|             |             |                  | anti-affinity   |                 |
|             |             |                  | group to which  |                 |
|             |             |                  | the affinity or |                 |
|             |             |                  | anti-affinity   |                 |
|             |             |                  | rule applies.   |                 |
+-------------+-------------+------------------+-----------------+-----------------+
| type        | Enum        | 1                | Specifies       | support:        |
|             |             |                  | whether the rule| MANDATORY       |
|             |             |                  | is an affinity  |                 |
|             |             |                  | rule or an      | valueRange:     |
|             |             |                  | anti-affinity   | "Affinity",     |
|             |             |                  | rule.           | "Anti-Affinity" |
+-------------+-------------+------------------+-----------------+-----------------+
| scope       | Enum        | 1                | Specifies       | support:        |
|             |             |                  | the scope       | MANDATORY       |
|             |             |                  | of the rule.    |                 |
|             |             |                  |                 | valueRange:     |
|             |             |                  |                 | "NFVI-PoP",     |
|             |             |                  |                 | "Zone",         |
|             |             |                  |                 | "ZoneGroup",    |
|             |             |                  |                 | "NFVI-node"     |
+-------------+-------------+------------------+-----------------+-----------------+
