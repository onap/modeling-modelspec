.. Copyright 2018 (Huawei)
.. This file is licensed under the CREATIVE COMMONS ATTRIBUTION 4.0 INTERNATIONAL LICENSE
.. Full license text at https://creativecommons.org/licenses/by/4.0/legalcode

Class: RequestedAdditionalCapabilityData

+-----------------------------------------------+-------------+------------------+-----------------+---------------+
| **Attribute Name**                            | **Type**    | **Multiplicity** | **Description** | **Applied     |
|                                               |             |                  |                 | Stereotypes** |
+===============================================+=============+==================+=================+===============+
| requestedAdditionalCapabilityName             | String      | 1                | Identifies      | support:      |
|                                               |             |                  | a requested     | MANDATORY     |
|                                               |             |                  | additional      |               |
|                                               |             |                  | capability      | valueRange:   |
|                                               |             |                  | for the         | For           |
|                                               |             |                  | VDU.            | acceleration  |
|                                               |             |                  |                 | capabilities, |
|                                               |             |                  |                 | reference     |
|                                               |             |                  |                 | to ETSI GS    |
|                                               |             |                  |                 | NFV-IFA       |
|                                               |             |                  |                 | 002.          |
+-----------------------------------------------+-------------+------------------+-----------------+---------------+
| supportMandatory                              | Boolean     | 1                | Indicates       | support:      |
|                                               |             |                  | whether the     | MANDATORY     |
|                                               |             |                  | requested       |               |
|                                               |             |                  | additional      |               |
|                                               |             |                  | capability      |               |
|                                               |             |                  | is              |               |
|                                               |             |                  | mandatory       |               |
|                                               |             |                  | for             |               |
|                                               |             |                  | successful      |               |
|                                               |             |                  | operation.      |               |
+-----------------------------------------------+-------------+------------------+-----------------+---------------+
| minRequestedAdditionalCapabilityVersion       | String      | 0..1             | Identifies      | support:      |
|                                               |             |                  | the minimum     | MANDATORY     |
|                                               |             |                  | version of      |               |
|                                               |             |                  | the             |               |
|                                               |             |                  | requested       |               |
|                                               |             |                  | additional      |               |
|                                               |             |                  | capability.     |               |
+-----------------------------------------------+-------------+------------------+-----------------+---------------+
| preferredRequestedAdditionalCapabilityVersion | String      | 0..1             | Identifies      | support:      |
|                                               |             |                  | the             | MANDATORY     |
|                                               |             |                  | preferred       |               |
|                                               |             |                  | version of      |               |
|                                               |             |                  | the             |               |
|                                               |             |                  | requested       |               |
|                                               |             |                  | additional      |               |
|                                               |             |                  | capability.     |               |
+-----------------------------------------------+-------------+------------------+-----------------+---------------+
| targetPerformanceParameters                   | KeyValuePair| 1..N             | Identifies      | support:      |
|                                               |             |                  | specific        | MANDATORY     |
|                                               |             |                  | attributes,     |               |
|                                               |             |                  | dependent       |               |
|                                               |             |                  | on the          |               |
|                                               |             |                  | requested       |               |
|                                               |             |                  | additional      |               |
|                                               |             |                  | capability      |               |
|                                               |             |                  | type.           |               |
+-----------------------------------------------+-------------+------------------+-----------------+---------------+
