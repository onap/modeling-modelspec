.. Copyright 2018 (Huawei)
.. This file is licensed under the CREATIVE COMMONS ATTRIBUTION 4.0 INTERNATIONAL LICENSE
.. Full license text at https://creativecommons.org/licenses/by/4.0/legalcode

Class: QoS

+--------------------+-------------+------------------+-----------------+---------------+
| **Attribute Name** | **Type**    | **Multiplicity** | **Description** | **Applied     |
|                    |             |                  |                 | Stereotypes** |
+====================+=============+==================+=================+===============+
| latency            | Number      | 1                | Maximum         | support:      |
|                    |             |                  | latency in ms.  | MANDATORY     |
+--------------------+-------------+------------------+-----------------+---------------+
|packetDelayVariation| Number      | 1                | Maximum         | support:      |
|                    |             |                  | jitter in ms.   | MANDATORY     |
+--------------------+-------------+------------------+-----------------+---------------+
| packetLossRatio    | Number      | 0..1             | Maximum         | support:      |
|                    |             |                  | packet loss     | MANDATORY     |
|                    |             |                  | ratio.          |               |
|                    |             |                  | Cardinality     |               |
|                    |             |                  | is 0 if no      |               |
|                    |             |                  | packetLossRatio |               |
|                    |             |                  | requirement     |               |
|                    |             |                  | exists.         |               |
+--------------------+-------------+------------------+-----------------+---------------+
