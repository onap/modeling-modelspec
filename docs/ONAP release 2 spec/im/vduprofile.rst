.. Copyright 2018 (China Mobile)
.. This file is licensed under the CREATIVE COMMONS ATTRIBUTION 4.0 INTERNATIONAL LICENSE
.. Full license text at https://creativecommons.org/licenses/by/4.0/legalcode

.. contents::
   :depth: 3
..

Class: VduProfile
=================

+--------------------+-------------+-------------------+-----------------+--------------------------+
| **Attribute Name** | **Type**    | **Multiplicity**  | **Description** | **Applied Stereotypes**  |
+====================+=============+===================+=================+==========================+
| vduId              | Identifier  | 1                 | Uniquely        | support:                 |
|                    | (Reference  |                   | identifies      | MANDATORY                |
|                    | to Vdu)     |                   | a VDU.          |                          |
+--------------------+-------------+-------------------+-----------------+--------------------------+
| minNumberOf        | Integer     | 1                 | Minimum         | support:                 |
| Instances          |             |                   | number of       | MANDATORY                |
|                    |             |                   | instances       |                          |
|                    |             |                   | of the VNFC     |                          |
|                    |             |                   | based on        |                          |
|                    |             |                   | this VDU        |                          |
|                    |             |                   | that is         |                          |
|                    |             |                   | permitted       |                          |
|                    |             |                   | to exist        |                          |
|                    |             |                   | for this        |                          |
|                    |             |                   | flavour.        |                          |
+--------------------+-------------+-------------------+-----------------+--------------------------+
| maxNumberOf        | Integer     | 1                 | Maximum         | support:                 |
| Instances          |             |                   | number of       | MANDATORY                |
|                    |             |                   | instances       |                          |
|                    |             |                   | of the VNFC     |                          |
|                    |             |                   | based on        |                          |
|                    |             |                   | this VDU        |                          |
|                    |             |                   | that is         |                          |
|                    |             |                   | permitted       |                          |
|                    |             |                   | to exist        |                          |
|                    |             |                   | for this        |                          |
|                    |             |                   | flavour.        |                          |
+--------------------+-------------+-------------------+-----------------+--------------------------+
| localAffini        | LocalAffini | 0..N              | Specifies       | support:                 |
| tyOrAntiAff        | tyOrAntiAff |                   | affinity or     | MANDATORY                |
| inityRule          | inityRule   |                   | anti-affini     |                          |
|                    |             |                   | ty              |                          |
|                    |             |                   | rules           |                          |
|                    |             |                   | applicable      |                          |
|                    |             |                   | between the     |                          |
|                    |             |                   | virtualisat     |                          |
|                    |             |                   | ion             |                          |
|                    |             |                   | containers      |                          |
|                    |             |                   | (e.g.           |                          |
|                    |             |                   | virtual         |                          |
|                    |             |                   | machines)       |                          |
|                    |             |                   | to be           |                          |
|                    |             |                   | created         |                          |
|                    |             |                   | based on        |                          |
|                    |             |                   | this VDU.       |                          |
|                    |             |                   |                 |                          |
|                    |             |                   | When the        |                          |
|                    |             |                   | cardinality     |                          |
|                    |             |                   | is greater      |                          |
|                    |             |                   | than 1,         |                          |
|                    |             |                   | both            |                          |
|                    |             |                   | affinity        |                          |
|                    |             |                   | rule(s) and     |                          |
|                    |             |                   | anti-affini     |                          |
|                    |             |                   | ty              |                          |
|                    |             |                   | rule(s)         |                          |
|                    |             |                   | with            |                          |
|                    |             |                   | different       |                          |
|                    |             |                   | scopes          |                          |
|                    |             |                   | (e.g.           |                          |
|                    |             |                   | "Affinity       |                          |
|                    |             |                   | with the        |                          |
|                    |             |                   | scope           |                          |
|                    |             |                   | resource        |                          |
|                    |             |                   | zone and        |                          |
|                    |             |                   | anti-affini     |                          |
|                    |             |                   | ty              |                          |
|                    |             |                   | with the        |                          |
|                    |             |                   | scope NFVI      |                          |
|                    |             |                   | node") are      |                          |
|                    |             |                   | applicable      |                          |
|                    |             |                   | to the          |                          |
|                    |             |                   | virtualisat     |                          |
|                    |             |                   | ion             |                          |
|                    |             |                   | containers      |                          |
|                    |             |                   | (e.g.           |                          |
|                    |             |                   | virtual         |                          |
|                    |             |                   | machines)       |                          |
|                    |             |                   | to be           |                          |
|                    |             |                   | created         |                          |
|                    |             |                   | based on        |                          |
|                    |             |                   | this VDU.       |                          |
+--------------------+-------------+-------------------+-----------------+--------------------------+
| affinityOrA        | Identifier  | 0..N              | Identifier(     | support:                 |
| ntiAffinity        |             |                   | s)              | MANDATORY                |
| GroupId            |             |                   | of the          |                          |
|                    |             |                   | affinity or     |                          |
|                    |             |                   | anti-affini     |                          |
|                    |             |                   | ty              |                          |
|                    |             |                   | group(s)        |                          |
|                    |             |                   | the VDU         |                          |
|                    |             |                   | belongs to.     |                          |
|                    |             |                   |                 |                          |
|                    |             |                   | NOTE: Each      |                          |
|                    |             |                   | identifier      |                          |
|                    |             |                   | references      |                          |
|                    |             |                   | an affinity     |                          |
|                    |             |                   | or              |                          |
|                    |             |                   | anti-affini     |                          |
|                    |             |                   | ty              |                          |
|                    |             |                   | group which     |                          |
|                    |             |                   | expresses       |                          |
|                    |             |                   | affinity or     |                          |
|                    |             |                   | anti-affini     |                          |
|                    |             |                   | ty              |                          |
|                    |             |                   | relationshi     |                          |
|                    |             |                   | ps              |                          |
|                    |             |                   | between the     |                          |
|                    |             |                   | virtualisat     |                          |
|                    |             |                   | ion             |                          |
|                    |             |                   | container(s     |                          |
|                    |             |                   | )               |                          |
|                    |             |                   | (e.g.           |                          |
|                    |             |                   | virtual         |                          |
|                    |             |                   | machine(s))     |                          |
|                    |             |                   | to be           |                          |
|                    |             |                   | created         |                          |
|                    |             |                   | using this      |                          |
|                    |             |                   | VDU and the     |                          |
|                    |             |                   | virtualisat     |                          |
|                    |             |                   | ion             |                          |
|                    |             |                   | container(s     |                          |
|                    |             |                   | )               |                          |
|                    |             |                   | (e.g.           |                          |
|                    |             |                   | virtual         |                          |
|                    |             |                   | machine(s))     |                          |
|                    |             |                   | to be           |                          |
|                    |             |                   | created         |                          |
|                    |             |                   | using other     |                          |
|                    |             |                   | VDU(s) in       |                          |
|                    |             |                   | the same        |                          |
|                    |             |                   | group.          |                          |
+--------------------+-------------+-------------------+-----------------+--------------------------+
| watchdog           | String      | 0..1              | Watchdog        | support:                 |
|                    |             |                   | action to       | MANDATORY                |
|                    |             |                   | be              |                          |
|                    |             |                   | triggered       |                          |
|                    |             |                   | by the VIM      |                          |
|                    |             |                   | for the VNF     |                          |
|                    |             |                   | in case the     |                          |
|                    |             |                   | heart beat      |                          |
|                    |             |                   | fails, e.g.     |                          |
|                    |             |                   | reset or        |                          |
|                    |             |                   | hard            |                          |
|                    |             |                   | shutdown,       |                          |
|                    |             |                   | etc.            |                          |
+--------------------+-------------+-------------------+-----------------+--------------------------+
| vmBootUpTim        | Integer     | 0..1              | Timeout         | support:                 |
| eOut               |             |                   | value for       | OPTIONAL                 |
|                    |             |                   | the VNFM to     |                          |
|                    |             |                   | wait before     |                          |
|                    |             |                   | the             |                          |
|                    |             |                   | successful      |                          |
|                    |             |                   | booting up      |                          |
|                    |             |                   | of the VDU.     |                          |
+--------------------+-------------+-------------------+-----------------+--------------------------+
