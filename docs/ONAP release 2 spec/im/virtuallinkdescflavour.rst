.. Copyright 2018 (China Mobile)
.. This file is licensed under the CREATIVE COMMONS ATTRIBUTION 4.0 INTERNATIONAL LICENSE
.. Full license text at https://creativecommons.org/licenses/by/4.0/legalcode

.. contents::
   :depth: 3
..

Class: VirtualLinkDescFlavour
=============================

+-------------------+-------------+------------------+-----------------+--------------------------+
| **Attribute Name**| **Type**    | **Multiplicity** | **Description** | **Applied Stereotypes**  |
+===================+=============+==================+=================+==========================+
| flavourId         | Identifier  | 1                | Identifies      | support:                 |
|                   |             |                  | a flavour       | MANDATORY                |
|                   |             |                  | within a        |                          |
|                   |             |                  | VnfVirtualL     |                          |
|                   |             |                  | inkDesc.        |                          |
+-------------------+-------------+------------------+-----------------+--------------------------+
| qos               | QoS         | 0..1             | QoS of the      | support:                 |
|                   |             |                  | VL.             | MANDATORY                |
+-------------------+-------------+------------------+-----------------+--------------------------+
