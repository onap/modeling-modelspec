.. Copyright 2018 (Huawei)
.. This file is licensed under the CREATIVE COMMONS ATTRIBUTION 4.0 INTERNATIONAL LICENSE
.. Full license text at https://creativecommons.org/licenses/by/4.0/legalcode

Class: VduLevel
=================

+-----------------+-------------+------------------+-----------------+---------------+
| **Attribute     | **Type**    | **Multiplicity** | **Description** | **Applied     |
| Name**          |             |                  |                 | Stereotypes** |
+=================+=============+==================+=================+===============+
| vduId           | Identifier  | 1                | Uniquely        | support:      |
|                 | (Reference  |                  | identifies      | MANDATORY     |
|                 | to Vdu)     |                  | a VDU.          |               |
+-----------------+-------------+------------------+-----------------+---------------+
|numberOfInstances| Integer     | 1                | Number of       | support:      |
|                 |             |                  | instances       | MANDATORY     |
|                 |             |                  | of VNFC based on|               |
|                 |             |                  | this VDU to     |               |
|                 |             |                  | deploy for an   |               |
|                 |             |                  | instantiation   |               |
|                 |             |                  | level or for a  |               |
|                 |             |                  | scaling delta.  |               |
+-----------------+-------------+------------------+-----------------+---------------+
