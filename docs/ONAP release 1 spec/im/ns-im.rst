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
|     DF     |       Deployment Flavour                   |
+------------+--------------------------------------------+
|     DSL    |       Domain Specific Language             |
+------------+--------------------------------------------+
|     GS     |       Group Specification                  |
+------------+--------------------------------------------+
|    MANO    |       MANagement and Orchestration         |
+------------+--------------------------------------------+
|    MPLS    |       Multi-Protocol Label Switching       |
+------------+--------------------------------------------+
|     NCT    |       Network Connectivity Topology        |
+------------+--------------------------------------------+
|     NF     |       Network Function                     |
+------------+--------------------------------------------+
|     NFP    |       Network Forwarding Path              |
+------------+--------------------------------------------+
|    NFPD    |       Network Forwarding Path Descriptor   |
+------------+--------------------------------------------+
|    NFVO    |       NFV Orchestrator                     |
+------------+--------------------------------------------+
|     NSD    |       Network Service Descriptor           |
+------------+--------------------------------------------+
|     UML    |       Unified Modeling Language            |
+------------+--------------------------------------------+
|     VL     |       Virtual Link                         |
+------------+--------------------------------------------+
|     VLD    |       Virtual Link Descriptor              |
+------------+--------------------------------------------+
|     VNF    |       Virtual Network Function             |
+------------+--------------------------------------------+
|    VNFD    |       VNF Descriptor                       |
+------------+--------------------------------------------+
|   VNFFGD   |       VNF Forwarding Graph Descriptors     |
+------------+--------------------------------------------+

NSD Information Model Overview
------------------------------

A Network Service (NS), as defined by ETSI NFV ISG is a composition of Network Functions (NF) arranged as a set of functions with unspecified connectivity between them or according to one or more forwarding graphs.

The Network Service Descriptor (NSD) is a deployment template which consists of information used by the NFV Orchestrator (NFVO) for life cycle management of an NS.

As illustrated in the following figure, the description of a NS as used by the NFV Management and Orchestration (MANO) functions to deploy an NS instance includes or references the descriptors of its constituent objects:

* Zero, one or more Virtualized Network Function Descriptors (VNFD);
* Zero, one or more Physical Network connect PNFs to VLs;
* Zero, one or more nested NSD;
* Zero, one or more Virtual Link Descriptor (VLD) used by the NFVO to deploy Virtual Links (VL) ; and
* Zero, one or more VNF Forwarding Graph Descriptors (VNFFGD).

Functional Requirements
-----------------------

NSD Information Model Definitions
---------------------------------


