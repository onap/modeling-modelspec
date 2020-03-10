.. Copyright 2018 (China Mobile)
.. This file is licensed under the CREATIVE COMMONS ATTRIBUTION 4.0 INTERNATIONAL LICENSE
.. Full license text at https://creativecommons.org/licenses/by/4.0/legalcode

.. contents::
   :depth: 3
..


Classes
-------

Attachment
~~~~~~~~~~

Applied stereotypes:

-  OpenModelClass

-  **support: MANDATORY**

================== ========== ========= ================================== ===============
**Attribute Name** **Type**   **Mult.** **Stereotypes**                    **Description**
id                 String     1         OpenModelAttribute                
                                                                          
                                        -  isInvariant: false             
                                                                          
                                        -  valueRange: no range constraint
                                                                          
                                        -  support: MANDATORY             
href               String     1         OpenModelAttribute                
                                                                          
                                        -  isInvariant: false             
                                                                          
                                        -  valueRange: no range constraint
                                                                          
                                        -  support: MANDATORY             
name               String     1         OpenModelAttribute                
                                                                          
                                        -  isInvariant: false             
                                                                          
                                        -  valueRange: no range constraint
                                                                          
                                        -  support: MANDATORY             
description        String     1         OpenModelAttribute                
                                                                          
                                        -  isInvariant: false             
                                                                          
                                        -  valueRange: no range constraint
                                                                          
                                        -  support: MANDATORY             
type               String     1         OpenModelAttribute                
                                                                          
                                        -  isInvariant: false             
                                                                          
                                        -  valueRange: no range constraint
                                                                          
                                        -  support: MANDATORY             
uri                String     1         OpenModelAttribute                
                                                                          
                                        -  isInvariant: false             
                                                                          
                                        -  valueRange: no range constraint
                                                                          
                                        -  support: MANDATORY             
mimeType           String     1         OpenModelAttribute                
                                                                          
                                        -  isInvariant: false             
                                                                          
                                        -  valueRange: no range constraint
                                                                          
                                        -  support: MANDATORY             
validFor           TimePeriod 1         OpenModelAttribute                
                                                                          
                                        -  isInvariant: false             
                                                                          
                                        -  valueRange: no range constraint
                                                                          
                                        -  support: MANDATORY             
================== ========== ========= ================================== ===============

.. _attachment-1:

Attachment
~~~~~~~~~~

Applied stereotypes:

-  OpenModelClass

-  **support: MANDATORY**

================== ======== ========= ================================== ===============
**Attribute Name** **Type** **Mult.** **Stereotypes**                    **Description**
id                 String   1         OpenModelAttribute                
                                                                        
                                      -  isInvariant: false             
                                                                        
                                      -  valueRange: no range constraint
                                                                        
                                      -  support: MANDATORY             
name               String   1         OpenModelAttribute                
                                                                        
                                      -  isInvariant: false             
                                                                        
                                      -  valueRange: no range constraint
                                                                        
                                      -  support: MANDATORY             
description        String   1         OpenModelAttribute                
                                                                        
                                      -  isInvariant: false             
                                                                        
                                      -  valueRange: no range constraint
                                                                        
                                      -  support: MANDATORY             
type               String   1         OpenModelAttribute                
                                                                        
                                      -  isInvariant: false             
                                                                        
                                      -  valueRange: no range constraint
                                                                        
                                      -  support: MANDATORY             
url                String   1         OpenModelAttribute                
                                                                        
                                      -  isInvariant: false             
                                                                        
                                      -  valueRange: no range constraint
                                                                        
                                      -  support: MANDATORY             
================== ======== ========= ================================== ===============

CpdPool
~~~~~~~

The CpdPool class specifies a pool of descriptors of connection points and service access points.

Applied stereotypes:

-  Future

-  OpenModelClass

-  **support: MANDATORY**

================== ========== ========= ================================== =======================================================================================================
**Attribute Name** **Type**   **Mult.** **Stereotypes**                    **Description**
cpdPoolId          Identifier 1         OpenModelAttribute                 Identifier of this CpdPool class. It identifies a pool of descriptors of connection points and NS SAPs.
                                                                          
                                        -  isInvariant: false             
                                                                          
                                        -  valueRange: no range constraint
                                                                          
                                        -  support: MANDATORY             
================== ========== ========= ================================== =======================================================================================================

Dependencies
~~~~~~~~~~~~

The Dependencies class provides indications on the order in which VNFs associated to different VNF Profiles and/or nested NSs associated to different NS Profiles are to be instantiated.

Applied stereotypes:

-  Future

-  OpenModelClass

-  **support: MANDATORY**

=========================== ============== ========= ================================== ==============================================================================================================================================================================================================================================================================================
**Attribute Name**          **Type**       **Mult.** **Stereotypes**                    **Description**
\_primaryProfileReference   NsOrVnfProfile 1..\*     OpenModelAttribute                 References a VnfProfile or NsProfile.
                                                                                        NOTE: NFV Management and Orchestration functions shall instantiate VNFs from the VnfProfile and/or nested NSs from the NsProfile referenced in the primary attribute before instantiating VNFs from the VnfProfile and/or nested NSs from the NsProfile referenced in the secondary attribute.
                                                     -  isInvariant: false             
                                                                                       
                                                     -  valueRange: no range constraint
                                                                                       
                                                     -  support: MANDATORY             
\_secondaryProfileReference NsOrVnfProfile 1..\*     OpenModelAttribute                 References a VnfProfile or NsProfile.
                                                                                        NOTE: NFV Management and Orchestration functions shall instantiate VNFs from the VnfProfile and/or nested NSs from the NsProfile referenced in the primary attribute before instantiating VNFs from the VnfProfile and/or nested NSs from the NsProfile referenced in the secondary attribute
                                                     -  isInvariant: false             
                                                                                       
                                                     -  valueRange: no range constraint
                                                                                       
                                                     -  support: MANDATORY             
=========================== ============== ========= ================================== ==============================================================================================================================================================================================================================================================================================

NetworkServiceInstance
~~~~~~~~~~~~~~~~~~~~~~

A composition of Network Functions and defined by its functional and behavioural specification.
NOTE: The Network Service (NS) contributes to the behaviour of the higher layer service, which is characterized by at least performance, dependability, and security specifications. The end-to-end network service behaviour is the result of the combination of the individual network function behaviours as well as the behaviours of the network infrastructure composition mechanism.

**Parent class:** ServiceComponentInstance

Applied stereotypes:

-  Future

-  OpenModelClass

-  **support: MANDATORY**

========================== ======================== ========= ================================== ============================================================================================================================
**Attribute Name**         **Type**                 **Mult.** **Stereotypes**                    **Description**
nsInstanceId               Identifier               1         OpenModelAttribute                 Identifier of this NetworkService, identifying the NS instance.
                                                                                                
                                                              -  isInvariant: false             
                                                                                                
                                                              -  valueRange: no range constraint
                                                                                                
                                                              -  support: MANDATORY             
nsName                     String                   1         OpenModelAttribute                 Human readable name of the NS instance.
                                                                                                
                                                              -  isInvariant: false             
                                                                                                
                                                              -  valueRange: no range constraint
                                                                                                
                                                              -  support: MANDATORY             
description                String                   1         OpenModelAttribute                 Human readable description of the NS instance
                                                                                                
                                                              -  isInvariant: false             
                                                                                                
                                                              -  valueRange: no range constraint
                                                                                                
                                                              -  support: MANDATORY             
\_nf                       NetworkFunction          0..\*     OpenModelAttribute                 Reference to consistituent VNFs and PNFs on this NS.
                                                                                                 NOTE: Cardinality of zero is only valid for a non-instantiated NS.
                                                              -  isInvariant: false             
                                                                                                
                                                              -  valueRange: no range constraint
                                                                                                
                                                              -  support: MANDATORY             
\_nsVirtualLink            NsVirtualLink            0..\*     OpenModelAttribute                 Information on the VLs of this NS.
                                                                                                 NOTE: Cardinality of zero is only valid for a non-instantiated NS.
                                                              -  isInvariant: false             
                                                                                                
                                                              -  valueRange: no range constraint
                                                                                                
                                                              -  support: MANDATORY             
\_sap                      Sap                      0..\*     OpenModelAttribute                 Information on the SAPs of this NS.
                                                                                                
                                                              -  isInvariant: false             
                                                                                                
                                                              -  valueRange: no range constraint
                                                                                                
                                                              -  support: MANDATORY             
\_nestedNsi                NetworkServiceInstance   0..\*     OpenModelAttribute                 Reference to information on nested NSs of this NS.
                                                                                                
                                                              -  isInvariant: false             
                                                                                                
                                                              -  valueRange: no range constraint
                                                                                                
                                                              -  support: MANDATORY             
\_vnffg                    Vnffg                    0..\*     OpenModelAttribute                 Information on the VNFFGs of this NS.
                                                                                                
                                                              -  isInvariant: false             
                                                                                                
                                                              -  valueRange: no range constraint
                                                                                                
                                                              -  support: MANDATORY             
instanceId                 Identifier               1         OpenModelAttribute                 Uniquely identifies this instance of a service component.
                                                                                                
                                                              -  isInvariant: false             
                                                                                                
                                                              -  valueRange: no range constraint
                                                                                                
                                                              -  support: MANDATORY             
name                       String                   1         OpenModelAttribute                 The name assigned to the service component instance.
                                                                                                
                                                              -  isInvariant: false             
                                                                                                
                                                              -  valueRange: no range constraint
                                                                                                
                                                              -  support: MANDATORY             
modelInvariantUuid         Uuid                     1         OpenModelAttribute                 Constant identifier of the service component model.
                                                                                                
                                                              -  isInvariant: false             
                                                                                                
                                                              -  valueRange: no range constraint
                                                                                                
                                                              -  support: MANDATORY             
modelUuid                  Uuid                     1         OpenModelAttribute                 Versioned identifier of the service component model (this uuid is changed for every major version of the service component).
                                                                                                
                                                              -  isInvariant: false             
                                                                                                
                                                              -  valueRange: no range constraint
                                                                                                
                                                              -  support: MANDATORY             
modelVersion               String                   1         OpenModelAttribute                 The service version in SDC catalog.
                                                                                                
                                                              -  isInvariant: false             
                                                                                                
                                                              -  valueRange: no range constraint
                                                                                                
                                                              -  support: MANDATORY             
selfLink                   Uri                      1         OpenModelAttribute                 URL to endpoint where more details can be gotten.
                                                                                                
                                                              -  isInvariant: false             
                                                                                                
                                                              -  valueRange: no range constraint
                                                                                                
                                                              -  support: MANDATORY             
orchestrationStatus        String                   1         OpenModelAttribute                 Orchestration status of the service component instance.
                                                                                                
                                                              -  isInvariant: false             
                                                                                                
                                                              -  valueRange: no range constraint
                                                                                                
                                                              -  support: MANDATORY             
description                String                   1         OpenModelAttribute                 The description of service component instance.
                                                                                                
                                                              -  isInvariant: false             
                                                                                                
                                                              -  valueRange: no range constraint
                                                                                                
                                                              -  support: MANDATORY             
\_serviceComponentInstance ServiceComponentInstance 0..\*     OpenModelAttribute                
                                                                                                
                                                              -  isInvariant: false             
                                                                                                
                                                              -  valueRange: no range constraint
                                                                                                
                                                              -  support: MANDATORY             
========================== ======================== ========= ================================== ============================================================================================================================

Nfpd
~~~~

The Nfpd class associates traffic flow criteria to a list of descriptors associated to the connection points and service access points to be visited by traffic flows matching these criteria.

Applied stereotypes:

-  Future

-  OpenModelClass

-  **support: MANDATORY**

================== ======== ========= ================================== =====================================================================================================================================================================================================================================================================================
**Attribute Name** **Type** **Mult.** **Stereotypes**                    **Description**
nfpdId             invalid  1         OpenModelAttribute                 Identifies this nfpd class within a VNFFGD.
                                                                        
                                      -  isInvariant: false             
                                                                        
                                      -  valueRange: no range constraint
                                                                        
                                      -  support: MANDATORY             
nfpRule            invalid  1         OpenModelAttribute                 Provides an NFP classification and selection rule.
                                                                         The rule may be expressed as a criteria constructed out of atomic assertions linked by Boolean operators AND, OR and NOT.
                                      -  isInvariant: false              NOTE: Examples of atomic assertions are assertions on packet header fields' values, date and time ranges, etc.
                                                                        
                                      -  valueRange: no range constraint
                                                                        
                                      -  support: MANDATORY             
cpd                invalid  1         OpenModelAttribute                 References the descriptor of a connection point to be traversed by the traffic flows matching the criteria. This shall be a connection point attached to one of the constituent VNFs and PNFs of the parent VNFFG, or a SAP of one of the constituent nested NSs of the parent VNFFG.
                                                                         NOTE: When multiple values are provided, the order is significant and specifies the sequence of connection points to be traversed.
                                      -  isInvariant: false             
                                                                        
                                      -  valueRange: no range constraint
                                                                        
                                      -  support: MANDATORY             
================== ======== ========= ================================== =====================================================================================================================================================================================================================================================================================

NsLevel
~~~~~~~

The NsLevel class describes the details of an NS level. An NS level consists of a list of involved entities, i.e. VNFs, VLs and/or nested NSs.
For each involved VNF/nested NS, the number of instances required by the NS level is specified. For each involved VL, the bitrate requirements corresponding to the NS level are specified.
NS levels shall be used in the context of NS instantiation and in this case they are referred to as NS instantiation levels.
Every VNF, VL and nested NS whose descriptor is referenced by the NS DF shall be involved in an NS instantiation level of the parent NS. If no instances of a given VNF/nested NS have to be deployed at NS instantiation time, the numberOfInstances attribute in the corresponding VnfToLevelMapping/NsToLevelMapping datatype shall be set to 0.
NS levels may be used in the context of NS scaling and in this case they are referred to as NS scale levels.
Only a subset of the VNFs, VLs and nested NSs whose descriptor is referenced by the NS DF may be involved in an NS scale level of the parent NS.

Applied stereotypes:

-  Future

-  OpenModelClass

-  **support: MANDATORY**

========================= ========================= ========= ================================== ==========================================================================================================================
**Attribute Name**        **Type**                  **Mult.** **Stereotypes**                    **Description**
nsLevelId                 Identifier                1         OpenModelAttribute                 Identifier of this NsLevel class. It uniquely identifies an NS level within the DF.
                                                                                                
                                                              -  isInvariant: false             
                                                                                                
                                                              -  valueRange: no range constraint
                                                                                                
                                                              -  support: MANDATORY             
description               String                    1         OpenModelAttribute                 Human readable description of the NS level.
                                                                                                
                                                              -  isInvariant: false             
                                                                                                
                                                              -  valueRange: no range constraint
                                                                                                
                                                              -  support: MANDATORY             
vnfToLevelMapping         VnfToLevelMapping         0..\*     OpenModelAttribute                 Specifies the profile of the VNFs involved in this NS level and, for each of them, the required number of instances.
                                                                                                
                                                              -  isInvariant: false             
                                                                                                
                                                              -  valueRange: no range constraint
                                                                                                
                                                              -  support: MANDATORY             
virtualLinkToLevelMapping VirtualLinkToLevelMapping 0..\*     OpenModelAttribute                 Specifies the profile of the VLs involved in this NS level and, for each of them, the needed bandwidth.
                                                                                                
                                                              -  isInvariant: false             
                                                                                                
                                                              -  valueRange: no range constraint
                                                                                                
                                                              -  support: MANDATORY             
nsToLevelMapping          NsToLevelMapping          0..\*     OpenModelAttribute                 Specifies the profile of the nested NSs involved in this NS level and, for each of them, the required number of instances.
                                                                                                
                                                              -  isInvariant: false             
                                                                                                
                                                              -  valueRange: no range constraint
                                                                                                
                                                              -  support: MANDATORY             
========================= ========================= ========= ================================== ==========================================================================================================================

NsLinkPort
~~~~~~~~~~

Respresents the port of a NS VL.

Applied stereotypes:

-  Future

-  OpenModelClass

-  **support: MANDATORY**

NsOrVnfProfile
~~~~~~~~~~~~~~

This is an abstract proxy class, allowing to provide reference to either NsProfile or VnfProfile.

Applied stereotypes:

-  Future

-  OpenModelClass

-  **support: MANDATORY**

NsProfile
~~~~~~~~~

The NsProfile class specifies the profile to be used for a nested NS.

**Parent class:** NsOrVnfProfile

Applied stereotypes:

-  Future

-  OpenModelClass

-  **support: MANDATORY**

============================= =========================== ========= ================================== =================================================================================================================================================================================================================
**Attribute Name**            **Type**                    **Mult.** **Stereotypes**                    **Description**
nsProfileId                   Identifier                  1         OpenModelAttribute                 Identifies an NS profile.
                                                                                                      
                                                                    -  isInvariant: false             
                                                                                                      
                                                                    -  valueRange: no range constraint
                                                                                                      
                                                                    -  support: MANDATORY             
minNumberOfInstances          Integer                     1         OpenModelAttribute                 Minimum number of nested NS instances based on the referenced NSD that is permitted to exist for this NsProfile.
                                                                                                      
                                                                    -  isInvariant: false             
                                                                                                      
                                                                    -  valueRange: no range constraint
                                                                                                      
                                                                    -  support: MANDATORY             
maxNumberOfInstances          Integer                     1         OpenModelAttribute                 Maximum number of nested NS instances based on the referenced NSD that is permitted to exist for this NsProfile.
                                                                                                      
                                                                    -  isInvariant: false             
                                                                                                      
                                                                    -  valueRange: no range constraint
                                                                                                      
                                                                    -  support: MANDATORY             
affinityOrAntiaffinityGroupId AffinityOrAntiAffinityGroup 0..\*     OpenModelAttribute                 Identifies an affinity or anti-affinity group the NSs created according to this NsProfile belong to.
                                                                                                      
                                                                    -  isInvariant: false             
                                                                                                      
                                                                    -  valueRange: no range constraint
                                                                                                      
                                                                    -  support: MANDATORY             
\_nsdf                        NsDf                        0..1      OpenModelAttribute                 Identifies the applicable NS DF within the scope of the NSD.
                                                                                                      
                                                                    -  isInvariant: false             
                                                                                                      
                                                                    -  valueRange: no range constraint
                                                                                                      
                                                                    -  support: MANDATORY             
\_nsLevel                     NsLevel                     0..1      OpenModelAttribute                 Identifies the NS level within the referenced NS DF to be used in the context of the parent NS instantiation. If not present, the default NS instantiation level as declared in the referenced NSD shall be used.
                                                                                                      
                                                                    -  isInvariant: false             
                                                                                                      
                                                                    -  valueRange: no range constraint
                                                                                                      
                                                                    -  support: MANDATORY             
\_nsd                         NetworkServiceDescriptor    1         OpenModelAttribute                 Identifies the NSD applicable to NS instantiated according to this profile.
                                                                                                      
                                                                    -  isInvariant: false             
                                                                                                      
                                                                    -  valueRange: no range constraint
                                                                                                      
                                                                    -  support: MANDATORY             
============================= =========================== ========= ================================== =================================================================================================================================================================================================================

NsScalingAspect
~~~~~~~~~~~~~~~

The NsScalingAspect class describes the details of an NS scaling aspect. An NS scaling aspect is an abstraction representing a particular "dimension" or "property" along which a given NS can be scaled.
Defining NS levels, in this context also known as NS scale levels, within an NS scaling aspect allows to scale NS instances "by steps", i.e. to increase/decrease their capacity in a discrete manner moving from one NS scale level to another.
Scaling by a single step does not imply that exactly one instance of each entity involved in the NS scale level is created or removed.

Applied stereotypes:

-  Future

-  OpenModelClass

-  **support: MANDATORY**

================== ========== ========= ================================== ======================================================================================================================================================
**Attribute Name** **Type**   **Mult.** **Stereotypes**                    **Description**
nsScalingAspectId  Identifier 1         OpenModelAttribute                 Identifier of this NsScalingAspect class. It Uniquely identifies the NS scaling aspect in an NSD.
                                                                          
                                        -  isInvariant: false             
                                                                          
                                        -  valueRange: no range constraint
                                                                          
                                        -  support: MANDATORY             
name               String     1         OpenModelAttribute                 Provides a human readable name of the NS scaling aspect.
                                                                          
                                        -  isInvariant: false             
                                                                          
                                        -  valueRange: no range constraint
                                                                          
                                        -  support: MANDATORY             
description        String     1         OpenModelAttribute                 Provides a human readable description of the NS scaling aspect.
                                                                          
                                        -  isInvariant: false             
                                                                          
                                        -  valueRange: no range constraint
                                                                          
                                        -  support: MANDATORY             
\_nsLevel          NsLevel    1..\*     OpenModelAttribute                 Describes the details of an NS level.
                                                                           NOTE: Only a subset of the VNFs, VLs and nested NSs whose descriptor is referenced by the NS DF may be involved in an NS scale level of the parent NS.
                                        -  isInvariant: false             
                                                                          
                                        -  valueRange: no range constraint
                                                                          
                                        -  support: MANDATORY             
================== ========== ========= ================================== ======================================================================================================================================================

NsVirtualLink
~~~~~~~~~~~~~

This class provides run-time information about an NS VL instance.

**Parent class:** VirtualLink

Applied stereotypes:

-  Future

-  OpenModelClass

-  **support: MANDATORY**

====================== ======================= ========= ================================== ========================================================================================================================================================================
**Attribute Name**     **Type**                **Mult.** **Stereotypes**                    **Description**
virtualNetwork         invalid                 1         OpenModelAttribute                 Virtualised network resource(s) realizing this VL.
                                                                                           
                                                         -  isInvariant: false             
                                                                                           
                                                         -  valueRange: no range constraint
                                                                                           
                                                         -  support: MANDATORY             
\_linkPort             LinkPort                1..\*     OpenModelAttribute                 Link ports of this VL.
                                                                                           
                                                         -  isInvariant: false             
                                                                                           
                                                         -  valueRange: no range constraint
                                                                                           
                                                         -  support: MANDATORY             
vlInstanceId           Identifier              1         OpenModelAttribute                 Identifier of the virtual link instance.
                                                                                           
                                                         -  isInvariant: false             
                                                                                           
                                                         -  valueRange: no range constraint
                                                                                           
                                                         -  support: MANDATORY             
vlName                 String                  1         OpenModelAttribute                 An intelligent or human readable name of the virtual link instance.
                                                                                           
                                                         -  isInvariant: false             
                                                                                           
                                                         -  valueRange: no range constraint
                                                                                           
                                                         -  support: MANDATORY             
vlNameAlt              String                  1         OpenModelAttribute                 Additional intelligent or human readable name of the virtual link instance.
                                                                                           
                                                         -  isInvariant: false             
                                                                                           
                                                         -  valueRange: no range constraint
                                                                                           
                                                         -  support: MANDATORY             
vlType                 String                  1         OpenModelAttribute                 Generic description of the type of Virtual Link
                                                                                           
                                                         -  isInvariant: false             
                                                                                           
                                                         -  valueRange: no range constraint
                                                                                           
                                                         -  support: MANDATORY             
vlRole                 String                  1         OpenModelAttribute                 Role in the network this virtual link will be providing
                                                                                           
                                                         -  isInvariant: false             
                                                                                           
                                                         -  valueRange: no range constraint
                                                                                           
                                                         -  support: MANDATORY             
vlFunction             String                  1         OpenModelAttribute                 English description of the function this specific virtual link will be providing
                                                                                           
                                                         -  isInvariant: false             
                                                                                           
                                                         -  valueRange: no range constraint
                                                                                           
                                                         -  support: MANDATORY             
vlBandwidth            String                  1         OpenModelAttribute                 virtual link assigned (actual) bandwidth
                                                                                           
                                                         -  isInvariant: false             
                                                                                           
                                                         -  valueRange: no range constraint
                                                                                           
                                                         -  support: MANDATORY             
provStatus             String                  1         OpenModelAttribute                 provisioning status, used as a trigger for operational monitoring of this resource by service assurance systems valid value example: PROVISIONED, PREPROVISIONED, CAPPED
                                                                                           
                                                         -  isInvariant: false             
                                                                                           
                                                         -  valueRange: no range constraint
                                                                                           
                                                         -  support: MANDATORY             
adminStatus            String                  1         OpenModelAttribute                 Administrative status of the virtual link
                                                                                           
                                                         -  isInvariant: false             
                                                                                           
                                                         -  valueRange: no range constraint
                                                                                           
                                                         -  support: MANDATORY             
minBitRateRequirements LinkBitrateRequirements 1         OpenModelAttribute                 Specifies the minimum bitrate requirements for the virtual link
                                                                                           
                                                         -  isInvariant: false             
                                                                                           
                                                         -  valueRange: no range constraint
                                                                                           
                                                         -  support: MANDATORY             
maxBitRateRequirements LinkBitrateRequirements 1         OpenModelAttribute                 Specifies the maximum bitrate requirements for the virtual link
                                                                                           
                                                         -  isInvariant: false             
                                                                                           
                                                         -  valueRange: no range constraint
                                                                                           
                                                         -  support: MANDATORY             
dhcpEnabled            Boolean                 1         OpenModelAttribute                 Indicates whether DHCP is enabled
                                                                                           
                                                         -  isInvariant: false             
                                                                                           
                                                         -  valueRange: no range constraint
                                                                                           
                                                         -  support: MANDATORY             
vlanTransparent        Boolean                 1         OpenModelAttribute                 Indicates whether VLAn transparent mode is supported
                                                                                           
                                                         -  isInvariant: false             
                                                                                           
                                                         -  valueRange: no range constraint
                                                                                           
                                                         -  support: MANDATORY             
vlTrunkModeEnabled     Boolean                 1         OpenModelAttribute                 Indicates whether Trunk Mode is enabled
                                                                                           
                                                         -  isInvariant: false             
                                                                                           
                                                         -  valueRange: no range constraint
                                                                                           
                                                         -  support: MANDATORY             
vlanIdOuter            Integer                 1         OpenModelAttribute                 Outer vlan tag
                                                                                           
                                                         -  isInvariant: false             
                                                                                           
                                                         -  valueRange: no range constraint
                                                                                           
                                                         -  support: MANDATORY             
vlanIdInner            Integer                 1         OpenModelAttribute                 Inner vlan tag
                                                                                           
                                                         -  isInvariant: false             
                                                                                           
                                                         -  valueRange: no range constraint
                                                                                           
                                                         -  support: MANDATORY             
connectivityType       ConnectivityType        1         OpenModelAttribute                 Identified the layerProtocol and flowPattern used by the virtual link
                                                                                           
                                                         -  isInvariant: false             
                                                                                           
                                                         -  valueRange: no range constraint
                                                                                           
                                                         -  support: MANDATORY             
====================== ======================= ========= ================================== ========================================================================================================================================================================

OrderItemRelationship
~~~~~~~~~~~~~~~~~~~~~

Enables specifying any kind of relastionships between ServiceOrderItems

Applied stereotypes:

-  OpenModelClass

-  **support: MANDATORY**

================== ======== ========= ================================== =====================================================
**Attribute Name** **Type** **Mult.** **Stereotypes**                    **Description**
type               String   1         OpenModelAttribute                 The type of relationship such as contains, relies on.
                                                                        
                                      -  isInvariant: false             
                                                                        
                                      -  valueRange: no range constraint
                                                                        
                                      -  support: MANDATORY             
================== ======== ========= ================================== =====================================================

OrderRelationship
~~~~~~~~~~~~~~~~~

An assocation between two ServiceOrders.

Applied stereotypes:

-  OpenModelClass

-  **support: MANDATORY**

================== ======== ========= ================================== ===============================================================================
**Attribute Name** **Type** **Mult.** **Stereotypes**                    **Description**
type               String   1         OpenModelAttribute                 A categorization of the relationship, such as bulk, parent/child, and so forth.
                                                                        
                                      -  isInvariant: false             
                                                                        
                                      -  valueRange: no range constraint
                                                                        
                                      -  support: MANDATORY             
================== ======== ========= ================================== ===============================================================================

OrderState
~~~~~~~~~~

Applied stereotypes:

-  OpenModelClass

-  **support: MANDATORY**

Pnf
~~~

An implementation of a NF via a tightly coupled software and hardware system.

**Parent class:** NetworkFunction

Applied stereotypes:

-  Future

-  OpenModelClass

-  **support: MANDATORY**

================== ======== ========= ================================== =======================
**Attribute Name** **Type** **Mult.** **Stereotypes**                    **Description**
\_pnfExtCp         PnfExtCp 1..\*     OpenModelAttribute                 External CP of the PNF.
                                                                        
                                      -  isInvariant: false             
                                                                        
                                      -  valueRange: no range constraint
                                                                        
                                      -  support: MANDATORY             
================== ======== ========= ================================== =======================

PnfExtCp
~~~~~~~~

External CP of the PNF.

**Parent class:** Cp

Applied stereotypes:

-  Future

-  OpenModelClass

-  **support: MANDATORY**

================== ============= ========= ================================== ========================================================================================================================================================================
**Attribute Name** **Type**      **Mult.** **Stereotypes**                    **Description**
cpd                invalid       1         OpenModelAttribute                 Cpd used to deploy this PNF CP.
                                                                             
                                           -  isInvariant: false             
                                                                             
                                           -  valueRange: no range constraint
                                                                             
                                           -  support: MANDATORY             
cpId               Identifier    1         OpenModelAttribute                 Identifier of the connection point instance.
                                                                             
                                           -  isInvariant: false             
                                                                             
                                           -  valueRange: no range constraint
                                                                             
                                           -  support: MANDATORY             
cpName             String        1         OpenModelAttribute                 Name of the Cp instance.
                                                                             
                                           -  isInvariant: false             
                                                                             
                                           -  valueRange: no range constraint
                                                                             
                                           -  support: MANDATORY             
cpNameAlt          String        1         OpenModelAttribute                 alternative name of the Cp instance.
                                                                             
                                           -  isInvariant: false             
                                                                             
                                           -  valueRange: no range constraint
                                                                             
                                           -  support: MANDATORY             
cpType             String        1         OpenModelAttribute                 Generic description of the type of Cp
                                                                             
                                           -  isInvariant: false             
                                                                             
                                           -  valueRange: no range constraint
                                                                             
                                           -  support: MANDATORY             
cpRole             String        1         OpenModelAttribute                 Role in the network this Cp will be providing
                                                                             
                                           -  isInvariant: false             
                                                                             
                                           -  valueRange: no range constraint
                                                                             
                                           -  support: MANDATORY             
cpFunction         String        1         OpenModelAttribute                 English description of the function this specific Cp will be providing
                                                                             
                                           -  isInvariant: false             
                                                                             
                                           -  valueRange: no range constraint
                                                                             
                                           -  support: MANDATORY             
cpDescription      String        1         OpenModelAttribute                 Cp description
                                                                             
                                           -  isInvariant: false             
                                                                             
                                           -  valueRange: no range constraint
                                                                             
                                           -  support: MANDATORY             
cpBandwidth        String        1         OpenModelAttribute                 Cp assigned (actual) bandwidth
                                                                             
                                           -  isInvariant: false              Cp (max? assigned?) bandwidth
                                                                             
                                           -  valueRange: no range constraint
                                                                             
                                           -  support: MANDATORY             
provStatus         String        1         OpenModelAttribute                 provisioning status, used as a trigger for operational monitoring of this resource by service assurance systems valid value example: PROVISIONED, PREPROVISIONED, CAPPED
                                                                             
                                           -  isInvariant: false             
                                                                             
                                           -  valueRange: no range constraint
                                                                             
                                           -  support: MANDATORY             
adminsStatus       String        1         OpenModelAttribute                 Administrative status of the connection point.
                                                                             
                                           -  isInvariant: false             
                                                                             
                                           -  valueRange: no range constraint
                                                                             
                                           -  support: MANDATORY             
protocol           String        1         OpenModelAttribute                 Protocol used by the Cp
                                                                             
                                           -  isInvariant: false             
                                                                             
                                           -  valueRange: no range constraint
                                                                             
                                           -  support: MANDATORY             
trunkMode          Boolean       1         OpenModelAttribute                 Indicator whether the Cp is in trunk mode
                                                                             
                                           -  isInvariant: false             
                                                                             
                                           -  valueRange: no range constraint
                                                                             
                                           -  support: MANDATORY             
addressType        String        1         OpenModelAttribute                 Type of address: MAC address or IP address
                                                                             
                                           -  isInvariant: false             
                                                                             
                                           -  valueRange: no range constraint
                                                                             
                                           -  support: MANDATORY             
L2addressData      L2AddressData 0..1      OpenModelAttribute                 Only present when addressType is MAC address
                                                                             
                                           -  isInvariant: false             
                                                                             
                                           -  valueRange: no range constraint
                                                                             
                                           -  support: MANDATORY             
L3addressData      L3AddressData 0..1      OpenModelAttribute                 Only present when addressType is IP address
                                                                             
                                           -  isInvariant: false             
                                                                             
                                           -  valueRange: no range constraint
                                                                             
                                           -  support: MANDATORY             
================== ============= ========= ================================== ========================================================================================================================================================================

PnfProfile
~~~~~~~~~~

The PnfProfile class describes additional data for a given PNF instance used in a DF.

Applied stereotypes:

-  Future

-  OpenModelClass

-  **support: MANDATORY**

========================== ========================= ========= ================================== ========================================================================================================================================
**Attribute Name**         **Type**                  **Mult.** **Stereotypes**                    **Description**
pnfProfileId               Identifier                1         OpenModelAttribute                 Identifier of this PnfProfile class. It uniquely identifies a PnfProfile.
                                                                                                 
                                                               -  isInvariant: false             
                                                                                                 
                                                               -  valueRange: no range constraint
                                                                                                 
                                                               -  support: MANDATORY             
pnfVirtualLinkConnectivity NsVirtualLinkConnectivity 1..\*     OpenModelAttribute                 Defines the connection information of the PNF, it contains connection relationship between a PNF connection point and a NS virtual Link.
                                                                                                 
                                                               -  isInvariant: false             
                                                                                                 
                                                               -  valueRange: no range constraint
                                                                                                 
                                                               -  support: MANDATORY             
========================== ========================= ========= ================================== ========================================================================================================================================

ResourceDescriptor
~~~~~~~~~~~~~~~~~~

Applied stereotypes:

-  OpenModelClass

-  **support: MANDATORY**

================== ======== ========= ================================== ===============
**Attribute Name** **Type** **Mult.** **Stereotypes**                    **Description**
id                 String   1         OpenModelAttribute                
                                                                        
                                      -  isInvariant: false             
                                                                        
                                      -  valueRange: no range constraint
                                                                        
                                      -  support: MANDATORY             
href               String   1         OpenModelAttribute                
                                                                        
                                      -  isInvariant: false             
                                                                        
                                      -  valueRange: no range constraint
                                                                        
                                      -  support: MANDATORY             
name               String   1         OpenModelAttribute                
                                                                        
                                      -  isInvariant: false             
                                                                        
                                      -  valueRange: no range constraint
                                                                        
                                      -  support: MANDATORY             
description        String   1         OpenModelAttribute                
                                                                        
                                      -  isInvariant: false             
                                                                        
                                      -  valueRange: no range constraint
                                                                        
                                      -  support: MANDATORY             
type               String   1         OpenModelAttribute                
                                                                        
                                      -  isInvariant: false             
                                                                        
                                      -  valueRange: no range constraint
                                                                        
                                      -  support: MANDATORY             
resourceType       String   1         OpenModelAttribute                
                                                                        
                                      -  isInvariant: false             
                                                                        
                                      -  valueRange: no range constraint
                                                                        
                                      -  support: MANDATORY             
resourceRole       String   1         OpenModelAttribute                
                                                                        
                                      -  isInvariant: false             
                                                                        
                                      -  valueRange: no range constraint
                                                                        
                                      -  support: MANDATORY             
version            String   1         OpenModelAttribute                
                                                                        
                                      -  isInvariant: false             
                                                                        
                                      -  valueRange: no range constraint
                                                                        
                                      -  support: MANDATORY             
================== ======== ========= ================================== ===============

Sap
~~~

Provides information on a Service Access Point (SAP) of a NS

**Parent class:** Cp

Applied stereotypes:

-  Future

-  OpenModelClass

-  **support: MANDATORY**

ServiceAtomicDescriptor
~~~~~~~~~~~~~~~~~~~~~~~

**Parent class:** ServiceDescriptor

Applied stereotypes:

-  OpenModelClass

-  **support: MANDATORY**

============================ ========================== ========= ================================== =====================================================================================================================================================
**Attribute Name**           **Type**                   **Mult.** **Stereotypes**                    **Description**
serviceatomicinstance        ServiceAtomicInstance      0..\*     OpenModelAttribute                
                                                                                                    
                                                                  -  isInvariant: false             
                                                                                                    
                                                                  -  valueRange: no range constraint
                                                                                                    
                                                                  -  support: MANDATORY             
invariantUuid                Uuid                       1         OpenModelAttribute                 Constant identifier of the service model.
                                                                                                    
                                                                  -  isInvariant: false             
                                                                                                    
                                                                  -  valueRange: no range constraint
                                                                                                    
                                                                  -  support: MANDATORY             
uuid                         Uuid                       1         OpenModelAttribute                 Versioned identifier of the service model (this uuid is changed for every major version of the service)
                                                                                                    
                                                                  -  isInvariant: false             
                                                                                                    
                                                                  -  valueRange: no range constraint
                                                                                                    
                                                                  -  support: MANDATORY             
name                         String                     1         OpenModelAttribute                 The name of the service model designed.
                                                                                                    
                                                                  -  isInvariant: false             
                                                                                                    
                                                                  -  valueRange: no range constraint
                                                                                                    
                                                                  -  support: MANDATORY             
description                  String                     1         OpenModelAttribute                 The description of the service model designed.
                                                                                                    
                                                                  -  isInvariant: false             
                                                                                                    
                                                                  -  valueRange: no range constraint
                                                                                                    
                                                                  -  support: MANDATORY             
category                     String                     1..\*     OpenModelAttribute                 A predefined list which identifies the construct's category. There is a predefined list of service categories.
                                                                                                    
                                                                  -  isInvariant: false             
                                                                                                    
                                                                  -  valueRange: no range constraint
                                                                                                    
                                                                  -  support: MANDATORY             
version                      String                     1         OpenModelAttribute                 The service model version.
                                                                                                    
                                                                  -  isInvariant: false             
                                                                                                    
                                                                  -  valueRange: no range constraint
                                                                                                    
                                                                  -  support: MANDATORY             
serviceType                  String                     1         OpenModelAttribute                 An optional string field defining a generic type (like category) of the service. E.g. this field can be used for defining the service as "TRANSPORT".
                                                                                                    
                                                                  -  isInvariant: false             
                                                                                                    
                                                                  -  valueRange: no range constraint
                                                                                                    
                                                                  -  support: MANDATORY             
serviceRole                  String                     0..1      OpenModelAttribute                 An optional string field for shortcode that defines the function that the service is providing. E.g. "MISVPN" or "AIM".
                                                                                                    
                                                                  -  isInvariant: false             
                                                                                                    
                                                                  -  valueRange: no range constraint
                                                                                                    
                                                                  -  support: MANDATORY             
icon                         String                     1         OpenModelAttribute                 The icon path of the service.
                                                                                                    
                                                                  -  isInvariant: false             
                                                                                                    
                                                                  -  valueRange: no range constraint
                                                                                                    
                                                                  -  support: MANDATORY             
serviceComponentUuid         Uuid                       1         OpenModelAttribute                 The service component descriptor UUIDs that the service includes (relationhip to Service Component).
                                                                                                    
                                                                  -  isInvariant: false             
                                                                                                    
                                                                  -  valueRange: no range constraint
                                                                                                    
                                                                  -  support: MANDATORY             
\_serviceInstance            ServiceInstance            0..\*     OpenModelAttribute                
                                                                                                    
                                                                  -  isInvariant: false             
                                                                                                    
                                                                  -  valueRange: no range constraint
                                                                                                    
                                                                  -  support: MANDATORY             
\_serviceComponentDescriptor ServiceComponentDescriptor 1..\*     OpenModelAttribute                
                                                                                                    
                                                                  -  isInvariant: false             
                                                                                                    
                                                                  -  valueRange: no range constraint
                                                                                                    
                                                                  -  support: MANDATORY             
attachment                   Attachment                 0..\*     OpenModelAttribute                
                                                                                                    
                                                                  -  isInvariant: false             
                                                                                                    
                                                                  -  valueRange: no range constraint
                                                                                                    
                                                                  -  support: MANDATORY             
serviceinstance              ServiceInstance            0..\*     OpenModelAttribute                
                                                                                                    
                                                                  -  isInvariant: false             
                                                                                                    
                                                                  -  valueRange: no range constraint
                                                                                                    
                                                                  -  support: MANDATORY             
attachment                   Attachment                 1..\*     OpenModelAttribute                
                                                                                                    
                                                                  -  isInvariant: false             
                                                                                                    
                                                                  -  valueRange: no range constraint
                                                                                                    
                                                                  -  support: MANDATORY             
resourcedescriptor           ResourceDescriptor         0..1      OpenModelAttribute                
                                                                                                    
                                                                  -  isInvariant: false             
                                                                                                    
                                                                  -  valueRange: no range constraint
                                                                                                    
                                                                  -  support: MANDATORY             
============================ ========================== ========= ================================== =====================================================================================================================================================

ServiceAtomicInstance
~~~~~~~~~~~~~~~~~~~~~

**Parent class:** ServiceInstance

Applied stereotypes:

-  OpenModelClass

-  **support: MANDATORY**

ServiceCandidate (ServiceCatalogItem)
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

A ServiceCandidate (ServiceCatalogItem) is an entity that makes a ServiceSpecification available to a catalog. A ServiceCandidate and its associated ServiceSpecification may be "published" (made visible) in any number of ServiceCatalogs, or in none. One ServiceSpecification can be composed of other ServiceSpecifications. These ServiceSpecifications may also be published.

Applied stereotypes:

-  OpenModelClass

-  **support: MANDATORY**

================== ======== ========= ================================== =================================================================================================
**Attribute Name** **Type** **Mult.** **Stereotypes**                    **Description**
ID                 String   1         OpenModelAttribute                 A unique identifier for the ServiceCandidate
                                                                        
                                      -  isInvariant: false             
                                                                        
                                      -  valueRange: no range constraint
                                                                        
                                      -  support: MANDATORY             
name               String   1         OpenModelAttribute                 A word or phrase that a ServiceCandidate is known and distinguished from other ServiceCandidates.
                                                                        
                                      -  isInvariant: false             
                                                                        
                                      -  valueRange: no range constraint
                                                                        
                                      -  support: MANDATORY             
description        String   1         OpenModelAttribute                 A narrative that explains the ServiceCandidate.
                                                                        
                                      -  isInvariant: false             
                                                                        
                                      -  valueRange: no range constraint
                                                                        
                                      -  support: MANDATORY             
validFor           EDate    1         OpenModelAttribute                 The period of time during which the ServiceCandidate is applicable.
                                                                        
                                      -  isInvariant: false             
                                                                        
                                      -  valueRange: no range constraint
                                                                        
                                      -  support: MANDATORY             
status             String   1         OpenModelAttribute                 The condition at which the ServiceCandidate exists such as planned, active and Obsolete.
                                                                        
                                      -  isInvariant: false             
                                                                        
                                      -  valueRange: no range constraint
                                                                        
                                      -  support: MANDATORY             
================== ======== ========= ================================== =================================================================================================

ServiceCatalog
~~~~~~~~~~~~~~

A ServiceCatalog is a collection of ServiceCandidates representing ServiceSpecifications. ServiceCandidates define the underlying services that support a ProductOffering. ServiceCandidates are exposed to one or more Product Catalogs to be utilized to configure one or more ProductOfferings. ServiceCandidates can be exposed to one or more Service Catalogs to be utilized or incorporated in one or more ServiceCandidates. A collection may consist of similar ServiceCandidates, such as a collection of broadband ServiceCatalogCandidates or a collection of wireless ServiceCatalogCandidates. A Service Catalog contents can expose a collection of ServiceCandidates to be utilized internal/external to an enterprise.

Applied stereotypes:

-  OpenModelClass

-  **support: MANDATORY**

ServiceCharacteristic
~~~~~~~~~~~~~~~~~~~~~

Applied stereotypes:

-  OpenModelClass

-  **support: MANDATORY**

================== ======== ========= ================================== ===============
**Attribute Name** **Type** **Mult.** **Stereotypes**                    **Description**
name               String   1         OpenModelAttribute                
                                                                        
                                      -  isInvariant: false             
                                                                        
                                      -  valueRange: no range constraint
                                                                        
                                      -  support: MANDATORY             
valueType          String   1         OpenModelAttribute                
                                                                        
                                      -  isInvariant: false             
                                                                        
                                      -  valueRange: no range constraint
                                                                        
                                      -  support: MANDATORY             
================== ======== ========= ================================== ===============

ServiceComponentDescriptor
~~~~~~~~~~~~~~~~~~~~~~~~~~

ServcieComponentDescriptor is used to model the design time representation of a service component or network service.

Applied stereotypes:

-  OpenModelClass

-  **support: MANDATORY**

============================ ========================== ========= ================================== ============================================================================================================================
**Attribute Name**           **Type**                   **Mult.** **Stereotypes**                    **Description**
invariantUuid                Uuid                       1         OpenModelAttribute                 Constant identifier of the Service Component model.
                                                                                                    
                                                                  -  isInvariant: false             
                                                                                                    
                                                                  -  valueRange: no range constraint
                                                                                                    
                                                                  -  support: MANDATORY             
uuid                         Uuid                       1         OpenModelAttribute                 Versioned identifier of the Service Component model (this uuid is changed for every major version of the service component).
                                                                                                    
                                                                  -  isInvariant: false             
                                                                                                    
                                                                  -  valueRange: no range constraint
                                                                                                    
                                                                  -  support: MANDATORY             
name                         String                     1         OpenModelAttribute                 The name of the service component.
                                                                                                    
                                                                  -  isInvariant: false             
                                                                                                    
                                                                  -  valueRange: no range constraint
                                                                                                    
                                                                  -  support: MANDATORY             
description                  String                     1         OpenModelAttribute                 The description of service component.
                                                                                                    
                                                                  -  isInvariant: false             
                                                                                                    
                                                                  -  valueRange: no range constraint
                                                                                                    
                                                                  -  support: MANDATORY             
version                      String                     1         OpenModelAttribute                 The version of service component.
                                                                                                    
                                                                  -  isInvariant: false             
                                                                                                    
                                                                  -  valueRange: no range constraint
                                                                                                    
                                                                  -  support: MANDATORY             
designer                     String                     1         OpenModelAttribute                 The designer of the service component.
                                                                                                    
                                                                  -  isInvariant: false             
                                                                                                    
                                                                  -  valueRange: no range constraint
                                                                                                    
                                                                  -  support: MANDATORY             
\_serviceComponentDescriptor ServiceComponentDescriptor 0..\*     OpenModelAttribute                
                                                                                                    
                                                                  -  isInvariant: false             
                                                                                                    
                                                                  -  valueRange: no range constraint
                                                                                                    
                                                                  -  support: MANDATORY             
\_serviceComponentInstance   ServiceComponentInstance   0..\*     OpenModelAttribute                
                                                                                                    
                                                                  -  isInvariant: false             
                                                                                                    
                                                                  -  valueRange: no range constraint
                                                                                                    
                                                                  -  support: MANDATORY             
============================ ========================== ========= ================================== ============================================================================================================================

ServiceComponentInstance
~~~~~~~~~~~~~~~~~~~~~~~~

ServiceComponentInstance is used to model the run time representation of a service component.

Applied stereotypes:

-  OpenModelClass

-  **support: MANDATORY**

========================== ======================== ========= ================================== ============================================================================================================================
**Attribute Name**         **Type**                 **Mult.** **Stereotypes**                    **Description**
instanceId                 Identifier               1         OpenModelAttribute                 Uniquely identifies this instance of a service component.
                                                                                                
                                                              -  isInvariant: false             
                                                                                                
                                                              -  valueRange: no range constraint
                                                                                                
                                                              -  support: MANDATORY             
name                       String                   1         OpenModelAttribute                 The name assigned to the service component instance.
                                                                                                
                                                              -  isInvariant: false             
                                                                                                
                                                              -  valueRange: no range constraint
                                                                                                
                                                              -  support: MANDATORY             
modelInvariantUuid         Uuid                     1         OpenModelAttribute                 Constant identifier of the service component model.
                                                                                                
                                                              -  isInvariant: false             
                                                                                                
                                                              -  valueRange: no range constraint
                                                                                                
                                                              -  support: MANDATORY             
modelUuid                  Uuid                     1         OpenModelAttribute                 Versioned identifier of the service component model (this uuid is changed for every major version of the service component).
                                                                                                
                                                              -  isInvariant: false             
                                                                                                
                                                              -  valueRange: no range constraint
                                                                                                
                                                              -  support: MANDATORY             
modelVersion               String                   1         OpenModelAttribute                 The service version in SDC catalog.
                                                                                                
                                                              -  isInvariant: false             
                                                                                                
                                                              -  valueRange: no range constraint
                                                                                                
                                                              -  support: MANDATORY             
selfLink                   Uri                      1         OpenModelAttribute                 URL to endpoint where more details can be gotten.
                                                                                                
                                                              -  isInvariant: false             
                                                                                                
                                                              -  valueRange: no range constraint
                                                                                                
                                                              -  support: MANDATORY             
orchestrationStatus        String                   1         OpenModelAttribute                 Orchestration status of the service component instance.
                                                                                                
                                                              -  isInvariant: false             
                                                                                                
                                                              -  valueRange: no range constraint
                                                                                                
                                                              -  support: MANDATORY             
description                String                   1         OpenModelAttribute                 The description of service component instance.
                                                                                                
                                                              -  isInvariant: false             
                                                                                                
                                                              -  valueRange: no range constraint
                                                                                                
                                                              -  support: MANDATORY             
\_serviceComponentInstance ServiceComponentInstance 0..\*     OpenModelAttribute                
                                                                                                
                                                              -  isInvariant: false             
                                                                                                
                                                              -  valueRange: no range constraint
                                                                                                
                                                              -  support: MANDATORY             
========================== ======================== ========= ================================== ============================================================================================================================

ServiceCompositeDescriptor
~~~~~~~~~~~~~~~~~~~~~~~~~~

**Parent class:** ServiceDescriptor

Applied stereotypes:

-  OpenModelClass

-  **support: MANDATORY**

============================ ========================== ========= ================================== =====================================================================================================================================================
**Attribute Name**           **Type**                   **Mult.** **Stereotypes**                    **Description**
servicecompositeinstance     ServiceCompositeInstance   0..\*     OpenModelAttribute                
                                                                                                    
                                                                  -  isInvariant: false             
                                                                                                    
                                                                  -  valueRange: no range constraint
                                                                                                    
                                                                  -  support: MANDATORY             
servicedescriptor            ServiceDescriptor          1..\*     OpenModelAttribute                
                                                                                                    
                                                                  -  isInvariant: false             
                                                                                                    
                                                                  -  valueRange: no range constraint
                                                                                                    
                                                                  -  support: MANDATORY             
invariantUuid                Uuid                       1         OpenModelAttribute                 Constant identifier of the service model.
                                                                                                    
                                                                  -  isInvariant: false             
                                                                                                    
                                                                  -  valueRange: no range constraint
                                                                                                    
                                                                  -  support: MANDATORY             
uuid                         Uuid                       1         OpenModelAttribute                 Versioned identifier of the service model (this uuid is changed for every major version of the service)
                                                                                                    
                                                                  -  isInvariant: false             
                                                                                                    
                                                                  -  valueRange: no range constraint
                                                                                                    
                                                                  -  support: MANDATORY             
name                         String                     1         OpenModelAttribute                 The name of the service model designed.
                                                                                                    
                                                                  -  isInvariant: false             
                                                                                                    
                                                                  -  valueRange: no range constraint
                                                                                                    
                                                                  -  support: MANDATORY             
description                  String                     1         OpenModelAttribute                 The description of the service model designed.
                                                                                                    
                                                                  -  isInvariant: false             
                                                                                                    
                                                                  -  valueRange: no range constraint
                                                                                                    
                                                                  -  support: MANDATORY             
category                     String                     1..\*     OpenModelAttribute                 A predefined list which identifies the construct's category. There is a predefined list of service categories.
                                                                                                    
                                                                  -  isInvariant: false             
                                                                                                    
                                                                  -  valueRange: no range constraint
                                                                                                    
                                                                  -  support: MANDATORY             
version                      String                     1         OpenModelAttribute                 The service model version.
                                                                                                    
                                                                  -  isInvariant: false             
                                                                                                    
                                                                  -  valueRange: no range constraint
                                                                                                    
                                                                  -  support: MANDATORY             
serviceType                  String                     1         OpenModelAttribute                 An optional string field defining a generic type (like category) of the service. E.g. this field can be used for defining the service as "TRANSPORT".
                                                                                                    
                                                                  -  isInvariant: false             
                                                                                                    
                                                                  -  valueRange: no range constraint
                                                                                                    
                                                                  -  support: MANDATORY             
serviceRole                  String                     0..1      OpenModelAttribute                 An optional string field for shortcode that defines the function that the service is providing. E.g. "MISVPN" or "AIM".
                                                                                                    
                                                                  -  isInvariant: false             
                                                                                                    
                                                                  -  valueRange: no range constraint
                                                                                                    
                                                                  -  support: MANDATORY             
icon                         String                     1         OpenModelAttribute                 The icon path of the service.
                                                                                                    
                                                                  -  isInvariant: false             
                                                                                                    
                                                                  -  valueRange: no range constraint
                                                                                                    
                                                                  -  support: MANDATORY             
serviceComponentUuid         Uuid                       1         OpenModelAttribute                 The service component descriptor UUIDs that the service includes (relationhip to Service Component).
                                                                                                    
                                                                  -  isInvariant: false             
                                                                                                    
                                                                  -  valueRange: no range constraint
                                                                                                    
                                                                  -  support: MANDATORY             
\_serviceInstance            ServiceInstance            0..\*     OpenModelAttribute                
                                                                                                    
                                                                  -  isInvariant: false             
                                                                                                    
                                                                  -  valueRange: no range constraint
                                                                                                    
                                                                  -  support: MANDATORY             
\_serviceComponentDescriptor ServiceComponentDescriptor 1..\*     OpenModelAttribute                
                                                                                                    
                                                                  -  isInvariant: false             
                                                                                                    
                                                                  -  valueRange: no range constraint
                                                                                                    
                                                                  -  support: MANDATORY             
attachment                   Attachment                 0..\*     OpenModelAttribute                
                                                                                                    
                                                                  -  isInvariant: false             
                                                                                                    
                                                                  -  valueRange: no range constraint
                                                                                                    
                                                                  -  support: MANDATORY             
serviceinstance              ServiceInstance            0..\*     OpenModelAttribute                
                                                                                                    
                                                                  -  isInvariant: false             
                                                                                                    
                                                                  -  valueRange: no range constraint
                                                                                                    
                                                                  -  support: MANDATORY             
attachment                   Attachment                 1..\*     OpenModelAttribute                
                                                                                                    
                                                                  -  isInvariant: false             
                                                                                                    
                                                                  -  valueRange: no range constraint
                                                                                                    
                                                                  -  support: MANDATORY             
resourcedescriptor           ResourceDescriptor         0..1      OpenModelAttribute                
                                                                                                    
                                                                  -  isInvariant: false             
                                                                                                    
                                                                  -  valueRange: no range constraint
                                                                                                    
                                                                  -  support: MANDATORY             
============================ ========================== ========= ================================== =====================================================================================================================================================

ServiceCompositeInstance
~~~~~~~~~~~~~~~~~~~~~~~~

**Parent class:** ServiceInstance

Applied stereotypes:

-  OpenModelClass

-  **support: MANDATORY**

================== =============== ========= ================================== ===============
**Attribute Name** **Type**        **Mult.** **Stereotypes**                    **Description**
serviceinstance    ServiceInstance 1..\*     OpenModelAttribute                
                                                                               
                                             -  isInvariant: false             
                                                                               
                                             -  valueRange: no range constraint
                                                                               
                                             -  support: MANDATORY             
================== =============== ========= ================================== ===============

ServiceDescAtomic
~~~~~~~~~~~~~~~~~

**Parent class:** ServiceDescriptor

Applied stereotypes:

-  OpenModelClass

-  **support: MANDATORY**

ServiceDescComposite
~~~~~~~~~~~~~~~~~~~~

**Parent class:** ServiceDescriptor

Applied stereotypes:

-  OpenModelClass

-  **support: MANDATORY**

.. _servicedescriptor-1:

ServiceDescriptor
~~~~~~~~~~~~~~~~~

ServiceDescriptor is used to model the design time representation of a service.

Applied stereotypes:

-  OpenModelClass

-  **support: MANDATORY**

============================ ========================== ========= ================================== =====================================================================================================================================================
**Attribute Name**           **Type**                   **Mult.** **Stereotypes**                    **Description**
invariantUuid                Uuid                       1         OpenModelAttribute                 Constant identifier of the service model.
                                                                                                    
                                                                  -  isInvariant: false             
                                                                                                    
                                                                  -  valueRange: no range constraint
                                                                                                    
                                                                  -  support: MANDATORY             
uuid                         Uuid                       1         OpenModelAttribute                 Versioned identifier of the service model (this uuid is changed for every major version of the service)
                                                                                                    
                                                                  -  isInvariant: false             
                                                                                                    
                                                                  -  valueRange: no range constraint
                                                                                                    
                                                                  -  support: MANDATORY             
name                         String                     1         OpenModelAttribute                 The name of the service model designed.
                                                                                                    
                                                                  -  isInvariant: false             
                                                                                                    
                                                                  -  valueRange: no range constraint
                                                                                                    
                                                                  -  support: MANDATORY             
description                  String                     1         OpenModelAttribute                 The description of the service model designed.
                                                                                                    
                                                                  -  isInvariant: false             
                                                                                                    
                                                                  -  valueRange: no range constraint
                                                                                                    
                                                                  -  support: MANDATORY             
category                     String                     1..\*     OpenModelAttribute                 A predefined list which identifies the construct's category. There is a predefined list of service categories.
                                                                                                    
                                                                  -  isInvariant: false             
                                                                                                    
                                                                  -  valueRange: no range constraint
                                                                                                    
                                                                  -  support: MANDATORY             
version                      String                     1         OpenModelAttribute                 The service model version.
                                                                                                    
                                                                  -  isInvariant: false             
                                                                                                    
                                                                  -  valueRange: no range constraint
                                                                                                    
                                                                  -  support: MANDATORY             
serviceType                  String                     1         OpenModelAttribute                 An optional string field defining a generic type (like category) of the service. E.g. this field can be used for defining the service as "TRANSPORT".
                                                                                                    
                                                                  -  isInvariant: false             
                                                                                                    
                                                                  -  valueRange: no range constraint
                                                                                                    
                                                                  -  support: MANDATORY             
serviceRole                  String                     0..1      OpenModelAttribute                 An optional string field for shortcode that defines the function that the service is providing. E.g. "MISVPN" or "AIM".
                                                                                                    
                                                                  -  isInvariant: false             
                                                                                                    
                                                                  -  valueRange: no range constraint
                                                                                                    
                                                                  -  support: MANDATORY             
icon                         String                     1         OpenModelAttribute                 The icon path of the service.
                                                                                                    
                                                                  -  isInvariant: false             
                                                                                                    
                                                                  -  valueRange: no range constraint
                                                                                                    
                                                                  -  support: MANDATORY             
serviceComponentUuid         Uuid                       1         OpenModelAttribute                 The service component descriptor UUIDs that the service includes (relationhip to Service Component).
                                                                                                    
                                                                  -  isInvariant: false             
                                                                                                    
                                                                  -  valueRange: no range constraint
                                                                                                    
                                                                  -  support: MANDATORY             
\_serviceInstance            ServiceInstance            0..\*     OpenModelAttribute                
                                                                                                    
                                                                  -  isInvariant: false             
                                                                                                    
                                                                  -  valueRange: no range constraint
                                                                                                    
                                                                  -  support: MANDATORY             
\_serviceComponentDescriptor ServiceComponentDescriptor 1..\*     OpenModelAttribute                
                                                                                                    
                                                                  -  isInvariant: false             
                                                                                                    
                                                                  -  valueRange: no range constraint
                                                                                                    
                                                                  -  support: MANDATORY             
attachment                   Attachment                 0..\*     OpenModelAttribute                
                                                                                                    
                                                                  -  isInvariant: false             
                                                                                                    
                                                                  -  valueRange: no range constraint
                                                                                                    
                                                                  -  support: MANDATORY             
serviceinstance              ServiceInstance            0..\*     OpenModelAttribute                
                                                                                                    
                                                                  -  isInvariant: false             
                                                                                                    
                                                                  -  valueRange: no range constraint
                                                                                                    
                                                                  -  support: MANDATORY             
attachment                   Attachment                 1..\*     OpenModelAttribute                
                                                                                                    
                                                                  -  isInvariant: false             
                                                                                                    
                                                                  -  valueRange: no range constraint
                                                                                                    
                                                                  -  support: MANDATORY             
resourcedescriptor           ResourceDescriptor         0..1      OpenModelAttribute                
                                                                                                    
                                                                  -  isInvariant: false             
                                                                                                    
                                                                  -  valueRange: no range constraint
                                                                                                    
                                                                  -  support: MANDATORY             
============================ ========================== ========= ================================== =====================================================================================================================================================

ServiceInstance
~~~~~~~~~~~~~~~

ServiceInstance is used to model the run time representation of a service.

Applied stereotypes:

-  OpenModelClass

-  **support: MANDATORY**

========================== ======================== ========= ================================== =====================================================================================================================================================
**Attribute Name**         **Type**                 **Mult.** **Stereotypes**                    **Description**
serviceInstanceId          Identifier               1         OpenModelAttribute                 Uniquely identifies this instance of a service.
                                                                                                
                                                              -  isInvariant: false             
                                                                                                
                                                              -  valueRange: no range constraint
                                                                                                
                                                              -  support: MANDATORY             
serviceInstanceName        String                   1         OpenModelAttribute                 The name assigned to the service-instance.
                                                                                                
                                                              -  isInvariant: false             
                                                                                                
                                                              -  valueRange: no range constraint
                                                                                                
                                                              -  support: MANDATORY             
serviceInstanceDescription String                   1         OpenModelAttribute                 The description assigned to the service-instance.
                                                                                                
                                                              -  isInvariant: false             
                                                                                                
                                                              -  valueRange: no range constraint
                                                                                                
                                                              -  support: MANDATORY             
modelInvariantUuid         Uuid                     1         OpenModelAttribute                 Constant identifier of the service model (relationship to service model).
                                                                                                
                                                              -  isInvariant: false             
                                                                                                
                                                              -  valueRange: no range constraint
                                                                                                
                                                              -  support: MANDATORY             
modelUuid                  Uuid                     1         OpenModelAttribute                 Versioned identifier of the service model (relationship to service model).
                                                                                                
                                                              -  isInvariant: false             
                                                                                                
                                                              -  valueRange: no range constraint
                                                                                                
                                                              -  support: MANDATORY             
modelVersion               String                   1         OpenModelAttribute                 The service model version in SDC catalog.
                                                                                                
                                                              -  isInvariant: false             
                                                                                                
                                                              -  valueRange: no range constraint
                                                                                                
                                                              -  support: MANDATORY             
serviceType                String                   0..1      OpenModelAttribute                 An optional string field defining a generic type (like category) of the service. E.g. this field can be used for defining the service as "TRANSPORT".
                                                                                                
                                                              -  isInvariant: false             
                                                                                                
                                                              -  valueRange: no range constraint
                                                                                                
                                                              -  support: MANDATORY             
serviceRole                String                   1         OpenModelAttribute                 An optional string field for shortcode that defines the function that the service is providing. E.g. "MISVPN" or "AIM".
                                                                                                
                                                              -  isInvariant: false             
                                                                                                
                                                              -  valueRange: no range constraint
                                                                                                
                                                              -  support: MANDATORY             
selfLink                   Uri                      1         OpenModelAttribute                 URL to endpoint where more details can be gotten.
                                                                                                
                                                              -  isInvariant: false             
                                                                                                
                                                              -  valueRange: no range constraint
                                                                                                
                                                              -  support: MANDATORY             
orchestrationStatus        String                   1         OpenModelAttribute                 Orchestration status of the service instance.
                                                                                                
                                                              -  isInvariant: false             
                                                                                                
                                                              -  valueRange: no range constraint
                                                                                                
                                                              -  support: MANDATORY             
serviceComponentInstanceId Identifier               1         OpenModelAttribute                 The service component instance ID that the service instance includes.
                                                                                                
                                                              -  isInvariant: false             
                                                                                                
                                                              -  valueRange: no range constraint
                                                                                                
                                                              -  support: MANDATORY             
\_serviceInstance          ServiceInstance          0..\*     OpenModelAttribute                
                                                                                                
                                                              -  isInvariant: false             
                                                                                                
                                                              -  valueRange: no range constraint
                                                                                                
                                                              -  support: MANDATORY             
\_serviceComponentInstance ServiceComponentInstance 1..\*     OpenModelAttribute                
                                                                                                
                                                              -  isInvariant: false             
                                                                                                
                                                              -  valueRange: no range constraint
                                                                                                
                                                              -  support: MANDATORY             
========================== ======================== ========= ================================== =====================================================================================================================================================

.. _serviceinstance-1:

ServiceInstance
~~~~~~~~~~~~~~~

Applied stereotypes:

-  OpenModelClass

-  **support: MANDATORY**

ServiceOrder
~~~~~~~~~~~~

A type of Request that represents a Customer Order's products decomposed into the services through which the products are realized.

Applied stereotypes:

-  OpenModelClass

-  **support: MANDATORY**

======================= ================ ========= ================================== =============================================================================================================================================================================
**Attribute Name**      **Type**         **Mult.** **Stereotypes**                    **Description**
id                      String           1         OpenModelAttribute                 Unique identifier for Interaction.
                                                                                     
                                                   -  isInvariant: false             
                                                                                     
                                                   -  valueRange: no range constraint
                                                                                     
                                                   -  support: MANDATORY             
externalId              String           1         OpenModelAttribute                 ID given by the order requester and only understandable by him (to facilitate his searches afterwards). It could an order number reference from the triggering system (OM)
                                                                                     
                                                   -  isInvariant: false             
                                                                                     
                                                   -  valueRange: no range constraint
                                                                                     
                                                   -  support: MANDATORY             
priority                OrderPriority    1         OpenModelAttribute                 A way that can be used by order requester to prioritize orders in Service Order
                                                                                     
                                                   -  isInvariant: false             
                                                                                     
                                                   -  valueRange: no range constraint
                                                                                     
                                                   -  support: MANDATORY             
description             String           1         OpenModelAttribute                 Narrative that explains the interaction and details about the interaction, such as why the interaction is taking place.
                                                                                     
                                                   -  isInvariant: false             
                                                                                     
                                                   -  valueRange: no range constraint
                                                                                     
                                                   -  support: MANDATORY             
category                String           1         OpenModelAttribute                 Used to categorize the order - Requester valued it and this category can be useful for the Service Order Management system and/or requester (e.g. "broadband", "TV option",).
                                                                                     
                                                   -  isInvariant: false             
                                                                                     
                                                   -  valueRange: no range constraint
                                                                                     
                                                   -  support: MANDATORY             
state                   OrderState       1         OpenModelAttribute                 State of the order
                                                                                     
                                                   -  isInvariant: false             
                                                                                     
                                                   -  valueRange: no range constraint
                                                                                     
                                                   -  support: MANDATORY             
completionDate          EDate            1         OpenModelAttribute                 The date on which an interaction is closed or completed.
                                                                                     
                                                   -  isInvariant: false             
                                                                                     
                                                   -  valueRange: no range constraint
                                                                                     
                                                   -  support: MANDATORY             
requestedStartDate      EDate            1         OpenModelAttribute                 The date that was requested to start processing the order.
                                                                                     
                                                   -  isInvariant: false             
                                                                                     
                                                   -  valueRange: no range constraint
                                                                                     
                                                   -  support: MANDATORY             
requestedCompletionDate EDate            1         OpenModelAttribute                 The date on which an interaction is closed or completed.
                                                                                     
                                                   -  isInvariant: false             
                                                                                     
                                                   -  valueRange: no range constraint
                                                                                     
                                                   -  support: MANDATORY             
expectedCompletionDate  EDate            1         OpenModelAttribute                 The date on which an interaction is expected to be completed.
                                                                                     
                                                   -  isInvariant: false             
                                                                                     
                                                   -  valueRange: no range constraint
                                                                                     
                                                   -  support: MANDATORY             
startDate               EDate            1         OpenModelAttribute                 The date on which an interaction is started.
                                                                                     
                                                   -  isInvariant: false             
                                                                                     
                                                   -  valueRange: no range constraint
                                                                                     
                                                   -  support: MANDATORY             
notificationContact     String           1         OpenModelAttribute                 Contact attached to the order to send back information regarding this order
                                                                                     
                                                   -  isInvariant: false             
                                                                                     
                                                   -  valueRange: no range constraint
                                                                                     
                                                   -  support: MANDATORY             
\_serviceOrderItem      ServiceOrderItem 1..\*     OpenModelAttribute                 Reference to ServiceOrderItem
                                                                                     
                                                   -  isInvariant: false             
                                                                                     
                                                   -  valueRange: no range constraint
                                                                                     
                                                   -  support: MANDATORY             
OrderDate               EDate            1         OpenModelAttribute                 The date the order was placed.
                                                                                     
                                                   -  isInvariant: false             
                                                                                     
                                                   -  valueRange: no range constraint
                                                                                     
                                                   -  support: MANDATORY             
======================= ================ ========= ================================== =============================================================================================================================================================================

ServiceOrderItem
~~~~~~~~~~~~~~~~

The purpose for the ServiceOrder expressed in terms of a ServiceSpecification or a Service.

Applied stereotypes:

-  OpenModelClass

-  **support: MANDATORY**

================== ========== ========= ================================== =============================================================================================
**Attribute Name** **Type**   **Mult.** **Stereotypes**                    **Description**
id                 String     1         OpenModelAttribute                 Identifier of the line item (generally it is a sequence number 01, 02, 03, ...).
                                                                          
                                        -  isInvariant: false             
                                                                          
                                        -  valueRange: no range constraint
                                                                          
                                        -  support: MANDATORY             
action             Action     1         OpenModelAttribute                 The action to take for an InteractionItem, such as add, change, remove.
                                                                          
                                        -  isInvariant: false             
                                                                          
                                        -  valueRange: no range constraint
                                                                          
                                        -  support: MANDATORY             
state              OrderState 1         OpenModelAttribute                 State of the order item: described in the state machine diagram. This is the requested state.
                                                                          
                                        -  isInvariant: false             
                                                                          
                                        -  valueRange: no range constraint
                                                                          
                                        -  support: MANDATORY             
Quantity           Integer    1         OpenModelAttribute                 Quantity of an interaction item involved in an interaction.
                                                                          
                                        -  isInvariant: false             
                                                                          
                                        -  valueRange: no range constraint
                                                                          
                                        -  support: MANDATORY             
================== ========== ========= ================================== =============================================================================================

Value
~~~~~

Applied stereotypes:

-  OpenModelClass

-  **support: MANDATORY**

================== ======== ========= ================================== ==========================================
**Attribute Name** **Type** **Mult.** **Stereotypes**                    **Description**
value              String   1         OpenModelAttribute                 The value of a given ServiceCharacteristic
                                                                        
                                      -  isInvariant: false             
                                                                        
                                      -  valueRange: no range constraint
                                                                        
                                      -  support: MANDATORY             
================== ======== ========= ================================== ==========================================

VirtualLinkProfile
~~~~~~~~~~~~~~~~~~

The VirtualLinkProfile class specifies a profile for instantiating VLs of a particular NS DF according to a specific VLD and VL DF.

Applied stereotypes:

-  Future

-  OpenModelClass

-  **support: MANDATORY**

=============================== =============================== ========= ================================== ==============================================================================================================================================================================================================================================
**Attribute Name**              **Type**                        **Mult.** **Stereotypes**                    **Description**
virtualLinkProfileId            Identifier                      1         OpenModelAttribute                 Uniquely identifies this VirtualLinkProfile class.
                                                                                                            
                                                                          -  isInvariant: false             
                                                                                                            
                                                                          -  valueRange: no range constraint
                                                                                                            
                                                                          -  support: MANDATORY             
flavourId                       VirtualLinkDf                   1         OpenModelAttribute                 Identifies a flavour within the VLD.
                                                                                                            
                                                                          -  isInvariant: false             
                                                                                                            
                                                                          -  valueRange: no range constraint
                                                                                                            
                                                                          -  support: MANDATORY             
localAffinityOrAntiAffinityRule LocalAffinityOrAntiAffinityRule 0..\*     OpenModelAttribute                 Specifies affinity and anti-affinity rules applicable between VLs instantiated from the referenced VLD.
                                                                                                            
                                                                          -  isInvariant: false             
                                                                                                            
                                                                          -  valueRange: no range constraint
                                                                                                            
                                                                          -  support: MANDATORY             
affinityOrAntiAffinityGroupId   AffinityOrAntiAffinityGroup     0..\*     OpenModelAttribute                 Identifies an affinity or anti-affinity group the VLs instantiated according to the VlProfile belong to.
                                                                                                             NOTE : Each identifier references an affinity or anti-affinity group which expresses affinity or anti-affinity relationship between the VL(s) using this VirtualLinkProfile and the VL(s) using other VirtualLinkProfile(s) in the same group.
                                                                          -  isInvariant: false             
                                                                                                            
                                                                          -  valueRange: no range constraint
                                                                                                            
                                                                          -  support: MANDATORY             
maxBitrateRequirements          LinkBitrateRequirements         1         OpenModelAttribute                 Specifies the maximum bitrate requirements for a VL instantiated according to this profile.
                                                                                                             NOTE: These attributes are used to control scaling boundaries.
                                                                          -  isInvariant: false             
                                                                                                            
                                                                          -  valueRange: no range constraint
                                                                                                            
                                                                          -  support: MANDATORY             
minBitrateRequirements          LinkBitrateRequirements         1         OpenModelAttribute                 Specifies the minimum bitrate requirements for a VL instantiated according to this profile.
                                                                                                             NOTE: These attributes are used to control scaling boundaries.
                                                                          -  isInvariant: false             
                                                                                                            
                                                                          -  valueRange: no range constraint
                                                                                                            
                                                                          -  support: MANDATORY             
\_nsVirtualLinkDesc             NsVirtualLinkDesc               1         OpenModelAttribute                 Uniquely references a VLD.
                                                                                                            
                                                                          -  isInvariant: false             
                                                                                                            
                                                                          -  valueRange: no range constraint
                                                                                                            
                                                                          -  support: MANDATORY             
=============================== =============================== ========= ================================== ==============================================================================================================================================================================================================================================

VnfProfile
~~~~~~~~~~

The VnfProfile class specifies a profile for instantiating VNFs of a particular NS DF according to a specific VNFD and VNF DF.

**Parent class:** NsOrVnfProfile

Applied stereotypes:

-  Future

-  OpenModelClass

-  **support: MANDATORY**

=============================== =============================== ========= ================================== ==================================================================================================================================================================================================================================================================
**Attribute Name**              **Type**                        **Mult.** **Stereotypes**                    **Description**
vnfProfileId                    Identifier                      1         OpenModelAttribute                 Identifier of this vnfProfile class. It uniquely identifies a VnfProfile.
                                                                                                            
                                                                          -  isInvariant: false             
                                                                                                            
                                                                          -  valueRange: no range constraint
                                                                                                            
                                                                          -  support: MANDATORY             
instantiationLevel              Identifier                      0..1      OpenModelAttribute                 Identifier of the instantiation level of the VNF DF to be used for instantiation.
                                                                                                             If not present, the default instantiation level as declared in the VNFD shall be used.
                                                                          -  isInvariant: false             
                                                                                                            
                                                                          -  valueRange: no range constraint
                                                                                                            
                                                                          -  support: MANDATORY             
minNumberOfInstances            Integer                         1         OpenModelAttribute                 Minimum number of instances of the VNF based on this VNFD that is permitted to exist for this VnfProfile.
                                                                                                            
                                                                          -  isInvariant: false             
                                                                                                            
                                                                          -  valueRange: no range constraint
                                                                                                            
                                                                          -  support: MANDATORY             
maxNumberOfInstances            Integer                         1         OpenModelAttribute                 Maximum number of instances of the VNF based on this VNFD that is permitted to exist for this VnfProfile.
                                                                                                            
                                                                          -  isInvariant: false             
                                                                                                            
                                                                          -  valueRange: no range constraint
                                                                                                            
                                                                          -  support: MANDATORY             
localAffinityOrAntiAffinityRule LocalAffinityOrAntiAffinityRule 0..\*     OpenModelAttribute                 Specifies affinity and anti-affinity rules applicable between VNF instances created from this profile.
                                                                                                            
                                                                          -  isInvariant: false             
                                                                                                            
                                                                          -  valueRange: no range constraint
                                                                                                            
                                                                          -  support: MANDATORY             
affinityOrAntiAffinityGroupId   invalid                         1         OpenModelAttribute                 Identifier(s) of the affinity or anti-affinity group(s) the VnfProfile belongs to.
                                                                                                             NOTE: Each identifier references an affinity or anti-affinity group which expresses affinity or anti-affinity relationships between the VNF instance(s) created using this VnfProfile and the VNF instance(s) created using other VnfProfile(s) in the same group.
                                                                          -  isInvariant: false             
                                                                                                            
                                                                          -  valueRange: no range constraint
                                                                                                            
                                                                          -  support: MANDATORY             
nsVirtualLinkConnectivity       NsVirtualLinkConnectivity       1..\*     OpenModelAttribute                 Defines the connection information of the VNF, it contains connection relationship between a VNF connection point and a NS virtual Link.
                                                                                                            
                                                                          -  isInvariant: false             
                                                                                                            
                                                                          -  valueRange: no range constraint
                                                                                                            
                                                                          -  support: MANDATORY             
\_vnfDf                         VnfDf                           1         OpenModelAttribute                 Identifies a flavour within the VNFD.
                                                                                                            
                                                                          -  isInvariant: false             
                                                                                                            
                                                                          -  valueRange: no range constraint
                                                                                                            
                                                                          -  support: MANDATORY             
\_vnfd                          Vnfd                            0..1      OpenModelAttribute                 Reference to the VNFD.
                                                                                                            
                                                                          -  isInvariant: false             
                                                                                                            
                                                                          -  valueRange: no range constraint
                                                                                                            
                                                                          -  support: MANDATORY             
=============================== =============================== ========= ================================== ==================================================================================================================================================================================================================================================================

Vnffg
~~~~~

A graph of logical links connecting NF nodes,where at least one node is a VNF, for the purpose of describing traffic flow between these network functions

Applied stereotypes:

-  Future

-  OpenModelClass

-  **support: MANDATORY**

================== ======== ========= ================================== ============================================================================================================
**Attribute Name** **Type** **Mult.** **Stereotypes**                    **Description**
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
cpId               invalid  1         OpenModelAttribute                 Identifiers of the CP instances attached to the constituent VNFs and PNFs or the sap instances of the VNFFG.
                                                                         NOTE: It indicates an exhaustive list of all the CP instances and SAP instances of the VNFFG.
                                      -  isInvariant: false             
                                                                        
                                      -  valueRange: no range constraint
                                                                        
                                      -  support: MANDATORY             
nfp                invalid  1         OpenModelAttribute                 Information on the NFPs of this VNFFG.
                                                                        
                                      -  isInvariant: false             
                                                                        
                                      -  valueRange: no range constraint
                                                                        
                                      -  support: MANDATORY             
================== ======== ========= ================================== ============================================================================================================

Data Types
----------

NsToLevelMapping
~~~~~~~~~~~~~~~~

The NsToLevelMapping datatype specifies the profile to be used for a nested NS involved in a given NS level and the required number of instances.

================== ======== ========= ========== ================================== =================================================================================================================================================================================================================================================================================================================================================================================================================================================================
**Attribute Name** **Type** **Mult.** **Access** **Stereotypes**                    **Description**
nsProfileId        invalid  1         RW         OpenModelAttribute                 Identifies the profile to be used for a nested NS involved in the NS level.
                                                                                   
                                                 -  isInvariant: false             
                                                                                   
                                                 -  valueRange: no range constraint
                                                                                   
                                                 -  support: MANDATORY             
numberOfInstances  Integer  1         RW         OpenModelAttribute                 Specifies the number of nested NS instances required for the NS scale level.
                                                                                    NOTE 1: It shall be in the range of minNumberOfInstances-maxNumberOfInstances, as specified in the referenced NsProfile.
                                                 -  isInvariant: false              NOTE 2: When the corresponding NS level is used in the context of NS instantiation, the numberOfInstances attribute specifies the number of nested NS instances to be deployed.
                                                                                    NOTE 3: When the corresponding NS level is used in the context of NS scaling, the numberOfInstances attribute does not specify the number of nested NS instances to be added/removed when reaching that NS scale level. The actual number of nested NS instances to be added/removed can be derived by subtracting the numberOfInstances declared in the source NS scale level from the numberOfInstances declared in the target NS level of the scaling request.
                                                 -  valueRange: no range constraint
                                                                                   
                                                 -  support: MANDATORY             
================== ======== ========= ========== ================================== =================================================================================================================================================================================================================================================================================================================================================================================================================================================================

NsVirtualLinkConnectivity
~~~~~~~~~~~~~~~~~~~~~~~~~

The NsVirtuallLinkConnectivity datatype describes connection information between a connection point and a NS virtual Link.

==================== ======== ========= ========== ================================== =====================================================================================================================================================================================
**Attribute Name**   **Type** **Mult.** **Access** **Stereotypes**                    **Description**
virtualLinkProfileId invalid  1         RW         OpenModelAttribute                 Reference an NS VL profile.
                                                                                     
                                                   -  isInvariant: false             
                                                                                     
                                                   -  valueRange: no range constraint
                                                                                     
                                                   -  support: MANDATORY             
cpdId                invalid  1         RW         OpenModelAttribute                 References the descriptor of a connection point on a VNF/PNF or a SAP which connects to virtual links instantiated from the profile identified in the virtualLinkProfileId attribute.
                                                                                     
                                                   -  isInvariant: false             
                                                                                     
                                                   -  valueRange: no range constraint
                                                                                     
                                                   -  support: MANDATORY             
==================== ======== ========= ========== ================================== =====================================================================================================================================================================================

TimePeriod
~~~~~~~~~~

A base / value business entity used to represent a period of time, between two timepoints

================== ======== ========= ========== ================================== =================================================
**Attribute Name** **Type** **Mult.** **Access** **Stereotypes**                    **Description**
startDateTime      EDate    1         RW         OpenModelAttribute                 An instant of time, starting at the TimePeriod
                                                                                    Notes:
                                                 -  isInvariant: false              If null, then represents to the beginning of time
                                                                                   
                                                 -  valueRange: no range constraint
                                                                                   
                                                 -  support: MANDATORY             
endDateTime        EDate    1         RW         OpenModelAttribute                 An instant of time, ending at the TimePeriod:
                                                                                    Notes:
                                                 -  isInvariant: false              If null, then represents to the end of time
                                                                                   
                                                 -  valueRange: no range constraint
                                                                                   
                                                 -  support: MANDATORY             
================== ======== ========= ========== ================================== =================================================

VirtualLinkToLevelMapping
~~~~~~~~~~~~~~~~~~~~~~~~~

The VirtualLinkToLevelMapping datatype specifies the profile to be used for a VL involved in a given NS level and bitrate requirements.

==================== ======== ========= ========== ================================== =====================================================================================================================================
**Attribute Name**   **Type** **Mult.** **Access** **Stereotypes**                    **Description**
virtualLinkProfileId invalid  1         RW         OpenModelAttribute                 Identifies the profile to be used for a VL involved in an NS level.
                                                                                     
                                                   -  isInvariant: false             
                                                                                     
                                                   -  valueRange: no range constraint
                                                                                     
                                                   -  support: MANDATORY             
bitRateRequirements  invalid  1         RW         OpenModelAttribute                 Specifies the bit rate requirements for the NS level.
                                                                                      NOTE: It shall be in the range of minBitrateRequirements - maxBitrateRequirements, as specified in the referenced VirtualLinkProfile.
                                                   -  isInvariant: false             
                                                                                     
                                                   -  valueRange: no range constraint
                                                                                     
                                                   -  support: MANDATORY             
==================== ======== ========= ========== ================================== =====================================================================================================================================

VnfIndicatorData
~~~~~~~~~~~~~~~~

The VnfIndicatorData datatype identifies a VNF indicator in a VNFD.

================== ======== ========= ========== ================================== ===========================================
**Attribute Name** **Type** **Mult.** **Access** **Stereotypes**                    **Description**
vnfdId             invalid  1         RW         OpenModelAttribute                 Identifies a VNFD.
                                                                                   
                                                 -  isInvariant: false             
                                                                                   
                                                 -  valueRange: no range constraint
                                                                                   
                                                 -  support: MANDATORY             
vnfIndicator       invalid  1         RW         OpenModelAttribute                 Identifies a VNF indicator within the VNFD.
                                                                                   
                                                 -  isInvariant: false             
                                                                                   
                                                 -  valueRange: no range constraint
                                                                                   
                                                 -  support: MANDATORY             
================== ======== ========= ========== ================================== ===========================================

VnfToLevelMapping
~~~~~~~~~~~~~~~~~

The VnfToLevelMapping datatype specifies the profile to be used for a VNF involved in a given NS level and the required number of instances.

================== ======== ========= ========== ================================== =====================================================================================================================================================================================================================================================================================================================================================================================================================================================
**Attribute Name** **Type** **Mult.** **Access** **Stereotypes**                    **Description**
vnfProfileId       invalid  1         RW         OpenModelAttribute                 Identifies the profile to be used for a VNF involved in an NS level.
                                                                                   
                                                 -  isInvariant: false             
                                                                                   
                                                 -  valueRange: no range constraint
                                                                                   
                                                 -  support: MANDATORY             
numberOfInstances  Integer  1         RW         OpenModelAttribute                 Specifies the number of VNF instances required for an NS level.
                                                                                    NOTE 1: It shall be in the range of minNumberOfInstances-maxNumberOfInstances, as specified in the referenced VnfProfile.
                                                 -  isInvariant: false              NOTE 2: When the corresponding NS level is used in the context of NS instantiation, the numberOfInstances attribute specifies the number of VNF instances to be deployed.
                                                                                    NOTE 3: When the corresponding NS level is used in the context of NS scaling, the numberOfInstances attribute does not specify the number of VNF instances to be added/removed when reaching that NS scale level. The actual number of VNF instances to be added/removed can be derived by subtracting the numberOfInstances declared in the source NS scale level from the numberOfInstances declared in the target NS level of the scaling request.
                                                 -  valueRange: no range constraint
                                                                                   
                                                 -  support: MANDATORY             
================== ======== ========= ========== ================================== =====================================================================================================================================================================================================================================================================================================================================================================================================================================================

Enumerations
------------

Action
~~~~~~

Contains Enumeration Literals:

-  ADD:

-  MODIFY:

-  DELETE:

-  NO_CHANGE:

OrderPriority
~~~~~~~~~~~~~

A way that can be used by order requester to prioritize orders in Service Order Management system (from 0 to 4: 0 is the highest priority, and 4 the lowest). It could be for example valued by BSS based on customer order requested priority.

Contains Enumeration Literals:

-  0:

-  1:

-  2:

-  3:

-  4:

.. _orderstate-1:

OrderState
~~~~~~~~~~

Contains Enumeration Literals:

-  ACKNOWLEDGED:

-  IN_PROGRESS:

-  PENDING:

-  HELD:

-  CANCELLED:

-  COMPLETED:

-  FAILED:

-  PARTIAL:

-  REJECTED:

Primitives
----------

Interfaces
----------

Signals
-------

Operations
----------
