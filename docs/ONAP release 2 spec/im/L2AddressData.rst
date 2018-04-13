.. Copyright 2018 (Huawei)
.. This file is licensed under the CREATIVE COMMONS ATTRIBUTION 4.0 INTERNATIONAL LICENSE
.. Full license text at https://creativecommons.org/licenses/by/4.0/legalcode

Class: L2AddressData
======================

+----------------------+-------------+------------------+-----------------+---------------+
| **Attribute          | **Type**    | **Multiplicity** | **Description** | **Applied     |
| Name**               |             |                  |                 | Stereotypes** |
+======================+=============+==================+=================+===============+
| macAddressAssignment | Boolean     | 1                | Specify if      | support:      |
|                      |             |                  | the MAC address | MANDATORY     |
|                      |             |                  | assignment      |               |
|                      |             |                  | is the          |               |
|                      |             |                  | responsibility  |               |
|                      |             |                  | of management   |               |
|                      |             |                  | and             |               |
|                      |             |                  | orchestration   |               |
|                      |             |                  | function or not.|               |
|                      |             |                  |                 |               |
|                      |             |                  | If it is set to |               |
|                      |             |                  | True, it is the |               |
|                      |             |                  | management and  |               |
|                      |             |                  | orchestration   |               |
|                      |             |                  | function        |               |
|                      |             |                  | responsibility. |               |
|                      |             |                  |                 |               |
|                      |             |                  | If it is set to |               |
|                      |             |                  | False, it will  |               |
|                      |             |                  | be provided by  |               |
|                      |             |                  | an external     |               |
|                      |             |                  | entity, e.g.    |               |
|                      |             |                  | OSS/BSS.        |               |
+----------------------+-------------+------------------+-----------------+---------------+
