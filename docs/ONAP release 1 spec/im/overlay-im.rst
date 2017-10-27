===========================================================================
ONAP VoLTE Overlay Descriptor Information Model Specification (Amsterdam)
===========================================================================

Scope
-----

The scope of the present document is to describe the Overlay VPN Descriptor Information Model for VoLTE Usecase.


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
|     NCT    |       Network Connectivity Topology        |
+------------+--------------------------------------------+
|     NSD    |       Network Service Descriptor           |
+------------+--------------------------------------------+


Overlay Descriptor Infomration Model Overview
---------------------------------------------

VoLTE use case contains a VXLAN tunnel between edge and core datacenters.

This document defines the information model for overlay descriptor that enables user to input configuration
parameters required to associate local network within dataceter to a VXLAN tunnel between data centers. Local network within data center is created dynamically while provisioning either vIMS or vEPC services. This model enables configuration of VXLAN gateways to forward local network traffic through inter-DC VXLAN tunnel.

The overlay descriptor is actually a specific type of resource, a special type of Virtual Link (VL) in precise.

Functional Requirements
-----------------------

The following table specifies requirements to the templates for Overlay descriptor in R1.

+-----------------+-----------------------------------------------------------------+
|  Numbereing     |                  Requirement Description                        |
+-----------------+-----------------------------------------------------------------+
|  NST_OVED001    | The Overlay VPN Descriptor shall reference to its constituent 2 |
|                 | sites.                                                          |
+-----------------+-----------------------------------------------------------------+
|  NST_OVED002    | The Overlay VPN Descriptor shall enable L2/L3 VxLAN VPN options.|
+-----------------+-----------------------------------------------------------------+


Overlay VPN Descriptor Information Model Definitions
----------------------------------------------------

The Overlay VPN Descriptor information element is a template whose instances are used by the Service Orchestrator (SO) and SDN-C (Network Controller) for the deployment and configuration of L2/L3 VxLAN 
VPN for DCI connections.

+---------------+-----------+-------------+----------+--------------------------------------------+
|   Attribute   | Qualifier | Cardinality |  Content |                 Description                |
+---------------+-----------+-------------+----------+--------------------------------------------+
|    id         |     O     |      1      |Identifier| Identifier of the Tunnel Endpoint node.    |
+---------------+-----------+-------------+----------+--------------------------------------------+
|     name      |     O     |      1      | String   | Overlay tunnel name.                       |
+---------------+-----------+-------------+----------+--------------------------------------------+
|   version     |     O     |      1      | String   | Overlay tunnel template version.           |
+---------------+-----------+-------------+----------+--------------------------------------------+
|  description  |     O     |      1      | String   | Addtional comments/information about the   |
|               |           |             |          | the overlay tunnel.                        |
+---------------+-----------+-------------+----------+--------------------------------------------+
|  tunneltype   |     M     |      1      |  Enum    | The type of overlay tunnel.                |
|               |           |             |          | Valid values include 'L3-DCI' and 'L2-DCI'.|
+---------------+-----------+-------------+----------+--------------------------------------------+
|    sites      |     M     |      2      |  Site    | Speficies the constituent two Sites.       |
+---------------+-----------+-------------+----------+--------------------------------------------+

Site Description
^^^^^^^^^^^^^^^^

The Site information element provides general information enabling the instantiation of sites.

+------------------+-----------+-------------+----------+--------------------------------------------+
|      Attribute   | Qualifier | Cardinality |  Content |                 Description                |
+------------------+-----------+-------------+----------+--------------------------------------------+
|       id         |     M     |      1      |Identifier| Identifier of DCI overlay tunnel endpoint. |
|                  |           |             |          | Could be IP address of domain controller.  |
+------------------+-----------+-------------+----------+--------------------------------------------+
|    networkname   |     M     |      1      | String   | Name of network associated with the tunnel.|
+------------------+-----------+-------------+----------+--------------------------------------------+
|     rounterId    |     O     |      1      | String   | Identifier of router connected to L3 tunnel|
|                  |           |             |          | end point, while configuring L3-DCI tunnel.|
+------------------+-----------+-------------+----------+--------------------------------------------+
|     description  |     M     |     0..1    | String   | Additional comment/informaiton about the   |
|                  |           |             |          | tunnel or domain controller.               |
+------------------+-----------+-------------+----------+--------------------------------------------+
|     ImportRT     |     O     |      1      |   List   | List of Route targets imported by the local|
|                  |           |             |          | router.                                    |
+------------------+-----------+-------------+----------+--------------------------------------------+
|     exportRT     |     O     |      1      |   List   | List of Route targets exported by the local|
|                  |           |             |          | router.                                    |
+------------------+-----------+-------------+----------+--------------------------------------------+
|        vni       |     O     |      1      |  Integer | VXLAN ID.                                  |
+------------------+-----------+-------------+----------+--------------------------------------------+
|  firewalEnable   |     O     |      1      |  Boolean | Identifies if a firewall exists in the path|
|                  |           |             |          | of overlay tunnel.                         |
+------------------+-----------+-------------+----------+--------------------------------------------+
|    firewallId    |     O     |      1      |  String  | Identifier of Firewall that is in overlay  |
|                  |           |             |          | tunnel path.                               |
+------------------+-----------+-------------+----------+--------------------------------------------+
| localNetworkAll  |     O     |      1      |  Boolean | Identifies whether all the local networks  |
|                  |           |             |          | associate with the tunnel or not.          |
+------------------+-----------+-------------+----------+--------------------------------------------+