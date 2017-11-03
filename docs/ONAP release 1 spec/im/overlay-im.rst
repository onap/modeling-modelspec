===========================================================================
ONAP VoLTE Overlay Descriptor Information Model Specification (Amsterdam)
===========================================================================

Scope
-----

The scope of the present document is to describe the Overlay VPN Descriptor Information Model.
For Amsterdam release, this descriptor is currently leveraged by VoLTE usecase to provision the L2/L2 VPN tunnel between the core DC and edage DC, but it is in nature a generic descriptor which could be used by other usecase for L2/L3 VPN tunnel provision as well.


Terms, Definitions and Abbreviations
------------------------------------

For the purposes of the present document, the following abbreviations apply:

+------------+--------------------------------------------+
|Abbreviation|             Definition                     |
+------------+--------------------------------------------+
|   L3-DCI   |     Layer-3 Data Center Interconnection    |
+------------+--------------------------------------------+
|   L2-DCI   |     Layer-2 Data Center Interconnectio     |
+------------+--------------------------------------------+


Overlay Descriptor Infomration Model Overview
---------------------------------------------

This document defines the configuration information model for overlay descriptor that enables user to input configuration
parameters required to associate local network within dataceter to a VXLAN tunnel between data centers. 

For example, VoLTE use case contains a VXLAN tunnel between edge and core datacenters.
Local network within data center is created dynamically while provisioning either vIMS or vEPC services. This model enables configuration of VXLAN gateways to forward local network traffic through inter-DC VXLAN tunnel.

From the perspective of deployment, the overlay descriptor is actually a specific type of resource, a special type of Virtual Link (VL) in precise, as defined by Service Descriptor.

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

+----------------------+-----------+-------------+----------+--------------------------------------------+
|   Attribute          | Qualifier | Cardinality |  Content |                 Description                |
+----------------------+-----------+-------------+----------+--------------------------------------------+
|    id                |     M     |      1      |Identifier| Identifier of the Tunnel Endpoint node.    |
+----------------------+-----------+-------------+----------+--------------------------------------------+
|     name             |     O     |      1      | String   | Overlay tunnel name.                       |
+----------------------+-----------+-------------+----------+--------------------------------------------+
|   version            |     O     |      1      | String   | Overlay tunnel template version.           |
+----------------------+-----------+-------------+----------+--------------------------------------------+
|  description         |     O     |      1      | String   | Addtional comments/information about the   |
|                      |           |             |          | the overlay tunnel.                        |
+----------------------+-----------+-------------+----------+--------------------------------------------+
|  tunneltype          |     M     |      1      |  Enum    | The type of overlay tunnel.                |
|                      |           |             |          | Valid values include 'L3-DCI' and 'L2-DCI'.|
+----------------------+-----------+-------------+----------+--------------------------------------------+
|    site1_id          |     M     |      1      |  String  | Identifies site1.                          |
+----------------------+-----------+-------------+----------+--------------------------------------------+
|  site1_description   |      O    |      1      |  String  | Information about overlay tunnel endpoint. |
|                      |           |             |          | Identifies local domain controller.        |
+----------------------+-----------+-------------+----------+--------------------------------------------+
|  site1_networkName   |     M     |      1      |  String  | A comma seperated list of network names    |
|                      |           |             |          | associated with tunnel in site1.           |
+----------------------+-----------+-------------+----------+--------------------------------------------+
|  site1_routerId      |     O     |      1      |  String  | Router ID connected to L3 end point.       |
+----------------------+-----------+-------------+----------+--------------------------------------------+
|  site1_importRT1     |     M     |      1      |  String  | Imported Route Target                      |
+----------------------+-----------+-------------+----------+--------------------------------------------+
|  site1_exportRT1     |     M     |      1      |  String  | Exported Route Target                      |
+----------------------+-----------+-------------+----------+--------------------------------------------+
|    site1_vni         |     M     |      1      |  Integer | Tunnel local VXLAN Identfier in site1      |
+----------------------+-----------+-------------+----------+--------------------------------------------+
| site1_fireWallEnable |     O     |      1      |  Boolean | Identifies if firewall is in tunnel path   |
+----------------------+-----------+-------------+----------+--------------------------------------------+
|   site1_fireWallId   |     O     |      1      |  String  | Firewall Id, if exists in tunnel path      |
+----------------------+-----------+-------------+----------+--------------------------------------------+
| site1_localNetworkAll|     O     |      1      |  Boolean | Identifies if all local networks associate |
|                      |           |             |          | with the VXLAN tunnel.                     |
+----------------------+-----------+-------------+----------+--------------------------------------------+
|     site2_id         |     M     |      1      |  String  | Identifies site2.                          |
+----------------------+-----------+-------------+----------+--------------------------------------------+
|  site2_description   |     O     |      1      |  String  | Information about tunnel site2   endpoint. |
|                      |           |             |          | Identifies local domain controller.        |
+----------------------+-----------+-------------+----------+--------------------------------------------+
|  site2_networkName   |     M     |      1      |  String  | A comma seperated list of network names    |
|                      |           |             |          | associated with tunnel in site2.           |
+----------------------+-----------+-------------+----------+--------------------------------------------+
|   site2_routerId     |     O     |      1      |  String  | Router ID connected to L3 end point.       |    
+----------------------+-----------+-------------+----------+--------------------------------------------+
|   site2_importRT1    |     M     |      1      |  String  | Imported Route Target                      |
+----------------------+-----------+-------------+----------+--------------------------------------------+
|   site2_exportRT1    |     M     |      1      |  String  | Exported Route Target                      |
+----------------------+-----------+-------------+----------+--------------------------------------------+
|    site2_vni         |     M     |      1      |  Integer | Tunnel local VXLAN Identfier in site2      |
+----------------------+-----------+-------------+----------+--------------------------------------------+
| site2_fireWallEnable |     O     |      1      |  Boolean | Identifies if firewall is in tunnel path   |
+----------------------+-----------+-------------+----------+--------------------------------------------+
|  site2_fireWallId    |     O     |      1      |  String  | Firewall Id, if exists in tunnel path      |
+----------------------+-----------+-------------+----------+--------------------------------------------+
| site2_localNetworkAll|     O     |      1      |  Boolean | Identifies if all local networks associate |
|                      |           |             |          | with the VXLAN tunnel.                     |
+----------------------+-----------+-------------+----------+--------------------------------------------+
