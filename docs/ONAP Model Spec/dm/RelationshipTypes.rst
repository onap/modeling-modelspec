.. Copyright 2019 (China Mobile)
.. This file is licensed under the CREATIVE COMMONS ATTRIBUTION 4.0 INTERNATIONAL LICENSE
.. Full license text at https://creativecommons.org/licenses/by/4.0/legalcode

Relationships Types
===================

| **tosca.relationships.nfv.VirtualBindsTo:**
|     derived_from: tosca.relationships.DependsOn
|     description: Represents an association relationship between Vdu.Compute and VduCp node types 
|     valid_target_types: [ tosca.capabilities.nfv.VirtualBindable]
| 
| 
| **tosca.relationships.nfv.VirtualLinksTo:**
|     derived_from: tosca.relationships.DependsOn
|     description: Represents an association relationship between the VduCp and VnfVirtualLink node types 
|     valid_target_types: [ tosca.capabilities.nfv.VirtualLinkable]
|
|
| **tosca.relationships.nfv.AttachesTo:**
|     derived_from: tosca.relationships.Root
|     description: Represents an association relationship between the Vdu.Compute and one of the node types, Vdu.VirtualBlockStorage, Vdu.VirtualObjectStorage or Vdu.VirtualFileStorage
|     valid_target_types: [ tosca.capabilities.nfv.VirtualStorage ]

