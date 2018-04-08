.. Copyright 2018 (Huawei)
.. This file is licensed under the CREATIVE COMMONS ATTRIBUTION 4.0 INTERNATIONAL LICENSE
.. Full license text at https://creativecommons.org/licenses/by/4.0/legalcode

Class: VnfIndicator

+----------------+-------------+------------------+-----------------+---------------+
| **Attribute    | **Type**    | **Multiplicity** | **Description** | **Applied     |
| Name**         |             |                  |                 | Stereotypes** |
+================+=============+==================+=================+===============+
| id             | Identifier  | 1                | Unique          | support:      |
|                |             |                  | identifier.     | MANDATORY     |
+----------------+-------------+------------------+-----------------+---------------+
| name           | String      | 0..1             | The human       | support:      |
|                |             |                  | readable        | MANDATORY     |
|                |             |                  | name of the     |               |
|                |             |                  | VnfIndicator.   |               |
+----------------+-------------+------------------+-----------------+---------------+
| indicatorValue | String      | 1..N             | Defines the     | support:      |
|                |             |                  | allowed         | MANDATORY     |
|                |             |                  | values or       |               |
|                |             |                  | value           |               |
|                |             |                  | ranges of       |               |
|                |             |                  | this            |               |
|                |             |                  | indicator.      |               |
+----------------+-------------+------------------+-----------------+---------------+
| source         | Enum        | 1                | Describe        | support:      |
|                |             |                  | the source      | MANDATORY     |
|                |             |                  | of the          |               |
|                |             |                  | indicator.      | valueRange:   |
|                |             |                  | This tells      | "VNF",        |
|                |             |                  | the             | "EM",         |
|                |             |                  | consumer        | "Both"        |
|                |             |                  | where to        |               |
|                |             |                  | send the        |               |
|                |             |                  | subscription    |               |
|                |             |                  | request.        |               |
+----------------+-------------+------------------+-----------------+---------------+
