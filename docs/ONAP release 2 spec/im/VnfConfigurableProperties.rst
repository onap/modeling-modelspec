.. Copyright 2018 (Huawei)
.. This file is licensed under the CREATIVE COMMONS ATTRIBUTION 4.0 INTERNATIONAL LICENSE
.. Full license text at https://creativecommons.org/licenses/by/4.0/legalcode

Class: VnfConfigurableProperties
==================================

+--------------------------------+-------------+------------------+-----------------+---------------+
| **Attribute Name**             | **Type**    | **Multiplicity** | **Description** | **Applied     |
|                                |             |                  |                 | Stereotypes** |
+================================+=============+==================+=================+===============+
| isAutoscaleEnabled             | Boolean     | 0..1             | It permits      | support:      |
|                                |             |                  | to enable       | MANDATORY     |
|                                |             |                  | (TRUE)/disable  |               |
|                                |             |                  | (FALSE) the     |               |
|                                |             |                  | auto-scaling    |               |
|                                |             |                  | functionality.  |               |
|                                |             |                  |                 |               |
|                                |             |                  | NOTE: A         |               |
|                                |             |                  | cardinality     |               |
|                                |             |                  | of "0"          |               |
|                                |             |                  | indicates       |               |
|                                |             |                  | that            |               |
|                                |             |                  | configuring     |               |
|                                |             |                  | this            |               |
|                                |             |                  | present VNF     |               |
|                                |             |                  | property is     |               |
|                                |             |                  | not             |               |
|                                |             |                  | supported.      |               |
+--------------------------------+-------------+------------------+-----------------+---------------+
| isAutohealEnabled              | Boolean     | 0..1             | It permits      | support:      |
|                                |             |                  | to enable       | MANDATORY     |
|                                |             |                  | (TRUE)/disable  |               |
|                                |             |                  | (FALSE) the     |               |
|                                |             |                  | auto-healing    |               |
|                                |             |                  | functionality.  |               |
|                                |             |                  |                 |               |
|                                |             |                  | NOTE: A         |               |
|                                |             |                  | cardinality     |               |
|                                |             |                  | of "0"          |               |
|                                |             |                  | indicates       |               |
|                                |             |                  | that            |               |
|                                |             |                  | configuring     |               |
|                                |             |                  | this            |               |
|                                |             |                  | present VNF     |               |
|                                |             |                  | property is     |               |
|                                |             |                  | not             |               |
|                                |             |                  | supported.      |               |
+--------------------------------+-------------+------------------+-----------------+---------------+
| additionalConfigurableProperty | String      | 0..N             | It provides     | support:      |
|                                |             |                  | VNF             | MANDATORY     |
|                                |             |                  | specific        |               |
|                                |             |                  | configurable    |               |
|                                |             |                  | properties      |               |
|                                |             |                  | that can be     |               |
|                                |             |                  | modified        |               |
|                                |             |                  | using the       |               |
|                                |             |                  | ModifyVnfInfo   |               |
|                                |             |                  | operation.      |               |
+--------------------------------+-------------+------------------+-----------------+---------------+
