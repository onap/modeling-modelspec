.. Copyright 2018 (China Mobile)
.. This file is licensed under the CREATIVE COMMONS ATTRIBUTION 4.0 INTERNATIONAL LICENSE
.. Full license text at https://creativecommons.org/licenses/by/4.0/legalcode

Class: VduProfile
=================

+---------------------------------+---------------------------------+-------------------+-----------------+--------------------------+
| **Attribute Name**              | **Type**                        | **Multiplicity**  | **Description** | **Applied Stereotypes**  |
+=================================+=================================+===================+=================+==========================+
| vduId                           | Identifier                      | 1                 | Uniquely        | support:                 |
|                                 | (Reference                      |                   | identifies      | MANDATORY                |
|                                 | to Vdu)                         |                   | a VDU.          |                          |
+---------------------------------+---------------------------------+-------------------+-----------------+--------------------------+
| minNumberOfInstances            | Integer                         | 1                 | Minimum         | support:                 |
|                                 |                                 |                   | number of       | MANDATORY                |
|                                 |                                 |                   | instances       |                          |
|                                 |                                 |                   | of the VNFC     |                          |
|                                 |                                 |                   | based on        |                          |
|                                 |                                 |                   | this VDU        |                          |
|                                 |                                 |                   | that is         |                          |
|                                 |                                 |                   | permitted       |                          |
|                                 |                                 |                   | to exist        |                          |
|                                 |                                 |                   | for this        |                          |
|                                 |                                 |                   | flavour.        |                          |
+---------------------------------+---------------------------------+-------------------+-----------------+--------------------------+
| maxNumberOfInstances            | Integer                         | 1                 | Maximum         | support:                 |
|                                 |                                 |                   | number of       | MANDATORY                |
|                                 |                                 |                   | instances       |                          |
|                                 |                                 |                   | of the VNFC     |                          |
|                                 |                                 |                   | based on        |                          |
|                                 |                                 |                   | this VDU        |                          |
|                                 |                                 |                   | that is         |                          |
|                                 |                                 |                   | permitted       |                          |
|                                 |                                 |                   | to exist        |                          |
|                                 |                                 |                   | for this        |                          |
|                                 |                                 |                   | flavour.        |                          |
+---------------------------------+---------------------------------+-------------------+-----------------+--------------------------+
| localAffinityOrAntiAffinityRule | LocalAffinityOrAntiAffinityRule | 0..N              | Specifies       | support:                 |
|                                 |                                 |                   | affinity or     | MANDATORY                |
|                                 |                                 |                   | anti-affinity   |                          |
|                                 |                                 |                   | rules           |                          |
|                                 |                                 |                   | applicable      |                          |
|                                 |                                 |                   | between the     |                          |
|                                 |                                 |                   | virtualisation  |                          |
|                                 |                                 |                   | containers      |                          |
|                                 |                                 |                   | (e.g.           |                          |
|                                 |                                 |                   | virtual         |                          |
|                                 |                                 |                   | machines)       |                          |
|                                 |                                 |                   | to be           |                          |
|                                 |                                 |                   | created         |                          |
|                                 |                                 |                   | based on        |                          |
|                                 |                                 |                   | this VDU.       |                          |
|                                 |                                 |                   |                 |                          |
|                                 |                                 |                   | When the        |                          |
|                                 |                                 |                   | cardinality     |                          |
|                                 |                                 |                   | is greater      |                          |
|                                 |                                 |                   | than 1,         |                          |
|                                 |                                 |                   | both            |                          |
|                                 |                                 |                   | affinity        |                          |
|                                 |                                 |                   | rule(s) and     |                          |
|                                 |                                 |                   | anti-affinity   |                          |
|                                 |                                 |                   | rule(s)         |                          |
|                                 |                                 |                   | with            |                          |
|                                 |                                 |                   | different       |                          |
|                                 |                                 |                   | scopes          |                          |
|                                 |                                 |                   | (e.g.           |                          |
|                                 |                                 |                   | "Affinity       |                          |
|                                 |                                 |                   | with the        |                          |
|                                 |                                 |                   | scope           |                          |
|                                 |                                 |                   | resource        |                          |
|                                 |                                 |                   | zone and        |                          |
|                                 |                                 |                   | anti-affinity   |                          |
|                                 |                                 |                   | with the        |                          |
|                                 |                                 |                   | scope NFVI      |                          |
|                                 |                                 |                   | node") are      |                          |
|                                 |                                 |                   | applicable      |                          |
|                                 |                                 |                   | to the          |                          |
|                                 |                                 |                   | virtualisation  |                          |
|                                 |                                 |                   | containers      |                          |
|                                 |                                 |                   | (e.g.           |                          |
|                                 |                                 |                   | virtual         |                          |
|                                 |                                 |                   | machines)       |                          |
|                                 |                                 |                   | to be           |                          |
|                                 |                                 |                   | created         |                          |
|                                 |                                 |                   | based on        |                          |
|                                 |                                 |                   | this VDU.       |                          |
+---------------------------------+---------------------------------+-------------------+-----------------+--------------------------+
| affinityOrAntiAffinityGroupId   | Identifier                      | 0..N              | Identifier(s)   | support:                 |
|                                 |                                 |                   | of the          | MANDATORY                |
|                                 |                                 |                   | affinity or     |                          |
|                                 |                                 |                   | anti-affinity   |                          |
|                                 |                                 |                   | group(s)        |                          |
|                                 |                                 |                   | the VDU         |                          |
|                                 |                                 |                   | belongs to.     |                          |
|                                 |                                 |                   |                 |                          |
|                                 |                                 |                   | NOTE: Each      |                          |
|                                 |                                 |                   | identifier      |                          |
|                                 |                                 |                   | references      |                          |
|                                 |                                 |                   | an affinity     |                          |
|                                 |                                 |                   | or              |                          |
|                                 |                                 |                   | anti-affinity   |                          |
|                                 |                                 |                   | group which     |                          |
|                                 |                                 |                   | expresses       |                          |
|                                 |                                 |                   | affinity or     |                          |
|                                 |                                 |                   | anti-affinity   |                          |
|                                 |                                 |                   | relationships   |                          |
|                                 |                                 |                   | between the     |                          |
|                                 |                                 |                   | virtualisation  |                          |
|                                 |                                 |                   | container(s)    |                          |
|                                 |                                 |                   | (e.g.           |                          |
|                                 |                                 |                   | virtual         |                          |
|                                 |                                 |                   | machine(s))     |                          |
|                                 |                                 |                   | to be           |                          |
|                                 |                                 |                   | created         |                          |
|                                 |                                 |                   | using this      |                          |
|                                 |                                 |                   | VDU and the     |                          |
|                                 |                                 |                   | virtualisation  |                          |
|                                 |                                 |                   | container(s)    |                          |
|                                 |                                 |                   | (e.g.           |                          |
|                                 |                                 |                   | virtual         |                          |
|                                 |                                 |                   | machine(s))     |                          |
|                                 |                                 |                   | to be           |                          |
|                                 |                                 |                   | created         |                          |
|                                 |                                 |                   | using other     |                          |
|                                 |                                 |                   | VDU(s) in       |                          |
|                                 |                                 |                   | the same        |                          |
|                                 |                                 |                   | group.          |                          |
+---------------------------------+---------------------------------+-------------------+-----------------+--------------------------+
| watchdog                        | String                          | 0..1              | Watchdog        | support:                 |
|                                 |                                 |                   | action to       | MANDATORY                |
|                                 |                                 |                   | be              |                          |
|                                 |                                 |                   | triggered       |                          |
|                                 |                                 |                   | by the VIM      |                          |
|                                 |                                 |                   | for the VNF     |                          |
|                                 |                                 |                   | in case the     |                          |
|                                 |                                 |                   | heart beat      |                          |
|                                 |                                 |                   | fails, e.g.     |                          |
|                                 |                                 |                   | reset or        |                          |
|                                 |                                 |                   | hard            |                          |
|                                 |                                 |                   | shutdown,       |                          |
|                                 |                                 |                   | etc.            |                          |
+---------------------------------+---------------------------------+-------------------+-----------------+--------------------------+
| vmBootUpTimeOut                 | Integer                         | 0..1              | Timeout         | support:                 |
|                                 |                                 |                   | value for       | OPTIONAL                 |
|                                 |                                 |                   | the VNFM to     |                          |
|                                 |                                 |                   | wait before     |                          |
|                                 |                                 |                   | the             |                          |
|                                 |                                 |                   | successful      |                          |
|                                 |                                 |                   | booting up      |                          |
|                                 |                                 |                   | of the VDU.     |                          |
+---------------------------------+---------------------------------+-------------------+-----------------+--------------------------+
