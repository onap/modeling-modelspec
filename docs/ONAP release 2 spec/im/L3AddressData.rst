.. Copyright 2018 (Huawei)
.. This file is licensed under the CREATIVE COMMONS ATTRIBUTION 4.0 INTERNATIONAL LICENSE
.. Full license text at https://creativecommons.org/licenses/by/4.0/legalcode

Class: L3AddressData

+---------------------+-------------+------------------+-----------------+---------------+
| **Attribute         | **Type**    | **Multiplicity** | **Description** | **Applied     |
| Name**              |             |                  |                 | Stereotypes** |
+=====================+=============+==================+=================+===============+
| iPAddressAssignment | Boolean     | 1                | Specify if      | support:      |
|                     |             |                  | the address     | MANDATORY     |
|                     |             |                  | assignment      |               |
|                     |             |                  | is the          |               |
|                     |             |                  | responsibility  |               |
|                     |             |                  | of management   |               |
|                     |             |                  | and             |               |
|                     |             |                  | orchestration   |               |
|                     |             |                  | function or not.|               |
|                     |             |                  |                 |               |
|                     |             |                  | If it is set to |               |
|                     |             |                  | True, it is the |               |
|                     |             |                  | management and  |               |
|                     |             |                  | orchestration   |               |
|                     |             |                  | function        |               |
|                     |             |                  | responsibility. |               |
+---------------------+-------------+------------------+-----------------+---------------+
| floatingIpActivated | Boolean     | 1                | Specify if the  | support:      |
|                     |             |                  | floating IP     | MANDATORY     |
|                     |             |                  | scheme is       |               |
|                     |             |                  | activated on    |               |
|                     |             |                  | the CP or not.  |               |
+---------------------+-------------+------------------+-----------------+---------------+
| iPAddressType       | Enum        | 0..1             | Define address  | support:      |
|                     |             |                  | type.           | MANDATORY     |
|                     |             |                  |                 |               |
|                     |             |                  | NOTE: The       | valueRange:   |
|                     |             |                  | address type    | "IPv4",       |
|                     |             |                  | should be       | "IPv6"        |
|                     |             |                  | aligned with    |               |
|                     |             |                  | the address type|               |
|                     |             |                  | supported by the|               |
|                     |             |                  | layerProtocol   |               |
|                     |             |                  | attribute of    |               |
|                     |             |                  | the parent Cpd. |               |
+---------------------+-------------+------------------+-----------------+---------------+
| numberOfIpAddress   | Integer     | 0..1             | Minimum         | support:      |
|                     |             |                  | number of IP    | MANDATORY     |
|                     |             |                  | addresses to be |               |
|                     |             |                  | assigned based  |               |
|                     |             |                  | on this         |               |
|                     |             |                  | L3AddressData   |               |
|                     |             |                  | information     |               |
|                     |             |                  | element.        |               |
+---------------------+-------------+------------------+-----------------+---------------+
