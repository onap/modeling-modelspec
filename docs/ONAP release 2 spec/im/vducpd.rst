.. Copyright 2018 (China Mobile)
.. This file is licensed under the CREATIVE COMMONS ATTRIBUTION 4.0 INTERNATIONAL LICENSE
.. Full license text at https://creativecommons.org/licenses/by/4.0/legalcode

.. contents::
   :depth: 3
..

Class: VduCpd/VDUCPDesc
=======================

+--------------------+-------------+------------------+------------------+--------------------------+
| **Attribute Name** | **Type**    | **Multiplicity** | **Description**  | **Applied Stereotypes**  |
+====================+=============+==================+==================+==========================+
| bitrateRequ        | Number      | 0..1             | Bitrate          | support:                 |
| irement            | (recommende |                  | requirement      | MANDATORY                |
|                    | d           |                  | on this CP.      |                          |
|                    | DM type:    |                  |                  |                          |
|                    | Scalar-Unit |                  |                  |                          |
|                    | -Rate)      |                  |                  |                          |
+--------------------+-------------+------------------+------------------+--------------------------+
| vnicName           | String      | 0..1             | Describes        | support:                 |
|                    |             |                  | the name of      | MANDATORY                |
|                    |             |                  | the vNIC         |                          |
|                    |             |                  | this CP          |                          |
|                    |             |                  | attaches         |                          |
|                    |             |                  | to, e.g.         |                          |
|                    |             |                  | eth0. It         |                          |
|                    |             |                  | will be          |                          |
|                    |             |                  | configured       |                          |
|                    |             |                  | during the       |                          |
|                    |             |                  | Vdu booting      |                          |
|                    |             |                  | process.         |                          |
+--------------------+-------------+------------------+------------------+--------------------------+
| vnicOrder          | Integer     | 0..1             | Describes        | support:                 |
|                    |             |                  | the order        | MANDATORY                |
|                    |             |                  | to create        |                          |
|                    |             |                  | the vNIC         |                          |
|                    |             |                  | within the       |                          |
|                    |             |                  | scope of         |                          |
|                    |             |                  | this Vdu.        |                          |
+--------------------+-------------+------------------+------------------+--------------------------+
| vnicType           | Enum        | 0..1             | Describes        | support:                 |
|                    |             |                  | the type of      | MANDATORY                |
|                    |             |                  | the vNIC         |                          |
|                    |             |                  | this CP          | valueRange:              |
|                    |             |                  | attaches         | normal,                  |
|                    |             |                  | to.              | macvtap,                 |
|                    |             |                  |                  | direct,                  |
|                    |             |                  |                  | baremetal,               |
|                    |             |                  |                  | direct-phys              |
|                    |             |                  |                  | ical                     |
|                    |             |                  |                  | and                      |
|                    |             |                  |                  | virtio-forw              |
|                    |             |                  |                  | arder                    |
+--------------------+-------------+------------------+------------------+--------------------------+
| virtualNetw        | VirtualNetw | 0..N             | Specifies        | support:                 |
| orkInterfac        | orkInterfac |                  | requirement      | MANDATORY                |
| eRequiremen        | eRequiremen |                  | s                |                          |
| ts                 | ts          |                  | on a             |                          |
|                    |             |                  | virtual          |                          |
|                    |             |                  | network          |                          |
|                    |             |                  | interface        |                          |
|                    |             |                  | realising        |                          |
|                    |             |                  | the CPs          |                          |
|                    |             |                  | instantiate      |                          |
|                    |             |                  | d                |                          |
|                    |             |                  | from this        |                          |
|                    |             |                  | CPD.             |                          |
+--------------------+-------------+------------------+------------------+--------------------------+
| (inherited         |             |                  | All              |                          |
| attributes)        |             |                  | attributes       |                          |
|                    |             |                  | inherited        |                          |
|                    |             |                  | from Cpd.        |                          |
+--------------------+-------------+------------------+------------------+--------------------------+
