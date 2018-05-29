.. Copyright 2018 (China Mobile)
.. This file is licensed under the CREATIVE COMMONS ATTRIBUTION 4.0 INTERNATIONAL LICENSE
.. Full license text at https://creativecommons.org/licenses/by/4.0/legalcode

Class: PlacementGroup (Experimental)
====================================

+-------------------+-------------+------------------+-----------------+---------------+
| **Attribute       | **Type**    | **Multiplicity** | **Description** | **Applied     |
| Name**            |             |                  |                 | Stereotypes** |
+===================+=============+==================+=================+===============+
| elementGroupId    | Identifier  | 1                | Unique          | support:      |
|                   |             |                  | identifier      | MANDATORY     |
|                   |             |                  | of this         |               |
|                   |             |                  | group in        |               |
|                   |             |                  | the VNFD.       |               |
+-------------------+-------------+------------------+-----------------+---------------+
| placementStrategy | Enum        | 1                | Determine       | support:      |
|                   |             |                  | where           | MANDATORY     |
|                   |             |                  | VNFC's          |               |
|                   |             |                  | (VDU's) are     | valueRange:   |
|                   |             |                  | placed with     | "co-location",|
|                   |             |                  | respect to      | "isolation",  |
|                   |             |                  | the VNF.        | "exclusively" |
|                   |             |                  |                 |               |
|                   |             |                  |                 | NOTE:         |
|                   |             |                  |                 |               |
|                   |             |                  |                 | -  Co-location|
|                   |             |                  |                 |    -          |
|                   |             |                  |                 |    members    |
|                   |             |                  |                 |    of the     |
|                   |             |                  |                 |    group      |
|                   |             |                  |                 |    share      |
|                   |             |                  |                 |    the same   |
|                   |             |                  |                 |    physical   |
|                   |             |                  |                 |    host or    |
|                   |             |                  |                 |    rack.      |
|                   |             |                  |                 |               |
|                   |             |                  |                 | -  isolation  |
|                   |             |                  |                 |    -          |
|                   |             |                  |                 |    members    |
|                   |             |                  |                 |    of the     |
|                   |             |                  |                 |    group do   |
|                   |             |                  |                 |    not        |
|                   |             |                  |                 |    share      |
|                   |             |                  |                 |    the same   |
|                   |             |                  |                 |    physical   |
|                   |             |                  |                 |    host or    |
|                   |             |                  |                 |    rack.      |
|                   |             |                  |                 |               |
|                   |             |                  |                 | -  Exclusively|
|                   |             |                  |                 |    -          |
|                   |             |                  |                 |    members    |
|                   |             |                  |                 |    have       |
|                   |             |                  |                 |    sole use   |
|                   |             |                  |                 |    of a       |
|                   |             |                  |                 |    given      |
|                   |             |                  |                 |    physical   |
|                   |             |                  |                 |    host or    |
|                   |             |                  |                 |    rack       |
|                   |             |                  |                 |    (not       |
|                   |             |                  |                 |    shared     |
|                   |             |                  |                 |    with any   |
|                   |             |                  |                 |    vnfcs      |
|                   |             |                  |                 |    outside    |
|                   |             |                  |                 |    the        |
|                   |             |                  |                 |    group).    |
+-------------------+-------------+------------------+-----------------+---------------+
| vnfcMembers       | Not         | 0..N             | References      | support:      |
|                   | specified   |                  | to Vdus         | MANDATORY     |
|                   |             |                  | that are        |               |
|                   |             |                  | part of         |               |
|                   |             |                  | this group.     |               |
|                   |             |                  |                 |               |
|                   |             |                  |                 |               |
|                   |             |                  |                 |               |
+-------------------+-------------+------------------+-----------------+---------------+
| strategyScope     | Enum        | 1                | indicate if     | support:      |
|                   |             |                  | the             | MANDATORY     |
|                   |             |                  | strategy is     |               |
|                   |             |                  | applied at      | valueRange:   |
|                   |             |                  | the host or     | "host",       |
|                   |             |                  | rack level      | "rack"        |
+-------------------+-------------+------------------+-----------------+---------------+
