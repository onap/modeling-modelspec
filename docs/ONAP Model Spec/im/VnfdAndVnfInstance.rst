ONAP Vnf Sub Model

1. .. rubric:: Diagrams
      :name: diagrams

   1. .. rubric:: ONAP Vnfd - Topology View
         :name: onap-vnfd---topology-view

   2. .. rubric:: ONAP Vnfd View
         :name: onap-vnfd-view

   3. .. rubric:: VNF Datatypes
         :name: vnf-datatypes

   4. .. rubric:: VNF Instance
         :name: vnf-instance

   5. .. rubric:: Vnf Deployment Flavor
         :name: vnf-deployment-flavor

   6. .. rubric:: Vnf Element Group
         :name: vnf-element-group

2. .. rubric:: Classes
      :name: classes

   7. .. rubric:: BaseConfigGroup
         :name: baseconfiggroup

Every Vnf contains a BaseConfigGroup. BaseConfigGroup may set Access
Control Lists (ACL's) and establish security groups and server groups.
BaseConfigGroup reates/establishs storage for the VM's (OpenStack
Cinder). BaseConfigGroup may establish internal networks such as OAM
(VNF Mgmt) or MNS (Maintenance & Surveillance) established. A very
simple VNF may only have a BaseConfig VnfElementGroup.

**Parent class:** VnfdElementGroup

Applied stereotypes:

-  Experimental

-  OpenModelClass

-  support: MANDATORY

   8. .. rubric:: DeploymentGroup
         :name: deploymentgroup

DeploymentGroup provides the minimum viable VDU and associated VNFC
configuration for a useable VNF. I can have a small, medium, large
deployment configuration.

**Parent class:** VnfdElementGroup

Applied stereotypes:

-  Experimental

-  OpenModelClass

-  support: MANDATORY

   9. .. rubric:: HomingGroup
         :name: hominggroup

Homing selects what cloud selection strategy will be used. HomingGroup
is used to determine where VNF's within a given group are placed with
respect to a service component. Homing strategy is as follows:
Colocation - members of the group share the same cloud region (VIM
Domain) isolation - members of the group do not share the same cloud
region.

**Parent class:** VnfdElementGroup

Applied stereotypes:

-  Experimental

-  OpenModelClass

-  support: MANDATORY

.. list-table::
   :header-rows: 1

   * - **AttributeName**
     - **Type**
     - **Mult.**
     - **Stereotypes**
     - **Description**

   * - homingStrategy
     - HomingStrategy
     - 1
     - OpenModelAttribute

       -  isInvariant: false
       -  valueRange: no range constraint
       -  support: MANDATORY
     - The homing strategy can be one of the following:
       Exclusivity
       - Resources within the cloud region are exclusive to the group
       Inclusively
       - Resources are co-located in the same cloud-region.
       Diversity
	   - Resources are geo-diverse (cannot be co-located).

   * - vnfdMembers
     - invalid
     - 1
     - OpenModelAttribute

       -  isInvariant: false
       -  valueRange: no range constraint
       -  support: MANDATORY
     -

   * - vnfdElementGroupId
     - Identifier
     - 1
     - OpenModelAttribute

       -  isInvariant: false
       -  valueRange: no range constraint
       -  support: MANDATORY

       Preliminary
     - Unique identifier of this group in the VNFD.

   * - description
     - String
     - 1
     - OpenModelAttribute

	   -  isInvariant: false
       -  valueRange: no range constraint
       -  support: MANDATORY

       Preliminary
     - Human readable description of the group.

   * - \_vdu
     - Vdu
     - 0..\*
     - OpenModelAttribute

       -  isInvariant: false
       -  valueRange: no range constraint
       -  support: MANDATORY

       Preliminary
     - References to Vdus that are part of this group.

   * - \_vnfVirtualLinkdesc
     - LinkDesc
     - 0..\*
     - OpenModelAttribute

       -  isInvariant: false
       -  valueRange: no range constraint
       -  support: MANDATORY

       Preliminary
     - References to VnfVirtualLinkDesc that are part of this group.


InstantiationLevel
~~~~~~~~~~~~~~~~~~

The InstantiationLevel class describes a given level of resources to be
instantiated within a DF in term of the number of VNFC instances to be
created from each VDU. All the VDUs referenced in the level shall be
part of the corresponding DF and their number shall be within the range
(min/max) for this DF.

Applied stereotypes:

-  Preliminary

-  OpenModelClass

-  support: MANDATORY

.. list-table::
   :header-rows: 1


   * - **AttributeName**
     - **Type**
     - **Mult.**
     - **Stereotypes**
     - **Description**

   * - levelId
     - Identifier
     - 1
     - OpenModelAttribute

       -  isInvariant: false
       -  valueRange: no range constraint
       -  support: MANDATORY

       Preliminary
     - Uniquely identifies a level with the DF.

   * - description
     - String
     - 1
     - OpenModelAttribute

       -  isInvariant: false
       -  valueRange: no range constraint
       -  support: MANDATORY

       Preliminary
     - Human readable description of the level.

   * - scaleInfo
     - ScaleInfo
     - 0..\*
     - OpenModelAttribute

       -  isInvariant: false
       -  valueRange: no range constraint
       -  support: MANDATORY

       Preliminary
     - Represents for each aspect the scale level that corresponds to this instantiationlevel.
       scaleInfo shall be present if the VNF supports scaling.

   * - \_vduLevel
     - VduLevel
     - 1..\*
     - OpenModelAttribute

       -  isInvariant: false
       -  valueRange: no range constraint
       -  support: MANDATORY

       Preliminary
     - Indicates the number of instance of this VDU to deploy for this level.

   * - virtualLinkBitRateLevel
     - VirtualLinkBitRateLevel
     - 0..\*
     - OpenModelAttribute

       -  isInvariant: false
       -  valueRange: no range constraint
       -  support: MANDATORY

       Preliminary
     - Specifies bitrate requirements applicable to virtual links created from particular virtual link descriptors for this level.
       NOTE: If not present, it is assumed that the bitrate requirements can be derived from those specified in the VduCpd instances applicable to the internal VL. If present in
       both the InstantiationLevel and the VduCpd instances applicable to the internal VL, the highest value takes precedence.

LinkDesc
~~~~~~~~

A communication channel that connects two or more devices, nodes, or entities.

**Parent class:** ResourceDesc (ResourceSpecification)

Applied stereotypes:

-  OpenModelClass

-  support: MANDATORY

-  Preliminary

.. list-table::
   :header-rows: 1

   
   * - **AttributeName**
     - **Type**
     - **Mult.**
     - **Stereotypes**
     - **Description**

   * - virtualLinkDescId
     - Identifier
     - 1
     - OpenModelAttribute

       -  isInvariant: false

       -  valueRange: no range constraint

       -  support: MANDATORY

       Preliminary
     - Unique identifier of this internal VLD in VNFD.

   * - connectivityType
     - ConnectivityType
     - 1
     - OpenModelAttribute

       -  isInvariant: false

       -  valueRange: no range constraint

       -  support: MANDATORY

       Preliminary
     - Specifies the protocol exposed by a VL and the flow pattern supported by the VL.

   * - testAccess
     - String
     - 0..\*
     - OpenModelAttribute

       -  isInvariant: false

       -  valueRange: no range constraint

       -  support: MANDATORY

       Preliminary
     - Specifies test access facilities expected on the VL (e.g. none, passive monitoring, or active (intrusive) loopbacks at endpoints).

   * - description
     - String
     - 0..1
     - OpenModelAttribute

       -  isInvariant: false

       -  valueRange: no range constraint

       -  support: MANDATORY

       Preliminary
     - Provides human-readable information on the purpose of the VL (e.g. control plane traffic).

   * - monitoringParameter
     - MonitoringParameter
     - 0..\*
     - OpenModelAttribute

       -  isInvariant: false

       -  valueRange: no range constraint

       -  support: MANDATORY

       Preliminary
     - Defines the virtualised resources monitoring parameters on VLD level.

   * - \_virtuaLlinkDescFlavour
     - VirtualLinkDescFlavour
     - 1..\*
     - OpenModelAttribute

       -  isInvariant: false

       -  valueRange: no range constraint

       -  support: MANDATORY

       Preliminary
     - Describes a specific flavour of the VL with specific bitrate requirements.   

	 
PlacementGroup
~~~~~~~~~~~~~~

**Parent class:** VnfdElementGroup

Applied stereotypes:

-  Experimental

-  OpenModelClass

-  support: MANDATORY

.. list-table::
   :header-rows: 1


   * - **AttributeName**
     - **Type**
     - **Mult.**
     - **Stereotypes**
     - **Description**

   * - placementStrategy
     - PlacementStrategy
     - 1
     - OpenModelAttribute

       -  isInvariant: false
       -  valueRange: no range constraint
       -  support: MANDATORY
     -

   * - strategScope
     - invalid
     - 1
     - OpenModelAttribute

       -  isInvariant: false
       -  valueRange: no range constraint
       -  support: MANDATORY
     -

   * - vnfdElementGroupId
     - Identifier
     - 1
     - OpenModelAttribute

       -  isInvariant: false
       -  valueRange: no range constraint
       -  support: MANDATORY

       Preliminary
     - Unique identifier of this group in the VNFD.

   * - description
     - String
     - 1
     - OpenModelAttribute

       -  isInvariant: false
       -  valueRange: no range constraint
       -  support: MANDATORY

       Preliminary
     - Human readable description of the group.

   * - \_vdu
     - Vdu
     - 0..\*
     - OpenModelAttribute

       -  isInvariant: false
       -  valueRange: no range constraint
       -  support: MANDATORY

       Preliminary
     - References to Vdus that are part of this group.

   * - \_vnfVirtualLinkdesc
     - LinkDesc
     - 0..\*
     - OpenModelAttribute

       -  isInvariant: false
       -  valueRange: no range constraint
       -  support: MANDATORY

       Preliminary
     - References to VnfVirtualLinkDesc that are part of this group.

	 
13. .. rubric:: ScalingAspect
       :name: scalingaspect

The ScalingAspect class describes the details of an aspect used for
horizontal scaling.

Applied stereotypes:

-  Experimental

-  OpenModelClass

-  support: MANDATORY

   14. .. rubric:: ScalingGroup
          :name: scalinggroup

A ScalingGroup determines which VNFC's (VDU's) are scaled together based
on demand.

**Parent class:** VnfdElementGroup

Applied stereotypes:

-  Experimental

-  OpenModelClass

-  support: MANDATORY

   15. .. rubric:: SwImageDesc
          :name: swimagedesc

The SwImageDesc information element describes requested additional
capability for a particular VDU. Such a capability may be for
acceleration or specific tasks. Storage not necessarily related to the
compute, may be Network Attached Storage (NAS) References:
tosca-nfv-YAML-v1.0-wd05-rev02 ETSI GS NFV-IFA 011 V2.1.3

Applied stereotypes:

-  Preliminary

-  OpenModelClass

-  support: MANDATORY

.. list-table::
   :header-rows: 1


   * - **AttributeName**
     - **Type**
     - **Mult.**
     - **Stereotypes**
     - **Description**

   * - id
     - Identifier
     - 1
     - OpenModelAttribute

       -  isInvariant: false
       -  valueRange: no range constraint
       -  support: MANDATORY

       Preliminary
     - The identifier of this software image.

   * - name
     - String
     - 1
     - OpenModelAttribute

       -  isInvariant: false
       -  valueRange: no range constraint
       -  support: MANDATORY

       Preliminary
     - The name of this software image.

   * - version
     - String
     - 1
     - OpenModelAttribute

       -  isInvariant: false
       -  valueRange: no range constraint
       -  support: MANDATORY

       Preliminary
     - The version of this software image.

   * - checksum
     - String
     - 1
     - OpenModelAttribute

       -  isInvariant: false
       -  valueRange: no range constraint
       -  support: MANDATORY

       Preliminary
     - The checksum of the software image file.

   * - containerFormat
     - String
     - 1
     - OpenModelAttribute

       -  isInvariant: false
       -  valueRange: no range constraint
       -  support: MANDATORY

       Preliminary
     - The container format describes the container file format in which software image is provided.

   * - diskFormat
     - String
     - 1
     - OpenModelAttribute

       -  isInvariant: false
       -  valueRange: no range constraint
       -  support: MANDATORY

       Preliminary
     - The disk format of a software image is the format of the underlying disk image.

   * - minRam
     - Number
     - 0..1
     - OpenModelAttribute

       -  isInvariant: false
       -  valueRange: no range constraint
       -  support: MANDATORY

       Preliminary
     - The minimal RAM requirement for this software image. The value of the "size" attribute of VirtualMemoryData of the Vdu referencing this
       SwImageDesc shall not be smaller than the value of minRam.

   * - minDisk
     - Number
     - 1
     - OpenModelAttribute

       -  isInvariant: false
       -  valueRange: no range constraint
       -  support: MANDATORY

       Preliminary
     - The minimal disk size requirement for this software image. The value of the "size of storage" attribute of the
       VirtualStorageDesc referencing this SwImageDesc shall not be smaller than the value of minDisk.

   * - size
     - Number
     - 1
     - OpenModelAttribute

       -  isInvariant: false
       -  valueRange: no range constraint
       -  support: MANDATORY

       Preliminary
     - The size of the software image.

   * - operatingSystem
     - String
     - 0..1
     - OpenModelAttribute

       -  isInvariant: false
       -  valueRange: no range constraint
       -  support: MANDATORY

       Preliminary
     - Identifies the operating system used in the software image. This attribute may also identify if a 32 bit or 64 bit software image is used.
       support:

   * - supportedVirtualisationEnvironment
     - String
     - 0..\*
     - OpenModelAttribute

       -  isInvariant: false
       -  valueRange: no range constraint
       -  support: MANDATORY

       Preliminary
     - Identifies the virtualisation environments (e.g. hypervisor) compatible with this software image.

   * - swImage
     - Identifier
     - 1
     - OpenModelAttribute

       -  isInvariant: false
       -  valueRange: no range constraint
       -  support: MANDATORY

       Preliminary
     - The minimal disk size requirement for this software image. The value of the "size of storage" attribute of the VirtualStorageDesc referencing this SwImageDesc
       shall not be smaller than the value of minDisk.


Vdu
~~~

The Virtualisation Deployment Unit (VDU) is a construct supporting the
description of the deployment and operational behavior of a VNFC. A VNFC
instance created based on the VDU maps to a single virtualisation
container (e.g. a VM). A VNFC will only be in one VNFDesc. If a vendor
wants to use the VNFC in mupliple VNFDesc (their product) they can do
so, but it will be 'repeated'. References:
tosca-nfv-YAML-v1.0-wd05-rev02 ETSI GS NFV-IFA 011 V2.1.3

Applied stereotypes:

-  Preliminary
-  OpenModelClass
-  support: MANDATORY

.. list-table::
   :header-rows: 1


   * - **AttributeName**
     - **Type**
     - **Mult.**
     - **Stereotypes**
     - **Description**

   * - vduId
     - Identifier
     - 1
     - OpenModelAttribute

       -  isInvariant: false
       -  valueRange: no range constraint
       -  support: MANDATORY

       Preliminary
     - Unique identifier of this Vdu in VNFD.

   * - name
     - String
     - 1
     - OpenModelAttribute

       -  isInvariant: false
       -  valueRange: no range constraint
       -  support: MANDATORY

       Preliminary
     - Human readable name of the Vdu.

   * - description
     - String
     - 1
     - OpenModelAttribute

       -  isInvariant: false
       -  valueRange: no range constraint
       -  support: MANDATORY

       Preliminary
     - Human readable description of the Vdu.

   * - bootOrder
     - KeyValuePair
     - 0..\*
     - OpenModelAttribute

       -  isInvariant: false
       -  valueRange: no range constraint
       -  support: MANDATORY

       Preliminary
     - Boot order of valid boot devices.
       NOTE: If no boot order is defined the default boot order defined in the VIM or NFVI shall be used.

   * - nfviConstraint
     - KeyValuePair
     - 0..\*
     - OpenModelAttribute

       -  isInvariant: false
       -  valueRange: no range constraint
       -  support: MANDATORY

       Preliminary
     - Describes constraints on the NFVI for the VNFC instance(s) created from this Vdu. For example, aspects of a secure hosting environment
       for the VNFC instance that involve additional entities or processes.
       NOTE: These are constraints other than stipulating that a VNFC instance has access to a certain resource, as a prerequisite to instantiation.
       The attributes virtualComputeDesc and virtualStorageDesc define the resources required for instantiation of the VNFC instance.

   * - monitoringParameter
     - MonitoringParameter
     - 0..\*
     - OpenModelAttribute

       -  isInvariant: false
       -  valueRange: no range constraint
       -  support: MANDATORY

       Preliminary
     - Defines the virtualised resources monitoring parameters on VDU level.

   * - injectFiles
     - String
     - 0..\*
     - OpenModelAttribute

       -  isInvariant: false
       -  valueRange: no range constraint
       -  support: MANDATORY

       Preliminary
     - Describes the information (e.g. URL) about the scripts, config drive metadata, etc. which can be used during Vdu booting process.

   * - configurableProperties
     - VnfcConfigurableProperties
     - 1
     - OpenModelAttribute

       -  isInvariant: false
       -  valueRange: no range constraint
       -  support: MANDATORY

       Preliminary
     - Describes the configurable properties of all VNFC instances based on this VDU.

   * - \_vduCpd
     - VduCpd
     - 1
     - OpenModelAttribute

       -  isInvariant: false
       -  valueRange: no range constraint
       -  support: MANDATORY

       Preliminary
     - Describes network connectivity between a VNFC instance (based on this Vdu) and an Virtual Link (VL).

   * - \_virtualComputeDesc
     - VirtualComputeDesc
     - 1..\*
     - OpenModelAttribute

       -  isInvariant: false
       -  valueRange: no range constraint
       -  support: MANDATORY

       Preliminary
     - Describes CPU, Memory and acceleration requirements of the Virtualisation Container realising this Vdu.

   * - \_virtualStorageDesc
     - VirtualStorageDesc
     - 0..\*
     - OpenModelAttribute

       -  isInvariant: false
       -  valueRange: no range constraint
       -  support: MANDATORY

       Preliminary
     - Describes storage requirements for a VirtualStorage instance attached to the virtualisation container created from
       virtualComputeDesc defined for this Vdu.

   * - \_swImageDesc
     - SwImageDesc
     - 0..1
     - OpenModelAttribute

       -  isInvariant: false
       -  valueRange: no range constraint
       -  support: MANDATORY

       Preliminary
     - Describes the software image which is directly loaded on the virtualisation
       container realising this Vdu.
       NOTE: More software images can be attached to the virtualisation container using VirtualStorage resources.


VduCpd
~~~~~~

A VduCpd information element is a type of Cpd and describes network
connectivity between a VNFC instance (based on this VDU) and an internal
VL.

**Parent class:** Cpd

Applied stereotypes:

-  Preliminary

-  OpenModelClass

-  support: MANDATORY

.. list-table::
   :header-rows: 1


   * - **AttributeName**
     - **Type**
     - **Mult.**
     - **Stereotypes**
     - **Description**

   * - bitrateRequirement
     - Number
     - 0..1
     - OpenModelAttribute

       -  isInvariant: false
       -  valueRange: no range constraint
       -  support: MANDATORY

       Preliminary
     - Bitrate requirement on this CP.

   * - vnicName
     - String
     - 0..1
     - OpenModelAttribute

       -  isInvariant: false
       -  valueRange: no range constraint
       -  support: MANDATORY

       Preliminary
     - Describes the name of the vNIC this CP attaches to, e.g. eth0. It will be configured during the Vdu booting process.

   * - vnicOrder
     - String
     - 0..1
     - OpenModelAttribute

       -  isInvariant: false
       -  valueRange: no range constraint
       -  support: MANDATORY

       Preliminary
     - Describes the order to create the vNIC within the scope of this Vdu.

   * - vnicType
     - VnicType
     - 0..1
     - OpenModelAttribute

       -  isInvariant: false
       -  valueRange: no range constraint
       -  support: MANDATORY

       Preliminary
     - Describes the type of the vNIC this CP attaches to.

   * - \_virtualNetworkInterfaceRequirements
     - VirtualNetworkInterfaceRequirements
     - 0..\*
     - OpenModelAttribute

       -  isInvariant: false
       -  valueRange: no range constraint
       -  support: MANDATORY

       Preliminary
     - Specifies requirements on a virtual network interface realising the CPs instantiated from this CPD.

   * - cpdId
     - Identifier
     - 1
     - OpenModelAttribute

       -  isInvariant: false
       -  valueRange: no range constraint
       -  support: MANDATORY

       Preliminary
     - Identifier of this Cpd information element.

   * - cpRole
     - String
     - 0..1
     - OpenModelAttribute

       -  isInvariant: false
       -  valueRange: no range constraint
       -  support: MANDATORY

       Preliminary
     - Identifies the role of the port in the context of the traffic flow
       patterns in the VNF or parent NS. For example a VNF with a tree flow
       pattern within the VNF will have legal cpRoles of ROOT and LEAF.

   * - description
     - String
     - 0..1
     - OpenModelAttribute

       -  isInvariant: false
       -  valueRange: no range constraint
       -  support: MANDATORY

       Preliminary
     - Provides human-readable information on the purpose of the CP (e.g. CP for control plane traffic).

   * - cpProtocol
     - CpProtocolData
     - 1..\*
     - OpenModelAttribute

       -  isInvariant: false
       -  valueRange: no range constraint
       -  support: MANDATORY

       Preliminary
     - Identifies the protocol layering information the CP uses for connectivity
       purposes and associated information. There shall be one cpProtocol for each layer
       protocol as indicated by the attribute layerProtocol.
       Editor's note: the attribute "layerProtocol" still needs further discussion and not included in this table.

   * - trunkMode
     - Boolean
     - 1
     - OpenModelAttribute

       -  isInvariant: false
       -  valueRange: no range constraint
       -  support: MANDATORY

       Preliminary
     - Information about whether the CP instantiated from this CPD is in Trunk mode (802.1Q or other).

   * - allowedAddressData
     - AddressData
     - 0..\*
     - OpenModelAttribute

       -  isInvariant: false
       -  valueRange: no range constraint
       -  support: MANDATORY

       Preliminary
     - For specifying floating IP(s) to be shared among Cpds, which are reserved for vnfReservedCpd described in the VNFD.


VduLevel
~~~~~~~~

The VduLevel information element indicates for a given VDU in a given
level the number of instances to deploy.

Applied stereotypes:

-  Preliminary

-  OpenModelClass

-  support: MANDATORY

.. list-table::
   :header-rows: 1


   * - **AttributeName**
     - **Type**
     - **Mult.**
     - **Stereotypes**
     - **Description**

   * - vduId
     - Identifier
     - 1
     - OpenModelAttribute

       -  isInvariant: false
       -  valueRange: no range constraint
       -  support: MANDATORY

       Preliminary
     - Uniquely identifies a VDU.

   * - numberOfInstances
     - Integer
     - 1
     - OpenModelAttribute

       -  isInvariant: false
       -  valueRange: no range constraint
       -  support: MANDATORY

       Preliminary
     - Number of instances of VNFC based on this VDU to deploy for an instantiation level or for a scaling delta.


VduProfile
~~~~~~~~~~

The VduProfile describes additional instantiation data for a given VDU
used in a DF.

Applied stereotypes:

-  Preliminary

-  OpenModelClass

-  support: MANDATORY

.. list-table::
   :header-rows: 1


   * - **AttributeName**
     - **Type**
     - **Mult.**
     - **Stereotypes**
     - **Description**

   * - vdudId
     - Identifier
     - 1
     - OpenModelAttribute

       -  isInvariant: false
       -  valueRange: no range constraint
       -  support: MANDATORY

       Preliminary
     - Uniquely identifies a VDU.

   * - minNumberOfInstances
     - Integer
     - 1
     - OpenModelAttribute

       -  isInvariant: false
       -  valueRange: no range constraint
       -  support: MANDATORY

       Preliminary
     - Minimum number of instances of the VNFC based on this VDU that is permitted to exist for this flavour.

   * - maxNumberOfInstances
     - Integer
     - 1
     - OpenModelAttribute

       -  isInvariant: false
       -  valueRange: no range constraint
       -  support: MANDATORY

       Preliminary
     - Maximum number of instances of the VNFC based on this VDU that is permitted to exist for this flavour.

   * - localAffinityOrAntiAffinityRule
     - LocalAffinityOrAntiAffinityRule
     - 0..\*
     - OpenModelAttribute

       -  isInvariant: false
       -  valueRange: no range constraint
       -  support: MANDATORY

       Preliminary
     - Specifies affinity or anti-affinity rules applicable between the virtualisation containers (e.g. virtual machines)
       to be created based on this VDU.

   * - affinityOrAntiAffinityGroupId
     - Identifier
     - 0..\*
     - OpenModelAttribute

       -  isInvariant: false
       -  valueRange: no range constraint
       -  support: MANDATORY

       Preliminary
     - Identifier(s) of the affinity or anti-affinity group(s) the VDU belongs to.
       NOTE: Each identifier references an affinity or anti-affinity group which expresses affinity or anti-affinity
       relationships between the virtualisation container(s) (e.g. virtual machine(s)) to be created using this VDU and the
       virtualisation container(s) (e.g. virtual machine(s)) to be created using other VDU(s) in the same group.

   * - watchdog
     - String
     - 0..1
     - OpenModelAttribute

       -  isInvariant: false
       -  valueRange: no range constraint
       -  support: MANDATORY

       Preliminary
     - Watchdog action to be triggered by the VIM for the VNF in case the heart beat fails, e.g. reset or hard shutdown, etc.

   * - vmBootUpTimeOut
     - Integer
     - 0..1
     - OpenModelAttribute

       -  isInvariant: false
       -  valueRange: no range constraint
       -  support: MANDATORY

       Preliminary
     - Timeout value for the VNFM to wait before the successful booting up of the VDU.


VirtualComputeDesc
~~~~~~~~~~~~~~~~~~

The VirtualComputeDesc information element supports the specification of
requirements related to virtual compute resources.

Applied stereotypes:

-  Preliminary

-  OpenModelClass

-  support: MANDATORY

.. list-table::
   :header-rows: 1


   * - **AttributeName**
     - **Type**
     - **Mult.**
     - **Stereotypes**
     - **Description**

   * - virtualComputeDescId
     - Identifier
     - 1
     - OpenModelAttribute

       -  isInvariant: false
       -  valueRange: no range constraint
       -  support: MANDATORY

       Preliminary
     - Unique identifier of this VirtualComputeDesc in the VNFD

   * - logicalNode
     - LogicalNodeData
     - 1..\*
     - OpenModelAttribute

       -  isInvariant: false
       -  valueRange: no range constraint
       -  support: MANDATORY

       Preliminary
     - The logical Node requirements.

   * - requestAdditionalCapabilities
     - RequestedAdditionalCapabilityData
     - 0..\*
     - OpenModelAttribute

       -  isInvariant: false
       -  valueRange: no range constraint
       -  support: MANDATORY

       Obsolete
     - Specifies requirements for additional capabilities. These may be for a range of purposes.
       One example is acceleration related capabilities.

   * - computeRequirements
     - KeyValuePair
     - 0..\*
     - OpenModelAttribute

       -  isInvariant: false
       -  valueRange: no range constraint
       -  support: MANDATORY

       Preliminary
     - Specifies compute requirements.

   * - virtualMemory
     - VirtualMemoryData
     - 1
     - OpenModelAttribute

       -  isInvariant: false
       -  valueRange: no range constraint
       -  support: MANDATORY

       Preliminary
     - The virtual memory of the virtualised compute.

   * - virtualCpu
     - VirtualCpuData
     - 1
     - OpenModelAttribute

       -  isInvariant: false
       -  valueRange: no range constraint
       -  support: MANDATORY

       Preliminary
     - The virtual CPU(s) of the virtualised compute.


VirtualLinkDescFlavour
~~~~~~~~~~~~~~~~~~~~~~

The VirtualLinkDescFlavour describes additional instantiation data for a
given internal VL used in a DF.

Applied stereotypes:

-  Preliminary

-  OpenModelClass

-  support: MANDATORY

.. list-table::
   :header-rows: 1


   * - **AttributeName**
     - **Type**
     - **Mult.**
     - **Stereotypes**
     - **Description**

   * - qos
     - QoS
     - 0..1
     - OpenModelAttribute

       -  isInvariant: false
       -  valueRange: no range constraint
       -  support: MANDATORY

       Preliminary
     - QoS of the VL.

   * - flavourId
     - Identifier
     - 1
     - OpenModelAttribute

       -  isInvariant: false
       -  valueRange: no range constraint
       -  support: MANDATORY

       Preliminary
     - Identifies a flavour within a VnfVirtualLinkDesc.


VirtualLinkProfile
~~~~~~~~~~~~~~~~~~

The VirtualLinkProfile describes additional instantiation data for a
given VL used in a DF.

Applied stereotypes:

-  Preliminary

-  OpenModelClass

-  support: MANDATORY

.. list-table::
   :header-rows: 1


   * - **AttributeName**
     - **Type**
     - **Mult.**
     - **Stereotypes**
     - **Description**

   * - localAffinityOrAntiAffinityRule
     - LocalAffinityOrAntiAffinityRule
     - 0..\*
     - OpenModelAttribute

       -  isInvariant: false
       -  valueRange: no range constraint
       -  support: MANDATORY

       Preliminary
     - Specifies affinity or anti-affinity rules applicable between the VLs based on this
       VnfVirtualLinkDesc. When the cardinality is greater than 1, both affinity rule(s) and anti-affinity
       rule(s) with different scopes are applicable to the VLs based on this VnfVirtualLinkDesc.

   * - affinityOrAntiAffinityGroupId
     - Identifier
     - 0..\*
     - OpenModelAttribute

       -  isInvariant: false
       -  valueRange: no range constraint
       -  support: MANDATORY

       Preliminary
     - Identifier(s) of the affinity or anti-affinity group(s) the VnfVirtualLinkDesc belongs to.
       NOTE: Each identifier references an affinity or anti-affinity group which expresses affinity or anti-affinity
       relationship between the VL(s) using this VnfVirtualLinkDesc and the VL(s) using other VnfVirtualLinkDesc(s)
       in the same group.

   * - maxBitRateRequirements
     - LinkBitrateRequirements
     - 1
     - OpenModelAttribute

       -  isInvariant: false
       -  valueRange: no range constraint
       -  support: MANDATORY

       Preliminary
     - Specifies the minimum bitrate requirements for a VL instantiated
       according to this profile.

   * - minBitRateRequirements
     - LinkBitrateRequirements
     - 1
     - OpenModelAttribute

       -  isInvariant: false
       -  valueRange: no range constraint
       -  support: MANDATORY

       Preliminary
     - Specifies the minimum bitrate requirements for a VL instantiated according to this profile.

   * - initiationParameters
     - KeyValuePair
     - 0..\*
     - OpenModelAttribute

       -  isInvariant: false
       -  valueRange: no range constraint
       -  support: MANDATORY

       Preliminary
     - Specifies initiation parameters for the virtual link.

   * - networkType
     - NetworkType
     - 0..1
     - OpenModelAttribute

       -  isInvariant: false
       -  valueRange: no range constraint
       -  support: MANDATORY

       Preliminary
     - Type of the network

   * - dhcpEnabled
     - Boolean
     - 0..1
     - OpenModelAttribute

       -  isInvariant: false
       -  valueRange: no range constraint
       -  support: MANDATORY

       Preliminary
     - Indicating whether DHCP is enabled. Default is "FALSE" if not specified otherwise.

   * - vlanTransparent
     - Boolean
     - 0..1
     - OpenModelAttribute

       -  isInvariant: false
       -  valueRange: no range constraint
       -  support: MANDATORY

       Preliminary
     - Indicating whether "VLAN Transparent Mode" is supported.
       Default is "FALSE" if not specified otherwise.

   * - \_virtualLinkDescFlavour
     - VirtualLinkDescFlavour
     - 1
     - OpenModelAttribute

       -  isInvariant: false
       -  valueRange: no range constraint
       -  support: MANDATORY

       Preliminary
     - Identifies a flavour within the VnfVirtualLinkDesc.

   * - \_virtualLinkDesc
     - LinkDesc
     - 1
     - OpenModelAttribute

       -  isInvariant: false
       -  valueRange: no range constraint
       -  support: MANDATORY

       Preliminary
     - Uniquely identifies a Vnf VLD.


VirtualNetworkInterfaceRequirements
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

This class specifies requirements on a virtual network interface.

Applied stereotypes:

-  Preliminary

-  OpenModelClass

-  support: MANDATORY

.. list-table::
   :header-rows: 1


   * - **AttributeName**
     - **Type**
     - **Mult.**
     - **Stereotypes**
     - **Description**

   * - name
     - String
     - 0..1
     - OpenModelAttribute

       -  isInvariant: false
       -  valueRange: no range constraint
       -  support: MANDATORY

       Preliminary
     - Provides a human readable name for the requirement.

   * - description
     - String
     - 0..1
     - OpenModelAttribute

       -  isInvariant: false
       -  valueRange: no range constraint
       -  support: MANDATORY

       Preliminary
     - Provides a human readable description of the requirement.

   * - supportMandatory
     - Boolean
     - 1
     - OpenModelAttribute

       -  isInvariant: false
       -  valueRange: no range constraint
       -  support: MANDATORY

       Preliminary
     - Indicates whether fulfilling the constraint is mandatory (TRUE) for successful operation or
       desirable (FALSE).

   * - networkInterfaceRequirements
     - KeyValuePair
     - 0..\*
     - OpenModelAttribute

       -  isInvariant: false
       -  valueRange: no range constraint
       -  support: MANDATORY

       Preliminary
     - The network interface requirements. An element from an array of key-value pairs that
       articulate the network interface deployment requirements

   * - nicIoRequirements
     - LogicalNodeData
     - 0..1
     - OpenModelAttribute

       -  isInvariant: false
       -  valueRange: no range constraint
       -  support: MANDATORY

       Preliminary
     - This references (couples) the CPD with any logical node I/O requirements (for network devices) that may have been created.
       Linking these attributes is necessary so that so that I/O requirements
       that need to be articulated at the logical node level can be associated with the network interface requirements
       associated with the CPD.


VirtualStorageDesc
~~~~~~~~~~~~~~~~~~

Applied stereotypes:

-  Preliminary

-  OpenModelClass

-  support: MANDATORY

.. list-table::
   :header-rows: 1


   * - **AttributeName**
     - **Type**
     - **Mult.**
     - **Stereotypes**
     - **Description**

   * - id
     - Identifier
     - 1
     - OpenModelAttribute

       -  isInvariant: false
       -  valueRange: no range constraint
       -  support: MANDATORY

       Preliminary
     - Unique identifier of this VirtualStorageDesc in the VNFD.

   * - typeOfStorage
     - String
     - 1
     - OpenModelAttribute

       -  isInvariant: false
       -  valueRange: no range constraint
       -  support: MANDATORY

       Preliminary
     - Type of virtualised storage resource (e.g. volume, object).

   * - sizeOfStorage
     - Number
     - 1
     - OpenModelAttribute

       -  isInvariant: false
       -  valueRange: no range constraint
       -  support: MANDATORY

       Preliminary
     - Size of virtualised storage resource (e.g. size of volume, in GB).

   * - vduStorageRequirements
     - KeyValuePair
     - 0..\*
     - OpenModelAttribute

       -  isInvariant: false
       -  valueRange: no range constraint
       -  support: MANDATORY

       Preliminary
     - An array of key-value pairs that articulate the storage deployment requirements.

   * - rdmaEnabled
     - Boolean
     - 0..1
     - OpenModelAttribute

       -  isInvariant: false
       -  valueRange: no range constraint
       -  support: MANDATORY

       Obsolete
     - Indicate if the storage support RDMA.

   * - swImageDesc
     - Identifier
     - 0..1
     - OpenModelAttribute

       -  isInvariant: false
       -  valueRange: no range constraint
       -  support: MANDATORY

       Preliminary
     - Software image to be loaded on the VirtualStorage resource created
       based on this VirtualStorageDesc.

Vnf
~~~

An implementation of an NF that can be deployed on a Network Function
Virtualisation Infrastructure (NFVI).

Applied stereotypes:

-  Experimental

-  OpenModelClass

-  support: MANDATORY

.. list-table::
   :header-rows: 1


   * - **AttributeName**
     - **Type**
     - **Mult.**
     - **Stereotypes**
     - **Description**

   * - vnfInstanceId
     - Identifier
     - 1
     - OpenModelAttribute

       -  isInvariant: false
       -  valueRange: no range constraint
       -  support: MANDATORY

       Experimental
     - identifier of the VNF instance

   * - vnfInstanceName
     - String
     - 1..\*
     - OpenModelAttribute

       -  isInvariant: false
       -  valueRange: no range constraint
       -  support: MANDATORY

       Experimental
     - name of the VNF instance. Multiple names are possible.

   * - vnfProductName
     - String
     - 0..1
     - OpenModelAttribute

       -  isInvariant: false
       -  valueRange: no range constraint
       -  support: MANDATORY

       Experimental
     - name to identify the VNF Product, invariant for the VNF Product lifetime

   * - description
     - invalid
     - 0..1
     - OpenModelAttribute

       -  isInvariant: false
       -  valueRange: no range constraint
       -  support: MANDATORY

       Experimental
     - description of the VNF instance

   * - vnfProvider
     - invalid
     - 1
     - OpenModelAttribute

       -  isInvariant: false
       -  valueRange: no range constraint
       -  support: MANDATORY

       Experimental
     - provider of the VNF model

   * - vnfdId
     - Identifier
     - 1
     - OpenModelAttribute

       -  isInvariant: false
       -  valueRange: no range constraint
       -  support: MANDATORY

       Experimental
     - identifier of the VNF model

   * - vnfdVersion
     - String
     - 1
     - OpenModelAttribute

       -  isInvariant: false
       -  valueRange: no range constraint
       -  support: MANDATORY

       Experimental
     - version of the VNF model

   * - vnfSoftwareVersion
     - String
     - 1
     - OpenModelAttribute

       -  isInvariant: false
       -  valueRange: no range constraint
       -  support: MANDATORY

       Experimental
     - Software version of the VNF. This is changed when there is any change to the software that is included in the VNF package

   * - onboardedVnfPkgInfoId
     - Identifier
     - 1
     - OpenModelAttribute

       -  isInvariant: false
       -  valueRange: no range constraint
       -  support: MANDATORY

       Experimental
     - identifier of the specific VNF package on which the VNF instance is based

   * - availabilityZone
     - invalid
     - 1
     - OpenModelAttribute

       -  isInvariant: false
       -  valueRange: no range constraint
       -  support: MANDATORY

       Experimental
     - availability zone information of the VNF instance

   * - operationalStatus
     - OperationalStatus
     - 0..1
     - OpenModelAttribute

       -  isInvariant: false
       -  valueRange: no range constraint
       -  support: MANDATORY

       Experimental
     - indicator for whether the resource is considered operational.
       Valid values are in-service-path and out-of-service-path.

   * - orchestrationStatus
     - OrchestrationStatus
     - 1
     - OpenModelAttribute

       -  isInvariant: false
       -  valueRange: no range constraint
       -  support: MANDATORY

       Experimental
     - whether the VNF instance is instantiated

   * - oamlpv4Address
     - invalid
     - 0..1
     - OpenModelAttribute

       -  isInvariant: false
       -  valueRange: no range constraint
       -  support: MANDATORY

       Experimental
     - oam ip address, ipv4

   * - oamlpv6Address
     - invalid
     - 0..1
     - OpenModelAttribute

       -  isInvariant: false
       -  valueRange: no range constraint
       -  support: MANDATORY

       Experimental
     - oam ip address, ipv6

   * - instantiatedVnfInfo
     - invalid
     - 0..1
     - OpenModelAttribute

       -  isInvariant: false
       -  valueRange: no range constraint
       -  support: MANDATORY

       Experimental
     - information specific to an instantiated VNF instance, e.g., vm information

   * - inMaint
     - Boolean
     - 0..1
     - OpenModelAttribute

       -  isInvariant: false
       -  valueRange: no range constraint
       -  support: MANDATORY

       Experimental
     - whether the VNF instance is in maintenance mode, if yes, DCAE will not observe alarms/traps, etc.

   * - isClosedLoopDisabled
     - Boolean
     - 0..1
     - OpenModelAttribute

       -  isInvariant: false
       -  valueRange: no range constraint
       -  support: MANDATORY

       Experimental
     - whether closed loop function is enabled

   * - encryptedAccessFlag
     - Boolean
     - 0..1
     - OpenModelAttribute

       -  isInvariant: false
       -  valueRange: no range constraint
       -  support: MANDATORY

       Experimental
     - whether this VNF is accessed using SSH

   * - vnfConfigurableProperty
     - invalid
     - 0..1
     - OpenModelAttribute

       -  isInvariant: false
       -  valueRange: no range constraint
       -  support: MANDATORY

       Experimental
     - indicator for whether autoHeal and autoScale is enabled

   * - nfNamingCode
     - String
     - 1
     - OpenModelAttribute

       -  isInvariant: false
       -  valueRange: no range constraint
       -  support: MANDATORY

       Experimental
     - String assigned to this model used for naming purpose.

   * - vnfNamingPolicyId
     - String
     - 1
     - OpenModelAttribute

       -  isInvariant: false
       -  valueRange: no range constraint
       -  support: MANDATORY

       Experimental
     - Identifier of the policy which has the naming logic for this VNF instance

   * - vnfHomingPolicyId
     - String
     - 1
     - OpenModelAttribute

       -  isInvariant: false
       -  valueRange: no range constraint
       -  support: MANDATORY

       Experimental
     - Identifier of the policy which provides homing conditions.

   * - nfType
     - String
     - 1
     - OpenModelAttribute

       -  isInvariant: false
       -  valueRange: no range constraint
       -  support: MANDATORY

       Experimental
     - Generic description of the type of network function

   * - nfFunction
     - String
     - 1
     - OpenModelAttribute

       -  isInvariant: false
       -  valueRange: no range constraint
       -  support: MANDATORY

       Experimental
     - English description of network function that the specific VNF deployment is providing.

   * - nfRole
     - String
     - 1
     - OpenModelAttribute

       -  isInvariant: false
       -  valueRange: no range constraint
       -  support: MANDATORY

       Experimental
     - Role in the network this model will be providing

   * - closedLoopStatus
     - ClosedLoopStatus
     - 1
     - OpenModelAttribute

       -  isInvariant: false
       -  valueRange: no range constraint
       -  support: MANDATORY

       Experimental
     - Whether closed loop capabilities are enabled for this or not.

   * - \_nfc(vnfcinstance)
     - Vnfc
     - 1..\*
     - OpenModelAttribute

       -  isInvariant: false
       -  valueRange: no range constraint
       -  support: MANDATORY

       Experimental
     - Relatonship to the NF components that are part of this VNF.

   * - \_vnfd
     - Vnfd
     - 1
     - OpenModelAttribute

       -  isInvariant: false
       -  valueRange: no range constraint
       -  support: MANDATORY

       Experimental
     - Relationship to the VNF descriptor

   * - \_vnfvirtuallink
     - VnfVirtualL ink
     - 0..\*
     - OpenModelAttribute

       -  isInvariant: false
       -  valueRange: no range constraint
       -  support: MANDATORY

       Experimental
     - Relationship to VnfVirtualLink


VnfDf
~~~~~

The VnfDf describes a specific deployment version of a VNF.

Applied stereotypes:

-  Preliminary

-  OpenModelClass

-  support: MANDATORY

.. list-table::
   :header-rows: 1


   * - **AttributeName**
     - **Type**
     - **Mult.**
     - **Stereotypes**
     - **Description**

   * - flavorId
     - Identifier
     - 1
     - OpenModelAttribute

       -  isInvariant: false
       -  valueRange: no range constraint
       -  support: MANDATORY

       Preliminary
     - Identifier of this DF within the VNFD.

   * - description
     - String
     - 1
     - OpenModelAttribute

       -  isInvariant: false
       -  valueRange: no range constraint
       -  support: MANDATORY

       Preliminary
     - Human readable description of the DF.

   * - \_virtuaLlinkProfile
     - VirtualLinkProfile
     - 0..\*
     - OpenModelAttribute

       -  isInvariant: false
       -  valueRange: no range constraint
       -  support: MANDATORY

       Preliminary
     - Defines the internal VLD along with additional data which is used in this DF.
       NOTE 1: This allows for different VNF internal topologies between DFs.
	   NOTE 2: virtualLink Profile needs to be provided for all VLs that the CPs of the VDUs in the VDU profiles connect to.

   * - \_instantiationLevel
     - InstantiationLevel
     - 1..\*
     - OpenModelAttribute

       -  isInvariant: false
       -  valueRange: no range constraint
       -  support: MANDATORY

       Preliminary
     - Describes the various levels of resources that can be used to instantiate the VNF using this flavour.
       Examples: Small, Medium, Large. If there is only one "instantiationLevel" entry, it shall be treated as
       the default instantiation level for this DF.

   * - \_affinityOrAntiAffinityGroup
     - AffinityOrAntiAffinityGroup
     - 0..\*
     - OpenModelAttribute

       -  isInvariant: false
       -  valueRange: no range constraint
       -  support: MANDATORY

       Preliminary
     - Specifies affinity or anti-affinity relationship applicable between the virtualisation containers
       (e.g. virtual machines) to be created using different VDUs or internal VLs to be created using
       different VnfVirtualLinkDesc(s) in the same affinity or anti-affinity group.
       NOTE: In the present specification, including either VDU(s) or VnfVirtualLinkDesc(s) into the
       same affinity or anti-affinity group is supported. Extension to support including both VDU(s)
       and VnfVirtualLinkDesc(s) into the same affinity or anti-affinity group is left for future
       specification.

   * - \_scalingAspect
     - ScalingAspect
     - 0..\*
     - OpenModelAttribute

       -  isInvariant: false
       -  valueRange: no range constraint
       -  support: MANDATORY

       Preliminary
     - The scaling aspects supported by this DF of the VNF.
       scalingAspect shall be present if the VNF supports scaling.

   * - \_vduProfile
     - VduProfile
     - 1..\*
     - OpenModelAttribute

       -  isInvariant: false
       -  valueRange: no range constraint
       -  support: MANDATORY

       Preliminary
     - Describes additional instantiation data for the VDUs used in this flavor.

   * - \_placementGroup
     - PlacementGroup
     - 0..\*
     - OpenModelAttribute

       -  isInvariant: false
       -  valueRange: no range constraint
       -  support: MANDATORY

       Preliminary
     - Determine where VNFC's (VDU's) are placed with respect to the VNF

   * - \_baseConfigGroup
     - BaseConfigGroup
     - 1
     - OpenModelAttribute

       -  isInvariant: false
       -  valueRange: no range constraint
       -  support: MANDATORY

       Preliminary
     - BaseConfigGroup may set Access Control Lists (ACL's) and establish security
       groups and server groups.
       BaseConfigGroup creates/establishs storage for the VM's (OpenStack Cinder).
       BaseConfigGroup may establish internal networks such as OAM (VNF Mgmt) or MNS
       (Maintenance & Surveillance) established.

   * - \_deploymentGroup
     - DeploymentGroup
     - 0..\*
     - OpenModelAttribute

       -  isInvariant: false
       -  valueRange: no range constraint
       -  support: MANDATORY

       Preliminary
     - DeploymentGroup provides the minimum viable VDU and associated VNFC configuration
       for a useable VNF.

   * - \_scalinggroup
     - ScalingGroup
     - 0..\*
     - OpenModelAttribute

       -  isInvariant: false
       -  valueRange: no range constraint
       -  support: MANDATORY

       Preliminary
     - Identifies the vaious scaling groups within the VNF which identify which vnfcs that need to be scaled together.


VnfExtCp
~~~~~~~~

Describes an external CP exposed by a VNF.

**Parent class:** Cp

Applied stereotypes:

-  OpenModelClass

-  support: MANDATORY

   29. .. rubric:: VnfExtCpd
          :name: vnfextcpd

Applied stereotypes:

-  Preliminary

-  OpenModelClass

-  support: MANDATORY

.. list-table::
   :header-rows: 1


   * - **AttributeName**
     - **Type**
     - **Mult.**
     - **Stereotypes**
     - **Description**

   * - \_virtualNetworkInterfaceRequirements
     - VirtualNetworkInterfaceRequirements
     - 0..\*
     - OpenModelAttribute

       -  isInvariant: false
       -  valueRange: no range constraint
       -  support: MANDATORY

       Preliminary
     - Specifies requirements on a virtual network interface realising the CPs instantiated from this CPD.
	   NOTE: In case of referencing an intCpd via its identifier, the virtualNetworkInterfaceRequirements attribute
       of the referenced intCpd applies.

   * - \_vduCpd
     - VduCpd
     - 0..1
     - OpenModelAttribute

       -  isInvariant: false
       -  valueRange: no range constraint
       -  support: MANDATORY

       Preliminary
     - Reference to the internal VDU CPD which is used to instantiate internal CPs. These internal CPs are, in turn,
       exposed as external CPs defined by this external CPD.


VnfIndicator
~~~~~~~~~~~~

The VnfIndicator information element defines the indicator the VNF
supports.

Applied stereotypes:

-  Preliminary

-  OpenModelClass

-  support: MANDATORY

.. list-table::
   :header-rows: 1


   * - **AttributeName**
     - **Type**
     - **Mult.**
     - **Stereotypes**
     - **Description**

   * - id
     - Identifier
     - 1
     - OpenModelAttribute

       -  isInvariant: false
       -  valueRange: no range constraint
       -  support: MANDATORY

       Preliminary
     - Unique identifier.

   * - name
     - String
     - 0..1
     - OpenModelAttribute

       -  isInvariant: false
       -  valueRange: no range constraint
       -  support: MANDATORY

       Preliminary
     - The human readable name of the VnfIndicator.

   * - indicatorValue
     - String
     - 1..\*
     - OpenModelAttribute

       -  isInvariant: false
       -  valueRange: no range constraint
       -  support: MANDATORY

       Preliminary
     - Defines the allowed values or value ranges of this indicator.

   * - source
     - VnfSource
     - 1
     - OpenModelAttribute

       -  isInvariant: false
       -  valueRange: no range constraint
       -  support: MANDATORY

       Preliminary
     - Describe the source of the indicator. This tells the consumer where to send the
       subscription request.


VnfVirtualLink
~~~~~~~~~~~~~~

**Parent class:** VirtualLink

Applied stereotypes:

-  OpenModelClass

-  support: MANDATORY

   32. .. rubric:: Vnfc
          :name: vnfc

An internal component of a VNF providing a VNF Provider a defined
sub-set of that VNF's functionality, with the main characteristic that a
single instance of this component maps 1:1 against a single
Virtualisation Container.

Applied stereotypes:

-  Experimental

-  OpenModelClass

-  support: MANDATORY

.. list-table::
   :header-rows: 1


   * - **AttributeName**
     - **Type**
     - **Mult.**
     - **Stereotypes**
     - **Description**

   * - vnfcInstanceId
     - Identifier
     - 1
     - OpenModelAttribute

       -  isInvariant: false
       -  valueRange: no range constraint
       -  support: MANDATORY

       Experimental
     - identifier of the NFC instance

   * - nfcNamingCode
     - String
     - 0..1
     - OpenModelAttribute

       -  isInvariant: false
       -  valueRange: no range constraint
       -  support: MANDATORY

       Experimental
     - short code of the NFC instance

   * - description
     - invalid
     - 0..1
     - OpenModelAttribute

       -  isInvariant: false
       -  valueRange: no range constraint
       -  support: MANDATORY

       Experimental
     - description of the NFC instance

   * - vdudId
     - Identifier
     - 1
     - OpenModelAttribute

       -  isInvariant: false
       -  valueRange: no range constraint
       -  support: MANDATORY

       Experimental
     - identifier of the model of the NFC instance

   * - l3InterfaceIpv4AddressList
     - invalid
     - 0..\*
     - OpenModelAttribute

       -  isInvariant: false
       -  valueRange: no range constraint
       -  support: MANDATORY

       Experimental
     - layer-3 interface addresses, ipv4

   * - l3InterfaceIpv6AddressList
     - invalid
     - 0..\*
     - OpenModelAttribute

       -  isInvariant: false
       -  valueRange: no range constraint
       -  support: MANDATORY

       Experimental
     - layer-3 interface addresses, ipv6

   * - vnfcState
     - invalid
     - 0..1
     - OpenModelAttribute

       -  isInvariant: false
       -  valueRange: no range constraint
       -  support: MANDATORY

       Experimental
     - operating status of the VM valid value example:
       STARTED (POWER_ON),
       STOPPED (POWER_OFF)

   * - inMaint
     - Boolean
     - 0..1
     - OpenModelAttribute

       -  isInvariant: false
       -  valueRange: no range constraint
       -  support: MANDATORY

       Experimental
     - whether the NFC instance is in maintenance mode, if yes, DCAE will not observe alarms/traps, etc.

   * - isClosedLoopDisabled
     - Boolean
     - 0..1
     - OpenModelAttribute

       -  isInvariant: false
       -  valueRange: no range constraint
       -  support: MANDATORY

       Experimental
     - whether closed loop function is enabled

   * - vnfcInstanceName
     - String
     - 1..\*
     - OpenModelAttribute

       -  isInvariant: false
       -  valueRange: no range constraint
       -  support: MANDATORY

       Experimental
     - An intelligent or human readable name of the vnfc instance. Multiple names are possible.

   * - \_vnfcCp
     - VnfcCp
     - 1..\*
     - OpenModelAttribute

       -  isInvariant: false
       -  valueRange: no range constraint
       -  support: MANDATORY

       Experimental
     - Reference to the connection points of the vnfc

   * - vnfcNamingPolicyId
     - String
     - 1
     - OpenModelAttribute

       -  isInvariant: false
       -  valueRange: no range constraint
       -  support: MANDATORY

       Experimental
     - Identifier of the policy which has the naming logic for this VNFC instance

   * - nfcFunction
     - String
     - 1
     - OpenModelAttribute

       -  isInvariant: false
       -  valueRange: no range constraint
       -  support: MANDATORY

       Experimental
     - English description of network function component that the specific VNFC deployment is providing.

   * - operationalStatus
     - OperationalStatus
     - 1
     - OpenModelAttribute

       -  isInvariant: false
       -  valueRange: no range constraint
       -  support: MANDATORY

       Experimental
     - indicator for whether the resource is considered operational.
       Valid values are in-service-path and out-of-service-path.

   * - orchestrationStatus
     - OrchestrationStatus
     - 1
     - OpenModelAttribute

       -  isInvariant: false
       -  valueRange: no range constraint
       -  support: MANDATORY

       Experimental
     - whether the VNFC instance is instantiated

   * - closedLoopStatus
     - ClosedLoopStatus
     - 1
     - OpenModelAttribute

       -  isInvariant: false
       -  valueRange: no range constraint
       -  support: MANDATORY

       Experimental
     - Whether closed loop capabilities are enabled for this or not.

   * - \_vdu
     - Vdu
     - 1
     - OpenModelAttribute

       -  isInvariant: false
       -  valueRange: no range constraint
       -  support: MANDATORY

       Experimental
     - Reference to the VDU


VnfcCp
~~~~~~

**Parent class:** Cp

Applied stereotypes:

-  Experimental

-  OpenModelClass

-  support: MANDATORY

   34. .. rubric:: Vnfd
          :name: vnfd

A Vnfd, or VNF Descriptor, is template which describes a VNF in terms of
deployment and operational behaviour requirements. It also contains
connectivity, interface and virtualised resource requirements.
References: tosca-nfv-YAML-v1.0-wd05-rev02 (tosca.nodes.nfv.vnfd, but
node details are not defined) ETSI GS NFV-IFA 011 V2.1.3 (VNFD)

**Parent class:** NetworkFunctionDesc

Applied stereotypes:

-  Preliminary

-  OpenModelClass

-  support: MANDATORY

.. list-table::
   :header-rows: 1


   * - **AttributeName**
     - **Type**
     - **Mult.**
     - **Stereotypes**
     - **Description**

   * - vnfProvider
     - String
     - 1
     - OpenModelAttribute

       -  isInvariant: false
       -  valueRange: no range constraint
       -  support: MANDATORY

       Preliminary
     - Provider of the VNF and of the VNFD.

   * - vnfProductName
     - String
     - 1
     - OpenModelAttribute

       -  isInvariant: false
       -  valueRange: no range constraint
       -  support: MANDATORY

       Preliminary
     - Name to identify the VNF Product.
       Invariant for the VNF Product lifetime.

   * - vnfSoftwareVersion
     - String
     - 1
     - OpenModelAttribute

       -  isInvariant: false
       -  valueRange: no range constraint
       -  support: MANDATORY

       Preliminary
     - Software version of the VNF.
       This is changed when there is any change to the
       software that is included in the VNF Package.

   * - vnfdVersion
     - String
     - 1
     - OpenModelAttribute

       -  isInvariant: false
       -  valueRange: no range constraint
       -  support: MANDATORY

       Preliminary
     - Identifies the version of the VNFD.

   * - vnfProductInfoName
     - String
     - 0..1
     - OpenModelAttribute

       -  isInvariant: false
       -  valueRange: no range constraint
       -  support: MANDATORY

       Preliminary
     - Human readable name for the VNF Product.
       Can change during the VNF Product lifetime.

   * - vnfProductInfoDescription
     - String
     - 0..1
     - OpenModelAttribute

       -  isInvariant: false
       -  valueRange: no range constraint
       -  support: MANDATORY

       Preliminary
     - Human readable description of the VNF Product.
       Can change during the VNF Product lifetime.

   * - vnfmInfo
     - String
     - 0..\*
     - OpenModelAttribute

       -  isInvariant: false
       -  valueRange: no range constraint
       -  support: MANDATORY

       Preliminary
     - Identifies VNFM(s) compatible with the VNF described in this version of the VNFD.

   * - localizationLanguage
     - String
     - 0..\*
     - OpenModelAttribute

       -  isInvariant: false
       -  valueRange: no range constraint
       -  support: MANDATORY

       Preliminary
     - Information about localization languages of the VNF (includes e.g. strings in the VNFD).
       NOTE: This allows to provide one or more localization languages to support selecting a
       specific localization language at VNF instantiation time.

   * - modifiableAttributes
     - VnfInfoModifiableAttributes
     - 0..1
     - OpenModelAttribute

       -  isInvariant: false
       -  valueRange: no range constraint
       -  support: MANDATORY

       Preliminary
     - Defines the VNF-specific extension and metadata attributes of the VnfInfo that are writeable via the
       ModifyVnfInfo operation.

   * - vnfdId
     - Identifier
     - 1
     - OpenModelAttribute

       -  isInvariant: false
       -  valueRange: no range constraint
       -  support: MANDATORY

       Preliminary
     - Identifier of this VNFD information element. This attribute shall be globally unique.
       NOTE: The VNFD Identifier shall be used as the unique identifier of the VNF Package that
       contains this VNFD. Any modification of the content of the VNFD or the VNF Package
       shall result in a new VNFD Identifier.

   * - defaultLocalizationLanguage
     - String
     - 0..1
     - OpenModelAttribute

       -  isInvariant: false
       -  valueRange: no range constraint
       -  support: MANDATORY

       Preliminary
     - Information about localization languages of the VNF (includes e.g. strings in the VNFD).
       NOTE: This allows to provide one or more localization languages to support selecting a
       specific localization language at VNF instantiation time.

   * - configurableProperties
     - VnfConfigurableProperties
     - 0..1
     - OpenModelAttribute

       -  isInvariant: false
       -  valueRange: no range constraint
       -  support: MANDATORY

       Preliminary
     - Describes the configurable properties of the VNF (e.g. related to auto scaling and auto healing).

   * - lifecycleManagementScript
     - LifecycleManagementScript
     - 0..\*
     - OpenModelAttribute

       -  isInvariant: false
       -  valueRange: no range constraint
       -  support: MANDATORY

       Preliminary
     - Includes a list of events and corresponding management scripts performed for the VNF.

   * - logo
     - String
     - 0..1
     - OpenModelAttribute

       -  isInvariant: false
       -  valueRange: no range constraint
       -  support: MANDATORY

       Preliminary
     - File path of the vendor specified logo.

   * - guide
     - String
     - 0..1
     - OpenModelAttribute

       -  isInvariant: false
       -  valueRange: no range constraint
       -  support: MANDATORY

       Preliminary
     - UUID of the vendor guide/documentation which is attached to VNF and can be downloaded from the model.

   * - \_vdu
     - Vdu
     - 1..\*
     - OpenModelAttribute

       -  isInvariant: false
       -  valueRange: no range constraint
       -  support: MANDATORY

       Preliminary
     - Virtualisation Deployment Unit.

   * - \_vnfExtCpd
     - VnfExtCpd
     - 1..\*
     - OpenModelAttribute

       -  isInvariant: false
       -  valueRange: no range constraint
       -  support: MANDATORY

       Preliminary
     - Describes external interface(s) exposed by this VNF enabling connection with a VL.

   * - \_deploymentFlavour
     - VnfDf
     - 1..\*
     - OpenModelAttribute

       -  isInvariant: false
       -  valueRange: no range constraint
       -  support: MANDATORY

       Preliminary
     - Describes specific DF(s) of a VNF with specific requirements for capacity and performance.

   * - \_vnfIndicator
     - VnfIndicator
     - 0..\*
     - OpenModelAttribute

       -  isInvariant: false
       -  valueRange: no range constraint
       -  support: MANDATORY

       Preliminary
     - Declares the VNF indicators that are supported by this VNF.

   * - \_virtualComputeDesc
     - VirtualComputeDesc
     - 0..\*
     - OpenModelAttribute

       -  isInvariant: false
       -  valueRange: no range constraint
       -  support: MANDATORY

       Preliminary
     - Defines descriptors of virtual compute resources to be used by the VNF.

   * - \_virtualStorageDesc
     - VirtualStorageDesc
     - 0..\*
     - OpenModelAttribute

       -  isInvariant: false
       -  valueRange: no range constraint
       -  support: MANDATORY

       Preliminary
     - Defines descriptors of virtual storage resources to be used by the VNF.

   * - \_intVirtuallinkdesc
     - LinkDesc
     - 0..\*
     - OpenModelAttribute

       -  isInvariant: false
       -  valueRange: no range constraint
       -  support: MANDATORY

       Preliminary
     - Represents the type of network connectivity mandated by the VNF provider
       between two or more CPs which includes at least one internal CP.

   * - \_vnfReservedCpd
     - VduCpd
     - 0..\*
     - OpenModelAttribute

       -  isInvariant: false
       -  valueRange: no range constraint
       -  support: MANDATORY

       Preliminary
     - Reserved IP Address for VNF which is not bounded to any
       specific VNFC, but assigned manually from outside and potentially
       shared as a floating IP among VNFCs.

   * - \_elementGroup
     - VnfdElementGroup
     - 0..\*
     - OpenModelAttribute

       -  isInvariant: false
       -  valueRange: no range constraint
       -  support: MANDATORY

       Preliminary
     - Describes the associated elements of a VNFD for a certain purpose
       during VNF lifecycle management.


VnfdElementGroup
~~~~~~~~~~~~~~~~

A VNFD Element Group is a mechanism for associating elements of a VNFD
(Vdus and VnfVirtualLinkDesc(s)) for a certain purpose, for example,
scaling aspects. A given element can belong to multiple groups.

Applied stereotypes:

-  Preliminary

-  OpenModelClass

-  support: MANDATORY

.. list-table::
   :header-rows: 1


   * - **AttributeName**
     - **Type**
     - **Mult.**
     - **Stereotypes**
     - **Description**

   * - vnfdElementGroupId
     - Identifier
     - 1
     - OpenModelAttribute

       -  isInvariant: false
       -  valueRange: no range constraint
       -  support: MANDATORY

       Preliminary
     - Unique identifier of this group in the VNFD.

   * - description
     - String
     - 1
     - OpenModelAttribute

       -  isInvariant: false
       -  valueRange: no range constraint
       -  support: MANDATORY

       Preliminary
     - Human readable description of the group.

   * - \_vdu
     - Vdu
     - 0..\*
     - OpenModelAttribute

       -  isInvariant: false
       -  valueRange: no range constraint
       -  support: MANDATORY

       Preliminary
     - References to Vdus that are part of this group.

   * - \_vnfVirtualLinkdesc
     - LinkDesc
     - 0..\*
     - OpenModelAttribute

       -  isInvariant: false
       -  valueRange: no range constraint
       -  support: MANDATORY

       Preliminary
     - References to VnfVirtualLinkDesc that are part of this group.


3. .. rubric:: Data Types
      :name: data-types

   36. .. rubric:: LifecycleManagementScript
          :name: lifecyclemanagementscript

.. list-table::
   :header-rows: 1


   * - **AttributeName**
     - **Type**
     - **Mult.**
     - **Access**
     - **Stereotypes**
     - **Description**

   * - event
     - LcmEvent
     - 0..\*
     - RW
     - OpenModelAttribute

       -  isInvariant: false
       -  valueRange: no range constraint
       -  support: MANDATORY

       Preliminary
     - Describes VNF lifecycle event(s) or an external stimulus detected on a VNFM reference point.

   * - icmTransitionEvent
     - String
     - 0..\*
     - RW
     - OpenModelAttribute

       -  isInvariant: false
       -  valueRange: no range constraint
       -  support: MANDATORY

       Preliminary
     - Describes the transition VNF lifecycle event(s) that cannot be mapped to any of
       the enumerated values defined for the event attribute.
       NOTE: At least one of these two attributes shall be included.

   * - script
     - String
     - 1
     - RW
     - OpenModelAttribute

       -  isInvariant: false
       -  valueRange: no range constraint
       -  support: MANDATORY

       Preliminary
     - Information to locate a VNF LCM script (e.g. written in a DSL as specified in requirement VNF_PACK.LCM.001)
       triggered to react to one of the events listed in the event attribute.

   * - scriptDsl
     - String
     - 1
     - RW
     - OpenModelAttribute

       -  isInvariant: false
       -  valueRange: no range constraint
       -  support: MANDATORY

       Preliminary
     - Defines the domain specific language (i.e. the type) of script that is provided.
       Types of scripts could include bash, python, etc.

   * - scriptInput
     - KeyValuePair
     - 0..\*
     - RW
     - OpenModelAttribute

       -  isInvariant: false
       -  valueRange: no range constraint
       -  support: MANDATORY

       Preliminary
     - Array of KVP requirements with the key as the parameter name and the value as the parameter that need to be passed as an input to the script.
       NOTE: The scriptInput values are passed to the scripts in addition to the parameters received in the operation invocation request or
       indicator value change.


LogicalNodeData
~~~~~~~~~~~~~~~

This information element describes compute, memory and I/O requirements
that are to be associated with the logical node of infrastructure. The
logical node requirements are a sub-component of the VDU level
requirements. As an example for illustration purposes, a logical node
correlates to the concept of a NUMA cell in libvirt terminology.

.. list-table::
   :header-rows: 1


   * - **AttributeName**
     - **Type**
     - **Mult.**
     - **Access**
     - **Stereotypes**
     - **Description**

   * - logicalNodeRequirement
     - KeyValuePair
     - 0..\*
     - RW
     - OpenModelAttribute

       -  isInvariant: false
       -  valueRange: no range constraint
       -  support: MANDATORY

       Preliminary
     - The logical node-level compute, memory and I/O requirements. An array of key-value pairs
       that articulate the deployment requirements. This could include the number of CPU cores
       on this logical node, a memory configuration specific to a logical node (e.g. such as
       available in the Linux kernel via the libnuma library) or a requirement related to the
       association of an I/O device with the logical node.


MonitoringParameter
~~~~~~~~~~~~~~~~~~~

Specifies the virtualised resource related performance metric to be
tracked by the VNFM, e.g. for auto-scaling purposes. The VNFM collects
the values of performance metrics identified by this information element
from the VIM(s) using one or more locally initiated PM Jobs. These
values can be used as inputs to auto-scaling rules.

.. list-table::
   :header-rows: 1


   * - **AttributeName**
     - **Type**
     - **Mult.**
     - **Access**
     - **Stereotypes**
     - **Description**

   * - id
     - Identifier
     - 1
     - RW
     - OpenModelAttribute

       -  isInvariant: false
       -  valueRange: no range constraint
       -  support: MANDATORY

       Preliminary
     - Unique identifier of the monitoring parameter.

   * - name
     - String
     - 0..1
     - RW
     - OpenModelAttribute

       -  isInvariant: false
       -  valueRange: no range constraint
       -  support: MANDATORY

       Preliminary
     - Human readable name of the monitoring parameter.

   * - performanceMetric
     - String
     - 1
     - RW
     - OpenModelAttribute

       -  isInvariant: false
       -  valueRange: no range constraint
       -  support: MANDATORY

       Preliminary
     -

   * - collectionPeriod
     - invalid
     - 0..1
     - RW
     - OpenModelAttribute

       -  isInvariant: false
       -  valueRange: no range constraint
       -  support: MANDATORY

       Preliminary
     - An attribute that describes the recommended periodicity at which to collect the performance information.
       VNFM determines if this parameter is considered. The vendor may provide this information as a guidance for
       creating PmJobs if needed.
       NOTE: The MANO or NFVI may not support the recommended collectionPeriod based on their functionalities, and can
       reject the requests based on the recommended collectionPeriod in this case.


QoS
~~~

The QoS information element describes QoS data for a given VL used in a
DF.

.. list-table::
   :header-rows: 1


   * - **AttributeName**
     - **Type**
     - **Mult.**
     - **Access**
     - **Stereotypes**
     - **Description**

   * - latency
     - Number
     - 1
     - RW
     - OpenModelAttribute

       -  isInvariant: false
       -  valueRange: no range constraint
       -  support: MANDATORY

       Preliminary
     - Maximum latency in ms.

   * - packetDelayVariation
     - Number
     - 1
     - RW
     - OpenModelAttribute

       -  isInvariant: false
       -  valueRange: no range constraint
       -  support: MANDATORY

       Preliminary
     - Maximum jitter in ms.

   * - packetLossRatio
     - Number
     - 0..1
     - RW
     - OpenModelAttribute

       -  isInvariant: false
       -  valueRange: no range constraint
       -  support: MANDATORY

       Preliminary
     - Maximum packet loss ratio. Cardinality is 0 if no packetLossRatio requirement exists.


RequestedAdditionalCapabilityData
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

This information element describes requested additional capability for a
particular VDU. Such a capability may be for acceleration or specific
tasks.

.. list-table::
   :header-rows: 1


   * - **AttributeName**
     - **Type**
     - **Mult.**
     - **Access**
     - **Stereotypes**
     - **Description**

   * - supportMandatory
     - Boolean
     - 1
     - RW
     - OpenModelAttribute

       -  isInvariant: false
       -  valueRange: no range constraint
       -  support: MANDATORY

       Obsolete
     - Indicates whether the requested additional capability is mandatory for successful operation.

   * - requestedAdditionalCapabilityName
     - String
     - 1
     - RW
     - OpenModelAttribute

       -  isInvariant: false
       -  valueRange: no range constraint
       -  support: MANDATORY

       Obsolete
     - Identifies a requested additional capability for the VDU.

   * - minRequestedAdditionalCapabilityVersion
     - String
     - 0..1
     - RW
     - OpenModelAttribute

       -  isInvariant: false
       -  valueRange: no range constraint
       -  support: MANDATORY

       Obsolete
     - Identifies the minimum version of the requested additional capability.

   * - preferredRequestedAdditionalCapabilityVersion
     - String
     - 0..1
     - RW
     - OpenModelAttribute

       -  isInvariant: false
       -  valueRange: no range constraint
       -  support: MANDATORY

       Obsolete
     - Identifies the preferred version of the requested additional capability.

   * - targetPerformanceParameters
     - KeyValuePair
     - 1..\*
     - RW
     - OpenModelAttribute

       -  isInvariant: false
       -  valueRange: no range constraint
       -  support: MANDATORY

       Obsolete
     - Identifies specific attributes, dependent on the requested additional capability type.


ScaleInfo
~~~~~~~~~

The ScaleInfo information element represents a scale level for a
particular scaling aspect.

.. list-table::
   :header-rows: 1


   * - **AttributeName**
     - **Type**
     - **Mult.**
     - **Access**
     - **Stereotypes**
     - **Description**

   * - aspectId
     - Identifier
     - 1
     - RW
     - OpenModelAttribute

       -  isInvariant: false
       -  valueRange: no range constraint
       -  support: MANDATORY

       Preliminary
     - Reference to the scaling aspect.

   * - scaleLevel
     - Integer
     - 1
     - RW
     - OpenModelAttribute

       -  isInvariant: false
       -  valueRange: no range constraint
       -  support: MANDATORY

       Preliminary
     - The scale level, greater than or equal to 0


VirtualCpuData
~~~~~~~~~~~~~~

The VirtualCpuData information element supports the specification of
requirements related to virtual CPU(s) of a virtual compute resource.

.. list-table::
   :header-rows: 1


   * - **AttributeName**
     - **Type**
     - **Mult.**
     - **Access**
     - **Stereotypes**
     - **Description**

   * - cpuArchitecture
     - String
     - 0..1
     - RW
     - OpenModelAttribute

       -  isInvariant: false
       -  valueRange: no range constraint
       -  support: MANDATORY

       Preliminary
     - CPU architecture type. Examples are x86, ARM. The cardinality can be 0 during the allocation request, if no particular CPU architecture type is requested.

   * - numVirtualCpu
     - Integer
     - 1
     - RW
     - OpenModelAttribute

       -  isInvariant: false
       -  valueRange: no range constraint
       -  support: MANDATORY

       Preliminary
     - Number of virtual CPUs.

   * - virtualCpuClock
     - Number
     - 0..1
     - RW
     - OpenModelAttribute

       -  isInvariant: false
       -  valueRange: no range constraint
       -  support: MANDATORY

       Preliminary
     - Minimum virtual CPU clock rate (e.g. in MHz). The cardinality can be 0 during the allocation request, if no particular value is requested.

   * - virtualCpuOversubscriptionPolicy
     - String
     - 0..1
     - RW
     - OpenModelAttribute

       -  isInvariant: false
       -  valueRange: no range constraint
       -  support: MANDATORY

       Obsolete
     - The CPU core oversubscription policy e.g. the relation of virtual CPU cores to physical CPU cores/threads. The cardinality can be 0 during the allocation request, if no particular value is requested.

   * - vduCpuRequirements
     - KeyValuePair
     - 0..\*
     - RW
     - OpenModelAttribute

       -  isInvariant: false
       -  valueRange: no range constraint
       -  support: MANDATORY

       Preliminary
     - Array of key-value pair requirements on the Compute (CPU) for the VDU.

   * - virtualCpuPinning
     - VirtualCpuPinningData
     - 0..1
     - RW
     - OpenModelAttribute

       -  isInvariant: false
       -  valueRange: no range constraint
       -  support: MANDATORY

       Obsolete
     - The virtual CPU pinning configuration for the virtualised compute resource.


VirtualCpuPinningData
~~~~~~~~~~~~~~~~~~~~~

The VirtualCpuPinningData information element supports the specification
of requirements related to the virtual CPU pinning configuration of a
virtual compute resource.

.. list-table::
   :header-rows: 1


   * - **AttributeName**
     - **Type**
     - **Mult.**
     - **Access**
     - **Stereotypes**
     - **Description**

   * - virtualCpuPinningPolicy
     - PinningPolicy
     - 0..1
     - RW
     - OpenModelAttribute

       -  isInvariant: false
       -  valueRange: no range constraint
       -  support: MANDATORY

       Obsolete
     - The policy can take values of "static" or "dynamic". In case of "static" the virtual CPU cores are requested to be allocated to logical CPU cores according to the rules defined in virtualCpuPinningRules.
       In case of "dynamic" the allocation of virtual CPU cores to logical CPU cores is decided by the VIM. (e.g.: SMT (Simultaneous Multi-Threading) requirements).

   * - virtualCpuPinningRule
     - invalid
     - 0..1
     - RW
     - OpenModelAttribute

       -  isInvariant: false
       -  valueRange: no range constraint
       -  support: MANDATORY

       Obsolete
     - A list of rules that should be considered during the allocation of the virtual CPUs to logical CPUs in case of "static" virtualCpuPinningPolicy.


VirtualLinkBitRateLevel
~~~~~~~~~~~~~~~~~~~~~~~

The VirtualLinkBitRateLevel information element specifies bitrate
requirements applicable to a virtual link instantiated from a particular
VnfVirtualLinkDesc.

VirtualMemoryData
~~~~~~~~~~~~~~~~~

.. list-table::
   :header-rows: 1


   * - **AttributeName**
     - **Type**
     - **Mult.**
     - **Access**
     - **Stereotypes**
     - **Description**

   * - virtualMemSize
     - Number
     - 1
     - RW
     - OpenModelAttribute

       -  isInvariant: false
       -  valueRange: no range constraint
       -  support: MANDATORY

       Preliminary
     - Amount of virtual Memory (e.g. in MB).

   * - virtualMemOversubscriptionPolicy
     - String
     - 0..1
     - RW
     - OpenModelAttribute

       -  isInvariant: false
       -  valueRange: no range constraint
       -  support: MANDATORY

       Preliminary

       Obsolete
     - The memory core oversubscription policy in terms of virtual memory to physical memory on the platform. The cardinality can be 0 during the allocation request, if no particular value is requested.

   * - vduMemRequirements
     - KeyValuePair
     - 0..\*
     - RW
     - OpenModelAttribute

       -  isInvariant: false
       -  valueRange: no range constraint
       -  support: MANDATORY

       Preliminary
     - Array of key-value pair requirements on the memory for the VDU.

   * - numaEnabled
     - Boolean
     - 0..1
     - RW
     - OpenModelAttribute

       -  isInvariant: false
       -  valueRange: no range constraint
       -  support: MANDATORY

       Obsolete
     - It specifies the memory allocation to be cognisant of the relevant process/core allocation. The cardinality can be 0 during the allocation request, if no particular value is requested.


VnfConfigurableProperties
~~~~~~~~~~~~~~~~~~~~~~~~~

This datatype defines the configurable properties of a VNF (e.g. related
to auto scaling and auto healing). For a VNF instance, the value of
these properties can be modified by the VNFM

.. list-table::
   :header-rows: 1


   * - **AttributeName**
     - **Type**
     - **Mult.**
     - **Access**
     - **Stereotypes**
     - **Description**

   * - isAutoscaleEnabled
     - Boolean
     - 0..1
     - RW
     - OpenModelAttribute

       -  isInvariant: false
       -  valueRange: no range constraint
       -  support: MANDATORY

       Preliminary
     - It permits to enable (TRUE)/disable (FALSE) the auto-scaling functionality.
       NOTE: A cardinality of "0" indicates that configuring this present VNF property is not supported.

   * - isAutohealEnabled
     - Boolean
     - 0..1
     - RW
     - OpenModelAttribute

       -  isInvariant: false
       -  valueRange: no range constraint
       -  support: MANDATORY

       Preliminary
     - It permits to enable (TRUE)/disable (FALSE) the auto-healing functionality.
       NOTE: A cardinality of "0" indicates that configuring this present VNF property is not supported.

   * - additionalConfigurableProperty
     - String
     - 0..\*
     - RW
     - OpenModelAttribute

       -  isInvariant: false
       -  valueRange: no range constraint
       -  support: MANDATORY

       Preliminary
     -


VnfInfoModifiableAttributes
~~~~~~~~~~~~~~~~~~~~~~~~~~~

This datatype defines the VNF-specific extension and metadata attributes
of the VnfInfo that are writeable via the ModifyVnfInfo operation.

.. list-table::
   :header-rows: 1


   * - **AttributeName**
     - **Type**
     - **Mult.**
     - **Access**
     - **Stereotypes**
     - **Description**

   * - extension
     - invalid
     - 0..\*
     - RW
     - OpenModelAttribute

       -  isInvariant: false
       -  valueRange: no range constraint
       -  support: MANDATORY

       Experimental
     - "Extension" attributes of VnfInfo that are writeable.

   * - metadata
     - invalid
     - 0..\*
     - RW
     - OpenModelAttribute

       -  isInvariant: false
       -  valueRange: no range constraint
       -  support: MANDATORY

       Experimental
     - Metadata" attributes of VnfInfo that are writeable


VnfcConfigurableProperties
~~~~~~~~~~~~~~~~~~~~~~~~~~

This datatype defines the configurable properties of a VNFC. For a VNFC
instance, the value of these properties can be modified through the
VNFM.

.. list-table::
   :header-rows: 1


   * - **AttributeName**
     - **Type**
     - **Mult.**
     - **Access**
     - **Stereotypes**
     - **Description**

   * - additionalVnfcConfigurableProperty
     - String
     - 0..\*
     - RW
     - OpenModelAttribute

       -  isInvariant: false
       -  valueRange: no range constraint
       -  support: MANDATORY

       Preliminary
     - It provides VNFC configurable properties that can be modified using the ModifyVnfInfo operation.


4. .. rubric:: Enumerations
      :name: enumerations

   49. .. rubric:: AddressType
          :name: addresstype

Type of address

Contains Enumeration Literals:

-  MAC:

-  IP:

   50. .. rubric:: ClosedLoopStatus
          :name: closedloopstatus

Contains Enumeration Literals:

-  ENABLED:

-  DISABLED:

   51. .. rubric:: CollectionPeriod
          :name: collectionperiod

Specifies the periodicity at which the producer will collect performance
information.

Contains Enumeration Literals:

HomingStrategy
~~~~~~~~~~~~~~

Contains Enumeration Literals:

-  Colocation:

-  isolation:

   53. .. rubric:: LcmEvent
          :name: lcmevent

Describes VNF lifecycle event(s) or an external stimulus detected on a
VNFM reference point.

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

   54. .. rubric:: OperationalStatus
          :name: operationalstatus

Indicator for whether the resource is considered operational. Valid
values are in-service-path and out-of-service-path.

Contains Enumeration Literals:

-  IN-SERVICE-PATH:

-  OUT-OF-SERVICE-PATH:

   55. .. rubric:: OrchestrationStatus
          :name: orchestrationstatus

Contains Enumeration Literals:

-  INVENTORIED:

-  ASSIGNED:

-  CREATED:

-  ACTIVE:

   56. .. rubric:: PinningPolicy
          :name: pinningpolicy

Defines the CPU pinning policy.

Contains Enumeration Literals:

-  STATIC:

-  DYNAMIC:

   57. .. rubric:: PlacementStrategy
          :name: placementstrategy

Contains Enumeration Literals:

-  COLOCATION:

-  ISOLATION:

-  EXCLUSIVITY:

   58. .. rubric:: ProvStatus
          :name: provstatus

Provisioning status, used as a trigger for operational monitoring of
this resource by service assurance systems.

Contains Enumeration Literals:

-  PROVISIONED:

-  PREPROVISIONED:

-  CAPPED:

   59. .. rubric:: VnfSource
          :name: vnfsource

Describes the source of the indicator.

Contains Enumeration Literals:

-  VNF:

-  EM:

-  BOTH:

   60. .. rubric:: VnicType
          :name: vnictype

Describes the type of VNIC to which a CP attaches.

Contains Enumeration Literals:

-  NORMAL:

-  MACVTAP:

-  DIRECT:

-  BAREMETAL:

-  DIRECT_PHYSICAL:

-  VIRTIO_FORWARDER:

   5. .. rubric:: Primitives
         :name: primitives

   6. .. rubric:: Interfaces
         :name: interfaces

7. .. rubric:: Signals
      :name: signals

8. .. rubric:: Operations
      :name: operations


