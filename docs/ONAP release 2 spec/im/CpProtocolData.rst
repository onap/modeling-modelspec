.. Copyright 2018 (Huawei)
.. This file is licensed under the CREATIVE COMMONS ATTRIBUTION 4.0 INTERNATIONAL LICENSE
.. Full license text at https://creativecommons.org/licenses/by/4.0/legalcode

Class: CpProtocolData
=======================

+-------------------------+-------------+------------------+-----------------+---------------+
| **Attribute Name**      | **Type**    | **Multiplicity** | **Description** | **Applied     |
|                         |             |                  |                 | Stereotypes** |
+=========================+=============+==================+=================+===============+
| associatedLayerProtocol | Enum        | 1                | One of the      | support:      |
|                         |             |                  | values of the   | MANDATORY     |
|                         |             |                  | attribute       |               |
|                         |             |                  | layerProtocol   |               |
|                         |             |                  | of the Cpd IE.  |               |
+-------------------------+-------------+------------------+-----------------+---------------+
| addressData             | AddressData | 0..N             | Provides        | support:      |
|                         |             |                  | information     | MANDATORY     |
|                         |             |                  | on the addresses|               |
|                         |             |                  | to be           |               |
|                         |             |                  | assigned to     |               |
|                         |             |                  | the CP(s)       |               |
|                         |             |                  | instantiated    |               |
|                         |             |                  | from the CPD.   |               |
+-------------------------+-------------+------------------+-----------------+---------------+
