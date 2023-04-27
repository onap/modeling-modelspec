.. Copyright 2018 (China Mobile)
.. This file is licensed under the CREATIVE COMMONS ATTRIBUTION 4.0 INTERNATIONAL LICENSE
.. Full license text at https://creativecommons.org/licenses/by/4.0/legalcode

Node Types
==========

| **tosca.nodes.nfv.Vdu.Compute:**
|   derived_from: tosca.nodes.Root
|   properties:
|     #id:
|       # node name
|     name:       # align with the IM, please refer to https://wiki.onap.org/display/DW/Design+Time+Model+Clean+Version#DesignTimeModelCleanVersion-Class:Vdu
|       type: string
|       required: true
|     description:
|       type: string
|       required: true
|     boot_order:
|       type: map # explicit index (boot index) not necessary, contrary to IFA011. In the IM, it shoul be a array of KeyValuePair/NameValuePair
|       entry_schema:
|         type: string
|       required: false 
|     nfvi_constraints:  
|       type: map # Align with IM, it shoul be a array of KeyValuePair/NameValuePair
|       entry_schema:
|         type: string
|       required: false
|     configurable_properties: 
|        type: map   #In the IM, the multipilicity of VnfcConfigurableProperties is 1, not a map.
|        entry_schema:
|           type: tosca.datatypes.nfv.VnfcConfigurableProperties
|        required: true 
|     vdu_profile:          
|        type: tosca.datatypes.nfv.VduProfile
|        required: true
|     inject_files: # Used for vCPE usecase Aligned with ONAP R2 IM. not defined in IFA011 v2.4.1 and SOL001 v0.6.0.
|        type: tosca.datatypes.nfv.injectFile
|        required: false  #Aligned with ONAP R2 IM. it should be false.
|     meta_data: #metadata attached to the VM or container
|        type: map
|        entry_schema:
|          type: string
|        required: false
|     user_data: #cloudinit userdata script support
|       type: string
|       required: false
|   #attributes: NOT DEFINED IN ONAP IM and SOL001
|     #private_address:
|     #  status: deprecated
|     #public_address:
|     #  status: deprecated
|     #networks:
|     #  status: deprecated
|     #ports:
|     #  status: deprecated
|   capabilities:
|     virtual_compute: 
|       type: tosca.capabilities.nfv.VirtualCompute
|     virtual_binding: 
|       type: tosca.capabilities.nfv.VirtualBindable
|       occurrences: [1, UNBOUND]
|     monitoring_parameter:     
|       type: tosca.capabilities.nfv.Metric # this is not a very clear data structure enough to be coded, suggest to be annotated.
|       occurrences: [0,UNBOUND]
|   requirements:
|     - virtual_storage:
|         capability: tosca.capabilities.nfv.VirtualStorage
|         relationship: tosca.relationships.nfv.Vdu.AttachedTo
|         node: tosca.nodes.nfv.VDU.VirtualStorage
|         occurences: [ 0, UNBOUNDED ]
|   artifacts:    
|     - sw_image:
|         file:    
|         type: tosca.artifacts.nfv.SwImage
| 
| 
| **tosca.nodes.nfv.Vdu.VirtualStorage:** 
|   derived_from: tosca.nodes.Root
|   properties:
|     #id:
|       # node name
|     type_of_storage:
|       type: string
|       constraints:
|           - valid_values: [volume, object, root, block]
|       required: true 
|     size_of_storage:
|       type: scalar-unit.size
|       required: true
|     vdu_storage_requirements: 
|       type: map
|       required: false
|     rdma_enabled:
|       type: boolean
|       required: false
|   capabilities:
|     virtual_storage:
|       type: tosca.capabilities.nfv.VirtualStorage
|   artifacts:  
|     - sw_image:
|         file:       
|         type: tosca.artifacts.Deployment.Image
| #interfaces: # not needed for virtualstroage. it doesn't support cloudinit.
| #	cloudinit:
| #       type:tosca.interfaces.nfv.vdu.cloudinit
| 
| 
| **tosca.nodes.nfv.Cp:**
|   derived_from: tosca.nodes.Root 
|     properties:
|     layer_protocol:
|       type:list
|       entry_schema:
|         constraints:
|           - valid_values: [ethernet, mpls, odu2, ipv4, ipv6, pseudo_wire ]
|       required:true
|     role: #Name in ETSI NFV IFA011 v0.7.3 cpRole
|       type:string
|       constraints:
|         - valid_values: [ root, leaf ]
|       required:false
|     description:
|       type: string
|       required: false
|     protocol_data:
|       type: list
|       entry_schema:
|         type: tosca.datatypes.nfv.CpProtocolData
|       required:true
|     trunk_mode:
|       type: boolean
|       required: true
|     allowed_address_data: # Aligned with ONAP R2 Im.not defined in IFA011 v2.4.1 and SOL001 v0.6.0.                        
|       type: tosca.datatypes.nfv.AddressData   # In the IM, it is a array, but here it is not a array. TBD.
|       required: false
| 
| 
| **tosca.nodes.nfv.VduCp:**
|   derived_from: tosca.nodes.nfv.Cp
|   properties:
|     bitrate_requirement:
|       type: integer
|       required:false
|     vnic_name: #  Aligned with ONAP R2 Im.not defined in IFA011 v2.4.1 and SOL001 v0.6.0. 
|       type: string
|       required:false
|     vnic_order: # Aligned with ONAP R2 Im. not defined in IFA011 v2.4.1 and SOL001 v0.6.0. 
|       type: integer
|       required:false
|     vnic_type: # Aligned with ONAP R2 Im. not defined in IFA011 v2.4.1 and SOL001 v0.6.0
|       type: string
| 	  constraints:
|           - valid_values: [normal, macvtap, direct, baremetal, direct-physical, virtio-forwarder]
|       required:false
|     virtual_network_interface_requirements: 
|       type: list
|       entry_schema:
|         type: VirtualNetworkInterfaceRequirements
|       required:false
|    # order:      #there is no this attribute in IM.
|    #   type: integer
|    #   required: false
|    #   constraints:
|    #     - greater_or_equal: 0
|     requirements:
|         - virtual_link:
|           capability: tosca.capabilities.nfv.VirtualLinkable
|           relationship: tosca.relationships.nfv.VirtualLinksTo
|           node: tosca.nodes.nfv.VnfVirtualLink    
|         - virtual_binding:
|           capability: tosca.capabilities.nfv.VirtualBindable
|           relationship: tosca.relationships.nfv.VirtualBindsTo
|           node: tosca.nodes.nfv.Vdu.Compute
| 
| 
| **tosca.nodes.nfv.VnfVirtualLink:**
|   derived_from: tosca.nodes.Root
|   properties:
|     connectivity_type:
|       type: tosca.datatypes.nfv.ConnectivityType
|       required: true
|     description:
|       type: string
|       required: false
|     test_access:
|       type: list
|       entry_schema:
|         type: string
|       required: false
|     vl_profile:
|       type: tosca.datatypes.nfv.VlProfile
|       required: true
|   capabilities:
|     monitoring_parameter:   # this is not a very clear data structure enough to be coded, suggest to be annotated.
|       type: tosca.capabilities.nfv.Metric
|       occurrences: [0,UNBOUND]
|     virtual_linkable:
|       type: tosca.capabilities.nfv.VirtualLinkable
| 
| 
| **tosca.nodes.nfv.VNF:**
|   derived_from: tosca.nodes.Root
|   properties: 
|     descriptor_id: # instead of vnfd_id
|       type: string # GUID
|       required: true
|     descriptor_version: # instead of vnfd_version
|       type: string
|       required: true
|     provider: # instead of vnf_provider
|       type: string
|       required: true
|     product_name: # instead of vnf_product_name
|       type: string
|       required: true
|     software_version: # instead of vnf_software_version
|       type: string
|       required: true
|     product_info_name: # instead of vnf_product_info_name
|       type: string
|       required: false
|     product_info_description: # instead of vnf_product_info_description
|       type: string
|       required: false
|     vnfm_info:
|       type: list
|       entry_schema:
|         type: string
|       required: true
|     localization_languages:
|       type: list
|       entry_schema:
|         type: string
|       required: false
|     default_localization_language:
|       type: string
|       required: false
|     configurable_properties:
|       type: tosca.datatypes.nfv.VnfConfigurableProperties
|       required: false
|     modifiable_attributes:
|       type: tosca.datatypes.nfv.VnfInfoModifiableAttributes
|       required: false  # true in IFA011, but all of members are false. Align with the IM, it is false
|     flavour_id:
|       type: string
|       required: true  
|     flavour_description:
|       type: string
|       required: true  
|   capabilities:
|     # monitoring_parameter:
|       # modelled as ad hoc capabilities in the VNF node template
|   requirements:
|     - virtual_link:
|         capability: tosca.capabilities.nfv.VirtualLinkable
|         relationship: tosca.relationships.nfv.VirtualLinksTo
|         node: tosca.nodes.nfv.VnfVirtualLink
|         occurrences: [ 0, UNBOUNDED ]
|   interfaces:
|     Nfv:
|       type: tosca.interfaces.nfv.vnf.lifecycle.Nfv
| 