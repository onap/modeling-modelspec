===================================================================
ONAP Service Descriptor Information Model Specification (Amsterdam)
===================================================================

Scope
-----

The scope of the present document is to describe the Service Descriptor Information Model Specification.

Terms, Definitions and Abbreviations
------------------------------------

For the purposes of the present document, the following abbreviations apply:

+-----------------+---------------------------------------------------------------------+
|  Abbreviation   |                      Definition                                     |
+-----------------+---------------------------------------------------------------------+
|      RD         | Resource Descriptor                                                 |
+-----------------+---------------------------------------------------------------------+
|      SD         | Service Descriptor                                                  |
+-----------------+---------------------------------------------------------------------+
|      SO         | Service Orchestrator                                                |
+-----------------+---------------------------------------------------------------------+
|      VF         | Virtual Function                                                    |
+-----------------+---------------------------------------------------------------------+
|      VL         | Virtual Link                                                        |
+-----------------+---------------------------------------------------------------------+



SD Information Model Overview
-----------------------------

The Service Descriptor (SD) is a deployment template which consists of information used by the Service Orchestrator (SO) for life cycle management of a service.
A service is a composition of resources. The description of a service as used by the Service Orchestration (SO) to deploy a service instance includes or references the descriptors of its constituent objects: one or more resources;
A resource could be a VL, VF, WAN Descriptor etc.

Functional Requirements
-----------------------

The following table specifies requirements to the templates for SD instances.

+------------------+-------------------------------------------------------+
|   Numbering      |                Requirement Description                |
+------------------+-------------------------------------------------------+
|   NST_SD001      | The SD shall reference the resource applicable to its |
|                  | constituent services.                                 |
+------------------+-------------------------------------------------------+

SD Information Model Definitions
--------------------------------
The SD information element is a template whose instances are used by the SO for the lifecycle management of Services.

+-----------+-----------+-------------+----------+-------------------------------------------+
|Attribute  | Qualifier | Cardinality |  Content |                 Description               |
+-----------+-----------+-------------+----------+-------------------------------------------+
|    id     |     M     |      1      |Identifier| Identifier of this SD information element.|
|           |           |             |          |It globally uniquely identifies an instance|
|           |           |             |          |of the SD.                                 |
+-----------+-----------+-------------+----------+-------------------------------------------+
| designer  |     M     |      1      | String   | Designer of this SD.                      |
+-----------+-----------+-------------+----------+-------------------------------------------+
|   name    |     M     |      1      | String   | The name of the SD.                       |
+-----------+-----------+-------------+----------+-------------------------------------------+
| version   |     M     |      1      | String   | The vesion of the SD.                     |
+-----------+-----------+-------------+----------+-------------------------------------------+
|description|     M     |      1      | String   | The description of the SD.                |
+-----------+-----------+-------------+----------+-------------------------------------------+
|  vendor   |     M     |      1      | String   | The vendor of the SD. (TBD)               |
+-----------+-----------+-------------+----------+-------------------------------------------+
|    type   |     M     |      1      | String   | Value set to "Service".                   |
+-----------+-----------+-------------+----------+-------------------------------------------+
| category  |     M     |      1      | String   | Value set to either "E2E" or "NS".        |
+-----------+-----------+-------------+----------+-------------------------------------------+
|serviceType|     M     |      1      | String   | The service type of the SD.               |
+-----------+-----------+-------------+----------+-------------------------------------------+
|ServiceRole|     M     |      1      | String   | The service role of the SD.               |
+-----------+-----------+-------------+----------+-------------------------------------------+
|  resource |     M     |    1..N     | RD       | The consituent RDs of the SD.             |
|           |           |             |          | It could be VF/WAN Descriptor etc.        |
+-----------+-----------+-------------+----------+-------------------------------------------+


