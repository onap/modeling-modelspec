.. Copyright 2018 (Huawei)
.. This file is licensed under the CREATIVE COMMONS ATTRIBUTION 4.0 INTERNATIONAL LICENSE
.. Full license text at https://creativecommons.org/licenses/by/4.0/legalcode

Class: LocalAffinityOrAntiAffinityRule

+-------------+-------------+------------------+-----------------+----------------+
| **Attribute | **Type**    | **Multiplicity** | **Description** | **Applied      |
| Name**      |             |                  |                 | Stereotypes**  |
+=============+=============+==================+=================+================+
| type        | Enum        | 1                | Specifies       | support:       |
|             |             |                  | whether the rule| MANDATORY      |
|             |             |                  | is an affinity  |                |
|             |             |                  | rule or an      | valueRange:    |
|             |             |                  | anti-affinity   | "Affinity",    |
|             |             |                  | rule.           | "Anti-Affinity"|
+-------------+-------------+------------------+-----------------+----------------+
| scope       | Enum        | 1                | Specifies the   | support:       |
|             |             |                  | scope of the    | MANDATORY      |
|             |             |                  | rule.           |                |
|             |             |                  |                 | valueRange:    |
|             |             |                  |                 | "NFVI-PoP",    |
|             |             |                  |                 | "Zone",        |
|             |             |                  |                 | "ZoneGroup",   |
|             |             |                  |                 | "NFVI-node"    |
+-------------+-------------+------------------+-----------------+----------------+
