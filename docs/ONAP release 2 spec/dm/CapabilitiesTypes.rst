.. Copyright 2018 (ONAP)
.. This file is licensed under the CREATIVE COMMONS ATTRIBUTION 4.0 INTERNATIONAL LICENSE
.. Full license text at https://creativecommons.org/licenses/by/4.0/legalcode

Capabilities Types
==============================================
| **tosca.capabilities.nfv.VirtualBindable:**
|   derived_from: tosca.capabilities.root
 
| **tosca.capabilities.nfv.VirtualCompute:**
|   derived_from: tosca.capabilities.Root
|   properties:
|     logical_node:
|       type: tosca.datatypes.nfv.LogicalNodeData
|       required: false
|     compute_requirements: 
|       type: map
|       required: false
|     requested_additional_capabilities:
|       type: map
|       entry_schema:
|          type: tosca.datatypes.nfv.RequestedAdditionalCapability
|       required: false
|     virtual_memory:
|       type: tosca.datatypes.nfv.VirtualMemory
|       required: true
|     virtual_cpu:
|       type: tosca.datatypes.nfv.VirtualCpu
|       required: true

| **tosca.capabilities.nfv.VirtualLinkable:**
|   derived_from: tosca.capabilities.root

| **tosca.capabilities.nfv.ExtVirtualLinkable:**
|   derived_from: tosca.capabilities.root

| **tosca.capabilities.nfv.VirtualStorage:**
|   derived_from: tosca.capabilities.root
