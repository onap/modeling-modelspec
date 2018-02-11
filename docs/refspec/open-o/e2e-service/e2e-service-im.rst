.. Copyright 2017 (HUAWEI)
.. This file is licensed under the CREATIVE COMMONS ATTRIBUTION 4.0 INTERNATIONAL LICENSE
.. Full license text at https://creativecommons.org/licenses/by/4.0/legalcode

.. contents::
   :depth: 3
..

TOSCA template for e2e-service
===================================

Data Types
------------------

gso.datatypes.service.basicInfo
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

Describe the basic information for the service

Properties
^^^^^^^^^^

+------------+----------+--------+-------------+-----------------------------------+
| Name       | Required | Type   | Constraints | Description                       |
+============+==========+========+=============+===================================+
| createTime | No       | string |             | The creation time of the service  |
+------------+----------+--------+-------------+-----------------------------------+
| updateTime | No       | string |             | The update time of the service    |
+------------+----------+--------+-------------+-----------------------------------+
| creatorId  | No       | string |             | The identification of the creator |
+------------+----------+--------+-------------+-----------------------------------+
| location   | No       | string |             | Location of the single domain     |
+------------+----------+--------+-------------+-----------------------------------+

Definition
^^^^^^^^^^

+-----------------------------------------------------------------------+
| #                                                                     |
| \******************************************************************** |
| ********\*                                                            |
|                                                                       |
| # data types                                                          |
|                                                                       |
| #                                                                     |
| \******************************************************************** |
| ********\*                                                            |
|                                                                       |
| data_types:                                                           |
|                                                                       |
|   gso.datatypes.service.basicInfo:                                    |
|                                                                       |
|     derived_from: tosca.datatypes.Root                                |
|                                                                       |
|     properties:                                                       |
|                                                                       |
|       createTime:                                                     |
|                                                                       |
|         type: string                                                  |
|                                                                       |
|         description: create time                                      |
|                                                                       |
|       updateTime:                                                     |
|                                                                       |
|         type: string                                                  |
|                                                                       |
|         description: update time                                      |
|                                                                       |
|       creatorId:                                                      |
|                                                                       |
|         type: string                                                  |
|                                                                       |
|         description: ID of the creator                                |
|                                                                       |
|       location:                                                       |
|                                                                       |
|         type: string                                                  |
|                                                                       |
|         description: Location of the single domain                    |
+-----------------------------------------------------------------------+

Interface Types
--------------------

gso.interfaces.lifecycle.Standard
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

There is the lifecycle standard interface of the service.

.. properties-1:

Properties
^^^^^^^^^^

.. definition-1:

Definition
^^^^^^^^^^

+-----------------------------------------------------------------------------+
| #                                                                           |
| \********************************************************************       |
| ********\*                                                                  |
|                                                                             |
| # interface_types                                                           |
|                                                                             |
| #                                                                           |
| \********************************************************************       |
| ********\*                                                                  |
|                                                                             |
| interface_types:                                                            |
|                                                                             |
|   gso.interfaces.lifecycle.Standard:                                        |
|                                                                             |
|     derived_from: tosca.interfaces.Root                                     |
|                                                                             |
|     create:                                                                 |
|                                                                             |
|       description: Standard lifecycle create operation.                     |
|                                                                             |
|     update:                                                                 |
|                                                                             |
|       description: Standard lifecycle configure and update operation.       |
|                                                                             |
|     instantiate:                                                            |
|                                                                             |
|       description: Standard lifecycle instantiate operation.                |
|                                                                             |
|     terminate:                                                              |
|                                                                             |
|       description: Standard lifecycle terminate operation.                  |
|                                                                             |
|     delete:                                                                 |
|                                                                             |
|       description: Standard lifecycle delete operation.                     |
|                                                                             |
|     query:                                                                  |
|                                                                             |
|       description: Standard lifecycle query operation.                      |
|                                                                             |
|     scalingIn:                                                              |
|                                                                             |
|       description: Standard lifecycle scalingIn operation.                  |
|                                                                             |
|     scalingOut:                                                             |
|                                                                             |
|       description: Standard lifecycle query operation.                      |
+-----------------------------------------------------------------------------+

Capability Types
---------------------

gso.capability.SingleDomainNs
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

There is the depended capability of single domain network service.

.. properties-2:

Properties
^^^^^^^^^^

.. definition-2:

Definition
^^^^^^^^^^

+-------------------------------------------+
| capability_types:                         |
|                                           |
|   gso.capability.SingleDomainNs:          |
|                                           |
|     derived_from: tosca.capabilities.Root |
+-------------------------------------------+

Relationship Types
--------------------------

gso.relationship.DependOn
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

There is the relationship of single domain network service and global
network service.

.. properties-3:

Properties
^^^^^^^^^^

.. definition-3:

Definition
^^^^^^^^^^

+-----------------------------------------------------------------------+
| #                                                                     |
| \******************************************************************** |
| ********\*                                                            |
|                                                                       |
| # relationship types                                                  |
|                                                                       |
| #                                                                     |
| \******************************************************************** |
| ********\*                                                            |
|                                                                       |
| relationship_types:                                                   |
|                                                                       |
|   gso.relationship.DependOn:                                          |
|                                                                       |
|     derived_from: tosca.relationships.Root                            |
|                                                                       |
|     description:                                                      |
|                                                                       |
|     valid_target_types: [gso.capability.SingleDomainNs]               |
+-----------------------------------------------------------------------+

Node Types
----------------

gso.node.Root
~~~~~~~~~~~~~~~~~~~

Root is the super class of all the gs-o network service.

.. properties-4:

Properties
^^^^^^^^^^

+-------------+----------+--------+-------------+-----------------------------------+
| Name        | Required | Type   | Constraints | Description                       |
+=============+==========+========+=============+===================================+
| Id          | Yes      | string |             | The identification of the service |
+-------------+----------+--------+-------------+-----------------------------------+
| name        | Yes      | string |             | The name of the service           |
+-------------+----------+--------+-------------+-----------------------------------+
| description | No       | string |             | The description of the service    |
+-------------+----------+--------+-------------+-----------------------------------+

.. definition-4:

Definition
^^^^^^^^^^

+-----------------------------------------------------------------------+
| #                                                                     |
| \******************************************************************** |
| ********\*                                                            |
|                                                                       |
| # node types                                                          |
|                                                                       |
| #                                                                     |
| \******************************************************************** |
| ********\*                                                            |
|                                                                       |
| node_types:                                                           |
|                                                                       |
|   gso.node.Root:                                                      |
|                                                                       |
|     derived_from: tosca.nodes.Root                                    |
|                                                                       |
|     description: gso root type                                        |
|                                                                       |
|     properties:                                                       |
|                                                                       |
|       id:                                                             |
|                                                                       |
|         type: string                                                  |
|                                                                       |
|       name:                                                           |
|                                                                       |
|         type: string                                                  |
|                                                                       |
|       description:                                                    |
|                                                                       |
|         type: string                                                  |
|                                                                       |
|         required: false                                               |
+-----------------------------------------------------------------------+

gso.node.NetworkService
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

Describe the information for the network service

.. properties-5:

Properties
^^^^^^^^^^

+-------------+-------------+-------------+-------------+-------------+
| Name        | Required    | Type        | Constraints | Description |
+=============+=============+=============+=============+=============+
| baseService | Yes         | gso.datatyp |             | The basic   |
| Info        |             | es.service. |             | information |
|             |             | basicInfo   |             | of the      |
|             |             |             |             | service     |
+-------------+-------------+-------------+-------------+-------------+
| templateId  | Yes         | string      |             | The         |
|             |             |             |             | template id |
|             |             |             |             | of the      |
|             |             |             |             | service     |
+-------------+-------------+-------------+-------------+-------------+
| serviceDefI | Yes         | string      |             | The csar    |
| d           |             |             |             | package id  |
|             |             |             |             | of the      |
|             |             |             |             | service     |
+-------------+-------------+-------------+-------------+-------------+

.. definition-5:

Definition
^^^^^^^^^^

+-----------------------------------------------+
| gso.node.NetworkService:                      |
|                                               |
|   derived_from: gso.node.Root                 |
|                                               |
|   description: basic network service          |
|                                               |
|   properties:                                 |
|                                               |
|     baseServiceInfo:                          |
|                                               |
|       type: gso.datatypes.service.basicInfo   |
|                                               |
|     templateId:                               |
|                                               |
|       type: string                            |
|                                               |
|     serviceDefId:                             |
|                                               |
|       type: string                            |
|                                               |
|   interfaces:                                 |
|                                               |
|     standard:                                 |
|                                               |
|       type: gso.interfaces.lifecycle.Standard |
+-----------------------------------------------+

gso.node.SingleDomainNetworkService
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

Describe the information for the single domain network service

.. properties-6:

Properties
^^^^^^^^^^

.. definition-6:

Definition
^^^^^^^^^^

+----------------------------------------------+
| gso.node.SingleDomainNetworkService:         |
|                                              |
|   derived_from: gso.node.NetworkService      |
|                                              |
|   description: single domain network service |
+----------------------------------------------+

gso.node.CrossDomainNetworkService
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

Describe the basic information for cross domain network service

.. properties-7:

Properties 
^^^^^^^^^^^

.. definition-7:

Definition
^^^^^^^^^^

+-------------------------------------------------+
| gso.node.CrossDomainNetworkService:             |
|                                                 |
|   derived_from: gso.node.NetworkService         |
|                                                 |
|   description: cross domain network service     |
|                                                 |
|   requirements:                                 |
|                                                 |
|     -realizes:                                  |
|                                                 |
|       node: gso.node.SingleDomainNetworkService |
|                                                 |
|       capability: gso.capability.SingleDomainNs |
|                                                 |
|       relationship: gso.relationship.DependOn   |
|                                                 |
|       occurrences: [2, UNBOUNDED]               |
+-------------------------------------------------+
                                