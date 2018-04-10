.. Copyright 2018 (China Mobile)
.. This file is licensed under the CREATIVE COMMONS ATTRIBUTION 4.0 INTERNATIONAL LICENSE
.. Full license text at https://creativecommons.org/licenses/by/4.0/legalcode

.. contents::
   :depth: 3
..

Class: VDU/VDUDesc
==================

+-------------------+-------------+------------------+-----------------+-------------------------+
| **Attribute Name**| **Type**    | **Multiplicity** | **Description** | **Applied Stereotypes** |
+===================+=============+==================+=================+=========================+
| vduId             | Identifier  | 1                | Unique          | support:                |
|                   |             |                  | identifier      | MANDATORY               |
|                   |             |                  | of this Vdu     |                         |
|                   |             |                  | in VNFD.        |                         |
+-------------------+-------------+------------------+-----------------+-------------------------+
| name              | String      | 1                | Human           | support:                |
|                   |             |                  | readable        | MANDATORY               |
|                   |             |                  | name of the     |                         |
|                   |             |                  | Vdu.            |                         |
+-------------------+-------------+------------------+-----------------+-------------------------+
| description       | String      | 1                | Human           | support:                |
|                   |             |                  | readable        | MANDATORY               |
|                   |             |                  | description     |                         |
|                   |             |                  | of the Vdu.     |                         |
+-------------------+-------------+------------------+-----------------+-------------------------+
| vduCpd            | VduCpd/VDUC | 1..N             | Describes       | support:                |
|                   | PDesc       |                  | network         | MANDATORY               |
|                   |             |                  | connectivit     |                         |
|                   |             |                  | y               |                         |
|                   |             |                  | between a       |                         |
|                   |             |                  | VNFC            |                         |
|                   |             |                  | instance        |                         |
|                   |             |                  | (based on       |                         |
|                   |             |                  | this Vdu)       |                         |
|                   |             |                  | and an          |                         |
|                   |             |                  | Virtual         |                         |
|                   |             |                  | Link (VL).      |                         |
+-------------------+-------------+------------------+-----------------+-------------------------+
| virtualComp       | Identifier  | 1                | Describes       | support:                |
| uteDesc           | (reference  |                  | CPU, Memory     | MANDATORY               |
|                   | to          |                  | and             |                         |
|                   | VirtualComp |                  | acceleratio     |                         |
|                   | uteDesc)    |                  | n               |                         |
|                   |             |                  | requirement     |                         |
|                   |             |                  | s               |                         |
|                   |             |                  | of the          |                         |
|                   |             |                  | Virtualisat     |                         |
|                   |             |                  | ion             |                         |
|                   |             |                  | Container       |                         |
|                   |             |                  | realising       |                         |
|                   |             |                  | this Vdu.       |                         |
+-------------------+-------------+------------------+-----------------+-------------------------+
| virtualStor       | Identifier  | 0..N             | Describes       | support:                |
| ageDesc           | (reference  |                  | storage         | MANDATORY               |
|                   | to          |                  | requirement     |                         |
|                   | VirtualStor |                  | s               |                         |
|                   | ageDesc)    |                  | for a           |                         |
|                   |             |                  | VirtualStor     |                         |
|                   |             |                  | age             |                         |
|                   |             |                  | instance        |                         |
|                   |             |                  | attached to     |                         |
|                   |             |                  | the             |                         |
|                   |             |                  | virtualisat     |                         |
|                   |             |                  | ion             |                         |
|                   |             |                  | container       |                         |
|                   |             |                  | created         |                         |
|                   |             |                  | from            |                         |
|                   |             |                  | virtualComp     |                         |
|                   |             |                  | uteDesc         |                         |
|                   |             |                  | defined for     |                         |
|                   |             |                  | this Vdu.       |                         |
+-------------------+-------------+------------------+-----------------+-------------------------+
| bootOrder         | KeyValuePai | 0..N             | Boot order      | support:                |
|                   | r/NameValue |                  | of valid        | MANDATORY               |
|                   | Pair        |                  | boot            |                         |
|                   |             |                  | devices.        | valueRange:             |
|                   |             |                  |                 | "key/name"              |
|                   |             |                  | NOTE: If no     | indicates               |
|                   |             |                  | boot order      | the the                 |
|                   |             |                  | is defined      | boot index              |
|                   |             |                  | the default     | (lowest                 |
|                   |             |                  | boot order      | index                   |
|                   |             |                  | defined in      | defines                 |
|                   |             |                  | the VIM or      | highest                 |
|                   |             |                  | NFVI shall      | boot                    |
|                   |             |                  | be used.        | priority).              |
|                   |             |                  |                 | "value"                 |
|                   |             |                  |                 | references              |
|                   |             |                  |                 | a                       |
|                   |             |                  |                 | descriptor              |
|                   |             |                  |                 | from which              |
|                   |             |                  |                 | a valid                 |
|                   |             |                  |                 | boot device             |
|                   |             |                  |                 | is created              |
|                   |             |                  |                 | e.g.                    |
|                   |             |                  |                 | VirtualStor             |
|                   |             |                  |                 | ageDesc                 |
|                   |             |                  |                 | from which              |
|                   |             |                  |                 | a                       |
|                   |             |                  |                 | VirtualStor             |
|                   |             |                  |                 | age                     |
|                   |             |                  |                 | instance is             |
|                   |             |                  |                 | created.                |
+-------------------+-------------+------------------+-----------------+-------------------------+
| swImageDesc       | SwImageDesc | 0..1             | Describes       | support:                |
|                   |             |                  | the             | MANDATORY               |
|                   |             | Editor's         | software        |                         |
|                   |             | note: the        | image which     |                         |
|                   |             | scenario of      | is directly     |                         |
|                   |             | using "0"        | loaded on       |                         |
|                   |             | needs to be      | the             |                         |
|                   |             | clarified.       | virtualisat     |                         |
|                   |             |                  | ion             |                         |
|                   |             |                  | container       |                         |
|                   |             |                  | realising       |                         |
|                   |             |                  | this Vdu.       |                         |
|                   |             |                  |                 |                         |
|                   |             |                  | NOTE: More      |                         |
|                   |             |                  | software        |                         |
|                   |             |                  | images can      |                         |
|                   |             |                  | be attached     |                         |
|                   |             |                  | to the          |                         |
|                   |             |                  | virtualisat     |                         |
|                   |             |                  | ion             |                         |
|                   |             |                  | container       |                         |
|                   |             |                  | using           |                         |
|                   |             |                  | VirtualStor     |                         |
|                   |             |                  | age             |                         |
|                   |             |                  | resources.      |                         |
+-------------------+-------------+------------------+-----------------+-------------------------+
| nfviConstra       | KeyValuthae | 0..N             | Describes       | support:                |
| int               | Pair/NameVa |                  | constraints     | MANDATORY               |
|                   | luePair     |                  | on the NFVI     |                         |
|                   |             |                  | for the         | valueRange:             |
|                   |             |                  | VNFC            | "key/name"              |
|                   |             |                  | instance(s)     | includes                |
|                   |             |                  | created         | "Availabili             |
|                   |             |                  | from this       | tyZone",                |
|                   |             |                  | Vdu. For        | "HostAggreg             |
|                   |             |                  | example,        | ates".                  |
|                   |             |                  | aspects of      |                         |
|                   |             |                  | a secure        |                         |
|                   |             |                  | hosting         |                         |
|                   |             |                  | environment     |                         |
|                   |             |                  | for the         |                         |
|                   |             |                  | VNFC            |                         |
|                   |             |                  | instance        |                         |
|                   |             |                  | that            |                         |
|                   |             |                  | involve         |                         |
|                   |             |                  | additional      |                         |
|                   |             |                  | entities or     |                         |
|                   |             |                  | processes.      |                         |
|                   |             |                  |                 |                         |
|                   |             |                  | NOTE: These     |                         |
|                   |             |                  | are             |                         |
|                   |             |                  | constraints     |                         |
|                   |             |                  | other than      |                         |
|                   |             |                  | stipulating     |                         |
|                   |             |                  | that a VNFC     |                         |
|                   |             |                  | instance        |                         |
|                   |             |                  | has access      |                         |
|                   |             |                  | to a            |                         |
|                   |             |                  | certain         |                         |
|                   |             |                  | resource,       |                         |
|                   |             |                  | as a            |                         |
|                   |             |                  | prerequisit     |                         |
|                   |             |                  | e               |                         |
|                   |             |                  | to              |                         |
|                   |             |                  | instantiati     |                         |
|                   |             |                  | on.             |                         |
|                   |             |                  | The             |                         |
|                   |             |                  | attributes      |                         |
|                   |             |                  | virtualComp     |                         |
|                   |             |                  | uteDesc         |                         |
|                   |             |                  | and             |                         |
|                   |             |                  | virtualStor     |                         |
|                   |             |                  | ageDesc         |                         |
|                   |             |                  | define the      |                         |
|                   |             |                  | resources       |                         |
|                   |             |                  | required        |                         |
|                   |             |                  | for             |                         |
|                   |             |                  | instantiati     |                         |
|                   |             |                  | on              |                         |
|                   |             |                  | of the VNFC     |                         |
|                   |             |                  | instance.       |                         |
+-------------------+-------------+------------------+-----------------+-------------------------+
| monitoringP       | MonitoringP | 0..N             | Defines the     | support:                |
| arameter          | arameter    |                  | virtualised     | MANDATORY               |
|                   |             |                  | resources       |                         |
|                   |             |                  | monitoring      |                         |
|                   |             |                  | parameters      |                         |
|                   |             |                  | on VDU          |                         |
|                   |             |                  | level.          |                         |
+-------------------+-------------+------------------+-----------------+-------------------------+
| configurabl       | VnfcConfigu | 1                | Describes       | support:                |
| eProperties       | rableProper |                  | the             | MANDATORY               |
|                   | ties        |                  | configurabl     |                         |
|                   |             |                  | e               |                         |
|                   |             |                  | properties      |                         |
|                   |             |                  | of all VNFC     |                         |
|                   |             |                  | instances       |                         |
|                   |             |                  | based on        |                         |
|                   |             |                  | this VDU.       |                         |
+-------------------+-------------+------------------+-----------------+-------------------------+
| injectFiles       | String      | 0..N             | Describes       | support:                |
|                   |             |                  | the             | MANDATORY               |
|                   |             |                  | information     |                         |
|                   |             |                  | (e.g. URL)      |                         |
|                   |             |                  | about the       |                         |
|                   |             |                  | scripts,        |                         |
|                   |             |                  | config          |                         |
|                   |             |                  | drive           |                         |
|                   |             |                  | metadata,       |                         |
|                   |             |                  | etc. which      |                         |
|                   |             |                  | can be used     |                         |
|                   |             |                  | during Vdu      |                         |
|                   |             |                  | booting         |                         |
|                   |             |                  | process.        |                         |
+-------------------+-------------+------------------+-----------------+-------------------------+
|                   |             |                  |                 |                         |
+-------------------+-------------+------------------+-----------------+-------------------------+
                                                                                                 