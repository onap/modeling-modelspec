.. Copyright 2018 (Huawei)
.. This file is licensed under the CREATIVE COMMONS ATTRIBUTION 4.0 INTERNATIONAL LICENSE
.. Full license text at https://creativecommons.org/licenses/by/4.0/legalcode

Class: VirtualCpuPinningData
==============================

+-------------------------+-------------+------------------+-------------------------+---------------+
| **Attribute Name**      | **Type**    | **Multiplicity** | **Description**         | **Applied     |
|                         |             |                  |                         | Stereotypes** |
+=========================+=============+==================+=========================+===============+
| virtualCpuPinningPolicy | Enum        | 0..1             | The policy              | support:      |
|                         |             |                  | can take                | MANDATORY     |
|                         |             |                  | values of               |               |
|                         |             |                  | "static" or             | valueRange:   |
|                         |             |                  | "dynamic".              | "static",     |
|                         |             |                  | In case of              | "dynamic"     |
|                         |             |                  | "static" the virtual    |               |
|                         |             |                  | CPU cores are           |               |
|                         |             |                  | requested to be         |               |
|                         |             |                  | allocated to logical    |               |
|                         |             |                  | CPU cores according     |               |
|                         |             |                  | to the rules defined in |               |
|                         |             |                  | virtualCpuPinningRules. |               |
|                         |             |                  | In case of "dynamic"    |               |
|                         |             |                  | the allocation          |               |
|                         |             |                  | of virtual CPU cores    |               |
|                         |             |                  | to logical CPU cores    |               |
|                         |             |                  | is decided by the VIM.  |               |
|                         |             |                  | (e.g.: SMT              |               |
|                         |             |                  | (Simultaneous           |               |
|                         |             |                  | Multi-Threading)        |               |
|                         |             |                  | requirements).          |               |
+-------------------------+-------------+------------------+-------------------------+---------------+
| virtualCpuPinningRule   | Not         | 0..1             | A list of               | support:      |
|                         | specified   |                  | rules that              | MANDATORY     |
|                         |             |                  | should be               |               |
|                         | Editor's    |                  | considered              |               |
|                         | note: need  |                  | during the              |               |
|                         | to be       |                  | allocation              |               |
|                         | specified   |                  | of the                  |               |
|                         |             |                  | virtual CPUs to         |               |
|                         |             |                  | logical CPUs in case of |               |
|                         |             |                  | "static"                |               |
|                         |             |                  | virtualCpuPinningPolicy.|               |
+-------------------------+-------------+------------------+-------------------------+---------------+
