.. Copyright 2018 (Huawei)
.. This file is licensed under the CREATIVE COMMONS ATTRIBUTION 4.0 INTERNATIONAL LICENSE
.. Full license text at https://creativecommons.org/licenses/by/4.0/legalcode

Class: LifecycleManagementScript

+--------------------+-------------+------------------+-------------------+-------------------------------------+
| **Attribute Name** | **Type**    | **Multiplicity** | **Description**   | **Applied Stereotypes**             |
+====================+=============+==================+===================+=====================================+
| event              | Enum        | 0..N             | Describes         | support:                            |
|                    |             |                  | VNF               | MANDATORY                           |
|                    |             |                  | lifecycle         |                                     |
|                    |             |                  | event(s) or       | valueRange:                         |
|                    |             |                  | an external       | for                                 |
|                    |             |                  | stimulus          | lifecycle                           |
|                    |             |                  | detected on       | events,                             |
|                    |             |                  | a VNFM            | include:                            |
|                    |             |                  | reference         | "EVENT_START_INSTANTIATION",        |
|                    |             |                  | point.            | "EVENT_END_INSTANTIATION",          |
|                    |             |                  |                   | "EVENT_START_SCALING",              |
|                    |             |                  | NOTE: At          | "EVENT_END_SCALING",                |
|                    |             |                  | least one         | "EVENT_START_SCALING_TO_LEVEL",     |
|                    |             |                  | of these          | "EVENT_END_SCALING_TO_LEVEL",       |
|                    |             |                  | two               | "EVENT_START_HEALING",              |
|                    |             |                  | attributes        | "EVENT_END_HEALING",                |
|                    |             |                  | shall be          | "EVENT_START_TERMINATION",          |
|                    |             |                  | included.         | "EVENT_END_TERMINATION",            |
|                    |             |                  |                   | "EVENT_START_VNF_FLAVOR_CHANGE",    |
|                    |             |                  |                   | "EVENT_END_VNF_FLAVOR_CHANGE",      |
|                    |             |                  |                   | "EVENT_START_VNF_OPERATION_CHANGE", |
|                    |             |                  |                   | "EVENT_END_VNF_OPERATION_CHANGE",   |
|                    |             |                  |                   | "EVENT_START_VNF_EXT_CONN_CHANGE",  |
|                    |             |                  |                   | "EVENT_END_VNF_EXT_CONN_CHANGE",    |
|                    |             |                  |                   | "EVENT_START_VNFINFO_MODIFICATION", |
|                    |             |                  |                   | "EVENT_END_VNFINFO_MODIFICATION";   |
|                    |             |                  |                   | for                                 |
|                    |             |                  |                   | external                            |
|                    |             |                  |                   | stimulus,                           |
|                    |             |                  |                   | include:                            |
|                    |             |                  |                   | receipt of                          |
|                    |             |                  |                   | request                             |
|                    |             |                  |                   | message of                          |
|                    |             |                  |                   | instantiation,                      |
|                    |             |                  |                   | scaling,                            |
|                    |             |                  |                   | healing,                            |
|                    |             |                  |                   | termination,                        |
|                    |             |                  |                   | change of                           |
|                    |             |                  |                   | VNF                                 |
|                    |             |                  |                   | flavour,                            |
|                    |             |                  |                   | change of                           |
|                    |             |                  |                   | the                                 |
|                    |             |                  |                   | operation                           |
|                    |             |                  |                   | state of                            |
|                    |             |                  |                   | the VNF,                            |
|                    |             |                  |                   | change of                           |
|                    |             |                  |                   | external                            |
|                    |             |                  |                   | VNF                                 |
|                    |             |                  |                   | connectivity,                       |
|                    |             |                  |                   | modification                        |
|                    |             |                  |                   | of VNF                              |
|                    |             |                  |                   | information                         |
|                    |             |                  |                   | or the                              |
|                    |             |                  |                   | receipt of                          |
|                    |             |                  |                   | a                                   |
|                    |             |                  |                   | notification                        |
|                    |             |                  |                   | regarding                           |
|                    |             |                  |                   | the change                          |
|                    |             |                  |                   | of a VNF                            |
|                    |             |                  |                   | indicator                           |
|                    |             |                  |                   | value.                              |
+--------------------+-------------+------------------+-------------------+-------------------------------------+
| lcmTransitionEvent | String      | 0..N             | Describes         | support:                            |
|                    |             |                  | the               | MANDATORY                           |
|                    |             |                  | transition        |                                     |
|                    |             |                  | VNF               |                                     |
|                    |             |                  | lifecycle         |                                     |
|                    |             |                  | event(s)          |                                     |
|                    |             |                  | that cannot       |                                     |
|                    |             |                  | be mapped         |                                     |
|                    |             |                  | to any of         |                                     |
|                    |             |                  | the               |                                     |
|                    |             |                  | enumerated        |                                     |
|                    |             |                  | values            |                                     |
|                    |             |                  | defined for       |                                     |
|                    |             |                  | the event         |                                     |
|                    |             |                  | attribute.        |                                     |
|                    |             |                  |                   |                                     |
|                    |             |                  | NOTE: At          |                                     |
|                    |             |                  | least one         |                                     |
|                    |             |                  | of these          |                                     |
|                    |             |                  | two               |                                     |
|                    |             |                  | attributes        |                                     |
|                    |             |                  | shall be          |                                     |
|                    |             |                  | included.         |                                     |
+--------------------+-------------+------------------+-------------------+-------------------------------------+
| script             | String      | 1                | Information       | support:                            |
|                    |             |                  | to locate a       | MANDATORY                           |
|                    |             |                  | VNF LCM           |                                     |
|                    |             |                  | script            |                                     |
|                    |             |                  | (e.g.             |                                     |
|                    |             |                  | written in        |                                     |
|                    |             |                  | a DSL as          |                                     |
|                    |             |                  | specified         |                                     |
|                    |             |                  | in                |                                     |
|                    |             |                  | requirement       |                                     |
|                    |             |                  | VNF_PACK.LCM.001) |                                     |
|                    |             |                  | triggered         |                                     |
|                    |             |                  | to react to       |                                     |
|                    |             |                  | one of the        |                                     |
|                    |             |                  | events            |                                     |
|                    |             |                  | listed in         |                                     |
|                    |             |                  | the event         |                                     |
|                    |             |                  | attribute.        |                                     |
+--------------------+-------------+------------------+-------------------+-------------------------------------+
| scriptDsl          | String      | 1                | Defines the       | support:                            |
|                    |             |                  | domain            | MANDATORY                           |
|                    |             |                  | specific          |                                     |
|                    |             |                  | language          |                                     |
|                    |             |                  | (i.e. the         |                                     |
|                    |             |                  | type) of          |                                     |
|                    |             |                  | script that       |                                     |
|                    |             |                  | is                |                                     |
|                    |             |                  | provided.         |                                     |
|                    |             |                  | Types of          |                                     |
|                    |             |                  | scripts           |                                     |
|                    |             |                  | could             |                                     |
|                    |             |                  | include           |                                     |
|                    |             |                  | bash,             |                                     |
|                    |             |                  | python,           |                                     |
|                    |             |                  | etc.              |                                     |
+--------------------+-------------+------------------+-------------------+-------------------------------------+
| scriptInput        | KeyValuePair| 0..N             | Array of          | support:                            |
|                    |             |                  | KVP               | MANDATORY                           |
|                    |             |                  | requirements      |                                     |
|                    |             |                  | with the          |                                     |
|                    |             |                  | key as the        |                                     |
|                    |             |                  | parameter         |                                     |
|                    |             |                  | name and          |                                     |
|                    |             |                  | the value         |                                     |
|                    |             |                  | as the            |                                     |
|                    |             |                  | parameter         |                                     |
|                    |             |                  | that need         |                                     |
|                    |             |                  | to be             |                                     |
|                    |             |                  | passed as         |                                     |
|                    |             |                  | an input to       |                                     |
|                    |             |                  | the script.       |                                     |
|                    |             |                  |                   |                                     |
|                    |             |                  | NOTE: The         |                                     |
|                    |             |                  | scriptInput       |                                     |
|                    |             |                  | values are        |                                     |
|                    |             |                  | passed to         |                                     |
|                    |             |                  | the scripts       |                                     |
|                    |             |                  | in addition       |                                     |
|                    |             |                  | to the            |                                     |
|                    |             |                  | parameters        |                                     |
|                    |             |                  | received in       |                                     |
|                    |             |                  | the               |                                     |
|                    |             |                  | operation         |                                     |
|                    |             |                  | invocation        |                                     |
|                    |             |                  | request or        |                                     |
|                    |             |                  | indicator         |                                     |
|                    |             |                  | value             |                                     |
|                    |             |                  | change.           |                                     |
+--------------------+-------------+------------------+-------------------+-------------------------------------+
