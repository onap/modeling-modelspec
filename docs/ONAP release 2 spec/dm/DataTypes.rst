.. Copyright 2018 (ONAP)
.. This file is licensed under the CREATIVE COMMONS ATTRIBUTION 4.0 INTERNATIONAL LICENSE
.. Full license text at https://creativecommons.org/licenses/by/4.0/legalcode

Data Types
==============================================

| **tosca.datatypes.nfv.L2AddressData:**
|   derived_from: tosca.datatypes.Root
|   properties:  
|     mac_address_assignment:
|       type: Boolean
|       required: true
| 
| 
| **tosca.datatypes.nfv.injectFile: #used for vCPE usecase**
|   derived_from: tosca.datatypes.Root
|   properties:  
|     source_path: 
|       type: string
|       required: true
|     dest_path:
|       type:string
| 	  required: true
| 
| 
| **tosca.datatypes.nfv.L3AddressData:**
|   derived_from: tosca.datatypes.Root
|   properties:  
|     ip_address_assignment: 
|       type: Boolean
|       required: true    
|     floating_ip_activated: 
|       type: Boolean
|       required: true
|     ip_address_type:
|       type: string
|       required: false
|       constraints:
|         - valid_values: [ipv4, ipv6]
|     number_of_ip_address:
|       type: integer
|       required: false 
|    fixed_ip_address: #used for vCPE usecase
|       type:list
|       entry_schema:
| 		type:string
| 	  required: false
| 
| 
| **tosca.datatypes.nfv.AddressData:**
|   derived_from: tosca.datatypes.Root
|   properties:  
|     address_type: 
|       type: string
|       required: true
|       constraints:
|         - valid_values: [mac_address, ip_address]     
|     l2_address_data: 
|       type: tosca.datatypes.nfv.L2AddressData # empty in "GS NFV IFA011 V0.7.3"
|       required: false
|     l3_address_data:
|       type: tosca.datatypes.nfv.L3AddressData
|       required: false 
| 
| 
| **tosca.datatypes.nfv.VirtualNetworkInterfaceRequirements:**
|   derived_from: tosca.datatypes.Root
|   properties:  
|     name: 
|       type: string
|       required: false    
|     description: 
|       type: string
|       required: false
|     support_mandatory:
|       type: boolean
|       required: true
|     network_interface_requirements:
|       type: Map 
|       entry_schema:
|         type: string
|       required: true
|     nic_io_requirements:
|       type: tosca.datatypes.nfv.LogicalNodeData
|       required: false
| 
| 
| **tosca.datatypes.nfv.ConnectivityType:**
|   derived_from: tosca.datatypes.Root
|   properties:  
|     layer_protocol: 
|       type: string
|       required: true
|       constraints:
|         - valid_values: [ethernet, mpls, odu2, ipv4, ipv6, pseudo_wire ]   
|     flow_pattern: 
|       type: string
|       required: false
|       constraints: # not defined in IFA011 v2.4.1 and SOL001 v.6.0 
|         - valid_values: [Line, Tree, Mesh]
| 
| 
| **tosca.datatypes.nfv.RequestedAdditionalCapability:**
|   derived_from: tosca.datatypes.Root
|   properties:
|     #name:
|       # key of containing map
|     support_mandatory:
|       type: boolean
|       required: true
|     min_requested_additional_capability_version:
|       type: string
|       required: false
|     preferred_requested_additional_capability_version:
|       type: string
|       required: false
|     requested_additional_capability_name:
|       type: string
|       required: true
|     target_performance_parameters:
|       type: map
|       entry_schema:
|         type: string
|       required: true     
| 
| 
| **tosca.datatypes.nfv.VirtualMemory:**
|     derived_from: tosca.datatypes.Root
|     properties:
|       virtual_mem_size:
|         type: scalar-unit.size # Number
|         required: true
|       virtual_mem_oversubscription_policy:
|         type: string
|         required: false
|       vdu_memory_requirements:
|         type: map
|         entry_schema:
|           type: string
|         required: false
|       numa_enabled:
|         type: boolean
|         required: false
| 
| 
| **tosca.datatypes.nfv.VirtualCpu:**
|   derived_from: tosca.datatypes.Root
|   properties:
|     cpu_architecture:
|       type: string
|       required: false
|     num_virtual_cpu:
|       type: integer
|       required: true
|     virtual_cpu_clock:
|       type: scalar-unit.frequency
|       required: false
|     virtual_cpu_oversubscription_policy:
|       type: string
|       required: false
|     vdu_cpu_requirements:
|       type: map
|       entry_schema:
|         type: string
|       required: false
|     virtual_cpu_pinning:
|       type: tosca.datatypes.nfv.VirtualCpuPinning
|       required: false
| 
| 
| **tosca.datatypes.nfv.VirtualCpuPinning:**
|   derived_from: tosca.datatypes.Root
|   properties:
|     cpu_pinning_policy:
|       type: string # CpuPinningPolicy
|       constraints:
|         - valid_values: [ static, dynamic ]
|       required: false
|     cpu_pinning_map:
|       type: map
|       entry_schema:
|         type: string
|       required: false
| 
| 
| **tosca.datatypes.nfv.VnfcConfigurableProperties:**
|   derived_from: tosca.datatypes.Root
|   properties:
|     additional_vnfc_configurable_properties:
|       type: map
|       entry_schema:
|         type: string
|       required: false
| 
| 
| **tosca.datatypes.nfv.VduProfile:**
|     derived_from: tosca.datatypes.Root
|     properties:
|       min_number_of_instances:
|         type: integer
|         required: true
|       max_number_of_instances:
|         type: integer
|         required: true
|       #localAffinityOrAntiAffinityRule:  # not defined in SOL001 v.6.0 
|       #  type: tosca.datatypes.nfv.LocalAffinityOrAntiAffinityRule
|       #  required: true
|       #affinityOrAntiAffinityGroupId: # not defined in SOL001 v.6.0 
|       #  type: string
|       #  required: true
|       watchdog: #Align with ONAP R2 IM. not defined in IFA011 v2.4.1 and SOL001 v.6.0 
|         type: string
|         required: true
|       vmBootUpTimeOut: #Align with ONAP R2 IM. not defined in IFA011 v2.4.1 and SOL001 v.6.0
|         type: integer
|         required: optional
| 
| 
| **tosca.datatypes.nfv.VlProfile:**
|     derived_from: tosca.datatypes.Root
|     properties:
|       max_bit_rate_requirements:
|          type: tosca.datatypes.nfv.LinkBitRateRequirements
|          required: true
|       min_bit_rate_requirements:
|          type: tosca.datatypes.nfv.LinkBitRateRequirements
|          required: true
|       qos:
|          type: tosca.datatypes.nfv.Qos
|          required: false
|       initiationParameters: #Align with ONAP R2 IM. not defined in IFA011 v2.4.1 and SOL001 v.6.0 
|          type: map
|          entry_schema:
|            type: string
|          required: false 
|       cidr: #Align with ONAP R2 IM. not defined in IFA011 v2.4.1 and SOL001 v.6.0
|          type: String
|          required: false
|       networkName:  #Align with ONAP R2 IM. not defined in IFA011 v2.4.1 and SOL001 v.6.0
|          type: String
|          required: false
|       startIp:  #Align with ONAP R2 IM. not defined in IFA011 v2.4.1 and SOL001 v.6.0
|          type: String
|          required: false
|       endIp:  #Align with ONAP R2 IM. not defined in IFA011 v2.4.1 and SOL001 v.6.0
|          type: String
|          required: false
|       gatewayIp:  #Align with ONAP R2 IM. not defined in IFA011 v2.4.1 and SOL001 v.6.0
|          type: String
|          required: false
|       segmentationId:  #Align with ONAP R2 IM. not defined in IFA011 v2.4.1 and SOL001 v.6.0
|          type: Integer
|          required: false
|       physicalNetwork:  #Align with ONAP R2 IM. not defined in IFA011 v2.4.1 and SOL001 v.6.0
|          type: String
|          required: false
|       networkType:  #Align with ONAP R2 IM. not defined in IFA011 v2.4.1 and SOL001 v.6.0
|          type: String
|          required: false
|          constraints:
|            - valid_values: [VLAN, VXLAN]
|       dhcpEnabled:  # not defined in IFA011 v2.4.1 and SOL001 v.6.0
|          type: Boolean
|          required: false
|       vlanTransparent:  #Align with ONAP R2 IM. not defined in IFA011 v2.4.1 and SOL001 v.6.0
|          type: Boolean
|          required: false
| 
| 
| **tosca.datatypes.nfv.InstantiationLevel:**
|     derived_from: tosca.datatypes.Root
|     properties:
|       description:
|         type: string
|         required: true
|       vdu_levels:
|         type: map # key: vduId
|         required: true
|         entry_schema:
|           type: tosca.datatypes.nfv.VduLevel
|       scale_info:
|         type: map # key: aspectId
|         required: false
|         entry_schema:
|           type: tosca.datatypes.nfv.ScaleInfo
| 
| 
| **tosca.datatypes.nfv.VduLevel:**
|     derived_from: tosca.datatypes.Root
|     properties:
|       number_of_instances:
|         type: integer
|         required: true

| **tosca.datatypes.nfv.VnfLcmOperationsConfiguration:**
|     derived_from: tosca.datatypes.Root 
|     properties: 
|       instantiate: 
|         type: tosca.datatypes.nfv.VnfInstantiateOperationConfiguration 
|       scale:  
|         type: tosca.datatypes.nfv.VnfScaleOperationConfiguration 
|       scale_to_level: 
|         type: tosca.datatypes.nfv.VnfScaleToLevelOperationConfiguration 
|       heal: 
|         type: tosca.datatypes.nfv.VnfHealOperationConfiguratin 
|       terminate: 
|         type: tosca.datatypes.nfv.VnfTerminateOperationConfiguration 
|       operate: 
|         type: tosca.datatypes.nfv.VnfOperateOperationConfiguration
| 
| 
| **tosca.datatypes.nfv.VnfInstantiateOperationConfiguration:**
|     derived_from: tosca.datatypes.Root
|     properties:
|       #parameters:
|           #modeled as part of operation parameter list
| 
| 
| **tosca.datatypes.nfv.VnfScaleOperationConfiguration:**
|     derived_from: tosca.datatypes.Root
|     properties: 
|       #parameters:
|          #modeled as part of the operation parameter list
|       scaling_by_more_than_one_step_supported:
|          type: boolean
| 
| 
| **tosca.datatypes.nfv.VnfScaleToLevelOperationConfiguration:**
|     derived_from: tosca.datatypes.Root
|     properties: 
|       #parameters:
|          #modeled as part of the operation parameter list
|       arbitrary_target_levels_supported:
|          type: boolean
| 
| 
| **tosca.datatypes.nfv.VnfHealOperationConfiguration**
|     derived_from: tosca.datatypes.Root
|     properties: 
|       #parameters:
|          #modeled as part of the operation parameter list
|       causes:
|          type: list
|          entry_schema:
|            type: string
| 
| 
| **tosca.datatypes.nfv.VnfTerminateOperationConfiguration**
|     derived_from: tosca.datatypes.Root
|     properties: 
|       min_graceful_termination_timeout:
|          type: integer
|       max_recommended_graceful_termination_timeout:
|          type: integer 
| 
| 
| 
| **tosca.datatypes.nfv.VnfOperateOperationConfiguration**
|   derived_from: tosca.datatypes.Root
|   properties:
|     min_graceful_termination_timeout:
|          type: integer
|     max_recommended_graceful_termination_timeout:
|          type: integer      
| 
| 
| **tosca.datatypes.nfv.ScaleInfo**
|   derived_from: tosca.datatypes.Root
|   properties:
|     scaleLevel:
|          type: integer
|          required: true
| 
| 
| **tosca.datatypes.nfv.ScaleAspect:**
|   derived_from: tosca.datatypes.Root
|   properties:
|     name:
|        type: string
|        required: true
|     description:
|        type: string
|        required: true
|     associated_group:
|        type: string #Identifier
|        required: false
|     max_scale_level:
|        type: integer #PositiveInteger
|        required: true
| 
| 
| **tosca.datatypes.nfv.LinkBitRateRequirements:**
|   derived_from: tosca.datatypes.Root
|   properties:
|     root:
|        type: integer
|        required: true
|     leaf:
|        type: integer
|        required: true
| 
| 
|   **tosca.datatypes.nfv.Qos:**
|     derived_from: tosca.datatypes.Root
|     properties:
|       latency:
|          type: integer #Number [ms]
|          required: true
|       packet_delay_variation:
|          type: integer #Number [ms]
|          required: true
|       packet_loss_ratio:
|          type: Scalar #Number [0 ..1]
|          required: false
| 
| 
|   **tosca.datatypes.nfv.CpProtocolData:**
|     derived_from: tosca.datatypes.Root
|     properties:
|       asscociated_layer_protocol:
|         type: string
|         constraints:
|           - valid_values: [ethernet, mpls, odu2, ipv4, ipv6, pseudo-wire ]
|         required: true
|       address_data:
|         type: tosca.datatypes.nfv.AddressData
|         required: false
| 
| 
| **tosca.datatypes.nfv.VnfConfigurableProperties:**
|     derived_from: tosca.datatypes.Root
|     properties:
|       is_autoscale_enabled:
|         type: boolean
|         required: false
|       is_autoheal_enabled:
|         type: boolean
|         required: false
|       additional_configurable_properties:
|         type: tosca.datatypes.nfv.VnfAdditionalConfigurableProperties
|         required: false

| **tosca.datatypes.nfv.VnfAdditionalConfigurableProperties:** 
|     derived_from: tosca.datatypes.Root
| 
| 
| **tosca.datatypes.nfv.VnfInfoModifiableAttributes:**
|     derived_from: tosca.datatypes.Root
|     properties:
|       extensions:
|         type: tosca.datatypes.nfv.VnfInfoModifiableAttributesExtensions
|         required: false
|       metadata:
|         type: tosca.datatypes.nfv.VnfInfoModifiableAttributesMetadata
|         required: false
| 
| 
|   **tosca.datatypes.nfv.VnfInfoModifiableAttributesExtensions:**
|     derived_from: tosca.datatypes.Root
| 
| 
|   **tosca.datatypes.nfv.VnfInfoModifiableAttributesMetadata:**
|     derived_from: tosca.datatypes.Root
| 
| 
|   **tosca.datatypes.nfv.LogicalNodeData:**
|     derived_from: tosca.datatypes.Root
|     properties:
|       logical_node_requirements:
|         type: map # not defined in SOL001 v.6.0
|         entry_schema:
|           type: string
|         required: false
