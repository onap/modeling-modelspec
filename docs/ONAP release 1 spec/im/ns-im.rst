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
|     DF     |       Depoyment Flavour                    |
+------------+--------------------------------------------+
|     DSL    |       Domain Specific Language             |
+------------+--------------------------------------------+
|     GS     |       Group Specification                  |
+------------+--------------------------------------------+
|    MANO    |       Management and Orchestration         |
+------------+--------------------------------------------+
|    MPLS    |       Multi-Protocol Label Switching       |
+------------+--------------------------------------------+
|     NCT    |       Network Connectivity Topology        |
+------------+--------------------------------------------+
|     NFP    |       Network Forwarding Path              |
+------------+--------------------------------------------+
|    NFPD    |       Network Forwarding Path Descriptor   |
+------------+--------------------------------------------+
|     NSD    |       Network Service Descriptor           |
+------------+--------------------------------------------+
|     UML    |       Unified Modeling Language            |
+------------+--------------------------------------------+
|     VL     |       Virtual Link                         |
+------------+--------------------------------------------+
|     VLD    |       Virtual Link Descriptor              |
+------------+--------------------------------------------+

NSD Infomration Model Overview
------------------------------

An Network Service (NS), as defined by ETSI NFV ISG is a composition of Network Functions (NF) arranged as a set of functions with unspecified connectivity between them or according to one or more forwarding graphs.

The Network Service Descriptor (NSD) is a deployment template which consists of information used by the NFV Orchestrator (NFVO) for life cycle management of an NS.

As illustrated in the following figure, the description of a NS as used by the NFV Management and Orchestration (MANO) functions to deploy an NS instance includes or references the descriptors of its constituent objects:

* Zero, one or more Virtualized Network Function Descriptors (VNFD);
* Zero, one or more Virtual Link Descriptor (VLD) used by the NFVO to deploy Virtual Links (VL);
* Zero, one or more Physical Network connect PNFs to VLs;
* Zero, one or more nested NSD; and
* Zero, one or more VNF Forwarding Graph Descriptors (VNFFGD).

For the ONAP R1, according to the cases that VFC supports, the simplified NS model it supports,contains the following constituent objects:

* Zero, one or more Virtualized Network Function Descriptors (VNFD); and
* Zero, one or more Virtual Link Descriptor (VLD) used by the NFVO to deploy Virtual Links (VL).


Functional Requirements
-----------------------

The following table specifies requirements to the templates for NSD instances in R1.

+-----------------+-----------------------------------------------------------------+
|  Numbereing     |                  Requirement Description                        |
+-----------------+-----------------------------------------------------------------+
|  NST_NSD001     | The NSD shall reference the VNFDs applicable to its constituent |
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
|                 | crossing detection and other events that can occur at the NFVO  |
|                 | reference points.                                               |
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


The following table specifies requirements to the templates for VNF Node instances.

+-----------------+-----------------------------------------------------------------+
|  Numbereing     |                  Requirement Description                        |
+-----------------+-----------------------------------------------------------------+
|  NST_VNFD001    | A VNF Node information in the NSD shall enable specifying VNFD  |
|                 | in the VNF package. (TBD)                                       |
+-----------------+-----------------------------------------------------------------+


NSD Information Model Definitions
---------------------------------

NSD
^^^

The NSD information element is a template whose instances are used by the NFVO for the lifecycle management of NSs.

+---------------+-----------+-------------+----------+--------------------------------------------+
|   Attribute   | Qualifier | Cardinality |  Content |                 Description                |
+---------------+-----------+-------------+----------+--------------------------------------------+
|    id         |     M     |      1      |Identifier| Identifier of this NSD information element.|
|               |           |             |          | It globally uniquely identifies an instance|
|               |           |             |          | of the NSD.                                |
+---------------+-----------+-------------+----------+--------------------------------------------+
|   name        |     M     |      1      | String   | The name of the NSD.                       |
+---------------+-----------+-------------+----------+--------------------------------------------+
|  serviceType  |     M     |      1      | String   | Identifies the type of the SD.             |
|               |           |             |          | enum:E2E Service, Network                  |
+---------------+-----------+-------------+----------+--------------------------------------------+
|controllerinfo |     M     |      1      | String   | Identifies controller(s) conmpatible with  |
|               |           |             |          | the NS described in this version of the NSD|
|               |     M     |             |          | default: VF-C.                             |
+---------------+-----------+-------------+----------+--------------------------------------------+
|      vnfd     |     M     |     0..N    |  VNFD    | VNFD information element(s) of this NSD. It|
|               |           |             |          | It globally uniquely identifies an instance|
|               |           |             |          | of the NSD.                                |
+---------------+-----------+-------------+----------+--------------------------------------------+
|virtualLinkDesc|     M     |     0..N    |  VLD     | Speficies the constituent VLDs.            |
+---------------+-----------+-------------+----------+--------------------------------------------+

VLD
^^^

The VL information element provides general information enabling the instantiation of virtual links.

+------------------+-----------+-------------+----------+--------------------------------------------+
|      Attribute   | Qualifier | Cardinality |  Content |                 Description                |
+------------------+-----------+-------------+----------+--------------------------------------------+
|       id         |     M     |      1      |Identifier| Identifier of this VirtualLinkDesc informa-|
|                  |           |             |          | tion element. It globally uniquely identif-|
|                  |           |             |          | ies a VLD.                                 |
+------------------+-----------+-------------+----------+--------------------------------------------+
|       name       |     M     |      1      | String   | Specifies the name of the VLD.             |
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

VNFD
^^^^
+-----------------+-----------+-------------+----------+--------------------------------------------+
|     Attribute   | Qualifier | Cardinality |  Content |                 Description                |
+-----------------+-----------+-------------+----------+--------------------------------------------+
|      id         |     M     |      1      |Identifier|  Identifier of this VNF Descriptor.        |
+-----------------+-----------+-------------+----------+--------------------------------------------+
|      name       |     M     |      1      | String   | Specifies the name of the VNFD.            |
+-----------------+-----------+-------------+----------+--------------------------------------------+
|     description |     M     |     0..1    | String   | Specifies human-readable information on the|
|                 |           |             |          | purpose of the VNF.                        |
+-----------------+-----------+-------------+----------+--------------------------------------------+
|     vnfminfo    |     M     |     0..1    | String   | Identifies VNFM(s) compatible with the VNF |
|                 |           |             |          | described in this version of the VNFD.     |
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

