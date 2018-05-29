.. Copyright 2018 (China Mobile)
.. This file is licensed under the CREATIVE COMMONS ATTRIBUTION 4.0 INTERNATIONAL LICENSE
.. Full license text at https://creativecommons.org/licenses/by/4.0/legalcode

Class: VnfVirtualLinkDesc
=========================

+-----------------------+-----------------------+------------------+-----------------+--------------------------+
| **Attribute Name**    | **Type**              | **Multiplicity** | **Description** | **Applied Stereotypes**  |
+=======================+=======================+==================+=================+==========================+
| virtualLinkDescId     | Identifier            | 1                | Unique          | support:                 |
|                       |                       |                  | identifier      | MANDATORY                |
|                       |                       |                  | of this         |                          |
|                       |                       |                  | internal        |                          |
|                       |                       |                  | VLD in          |                          |
|                       |                       |                  | VNFD.           |                          |
+-----------------------+-----------------------+------------------+-----------------+--------------------------+
| virtualLinkDescFlavour| VirtualLinkDescFlavour| 1..N             | Describes a     | support:                 |
|                       |                       |                  | specific        | MANDATORY                |
|                       |                       |                  | flavour of      |                          |
|                       |                       |                  | the VL with     |                          |
|                       |                       |                  | specific        |                          |
|                       |                       |                  | bitrate         |                          |
|                       |                       |                  | requirements.   |                          |
+-----------------------+-----------------------+------------------+-----------------+--------------------------+
| connectivityType      | ConnectivityType      | 1                |                 | support:                 |
|                       |                       |                  |                 | MANDATORY                |
+-----------------------+-----------------------+------------------+-----------------+--------------------------+
| testAccess            | String                | 0..N             | Specifies       | support:                 |
|                       |                       |                  | test access     | MANDATORY                |
|                       |                       |                  | facilities      |                          |
|                       |                       |                  | expected on     |                          |
|                       |                       |                  | the VL          |                          |
|                       |                       |                  | (e.g. none,     |                          |
|                       |                       |                  | passive         |                          |
|                       |                       |                  | monitoring,     |                          |
|                       |                       |                  | or active       |                          |
|                       |                       |                  | (intrusive)     |                          |
|                       |                       |                  | loopbacks       |                          |
|                       |                       |                  | at              |                          |
|                       |                       |                  | endpoints).     |                          |
+-----------------------+-----------------------+------------------+-----------------+--------------------------+
| description           | String                | 0..1             | Provides        | support:                 |
|                       |                       |                  | human-readable  | MANDATORY                |
|                       |                       |                  | information     |                          |
|                       |                       |                  | on the          |                          |
|                       |                       |                  | purpose of      |                          |
|                       |                       |                  | the VL          |                          |
|                       |                       |                  | (e.g.           |                          |
|                       |                       |                  | control         |                          |
|                       |                       |                  | plane           |                          |
|                       |                       |                  | traffic).       |                          |
+-----------------------+-----------------------+------------------+-----------------+--------------------------+
| monitoringParameter   | MonitoringParameter   | 0..N             | Defines the     | support:                 |
|                       |                       |                  | virtualised     | MANDATORY                |
|                       |                       |                  | resources       |                          |
|                       |                       |                  | monitoring      |                          |
|                       |                       |                  | parameters      |                          |
|                       |                       |                  | on VLD          |                          |
|                       |                       |                  | level.          |                          |
+-----------------------+-----------------------+------------------+-----------------+--------------------------+
                                                                                                  