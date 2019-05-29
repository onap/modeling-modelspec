.. Copyright 2019 (China Mobile)
.. This file is licensed under the CREATIVE COMMONS ATTRIBUTION 4.0 INTERNATIONAL LICENSE
.. Full license text at https://creativecommons.org/licenses/by/4.0/legalcode

Capabilities Types
==================

| **tosca.capabilities.nfv.VirtualBindable:**
|   derived_from: tosca.capabilities.Node
|   description: Indicates that the node that includes it can be pointed by a tosca.relationships.nfv.VirtualBindsTo relationship type which is used to model the VduHasCpd association
 
| **tosca.capabilities.nfv.VirtualCompute:**
|   derived_from: tosca.capabilities.Node
|   description: Describes the capabilities related to virtual compute resources 
|   properties:
|     logical_node:
|       type: map
|       description: Describes the Logical Node requirements 
|       required: false
|       entry_schema:
|          type: tosca.datatypes.nfv.LogicalNodeData 
|     requested_additional_capabilities:
|       type: map
|       description: Describes additional capability for a particular VDU 
|       entry_schema:
|          type: tosca.datatypes.nfv.RequestedAdditionalCapability
|       required: false
|     compute_requirements:
|       type: map 
|       required: false 
|       entry_schema: 
|         type: string 
|     virtual_memory:
|       type: tosca.datatypes.nfv.VirtualMemory
|       description: Describes virtual CPU(s) of the virtualized compute 
|       required: true
|     virtual_cpu:
|       type: tosca.datatypes.nfv.VirtualCpu
|       description: Describes virtual CPU(s) of the virtualized compute 
|       required: true
|     virtual_local_storage:
|       type: list
|       description: A list of virtual system disks created and destroyed as part of the VM lifecycle
|       required: false
|       entry_schema:
|         type: tosca.datatypes.nfv.VirtualBlockStorageData 
|         description: virtual system disk definition      

| **tosca.capabilities.nfv.VirtualLinkable:**
|   derived_from: tosca.capabilities.root
|   description: A node type that includes the VirtualLinkable capability indicates that it can be pointed by by tosca.relationships.nfv.VirtualLinksTo relationship type

| **tosca.capabilities.nfv.VirtualStorage:**
|   derived_from: tosca.capabilities.root
|   description: Describes the attachment capabilities related to Vdu.Storage
