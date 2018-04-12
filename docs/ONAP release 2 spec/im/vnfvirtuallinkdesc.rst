.. Copyright 2018 (China Mobile)
.. This file is licensed under the CREATIVE COMMONS ATTRIBUTION 4.0 INTERNATIONAL LICENSE
.. Full license text at https://creativecommons.org/licenses/by/4.0/legalcode

.. contents::
   :depth: 3
..

Class: VnfVirtualLinkDesc
=========================

+-------------------+-------------+------------------+-----------------+--------------------------+
| **Attribute Name**| **Type**    | **Multiplicity** | **Description** | **Applied Stereotypes**  |
+===================+=============+==================+=================+==========================+
| virtualLink       | Identifier  | 1                | Unique          | support:                 |
| DescId            |             |                  | identifier      | MANDATORY                |
|                   |             |                  | of this         |                          |
|                   |             |                  | internal        |                          |
|                   |             |                  | VLD in          |                          |
|                   |             |                  | VNFD.           |                          |
+-------------------+-------------+------------------+-----------------+--------------------------+
| virtualLink       | VirtualLink | 1..N             | Describes a     | support:                 |
| DescFlavour       | DescFlavour |                  | specific        | MANDATORY                |
|                   |             |                  | flavour of      |                          |
|                   |             |                  | the VL with     |                          |
|                   |             |                  | specific        |                          |
|                   |             |                  | bitrate         |                          |
|                   |             |                  | requirement     |                          |
|                   |             |                  | s.              |                          |
+-------------------+-------------+------------------+-----------------+--------------------------+
| connectivit       | Connectivit | 1                |                 | support:                 |
| yType             | yType       |                  |                 | MANDATORY                |
+-------------------+-------------+------------------+-----------------+--------------------------+
| testAccess        | String      | 0..N             | Specifies       | support:                 |
|                   |             |                  | test access     | MANDATORY                |
|                   |             |                  | facilities      |                          |
|                   |             |                  | expected on     |                          |
|                   |             |                  | the VL          |                          |
|                   |             |                  | (e.g. none,     |                          |
|                   |             |                  | passive         |                          |
|                   |             |                  | monitoring,     |                          |
|                   |             |                  | or active       |                          |
|                   |             |                  | (intrusive)     |                          |
|                   |             |                  | loopbacks       |                          |
|                   |             |                  | at              |                          |
|                   |             |                  | endpoints).     |                          |
+-------------------+-------------+------------------+-----------------+--------------------------+
| description       | String      | 0..1             | Provides        | support:                 |
|                   |             |                  | human-reada     | MANDATORY                |
|                   |             |                  | ble             |                          |
|                   |             |                  | information     |                          |
|                   |             |                  | on the          |                          |
|                   |             |                  | purpose of      |                          |
|                   |             |                  | the VL          |                          |
|                   |             |                  | (e.g.           |                          |
|                   |             |                  | control         |                          |
|                   |             |                  | plane           |                          |
|                   |             |                  | traffic).       |                          |
+-------------------+-------------+------------------+-----------------+--------------------------+
| monitoringP       | MonitoringP | 0..N             | Defines the     | support:                 |
| arameter          | arameter    |                  | virtualised     | MANDATORY                |
|                   |             |                  | resources       |                          |
|                   |             |                  | monitoring      |                          |
|                   |             |                  | parameters      |                          |
|                   |             |                  | on VLD          |                          |
|                   |             |                  | level.          |                          |
+-------------------+-------------+------------------+-----------------+--------------------------+
                                                                                                  