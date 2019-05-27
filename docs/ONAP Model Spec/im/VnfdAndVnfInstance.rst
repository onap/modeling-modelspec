Vnfd and VNF instance model
===========================

Classes
-------

BaseConfigGroup
~~~~~~~~~~~~~~~

Every Vnf contains a BaseConfigGroup. BaseConfigGroup may set Access Control Lists (ACL's) and establish security groups and server groups. BaseConfigGroup reates/establishs storage for the VM's (OpenStack Cinder). BaseConfigGroup may establish internal networks such as OAM (VNF Mgmt) or MNS (Maintenance & Surveillance) established. A very simple VNF may only have a BaseConfig VnfElementGroup.

**Parent class:** VnfdElementGroup

Applied stereotypes:

-  Experimental

-  OpenModelClass

-  **support: MANDATORY**

DeploymentGroup
~~~~~~~~~~~~~~~

DeploymentGroup provides the minimum viable VDU and associated VNFC configuration for a useable VNF. I can have a small, medium, large deployment configuration.

**Parent class:** VnfdElementGroup

Applied stereotypes:

-  Experimental

-  OpenModelClass

-  **support: MANDATORY**

HomingGroup
~~~~~~~~~~~

Homing selects what cloud selection strategy will be used. HomingGroup is used to determine where VNF's within a given group are placed with respect to a service component. Homing strategy is as follows: Colocation - members of the group share the same cloud region (VIM Domain) isolation - members of the group do not share the same cloud region.

**Parent class:** VnfdElementGroup

Applied stereotypes:

-  Experimental

-  OpenModelClass

-  **support: MANDATORY**

==================== ============== ========= ================================== ===========================================================================================================================================================================================================================================================
**Attribute Name**   **Type**       **Mult.** **Stereotypes**                    **Description**
==================== ============== ========= ================================== ===========================================================================================================================================================================================================================================================
homingStrategy       HomingStrategy 1         OpenModelAttribute                 The homing strategy can be one of the following: Exclusivity - Resources within the cloud region are exclusive to the group Inclusively - Resources are co-located in the same cloud-region. Diversity - Resources are geo-diverse ( cannot be co-located).
                                                                                
                                              -  isInvariant: false             
                                                                                
                                              -  valueRange: no range constraint
                                                                                
                                              -  support: MANDATORY             
vnfdMembers          invalid        1         OpenModelAttribute                
                                                                                
                                              -  isInvariant: false             
                                                                                
                                              -  valueRange: no range constraint
                                                                                
                                              -  support: MANDATORY             
vnfdElementGroupId   Identifier     1         Preliminary                        Unique identifier of this group in the VNFD.
                                                                                
                                              OpenModelAttribute                
                                                                                
                                              -  isInvariant: false             
                                                                                
                                              -  valueRange: no range constraint
                                                                                
                                              -  support: MANDATORY             
description          String         1         Preliminary                        Human readable description of the group.
                                                                                
                                              OpenModelAttribute                
                                                                                
                                              -  isInvariant: false             
                                                                                
                                              -  valueRange: no range constraint
                                                                                
                                              -  support: MANDATORY             
\_vdu                Vdu            0..\*     Preliminary                        References to Vdus that are part of this group.
                                                                                
                                              OpenModelAttribute                
                                                                                
                                              -  isInvariant: false             
                                                                                
                                              -  valueRange: no range constraint
                                                                                
                                              -  support: MANDATORY             
\_vnfVirtualLinkdesc                0..\*     Preliminary                        References to VnfVirtualLinkDesc that are part of this group.
                                                                                
                                              OpenModelAttribute                
                                                                                
                                              -  isInvariant: false             
                                                                                
                                              -  valueRange: no range constraint
                                                                                
                                              -  support: MANDATORY             
==================== ============== ========= ================================== ===========================================================================================================================================================================================================================================================

InstantiationLevel
~~~~~~~~~~~~~~~~~~

The InstantiationLevel class describes a given level of resources to be instantiated within a DF in term of the number of VNFC instances to be created from each VDU. All the VDUs referenced in the level shall be part of the corresponding DF and their number shall be within the range (min/max) for this DF.

Applied stereotypes:

-  Reference

-  **reference: IFA011 v2.5.1**

-  Preliminary

-  OpenModelClass

-  **support: MANDATORY**

======================= ======================= ========= ================================== ==============================================================================================================================================================================================================================================================================================================================================================================================================================
**Attribute Name**      **Type**                **Mult.** **Stereotypes**                    **Description**
======================= ======================= ========= ================================== ==============================================================================================================================================================================================================================================================================================================================================================================================================================
levelId                 Identifier              1         Preliminary                        Uniquely identifies a level with the DF.
                                                                                            
                                                          OpenModelAttribute                
                                                                                            
                                                          -  isInvariant: true              
                                                                                            
                                                          -  valueRange: no range constraint
                                                                                            
                                                          -  support: MANDATORY             
description             String                  1         Preliminary                        Human readable description of the level.
                                                                                            
                                                          OpenModelAttribute                
                                                                                            
                                                          -  isInvariant: false             
                                                                                            
                                                          -  valueRange: no range constraint
                                                                                            
                                                          -  support: MANDATORY             
scaleInfo               ScaleInfo               0..\*     Preliminary                        Represents for each aspect the scale level that corresponds to this instantiation level. scaleInfo shall be present if the VNF supports scaling.
                                                                                            
                                                          OpenModelAttribute                
                                                                                            
                                                          -  isInvariant: false             
                                                                                            
                                                          -  valueRange: no range constraint
                                                                                            
                                                          -  support: MANDATORY             
\_vduLevel              VduLevel                1..\*     Preliminary                        Indicates the number of instance of this VDU to deploy for this level.
                                                                                            
                                                          OpenModelAttribute                
                                                                                            
                                                          -  isInvariant: false             
                                                                                            
                                                          -  valueRange: no range constraint
                                                                                            
                                                          -  support: MANDATORY             
virtualLinkBitRateLevel VirtualLinkBitRateLevel 0..\*     Preliminary                        Specifies bitrate requirements applicable to virtual links created from particular virtual link descriptors for this level. NOTE: If not present, it is assumed that the bitrate requirements can be derived from those specified in the VduCpd instances applicable to the internal VL. If present in both the InstantiationLevel and the VduCpd instances applicable to the internal VL, the highest value takes precedence.
                                                                                            
                                                          OpenModelAttribute                
                                                                                            
                                                          -  isInvariant: false             
                                                                                            
                                                          -  valueRange: no range constraint
                                                                                            
                                                          -  support: MANDATORY             
======================= ======================= ========= ================================== ==============================================================================================================================================================================================================================================================================================================================================================================================================================

LogicalNodeRequirements
~~~~~~~~~~~~~~~~~~~~~~~

This information element describes compute, memory and I/O requirements that are to be associated with the logical node of infrastructure. The logical node requirements are a sub-component of the VDU level requirements. As an example for illustration purposes, a logical node correlates to the concept of a NUMA cell in libvirt terminology.

Applied stereotypes:

-  Reference

-  **reference: IFA011 v2.5.1**

-  Preliminary

-  OpenModelClass

-  **support: MANDATORY**

============================ ============ ========= ================================== =================================================================================================================================================================================================================================================================================================================================================================================================================
**Attribute Name**           **Type**     **Mult.** **Stereotypes**                    **Description**
============================ ============ ========= ================================== =================================================================================================================================================================================================================================================================================================================================================================================================================
id                           Identifier   1         Preliminary                        Identifies this set of logical node requirements.
                                                                                      
                                                    OpenModelAttribute                
                                                                                      
                                                    -  isInvariant: true              
                                                                                      
                                                    -  valueRange: no range constraint
                                                                                      
                                                    -  support: MANDATORY             
logicalNodeRequirementDetail KeyValuePair 1..\*     Preliminary                        The logical node-level compute, memory and I/O requirements. An array of key-value pairs that articulate the deployment requirements. This could include the number of CPU cores on this logical node, a memory configuration specific to a logical node (e.g. such as available in the Linux kernel via the libnuma library) or a requirement related to the association of an I/O device with the logical node.
                                                                                      
                                                    OpenModelAttribute                
                                                                                      
                                                    -  isInvariant: false             
                                                                                      
                                                    -  valueRange: no range constraint
                                                                                      
                                                    -  support: MANDATORY             
============================ ============ ========= ================================== =================================================================================================================================================================================================================================================================================================================================================================================================================

NetworkFunctionType
~~~~~~~~~~~~~~~~~~~

Applied stereotypes:

-  OpenModelClass

-  **support: MANDATORY**

================== ======== ========= ================================== ===============
**Attribute Name** **Type** **Mult.** **Stereotypes**                    **Description**
================== ======== ========= ================================== ===============
type               String   1         OpenModelAttribute                
                                                                        
                                      -  isInvariant: false             
                                                                        
                                      -  valueRange: no range constraint
                                                                        
                                      -  support: MANDATORY             
================== ======== ========= ================================== ===============

PlacementGroup
~~~~~~~~~~~~~~

**Parent class:** VnfdElementGroup

Applied stereotypes:

-  Experimental

-  OpenModelClass

-  **support: MANDATORY**

==================== ================= ========= ================================== =============================================================
**Attribute Name**   **Type**          **Mult.** **Stereotypes**                    **Description**
==================== ================= ========= ================================== =============================================================
placementStrategy    PlacementStrategy 1         OpenModelAttribute                
                                                                                   
                                                 -  isInvariant: false             
                                                                                   
                                                 -  valueRange: no range constraint
                                                                                   
                                                 -  support: MANDATORY             
                                                                                   
                                                 Future                            
strategScope         invalid           1         OpenModelAttribute                
                                                                                   
                                                 -  isInvariant: false             
                                                                                   
                                                 -  valueRange: no range constraint
                                                                                   
                                                 -  support: MANDATORY             
                                                                                   
                                                 Future                            
vnfdElementGroupId   Identifier        1         Preliminary                        Unique identifier of this group in the VNFD.
                                                                                   
                                                 OpenModelAttribute                
                                                                                   
                                                 -  isInvariant: false             
                                                                                   
                                                 -  valueRange: no range constraint
                                                                                   
                                                 -  support: MANDATORY             
description          String            1         Preliminary                        Human readable description of the group.
                                                                                   
                                                 OpenModelAttribute                
                                                                                   
                                                 -  isInvariant: false             
                                                                                   
                                                 -  valueRange: no range constraint
                                                                                   
                                                 -  support: MANDATORY             
\_vdu                Vdu               0..\*     Preliminary                        References to Vdus that are part of this group.
                                                                                   
                                                 OpenModelAttribute                
                                                                                   
                                                 -  isInvariant: false             
                                                                                   
                                                 -  valueRange: no range constraint
                                                                                   
                                                 -  support: MANDATORY             
\_vnfVirtualLinkdesc                   0..\*     Preliminary                        References to VnfVirtualLinkDesc that are part of this group.
                                                                                   
                                                 OpenModelAttribute                
                                                                                   
                                                 -  isInvariant: false             
                                                                                   
                                                 -  valueRange: no range constraint
                                                                                   
                                                 -  support: MANDATORY             
==================== ================= ========= ================================== =============================================================

PnfInstance
~~~~~~~~~~~

**Parent class:** NetworkFunction

Applied stereotypes:

-  OpenModelClass

-  **support: MANDATORY**

Pnfd
~~~~

**Parent class:** NetworkFunctionDesc

Applied stereotypes:

-  OpenModelClass

-  **support: MANDATORY**

ScalingAspect
~~~~~~~~~~~~~

The ScalingAspect class describes the details of an aspect used for horizontal scaling.

Applied stereotypes:

-  Reference

-  **reference: IFA011 v2.5.1**

-  Experimental

-  OpenModelClass

-  **support: MANDATORY**

================== ======== ========= ================================== =============================================
**Attribute Name** **Type** **Mult.** **Stereotypes**                    **Description**
================== ======== ========= ================================== =============================================
id                 String   1         Experimental                       Unique identifier of this aspect in the VNFD.
                                                                        
                                      OpenModelAttribute                
                                                                        
                                      -  isInvariant: true              
                                                                        
                                      -  valueRange: no range constraint
                                                                        
                                      -  support: MANDATORY             
name               String   1         Experimental                       Human readable name of the aspect.
                                                                        
                                      OpenModelAttribute                
                                                                        
                                      -  isInvariant: false             
                                                                        
                                      -  valueRange: no range constraint
                                                                        
                                      -  support: MANDATORY             
description        String   1         Experimental                       Human readable description of the aspect.
                                                                        
                                      OpenModelAttribute                
                                                                        
                                      -  isInvariant: false             
                                                                        
                                      -  valueRange: no range constraint
                                                                        
                                      -  support: MANDATORY             
================== ======== ========= ================================== =============================================

ScalingGroup
~~~~~~~~~~~~

A ScalingGroup determines which VNFC's (VDU's) are scaled together based on demand.

**Parent class:** VnfdElementGroup

Applied stereotypes:

-  Reference

-  **reference: IFA011 v2.5.1**

-  Experimental

-  OpenModelClass

-  **support: MANDATORY**

SecurityGroupRule
~~~~~~~~~~~~~~~~~

Security group rule specifies the matching criteria for the ingress and/or egress traffic to/from the visited connection points. If an ingress traffic is accepted, the corresponding egress response shall be allowed, regardless of the security group rules on the egress direction. If an egress traffic is allowed, the corresponding ingress response shall be accepted, regardless of the security group rules on the ingress direction. The design of security group rule follows a permissive model where all security group rules applied to a CP are dealt with in an "OR" logic fashion, i.e. the traffic is allowed if it matches any security group rule applied to this CP.

Applied stereotypes:

-  Reference

-  **reference: IFA011 V2.5.1**

-  Preliminary

-  OpenModelClass

-  **support: MANDATORY**

=================== ========== ========= ================================== =========================================================================================================================================================================================================================================================================================================================
**Attribute Name**  **Type**   **Mult.** **Stereotypes**                    **Description**
=================== ========== ========= ================================== =========================================================================================================================================================================================================================================================================================================================
securityGroupRuleId Identifier 1         Preliminary                        Identifier of the security group rule.
                                                                           
                                         OpenModelAttribute                
                                                                           
                                         -  isInvariant: true              
                                                                           
                                         -  valueRange: no range constraint
                                                                           
                                         -  support: MANDATORY             
description         String     0..1      Preliminary                        Human readable description of the security group rule
                                                                           
                                         OpenModelAttribute                
                                                                           
                                         -  isInvariant: false             
                                                                           
                                         -  valueRange: no range constraint
                                                                           
                                         -  support: MANDATORY             
direction           Direction  0..1      Preliminary                        The direction in which the security group rule is applied.
                                                                           
                                         OpenModelAttribute                
                                                                           
                                         -  isInvariant: false             
                                                                           
                                         -  valueRange: no range constraint
                                                                           
                                         -  support: MANDATORY             
etherType           IpVersion  0..1      Preliminary                        Indicates the protocol carried over the Ethernet layer.
                                                                           
                                         OpenModelAttribute                
                                                                           
                                         -  isInvariant: false             
                                                                           
                                         -  valueRange: no range constraint
                                                                           
                                         -  support: MANDATORY             
protocol            String     0..1      Preliminary                        Indicates the protocol carried over the IP layer. Permitted values: any protocol defined in the IANA protocol registry, e.g. TCP, UDP, ICMP, etc. See https://www.iana.org/assignments/protocol-numbers/protocol-numbers.xhtml Note: IFA011 defines this as an enum, but as the list is not complete, made this a string.
                                                                           
                                         OpenModelAttribute                
                                                                           
                                         -  isInvariant: false             
                                                                           
                                         -  valueRange: no range constraint
                                                                           
                                         -  support: MANDATORY             
portRangeMin        Integer    0..1      Preliminary                        Indicates minimum port number in the range that is matched by the security group rule. If a value is provided at design-time, this value may be overridden at run-time based on other deployment requirements or constraints.
                                                                           
                                         OpenModelAttribute                
                                                                           
                                         -  isInvariant: false             
                                                                           
                                         -  valueRange: no range constraint
                                                                           
                                         -  support: MANDATORY             
portRangeMax        Integer    0..1      Preliminary                        Indicates maximum port number in the range that is matched by the security group rule. If a value is provided at design-time, this value may be overridden at run-time based on other deployment requirements or constraints.
                                                                           
                                         OpenModelAttribute                
                                                                           
                                         -  isInvariant: false             
                                                                           
                                         -  valueRange: no range constraint
                                                                           
                                         -  support: MANDATORY             
=================== ========== ========= ================================== =========================================================================================================================================================================================================================================================================================================================

ServiceProxy
~~~~~~~~~~~~

Applied stereotypes:

-  OpenModelClass

-  **support: MANDATORY**

SwImage
~~~~~~~

A software image

Applied stereotypes:

-  Reference

-  **reference: IFA011 v2.5.1**

-  Preliminary

-  OpenModelClass

-  **support: MANDATORY**

SwImageDesc
~~~~~~~~~~~

The SwImageDesc information element describes requested additional capability for a particular VDU. Such a capability may be for acceleration or specific tasks. Storage not necessarily related to the compute, may be Network Attached Storage (NAS)

Applied stereotypes:

-  Reference

-  **reference: IFA011 v2.5.1**

-  Preliminary

-  OpenModelClass

-  **support: MANDATORY**

================================== ========== ========= ================================== ==============================================================================================================================================================================================================
**Attribute Name**                 **Type**   **Mult.** **Stereotypes**                    **Description**
================================== ========== ========= ================================== ==============================================================================================================================================================================================================
id                                 Identifier 1         Preliminary                        The identifier of this software image.
                                                                                          
                                                        OpenModelAttribute                
                                                                                          
                                                        -  isInvariant: false             
                                                                                          
                                                        -  valueRange: no range constraint
                                                                                          
                                                        -  support: MANDATORY             
name                               String     1         Preliminary                        The name of this software image.
                                                                                          
                                                        OpenModelAttribute                
                                                                                          
                                                        -  isInvariant: false             
                                                                                          
                                                        -  valueRange: no range constraint
                                                                                          
                                                        -  support: MANDATORY             
version                            Version    1         Preliminary                        The version of this software image.
                                                                                          
                                                        OpenModelAttribute                
                                                                                          
                                                        -  isInvariant: false             
                                                                                          
                                                        -  valueRange: no range constraint
                                                                                          
                                                        -  support: MANDATORY             
checksum                           String     1         Preliminary                        The checksum of the software image file.
                                                                                          
                                                        OpenModelAttribute                
                                                                                          
                                                        -  isInvariant: false             
                                                                                          
                                                        -  valueRange: no range constraint
                                                                                          
                                                        -  support: MANDATORY             
containerFormat                    String     1         Preliminary                        The container format describes the container file format in which software image is provided.
                                                                                          
                                                        OpenModelAttribute                
                                                                                          
                                                        -  isInvariant: false             
                                                                                          
                                                        -  valueRange: no range constraint
                                                                                          
                                                        -  support: MANDATORY             
diskFormat                         String     1         Preliminary                        The disk format of a software image is the format of the underlying disk image.
                                                                                          
                                                        OpenModelAttribute                
                                                                                          
                                                        -  isInvariant: false             
                                                                                          
                                                        -  valueRange: no range constraint
                                                                                          
                                                        -  support: MANDATORY             
minRam                             Number     0..1      Preliminary                        The minimal RAM requirement for this software image. The value of the "size" attribute of VirtualMemoryData of the Vdu referencing this SwImageDesc shall not be smaller than the value of minRam.
                                                                                          
                                                        OpenModelAttribute                
                                                                                          
                                                        -  isInvariant: false             
                                                                                          
                                                        -  valueRange: no range constraint
                                                                                          
                                                        -  support: MANDATORY             
minDisk                            Number     1         Preliminary                        The minimal disk size requirement for this software image. The value of the "size of storage" attribute of the VirtualStorageDesc referencing this SwImageDesc shall not be smaller than the value of minDisk.
                                                                                          
                                                        OpenModelAttribute                
                                                                                          
                                                        -  isInvariant: false             
                                                                                          
                                                        -  valueRange: no range constraint
                                                                                          
                                                        -  support: MANDATORY             
size                               Number     1         Preliminary                        The size of the software image.
                                                                                          
                                                        OpenModelAttribute                
                                                                                          
                                                        -  isInvariant: false             
                                                                                          
                                                        -  valueRange: no range constraint
                                                                                          
                                                        -  support: MANDATORY             
operatingSystem                    String     0..1      Preliminary                        Identifies the operating system used in the software image. This attribute may also identify if a 32 bit or 64 bit software image is used.
                                                                                          
                                                        OpenModelAttribute                
                                                                                          
                                                        -  isInvariant: false             
                                                                                          
                                                        -  valueRange: no range constraint
                                                                                          
                                                        -  support: MANDATORY             
supportedVirtualisationEnvironment String     0..\*     Preliminary                        Identifies the virtualisation environments (e.g. hypervisor) compatible with this software image.
                                                                                          
                                                        OpenModelAttribute                
                                                                                          
                                                        -  isInvariant: false             
                                                                                          
                                                        -  valueRange: no range constraint
                                                                                          
                                                        -  support: MANDATORY             
\_swImage                          SwImage    1         Preliminary                        This is a reference to the actual software image. The reference can be relative to the root of the VNF Package or can be a URL
                                                                                          
                                                        OpenModelAttribute                
                                                                                          
                                                        -  isInvariant: false             
                                                                                          
                                                        -  valueRange: no range constraint
                                                                                          
                                                        -  support: MANDATORY             
                                                                                          
                                                        PassedByReference                 
================================== ========== ========= ================================== ==============================================================================================================================================================================================================

Vdu
~~~

The Virtualisation Deployment Unit (VDU) is a construct supporting the description of the deployment and operational behavior of a VNFC. A VNFC instance created based on the VDU maps to a single virtualisation container (e.g. a VM). A VNFC will only be in one VNFDesc. If a vendor wants to use the VNFC in mupliple VNFDesc (their product) they can do so, but it will be 'repeated'.

Applied stereotypes:

-  Reference

-  **reference: IFA011 v2.5.1**

-  Preliminary

-  OpenModelClass

-  **support: MANDATORY**

====================== ========================== ========= ================================== ===========================================================================================================================================================================================================================================================================================================================================================================================================================================================================================================================================================================================================================================================================================================================================================================================================================================================================================================
**Attribute Name**     **Type**                   **Mult.** **Stereotypes**                    **Description**
====================== ========================== ========= ================================== ===========================================================================================================================================================================================================================================================================================================================================================================================================================================================================================================================================================================================================================================================================================================================================================================================================================================================================================================
id                     Identifier                 1         Preliminary                        Unique identifier of this Vdu in VNFD.
                                                                                              
                                                            OpenModelAttribute                
                                                                                              
                                                            -  isInvariant: true              
                                                                                              
                                                            -  valueRange: no range constraint
                                                                                              
                                                            -  support: MANDATORY             
name                   String                     1         Preliminary                        Human readable name of the Vdu.
                                                                                              
                                                            OpenModelAttribute                
                                                                                              
                                                            -  isInvariant: false             
                                                                                              
                                                            -  valueRange: no range constraint
                                                                                              
                                                            -  support: MANDATORY             
description            String                     1         Preliminary                        Human readable description of the Vdu.
                                                                                              
                                                            OpenModelAttribute                
                                                                                              
                                                            -  isInvariant: false             
                                                                                              
                                                            -  valueRange: no range constraint
                                                                                              
                                                            -  support: MANDATORY             
bootOrder              KeyValuePair               0..\*     Preliminary                        Boot order of valid boot devices. "key/name" indicates the the boot index "value" references a descriptor from which a valid boot device is created e.g. VirtualStorageDesc from which a VirtualStorage instance is created. NOTE: If no boot order is defined the default boot order defined in the VIM or NFVI shall be used.
                                                                                              
                                                            OpenModelAttribute                
                                                                                              
                                                            -  isInvariant: false             
                                                                                              
                                                            -  valueRange: no range constraint
                                                                                              
                                                            -  support: MANDATORY             
nfviConstraint         KeyValuePair               0..\*     Preliminary                        Describes constraints on the NFVI for the VNFC instance(s) created from this Vdu. For example, aspects of a secure hosting environment for the VNFC instance that involve additional entities or processes. "key/name" includes "AvailabilityZone", "HostAggregates". NOTE: These are constraints other than stipulating that a VNFC instance has access to a certain resource, as a prerequisite to instantiation. The attributes virtualComputeDesc and virtualStorageDesc define the resources required for instantiation of the VNFC instance.
                                                                                              
                                                            OpenModelAttribute                
                                                                                              
                                                            -  isInvariant: false             
                                                                                              
                                                            -  valueRange: no range constraint
                                                                                              
                                                            -  support: MANDATORY             
monitoringParameter    MonitoringParameter        0..\*     Preliminary                        Defines the virtualised resources monitoring parameters on VDU level.
                                                                                              
                                                            OpenModelAttribute                
                                                                                              
                                                            -  isInvariant: false             
                                                                                              
                                                            -  valueRange: no range constraint
                                                                                              
                                                            -  support: MANDATORY             
injectFiles            String                     0..\*     Preliminary                        Describes the information (e.g. URL) about the scripts, config drive metadata, etc. which can be used during Vdu booting process.
                                                                                              
                                                            OpenModelAttribute                
                                                                                              
                                                            -  isInvariant: false             
                                                                                              
                                                            -  valueRange: no range constraint
                                                                                              
                                                            -  support: MANDATORY             
configurableProperties VnfcConfigurableProperties 1         Preliminary                        Describes the configurable properties of all VNFC instances based on this VDU.
                                                                                              
                                                            OpenModelAttribute                
                                                                                              
                                                            -  isInvariant: false             
                                                                                              
                                                            -  valueRange: no range constraint
                                                                                              
                                                            -  support: MANDATORY             
bootData               String                     0..1      Experimental                       Contains a string or a URL to a file contained in the VNF package used to customize a virtualised compute resource at boot time. The bootData may contain variable parts that are replaced by deployment specific values before being sent to the VIM. NOTE: The parameters of each variable part shall be declared in the VnfLcmOperationsConfiguration information element as "volatile" parameters available to the bootData template during the respective VNF lifecycle management operation execution and/or in the extension attribute of the VnfInfoModifiableAttributes information element as "persistent" parameters available to the bootData template during the lifetime of the VNF instance. For VNF lifecycle management operations resulting in multiple VNFC instantiations, the VNFM supports the means to provide the appropriate parameters to appropriate VNFC instances Experimental
                                                                                              
                                                            OpenModelAttribute                 Contains a string or a URL to a file contained in the VNF package used to customize a virtualised compute resource at boot time. The bootData may contain variable parts that are replaced by deployment specific values before being sent to the VIM. NOTE: The parameters of each variable part shall be declared in the VnfLcmOperationsConfiguration information element as "volatile" parameters available to the bootData template during the respective VNF lifecycle management operation execution and/or in the extension attribute of the VnfInfoModifiableAttributes information element as "persistent" parameters available to the bootData template during the lifetime of the VNF instance. For VNF lifecycle management operations resulting in multiple VNFC instantiations, the VNFM supports the means to provide the appropriate parameters to appropriate VNFC instances Experimental
                                                                                              
                                                            -  isInvariant: false             
                                                                                              
                                                            -  valueRange: no range constraint
                                                                                              
                                                            -  support: MANDATORY             
\_intCpd               VduCpd                     1         Preliminary                        Describes network connectivity between a VNFC instance (based on this Vdu) and an internal Virtual Link (VL).
                                                                                              
                                                            OpenModelAttribute                
                                                                                              
                                                            -  isInvariant: false             
                                                                                              
                                                            -  valueRange: no range constraint
                                                                                              
                                                            -  support: MANDATORY             
\_virtualComputeDesc   VirtualComputeDesc         1..\*     Preliminary                        Describes CPU, Memory and acceleration requirements of the Virtualisation Container realising this Vdu.
                                                                                              
                                                            OpenModelAttribute                
                                                                                              
                                                            -  isInvariant: false             
                                                                                              
                                                            -  valueRange: no range constraint
                                                                                              
                                                            -  support: MANDATORY             
                                                                                              
                                                            PassedByReference                 
\_virtualStorageDesc   VirtualStorageDesc         0..\*     Preliminary                        Describes storage requirements for a VirtualStorage instance attached to the virtualisation container created from virtualComputeDesc defined for this Vdu.
                                                                                              
                                                            OpenModelAttribute                
                                                                                              
                                                            -  isInvariant: false             
                                                                                              
                                                            -  valueRange: no range constraint
                                                                                              
                                                            -  support: MANDATORY             
                                                                                              
                                                            PassedByReference                 
\_swImageDesc          SwImageDesc                0..1      Preliminary                        Describes the software image which is directly loaded on the virtualisation container realising this Vdu. NOTE: More software images can be attached to the virtualisation container using VirtualStorage resources.
                                                                                              
                                                            OpenModelAttribute                
                                                                                              
                                                            -  isInvariant: false             
                                                                                              
                                                            -  valueRange: no range constraint
                                                                                              
                                                            -  support: MANDATORY             
                                                                                              
                                                            PassedByReference                 
\_dependOn             Vdu                        0..\*     OpenModelAttribute                
                                                                                              
                                                            -  isInvariant: false             
                                                                                              
                                                            -  valueRange: no range constraint
                                                                                              
                                                            -  support: MANDATORY             
                                                                                              
                                                            Future                            
====================== ========================== ========= ================================== ===========================================================================================================================================================================================================================================================================================================================================================================================================================================================================================================================================================================================================================================================================================================================================================================================================================================================================================================

VduCpd
~~~~~~

A VduCpd information element is a type of Cpd and describes network connectivity between a VNFC instance (based on this VDU) and an internal VL.

**Parent class:** Cpd

Applied stereotypes:

-  Reference

-  **reference: IFA011 v2.5.1**

-  Preliminary

-  OpenModelClass

-  **support: MANDATORY**

===================================== =================================== ========= ================================== =============================================================================================================================================================================================================================================================================================================================
**Attribute Name**                    **Type**                            **Mult.** **Stereotypes**                    **Description**
===================================== =================================== ========= ================================== =============================================================================================================================================================================================================================================================================================================================
bitrateRequirement                    Number                              0..1      Preliminary                        Bitrate requirement on this CP.
                                                                                                                      
                                                                                    OpenModelAttribute                
                                                                                                                      
                                                                                    -  isInvariant: false             
                                                                                                                      
                                                                                    -  valueRange: no range constraint
                                                                                                                      
                                                                                    -  support: MANDATORY             
vnicName                              String                              0..1      Preliminary                        Describes the name of the vNIC this CP attaches to, e.g. eth0. It will be configured during the Vdu booting process.
                                                                                                                      
                                                                                    OpenModelAttribute                
                                                                                                                      
                                                                                    -  isInvariant: false             
                                                                                                                      
                                                                                    -  valueRange: no range constraint
                                                                                                                      
                                                                                    -  support: MANDATORY             
vnicOrder                             String                              0..1      Preliminary                        Describes the order to create the vNIC within the scope of this Vdu.
                                                                                                                      
                                                                                    OpenModelAttribute                
                                                                                                                      
                                                                                    -  isInvariant: false             
                                                                                                                      
                                                                                    -  valueRange: no range constraint
                                                                                                                      
                                                                                    -  support: MANDATORY             
vnicType                              VnicType                            0..1      Preliminary                        Describes the type of the vNIC this CP attaches to.
                                                                                                                      
                                                                                    OpenModelAttribute                
                                                                                                                      
                                                                                    -  isInvariant: false             
                                                                                                                      
                                                                                    -  valueRange: no range constraint
                                                                                                                      
                                                                                    -  support: MANDATORY             
\_virtualNetworkInterfaceRequirements VirtualNetworkInterfaceRequirements 0..\*     Preliminary                        Specifies requirements on a virtual network interface realising the CPs instantiated from this CPD.
                                                                                                                      
                                                                                    OpenModelAttribute                
                                                                                                                      
                                                                                    -  isInvariant: false             
                                                                                                                      
                                                                                    -  valueRange: no range constraint
                                                                                                                      
                                                                                    -  support: MANDATORY             
sriovAntiAffinityGroup                Identifier                          0..1      OpenModelAttribute                 Define the port anti-affinity group ID for each SR-IOV type vNIC. Multiple vNICs in the same anti-affinity group must belong to the same virtual network, and the number of vNICs in the same anti-affinity group cannot exceed two.
                                                                                                                      
                                                                                    -  isInvariant: false             
                                                                                                                      
                                                                                    -  valueRange: no range constraint
                                                                                                                      
                                                                                    -  support: OPTIONAL              
                                                                                                                      
                                                                                    Future                            
securityGroups                        String                              0..\*     OpenModelAttribute                 VNFD needs to specify the security group name {security_groups} for each vNic.
                                                                                                                      
                                                                                    -  isInvariant: false             
                                                                                                                      
                                                                                    -  valueRange: no range constraint
                                                                                                                      
                                                                                    -  support: MANDATORY             
                                                                                                                      
                                                                                    Future                            
portSecurityEnabled                   Boolean                             0..1      OpenModelAttribute                 VNFD needs to specify whether to enable security group for the vNic.
                                                                                                                      
                                                                                    -  isInvariant: false             
                                                                                                                      
                                                                                    -  valueRange: no range constraint
                                                                                                                      
                                                                                    -  support: MANDATORY             
                                                                                                                      
                                                                                    Future                            
qos                                   QoS                                 0..1      OpenModelAttribute                 Describe the Qos requirements of the VduCpd.
                                                                                                                      
                                                                                    -  isInvariant: false             
                                                                                                                      
                                                                                    -  valueRange: no range constraint
                                                                                                                      
                                                                                    -  support: MANDATORY             
                                                                                                                      
                                                                                    Future                            
\_intVirtualLinkDesc                  VnfVirtualLinkDesc                  0..1      Experimental                       Reference(s) of the Virtual Link Descriptor to which this Connection Point Descriptor(s) connects.
                                                                                                                      
                                                                                    OpenModelAttribute                
                                                                                                                      
                                                                                    -  isInvariant: false             
                                                                                                                      
                                                                                    -  valueRange: no range constraint
                                                                                                                      
                                                                                    -  support: MANDATORY             
                                                                                                                      
                                                                                    PassedByReference                 
allowedAddressData                    AddressData                         0..\*     Preliminary                        For specifying floating IP(s) to be shared among Cpds, which are reserved for vnfReservedCpd described in the VNFD.
                                                                                                                      
                                                                                    OpenModelAttribute                
                                                                                                                      
                                                                                    -  isInvariant: false             
                                                                                                                      
                                                                                    -  valueRange: no range constraint
                                                                                                                      
                                                                                    -  support: MANDATORY             
cpdId                                 Identifier                          1         Preliminary                        Identifier of this Cpd information element.
                                                                                                                      
                                                                                    OpenModelAttribute                
                                                                                                                      
                                                                                    -  isInvariant: true              
                                                                                                                      
                                                                                    -  valueRange: no range constraint
                                                                                                                      
                                                                                    -  support: MANDATORY             
cpdRole                               String                              0..1      Preliminary                        Identifies the role of the port in the context of the traffic flow patterns in the VNF or parent NS. For example a VNF with a tree flow pattern within the VNF will have legal cpRoles of ROOT and LEAF.
                                                                                                                      
                                                                                    OpenModelAttribute                
                                                                                                                      
                                                                                    -  isInvariant: false             
                                                                                                                      
                                                                                    -  valueRange: no range constraint
                                                                                                                      
                                                                                    -  support: MANDATORY             
description                           String                              0..1      Preliminary                        Provides human-readable information on the purpose of the CP (e.g. CP for control plane traffic).
                                                                                                                      
                                                                                    OpenModelAttribute                
                                                                                                                      
                                                                                    -  isInvariant: false             
                                                                                                                      
                                                                                    -  valueRange: no range constraint
                                                                                                                      
                                                                                    -  support: MANDATORY             
cpProtocol                            CpProtocolData                      1..\*     Preliminary                        Identifies the protocol layering information the CP uses for connectivity purposes and associated information. There shall be one cpProtocol for each layer protocol as indicated by the attribute layerProtocol. Editor's note: the attribute "layerProtocol" still needs further discussion and not included in this table.
                                                                                                                      
                                                                                    OpenModelAttribute                
                                                                                                                      
                                                                                    -  isInvariant: false             
                                                                                                                      
                                                                                    -  valueRange: no range constraint
                                                                                                                      
                                                                                    -  support: MANDATORY             
trunkMode                             Boolean                             1         Preliminary                        Information about whether the CP instantiated from this CPD is in Trunk mode (802.1Q or other).
                                                                                                                      
                                                                                    OpenModelAttribute                
                                                                                                                      
                                                                                    -  isInvariant: false             
                                                                                                                      
                                                                                    -  valueRange: no range constraint
                                                                                                                      
                                                                                    -  support: MANDATORY             
layerProtocol                         LayerProtocol                       1..\*     Experimental                       Identifies which protocol the CP uses for connectivity purposes (Ethernet, MPLS, ODU2, IPV4, IPV6, Pseudo-Wire, etc.).
                                                                                                                      
                                                                                    OpenModelAttribute                
                                                                                                                      
                                                                                    -  isInvariant: false             
                                                                                                                      
                                                                                    -  valueRange: no range constraint
                                                                                                                      
                                                                                    -  support: MANDATORY             
securityGroupRuleId                   Identifier                          0..\*     Experimental                       Reference of the security group rules bound to this CPD.
                                                                                                                      
                                                                                    OpenModelAttribute                
                                                                                                                      
                                                                                    -  isInvariant: false             
                                                                                                                      
                                                                                    -  valueRange: no range constraint
                                                                                                                      
                                                                                    -  support: MANDATORY             
===================================== =================================== ========= ================================== =============================================================================================================================================================================================================================================================================================================================

VduLevel
~~~~~~~~

The VduLevel information element indicates for a given VDU in a given level the number of instances to deploy.

Applied stereotypes:

-  Reference

-  **reference: IFA011 v2.5.1**

-  Preliminary

-  OpenModelClass

-  **support: MANDATORY**

================== ======== ========= ================================== ==========================================================================================================
**Attribute Name** **Type** **Mult.** **Stereotypes**                    **Description**
================== ======== ========= ================================== ==========================================================================================================
numberOfInstances  Integer  1         Preliminary                        Number of instances of VNFC based on this VDU to deploy for an instantiation level or for a scaling delta.
                                                                        
                                      OpenModelAttribute                
                                                                        
                                      -  isInvariant: false             
                                                                        
                                      -  valueRange: no range constraint
                                                                        
                                      -  support: MANDATORY             
\_vduId            Vdu      1         Experimental                       Uniquely identifies a VDU.
                                                                        
                                      OpenModelAttribute                
                                                                        
                                      -  isInvariant: false             
                                                                        
                                      -  valueRange: no range constraint
                                                                        
                                      -  support: MANDATORY             
                                                                        
                                      PassedByReference                 
================== ======== ========= ================================== ==========================================================================================================

VduProfile
~~~~~~~~~~

The VduProfile describes additional instantiation data for a given VDU used in a DF.

Applied stereotypes:

-  Reference

-  **reference: IFA011 v2.5.1**

-  Preliminary

-  OpenModelClass

-  **support: MANDATORY**

=============================== =============================== ========= ================================== =====================================================================================================================================================================================================================================================================================================================================================================================================================================================================================================================================================================================================================================================================================================================================================================================
**Attribute Name**              **Type**                        **Mult.** **Stereotypes**                    **Description**
=============================== =============================== ========= ================================== =====================================================================================================================================================================================================================================================================================================================================================================================================================================================================================================================================================================================================================================================================================================================================================================================
minNumberOfInstances            Integer                         1         Preliminary                        Minimum number of instances of the VNFC based on this VDU that is permitted to exist for this flavour. Shall be zero or greater.
                                                                                                            
                                                                          OpenModelAttribute                
                                                                                                            
                                                                          -  isInvariant: false             
                                                                                                            
                                                                          -  valueRange: no range constraint
                                                                                                            
                                                                          -  support: MANDATORY             
maxNumberOfInstances            Integer                         1         Preliminary                        Maximum number of instances of the VNFC based on this VDU that is permitted to exist for this flavour. Shall be zero or greater.
                                                                                                            
                                                                          OpenModelAttribute                
                                                                                                            
                                                                          -  isInvariant: false             
                                                                                                            
                                                                          -  valueRange: no range constraint
                                                                                                            
                                                                          -  support: MANDATORY             
localAffinityOrAntiAffinityRule LocalAffinityOrAntiAffinityRule 0..\*     Preliminary                        Specifies affinity or anti-affinity rules applicable between the virtualization containers (e.g. virtual machines) to be created based on this VDU. When the cardinality is greater than 1, both affinity rule(s) and anti-affinity rule(s) with different scopes (e.g. "Affinity with the scope resource zone and anti-affinity with the scope NFVI node") are applicable to the virtualization containers (e.g. virtual machines) to be created based on this VDU. When the cardinality is greater than 1, both affinity rule(s) and anti-affinity rule(s) with different scopes (e.g. "Affinity with the scope resource zone and anti-affinity with the scope NFVI node") are applicable to the virtualization containers (e.g. virtual machines) to be created based on this VDU.
                                                                                                            
                                                                          OpenModelAttribute                
                                                                                                            
                                                                          -  isInvariant: false             
                                                                                                            
                                                                          -  valueRange: no range constraint
                                                                                                            
                                                                          -  support: MANDATORY             
affinityOrAntiAffinityGroupId   Identifier                      0..\*     Preliminary                        Identifier(s) of the affinity or anti-affinity group(s) the VDU belongs to. NOTE: Each identifier references an affinity or anti-affinity group which expresses affinity or anti-affinity relationships between the virtualisation container(s) (e.g. virtual machine(s)) to be created using this VDU and the virtualisation container(s) (e.g. virtual machine(s)) to be created using other VDU(s) in the same group.
                                                                                                            
                                                                          OpenModelAttribute                
                                                                                                            
                                                                          -  isInvariant: false             
                                                                                                            
                                                                          -  valueRange: no range constraint
                                                                                                            
                                                                          -  support: MANDATORY             
watchdog                        String                          0..1      Preliminary                        Watchdog action to be triggered by the VIM for the VNF in case the heart beat fails, e.g. reset or hard shutdown, etc.
                                                                                                            
                                                                          OpenModelAttribute                
                                                                                                            
                                                                          -  isInvariant: false             
                                                                                                            
                                                                          -  valueRange: no range constraint
                                                                                                            
                                                                          -  support: MANDATORY             
vmBootUpTimeOut                 Integer                         0..1      Preliminary                        Timeout value for the VNFM to wait before the successful booting up of the VDU.
                                                                                                            
                                                                          OpenModelAttribute                
                                                                                                            
                                                                          -  isInvariant: false             
                                                                                                            
                                                                          -  valueRange: no range constraint
                                                                                                            
                                                                          -  support: MANDATORY             
securityGroups                  String                          0..\*     OpenModelAttribute                 VNFD needs to specify the security group name {security_groups} for each VDU.
                                                                                                            
                                                                          -  isInvariant: false             
                                                                                                            
                                                                          -  valueRange: no range constraint
                                                                                                            
                                                                          -  support: MANDATORY             
                                                                                                            
                                                                          Future                            
flavorExtraSpecs                KeyValuePair                    0..\*     OpenModelAttribute                 Additional expansion requirements for Infrastructure layer, e.g. HA property (Host Aggregate ).
                                                                                                            
                                                                          -  isInvariant: false             
                                                                                                            
                                                                          -  valueRange: no range constraint
                                                                                                            
                                                                          -  support: MANDATORY             
                                                                                                            
                                                                          Future                            
\_vduId                         Vdu                             1         Preliminary                       
                                                                                                            
                                                                          OpenModelAttribute                
                                                                                                            
                                                                          -  isInvariant: false             
                                                                                                            
                                                                          -  valueRange: no range constraint
                                                                                                            
                                                                          -  support: MANDATORY             
                                                                                                            
                                                                          PassedByReference                 
=============================== =============================== ========= ================================== =====================================================================================================================================================================================================================================================================================================================================================================================================================================================================================================================================================================================================================================================================================================================================================================================

VirtualComputeDesc
~~~~~~~~~~~~~~~~~~

The VirtualComputeDesc information element supports the specification of requirements related to virtual compute resources.

Applied stereotypes:

-  Reference

-  **reference: IFA011 v2.5.1**

-  Preliminary

-  OpenModelClass

-  **support: MANDATORY**

============================= ================================= ========= ================================== ===========================================================================================================================================
**Attribute Name**            **Type**                          **Mult.** **Stereotypes**                    **Description**
============================= ================================= ========= ================================== ===========================================================================================================================================
virtualComputeDescId          Identifier                        1         Preliminary                        Unique identifier of this VirtualComputeDesc in the VNFD
                                                                                                            
                                                                          OpenModelAttribute                
                                                                                                            
                                                                          -  isInvariant: false             
                                                                                                            
                                                                          -  valueRange: no range constraint
                                                                                                            
                                                                          -  support: MANDATORY             
requestAdditionalCapabilities RequestedAdditionalCapabilityData 0..\*     Deprecated                         Specifies requirements for additional capabilities. These may be for a range of purposes. One example is acceleration related capabilities.
                                                                                                            
                                                                          OpenModelAttribute                
                                                                                                            
                                                                          -  isInvariant: false             
                                                                                                            
                                                                          -  valueRange: no range constraint
                                                                                                            
                                                                          -  support: MANDATORY             
computeRequirements           KeyValuePair                      0..\*     Preliminary                        Specifies compute requirements.
                                                                                                            
                                                                          OpenModelAttribute                
                                                                                                            
                                                                          -  isInvariant: false             
                                                                                                            
                                                                          -  valueRange: no range constraint
                                                                                                            
                                                                          -  support: MANDATORY             
virtualMemory                 VirtualMemoryData                 1         Preliminary                        The virtual memory of the virtualised compute.
                                                                                                            
                                                                          OpenModelAttribute                
                                                                                                            
                                                                          -  isInvariant: false             
                                                                                                            
                                                                          -  valueRange: no range constraint
                                                                                                            
                                                                          -  support: MANDATORY             
virtualCpu                    VirtualCpuData                    1         Preliminary                        The virtual CPU(s) of the virtualised compute.
                                                                                                            
                                                                          OpenModelAttribute                
                                                                                                            
                                                                          -  isInvariant: false             
                                                                                                            
                                                                          -  valueRange: no range constraint
                                                                                                            
                                                                          -  support: MANDATORY             
\_logicalNodeRequirements     LogicalNodeRequirements           0..\*     Experimental                       The associated logical node requirements.
                                                                                                            
                                                                          OpenModelAttribute                
                                                                                                            
                                                                          -  isInvariant: false             
                                                                                                            
                                                                          -  valueRange: no range constraint
                                                                                                            
                                                                          -  support: MANDATORY             
virtualDisk                   BlockStorageData                  0..\*     Experimental                       The local or ephemeral disk(s) of the virtualised compute.
                                                                                                            
                                                                          OpenModelAttribute                
                                                                                                            
                                                                          -  isInvariant: false             
                                                                                                            
                                                                          -  valueRange: no range constraint
                                                                                                            
                                                                          -  support: MANDATORY             
============================= ================================= ========= ================================== ===========================================================================================================================================

VirtualLinkDescFlavour
~~~~~~~~~~~~~~~~~~~~~~

The VirtualLinkDescFlavour describes additional instantiation data for a given internal VL used in a DF.

Applied stereotypes:

-  Reference

-  **reference: IFA011 v2.5.1**

-  Preliminary

-  OpenModelClass

-  **support: MANDATORY**

================== ========== ========= ================================== =================================================
**Attribute Name** **Type**   **Mult.** **Stereotypes**                    **Description**
================== ========== ========= ================================== =================================================
qos                VnfQoS     0..1      Preliminary                        QoS of the VL.
                                                                          
                                        OpenModelAttribute                
                                                                          
                                        -  isInvariant: false             
                                                                          
                                        -  valueRange: no range constraint
                                                                          
                                        -  support: MANDATORY             
flavourId          Identifier 1         Preliminary                        Identifies a flavour within a VnfVirtualLinkDesc.
                                                                          
                                        OpenModelAttribute                
                                                                          
                                        -  isInvariant: false             
                                                                          
                                        -  valueRange: no range constraint
                                                                          
                                        -  support: MANDATORY             
================== ========== ========= ================================== =================================================

VirtualLinkProfile
~~~~~~~~~~~~~~~~~~

The VirtualLinkProfile describes additional instantiation data for a given VL used in a DF.

Applied stereotypes:

-  Reference

-  **reference: IFA011 v2.5.1**

-  Preliminary

-  OpenModelClass

-  **support: MANDATORY**

=============================== =============================== ========= ================================== =======================================================================================================================================================================================================================================================================================================================================================
**Attribute Name**              **Type**                        **Mult.** **Stereotypes**                    **Description**
=============================== =============================== ========= ================================== =======================================================================================================================================================================================================================================================================================================================================================
virtualLinkProfileId            Identifier                      1         Experimental                       Uniquely identifies this VirtualLinkProfile class
                                                                                                            
                                                                          OpenModelAttribute                
                                                                                                            
                                                                          -  isInvariant: true              
                                                                                                            
                                                                          -  valueRange: no range constraint
                                                                                                            
                                                                          -  support: MANDATORY             
localAffinityOrAntiAffinityRule LocalAffinityOrAntiAffinityRule 0..\*     Preliminary                        Specifies affinity or anti-affinity rules applicable between the VLs based on this VnfVirtualLinkDesc. When the cardinality is greater than 1, both affinity rule(s) and anti-affinity rule(s) with different scopes are applicable to the VLs based on this VnfVirtualLinkDesc.
                                                                                                            
                                                                          OpenModelAttribute                
                                                                                                            
                                                                          -  isInvariant: false             
                                                                                                            
                                                                          -  valueRange: no range constraint
                                                                                                            
                                                                          -  support: MANDATORY             
maxBitRateRequirements          LinkBitrateRequirements         1         Preliminary                        Specifies the minimum bitrate requirements for a VL instantiated according to this profile.
                                                                                                            
                                                                          OpenModelAttribute                
                                                                                                            
                                                                          -  isInvariant: false             
                                                                                                            
                                                                          -  valueRange: no range constraint
                                                                                                            
                                                                          -  support: MANDATORY             
minBitRateRequirements          LinkBitrateRequirements         1         Preliminary                        Specifies the minimum bitrate requirements for a VL instantiated according to this profile.
                                                                                                            
                                                                          OpenModelAttribute                
                                                                                                            
                                                                          -  isInvariant: false             
                                                                                                            
                                                                          -  valueRange: no range constraint
                                                                                                            
                                                                          -  support: MANDATORY             
\_flavourId                     VirtualLinkDescFlavour          1         Preliminary                        Identifies a flavour within the VnfVirtualLinkDesc.
                                                                                                            
                                                                          OpenModelAttribute                
                                                                                                            
                                                                          -  isInvariant: false             
                                                                                                            
                                                                          -  valueRange: no range constraint
                                                                                                            
                                                                          -  support: MANDATORY             
\_affinityOrAntiAffinityGroupId AffinityOrAntiAffinityGroup     0..\*     Experimental                       Identifies an affinity or anti-affinity group the VLs instantiated according to the VlProfile belong to. NOTE : Each identifier references an affinity or anti-affinity group which expresses affinity or anti-affinity relationship between the VL(s) using this VirtualLinkProfile and the VL(s) using other VirtualLinkProfile(s) in the same group.
                                                                                                            
                                                                          OpenModelAttribute                
                                                                                                            
                                                                          -  isInvariant: false             
                                                                                                            
                                                                          -  valueRange: no range constraint
                                                                                                            
                                                                          -  support: MANDATORY             
                                                                                                            
                                                                          PassedByReference                 
\_vnfVirtualLinkDescId          VnfVirtualLinkDesc              1         Preliminary                        Uniquely references a VLD.
                                                                                                            
                                                                          OpenModelAttribute                
                                                                                                            
                                                                          -  isInvariant: false             
                                                                                                            
                                                                          -  valueRange: no range constraint
                                                                                                            
                                                                          -  support: MANDATORY             
                                                                                                            
                                                                          PassedByReference                 
virtualLinkProtocolData         VirtualLinkProtocolData         0..\*     Preliminary                        Specifies the protocol data for a VL instantiated according to this profile. Cardinality 0 is used when no protocol data needs to be specified.
                                                                                                            
                                                                          OpenModelAttribute                
                                                                                                            
                                                                          -  isInvariant: false             
                                                                                                            
                                                                          -  valueRange: no range constraint
                                                                                                            
                                                                          -  support: MANDATORY             
=============================== =============================== ========= ================================== =======================================================================================================================================================================================================================================================================================================================================================

VirtualNetworkInterfaceRequirements
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

This class specifies requirements on a virtual network interface.

Applied stereotypes:

-  Reference

-  **reference: IFA011 v2.5.1**

-  Preliminary

-  OpenModelClass

-  **support: MANDATORY**

============================ ======================= ========= ================================== ==========================================================================================================================================================================================================================================================================================================================================
**Attribute Name**           **Type**                **Mult.** **Stereotypes**                    **Description**
============================ ======================= ========= ================================== ==========================================================================================================================================================================================================================================================================================================================================
name                         String                  0..1      Preliminary                        Provides a human readable name for the requirement.
                                                                                                 
                                                               OpenModelAttribute                
                                                                                                 
                                                               -  isInvariant: false             
                                                                                                 
                                                               -  valueRange: no range constraint
                                                                                                 
                                                               -  support: MANDATORY             
description                  String                  0..1      Preliminary                        Provides a human readable description of the requirement.
                                                                                                 
                                                               OpenModelAttribute                
                                                                                                 
                                                               -  isInvariant: false             
                                                                                                 
                                                               -  valueRange: no range constraint
                                                                                                 
                                                               -  support: MANDATORY             
supportMandatory             Boolean                 1         Preliminary                        Indicates whether fulfilling the constraint is mandatory (TRUE) for successful operation or desirable (FALSE).
                                                                                                 
                                                               OpenModelAttribute                
                                                                                                 
                                                               -  isInvariant: false             
                                                                                                 
                                                               -  valueRange: no range constraint
                                                                                                 
                                                               -  support: MANDATORY             
networkInterfaceRequirements KeyValuePair            0..\*     Preliminary                        The network interface requirements. An element from an array of key-value pairs that articulate the network interface deployment requirements
                                                                                                 
                                                               OpenModelAttribute                
                                                                                                 
                                                               -  isInvariant: false             
                                                                                                 
                                                               -  valueRange: no range constraint
                                                                                                 
                                                               -  support: MANDATORY             
\_nicIoRequirements          LogicalNodeRequirements 0..1      OpenModelAttribute                 This references (couples) the CPD with any logical node I/O requirements (for network devices) that may have been created. Linking these attributes is necessary so that so that I/O requirements that need to be articulated at the logical node level can be associated with the network interface requirements associated with the CPD.
                                                                                                 
                                                               -  isInvariant: false             
                                                                                                 
                                                               -  valueRange: no range constraint
                                                                                                 
                                                               -  support: MANDATORY             
                                                                                                 
                                                               PassedByReference                 
============================ ======================= ========= ================================== ==========================================================================================================================================================================================================================================================================================================================================

VirtualStorageDesc
~~~~~~~~~~~~~~~~~~

The VirtualStorageDesc information element supports the specifications of requirements related to persistent virtual storage resources. Ephemeral virtual storage is specified in VirtualComputeDesc information element.

Applied stereotypes:

-  Reference

-  **reference: IFA011 v2.5.1**

-  Preliminary

-  OpenModelClass

-  **support: MANDATORY**

================== ================= ========= ================================== ===============================================================================================================================================
**Attribute Name** **Type**          **Mult.** **Stereotypes**                    **Description**
================== ================= ========= ================================== ===============================================================================================================================================
id                 Identifier        1         Preliminary                        Unique identifier of this VirtualStorageDesc in the VNFD.
                                                                                 
                                               OpenModelAttribute                
                                                                                 
                                               -  isInvariant: false             
                                                                                 
                                               -  valueRange: no range constraint
                                                                                 
                                               -  support: MANDATORY             
typeOfStorage      String            1         Preliminary                        Type of virtualised storage resource (BLOCK, OBJECT, FILE).
                                                                                 
                                               OpenModelAttribute                
                                                                                 
                                               -  isInvariant: false             
                                                                                 
                                               -  valueRange: no range constraint
                                                                                 
                                               -  support: MANDATORY             
sizeOfStorage      Number            1         Preliminary                        Size of virtualised storage resource (e.g. size of volume, in GB).
                                                                                 
                                               OpenModelAttribute                
                                                                                 
                                               -  isInvariant: false             
                                                                                 
                                               -  valueRange: no range constraint
                                                                                 
                                               -  support: MANDATORY             
blockStorageData   BlockStorageData  0..1      Preliminary                        Specifies the details of block storage. It shall be present when the "typeOfStorage" attribute is set to "BLOCK". It shall be absent otherwise.
                                                                                 
                                               OpenModelAttribute                
                                                                                 
                                               -  isInvariant: false             
                                                                                 
                                               -  valueRange: no range constraint
                                                                                 
                                               -  support: MANDATORY             
objectStorageData  ObjectStorageData 0..1      Preliminary                        Specifies the details of object storage. It shall be present when the "typeOfStorage" attribute is set to "OBJECT". It shall be absent
                                                                                 
                                               OpenModelAttribute                
                                                                                 
                                               -  isInvariant: false             
                                                                                 
                                               -  valueRange: no range constraint
                                                                                 
                                               -  support: MANDATORY             
fileStorageData    FileStorageData   0..1      Preliminary                        Specifies the details of file storage. It shall be present when the "typeOfStorage" attribute is set to "FILE". It shall be absent otherwise.
                                                                                 
                                               OpenModelAttribute                
                                                                                 
                                               -  isInvariant: false             
                                                                                 
                                               -  valueRange: no range constraint
                                                                                 
                                               -  support: MANDATORY             
multiAttach        Boolean           0..1      OpenModelAttribute                 Indicating whether a vDisk is a shared volume in VNFD.
                                                                                 
                                               -  isInvariant: false             
                                                                                 
                                               -  valueRange: no range constraint
                                                                                 
                                               -  support: MANDATORY             
                                                                                 
                                               Future                            
storageQos         StorageQos        0..1      OpenModelAttribute                 Describe storage Qos requirements.
                                                                                 
                                               -  isInvariant: false             
                                                                                 
                                               -  valueRange: no range constraint
                                                                                 
                                               -  support: MANDATORY             
                                                                                 
                                               Future                            
volumeType         VolumeType        0..1      OpenModelAttribute                 Describe volume type.
                                                                                 
                                               -  isInvariant: false             
                                                                                 
                                               -  valueRange: no range constraint
                                                                                 
                                               -  support: MANDATORY             
                                                                                 
                                               Future                            
================== ================= ========= ================================== ===============================================================================================================================================

Vnf
~~~

An implementation of an NF that can be deployed on a Network Function Virtualisation Infrastructure (NFVI).

**Parent class:** NetworkFunction

Applied stereotypes:

-  Experimental

-  OpenModelClass

-  **support: MANDATORY**

======================= =================== ========= ================================== =========================================================================================================================
**Attribute Name**      **Type**            **Mult.** **Stereotypes**                    **Description**
======================= =================== ========= ================================== =========================================================================================================================
vnfProductName          String              1         Experimental                       name to identify the VNF Product, invariant for the VNF Product lifetime
                                                                                        
                                                      OpenModelAttribute                
                                                                                        
                                                      -  isInvariant: true              
                                                                                        
                                                      -  valueRange: no range constraint
                                                                                        
                                                      -  support: MANDATORY             
vnfProvider             String              1         Experimental                       provider of the VNF model
                                                                                        
                                                      OpenModelAttribute                
                                                                                        
                                                      -  isInvariant: false             
                                                                                        
                                                      -  valueRange: no range constraint
                                                                                        
                                                      -  support: MANDATORY             
vnfSoftwareVersion      Version             1         Experimental                       Software version of the VNF. This is changed when there is any change to the software that is included in the VNF package
                                                                                        
                                                      OpenModelAttribute                
                                                                                        
                                                      -  isInvariant: false             
                                                                                        
                                                      -  valueRange: no range constraint
                                                                                        
                                                      -  support: MANDATORY             
vnfPkgId                Identifier          1         Experimental                       identifier of the specific VNF package on which the VNF instance is based
                                                                                        
                                                      OpenModelAttribute                
                                                                                        
                                                      -  isInvariant: false             
                                                                                        
                                                      -  valueRange: no range constraint
                                                                                        
                                                      -  support: MANDATORY             
zone                    String              1         Experimental                       availability zone information of the VNF instance
                                                                                        
                                                      OpenModelAttribute                
                                                                                        
                                                      -  isInvariant: false             
                                                                                        
                                                      -  valueRange: no range constraint
                                                                                        
                                                      -  support: MANDATORY             
operationalStatus       OperationalStatus   0..1      Experimental                       indicator for whether the resource is considered operational. Valid values are in-service-path and out-of-service-path.
                                                                                        
                                                      OpenModelAttribute                
                                                                                        
                                                      -  isInvariant: false             
                                                                                        
                                                      -  valueRange: no range constraint
                                                                                        
                                                      -  support: MANDATORY             
orchestrationStatus     OrchestrationStatus 1         Experimental                       whether the VNF instance is instantiated
                                                                                        
                                                      OpenModelAttribute                
                                                                                        
                                                      -  isInvariant: false             
                                                                                        
                                                      -  valueRange: no range constraint
                                                                                        
                                                      -  support: MANDATORY             
oamlpv4Address          String              0..1      Experimental                       oam ip address, ipv4
                                                                                        
                                                      OpenModelAttribute                
                                                                                        
                                                      -  isInvariant: false             
                                                                                        
                                                      -  valueRange: no range constraint
                                                                                        
                                                      -  support: MANDATORY             
oamlpv6Address          String              0..1      Experimental                       oam ip address, ipv6
                                                                                        
                                                      OpenModelAttribute                
                                                                                        
                                                      -  isInvariant: false             
                                                                                        
                                                      -  valueRange: no range constraint
                                                                                        
                                                      -  support: MANDATORY             
instantiatedVnfInfo     String              0..1      Experimental                       information specific to an instantiated VNF instance, e.g., vm information
                                                                                        
                                                      OpenModelAttribute                
                                                                                        
                                                      -  isInvariant: false             
                                                                                        
                                                      -  valueRange: no range constraint
                                                                                        
                                                      -  support: MANDATORY             
inMaint                 Boolean             0..1      Experimental                       whether the VNF instance is in maintenance mode, if yes, DCAE will not observe alarms/traps, etc.
                                                                                        
                                                      OpenModelAttribute                
                                                                                        
                                                      -  isInvariant: false             
                                                                                        
                                                      -  valueRange: no range constraint
                                                                                        
                                                      -  support: MANDATORY             
closedLoopEnabled       Boolean             0..1      Experimental                       Indicates whether the closed loop function is enabled or disabled.
                                                                                        
                                                      OpenModelAttribute                
                                                                                        
                                                      -  isInvariant: false             
                                                                                        
                                                      -  valueRange: no range constraint
                                                                                        
                                                      -  support: MANDATORY             
encryptedAccessFlag     Boolean             0..1      Experimental                       whether this VNF is accessed using SSH
                                                                                        
                                                      OpenModelAttribute                
                                                                                        
                                                      -  isInvariant: false             
                                                                                        
                                                      -  valueRange: no range constraint
                                                                                        
                                                      -  support: MANDATORY             
vnfConfigurableProperty invalid             0..1      Experimental                       indicator for whether autoHeal and autoScale is enabled
                                                                                        
                                                      OpenModelAttribute                
                                                                                        
                                                      -  isInvariant: false             
                                                                                        
                                                      -  valueRange: no range constraint
                                                                                        
                                                      -  support: MANDATORY             
vnfNamingPolicyId       String              1         Experimental                       Identifier of the policy which has the naming logic for this VNF instance
                                                                                        
                                                      OpenModelAttribute                
                                                                                        
                                                      -  isInvariant: false             
                                                                                        
                                                      -  valueRange: no range constraint
                                                                                        
                                                      -  support: MANDATORY             
vnfHomingPolicyId       String              1         Experimental                       Identifier of the policy which provides homing conditions.
                                                                                        
                                                      OpenModelAttribute                
                                                                                        
                                                      -  isInvariant: false             
                                                                                        
                                                      -  valueRange: no range constraint
                                                                                        
                                                      -  support: MANDATORY             
\_vnfc                  Vnfc                1..\*     Experimental                       Relatonship to the VNF components that are part of this VNF.
                                                                                        
                                                      OpenModelAttribute                
                                                                                        
                                                      -  isInvariant: false             
                                                                                        
                                                      -  valueRange: no range constraint
                                                                                        
                                                      -  support: MANDATORY             
\_vnfd                  Vnfd                1         Experimental                       Relationship to the VNF descriptor
                                                                                        
                                                      OpenModelAttribute                
                                                                                        
                                                      -  isInvariant: false             
                                                                                        
                                                      -  valueRange: no range constraint
                                                                                        
                                                      -  support: MANDATORY             
                                                                                        
                                                      PassedByReference                 
\_vnfvirtuallink        VnfVirtualLink      0..\*     Experimental                       Relationship to VnfVirtualLink
                                                                                        
                                                      OpenModelAttribute                
                                                                                        
                                                      -  isInvariant: false             
                                                                                        
                                                      -  valueRange: no range constraint
                                                                                        
                                                      -  support: MANDATORY             
veVnfmVnfInterface      String              0..1      Experimental                       IP address between VNF and VNFM.
                                                                                        
                                                      OpenModelAttribute                
                                                                                        
                                                      -  isInvariant: false             
                                                                                        
                                                      -  valueRange: no range constraint
                                                                                        
                                                      -  support: MANDATORY             
id                      String              1         Experimental                       Identifier of the network function
                                                                                        
                                                      OpenModelAttribute                
                                                                                        
                                                      -  isInvariant: false             
                                                                                        
                                                      -  valueRange: no range constraint
                                                                                        
                                                      -  support: MANDATORY             
name                    String              0..1      Experimental                      
                                                                                        
                                                      OpenModelAttribute                
                                                                                        
                                                      -  isInvariant: false             
                                                                                        
                                                      -  valueRange: no range constraint
                                                                                        
                                                      -  support: MANDATORY             
type                    String              1         Experimental                       Description of the type of network function
                                                                                        
                                                      OpenModelAttribute                
                                                                                        
                                                      -  isInvariant: false             
                                                                                        
                                                      -  valueRange: no range constraint
                                                                                        
                                                      -  support: MANDATORY             
description             String              0..1      Experimental                       Description of the network function
                                                                                        
                                                      OpenModelAttribute                
                                                                                        
                                                      -  isInvariant: false             
                                                                                        
                                                      -  valueRange: no range constraint
                                                                                        
                                                      -  support: MANDATORY             
role                    String              1         Experimental                       Role the network function will be providing.
                                                                                        
                                                      OpenModelAttribute                
                                                                                        
                                                      -  isInvariant: false             
                                                                                        
                                                      -  valueRange: no range constraint
                                                                                        
                                                      -  support: MANDATORY             
======================= =================== ========= ================================== =========================================================================================================================

VnfDf
~~~~~

The VnfDf describes a specific deployment version of a VNF.

Applied stereotypes:

-  Reference

-  **reference: IFA011 v2.5.1**

-  Preliminary

-  OpenModelClass

-  **support: MANDATORY**

============================= =========================== ========= ================================== ===================================================================================================================================================================================================================================================================================================================================================================================================================================================================================================================================================================================
**Attribute Name**            **Type**                    **Mult.** **Stereotypes**                    **Description**
============================= =========================== ========= ================================== ===================================================================================================================================================================================================================================================================================================================================================================================================================================================================================================================================================================================
flavorId                      Identifier                  1         Preliminary                        Identifier of this DF within the VNFD.
                                                                                                      
                                                                    OpenModelAttribute                
                                                                                                      
                                                                    -  isInvariant: true              
                                                                                                      
                                                                    -  valueRange: no range constraint
                                                                                                      
                                                                    -  support: MANDATORY             
description                   String                      1         Preliminary                        Human readable description of the DF.
                                                                                                      
                                                                    OpenModelAttribute                
                                                                                                      
                                                                    -  isInvariant: false             
                                                                                                      
                                                                    -  valueRange: no range constraint
                                                                                                      
                                                                    -  support: MANDATORY             
defaultInstantiationLevel     Identifier                  0..1      Experimental                       This attribute references the "instantiationLevel" entry which defines the default instantiation level for this DF. It shall be present if there are multiple "instantiationLevel" entries.
                                                                                                      
                                                                    OpenModelAttribute                
                                                                                                      
                                                                    -  isInvariant: false             
                                                                                                      
                                                                    -  valueRange: no range constraint
                                                                                                      
                                                                    -  support: MANDATORY             
monitoringParameter           MonitoringParameter         0..\*     Experimental                       Specifies the virtualised resource related performance metrics to be tracked by the VNFM.
                                                                                                      
                                                                    OpenModelAttribute                
                                                                                                      
                                                                    -  isInvariant: false             
                                                                                                      
                                                                    -  valueRange: no range constraint
                                                                                                      
                                                                    -  support: MANDATORY             
\_virtuaLlinkProfile          VirtualLinkProfile          0..\*     Preliminary                        Defines the internal VLD along with additional data which is used in this DF. NOTE 1: This allows for different VNF internal topologies between DFs. NOTE 2: virtualLinkProfile needs to be provided for all VLs that the CPs of the VDUs in the VDU profiles connect to.
                                                                                                      
                                                                    OpenModelAttribute                
                                                                                                      
                                                                    -  isInvariant: false             
                                                                                                      
                                                                    -  valueRange: no range constraint
                                                                                                      
                                                                    -  support: MANDATORY             
\_instantiationLevel          InstantiationLevel          1..\*     Preliminary                        Describes the various levels of resources that can be used to instantiate the VNF using this flavour. Examples: Small, Medium, Large. If there is only one "instantiationLevel" entry, it shall be treated as the default instantiation level for this DF.
                                                                                                      
                                                                    OpenModelAttribute                
                                                                                                      
                                                                    -  isInvariant: false             
                                                                                                      
                                                                    -  valueRange: no range constraint
                                                                                                      
                                                                    -  support: MANDATORY             
\_affinityOrAntiAffinityGroup AffinityOrAntiAffinityGroup 0..\*     Preliminary                        Specifies affinity or anti-affinity relationship applicable between the virtualisation containers (e.g. virtual machines) to be created using different VDUs or internal VLs to be created using different VnfVirtualLinkDesc(s) in the same affinity or anti-affinity group. NOTE: In the present specification, including either VDU(s) or VnfVirtualLinkDesc(s) into the same affinity or anti-affinity group is supported. Extension to support including both VDU(s) and VnfVirtualLinkDesc(s) into the same affinity or anti-affinity group is left for future specification.
                                                                                                      
                                                                    OpenModelAttribute                
                                                                                                      
                                                                    -  isInvariant: false             
                                                                                                      
                                                                    -  valueRange: no range constraint
                                                                                                      
                                                                    -  support: MANDATORY             
\_scalingAspect               ScalingAspect               0..\*     Preliminary                        The scaling aspects supported by this DF of the VNF. scalingAspect shall be present if the VNF supports scaling.
                                                                                                      
                                                                    OpenModelAttribute                
                                                                                                      
                                                                    -  isInvariant: false             
                                                                                                      
                                                                    -  valueRange: no range constraint
                                                                                                      
                                                                    -  support: MANDATORY             
\_vduProfile                  VduProfile                  1..\*     Preliminary                        Describes additional instantiation data for the VDUs used in this flavor.
                                                                                                      
                                                                    OpenModelAttribute                
                                                                                                      
                                                                    -  isInvariant: false             
                                                                                                      
                                                                    -  valueRange: no range constraint
                                                                                                      
                                                                    -  support: MANDATORY             
\_placementGroup              PlacementGroup              0..\*     Preliminary                        Determine where VNFC's (VDU's) are placed with respect to the VNF
                                                                                                      
                                                                    OpenModelAttribute                
                                                                                                      
                                                                    -  isInvariant: false             
                                                                                                      
                                                                    -  valueRange: no range constraint
                                                                                                      
                                                                    -  support: MANDATORY             
\_baseConfigGroup             BaseConfigGroup             1         Preliminary                        BaseConfigGroup may set Access Control Lists (ACL's) and establish security groups and server groups. BaseConfigGroup creates/establishs storage for the VM's (OpenStack Cinder). BaseConfigGroup may establish internal networks such as OAM (VNF Mgmt) or MNS (Maintenance & Surveillance) established.
                                                                                                      
                                                                    OpenModelAttribute                
                                                                                                      
                                                                    -  isInvariant: false             
                                                                                                      
                                                                    -  valueRange: no range constraint
                                                                                                      
                                                                    -  support: MANDATORY             
\_deploymentGroup             DeploymentGroup             0..\*     Preliminary                        DeploymentGroup provides the minimum viable VDU and associated VNFC configuration for a useable VNF.
                                                                                                      
                                                                    OpenModelAttribute                
                                                                                                      
                                                                    -  isInvariant: false             
                                                                                                      
                                                                    -  valueRange: no range constraint
                                                                                                      
                                                                    -  support: MANDATORY             
\_scalinggroup                ScalingGroup                0..\*     Preliminary                        Identifies the vaious scaling groups within the VNF which identify which vnfcs that need to be scaled together.
                                                                                                      
                                                                    OpenModelAttribute                
                                                                                                      
                                                                    -  isInvariant: false             
                                                                                                      
                                                                    -  valueRange: no range constraint
                                                                                                      
                                                                    -  support: MANDATORY             
\_vnfIndicator                VnfIndicator                0..\*     Experimental                       Declares the VNF indicators that are supported by this VNF (specific to this DF).
                                                                                                      
                                                                    OpenModelAttribute                
                                                                                                      
                                                                    -  isInvariant: false             
                                                                                                      
                                                                    -  valueRange: no range constraint
                                                                                                      
                                                                    -  support: MANDATORY             
============================= =========================== ========= ================================== ===================================================================================================================================================================================================================================================================================================================================================================================================================================================================================================================================================================================

VnfExtCp
~~~~~~~~

Describes an external CP exposed by a VNF.

**Parent class:** Cp

Applied stereotypes:

-  OpenModelClass

-  **support: MANDATORY**

VnfExtCpd
~~~~~~~~~

A VnfExtCpd is a type of Cpd and describes an external interface, a.k.a external CP, exposed by this VNF enabling connection with a VL. When the VnfExtCpd is mapped to a VduCpd, the values for the attributes type, subType and description shall be identical for both elements.

Applied stereotypes:

-  Reference

-  **reference: IFA011 v2.5.1**

-  Preliminary

-  OpenModelClass

-  **support: MANDATORY**

===================================== =================================== ========= ================================================================== ===================================================================================================================================================================================================================================================================================
**Attribute Name**                    **Type**                            **Mult.** **Stereotypes**                                                    **Description**
===================================== =================================== ========= ================================================================== ===================================================================================================================================================================================================================================================================================
\_virtualNetworkInterfaceRequirements VirtualNetworkInterfaceRequirements 0..\*     Preliminary                                                        Specifies requirements on a virtual network interface realising the CPs instantiated from this CPD. NOTE: In case of referencing an intCpd via its identifier, the virtualNetworkInterfaceRequirements attribute of the referenced intCpd applies.
                                                                                                                                                      
                                                                                    OpenModelAttribute                                                
                                                                                                                                                      
                                                                                    -  isInvariant: false                                             
                                                                                                                                                      
                                                                                    -  valueRange: no range constraint                                
                                                                                                                                                      
                                                                                    -  support: MANDATORY                                             
\_intCpd                              VduCpd                              0..1      Preliminary                                                        A VnfExtCpd is a type of Cpd and describes an external interface, a.k.a external CP, exposed by this VNF enabling connection with a VL. When the VnfExtCpd is mapped to a VduCpd, the values for the attributes type, subType and description shall be identical for both elements.
                                                                                                                                                      
                                                                                    OpenModelAttribute                                                
                                                                                                                                                      
                                                                                    -  isInvariant: false                                             
                                                                                                                                                      
                                                                                    -  valueRange: no range constraint                                
                                                                                                                                                      
                                                                                    -  support: CONDITIONAL_MANDATORY                                 
                                                                                                                                                      
                                                                                    -  condition:Either intVirtualLinkDesc or intCpd shall be present.
                                                                                                                                                      
                                                                                    PassedByReference                                                 
\_intVirtualLinkDesc                  VnfVirtualLinkDesc                  0..1      Experimental                                                      
                                                                                                                                                      
                                                                                    OpenModelAttribute                                                
                                                                                                                                                      
                                                                                    -  isInvariant: false                                             
                                                                                                                                                      
                                                                                    -  valueRange: no range constraint                                
                                                                                                                                                      
                                                                                    -  support: CONDITIONAL_MANDATORY                                 
                                                                                                                                                      
                                                                                    -  condition:Either intVirtualLinkDesc or intCpd shall be present.
                                                                                                                                                      
                                                                                    PassedByReference                                                 
===================================== =================================== ========= ================================================================== ===================================================================================================================================================================================================================================================================================

VnfIndicator
~~~~~~~~~~~~

The VnfIndicator information element defines the indicator the VNF supports.

Applied stereotypes:

-  Reference

-  **reference: IFA011 v2.5.1**

-  Preliminary

-  OpenModelClass

-  **support: MANDATORY**

================== ========== ========= ================================== =====================================================================================================
**Attribute Name** **Type**   **Mult.** **Stereotypes**                    **Description**
================== ========== ========= ================================== =====================================================================================================
id                 Identifier 1         Preliminary                        Unique identifier.
                                                                          
                                        OpenModelAttribute                
                                                                          
                                        -  isInvariant: true              
                                                                          
                                        -  valueRange: no range constraint
                                                                          
                                        -  support: MANDATORY             
name               String     0..1      Preliminary                        The human readable name of the VnfIndicator.
                                                                          
                                        OpenModelAttribute                
                                                                          
                                        -  isInvariant: false             
                                                                          
                                        -  valueRange: no range constraint
                                                                          
                                        -  support: MANDATORY             
indicatorValue     String     1..\*     Preliminary                        Defines the allowed values or value ranges of this indicator.
                                                                          
                                        OpenModelAttribute                
                                                                          
                                        -  isInvariant: false             
                                                                          
                                        -  valueRange: no range constraint
                                                                          
                                        -  support: MANDATORY             
source             VnfSource  1         Preliminary                        Describe the source of the indicator. This tells the consumer where to send the subscription request.
                                                                          
                                        OpenModelAttribute                
                                                                          
                                        -  isInvariant: false             
                                                                          
                                        -  valueRange: no range constraint
                                                                          
                                        -  support: MANDATORY             
================== ========== ========= ================================== =====================================================================================================

VnfProfile
~~~~~~~~~~

The VnfProfile class specifies a profile for instantiating VNFs of a particular NS DF according to a specific VNFD and VNF DF.

**Parent class:** NsOrVnfProfile

Applied stereotypes:

-  OpenModelClass

-  **support: MANDATORY**

-  Future

=============================== ========================= ========= ================================== =====================================================================================================================================================================================================================================================================================================================================================
**Attribute Name**              **Type**                  **Mult.** **Stereotypes**                    **Description**
=============================== ========================= ========= ================================== =====================================================================================================================================================================================================================================================================================================================================================
vnfProfileId                    Identifier                1         OpenModelAttribute                 Identifier of this vnfProfile class. It uniquely identifies a VnfProfile.
                                                                                                      
                                                                    -  isInvariant: false             
                                                                                                      
                                                                    -  valueRange: no range constraint
                                                                                                      
                                                                    -  support: MANDATORY             
instantiationLevel              Identifier                0..1      OpenModelAttribute                 Identifier of the instantiation level of the VNF DF to be used for instantiation. If not present, the default instantiation level as declared in the VNFD shall be used.
                                                                                                      
                                                                    -  isInvariant: false             
                                                                                                      
                                                                    -  valueRange: no range constraint
                                                                                                      
                                                                    -  support: MANDATORY             
minNumberOfInstances            Integer                   1         OpenModelAttribute                 Minimum number of instances of the VNF based on this VNFD that is permitted to exist for this VnfProfile.
                                                                                                      
                                                                    -  isInvariant: false             
                                                                                                      
                                                                    -  valueRange: no range constraint
                                                                                                      
                                                                    -  support: MANDATORY             
maxNumberOfInstances            Integer                   1         OpenModelAttribute                 Maximum number of instances of the VNF based on this VNFD that is permitted to exist for this VnfProfile.
                                                                                                      
                                                                    -  isInvariant: false             
                                                                                                      
                                                                    -  valueRange: no range constraint
                                                                                                      
                                                                    -  support: MANDATORY             
localAffinityOrAntiAffinityRule invalid                   0..\*     OpenModelAttribute                 Specifies affinity and anti-affinity rules applicable between VNF instances created from this profile.
                                                                                                      
                                                                    -  isInvariant: false             
                                                                                                      
                                                                    -  valueRange: no range constraint
                                                                                                      
                                                                    -  support: MANDATORY             
affinityOrAntiAffinityGroupId   invalid                   1         OpenModelAttribute                 Identifier(s) of the affinity or anti-affinity group(s) the VnfProfile belongs to. NOTE: Each identifier references an affinity or anti-affinity group which expresses affinity or anti-affinity relationships between the VNF instance(s) created using this VnfProfile and the VNF instance(s) created using other VnfProfile(s) in the same group.
                                                                                                      
                                                                    -  isInvariant: false             
                                                                                                      
                                                                    -  valueRange: no range constraint
                                                                                                      
                                                                    -  support: MANDATORY             
nsVirtualLinkConnectivity       NsVirtualLinkConnectivity 1..\*     OpenModelAttribute                 Defines the connection information of the VNF, it contains connection relationship between a VNF connection point and a NS virtual Link.
                                                                                                      
                                                                    -  isInvariant: false             
                                                                                                      
                                                                    -  valueRange: no range constraint
                                                                                                      
                                                                    -  support: MANDATORY             
\_vnfDf                         VnfDf                     1         OpenModelAttribute                 Identifies a flavour within the VNFD.
                                                                                                      
                                                                    -  isInvariant: false             
                                                                                                      
                                                                    -  valueRange: no range constraint
                                                                                                      
                                                                    -  support: MANDATORY             
\_vnfd                          Vnfd                      0..1      OpenModelAttribute                 Reference to the VNFD.
                                                                                                      
                                                                    -  isInvariant: false             
                                                                                                      
                                                                    -  valueRange: no range constraint
                                                                                                      
                                                                    -  support: MANDATORY             
=============================== ========================= ========= ================================== =====================================================================================================================================================================================================================================================================================================================================================

VnfVirtualLink
~~~~~~~~~~~~~~

**Parent class:** VirtualLink

Applied stereotypes:

-  OpenModelClass

-  **support: MANDATORY**

VnfVirtualLinkDesc
~~~~~~~~~~~~~~~~~~

Represents the type of network connectivity mandated by the VNF vendor between two or more Connection Points which includes at least one Internal Connection Point.

**Parent class:** VirtualLinkDesc

Applied stereotypes:

-  Reference

-  **reference: IFA011 v2.5.1**

-  Experimental

-  OpenModelClass

-  **support: MANDATORY**

======================== ====================== ========= ================================== ==========================================================================================================================================================================================================================================================================================================================
**Attribute Name**       **Type**               **Mult.** **Stereotypes**                    **Description**
======================== ====================== ========= ================================== ==========================================================================================================================================================================================================================================================================================================================
monitoringParameter      MonitoringParameter    0..\*     Experimental                       Specifies the virtualised resource related performance metrics on VLD level to be tracked by the VNFM.
                                                                                            
                                                          OpenModelAttribute                
                                                                                            
                                                          -  isInvariant: false             
                                                                                            
                                                          -  valueRange: no range constraint
                                                                                            
                                                          -  support: MANDATORY             
\_virtualLinkDescFlavour VirtualLinkDescFlavour 1..\*     Preliminary                        Describes a specific flavour of the VL with specific bitrate requirements.
                                                                                            
                                                          OpenModelAttribute                
                                                                                            
                                                          -  isInvariant: false             
                                                                                            
                                                          -  valueRange: no range constraint
                                                                                            
                                                          -  support: MANDATORY             
virtualLinkDescId        Identifier             1         Preliminary                        Uniquely identifies a VLD in the parent descriptor. For VnfVirtualLinkDesc, the parent descriptor is the VNFD. For NsVirtualLinkDesc, the parent descriptor is the NSD. Note: the description of this class are different in ETSI GS NFV IFA 011 and ETSI GS NFV IFA 014. The present definition merges the 2 definitions.
                                                                                            
                                                          OpenModelAttribute                
                                                                                            
                                                          -  isInvariant: false             
                                                                                            
                                                          -  valueRange: no range constraint
                                                                                            
                                                          -  support: MANDATORY             
connectivityType         ConnectivityType       1         Preliminary                        Specifies the protocol exposed by a VL and the flow pattern supported by the VL.
                                                                                            
                                                          OpenModelAttribute                
                                                                                            
                                                          -  isInvariant: false             
                                                                                            
                                                          -  valueRange: no range constraint
                                                                                            
                                                          -  support: MANDATORY             
description              String                 0..1      Preliminary                        Provides human-readable information on the purpose of the VL (e.g. control plane traffic).
                                                                                            
                                                          OpenModelAttribute                
                                                                                            
                                                          -  isInvariant: false             
                                                                                            
                                                          -  valueRange: no range constraint
                                                                                            
                                                          -  support: MANDATORY             
======================== ====================== ========= ================================== ==========================================================================================================================================================================================================================================================================================================================

Vnfc
~~~~

An internal component of a VNF providing a VNF Provider a defined sub-set of that VNF's functionality, with the main characteristic that a single instance of this component maps 1:1 against a single Virtualisation Container.

Applied stereotypes:

-  Experimental

-  OpenModelClass

-  **support: MANDATORY**

========================== =================== ========= ================================== =======================================================================================================================
**Attribute Name**         **Type**            **Mult.** **Stereotypes**                    **Description**
========================== =================== ========= ================================== =======================================================================================================================
vnfcInstanceId             Identifier          1         Experimental                       identifier of the NFC instance
                                                                                           
                                                         OpenModelAttribute                
                                                                                           
                                                         -  isInvariant: false             
                                                                                           
                                                         -  valueRange: no range constraint
                                                                                           
                                                         -  support: MANDATORY             
nfcNamingCode              String              0..1      Experimental                       short code of the NFC instance
                                                                                           
                                                         OpenModelAttribute                
                                                                                           
                                                         -  isInvariant: false             
                                                                                           
                                                         -  valueRange: no range constraint
                                                                                           
                                                         -  support: MANDATORY             
description                invalid             0..1      Experimental                       description of the NFC instance
                                                                                           
                                                         OpenModelAttribute                
                                                                                           
                                                         -  isInvariant: false             
                                                                                           
                                                         -  valueRange: no range constraint
                                                                                           
                                                         -  support: MANDATORY             
vdudId                     Identifier          1         Experimental                       identifier of the model of the NFC instance
                                                                                           
                                                         OpenModelAttribute                
                                                                                           
                                                         -  isInvariant: false             
                                                                                           
                                                         -  valueRange: no range constraint
                                                                                           
                                                         -  support: MANDATORY             
l3InterfaceIpv4AddressList invalid             0..\*     Experimental                       layer-3 interface addresses, ipv4
                                                                                           
                                                         OpenModelAttribute                
                                                                                           
                                                         -  isInvariant: false             
                                                                                           
                                                         -  valueRange: no range constraint
                                                                                           
                                                         -  support: MANDATORY             
l3InterfaceIpv6AddressList invalid             0..\*     Experimental                       layer-3 interface addresses, ipv6
                                                                                           
                                                         OpenModelAttribute                
                                                                                           
                                                         -  isInvariant: false             
                                                                                           
                                                         -  valueRange: no range constraint
                                                                                           
                                                         -  support: MANDATORY             
vnfcState                  invalid             0..1      Experimental                       operating status of the VM valid value example: STARTED (POWER_ON), STOPPED (POWER_OFF)
                                                                                           
                                                         OpenModelAttribute                
                                                                                           
                                                         -  isInvariant: false             
                                                                                           
                                                         -  valueRange: no range constraint
                                                                                           
                                                         -  support: MANDATORY             
inMaint                    Boolean             0..1      Experimental                       whether the NFC instance is in maintenance mode, if yes, DCAE will not observe alarms/traps, etc.
                                                                                           
                                                         OpenModelAttribute                
                                                                                           
                                                         -  isInvariant: false             
                                                                                           
                                                         -  valueRange: no range constraint
                                                                                           
                                                         -  support: MANDATORY             
isClosedLoopDisabled       Boolean             0..1      Experimental                       whether closed loop function is enabled
                                                                                           
                                                         OpenModelAttribute                
                                                                                           
                                                         -  isInvariant: false             
                                                                                           
                                                         -  valueRange: no range constraint
                                                                                           
                                                         -  support: MANDATORY             
vnfcInstanceName           String              1..\*     Experimental                       An intelligent or human readable name of the vnfc instance. Multiple names are possible.
                                                                                           
                                                         OpenModelAttribute                
                                                                                           
                                                         -  isInvariant: false             
                                                                                           
                                                         -  valueRange: no range constraint
                                                                                           
                                                         -  support: MANDATORY             
\_vnfcCp                   VnfcCp              1..\*     Experimental                       Reference to the connection points of the vnfc
                                                                                           
                                                         OpenModelAttribute                
                                                                                           
                                                         -  isInvariant: false             
                                                                                           
                                                         -  valueRange: no range constraint
                                                                                           
                                                         -  support: MANDATORY             
vnfcNamingPolicyId         String              1         Experimental                       Identifier of the policy which has the naming logic for this VNFC instance
                                                                                           
                                                         OpenModelAttribute                
                                                                                           
                                                         -  isInvariant: false             
                                                                                           
                                                         -  valueRange: no range constraint
                                                                                           
                                                         -  support: MANDATORY             
nfcFunction                String              1         Experimental                       English description of network function component that the specific VNFC deployment is providing.
                                                                                           
                                                         OpenModelAttribute                
                                                                                           
                                                         -  isInvariant: false             
                                                                                           
                                                         -  valueRange: no range constraint
                                                                                           
                                                         -  support: MANDATORY             
operationalStatus          OperationalStatus   1         Experimental                       indicator for whether the resource is considered operational. Valid values are in-service-path and out-of-service-path.
                                                                                           
                                                         OpenModelAttribute                
                                                                                           
                                                         -  isInvariant: false             
                                                                                           
                                                         -  valueRange: no range constraint
                                                                                           
                                                         -  support: MANDATORY             
orchestrationStatus        OrchestrationStatus 1         Experimental                       whether the VNFC instance is instantiated
                                                                                           
                                                         OpenModelAttribute                
                                                                                           
                                                         -  isInvariant: false             
                                                                                           
                                                         -  valueRange: no range constraint
                                                                                           
                                                         -  support: MANDATORY             
closedLoopStatus           invalid             1         Experimental                       Whether closed loop capabilities are enabled for this or not.
                                                                                           
                                                         OpenModelAttribute                
                                                                                           
                                                         -  isInvariant: false             
                                                                                           
                                                         -  valueRange: no range constraint
                                                                                           
                                                         -  support: MANDATORY             
\_vdu                      Vdu                 1         Experimental                       Reference to the VDU
                                                                                           
                                                         OpenModelAttribute                
                                                                                           
                                                         -  isInvariant: false             
                                                                                           
                                                         -  valueRange: no range constraint
                                                                                           
                                                         -  support: MANDATORY             
========================== =================== ========= ================================== =======================================================================================================================

VnfcCp
~~~~~~

**Parent class:** Cp

Applied stereotypes:

-  Experimental

-  OpenModelClass

-  **support: MANDATORY**

Vnfd
~~~~

A Vnfd, or VNF Descriptor, is template which describes a VNF in terms of deployment and operational behaviour requirements. It also contains connectivity, interface and virtualised resource requirements.

**Parent class:** NetworkFunctionDesc

Applied stereotypes:

-  Reference

-  **reference: IFA011 v2.5.1**

-  Preliminary

-  OpenModelClass

-  **support: MANDATORY**

=========================== ============================ ========= ================================================================================================= ================================================================================================================================================================================================================================================================================================================
**Attribute Name**          **Type**                     **Mult.** **Stereotypes**                                                                                   **Description**
=========================== ============================ ========= ================================================================================================= ================================================================================================================================================================================================================================================================================================================
vnfProvider                 String                       1         Preliminary                                                                                       Provider of the VNF and of the VNFD.
                                                                                                                                                                    
                                                                   OpenModelAttribute                                                                               
                                                                                                                                                                    
                                                                   -  isInvariant: false                                                                            
                                                                                                                                                                    
                                                                   -  valueRange: no range constraint                                                               
                                                                                                                                                                    
                                                                   -  support: MANDATORY                                                                            
vnfProductName              String                       1         Preliminary                                                                                       Name to identify the VNF Product. Invariant for the VNF Product lifetime.
                                                                                                                                                                    
                                                                   OpenModelAttribute                                                                               
                                                                                                                                                                    
                                                                   -  isInvariant: true                                                                             
                                                                                                                                                                    
                                                                   -  valueRange: no range constraint                                                               
                                                                                                                                                                    
                                                                   -  support: MANDATORY                                                                            
vnfSoftwareVersion          Version                      1         Preliminary                                                                                       Software version of the VNF. This is changed when there is any change to the software that is included in the VNF Package.
                                                                                                                                                                    
                                                                   OpenModelAttribute                                                                               
                                                                                                                                                                    
                                                                   -  isInvariant: false                                                                            
                                                                                                                                                                    
                                                                   -  valueRange: no range constraint                                                               
                                                                                                                                                                    
                                                                   -  support: MANDATORY                                                                            
vnfdVersion                 Version                      1         Preliminary                                                                                       Identifies the version of the VNFD.
                                                                                                                                                                    
                                                                   OpenModelAttribute                                                                               
                                                                                                                                                                    
                                                                   -  isInvariant: false                                                                            
                                                                                                                                                                    
                                                                   -  valueRange: no range constraint                                                               
                                                                                                                                                                    
                                                                   -  support: MANDATORY                                                                            
vnfProductInfoName          String                       0..1      Preliminary                                                                                       Human readable name for the VNF Product. Can change during the VNF Product lifetime.
                                                                                                                                                                    
                                                                   OpenModelAttribute                                                                               
                                                                                                                                                                    
                                                                   -  isInvariant: false                                                                            
                                                                                                                                                                    
                                                                   -  valueRange: no range constraint                                                               
                                                                                                                                                                    
                                                                   -  support: MANDATORY                                                                            
vnfProductInfoDescription   String                       0..1      Preliminary                                                                                       Human readable description of the VNF Product. Can change during the VNF Product lifetime.
                                                                                                                                                                    
                                                                   OpenModelAttribute                                                                               
                                                                                                                                                                    
                                                                   -  isInvariant: false                                                                            
                                                                                                                                                                    
                                                                   -  valueRange: no range constraint                                                               
                                                                                                                                                                    
                                                                   -  support: MANDATORY                                                                            
vnfmInfo                    String                       0..\*     Preliminary                                                                                       Identifies VNFM(s) compatible with the VNF described in this version of the VNFD. Use the name of micro-service of the vnfm drive. For vendor specific VNFM, the value composes of "vendorname" and "vnfmdriver", e.g. "mycompanyvnfmdriver"; for generic VNFM, the value is "gvnfmdriver".
                                                                                                                                                                    
                                                                   OpenModelAttribute                                                                               
                                                                                                                                                                    
                                                                   -  isInvariant: false                                                                            
                                                                                                                                                                    
                                                                   -  valueRange: no range constraint                                                               
                                                                                                                                                                    
                                                                   -  support: MANDATORY                                                                            
localizationLanguage        String                       0..\*     Preliminary                                                                                       Information about localization languages of the VNF (includes e.g. strings in the VNFD). Refer to ISO936 https://www.iso.org/iso-639-language-codes.html NOTE: This allows to provide one or more localization languages to support selecting a specific localization language at VNF instantiation time.
                                                                                                                                                                    
                                                                   OpenModelAttribute                                                                               
                                                                                                                                                                    
                                                                   -  isInvariant: false                                                                            
                                                                                                                                                                    
                                                                   -  valueRange: no range constraint                                                               
                                                                                                                                                                    
                                                                   -  support: MANDATORY                                                                            
modifiableAttributes        VnfInfoModifiableAttributes  0..1      Preliminary                                                                                       Defines the VNF-specific extension and metadata attributes of the VnfInfo that are writeable via the ModifyVnfInfo operation.
                                                                                                                                                                    
                                                                   OpenModelAttribute                                                                               
                                                                                                                                                                    
                                                                   -  isInvariant: false                                                                            
                                                                                                                                                                    
                                                                   -  valueRange: no range constraint                                                               
                                                                                                                                                                    
                                                                   -  support: MANDATORY                                                                            
vnfdId                      Identifier                   1         Preliminary                                                                                       Identifier of this VNFD information element. This attribute shall be globally unique. NOTE: The VNFD Identifier shall be used as the unique identifier of the VNF Package that contains this VNFD. Any modification of the content of the VNFD or the VNF Package shall result in a new VNFD Identifier.
                                                                                                                                                                    
                                                                   OpenModelAttribute                                                                               
                                                                                                                                                                    
                                                                   -  isInvariant: true                                                                             
                                                                                                                                                                    
                                                                   -  valueRange: no range constraint                                                               
                                                                                                                                                                    
                                                                   -  support: MANDATORY                                                                            
defaultLocalizationLanguage String                       0..1      Preliminary                                                                                       Information about localization languages of the VNF (includes e.g. strings in the VNFD). Refer to ISO936 https://www.iso.org/iso-639-language-codes.html NOTE: This allows to provide one or more localization languages to support selecting a specific localization language at VNF instantiation time.
                                                                                                                                                                    
                                                                   OpenModelAttribute                                                                               
                                                                                                                                                                    
                                                                   -  isInvariant: false                                                                            
                                                                                                                                                                    
                                                                   -  valueRange: no range constraint                                                               
                                                                                                                                                                    
                                                                   -  support: CONDITIONAL_MANDATORY                                                                
                                                                                                                                                                    
                                                                   -  condition:Shall be present if "localizationLanguage" is present and shall be absent otherwise.
configurableProperties      VnfConfigurableProperties    0..1      Preliminary                                                                                       Describes the configurable properties of the VNF (e.g. related to auto scaling and auto healing).
                                                                                                                                                                    
                                                                   OpenModelAttribute                                                                               
                                                                                                                                                                    
                                                                   -  isInvariant: false                                                                            
                                                                                                                                                                    
                                                                   -  valueRange: no range constraint                                                               
                                                                                                                                                                    
                                                                   -  support: MANDATORY                                                                            
lifecycleManagementScript   VnfLifecycleManagementScript 0..\*     Preliminary                                                                                       Includes a list of events and corresponding management scripts performed for the VNF.
                                                                                                                                                                    
                                                                   OpenModelAttribute                                                                               
                                                                                                                                                                    
                                                                   -  isInvariant: false                                                                            
                                                                                                                                                                    
                                                                   -  valueRange: no range constraint                                                               
                                                                                                                                                                    
                                                                   -  support: MANDATORY                                                                            
logo                        String                       0..1      Preliminary                                                                                       File path of the vendor specified logo.
                                                                                                                                                                    
                                                                   OpenModelAttribute                                                                               
                                                                                                                                                                    
                                                                   -  isInvariant: false                                                                            
                                                                                                                                                                    
                                                                   -  valueRange: no range constraint                                                               
                                                                                                                                                                    
                                                                   -  support: MANDATORY                                                                            
guide                       String                       0..1      Preliminary                                                                                       UUID of the vendor guide/documentation which is attached to VNF and can be downloaded from the model.
                                                                                                                                                                    
                                                                   OpenModelAttribute                                                                               
                                                                                                                                                                    
                                                                   -  isInvariant: false                                                                            
                                                                                                                                                                    
                                                                   -  valueRange: no range constraint                                                               
                                                                                                                                                                    
                                                                   -  support: MANDATORY                                                                            
\_vdu                       Vdu                          1..\*     Preliminary                                                                                       Virtualisation Deployment Unit.
                                                                                                                                                                    
                                                                   OpenModelAttribute                                                                               
                                                                                                                                                                    
                                                                   -  isInvariant: false                                                                            
                                                                                                                                                                    
                                                                   -  valueRange: no range constraint                                                               
                                                                                                                                                                    
                                                                   -  support: MANDATORY                                                                            
\_vnfExtCpd                 VnfExtCpd                    1..\*     Preliminary                                                                                       Describes external interface(s) exposed by this VNF enabling connection with a VL.
                                                                                                                                                                    
                                                                   OpenModelAttribute                                                                               
                                                                                                                                                                    
                                                                   -  isInvariant: false                                                                            
                                                                                                                                                                    
                                                                   -  valueRange: no range constraint                                                               
                                                                                                                                                                    
                                                                   -  support: MANDATORY                                                                            
\_deploymentFlavour         VnfDf                        1..\*     Preliminary                                                                                       Describes specific DF(s) of a VNF with specific requirements for capacity and performance.
                                                                                                                                                                    
                                                                   OpenModelAttribute                                                                               
                                                                                                                                                                    
                                                                   -  isInvariant: false                                                                            
                                                                                                                                                                    
                                                                   -  valueRange: no range constraint                                                               
                                                                                                                                                                    
                                                                   -  support: MANDATORY                                                                            
\_vnfIndicator              VnfIndicator                 0..\*     Preliminary                                                                                       Declares the VNF indicators that are supported by this VNF.
                                                                                                                                                                    
                                                                   OpenModelAttribute                                                                               
                                                                                                                                                                    
                                                                   -  isInvariant: false                                                                            
                                                                                                                                                                    
                                                                   -  valueRange: no range constraint                                                               
                                                                                                                                                                    
                                                                   -  support: MANDATORY                                                                            
\_virtualComputeDesc        VirtualComputeDesc           0..\*     Preliminary                                                                                       Defines descriptors of virtual compute resources to be used by the VNF.
                                                                                                                                                                    
                                                                   OpenModelAttribute                                                                               
                                                                                                                                                                    
                                                                   -  isInvariant: false                                                                            
                                                                                                                                                                    
                                                                   -  valueRange: no range constraint                                                               
                                                                                                                                                                    
                                                                   -  support: MANDATORY                                                                            
\_virtualStorageDesc        VirtualStorageDesc           0..\*     Preliminary                                                                                       Defines descriptors of virtual storage resources to be used by the VNF.
                                                                                                                                                                    
                                                                   OpenModelAttribute                                                                               
                                                                                                                                                                    
                                                                   -  isInvariant: false                                                                            
                                                                                                                                                                    
                                                                   -  valueRange: no range constraint                                                               
                                                                                                                                                                    
                                                                   -  support: MANDATORY                                                                            
\_vnfReservedCpd            VduCpd                       0..\*     Preliminary                                                                                       Reserved IP Address for VNF which is not bounded to any specific VNFC, but assigned manually from outside and potentially shared as a floating IP among VNFCs.
                                                                                                                                                                    
                                                                   OpenModelAttribute                                                                               
                                                                                                                                                                    
                                                                   -  isInvariant: false                                                                            
                                                                                                                                                                    
                                                                   -  valueRange: no range constraint                                                               
                                                                                                                                                                    
                                                                   -  support: MANDATORY                                                                            
\_elementGroup              VnfdElementGroup             0..\*     Obsolete                                                                                          Describes the associated elements of a VNFD for a certain purpose during VNF lifecycle management.
                                                                                                                                                                    
                                                                   OpenModelAttribute                                                                               
                                                                                                                                                                    
                                                                   -  isInvariant: false                                                                            
                                                                                                                                                                    
                                                                   -  valueRange: no range constraint                                                               
                                                                                                                                                                    
                                                                   -  support: MANDATORY                                                                            
\_swImageDesc               SwImageDesc                  0..\*     Preliminary                                                                                       Defines descriptors of software images to be used by the VNF. NOTE: This shall be used to describe both the software image loaded on the virtualization container used to realize a VDU and the software images to be stored on VirtualStorage resources (e.g., volumes) attached to a virtualization container.
                                                                                                                                                                    
                                                                   OpenModelAttribute                                                                               
                                                                                                                                                                    
                                                                   -  isInvariant: false                                                                            
                                                                                                                                                                    
                                                                   -  valueRange: no range constraint                                                               
                                                                                                                                                                    
                                                                   -  support: MANDATORY                                                                            
\_intVirtualLinkDesc        VnfVirtualLinkDesc           0..\*     Preliminary                                                                                       Represents the type of network connectivity mandated by the VNF provider between two or more CPs which includes at least one internal CP.
                                                                                                                                                                    
                                                                   OpenModelAttribute                                                                               
                                                                                                                                                                    
                                                                   -  isInvariant: false                                                                            
                                                                                                                                                                    
                                                                   -  valueRange: no range constraint                                                               
                                                                                                                                                                    
                                                                   -  support: MANDATORY                                                                            
\_securityGroupRule         SecurityGroupRule            0..\*     Experimental                                                                                      Defines security group rules to be used by the VNF.
                                                                                                                                                                    
                                                                   OpenModelAttribute                                                                               
                                                                                                                                                                    
                                                                   -  isInvariant: false                                                                            
                                                                                                                                                                    
                                                                   -  valueRange: no range constraint                                                               
                                                                                                                                                                    
                                                                   -  support: MANDATORY                                                                            
=========================== ============================ ========= ================================================================================================= ================================================================================================================================================================================================================================================================================================================

VnfdElementGroup
~~~~~~~~~~~~~~~~

A VNFD Element Group is a mechanism for associating elements of a VNFD (Vdus and VnfVirtualLinkDesc(s)) for a certain purpose, for example, scaling aspects. A given element can belong to multiple groups.

Applied stereotypes:

-  Preliminary

-  Obsolete

-  OpenModelClass

-  **support: MANDATORY**

==================== ========== ========= ================================== =============================================================
**Attribute Name**   **Type**   **Mult.** **Stereotypes**                    **Description**
==================== ========== ========= ================================== =============================================================
vnfdElementGroupId   Identifier 1         Preliminary                        Unique identifier of this group in the VNFD.
                                                                            
                                          OpenModelAttribute                
                                                                            
                                          -  isInvariant: false             
                                                                            
                                          -  valueRange: no range constraint
                                                                            
                                          -  support: MANDATORY             
description          String     1         Preliminary                        Human readable description of the group.
                                                                            
                                          OpenModelAttribute                
                                                                            
                                          -  isInvariant: false             
                                                                            
                                          -  valueRange: no range constraint
                                                                            
                                          -  support: MANDATORY             
\_vdu                Vdu        0..\*     Preliminary                        References to Vdus that are part of this group.
                                                                            
                                          OpenModelAttribute                
                                                                            
                                          -  isInvariant: false             
                                                                            
                                          -  valueRange: no range constraint
                                                                            
                                          -  support: MANDATORY             
\_vnfVirtualLinkdesc            0..\*     Preliminary                        References to VnfVirtualLinkDesc that are part of this group.
                                                                            
                                          OpenModelAttribute                
                                                                            
                                          -  isInvariant: false             
                                                                            
                                          -  valueRange: no range constraint
                                                                            
                                          -  support: MANDATORY             
==================== ========== ========= ================================== =============================================================

Vnffg
~~~~~

A graph of logical links connecting NF nodes,where at least one node is a VNF, for the purpose of describing traffic flow between these network functions

Applied stereotypes:

-  OpenModelClass

-  **support: MANDATORY**

-  Future

================== ======== ========= ================================== ==========================================================================================================================================================================================================
**Attribute Name** **Type** **Mult.** **Stereotypes**                    **Description**
================== ======== ========= ================================== ==========================================================================================================================================================================================================
vnffgId            invalid  1         OpenModelAttribute                 Identier of this Vnffg class.
                                                                        
                                      -  isInvariant: false             
                                                                        
                                      -  valueRange: no range constraint
                                                                        
                                      -  support: MANDATORY             
nfId               invalid  1         OpenModelAttribute                 Identifier of the constituent NFs of the VNFFG
                                                                        
                                      -  isInvariant: false             
                                                                        
                                      -  valueRange: no range constraint
                                                                        
                                      -  support: MANDATORY             
virtualLinkId      invalid  1..\*     OpenModelAttribute                 Identifier(s) of the constituent VL instance(s) of the VNFFG.
                                                                        
                                      -  isInvariant: false             
                                                                        
                                      -  valueRange: no range constraint
                                                                        
                                      -  support: MANDATORY             
cpId               invalid  1         OpenModelAttribute                 Identifiers of the CP instances attached to the constituent VNFs and PNFs or the sap instances of the VNFFG. NOTE: It indicates an exhaustive list of all the CP instances and SAP instances of the VNFFG.
                                                                        
                                      -  isInvariant: false             
                                                                        
                                      -  valueRange: no range constraint
                                                                        
                                      -  support: MANDATORY             
nfp                invalid  1         OpenModelAttribute                 Information on the NFPs of this VNFFG.
                                                                        
                                      -  isInvariant: false             
                                                                        
                                      -  valueRange: no range constraint
                                                                        
                                      -  support: MANDATORY             
================== ======== ========= ================================== ==========================================================================================================================================================================================================

Vnffgd
~~~~~~

The Vnffgd class specifies a topology of connectivity of a NS and optionally forwarding rules applicable to the traffic conveyed over this topology.

Applied stereotypes:

-  Experimental

-  OpenModelClass

-  **support: MANDATORY**

================== ========== ========= ================================== =============================================================================================================================================================================================================================================================================================================================================================================================================================================
**Attribute Name** **Type**   **Mult.** **Stereotypes**                    **Description**
================== ========== ========= ================================== =============================================================================================================================================================================================================================================================================================================================================================================================================================================
vnffgdId           Identifier 1         Experimental                       Identifier of this Vnffgd information element. It uniquely identifies a VNFFGD.
                                                                          
                                        OpenModelAttribute                
                                                                          
                                        -  isInvariant: false             
                                                                          
                                        -  valueRange: no range constraint
                                                                          
                                        -  support: MANDATORY             
vnfdId             Vnfd       1..\*     OpenModelAttribute                 References the VNFD of a constituent VNF. NOTE 1: The list of constituent VNFs, PNFs, and nested NS SAPs of a VNFFG can be identical to the list of constituent VNFs, PNFs and nested NSs of the parent NSD, or can be a subset of it. NOTE 2: The presence of a VNFD or PNFD identifier in a VNFFGD does not imply that all connection points instantiated from all embedded CPDs are connected to the VNFFG instantiated using the VNFFGD.
                                                                          
                                        -  isInvariant: false             
                                                                          
                                        -  valueRange: no range constraint
                                                                          
                                        -  support: MANDATORY             
cpdPoolId          CpdPool    1..\*     OpenModelAttribute                 A reference to a pool of descriptors of connection points attached to one of the constituent VNFs and PNFs and/or one of the SAPs of the parent NS or of a nested NS.
                                                                          
                                        -  isInvariant: false             
                                                                          
                                        -  valueRange: no range constraint
                                                                          
                                        -  support: MANDATORY             
nfpd               Nfpd       0..\*     OpenModelAttribute                 The network forwarding path associated to the VNFFG.
                                                                          
                                        -  isInvariant: false             
                                                                          
                                        -  valueRange: no range constraint
                                                                          
                                        -  support: MANDATORY             
\_pnfd             Pnfd       0..\*     OpenModelAttribute                 References the PNFD of a constituent PNF. NOTE 1 : The list of constituent VNFs, PNFs, and nested NS SAPs of a VNFFG can be identical to the list of constituent VNFs, PNFs and nested NSs of the parent NSD, or can be a subset of it. NOTE 2: The presence of a VNFD or PNFD identifier in a VNFFGD does not imply that all connection points instantiated from all embedded CPDs are connected to the VNFFG instantiated using the VNFFGD.
                                                                          
                                        -  isInvariant: false             
                                                                          
                                        -  valueRange: no range constraint
                                                                          
                                        -  support: MANDATORY             
================== ========== ========= ================================== =============================================================================================================================================================================================================================================================================================================================================================================================================================================

Data Types
----------

BlockStorageData
~~~~~~~~~~~~~~~~

Specifies the details of the block storage resource.

Applied stereotypes:

-  Reference

-  **reference: IFA011 v2.5.1**

-  Preliminary

====================== ============ ========= ========== ================================== =================================================================================================================================================
**Attribute Name**     **Type**     **Mult.** **Access** **Stereotypes**                    **Description**
====================== ============ ========= ========== ================================== =================================================================================================================================================
sizeOfStorage          Number       1         RW         Preliminary                        Size of virtualised storage resource in GB.
                                                                                           
                                                         OpenModelAttribute                
                                                                                           
                                                         -  isInvariant: false             
                                                                                           
                                                         -  valueRange: no range constraint
                                                                                           
                                                         -  support: MANDATORY             
vduStorageRequirements KeyValuePair 0..\*     RW         Preliminary                        An array of key-value pairs that articulate the storage deployment requirements.
                                                                                           
                                                         OpenModelAttribute                
                                                                                           
                                                         -  isInvariant: false             
                                                                                           
                                                         -  valueRange: no range constraint
                                                                                           
                                                         -  support: MANDATORY             
rdmaEnabled            Boolean      0..1      RW         Obsolete                           Indicates if the storage supports rdma.
                                                                                           
                                                         OpenModelAttribute                
                                                                                           
                                                         -  isInvariant: false             
                                                                                           
                                                         -  valueRange: no range constraint
                                                                                           
                                                         -  support: MANDATORY             
swImageDesc            SwImageDesc  0..1      RW         Preliminary                        Software image to be loaded on the VirtualStorage resource created based on this VirtualStorageDesc. Shall be absent when used for virtual disks.
                                                                                           
                                                         OpenModelAttribute                
                                                                                           
                                                         -  isInvariant: false             
                                                                                           
                                                         -  valueRange: no range constraint
                                                                                           
                                                         -  support: MANDATORY             
====================== ============ ========= ========== ================================== =================================================================================================================================================

FileStorageData
~~~~~~~~~~~~~~~

The FileStorageData information element specifies the details of file storage resource.

Applied stereotypes:

-  Reference

-  **reference: IFA011 v2.5.1**

-  Preliminary

================== ================== ========= ========== ================================== ============================================================================================================================
**Attribute Name** **Type**           **Mult.** **Access** **Stereotypes**                    **Description**
================== ================== ========= ========== ================================== ============================================================================================================================
sizeOfStorage      Number             1         RW         Preliminary                        Size of virtualised storage resource in GB.
                                                                                             
                                                           OpenModelAttribute                
                                                                                             
                                                           -  isInvariant: false             
                                                                                             
                                                           -  valueRange: no range constraint
                                                                                             
                                                           -  support: MANDATORY             
fileSystemProtocol String             1         RW         Preliminary                        The shared file system protocol (e.g. NFS, CIFS).
                                                                                             
                                                           OpenModelAttribute                
                                                                                             
                                                           -  isInvariant: false             
                                                                                             
                                                           -  valueRange: no range constraint
                                                                                             
                                                           -  support: MANDATORY             
intVirtualLinkDesc VnfVirtualLinkDesc 1         RW         Preliminary                        Reference of the internal VLD which this file storage connects to. The attached VDUs shall connect to the same internal VLD.
                                                                                             
                                                           OpenModelAttribute                
                                                                                             
                                                           -  isInvariant: false             
                                                                                             
                                                           -  valueRange: no range constraint
                                                                                             
                                                           -  support: MANDATORY             
                                                                                             
                                                           PassedByReference                 
================== ================== ========= ========== ================================== ============================================================================================================================

MonitoringParameter
~~~~~~~~~~~~~~~~~~~

Specifies the virtualized resource related performance metric to be tracked by the VNFM, e.g. for auto-scaling purposes. The VNFM collects the values of performance metrics identified by this information element from the VIM(s) using one or more locally initiated PM Jobs. These values can be used as inputs to auto-scaling rules.

Applied stereotypes:

-  Reference

-  **reference: IFA011 v2.5.1**

-  Preliminary

=============================== =============================== ========= ========== ================================== ==========================================================================================================================================================================================================================================================================================================================================================================================================================================
**Attribute Name**              **Type**                        **Mult.** **Access** **Stereotypes**                    **Description**
=============================== =============================== ========= ========== ================================== ==========================================================================================================================================================================================================================================================================================================================================================================================================================================
id                              Identifier                      1         RW         Preliminary                        Unique identifier of the monitoring parameter.
                                                                                                                       
                                                                                     OpenModelAttribute                
                                                                                                                       
                                                                                     -  isInvariant: false             
                                                                                                                       
                                                                                     -  valueRange: no range constraint
                                                                                                                       
                                                                                     -  support: MANDATORY             
name                            String                          0..1      RW         Preliminary                        Human readable name of the monitoring parameter.
                                                                                                                       
                                                                                     OpenModelAttribute                
                                                                                                                       
                                                                                     -  isInvariant: false             
                                                                                                                       
                                                                                     -  valueRange: no range constraint
                                                                                                                       
                                                                                     -  support: MANDATORY             
performanceMetric               String                          1         RW         Preliminary                        Identifies the virtualized resource performance metric.
                                                                                                                       
                                                                                     OpenModelAttribute                
                                                                                                                       
                                                                                     -  isInvariant: false             
                                                                                                                       
                                                                                     -  valueRange: no range constraint
                                                                                                                       
                                                                                     -  support: MANDATORY             
collectionPeriod                CollectionPeriod                0..1      RW         Preliminary                        An attribute that describes the recommended periodicity at which to collect the performance information. VNFM determines if this parameter is considered. The vendor may provide this information as a guidance for creating PmJobs if needed. NOTE: The MANO or NFVI may not support the recommended collectionPeriod based on their functionalities, and can reject the requests based on the recommended collectionPeriod in this case.
                                                                                                                       
                                                                                     OpenModelAttribute                
                                                                                                                       
                                                                                     -  isInvariant: false             
                                                                                                                       
                                                                                     -  valueRange: no range constraint
                                                                                                                       
                                                                                     -  support: MANDATORY             
localAffinityOrAntiAffinityRule LocalAffinityOrAntiAffinityRule 0..1      RW         OpenModelAttribute                
                                                                                                                       
                                                                                     -  isInvariant: false             
                                                                                                                       
                                                                                     -  valueRange: no range constraint
                                                                                                                       
                                                                                     -  support: MANDATORY             
                                                                                                                       
                                                                                     Future                            
=============================== =============================== ========= ========== ================================== ==========================================================================================================================================================================================================================================================================================================================================================================================================================================

ObjectStorageData
~~~~~~~~~~~~~~~~~

The ObjectStorageData information element specifies the details of object storage resource.

Applied stereotypes:

-  Reference

-  **reference: IFA011 v2.5.1**

-  Preliminary

================== ======== ========= ========== ================================== ===============================================
**Attribute Name** **Type** **Mult.** **Access** **Stereotypes**                    **Description**
================== ======== ========= ========== ================================== ===============================================
maxSizeOfStorage   Number   0..1      RW         Preliminary                        Max size of virtualised storage resource in GB.
                                                                                   
                                                 OpenModelAttribute                
                                                                                   
                                                 -  isInvariant: false             
                                                                                   
                                                 -  valueRange: no range constraint
                                                                                   
                                                 -  support: MANDATORY             
================== ======== ========= ========== ================================== ===============================================

RequestedAdditionalCapabilityData
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

This information element describes requested additional capability for a particular VDU. Such a capability may be for acceleration or specific tasks.

Applied stereotypes:

-  Obsolete

============================================= ============ ========= ========== ================================== ============================================================================================
**Attribute Name**                            **Type**     **Mult.** **Access** **Stereotypes**                    **Description**
============================================= ============ ========= ========== ================================== ============================================================================================
supportMandatory                              Boolean      1         RW         Obsolete                           Indicates whether the requested additional capability is mandatory for successful operation.
                                                                                                                  
                                                                                OpenModelAttribute                
                                                                                                                  
                                                                                -  isInvariant: false             
                                                                                                                  
                                                                                -  valueRange: no range constraint
                                                                                                                  
                                                                                -  support: MANDATORY             
requestedAdditionalCapabilityName             String       1         RW         Obsolete                           Identifies a requested additional capability for the VDU.
                                                                                                                  
                                                                                OpenModelAttribute                
                                                                                                                  
                                                                                -  isInvariant: false             
                                                                                                                  
                                                                                -  valueRange: no range constraint
                                                                                                                  
                                                                                -  support: MANDATORY             
minRequestedAdditionalCapabilityVersion       String       0..1      RW         Obsolete                           Identifies the minimum version of the requested additional capability.
                                                                                                                  
                                                                                OpenModelAttribute                
                                                                                                                  
                                                                                -  isInvariant: false             
                                                                                                                  
                                                                                -  valueRange: no range constraint
                                                                                                                  
                                                                                -  support: MANDATORY             
preferredRequestedAdditionalCapabilityVersion String       0..1      RW         Obsolete                           Identifies the preferred version of the requested additional capability.
                                                                                                                  
                                                                                OpenModelAttribute                
                                                                                                                  
                                                                                -  isInvariant: false             
                                                                                                                  
                                                                                -  valueRange: no range constraint
                                                                                                                  
                                                                                -  support: MANDATORY             
targetPerformanceParameters                   KeyValuePair 1..\*     RW         Obsolete                           Identifies specific attributes, dependent on the requested additional capability type.
                                                                                                                  
                                                                                OpenModelAttribute                
                                                                                                                  
                                                                                -  isInvariant: false             
                                                                                                                  
                                                                                -  valueRange: no range constraint
                                                                                                                  
                                                                                -  support: MANDATORY             
============================================= ============ ========= ========== ================================== ============================================================================================

ScaleInfo
~~~~~~~~~

The ScaleInfo information element represents a scale level for a particular scaling aspect.

Applied stereotypes:

-  Reference

-  **reference: IFA011 v2.5.1**

-  Preliminary

================== ============= ========= ========== ================================== ===========================================
**Attribute Name** **Type**      **Mult.** **Access** **Stereotypes**                    **Description**
================== ============= ========= ========== ================================== ===========================================
aspectId           ScalingAspect 1         RW         Preliminary                        Reference to the scaling aspect.
                                                                                        
                                                      OpenModelAttribute                
                                                                                        
                                                      -  isInvariant: false             
                                                                                        
                                                      -  valueRange: no range constraint
                                                                                        
                                                      -  support: MANDATORY             
                                                                                        
                                                      PassedByReference                 
scaleLevel         Integer       1         RW         Preliminary                        The scale level, greater than or equal to 0
                                                                                        
                                                      OpenModelAttribute                
                                                                                        
                                                      -  isInvariant: false             
                                                                                        
                                                      -  valueRange: no range constraint
                                                                                        
                                                      -  support: MANDATORY             
================== ============= ========= ========== ================================== ===========================================

StorageQos
~~~~~~~~~~

Applied stereotypes:

-  Future

================== ============= ========= ========== ================================== =========================================================
**Attribute Name** **Type**      **Mult.** **Access** **Stereotypes**                    **Description**
================== ============= ========= ========== ================================== =========================================================
qosId              Identifier    1         RW         OpenModelAttribute                 Unique identifier of the storage Qos in VNFD.
                                                                                        
                                                      -  isInvariant: false             
                                                                                        
                                                      -  valueRange: no range constraint
                                                                                        
                                                      -  support: MANDATORY             
                                                                                        
                                                      Future                            
qosName            String        1         RW         OpenModelAttribute                 Name of storage QoS.
                                                                                        
                                                      -  isInvariant: false             
                                                                                        
                                                      -  valueRange: no range constraint
                                                                                        
                                                      -  support: MANDATORY             
                                                                                        
                                                      Future                            
consumer           ConsumerScope 1         RW         OpenModelAttribute                 Consumer type.
                                                                                        
                                                      -  isInvariant: false             
                                                                                        
                                                      -  valueRange: no range constraint
                                                                                        
                                                      -  support: MANDATORY             
                                                                                        
                                                      Future                            
qosSpecs           KeyValuePair  0..\*     RW         OpenModelAttribute                 Describe qualities of Qos?total_bytes_sec?total_iops_sec.
                                                                                        
                                                      -  isInvariant: false             
                                                                                        
                                                      -  valueRange: no range constraint
                                                                                        
                                                      -  support: MANDATORY             
                                                                                        
                                                      Future                            
================== ============= ========= ========== ================================== =========================================================

VirtualCpuData
~~~~~~~~~~~~~~

The VirtualCpuData information element supports the specification of requirements related to virtual CPU(s) of a virtual compute resource.

Applied stereotypes:

-  Reference

-  **reference: IFA011 v2.5.1**

-  Preliminary

================================ ===================== ========= ========== ================================== =======================================================================================================================================================================================================
**Attribute Name**               **Type**              **Mult.** **Access** **Stereotypes**                    **Description**
================================ ===================== ========= ========== ================================== =======================================================================================================================================================================================================
cpuArchitecture                  String                0..1      RW         Preliminary                        CPU architecture type. Examples are x86, ARM. The cardinality can be 0 during the allocation request, if no particular CPU architecture type is requested.
                                                                                                              
                                                                            OpenModelAttribute                
                                                                                                              
                                                                            -  isInvariant: false             
                                                                                                              
                                                                            -  valueRange: no range constraint
                                                                                                              
                                                                            -  support: MANDATORY             
numVirtualCpu                    Integer               1         RW         Preliminary                        Number of virtual CPUs.
                                                                                                              
                                                                            OpenModelAttribute                
                                                                                                              
                                                                            -  isInvariant: false             
                                                                                                              
                                                                            -  valueRange: no range constraint
                                                                                                              
                                                                            -  support: MANDATORY             
virtualCpuClock                  Number                0..1      RW         Preliminary                        Minimum virtual CPU clock rate (e.g. in MHz). The cardinality can be 0 during the allocation request, if no particular value is requested.
                                                                                                              
                                                                            OpenModelAttribute                
                                                                                                              
                                                                            -  isInvariant: false             
                                                                                                              
                                                                            -  valueRange: no range constraint
                                                                                                              
                                                                            -  support: MANDATORY             
virtualCpuOversubscriptionPolicy String                0..1      RW         Obsolete                           The CPU core oversubscription policy e.g. the relation of virtual CPU cores to physical CPU cores/threads. The cardinality can be 0 during the allocation request, if no particular value is requested.
                                                                                                              
                                                                            OpenModelAttribute                
                                                                                                              
                                                                            -  isInvariant: false             
                                                                                                              
                                                                            -  valueRange: no range constraint
                                                                                                              
                                                                            -  support: MANDATORY             
vduCpuRequirements               KeyValuePair          0..\*     RW         Preliminary                        Array of key-value pair requirements on the Compute (CPU) for the VDU.
                                                                                                              
                                                                            OpenModelAttribute                
                                                                                                              
                                                                            -  isInvariant: false             
                                                                                                              
                                                                            -  valueRange: no range constraint
                                                                                                              
                                                                            -  support: MANDATORY             
virtualCpuPinning                VirtualCpuPinningData 0..1      RW         Obsolete                           The virtual CPU pinning configuration for the virtualised compute resource.
                                                                                                              
                                                                            OpenModelAttribute                
                                                                                                              
                                                                            -  isInvariant: false             
                                                                                                              
                                                                            -  valueRange: no range constraint
                                                                                                              
                                                                            -  support: MANDATORY             
================================ ===================== ========= ========== ================================== =======================================================================================================================================================================================================

VirtualCpuPinningData
~~~~~~~~~~~~~~~~~~~~~

The VirtualCpuPinningData information element supports the specification of requirements related to the virtual CPU pinning configuration of a virtual compute resource.

Applied stereotypes:

-  Obsolete

======================= ============= ========= ========== ================================== =========================================================================================================================================================================================================================================================================================================================================================================
**Attribute Name**      **Type**      **Mult.** **Access** **Stereotypes**                    **Description**
======================= ============= ========= ========== ================================== =========================================================================================================================================================================================================================================================================================================================================================================
virtualCpuPinningPolicy PinningPolicy 0..1      RW         Obsolete                           The policy can take values of "static" or "dynamic". In case of "static" the virtual CPU cores are requested to be allocated to logical CPU cores according to the rules defined in virtualCpuPinningRules. In case of "dynamic" the allocation of virtual CPU cores to logical CPU cores is decided by the VIM. (e.g.: SMT (Simultaneous Multi-Threading) requirements).
                                                                                             
                                                           OpenModelAttribute                
                                                                                             
                                                           -  isInvariant: false             
                                                                                             
                                                           -  valueRange: no range constraint
                                                                                             
                                                           -  support: MANDATORY             
virtualCpuPinningRule   invalid       0..1      RW         Obsolete                           A list of rules that should be considered during the allocation of the virtual CPUs to logical CPUs in case of "static" virtualCpuPinningPolicy.
                                                                                             
                                                           OpenModelAttribute                
                                                                                             
                                                           -  isInvariant: false             
                                                                                             
                                                           -  valueRange: no range constraint
                                                                                             
                                                           -  support: MANDATORY             
======================= ============= ========= ========== ================================== =========================================================================================================================================================================================================================================================================================================================================================================

VirtualLinkBitRateLevel
~~~~~~~~~~~~~~~~~~~~~~~

The VirtualLinkBitRateLevel information element specifies bitrate requirements applicable to a virtual link instantiated from a particular VnfVirtualLinkDesc.

Applied stereotypes:

-  Reference

-  **reference: IFA011 v2.5.1**

-  Preliminary

==================== ======================= ========= ========== ================================== ====================================================================================
**Attribute Name**   **Type**                **Mult.** **Access** **Stereotypes**                    **Description**
==================== ======================= ========= ========== ================================== ====================================================================================
vnfVirtualLinkDescId VnfVirtualLinkDesc      1         RW         Preliminary                        Uniquely identifies a VnfVirtualLinkDesc
                                                                                                    
                                                                  OpenModelAttribute                
                                                                                                    
                                                                  -  isInvariant: false             
                                                                                                    
                                                                  -  valueRange: no range constraint
                                                                                                    
                                                                  -  support: MANDATORY             
                                                                                                    
                                                                  PassedByReference                 
bitrateRequirements  LinkBitrateRequirements 1         RW         Preliminary                        Bitrate requirements for an instantiation level or bitrate delta for a scaling step.
                                                                                                    
                                                                  OpenModelAttribute                
                                                                                                    
                                                                  -  isInvariant: false             
                                                                                                    
                                                                  -  valueRange: no range constraint
                                                                                                    
                                                                  -  support: MANDATORY             
==================== ======================= ========= ========== ================================== ====================================================================================

VirtualLinkProtocolData
~~~~~~~~~~~~~~~~~~~~~~~

The VirtualLinkProtocolData describes the protocol layer and associated protocol data for a virtual link

Applied stereotypes:

-  Reference

-  **reference: IFA011 v2.5.1**

-  Preliminary

======================= ============== ========= ========== ================================== ========================================================================================================================================================================
**Attribute Name**      **Type**       **Mult.** **Access** **Stereotypes**                    **Description**
======================= ============== ========= ========== ================================== ========================================================================================================================================================================
associatedLayerProtocol LayerProtocol  1         RW         Preliminary                        One of the values of the attribute layerProtocol of the ConnectivityType IE.
                                                                                              
                                                            OpenModelAttribute                
                                                                                              
                                                            -  isInvariant: false             
                                                                                              
                                                            -  valueRange: no range constraint
                                                                                              
                                                            -  support: MANDATORY             
l2ProtocolData          L2ProtocolData 0..1      RW         Preliminary                        Specifies the L2 protocol data for this virtual link. Shall be present when the associatedLayerProtocol attribute indicates a L2 protocol and shall be absent otherwise.
                                                                                              
                                                            OpenModelAttribute                
                                                                                              
                                                            -  isInvariant: false             
                                                                                              
                                                            -  valueRange: no range constraint
                                                                                              
                                                            -  support: MANDATORY             
l3ProtocolData          L3ProtocolData 0..1      RW         Preliminary                        Specifies the L3 protocol data for this virtual link. Shall be present when the associatedLayerProtocol attribute indicates a L3 protocol and shall be absent otherwise.
                                                                                              
                                                            OpenModelAttribute                
                                                                                              
                                                            -  isInvariant: false             
                                                                                              
                                                            -  valueRange: no range constraint
                                                                                              
                                                            -  support: MANDATORY             
======================= ============== ========= ========== ================================== ========================================================================================================================================================================

VirtualMemoryData
~~~~~~~~~~~~~~~~~

The VirtualMemoryData information element supports the specification of requirements related to virtual memory of a virtual compute resource.

Applied stereotypes:

-  Reference

-  **reference: IFA011 v2.5.1**

-  Preliminary

================================ ============ ========= ========== ================================== ===================================================================================================================================================================================================
**Attribute Name**               **Type**     **Mult.** **Access** **Stereotypes**                    **Description**
================================ ============ ========= ========== ================================== ===================================================================================================================================================================================================
virtualMemSize                   Number       1         RW         Preliminary                        Amount of virtual Memory (e.g. in MB).
                                                                                                     
                                                                   OpenModelAttribute                
                                                                                                     
                                                                   -  isInvariant: false             
                                                                                                     
                                                                   -  valueRange: no range constraint
                                                                                                     
                                                                   -  support: MANDATORY             
virtualMemOversubscriptionPolicy String       0..1      RW         Obsolete                           The memory core oversubscription policy in terms of virtual memory to physical memory on the platform. The cardinality can be 0 during the allocation request, if no particular value is requested.
                                                                                                     
                                                                   OpenModelAttribute                
                                                                                                     
                                                                   -  isInvariant: false             
                                                                                                     
                                                                   -  valueRange: no range constraint
                                                                                                     
                                                                   -  support: MANDATORY             
vduMemRequirements               KeyValuePair 0..\*     RW         Preliminary                        Array of key-value pair requirements on the memory for the VDU.
                                                                                                     
                                                                   OpenModelAttribute                
                                                                                                     
                                                                   -  isInvariant: false             
                                                                                                     
                                                                   -  valueRange: no range constraint
                                                                                                     
                                                                   -  support: MANDATORY             
numaEnabled                      Boolean      0..1      RW         Obsolete                           It specifies the memory allocation to be cognisant of the relevant process/core allocation. The cardinality can be 0 during the allocation request, if no particular value is requested.
                                                                                                     
                                                                   OpenModelAttribute                
                                                                                                     
                                                                   -  isInvariant: false             
                                                                                                     
                                                                   -  valueRange: no range constraint
                                                                                                     
                                                                   -  support: MANDATORY             
================================ ============ ========= ========== ================================== ===================================================================================================================================================================================================

VnfConfigurableProperties
~~~~~~~~~~~~~~~~~~~~~~~~~

This datatype defines the configurable properties of a VNF (e.g. related to auto scaling and auto healing). For a VNF instance, the value of these properties can be modified by the VNFM

Applied stereotypes:

-  Reference

-  **reference: IFA011 v2.5.1**

-  Preliminary

============================== ======== ========= ========== ================================== =============================================================================================================================================================================
**Attribute Name**             **Type** **Mult.** **Access** **Stereotypes**                    **Description**
============================== ======== ========= ========== ================================== =============================================================================================================================================================================
isAutoscaleEnabled             Boolean  0..1      RW         Preliminary                        It permits to enable (TRUE)/disable (FALSE) the auto-scaling functionality. NOTE: A cardinality of "0" indicates that configuring this present VNF property is not supported.
                                                                                               
                                                             OpenModelAttribute                
                                                                                               
                                                             -  isInvariant: false             
                                                                                               
                                                             -  valueRange: no range constraint
                                                                                               
                                                             -  support: MANDATORY             
isAutohealEnabled              Boolean  0..1      RW         Preliminary                        It permits to enable (TRUE)/disable (FALSE) the auto-healing functionality. NOTE: A cardinality of "0" indicates that configuring this present VNF property is not supported.
                                                                                               
                                                             OpenModelAttribute                
                                                                                               
                                                             -  isInvariant: false             
                                                                                               
                                                             -  valueRange: no range constraint
                                                                                               
                                                             -  support: MANDATORY             
additionalConfigurableProperty String   0..\*     RW         Preliminary                       
                                                                                               
                                                             OpenModelAttribute                
                                                                                               
                                                             -  isInvariant: false             
                                                                                               
                                                             -  valueRange: no range constraint
                                                                                               
                                                             -  support: MANDATORY             
============================== ======== ========= ========== ================================== =============================================================================================================================================================================

VnfIndicatorData
~~~~~~~~~~~~~~~~

The VnfIndicatorData datatype identifies a VNF indicator in a VNFD.

Applied stereotypes:

-  Reference

-  **reference: IFA011 v2.5.1**

-  Preliminary

================== ============ ========= ========== ================================== ===========================================
**Attribute Name** **Type**     **Mult.** **Access** **Stereotypes**                    **Description**
================== ============ ========= ========== ================================== ===========================================
vnfdId             Vnfd         1         RW         Preliminary                        Identifies a VNFD.
                                                                                       
                                                     OpenModelAttribute                
                                                                                       
                                                     -  isInvariant: false             
                                                                                       
                                                     -  valueRange: no range constraint
                                                                                       
                                                     -  support: MANDATORY             
vnfIndicator       VnfIndicator 1         RW         Preliminary                        Identifies a VNF indicator within the VNFD.
                                                                                       
                                                     OpenModelAttribute                
                                                                                       
                                                     -  isInvariant: false             
                                                                                       
                                                     -  valueRange: no range constraint
                                                                                       
                                                     -  support: MANDATORY             
================== ============ ========= ========== ================================== ===========================================

VnfInfoModifiableAttributes
~~~~~~~~~~~~~~~~~~~~~~~~~~~

This datatype defines the VNF-specific extension and metadata attributes of the VnfInfo that are writeable via the ModifyVnfInfo operation.

Applied stereotypes:

-  Reference

-  **reference: IFA011 v2.5.1**

-  Preliminary

================== ======== ========= ========== ================================== ====================================================================================================================================================================================================================================================================
**Attribute Name** **Type** **Mult.** **Access** **Stereotypes**                    **Description**
================== ======== ========= ========== ================================== ====================================================================================================================================================================================================================================================================
extension          invalid  0..\*     RW         Experimental                       "Extension" attributes of VnfInfo that are writeable. NOTE: The exact data structure describing the attribute is left for data model solution specification, but it should include: name, and any constraints on the values, such as ranges, predefined values, etc.
                                                                                   
                                                 OpenModelAttribute                
                                                                                   
                                                 -  isInvariant: false             
                                                                                   
                                                 -  valueRange: no range constraint
                                                                                   
                                                 -  support: MANDATORY             
metadata           invalid  0..\*     RW         Experimental                       Metadata" attributes of VnfInfo that are writeable. NOTE: The exact data structure describing the attribute is left for data model solution specification, but it should include: name, and any constraints on the values, such as ranges, predefined values, etc.
                                                                                   
                                                 OpenModelAttribute                
                                                                                   
                                                 -  isInvariant: false             
                                                                                   
                                                 -  valueRange: no range constraint
                                                                                   
                                                 -  support: MANDATORY             
================== ======== ========= ========== ================================== ====================================================================================================================================================================================================================================================================

VnfLcmOperationsConfiguration
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

Applied stereotypes:

-  Reference

-  **reference: IFA011 v2.5.1**

-  Experimental

VnfLifecycleManagementScript
~~~~~~~~~~~~~~~~~~~~~~~~~~~~

Applied stereotypes:

-  Reference

-  **reference: IFA011 v2.5.1**

-  Preliminary

================== ============ ========= ========== =========================================================================================== ==========================================================================================================================================================================================================================================================================================================
**Attribute Name** **Type**     **Mult.** **Access** **Stereotypes**                                                                             **Description**
================== ============ ========= ========== =========================================================================================== ==========================================================================================================================================================================================================================================================================================================
event              LcmEvent     0..\*     RW         Preliminary                                                                                 Describes VNF lifecycle event(s) or an external stimulus detected on a VNFM reference point.
                                                                                                                                                
                                                     OpenModelAttribute                                                                         
                                                                                                                                                
                                                     -  isInvariant: false                                                                      
                                                                                                                                                
                                                     -  valueRange: no range constraint                                                         
                                                                                                                                                
                                                     -  support: CONDITIONAL_MANDATORY                                                          
                                                                                                                                                
                                                     -  condition:At least one of the 2 attributes event or lcmTransitionEvent shall be included
icmTransitionEvent String       0..\*     RW         Preliminary                                                                                 Describes the transition VNF lifecycle event(s) that cannot be mapped to any of the enumerated values defined for the event attribute. NOTE: At least one of these two attributes shall be included.
                                                                                                                                                
                                                     OpenModelAttribute                                                                         
                                                                                                                                                
                                                     -  isInvariant: false                                                                      
                                                                                                                                                
                                                     -  valueRange: no range constraint                                                         
                                                                                                                                                
                                                     -  support: MANDATORY                                                                      
script             String       1         RW         Preliminary                                                                                 Information to locate a VNF LCM script (e.g. written in a DSL as specified in requirement VNF_PACK.LCM.001) triggered to react to one of the events listed in the event attribute.
                                                                                                                                                
                                                     OpenModelAttribute                                                                         
                                                                                                                                                
                                                     -  isInvariant: false                                                                      
                                                                                                                                                
                                                     -  valueRange: no range constraint                                                         
                                                                                                                                                
                                                     -  support: MANDATORY                                                                      
scriptDsl          String       1         RW         Preliminary                                                                                 Defines the domain specific language (i.e. the type) of script that is provided. Types of scripts could include bash, python, etc.
                                                                                                                                                
                                                     OpenModelAttribute                                                                         
                                                                                                                                                
                                                     -  isInvariant: false                                                                      
                                                                                                                                                
                                                     -  valueRange: no range constraint                                                         
                                                                                                                                                
                                                     -  support: MANDATORY                                                                      
scriptInput        KeyValuePair 0..\*     RW         Preliminary                                                                                 Array of KVP requirements with the key as the parameter name and the value as the parameter that need to be passed as an input to the script. NOTE: The scriptInput values are passed to the scripts in addition to the parameters received in the operation invocation request or indicator value change.
                                                                                                                                                
                                                     OpenModelAttribute                                                                         
                                                                                                                                                
                                                     -  isInvariant: false                                                                      
                                                                                                                                                
                                                     -  valueRange: no range constraint                                                         
                                                                                                                                                
                                                     -  support: MANDATORY                                                                      
================== ============ ========= ========== =========================================================================================== ==========================================================================================================================================================================================================================================================================================================

VnfQoS
~~~~~~

The QoS as applied to the vnf.

Applied stereotypes:

-  Reference

-  **reference: IFA011 v2.5.1**

-  Preliminary

VnfToLevelMapping
~~~~~~~~~~~~~~~~~

The VnfToLevelMapping datatype specifies the profile to be used for a VNF involved in a given NS level and the required number of instances.

Applied stereotypes:

-  Future

================== ======== ========= ========== ================================== =========================================================================================================================================================================================================================================================================================================================================================================================================================================================================================================================================================================================================================================================================================================================================================================================================================
**Attribute Name** **Type** **Mult.** **Access** **Stereotypes**                    **Description**
================== ======== ========= ========== ================================== =========================================================================================================================================================================================================================================================================================================================================================================================================================================================================================================================================================================================================================================================================================================================================================================================================================
vnfProfileId       invalid  1         RW         OpenModelAttribute                 Identifies the profile to be used for a VNF involved in an NS level.
                                                                                   
                                                 -  isInvariant: false             
                                                                                   
                                                 -  valueRange: no range constraint
                                                                                   
                                                 -  support: MANDATORY             
                                                                                   
                                                 Future                            
numberOfInstances  Integer  1         RW         OpenModelAttribute                 Specifies the number of VNF instances required for an NS level. NOTE 1: It shall be in the range of minNumberOfInstances-maxNumberOfInstances, as specified in the referenced VnfProfile. NOTE 2: When the corresponding NS level is used in the context of NS instantiation, the numberOfInstances attribute specifies the number of VNF instances to be deployed. NOTE 3: When the corresponding NS level is used in the context of NS scaling, the numberOfInstances attribute does not specify the number of VNF instances to be added/removed when reaching that NS scale level. The actual number of VNF instances to be added/removed can be derived by subtracting the numberOfInstances declared in the source NS scale level from the numberOfInstances declared in the target NS level of the scaling request.
                                                                                   
                                                 -  isInvariant: false             
                                                                                   
                                                 -  valueRange: no range constraint
                                                                                   
                                                 -  support: MANDATORY             
                                                                                   
                                                 Future                            
================== ======== ========= ========== ================================== =========================================================================================================================================================================================================================================================================================================================================================================================================================================================================================================================================================================================================================================================================================================================================================================================================================

VnfcConfigurableProperties
~~~~~~~~~~~~~~~~~~~~~~~~~~

This datatype defines the configurable properties of a VNFC. For a VNFC instance, the value of these properties can be modified through the VNFM.

Applied stereotypes:

-  Reference

-  **reference: IFA011 v2.5.1**

-  Preliminary

================================== ======== ========= ========== ================================== ================================================================================================
**Attribute Name**                 **Type** **Mult.** **Access** **Stereotypes**                    **Description**
================================== ======== ========= ========== ================================== ================================================================================================
additionalVnfcConfigurableProperty String   0..\*     RW         Preliminary                        It provides VNFC configurable properties that can be modified using the ModifyVnfInfo operation.
                                                                                                   
                                                                 OpenModelAttribute                
                                                                                                   
                                                                 -  isInvariant: false             
                                                                                                   
                                                                 -  valueRange: no range constraint
                                                                                                   
                                                                 -  support: MANDATORY             
================================== ======== ========= ========== ================================== ================================================================================================

VolumeType
~~~~~~~~~~

Applied stereotypes:

-  Future

================== ========== ========= ========== ================================== =========================================
**Attribute Name** **Type**   **Mult.** **Access** **Stereotypes**                    **Description**
================== ========== ========= ========== ================================== =========================================
volumeTypeId       Identifier 1         RW         OpenModelAttribute                 Unique identifier of volume type in VNFD.
                                                                                     
                                                   -  isInvariant: false             
                                                                                     
                                                   -  valueRange: no range constraint
                                                                                     
                                                   -  support: MANDATORY             
                                                                                     
                                                   Future                            
volumeTypeName     String     1         RW         OpenModelAttribute                 Name of volume type.
                                                                                     
                                                   -  isInvariant: false             
                                                                                     
                                                   -  valueRange: no range constraint
                                                                                     
                                                   -  support: MANDATORY             
                                                                                     
                                                   Future                            
backendName        String     1         RW         OpenModelAttribute                 Backend volume name of cinder.
                                                                                     
                                                   -  isInvariant: false             
                                                                                     
                                                   -  valueRange: no range constraint
                                                                                     
                                                   -  support: MANDATORY             
                                                                                     
                                                   Future                            
================== ========== ========= ========== ================================== =========================================

Enumerations
------------

CollectionPeriod
~~~~~~~~~~~~~~~~

Specifies the periodicity at which the producer will collect performance information. Note: at the end of each reportingPeriod, the producer will inform the consumer about availability of the performance data collected for each completed collection period during this reportingPeriod. While the exact definition of the types for collectionPeriod and reportingPeriod is left for further specification, it is recommended that the reportingPeriod be equal or a multiple of the collectionPeriod. In the latter case, the performance data for the collection periods within one reporting period would be reported together.

Contains Enumeration Literals:

ConsumerScope
~~~~~~~~~~~~~

Contains Enumeration Literals:

-  BACK_END:

Direction
~~~~~~~~~

Ingress or egress traffic

Contains Enumeration Literals:

-  INGRESS:

-  EGRESS:

HomingStrategy
~~~~~~~~~~~~~~

Contains Enumeration Literals:

-  Colocation:

-  isolation:

LcmEvent
~~~~~~~~

Describes VNF lifecycle event(s) or an external stimulus detected on a VNFM reference point.

Contains Enumeration Literals:

-  EVENT_START_INSTANTIATION:

-  EVENT_END_INSTANTIATION:

-  EVENT_START_SCALING:

-  EVENT_END_SCALING:

-  EVENT_START_SCALING_TO_LEVEL:

-  EVENT_END_SCALING_TO_LEVEL:

-  EVENT_START_HEALING:

-  EVENT_END_HEALING:

-  EVENT_START_TERMINATION:

-  EVENT_END_TERMINATION:

-  EVENT_START_VNF_FLAVOR_CHANGE:

-  EVENT_END_VNF_FLAVOR_CHANGE:

-  EVENT_START_VNF_OPERATION_CHANGE:

-  EVENT_END_VNF_OPERATION_CHANGE:

-  EVENT_START_VNF_EXT_CONN_CHANGE:

-  EVENT_END_VNF_EXT_CONN_CHANGE:

-  EVENT_START_VNFINFO_MODIFICATION:

-  EVENT_END_VNFINFO_MODIFICATION:

OperationalStatus
~~~~~~~~~~~~~~~~~

Indicator for whether the resource is considered operational. Valid values are in-service-path and out-of-service-path.

Contains Enumeration Literals:

-  IN_SERVICE:

-  OUT_OF_SERVICE:

OrchestrationStatus
~~~~~~~~~~~~~~~~~~~

Contains Enumeration Literals:

-  INVENTORIED:

-  ASSIGNED:

-  CREATED:

-  ACTIVE:

PinningPolicy
~~~~~~~~~~~~~

Defines the CPU pinning policy.

Contains Enumeration Literals:

-  STATIC:

-  DYNAMIC:

PlacementStrategy
~~~~~~~~~~~~~~~~~

Contains Enumeration Literals:

-  COLOCATION:

-  ISOLATION:

-  EXCLUSIVITY:

ProvStatus
~~~~~~~~~~

Provisioning status, used as a trigger for operational monitoring of this resource by service assurance systems.

Contains Enumeration Literals:

-  PROVISIONED:

-  PREPROVISIONED:

-  CAPPED:

VnfSource
~~~~~~~~~

Describes the source of the indicator.

Contains Enumeration Literals:

-  VNF:

-  EM:

-  BOTH:

VnicType
~~~~~~~~

Describes the type of VNIC to which a CP attaches.

Contains Enumeration Literals:

-  NORMAL:

-  MACVTAP:

-  DIRECT:

-  BAREMETAL:

-  DIRECT_PHYSICAL:

-  VIRTIO_FORWARDER: