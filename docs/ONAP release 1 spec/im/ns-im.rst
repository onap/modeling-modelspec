===========================================================================
ONAP Network Service Descriptor Information Model Specification (Amsterdam)
===========================================================================

Scope
-----

The scope of the present document is to describe the Network Service Descriptor (NSD) Information Model.


Terms, Definitions and Abbreviations
------------------------------------

For the purposes of the present document, the following abbreviations apply:

+------------+--------------------------------------------+
|Abbreviation|             Definition                     |
+------------+--------------------------------------------+
|     CM     |       Conditional Mandatory                |
+------------+--------------------------------------------+
|     CO     |       Conditional Optional                 |
+------------+--------------------------------------------+
|     CP     |       Connection Point                     |
+------------+--------------------------------------------+
|     CPD    |       Connection Point Description         |
+------------+--------------------------------------------+
|     DSL    |       Domain Specific Language             |
+------------+--------------------------------------------+
|     NCT    |       Network Connectivity Topology        |
+------------+--------------------------------------------+
|     NSD    |       Network Service Descriptor           |
+------------+--------------------------------------------+
|     UML    |       Unified Modeling Language            |
+------------+--------------------------------------------+
|     VL     |       Virtual Link                         |
+------------+--------------------------------------------+

NSD Infomration Model Overview
------------------------------

Network Service (NS) is a set of functions with unspecified connectivity between them or according to one or more forwarding graphs.

The Network Service Descriptor (NSD) is a deployment template which consists of information used by the NFV Orchestrator (NFVO) for life cycle management of an NS.

As illustrated in the following figure, the description of a NS used to deploy an NS instance includes or references the description of its constituent objects:

* Zero, one or more Virtualized Network Function Nodes Descriptors;
* Zero, one or more Physical Network connect PNFs to VLs;
* Zero, one or more nested NSD;
* Zero, one or more Virtual Link Description used by the NFVO to deploy Virtual Links (VL) ; and
* Zero, one or more VNF Forwarding Graph Descriptions.

Functional Requirements
-----------------------

The following table specifies requirements to the templates for NSD instances in R1.

+-----------------+-----------------------------------------------------------------+
|  Numbereing     |                  Requirement Description                        |
+-----------------+-----------------------------------------------------------------+
|  NST_NSD001     | The NSD shall reference the VNF Node description of constituent |
|                 | VNFs.                                                           |
+-----------------+-----------------------------------------------------------------+
|  NST_NSD002     | The NSD shall include the VLDs applicable to the VLs used by the|
|                 | NS to interconnect its constituent NFs.                         |
+-----------------+-----------------------------------------------------------------+
|  NST_NSD003     | The NSD shall include a globally unique identifier for identify-|
|                 | ing each descriptor instance.                                   |
+-----------------+-----------------------------------------------------------------+
|  NST_NSD004     | The NSD shall include an identifier to select the controller co-|
|                 | mpatible with the NSD.                                          |
+-----------------+-----------------------------------------------------------------+
|  NST_NSD005     | The NSD shall support the capability to include or reference NS |
|                 | life cycle management scripts describing how to react upon spec-|
|                 | ific life cycle events, fault detection, performance threshold  |
|                 | crossing detection and other events.                            | 
+-----------------+-----------------------------------------------------------------+
|  NST_NSD006     | The NSD shall support the capability to provide monitoring para-|
|                 | meters to be tracked during the lifetime of a NS instance.      |
+-----------------+-----------------------------------------------------------------+


The following table specifies requirements to the templates for VLD instances.

+-----------------+-----------------------------------------------------------------+
|  Numbereing     |                  Requirement Description                        |
+-----------------+-----------------------------------------------------------------+
|  NST_VLD001     | A VLD shall enable specifying the type of connectivity provided |
|                 | by the link between VNFs.                                       |
|                 | In the R1, the VL should support ELAN type at least.            |
+-----------------+-----------------------------------------------------------------+



NSD Information Model Definitions
---------------------------------

NSD
^^^

The NSD information element is a template whose instances are used by the VF-C for the lifecycle management of NSs. Note that NSD is actually defined as a special type of service descriptor, whose serviceType is set to "Network". In the same time, NSD can be included into an End-to-End service descriptor, as a resource or in other words, nested service.

+---------------+-----------+-------------+----------+--------------------------------------------+
|   Attribute   | Qualifier | Cardinality |  Content |                 Description                |
+---------------+-----------+-------------+----------+--------------------------------------------+
|    id         |     M     |      1      |Identifier| Identifier of this NSD information element.|
|               |           |             |          | It globally uniquely identifies an instance|
|               |           |             |          | of the NSD.                                |
+---------------+-----------+-------------+----------+--------------------------------------------+
|   name        |     M     |      1      | String   | The name of the NSD.                       |
+---------------+-----------+-------------+----------+--------------------------------------------+
|  serviceType  |     M     |      1      | String   | Identifies the type of the SD, which is set|
|               |           |             |          | to "Network" for NSD.                      |
+---------------+-----------+-------------+----------+--------------------------------------------+
|     vnfd      |     M     |     0..N    |  VNF id  | Consituent VNF node information of this NSD|
+---------------+-----------+-------------+----------+--------------------------------------------+
|virtualLinkDesc|     M     |     0..N    |  VLD     | Speficies the constituent VLDs.            |
+---------------+-----------+-------------+----------+--------------------------------------------+

VL Description
^^^^^^^^^^^^^^

The VL information element provides general information enabling the instantiation of virtual links.

+------------------+-----------+-------------+----------+--------------------------------------------+
|      Attribute   | Qualifier | Cardinality |  Content |                 Description                |
+------------------+-----------+-------------+----------+--------------------------------------------+
|       id         |     M     |      1      |Identifier| Identifier of this VirtualLinkDesc informa-|
|                  |           |             |          | tion element. It globally uniquely identif-|
|                  |           |             |          | ies a VL Description.                      |
+------------------+-----------+-------------+----------+--------------------------------------------+
|       name       |     M     |      1      | String   | Specifies the name of the VL Description.  |
+------------------+-----------+-------------+----------+--------------------------------------------+
|     description  |     M     |     0..1    | String   | Specifies human-readable information on the|
|                  |           |             |          | purpose of the VL (e.g. control plane traf-|
|                  |           |             |          | fic).                                      |
+------------------+-----------+-------------+----------+--------------------------------------------+
| isExternalNetwork|     M     |      1      | Boolean  | Whether the VL is external network.        |
+------------------+-----------+-------------+----------+--------------------------------------------+
|    shared        |     O     |     0..1    | Boolean  | Whether the VL is shared.                  |
+------------------+-----------+-------------+----------+--------------------------------------------+
| network_type     |     O     |     0..1    | String   | Network type of the VL.                    |
+------------------+-----------+-------------+----------+--------------------------------------------+
| segmentation_id  |     O     |     0..1    | String   | Network segmentation id of the VL.         |
+------------------+-----------+-------------+----------+--------------------------------------------+
| physical_network |     O     |     0..1    | String   | Physical network of the VL.                |
+------------------+-----------+-------------+----------+--------------------------------------------+
|      mtu         |     O     |     0..1    | Integer  | Network MTU of the VL.                     |
+------------------+-----------+-------------+----------+--------------------------------------------+
|      cidr        |     O     |     0..1    | String   | Subnetwork cidr of the VL.                 |
+------------------+-----------+-------------+----------+--------------------------------------------+
|    ip_version    |     O     |     0..1    | String   | Subnetwork IP protocol version of the VL.  |
+------------------+-----------+-------------+----------+--------------------------------------------+
| enable_dhcp      |     O     |     0..1    | Boolean  | Whether or not th subnetwork enables DHCP. |
+------------------+-----------+-------------+----------+--------------------------------------------+
|   gateway_ip     |     O     |     0..1    | String   | Subnetwork gateway IP address.             |
+------------------+-----------+-------------+----------+--------------------------------------------+

VNF Node Description Information
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

+-----------------+-----------+-------------+----------+--------------------------------------------+
|     Attribute   | Qualifier | Cardinality |  Content |                 Description                |
+-----------------+-----------+-------------+----------+--------------------------------------------+
|      id         |     M     |      1      |Identifier| Identifier of this VNF Descriptjion.       |
+-----------------+-----------+-------------+----------+--------------------------------------------+
|      name       |     M     |      1      | String   | Specifies the name of the VNF Description. |
+-----------------+-----------+-------------+----------+--------------------------------------------+
|     description |     M     |     0..1    | String   | Specifies human-readable information on the|
|                 |           |             |          | purpose of the VNF.                        |
+-----------------+-----------+-------------+----------+--------------------------------------------+
|     vnfminfo    |     M     |     0..1    | String   | Identifies VNFM(s) compatible with the VNF |
|                 |           |             |          | described in the VNF Description.          |
+-----------------+-----------+-------------+----------+--------------------------------------------+
|   vnfExtCpd     |     M     |     0..N    | vnfExtCpd| VNF External Connection Points.            |
+-----------------+-----------+-------------+----------+--------------------------------------------+


vnfExtCpd
^^^^^^^^^

+-----------------+-----------+-------------+----------+--------------------------------------------+
|     Attribute   | Qualifier | Cardinality |  Content |                 Description                |
+-----------------+-----------+-------------+----------+--------------------------------------------+
|      cpdid      |     M     |     1..N    |Identifier| Reference to the correspondent internal CPD|
+-----------------+-----------+-------------+----------+--------------------------------------------+
|      vldid      |     M     |     1..N    |Identifier| Reference to the external VLD(s).(TBD)     |
+-----------------+-----------+-------------+----------+--------------------------------------------+


