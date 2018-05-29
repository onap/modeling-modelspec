.. Copyright 2018 (China Mobile)
.. This file is licensed under the CREATIVE COMMONS ATTRIBUTION 4.0 INTERNATIONAL LICENSE
.. Full license text at https://creativecommons.org/licenses/by/4.0/legalcode

Class: VnfDf
============

+----------------------------+-----------------------------+------------------+-----------------------+--------------------------+
| **Attribute Name**         | **Type**                    | **Multiplicity** | **Description**       | **Applied Stereotypes**  |
+============================+=============================+==================+=======================+==========================+
| flavorId                   | Identifier                  | 1                | Identifier            | support:                 |
|                            |                             |                  | of this DF            | MANDATORY                |
|                            |                             |                  | within the            |                          |
|                            |                             |                  | VNFD.                 |                          |
+----------------------------+-----------------------------+------------------+-----------------------+--------------------------+
| description                | String                      | 1                | Human                 | support:                 |
|                            |                             |                  | readable              | MANDATORY                |
|                            |                             |                  | description           |                          |
|                            |                             |                  | of the DF.            |                          |
+----------------------------+-----------------------------+------------------+-----------------------+--------------------------+
| vduProfile                 | VduProfile                  | 1..N             | Describes             | support:                 |
|                            |                             |                  | additional            | MANDATORY                |
|                            |                             |                  | instantiation         |                          |
|                            |                             |                  | data for              |                          |
|                            |                             |                  | the VDUs              |                          |
|                            |                             |                  | used in               |                          |
|                            |                             |                  | this                  |                          |
|                            |                             |                  | flavor.               |                          |
+----------------------------+-----------------------------+------------------+-----------------------+--------------------------+
| virtualLinkProfile         | VirtualLinkProfile          | 0..N             | Defines the           | support:                 |
|                            |                             |                  | internal              | MANDATORY                |
|                            |                             |                  | VLD along             |                          |
|                            |                             |                  | with                  |                          |
|                            |                             |                  | additional            |                          |
|                            |                             |                  | data which            |                          |
|                            |                             |                  | is used in            |                          |
|                            |                             |                  | this DF.              |                          |
|                            |                             |                  |                       |                          |
|                            |                             |                  | NOTE 1:               |                          |
|                            |                             |                  | This allows           |                          |
|                            |                             |                  | for                   |                          |
|                            |                             |                  | different             |                          |
|                            |                             |                  | VNF                   |                          |
|                            |                             |                  | internal              |                          |
|                            |                             |                  | topologies            |                          |
|                            |                             |                  | between               |                          |
|                            |                             |                  | DFs.                  |                          |
|                            |                             |                  |                       |                          |
|                            |                             |                  | NOTE 2:               |                          |
|                            |                             |                  | virtualLink           |                          |
|                            |                             |                  | Profile               |                          |
|                            |                             |                  | needs to be           |                          |
|                            |                             |                  | provided              |                          |
|                            |                             |                  | for all VLs           |                          |
|                            |                             |                  | that the              |                          |
|                            |                             |                  | CPs of the            |                          |
|                            |                             |                  | VDUs in the           |                          |
|                            |                             |                  | VDU                   |                          |
|                            |                             |                  | profiles              |                          |
|                            |                             |                  | connect to.           |                          |
+----------------------------+-----------------------------+------------------+-----------------------+--------------------------+
| instantiationLevel         | InstantiationLevel          | 1..N             | Describes             | support:                 |
|                            |                             |                  | the various           | MANDATORY                |
|                            |                             |                  | levels of             |                          |
|                            |                             |                  | resources             |                          |
|                            |                             |                  | that can be           |                          |
|                            |                             |                  | used to               |                          |
|                            |                             |                  | instantiate           |                          |
|                            |                             |                  | the VNF               |                          |
|                            |                             |                  | using this            |                          |
|                            |                             |                  | flavour.              |                          |
|                            |                             |                  |                       |                          |
|                            |                             |                  | Examples:             |                          |
|                            |                             |                  | Small,                |                          |
|                            |                             |                  | Medium,               |                          |
|                            |                             |                  | Large.                |                          |
|                            |                             |                  |                       |                          |
|                            |                             |                  | If there is           |                          |
|                            |                             |                  | only one              |                          |
|                            |                             |                  | "instantiationLevel"  |                          |
|                            |                             |                  | entry, it             |                          |
|                            |                             |                  | shall be              |                          |
|                            |                             |                  | treated as            |                          |
|                            |                             |                  | the default           |                          |
|                            |                             |                  | instantiation         |                          |
|                            |                             |                  | level for             |                          |
|                            |                             |                  | this DF.              |                          |
+----------------------------+-----------------------------+------------------+-----------------------+--------------------------+
| affinityOrAntiAffinityGroup| AffinityOrAntiAffinityGroup | 0..N             | Specifies             | support:                 |
|                            |                             |                  | affinity or           | MANDATORY                |
|                            |                             |                  | anti-affinity         |                          |
|                            |                             |                  | relationship          |                          |
|                            |                             |                  | applicable            |                          |
|                            |                             |                  | between the           |                          |
|                            |                             |                  | virtualisation        |                          |
|                            |                             |                  | containers            |                          |
|                            |                             |                  | (e.g.                 |                          |
|                            |                             |                  | virtual               |                          |
|                            |                             |                  | machines)             |                          |
|                            |                             |                  | to be                 |                          |
|                            |                             |                  | created               |                          |
|                            |                             |                  | using                 |                          |
|                            |                             |                  | different             |                          |
|                            |                             |                  | VDUs or               |                          |
|                            |                             |                  | internal              |                          |
|                            |                             |                  | VLs to be             |                          |
|                            |                             |                  | created               |                          |
|                            |                             |                  | using                 |                          |
|                            |                             |                  | different             |                          |
|                            |                             |                  | VnfVirtualLinkDesc(s) |                          |
|                            |                             |                  | in the same           |                          |
|                            |                             |                  | affinity or           |                          |
|                            |                             |                  | anti-affinity         |                          |
|                            |                             |                  | group.                |                          |
|                            |                             |                  |                       |                          |
|                            |                             |                  | NOTE:                 |                          |
|                            |                             |                  | In the                |                          |
|                            |                             |                  | present               |                          |
|                            |                             |                  | specification,        |                          |
|                            |                             |                  | including             |                          |
|                            |                             |                  | either                |                          |
|                            |                             |                  | VDU(s) or             |                          |
|                            |                             |                  | VnfVirtualLinkDesc(s) |                          |
|                            |                             |                  | into the              |                          |
|                            |                             |                  | same                  |                          |
|                            |                             |                  | affinity or           |                          |
|                            |                             |                  | anti-affinity         |                          |
|                            |                             |                  | group is              |                          |
|                            |                             |                  | supported.            |                          |
|                            |                             |                  | Extension             |                          |
|                            |                             |                  | to support            |                          |
|                            |                             |                  | including             |                          |
|                            |                             |                  | both VDU(s)           |                          |
|                            |                             |                  | and                   |                          |
|                            |                             |                  | VnfVirtualLinkDesc(s) |                          |
|                            |                             |                  | into the              |                          |
|                            |                             |                  | same                  |                          |
|                            |                             |                  | affinity or           |                          |
|                            |                             |                  | anti-affinity         |                          |
|                            |                             |                  | group is              |                          |
|                            |                             |                  | left for              |                          |
|                            |                             |                  | future                |                          |
|                            |                             |                  | specification.        |                          |
+----------------------------+-----------------------------+------------------+-----------------------+--------------------------+
| scalingAspect              | ScalingAspect               | 0..N             | The scaling           | support:                 |
|                            |                             |                  | aspects               | MANDATORY                |
|                            |                             |                  | supported             |                          |
|                            |                             |                  | by this DF            |                          |
|                            |                             |                  | of the VNF.           |                          |
|                            |                             |                  | scalingAspect         |                          |
|                            |                             |                  | shall be              |                          |
|                            |                             |                  | present if            |                          |
|                            |                             |                  | the VNF               |                          |
|                            |                             |                  | supports              |                          |
|                            |                             |                  | scaling.              |                          |
+----------------------------+-----------------------------+------------------+-----------------------+--------------------------+
| placementGroup             | PlacementGroup              | 0..N             | Determine             | support:                 |
|                            |                             |                  | where                 | EXPERIMENTAL             |
|                            |                             |                  | VNFC's                |                          |
|                            |                             |                  | (VDU's) are           |                          |
|                            |                             |                  | placed with           |                          |
|                            |                             |                  | respect to            |                          |
|                            |                             |                  | the VNF               |                          |
+----------------------------+-----------------------------+------------------+-----------------------+--------------------------+
| baseConfigGroup            | BaseConfigGroup             | 0..1             |- BaseConfigGroup      | support:                 |
|                            |                             |                  |  may set              | EXPERIMENTAL             |
|                            |                             |                  |  Access               |                          |
|                            |                             |                  |  Control              |                          |
|                            |                             |                  |  Lists                |                          |
|                            |                             |                  |  (ACL's)              |                          |
|                            |                             |                  |  and                  |                          |
|                            |                             |                  |  establish            |                          |
|                            |                             |                  |  security             |                          |
|                            |                             |                  |  groups               |                          |
|                            |                             |                  |  and                  |                          |
|                            |                             |                  |  server               |                          |
|                            |                             |                  |  groups.              |                          |
|                            |                             |                  |                       |                          |
|                            |                             |                  |- BaseConfigGroup      |                          |
|                            |                             |                  |  creates/establishs   |                          |
|                            |                             |                  |  storage for the      |                          |
|                            |                             |                  |  VM's (OpenStack      |                          |
|                            |                             |                  |  Cinder).             |                          |
|                            |                             |                  |                       |                          |
|                            |                             |                  |- BaseConfigGroup      |                          |
|                            |                             |                  |  may                  |                          |
|                            |                             |                  |  establish            |                          |
|                            |                             |                  |  internal             |                          |
|                            |                             |                  |  networks             |                          |
|                            |                             |                  |  such as              |                          |
|                            |                             |                  |  OAM (VNF             |                          |
|                            |                             |                  |  Mgmt) or             |                          |
|                            |                             |                  |  MNS                  |                          |
|                            |                             |                  |  (Maintenance &       |                          |
|                            |                             |                  |  Surveillance)        |                          |
|                            |                             |                  |  established.         |                          |
+----------------------------+-----------------------------+------------------+-----------------------+--------------------------+
| deploymentGroup            | DeploymentGroup             | 1..N             | DeploymentGroup       | support:                 |
|                            |                             |                  | provides              | EXPERIMENTAL             |
|                            |                             |                  | the minimum           |                          |
|                            |                             |                  | viable VDU            |                          |
|                            |                             |                  | and                   |                          |
|                            |                             |                  | associated            |                          |
|                            |                             |                  | VNFC                  |                          |
|                            |                             |                  | configuration         |                          |
|                            |                             |                  | for a                 |                          |
|                            |                             |                  | useable               |                          |
|                            |                             |                  | VNF.                  |                          |
+----------------------------+-----------------------------+------------------+-----------------------+--------------------------+
                                                                          