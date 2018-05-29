.. Copyright 2018 (China Mobile)
.. This file is licensed under the CREATIVE COMMONS ATTRIBUTION 4.0 INTERNATIONAL LICENSE
.. Full license text at https://creativecommons.org/licenses/by/4.0/legalcode

Class: Vdu
==========

+-----------------------+---------------------------+------------------+--------------------+-------------------------+
| **Attribute Name**    | **Type**                  | **Multiplicity** | **Description**    | **Applied Stereotypes** |
+=======================+===========================+==================+====================+=========================+
| vduId                 | Identifier                | 1                | Unique             | support:                |
|                       |                           |                  | identifier         | MANDATORY               |
|                       |                           |                  | of this Vdu        |                         |
|                       |                           |                  | in VNFD.           |                         |
+-----------------------+---------------------------+------------------+--------------------+-------------------------+
| name                  | String                    | 1                | Human              | support:                |
|                       |                           |                  | readable           | MANDATORY               |
|                       |                           |                  | name of the        |                         |
|                       |                           |                  | Vdu.               |                         |
+-----------------------+---------------------------+------------------+--------------------+-------------------------+
| description           | String                    | 1                | Human              | support:                |
|                       |                           |                  | readable           | MANDATORY               |
|                       |                           |                  | description        |                         |
|                       |                           |                  | of the Vdu.        |                         |
+-----------------------+---------------------------+------------------+--------------------+-------------------------+
| vduCpd                | VduCpd                    | 1..N             | Describes          | support:                |
|                       |                           |                  | network            | MANDATORY               |
|                       |                           |                  | connectivity       |                         |
|                       |                           |                  | between a          |                         |
|                       |                           |                  | VNFC               |                         |
|                       |                           |                  | instance           |                         |
|                       |                           |                  | (based on          |                         |
|                       |                           |                  | this Vdu)          |                         |
|                       |                           |                  | and an             |                         |
|                       |                           |                  | Virtual            |                         |
|                       |                           |                  | Link (VL).         |                         |
+-----------------------+---------------------------+------------------+--------------------+-------------------------+
| virtualComputeDesc    | Identifier                | 1                | Describes          | support:                |
|                       | (reference                |                  | CPU, Memory        | MANDATORY               |
|                       | to                        |                  | and                |                         |
|                       | VirtualComputeDesc)       |                  | acceleration       |                         |
|                       |                           |                  | requirements       |                         |
|                       |                           |                  | of the             |                         |
|                       |                           |                  | Virtualisation     |                         |
|                       |                           |                  | Container          |                         |
|                       |                           |                  | realising          |                         |
|                       |                           |                  | this Vdu.          |                         |
+-----------------------+---------------------------+------------------+--------------------+-------------------------+
| virtualStorageDesc    | Identifier                | 0..N             | Describes          | support:                |
|                       | (reference                |                  | storage            | MANDATORY               |
|                       | to                        |                  | requirements       |                         |
|                       | VirtualStorageDesc)       |                  | for a              |                         |
|                       |                           |                  | VirtualStorage     |                         |
|                       |                           |                  | instance           |                         |
|                       |                           |                  | attached to        |                         |
|                       |                           |                  | the                |                         |
|                       |                           |                  | virtualisation     |                         |
|                       |                           |                  | container          |                         |
|                       |                           |                  | created            |                         |
|                       |                           |                  | from               |                         |
|                       |                           |                  | virtualComputeDesc |                         |
|                       |                           |                  | defined for        |                         |
|                       |                           |                  | this Vdu.          |                         |
+-----------------------+---------------------------+------------------+--------------------+-------------------------+
| bootOrder             | KeyValuePair              | 0..N             | Boot order         | support:                |
|                       |                           |                  | of valid           | MANDATORY               |
|                       |                           |                  | boot               |                         |
|                       |                           |                  | devices.           | valueRange:             |
|                       |                           |                  |                    | "key/name"              |
|                       |                           |                  | NOTE: If no        | indicates               |
|                       |                           |                  | boot order         | the the                 |
|                       |                           |                  | is defined         | boot index              |
|                       |                           |                  | the default        | (lowest                 |
|                       |                           |                  | boot order         | index                   |
|                       |                           |                  | defined in         | defines                 |
|                       |                           |                  | the VIM or         | highest                 |
|                       |                           |                  | NFVI shall         | boot                    |
|                       |                           |                  | be used.           | priority).              |
|                       |                           |                  |                    | "value"                 |
|                       |                           |                  |                    | references              |
|                       |                           |                  |                    | a                       |
|                       |                           |                  |                    | descriptor              |
|                       |                           |                  |                    | from which              |
|                       |                           |                  |                    | a valid                 |
|                       |                           |                  |                    | boot device             |
|                       |                           |                  |                    | is created              |
|                       |                           |                  |                    | e.g.                    |
|                       |                           |                  |                    | VirtualStorageDesc      |
|                       |                           |                  |                    | from which              |
|                       |                           |                  |                    | a                       |
|                       |                           |                  |                    | VirtualStorage          |
|                       |                           |                  |                    | instance is             |
|                       |                           |                  |                    | created.                |
+-----------------------+---------------------------+------------------+--------------------+-------------------------+
| swImageDesc           | SwImageDesc               | 0..1             | Describes          | support:                |
|                       |                           |                  | the                | MANDATORY               |
|                       |                           | Editor's         | software           |                         |
|                       |                           | note: the        | image which        |                         |
|                       |                           | scenario of      | is directly        |                         |
|                       |                           | using "0"        | loaded on          |                         |
|                       |                           | needs to be      | the                |                         |
|                       |                           | clarified.       | virtualisation     |                         |
|                       |                           |                  | container          |                         |
|                       |                           |                  | realising          |                         |
|                       |                           |                  | this Vdu.          |                         |
|                       |                           |                  |                    |                         |
|                       |                           |                  | NOTE: More         |                         |
|                       |                           |                  | software           |                         |
|                       |                           |                  | images can         |                         |
|                       |                           |                  | be attached        |                         |
|                       |                           |                  | to the             |                         |
|                       |                           |                  | virtualisation     |                         |
|                       |                           |                  | container          |                         |
|                       |                           |                  | using              |                         |
|                       |                           |                  | VirtualStorage     |                         |
|                       |                           |                  | resources.         |                         |
+-----------------------+---------------------------+------------------+--------------------+-------------------------+
| nfviConstraint        | KeyValuePair              | 0..N             | Describes          | support:                |
|                       |                           |                  | constraints        | MANDATORY               |
|                       |                           |                  | on the NFVI        |                         |
|                       |                           |                  | for the            | valueRange:             |
|                       |                           |                  | VNFC               | "key/name"              |
|                       |                           |                  | instance(s)        | includes                |
|                       |                           |                  | created            | "AvailabilityZone",     |
|                       |                           |                  | from this          | "HostAggregates".       |
|                       |                           |                  | Vdu. For           |                         |
|                       |                           |                  | example,           |                         |
|                       |                           |                  | aspects of         |                         |
|                       |                           |                  | a secure           |                         |
|                       |                           |                  | hosting            |                         |
|                       |                           |                  | environment        |                         |
|                       |                           |                  | for the            |                         |
|                       |                           |                  | VNFC               |                         |
|                       |                           |                  | instance           |                         |
|                       |                           |                  | that               |                         |
|                       |                           |                  | involve            |                         |
|                       |                           |                  | additional         |                         |
|                       |                           |                  | entities or        |                         |
|                       |                           |                  | processes.         |                         |
|                       |                           |                  |                    |                         |
|                       |                           |                  | NOTE: These        |                         |
|                       |                           |                  | are                |                         |
|                       |                           |                  | constraints        |                         |
|                       |                           |                  | other than         |                         |
|                       |                           |                  | stipulating        |                         |
|                       |                           |                  | that a VNFC        |                         |
|                       |                           |                  | instance           |                         |
|                       |                           |                  | has access         |                         |
|                       |                           |                  | to a               |                         |
|                       |                           |                  | certain            |                         |
|                       |                           |                  | resource,          |                         |
|                       |                           |                  | as a               |                         |
|                       |                           |                  | prerequisite       |                         |
|                       |                           |                  | to                 |                         |
|                       |                           |                  | instantiation.     |                         |
|                       |                           |                  | The                |                         |
|                       |                           |                  | attributes         |                         |
|                       |                           |                  | virtualComputeDesc |                         |
|                       |                           |                  | and                |                         |
|                       |                           |                  | virtualStorageDesc |                         |
|                       |                           |                  | define the         |                         |
|                       |                           |                  | resources          |                         |
|                       |                           |                  | required           |                         |
|                       |                           |                  | for                |                         |
|                       |                           |                  | instantiation      |                         |
|                       |                           |                  | of the VNFC        |                         |
|                       |                           |                  | instance.          |                         |
+-----------------------+---------------------------+------------------+--------------------+-------------------------+
| monitoringParameter   | MonitoringParameter       | 0..N             | Defines the        | support:                |
|                       |                           |                  | virtualised        | MANDATORY               |
|                       |                           |                  | resources          |                         |
|                       |                           |                  | monitoring         |                         |
|                       |                           |                  | parameters         |                         |
|                       |                           |                  | on VDU             |                         |
|                       |                           |                  | level.             |                         |
+-----------------------+---------------------------+------------------+--------------------+-------------------------+
| configurableProperties| VnfcConfigurableProperties| 1                | Describes          | support:                |
|                       |                           |                  | the                | MANDATORY               |
|                       |                           |                  | configurable       |                         |
|                       |                           |                  | properties         |                         |
|                       |                           |                  | of all VNFC        |                         |
|                       |                           |                  | instances          |                         |
|                       |                           |                  | based on           |                         |
|                       |                           |                  | this VDU.          |                         |
+-----------------------+---------------------------+------------------+--------------------+-------------------------+
| injectFiles           | String                    | 0..N             | Describes          | support:                |
|                       |                           |                  | the                | MANDATORY               |
|                       |                           |                  | information        |                         |
|                       |                           |                  | (e.g. URL)         |                         |
|                       |                           |                  | about the          |                         |
|                       |                           |                  | scripts,           |                         |
|                       |                           |                  | config             |                         |
|                       |                           |                  | drive              |                         |
|                       |                           |                  | metadata,          |                         |
|                       |                           |                  | etc. which         |                         |
|                       |                           |                  | can be used        |                         |
|                       |                           |                  | during Vdu         |                         |
|                       |                           |                  | booting            |                         |
|                       |                           |                  | process.           |                         |
+-----------------------+---------------------------+------------------+--------------------+-------------------------+
                                                                                                 