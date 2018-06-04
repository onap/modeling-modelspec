.. Copyright 2018 (China Mobile)
.. This file is licensed under the CREATIVE COMMONS ATTRIBUTION 4.0 INTERNATIONAL LICENSE
.. Full license text at https://creativecommons.org/licenses/by/4.0/legalcode

Class: VirtualLinkProfile
=========================

+---------------------------------+---------------------------------+------------------+-----------------------+--------------------------+
| **Attribute Name**              | **Type**                        | **Multiplicity** | **Description**       | **Applied Stereotypes**  |
+=================================+=================================+==================+=======================+==========================+
| vnfVirtualLinkDescId            | Identifier                      | 1                | Uniquely              | support:                 |
|                                 | (Reference                      |                  | identifies            | MANDATORY                |
|                                 | to                              |                  | a Vnf VLD.            |                          |
|                                 | VnfVirtualLinkDesc)             |                  |                       |                          |
|                                 |                                 |                  |                       |                          |
+---------------------------------+---------------------------------+------------------+-----------------------+--------------------------+
| flavourId                       | Identifier                      | 1                | Identifies            | support:                 |
|                                 | (Reference                      |                  | a flavour             | MANDATORY                |
|                                 | to                              |                  | within the            |                          |
|                                 | VirtualLinkDescFlavour)         |                  | VnfVirtualLinkDesc.   |                          |
+---------------------------------+---------------------------------+------------------+-----------------------+--------------------------+
| localAffinityOrAntiAffinityRule | LocalAffinityOrAntiAffinityRule | 0..N             | Specifies             | support:                 |
|                                 |                                 |                  | affinity or           | MANDATORY                |
|                                 |                                 |                  | anti-affinity         |                          |
|                                 |                                 |                  | rules                 |                          |
|                                 |                                 |                  | applicable            |                          |
|                                 |                                 |                  | between the           |                          |
|                                 |                                 |                  | VLs based             |                          |
|                                 |                                 |                  | on this               |                          |
|                                 |                                 |                  | VnfVirtualLinkDesc.   |                          |
|                                 |                                 |                  |                       |                          |
|                                 |                                 |                  | When the              |                          |
|                                 |                                 |                  | cardinality           |                          |
|                                 |                                 |                  | is greater            |                          |
|                                 |                                 |                  | than 1,               |                          |
|                                 |                                 |                  | both                  |                          |
|                                 |                                 |                  | affinity              |                          |
|                                 |                                 |                  | rule(s) and           |                          |
|                                 |                                 |                  | anti-affinity         |                          |
|                                 |                                 |                  | rule(s) with          |                          |
|                                 |                                 |                  | different             |                          |
|                                 |                                 |                  | scopes are            |                          |
|                                 |                                 |                  | applicable            |                          |
|                                 |                                 |                  | to the VLs            |                          |
|                                 |                                 |                  | based on this         |                          |
|                                 |                                 |                  | VnfVirtualLinkDesc.   |                          |
+---------------------------------+---------------------------------+------------------+-----------------------+--------------------------+
| affinityOrAntiAffinityGroupId   | Identifier                      | 0..N             | Identifier(s)         | support:                 |
|                                 |                                 |                  | of the                | MANDATORY                |
|                                 |                                 |                  | affinity or           |                          |
|                                 |                                 |                  | anti-affinity         |                          |
|                                 |                                 |                  | group(s) the          |                          |
|                                 |                                 |                  | VnfVirtualLinkDesc    |                          |
|                                 |                                 |                  | belongs to.           |                          |
|                                 |                                 |                  |                       |                          |
|                                 |                                 |                  | NOTE: Each            |                          |
|                                 |                                 |                  | identifier            |                          |
|                                 |                                 |                  | references            |                          |
|                                 |                                 |                  | an affinity           |                          |
|                                 |                                 |                  | or                    |                          |
|                                 |                                 |                  | anti-affinity         |                          |
|                                 |                                 |                  | group which           |                          |
|                                 |                                 |                  | expresses             |                          |
|                                 |                                 |                  | affinity or           |                          |
|                                 |                                 |                  | anti-affinity         |                          |
|                                 |                                 |                  | relationship          |                          |
|                                 |                                 |                  | between the           |                          |
|                                 |                                 |                  | VL(s) using           |                          |
|                                 |                                 |                  | this                  |                          |
|                                 |                                 |                  | VnfVirtualLinkDesc    |                          |
|                                 |                                 |                  | and the               |                          |
|                                 |                                 |                  | VL(s) using           |                          |
|                                 |                                 |                  | other                 |                          |
|                                 |                                 |                  | VnfVirtualLinkDesc(s) |                          |
|                                 |                                 |                  | in the same group.    |                          |
+---------------------------------+---------------------------------+------------------+-----------------------+--------------------------+
| maxBitRateRequirements          | LinkBitrateRequirements         | 1                | Specifies             | support:                 |
|                                 |                                 |                  | the maximum           | MANDATORY                |
|                                 |                                 |                  | bitrate               |                          |
|                                 |                                 |                  | requirements          |                          |
|                                 |                                 |                  | for a VL              |                          |
|                                 |                                 |                  | instantiated          |                          |
|                                 |                                 |                  | according             |                          |
|                                 |                                 |                  | to this               |                          |
|                                 |                                 |                  | profile.              |                          |
|                                 |                                 |                  |                       |                          |
|                                 |                                 |                  | NOTE: These           |                          |
|                                 |                                 |                  | attributes            |                          |
|                                 |                                 |                  | are used to           |                          |
|                                 |                                 |                  | control               |                          |
|                                 |                                 |                  | scaling               |                          |
|                                 |                                 |                  | boundaries.           |                          |
+---------------------------------+---------------------------------+------------------+-----------------------+--------------------------+
| minBitRateRequirements          | LinkBitrateRequirements         | 1                | Specifies             | support:                 |
|                                 |                                 |                  | the minimum           | MANDATORY                |
|                                 |                                 |                  | bitrate               |                          |
|                                 |                                 |                  | requirements          |                          |
|                                 |                                 |                  | for a VL              |                          |
|                                 |                                 |                  | instantiated          |                          |
|                                 |                                 |                  | according             |                          |
|                                 |                                 |                  | to this               |                          |
|                                 |                                 |                  | profile.              |                          |
+---------------------------------+---------------------------------+------------------+-----------------------+--------------------------+
| initiationParameters            | KeyValuePair                    | 0..N             | Specifies             | support:                 |
|                                 |                                 |                  | initiation            | MANDATORY                |
|                                 |                                 |                  | parameters            |                          |
|                                 |                                 |                  | for the               | valueRange:              |
|                                 |                                 |                  | virtual               |  specified               |
|                                 |                                 |                  | link.                 | values                   |
|                                 |                                 |                  |                       | include:                 |
|                                 |                                 |                  |                       | cidr,                    |
|                                 |                                 |                  |                       | allocationPools          |
|                                 |                                 |                  |                       | (represented             |
|                                 |                                 |                  |                       | by                       |
|                                 |                                 |                  |                       | [starting                |
|                                 |                                 |                  |                       | ip address,              |
|                                 |                                 |                  |                       | ending ip                |
|                                 |                                 |                  |                       | address]),               |
|                                 |                                 |                  |                       | gatewayIp,               |
|                                 |                                 |                  |                       | networkName,             |
|                                 |                                 |                  |                       | segmentationId,          |
|                                 |                                 |                  |                       | physicalNetwork.         |
+---------------------------------+---------------------------------+------------------+-----------------------+--------------------------+
| networkType                     | Enum                            | 0..1             | Type of the           | support:                 |
|                                 |                                 |                  | network.              | MANDATORY                |
|                                 |                                 |                  |                       |                          |
|                                 |                                 |                  |                       | valueRange:              |
|                                 |                                 |                  |                       | "VLAN",                  |
|                                 |                                 |                  |                       | "VXLAN"                  |
+---------------------------------+---------------------------------+------------------+-----------------------+--------------------------+
| dhcpEnabled                     | Boolean                         | 0..1             | Indicating            | support:                 |
|                                 |                                 |                  | whether               | MANDATORY                |
|                                 |                                 |                  | DHCP is               |                          |
|                                 |                                 |                  | enabled.              |                          |
|                                 |                                 |                  | Default is            |                          |
|                                 |                                 |                  | "FALSE" if            |                          |
|                                 |                                 |                  | not                   |                          |
|                                 |                                 |                  | specified             |                          |
|                                 |                                 |                  | otherwise.            |                          |
+---------------------------------+---------------------------------+------------------+-----------------------+--------------------------+
| vlanTransparent                 | Boolean                         | 0..1             | Indicating            | support:                 |
|                                 |                                 |                  | whether               | MANDATORY                |
|                                 |                                 |                  | "VLAN                 |                          |
|                                 |                                 |                  | Transparent           |                          |
|                                 |                                 |                  | Mode" is              |                          |
|                                 |                                 |                  | supported.            |                          |
|                                 |                                 |                  | Default is            |                          |
|                                 |                                 |                  | "FALSE" if            |                          |
|                                 |                                 |                  | not                   |                          |
|                                 |                                 |                  | specified             |                          |
|                                 |                                 |                  | otherwise.            |                          |
+---------------------------------+---------------------------------+------------------+-----------------------+--------------------------+
