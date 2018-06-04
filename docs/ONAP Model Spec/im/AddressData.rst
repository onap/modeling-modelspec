.. Copyright 2018 (China Mobile)
.. This file is licensed under the CREATIVE COMMONS ATTRIBUTION 4.0 INTERNATIONAL LICENSE
.. Full license text at https://creativecommons.org/licenses/by/4.0/legalcode

Class: AddressData
==================

+---------------+---------------+------------------+-----------------+---------------+
| **Attribute   | **Type**      | **Multiplicity** | **Description** | **Applied     |
| Name**        |               |                  |                 | Stereotypes** |
+===============+===============+==================+=================+===============+
| addressType   | Identifier    | 1                | Describes       | support:      |
|               |               |                  | the type of     | MANDATORY     |
|               |               |                  | the address to  |               |
|               |               |                  | be assigned to  |               |
|               |               |                  | the CP          |               |
|               |               |                  | instantiated    |               |
|               |               |                  | from the        |               |
|               |               |                  | parent CPD.     |               |
|               |               |                  | The content     |               |
|               |               |                  | type shall      |               |
|               |               |                  | be aligned      |               |
|               |               |                  | with the        |               |
|               |               |                  | address type    |               |
|               |               |                  | supported       |               |
|               |               |                  | by the          |               |
|               |               |                  | layerProtocol   |               |
|               |               |                  | attribute       |               |
|               |               |                  | of the          |               |
|               |               |                  | parent CPD.     |               |
+---------------+---------------+------------------+-----------------+---------------+
| l2AddressData | L2AddressData | 0..1             | Provides the    | support:      |
|               |               |                  | information on  | MANDATORY     |
|               |               |                  | the MAC         |               |
|               |               |                  | addresses to be |               |
|               |               |                  | assigned to     |               |
|               |               |                  | the CP(s)       |               |
|               |               |                  | instantiated    |               |
|               |               |                  | from the        |               |
|               |               |                  | parent CPD.     |               |
|               |               |                  |                 |               |
|               |               |                  | Shall be present|               |
|               |               |                  | when the        |               |
|               |               |                  | addressType is  |               |
|               |               |                  | MAC address.    |               |
+---------------+---------------+------------------+-----------------+---------------+
| l3AddressData | L3AddressData | 0..1             | Provides the    | support:      |
|               |               |                  | information on  | MANDATORY     |
|               |               |                  | the IP addresses|               |
|               |               |                  | to be assigned  |               |
|               |               |                  | to the CP       |               |
|               |               |                  | instantiated    |               |
|               |               |                  | from the        |               |
|               |               |                  | parent CPD.     |               |
|               |               |                  |                 |               |
|               |               |                  | Shall be        |               |
|               |               |                  | present when    |               |
|               |               |                  | the addressType |               |
|               |               |                  | is IP address.  |               |
+---------------+---------------+------------------+-----------------+---------------+
