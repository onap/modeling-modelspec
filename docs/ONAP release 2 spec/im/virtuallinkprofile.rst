.. Copyright 2018 (China Mobile)
.. This file is licensed under the CREATIVE COMMONS ATTRIBUTION 4.0 INTERNATIONAL LICENSE
.. Full license text at https://creativecommons.org/licenses/by/4.0/legalcode

.. contents::
   :depth: 3
..

Class: VirtualLinkProfile
=========================

+--------------------+-------------+------------------+-----------------+--------------------------+
| **Attribute Name** | **Type**    | **Multiplicity** | **Description** | **Applied Stereotypes**  |
+====================+=============+==================+=================+==========================+
| vnfVirtualL        | Identifier  | 1                | Uniquely        | support:                 |
| inkDescId          | (Reference  |                  | identifies      | MANDATORY                |
|                    | to          |                  | a Vnf VLD.      |                          |
|                    | VnfVirtualL |                  |                 |                          |
|                    | inkDesc)    |                  |                 |                          |
+--------------------+-------------+------------------+-----------------+--------------------------+
| flavourId          | Identifier  | 1                | Identifies      | support:                 |
|                    | (Reference  |                  | a flavour       | MANDATORY                |
|                    | to          |                  | within the      |                          |
|                    | VirtualLink |                  | VnfVirtualL     |                          |
|                    | DescFlavour |                  | inkDesc.        |                          |
|                    | )           |                  |                 |                          |
+--------------------+-------------+------------------+-----------------+--------------------------+
| localAffini        | LocalAffini | 0..N             | Specifies       | support:                 |
| tyOrAntiAff        | tyOrAntiAff |                  | affinity or     | MANDATORY                |
| inityRule          | inityRule   |                  | anti-affini     |                          |
|                    |             |                  | ty              |                          |
|                    |             |                  | rules           |                          |
|                    |             |                  | applicable      |                          |
|                    |             |                  | between the     |                          |
|                    |             |                  | VLs based       |                          |
|                    |             |                  | on this         |                          |
|                    |             |                  | VnfVirtualL     |                          |
|                    |             |                  | inkDesc.        |                          |
|                    |             |                  |                 |                          |
|                    |             |                  | When the        |                          |
|                    |             |                  | cardinality     |                          |
|                    |             |                  | is greater      |                          |
|                    |             |                  | than 1,         |                          |
|                    |             |                  | both            |                          |
|                    |             |                  | affinity        |                          |
|                    |             |                  | rule(s) and     |                          |
|                    |             |                  | anti-affini     |                          |
|                    |             |                  | ty              |                          |
|                    |             |                  | rule(s)         |                          |
|                    |             |                  | with            |                          |
|                    |             |                  | different       |                          |
|                    |             |                  | scopes are      |                          |
|                    |             |                  | applicable      |                          |
|                    |             |                  | to the VLs      |                          |
|                    |             |                  | based on        |                          |
|                    |             |                  | this            |                          |
|                    |             |                  | VnfVirtualL     |                          |
|                    |             |                  | inkDesc.        |                          |
+--------------------+-------------+------------------+-----------------+--------------------------+
| affinityOrA        | Identifier  | 0..N             | Identifier(     | support:                 |
| ntiAffinity        |             |                  | s)              | MANDATORY                |
| GroupId            |             |                  | of the          |                          |
|                    |             |                  | affinity or     |                          |
|                    |             |                  | anti-affini     |                          |
|                    |             |                  | ty              |                          |
|                    |             |                  | group(s)        |                          |
|                    |             |                  | the             |                          |
|                    |             |                  | VnfVirtualL     |                          |
|                    |             |                  | inkDesc         |                          |
|                    |             |                  | belongs to.     |                          |
|                    |             |                  |                 |                          |
|                    |             |                  | NOTE: Each      |                          |
|                    |             |                  | identifier      |                          |
|                    |             |                  | references      |                          |
|                    |             |                  | an affinity     |                          |
|                    |             |                  | or              |                          |
|                    |             |                  | anti-affini     |                          |
|                    |             |                  | ty              |                          |
|                    |             |                  | group which     |                          |
|                    |             |                  | expresses       |                          |
|                    |             |                  | affinity or     |                          |
|                    |             |                  | anti-affini     |                          |
|                    |             |                  | ty              |                          |
|                    |             |                  | relationshi     |                          |
|                    |             |                  | p               |                          |
|                    |             |                  | between the     |                          |
|                    |             |                  | VL(s) using     |                          |
|                    |             |                  | this            |                          |
|                    |             |                  | VnfVirtualL     |                          |
|                    |             |                  | inkDesc         |                          |
|                    |             |                  | and the         |                          |
|                    |             |                  | VL(s) using     |                          |
|                    |             |                  | other           |                          |
|                    |             |                  | VnfVirtualL     |                          |
|                    |             |                  | inkDesc(s)      |                          |
|                    |             |                  | in the same     |                          |
|                    |             |                  | group.          |                          |
+--------------------+-------------+------------------+-----------------+--------------------------+
| maxBitRateR        | LinkBitrate | 1                | Specifies       | support:                 |
| equirements        | Requirement |                  | the maximum     | MANDATORY                |
|                    | s           |                  | bitrate         |                          |
|                    |             |                  | requirement     |                          |
|                    |             |                  | s               |                          |
|                    |             |                  | for a VL        |                          |
|                    |             |                  | instantiate     |                          |
|                    |             |                  | d               |                          |
|                    |             |                  | according       |                          |
|                    |             |                  | to this         |                          |
|                    |             |                  | profile.        |                          |
|                    |             |                  |                 |                          |
|                    |             |                  | NOTE: These     |                          |
|                    |             |                  | attributes      |                          |
|                    |             |                  | are used to     |                          |
|                    |             |                  | control         |                          |
|                    |             |                  | scaling         |                          |
|                    |             |                  | boundaries.     |                          |
+--------------------+-------------+------------------+-----------------+--------------------------+
| minBitRateR        | LinkBitrate | 1                | Specifies       | support:                 |
| equirements        | Requirement |                  | the minimum     | MANDATORY                |
|                    | s           |                  | bitrate         |                          |
|                    |             |                  | requirement     |                          |
|                    |             |                  | s               |                          |
|                    |             |                  | for a VL        |                          |
|                    |             |                  | instantiate     |                          |
|                    |             |                  | d               |                          |
|                    |             |                  | according       |                          |
|                    |             |                  | to this         |                          |
|                    |             |                  | profile.        |                          |
+--------------------+-------------+------------------+-----------------+--------------------------+
| initiationP        | KeyValuePai | 0..N             | Specifies       | support:                 |
| arameters          | r/NameValue |                  | initiation      | MANDATORY                |
|                    | Pair        |                  | parameters      |                          |
|                    |             |                  | for the         | valueRange:              |
|                    |             |                  | virtual         |  specified               |
|                    |             |                  | link.           | values                   |
|                    |             |                  |                 | include:                 |
|                    |             |                  |                 | cidr,                    |
|                    |             |                  |                 | allocationP              |
|                    |             |                  |                 | ools                     |
|                    |             |                  |                 | (represente              |
|                    |             |                  |                 | d                        |
|                    |             |                  |                 | by                       |
|                    |             |                  |                 | [starting                |
|                    |             |                  |                 | ip address,              |
|                    |             |                  |                 | ending ip                |
|                    |             |                  |                 | address]),               |
|                    |             |                  |                 | gatewayIp,               |
|                    |             |                  |                 | networkName              |
|                    |             |                  |                 | ,                        |
|                    |             |                  |                 | segmentatio              |
|                    |             |                  |                 | nId,                     |
|                    |             |                  |                 | physicalNet              |
|                    |             |                  |                 | work.                    |
+--------------------+-------------+------------------+-----------------+--------------------------+
| networkType        | Enum        | 0..1             | Type of the     | support:                 |
|                    |             |                  | network.        | MANDATORY                |
|                    |             |                  |                 |                          |
|                    |             |                  |                 | valueRange:              |
|                    |             |                  |                 | "VLAN",                  |
|                    |             |                  |                 | "VXLAN"                  |
+--------------------+-------------+------------------+-----------------+--------------------------+
| dhcpEnabled        | Boolean     | 0..1             | Indicating      | support:                 |
|                    |             |                  | whether         | MANDATORY                |
|                    |             |                  | DHCP is         |                          |
|                    |             |                  | enabled.        |                          |
|                    |             |                  | Default is      |                          |
|                    |             |                  | "FALSE" if      |                          |
|                    |             |                  | not             |                          |
|                    |             |                  | specified       |                          |
|                    |             |                  | otherwise.      |                          |
+--------------------+-------------+------------------+-----------------+--------------------------+
| vlanTranspa        | Boolean     | 0..1             | Indicating      | support:                 |
| rent               |             |                  | whether         | MANDATORY                |
|                    |             |                  | "VLAN           |                          |
|                    |             |                  | Transparent     |                          |
|                    |             |                  | Mode" is        |                          |
|                    |             |                  | supported.      |                          |
|                    |             |                  | Default is      |                          |
|                    |             |                  | "FALSE" if      |                          |
|                    |             |                  | not             |                          |
|                    |             |                  | specified       |                          |
|                    |             |                  | otherwise.      |                          |
+--------------------+-------------+------------------+-----------------+--------------------------+
