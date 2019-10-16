.. Copyright 2019
.. This file is licensed under the CREATIVE COMMONS ATTRIBUTION 4.0 INTERNATIONAL LICENSE
.. Full license text at https://creativecommons.org/licenses/by/4.0/legalcode

VES Enumeration definition
--------------------------

.. contents::
   :depth: 3
..

AlertAction enumeration
^^^^^^^^^^^^^^^^^^^^^^^

**Qualified Name:** Ves::TypeDefinitions::AlertAction

**Description:**

Possible alertActions within thresholdCrossingAlertFields

**Applied Stereotypes:**

-  Preliminary

**Contains Enumeration Literals:**

-  SET

-  CONT

-  CLEAR

AlertType enumeration
^^^^^^^^^^^^^^^^^^^^^

**Qualified Name:** Ves::TypeDefinitions::AlertType

**Description:**

Possible values for ThresholdCrossingAlertFIelds alertType attribute.

**Applied Stereotypes:**

-  Preliminary

**Contains Enumeration Literals:**

-  CARD_ANOMALY

-  INTERFACE_ANOMALY

-  ELEMENT_ANOMALY

-  SERVICE_ANOMALY

Domain enumeration
^^^^^^^^^^^^^^^^^^

**Qualified Name:** Ves::TypeDefinitions::Domain

**Description:**

domain - Event domain enumeration:

'fault', 'heartbeat', 'measurementsForVfScaling', 'mobileFlow', 'other', 'sipSignaling', 'stateChange', 'syslog', 'thresholdCrossingAlert', 'voiceQuality'

**Applied Stereotypes:**

-  Preliminary

**Contains Enumeration Literals:**

-  FAULT

-  HEARTBEAT

-  MEASUREMENT

-  MOBILEFLOW

-  NOTIFICATION

-  OTHER

-  PERF3GPP

-  PNFREGISTRATION

-  SIPSIGNALING

-  STATECHANGE

-  SYSLOG

-  THRESHOLDCROSSINGALERT

-  VOICEQUALITY

EndpointDescription enumeration
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

**Qualified Name:** Ves::TypeDefinitions::EndpointDescription

**Applied Stereotypes:**

-  Preliminary

**Contains Enumeration Literals:**

-  CALLER

-  CALLEE

EventSeverity enumeration
^^^^^^^^^^^^^^^^^^^^^^^^^

**Qualified Name:** Ves::TypeDefinitions::EventSeverity

**Description:**

Event severity enumeration: 'CRITICAL', 'MAJOR', 'MINOR', 'WARNING', 'NORMAL'. NORMAL is used to represent clear.

**Applied Stereotypes:**

-  Preliminary

**Contains Enumeration Literals:**

-  CRITICAL

-  MAJOR

-  MINOR

-  WARNING

-  NORMAL

NicAdminState enumeration
^^^^^^^^^^^^^^^^^^^^^^^^^

**Qualified Name:** Ves::TypeDefinitions::NicAdminState

**Applied Stereotypes:**

-  Preliminary

**Contains Enumeration Literals:**

-  IN_SERVICE

-  OUT_OF_SERVICE

NicOpsState enumeration
^^^^^^^^^^^^^^^^^^^^^^^

**Qualified Name:** Ves::TypeDefinitions::NicOpsState

**Applied Stereotypes:**

-  Preliminary

**Contains Enumeration Literals:**

-  IN_SERVICE

-  OUT_OF_SERVICE

SyslogFacility enumeration
^^^^^^^^^^^^^^^^^^^^^^^^^^

**Qualified Name:** Ves::TypeDefinitions::SyslogFacility

**Description:**

Numeric code from 0 to 23 for facility:

0 kernel messages

1 user-level messages

2 mail system

3 system daemons

4 security/authorization messages

5 messages generated internally by syslogd

6 line printer subsystem

7 network news subsystem

8 UUCP subsystem

9 clock daemon

10 security/authorization messages

11 FTP daemon

12 NTP subsystem

13 log audit

14 log alert

15 clock daemon (note 2)

16 local use 0 (local0)

17 local use 1 (local1)

18 local use 2 (local2)

19 local use 3 (local3)

20 local use 4 (local4)

21 local use 5 (local5)

22 local use 6 (local6)

23 local use 7 (local7)

**Applied Stereotypes:**

-  Preliminary

**Contains Enumeration Literals:**

-  0

   -  kernel messages

-  1

   -  user-level messages

-  2

   -  mail system

-  3

   -  system daemons

-  4

   -  security/authorization messages

-  5

   -  messages generated internally by syslogd

-  6

   -  line printer subsystem

-  7

   -  network news subsystem

-  8

   -  UUCP subsystem

-  9

   -  clock daemon

-  10

   -  security/authorization messages

-  11

   -  FTP daemon

-  12

   -  NTP subsystem

-  13

   -  log audit

-  14

   -  log alert

-  15

   -  clock daemon

-  16

   -  local use 0 (local0)

-  17

   -  local use 1 (local1)

-  18

   -  local use 2 (local2)

-  19

   -  local use 3 (local3)

-  20

   -  local use 4 (local4)

-  21

   -  local use 5 (local5)

-  22

   -  local use 6 (local6)

-  23

   -  local use 7 (local7 )

SyslogSev enumeration
^^^^^^^^^^^^^^^^^^^^^

**Qualified Name:** Ves::TypeDefinitions::SyslogSev

**Description:**

Level-of-severity text enumeration defined below:

Text Sev Description

Emergency 0 system is unusable

Alert 1 action must be taken immediately

Critical 2 critical conditions

Error 3 error conditions

Warning 4 warning conditions

Notice 5 normal but significant condition

Info 6 Informational messages

Debug 7 debug-level messages

**Applied Stereotypes:**

-  Preliminary

**Contains Enumeration Literals:**

-  EMERGENCY

   -  0

   -  system is unusable

-  ALERT

   -  action must be taken immediately

   -  1

-  CRITICAL

   -  2

   -  critical conditions

-  ERROR

   -  error conditions

   -  3

-  WARNING

   -  4

   -  warning conditions

-  NOTICE

   -  5

   -  normal but significant condition

-  INFO

   -  6

   -  Informational messages

-  DEBUG

   -  7

   -  debug-level messages

TCACriticality enumeration
^^^^^^^^^^^^^^^^^^^^^^^^^^

**Qualified Name:** Ves::TypeDefinitions::TCACriticality

**Description:**

Threshold Crossing Alert counter criticality - possible values of CRIT and MAJ.

**Applied Stereotypes:**

-  Preliminary

**Contains Enumeration Literals:**

-  CRIT

-  MAJ

VfStatus enumeration
^^^^^^^^^^^^^^^^^^^^

**Qualified Name:** Ves::TypeDefinitions::VfStatus

**Description:**

Virtual function status enumeration: 'Active', 'Idle', 'Preparing to terminate', 'Ready to terminate', 'Requesting Termination'

**Applied Stereotypes:**

-  Preliminary

**Contains Enumeration Literals:**

-  ACTIVE

-  IDLE

-  PREPARING_TO_TERMINATE

-  READY_TO_TERMINATE

-  REQUESTING_TERMINATION
