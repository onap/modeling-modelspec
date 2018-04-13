.. Copyright 2018 (China Mobile)
.. This file is licensed under the CREATIVE COMMONS ATTRIBUTION 4.0 INTERNATIONAL LICENSE
.. Full license text at https://creativecommons.org/licenses/by/4.0/legalcode

.. contents::
   :depth: 3
..

Class: Cpd/CPDesc
=================

+--------------------+-------------+------------------+-----------------+--------------------------+
| **Attribute Name** | **Type**    | **Multiplicity** | **Description** | **Applied Stereotypes**  |
+====================+=============+==================+=================+==========================+
| cpdId              | Identifier  | 1                | Identifier      | support:                 |
|                    |             |                  | of this Cpd     | MANDATORY                |
|                    |             |                  | information     |                          |
|                    |             |                  | element.        |                          |
+--------------------+-------------+------------------+-----------------+--------------------------+
| cpRole             | String      | 0..1             | Identifies      | support:                 |
|                    |             |                  | the role of     | MANDATORY                |
|                    |             |                  | the port in     |                          |
|                    |             |                  | the context     |                          |
|                    |             |                  | of the          |                          |
|                    |             |                  | traffic         |                          |
|                    |             |                  | flow            |                          |
|                    |             |                  | patterns in     |                          |
|                    |             |                  | the VNF or      |                          |
|                    |             |                  | parent NS.      |                          |
|                    |             |                  |                 |                          |
|                    |             |                  | For example     |                          |
|                    |             |                  | a VNF with      |                          |
|                    |             |                  | a tree flow     |                          |
|                    |             |                  | pattern         |                          |
|                    |             |                  | within the      |                          |
|                    |             |                  | VNF will        |                          |
|                    |             |                  | have legal      |                          |
|                    |             |                  | cpRoles of      |                          |
|                    |             |                  | ROOT and        |                          |
|                    |             |                  | LEAF.           |                          |
+--------------------+-------------+------------------+-----------------+--------------------------+
| description        | String      | 0..1             | Provides        | support:                 |
|                    |             |                  | human-reada     | MANDATORY                |
|                    |             |                  | ble             |                          |
|                    |             |                  | information     |                          |
|                    |             |                  | on the          |                          |
|                    |             |                  | purpose of      |                          |
|                    |             |                  | the CP          |                          |
|                    |             |                  | (e.g. CP        |                          |
|                    |             |                  | for control     |                          |
|                    |             |                  | plane           |                          |
|                    |             |                  | traffic).       |                          |
+--------------------+-------------+------------------+-----------------+--------------------------+
| cpProtocol         | CpProtocolD | 1..N             | Identifies      | support:                 |
|                    | ata         |                  | the             | MANDATORY                |
|                    |             |                  | protocol        |                          |
|                    |             |                  | layering        |                          |
|                    |             |                  | information     |                          |
|                    |             |                  | the CP uses     |                          |
|                    |             |                  | for             |                          |
|                    |             |                  | connectivit     |                          |
|                    |             |                  | y               |                          |
|                    |             |                  | purposes        |                          |
|                    |             |                  | and             |                          |
|                    |             |                  | associated      |                          |
|                    |             |                  | information     |                          |
|                    |             |                  | .               |                          |
|                    |             |                  | There shall     |                          |
|                    |             |                  | be one          |                          |
|                    |             |                  | cpProtocol      |                          |
|                    |             |                  | for each        |                          |
|                    |             |                  | layer           |                          |
|                    |             |                  | protocol as     |                          |
|                    |             |                  | indicated       |                          |
|                    |             |                  | by the          |                          |
|                    |             |                  | attribute       |                          |
|                    |             |                  | layerProtoc     |                          |
|                    |             |                  | ol.             |                          |
|                    |             |                  |                 |                          |
|                    |             |                  | Editor's        |                          |
|                    |             |                  | note: the       |                          |
|                    |             |                  | attribute       |                          |
|                    |             |                  | "layerProto     |                          |
|                    |             |                  | col"            |                          |
|                    |             |                  | still needs     |                          |
|                    |             |                  | further         |                          |
|                    |             |                  | discussion      |                          |
|                    |             |                  | and not         |                          |
|                    |             |                  | included in     |                          |
|                    |             |                  | this table.     |                          |
+--------------------+-------------+------------------+-----------------+--------------------------+
| trunkMode          | Boolean     | 1                | Information     | support:                 |
|                    |             |                  | about           | MANDATORY                |
|                    |             |                  | whether the     |                          |
|                    |             |                  | CP              |                          |
|                    |             |                  | instantiate     |                          |
|                    |             |                  | d               |                          |
|                    |             |                  | from this       |                          |
|                    |             |                  | CPD is in       |                          |
|                    |             |                  | Trunk mode      |                          |
|                    |             |                  | (802.1Q or      |                          |
|                    |             |                  | other).         |                          |
+--------------------+-------------+------------------+-----------------+--------------------------+
| allowedAddr        | AddressData | 0..N             | For             | support:                 |
| essData            |             |                  | specifying      | MANDATORY                |
|                    |             |                  | floating        |                          |
|                    |             |                  | IP(s) to be     |                          |
|                    |             |                  | shared          |                          |
|                    |             |                  | among Cpds,     |                          |
|                    |             |                  | which are       |                          |
|                    |             |                  | reserved        |                          |
|                    |             |                  | for             |                          |
|                    |             |                  | vnfReserved     |                          |
|                    |             |                  | Cpd             |                          |
|                    |             |                  | described       |                          |
|                    |             |                  | in the          |                          |
|                    |             |                  | VNFD.           |                          |
+--------------------+-------------+------------------+-----------------+--------------------------+
