.. Copyright 2018 (China Mobile)
.. This file is licensed under the CREATIVE COMMONS ATTRIBUTION 4.0 INTERNATIONAL LICENSE
.. Full license text at https://creativecommons.org/licenses/by/4.0/legalcode

.. contents::
   :depth: 3
..

Class: VnfDf
============

+--------------------+-------------+------------------+-------------------+--------------------------+
| **Attribute Name** | **Type**    | **Multiplicity** | **Description**   | **Applied Stereotypes**  |
+====================+=============+==================+===================+==========================+
| flavorId           | Identifier  | 1                | Identifier        | support:                 |
|                    |             |                  | of this DF        | MANDATORY                |
|                    |             |                  | within the        |                          |
|                    |             |                  | VNFD.             |                          |
+--------------------+-------------+------------------+-------------------+--------------------------+
| description        | String      | 1                | Human             | support:                 |
|                    |             |                  | readable          | MANDATORY                |
|                    |             |                  | description       |                          |
|                    |             |                  | of the DF.        |                          |
+--------------------+-------------+------------------+-------------------+--------------------------+
| vduProfile         | VduProfile  | 1..N             | Describes         | support:                 |
|                    |             |                  | additional        | MANDATORY                |
|                    |             |                  | instantiati       |                          |
|                    |             |                  | on                |                          |
|                    |             |                  | data for          |                          |
|                    |             |                  | the VDUs          |                          |
|                    |             |                  | used in           |                          |
|                    |             |                  | this              |                          |
|                    |             |                  | flavor.           |                          |
+--------------------+-------------+------------------+-------------------+--------------------------+
| virtualLink        | VirtualLink | 0..N             | Defines the       | support:                 |
| Profile            | Profile     |                  | internal          | MANDATORY                |
|                    |             |                  | VLD along         |                          |
|                    |             |                  | with              |                          |
|                    |             |                  | additional        |                          |
|                    |             |                  | data which        |                          |
|                    |             |                  | is used in        |                          |
|                    |             |                  | this DF.          |                          |
|                    |             |                  |                   |                          |
|                    |             |                  | NOTE 1:           |                          |
|                    |             |                  | This allows       |                          |
|                    |             |                  | for               |                          |
|                    |             |                  | different         |                          |
|                    |             |                  | VNF               |                          |
|                    |             |                  | internal          |                          |
|                    |             |                  | topologies        |                          |
|                    |             |                  | between           |                          |
|                    |             |                  | DFs.              |                          |
|                    |             |                  |                   |                          |
|                    |             |                  | NOTE 2:           |                          |
|                    |             |                  | virtualLink       |                          |
|                    |             |                  | Profile           |                          |
|                    |             |                  | needs to be       |                          |
|                    |             |                  | provided          |                          |
|                    |             |                  | for all VLs       |                          |
|                    |             |                  | that the          |                          |
|                    |             |                  | CPs of the        |                          |
|                    |             |                  | VDUs in the       |                          |
|                    |             |                  | VDU               |                          |
|                    |             |                  | profiles          |                          |
|                    |             |                  | connect to.       |                          |
+--------------------+-------------+------------------+-------------------+--------------------------+
| instantiati        | Instantiati | 1..N             | Describes         | support:                 |
| onLevel            | onLevel     |                  | the various       | MANDATORY                |
|                    |             |                  | levels of         |                          |
|                    |             |                  | resources         |                          |
|                    |             |                  | that can be       |                          |
|                    |             |                  | used to           |                          |
|                    |             |                  | instantiate       |                          |
|                    |             |                  | the VNF           |                          |
|                    |             |                  | using this        |                          |
|                    |             |                  | flavour.          |                          |
|                    |             |                  |                   |                          |
|                    |             |                  | Examples:         |                          |
|                    |             |                  | Small,            |                          |
|                    |             |                  | Medium,           |                          |
|                    |             |                  | Large.            |                          |
|                    |             |                  |                   |                          |
|                    |             |                  | If there is       |                          |
|                    |             |                  | only one          |                          |
|                    |             |                  | "instantiat       |                          |
|                    |             |                  | ionLevel"         |                          |
|                    |             |                  | entry, it         |                          |
|                    |             |                  | shall be          |                          |
|                    |             |                  | treated as        |                          |
|                    |             |                  | the default       |                          |
|                    |             |                  | instantiati       |                          |
|                    |             |                  | on                |                          |
|                    |             |                  | level for         |                          |
|                    |             |                  | this DF.          |                          |
+--------------------+-------------+------------------+-------------------+--------------------------+
| affinityOrA        | AffinityOrA | 0..N             | Specifies         | support:                 |
| ntiAffinity        | ntiAffinity |                  | affinity or       |                          |
| Group              | Group       |                  | anti-affini       | MANDATORY                |
|                    |             |                  | ty                |                          |
|                    |             |                  | relationshi       |                          |
|                    |             |                  | p                 |                          |
|                    |             |                  | applicable        |                          |
|                    |             |                  | between the       |                          |
|                    |             |                  | virtualisat       |                          |
|                    |             |                  | ion               |                          |
|                    |             |                  | containers        |                          |
|                    |             |                  | (e.g.             |                          |
|                    |             |                  | virtual           |                          |
|                    |             |                  | machines)         |                          |
|                    |             |                  | to be             |                          |
|                    |             |                  | created           |                          |
|                    |             |                  | using             |                          |
|                    |             |                  | different         |                          |
|                    |             |                  | VDUs or           |                          |
|                    |             |                  | internal          |                          |
|                    |             |                  | VLs to be         |                          |
|                    |             |                  | created           |                          |
|                    |             |                  | using             |                          |
|                    |             |                  | different         |                          |
|                    |             |                  | VnfVirtualL       |                          |
|                    |             |                  | inkDesc(s)        |                          |
|                    |             |                  | in the same       |                          |
|                    |             |                  | affinity or       |                          |
|                    |             |                  | anti-affini       |                          |
|                    |             |                  | ty                |                          |
|                    |             |                  | group.            |                          |
|                    |             |                  |                   |                          |
|                    |             |                  | NOTE:             |                          |
|                    |             |                  | In the            |                          |
|                    |             |                  | present           |                          |
|                    |             |                  | specificati       |                          |
|                    |             |                  | on,               |                          |
|                    |             |                  | including         |                          |
|                    |             |                  | either            |                          |
|                    |             |                  | VDU(s) or         |                          |
|                    |             |                  | VnfVirtualL       |                          |
|                    |             |                  | inkDesc(s)        |                          |
|                    |             |                  | into the          |                          |
|                    |             |                  | same              |                          |
|                    |             |                  | affinity or       |                          |
|                    |             |                  | anti-affini       |                          |
|                    |             |                  | ty                |                          |
|                    |             |                  | group is          |                          |
|                    |             |                  | supported.        |                          |
|                    |             |                  | Extension         |                          |
|                    |             |                  | to support        |                          |
|                    |             |                  | including         |                          |
|                    |             |                  | both VDU(s)       |                          |
|                    |             |                  | and               |                          |
|                    |             |                  | VnfVirtualL       |                          |
|                    |             |                  | inkDesc(s)        |                          |
|                    |             |                  | into the          |                          |
|                    |             |                  | same              |                          |
|                    |             |                  | affinity or       |                          |
|                    |             |                  | anti-affini       |                          |
|                    |             |                  | ty                |                          |
|                    |             |                  | group is          |                          |
|                    |             |                  | left for          |                          |
|                    |             |                  | future            |                          |
|                    |             |                  | specificati       |                          |
|                    |             |                  | on.               |                          |
+--------------------+-------------+------------------+-------------------+--------------------------+
| scalingAspe        | ScalingAspe | 0..N             | The scaling       | support:                 |
| ct                 | ct          |                  | aspects           |                          |
|                    |             |                  | supported         | MANDATORY                |
|                    |             |                  | by this DF        |                          |
|                    |             |                  | of the VNF.       |                          |
|                    |             |                  | scalingAspe       |                          |
|                    |             |                  | ct                |                          |
|                    |             |                  | shall be          |                          |
|                    |             |                  | present if        |                          |
|                    |             |                  | the VNF           |                          |
|                    |             |                  | supports          |                          |
|                    |             |                  | scaling.          |                          |
+--------------------+-------------+------------------+-------------------+--------------------------+
| placementGr        | PlacementGr | 0..N             | Determine         | support:                 |
| oup                | oup         |                  | where             | EXPERIMENTA              |
|                    |             |                  | VNFC's            | L                        |
|                    |             |                  | (VDU's) are       |                          |
|                    |             |                  | placed with       |                          |
|                    |             |                  | respect to        |                          |
|                    |             |                  | the VNF           |                          |
+--------------------+-------------+------------------+-------------------+--------------------------+
| baseConfigG        | BaseConfigG | 0..1             |- BaseConfigGroup  | support:                 |
| roup               | roup        |                  |  may set          | EXPERIMENTA              |
|                    |             |                  |  Access           | L                        |
|                    |             |                  |  Control          |                          |
|                    |             |                  |  Lists            |                          |
|                    |             |                  |  (ACL's)          |                          |
|                    |             |                  |  and              |                          |
|                    |             |                  |  establish        |                          |
|                    |             |                  |  security         |                          |
|                    |             |                  |  groups           |                          |
|                    |             |                  |  and              |                          |
|                    |             |                  |  server           |                          |
|                    |             |                  |  groups.          |                          |
|                    |             |                  |                   |                          |
|                    |             |                  |- BaseConfigGroup  |                          |
|                    |             |                  |  creates/estab    |                          |
|                    |             |                  |  lishslishs       |                          |
|                    |             |                  |  storage for the  |                          |
|                    |             |                  |  VM's (OpenStack  |                          |
|                    |             |                  |  Cinder).         |                          |
|                    |             |                  |                   |                          |
|                    |             |                  |- BaseConfigGroup  |                          |
|                    |             |                  |  may              |                          |
|                    |             |                  |  establish        |                          |
|                    |             |                  |  internal         |                          |
|                    |             |                  |  networks         |                          |
|                    |             |                  |  such as          |                          |
|                    |             |                  |  OAM (VNF         |                          |
|                    |             |                  |  Mgmt) or         |                          |
|                    |             |                  |  MNS              |                          |
|                    |             |                  |  (Maintenance &   |                          |
|                    |             |                  |  Surveillance)    |                          |
|                    |             |                  |  established.     |                          |
+--------------------+-------------+------------------+-------------------+--------------------------+
| deploymentG        | DeploymentG | 1..N             | DeploymentG       | support:                 |
| roup               | roup        |                  | roup              | EXPERIMENTA              |
|                    |             |                  | provides          | L                        |
|                    |             |                  | the minimum       |                          |
|                    |             |                  | viable VDU        |                          |
|                    |             |                  | and               |                          |
|                    |             |                  | associated        |                          |
|                    |             |                  | VNFC              |                          |
|                    |             |                  | configurati       |                          |
|                    |             |                  | on                |                          |
|                    |             |                  | for a             |                          |
|                    |             |                  | useable           |                          |
|                    |             |                  | VNF.              |                          |
+--------------------+-------------+------------------+-------------------+--------------------------+
                                                                          