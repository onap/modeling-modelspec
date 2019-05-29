.. Copyright 2019 (China Mobile)
.. This file is licensed under the CREATIVE COMMONS ATTRIBUTION 4.0 INTERNATIONAL LICENSE
.. Full license text at https://creativecommons.org/licenses/by/4.0/legalcode

Group Types
===================

| **tosca.groups.nfv.PlacementGroup:**
|     derived_from: tosca.groups.Root
|     description: PlacementGroup is used for describing the affinity or anti-affinity relationship applicable between the virtualization containers to be created based on different VDUs, or between internal VLs to be created based on different VnfVirtualLinkDesc(s)
|     properties:
|       description:
|         type: string
|         description: Human readable description of the group
|         required: true
|     members: [ tosca.nodes.nfv.Vdu.Compute, tosca.nodes.nfv.VnfVirtualLink ]

