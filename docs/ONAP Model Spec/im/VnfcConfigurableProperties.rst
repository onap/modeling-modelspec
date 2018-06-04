.. Copyright 2018 (China Mobile)
.. This file is licensed under the CREATIVE COMMONS ATTRIBUTION 4.0 INTERNATIONAL LICENSE
.. Full license text at https://creativecommons.org/licenses/by/4.0/legalcode

Class: VnfcConfigurableProperties
=================================

+------------------------------------+-------------+------------------+-----------------+---------------+
| **Attribute Name**                 | **Type**    | **Multiplicity** | **Description** | **Applied     |
|                                    |             |                  |                 | Stereotypes** |
+====================================+=============+==================+=================+===============+
| additionalVnfcConfigurableProperty | String      | 0..N             | It provides     | support:      |
|                                    |             |                  | VNFC            | MANDATORY     |
|                                    |             |                  | configurable    |               |
|                                    |             |                  | properties      |               |
|                                    |             |                  | that can be     |               |
|                                    |             |                  | modified        |               |
|                                    |             |                  | using the       |               |
|                                    |             |                  | ModifyVnfInfo   |               |
|                                    |             |                  | operation.      |               |
|                                    |             |                  |                 |               |
|                                    |             |                  | NOTE: A         |               |
|                                    |             |                  | cardinality     |               |
|                                    |             |                  | of "0"          |               |
|                                    |             |                  | indicates       |               |
|                                    |             |                  | that            |               |
|                                    |             |                  | configuring     |               |
|                                    |             |                  | this            |               |
|                                    |             |                  | present VNF     |               |
|                                    |             |                  | property is     |               |
|                                    |             |                  | not             |               |
|                                    |             |                  | supported.      |               |
+------------------------------------+-------------+------------------+-----------------+---------------+
