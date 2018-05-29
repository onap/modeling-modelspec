.. Copyright 2018 (China Mobile)
.. This file is licensed under the CREATIVE COMMONS ATTRIBUTION 4.0 INTERNATIONAL LICENSE
.. Full license text at https://creativecommons.org/licenses/by/4.0/legalcode

Class: LinkBitrateRequirements
==============================

+--------------------+-------------+------------------+-----------------+--------------------------+
| **Attribute Name** | **Type**    | **Multiplicity** | **Description** | **Applied Stereotypes**  |
+====================+=============+==================+=================+==========================+
| root               | Number      | 1                | Throughput      | support:                 |
|                    |             |                  | requirement     | MANDATORY                |
|                    |             |                  | of the          |                          |
|                    |             |                  | link (e.g.      |                          |
|                    |             |                  | bitrate of      |                          |
|                    |             |                  | E-Line,         |                          |
|                    |             |                  | root            |                          |
|                    |             |                  | bitrate of      |                          |
|                    |             |                  | E-Tree,         |                          |
|                    |             |                  | aggregate       |                          |
|                    |             |                  | capacity of     |                          |
|                    |             |                  | E-LAN).         |                          |
+--------------------+-------------+------------------+-----------------+--------------------------+
| leaf               | Number      | 0..1             | Throughput      | support:                 |
|                    |             |                  | requirement     | MANDATORY                |
|                    |             |                  | of leaf         |                          |
|                    |             |                  | connections     |                          |
|                    |             |                  | to the link     |                          |
|                    |             |                  | when            |                          |
|                    |             |                  | applicable      |                          |
|                    |             |                  | to the          |                          |
|                    |             |                  | connectivity    |                          |
|                    |             |                  | type (e.g.      |                          |
|                    |             |                  | for E-Tree      |                          |
|                    |             |                  | and E-LAN       |                          |
|                    |             |                  | branches).      |                          |
|                    |             |                  |                 |                          |
|                    |             |                  | NOTE: The       |                          |
|                    |             |                  | present         |                          |
|                    |             |                  | document        |                          |
|                    |             |                  | does not        |                          |
|                    |             |                  | specify the     |                          |
|                    |             |                  | means to        |                          |
|                    |             |                  | declare         |                          |
|                    |             |                  | different       |                          |
|                    |             |                  | bitrate         |                          |
|                    |             |                  | requirements    |                          |
|                    |             |                  | for leaf        |                          |
|                    |             |                  | connections     |                          |
|                    |             |                  | (e.g. E-LAN     |                          |
|                    |             |                  | leaves).        |                          |
+--------------------+-------------+------------------+-----------------+--------------------------+
