.. Copyright 2021
.. This file is licensed under the CREATIVE COMMONS ATTRIBUTION 4.0 INTERNATIONAL LICENSE
.. Full license text at https://creativecommons.org/licenses/by/4.0/legalcode

VES Enumeration definition
--------------------------

.. contents::
   :depth: 3
..

Enumerations
------------

AlertAction
~~~~~~~~~~~

Possible alertActions within thresholdCrossingAlertFields

Contains Enumeration Literals:

-  SET:

-  CONT:

-  CLEAR:

AlertType
~~~~~~~~~

Possible values for ThresholdCrossingAlertFIelds alertType attribute.

Contains Enumeration Literals:

-  CARD_ANOMALY:

-  INTERFACE_ANOMALY:

-  ELEMENT_ANOMALY:

-  SERVICE_ANOMALY:

Domain
~~~~~~

domain - Event domain enumeration:
'fault', 'heartbeat', 'measurementsForVfScaling', 'mobileFlow', 'other', 'sipSignaling', 'stateChange', 'syslog', 'thresholdCrossingAlert', 'voiceQuality'

Contains Enumeration Literals:

-  FAULT:

-  HEARTBEAT:

-  MEASUREMENT:

-  MOBILEFLOW:

-  NOTIFICATION:

-  OTHER:

-  PERF3GPP:

-  PNFREGISTRATION:

-  SIPSIGNALING:

-  STATECHANGE:

-  SYSLOG:

-  THRESHOLDCROSSINGALERT:

-  VOICEQUALITY:

-  STNDDEFINED:

-  STNDDEFINED:

EndpointDescription
~~~~~~~~~~~~~~~~~~~

Contains Enumeration Literals:

-  CALLER:

-  CALLEE:

EventSeverity
~~~~~~~~~~~~~

Event severity enumeration: 'CRITICAL', 'MAJOR', 'MINOR', 'WARNING', 'NORMAL'. NORMAL is used to represent clear.

Contains Enumeration Literals:

-  CRITICAL:

-  MAJOR:

-  MINOR:

-  WARNING:

-  NORMAL:

NicAdminState
~~~~~~~~~~~~~

Contains Enumeration Literals:

-  IN_SERVICE:

-  OUT_OF_SERVICE:

NicOpsState
~~~~~~~~~~~

Contains Enumeration Literals:

-  IN_SERVICE:

-  OUT_OF_SERVICE:

SourceIndicator
~~~~~~~~~~~~~~~

Indicates the source of the operation

Contains Enumeration Literals:

-  RESOURCE_OPERATION:

   -  internal operation of resource

-  MANAGEMENT_OPERATOIN:

   -  response to management operation

-  SON_OPERATOIN:

   -  result of SON

-  UNKNOWN:

   -  can't determine why

SyslogFacility
~~~~~~~~~~~~~~

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

Contains Enumeration Literals:

-  0:

   -  kernel messages

-  1:

   -  user-level messages

-  2:

   -  mail system

-  3:

   -  system daemons

-  4:

   -  security/authorization messages

-  5:

   -  messages generated internally by syslogd

-  6:

   -  line printer subsystem

-  7:

   -  network news subsystem

-  8:

   -  UUCP subsystem

-  9:

   -  clock daemon

-  10:

   -  security/authorization messages

-  11:

   -  FTP daemon

-  12:

   -  NTP subsystem

-  13:

   -  log audit

-  14:

   -  log alert

-  15:

   -  clock daemon

-  16:

   -  local use 0 (local0)

-  17:

   -  local use 1 (local1)

-  18:

   -  local use 2 (local2)

-  19:

   -  local use 3 (local3)

-  20:

   -  local use 4 (local4)

-  21:

   -  local use 5 (local5)

-  22:

   -  local use 6 (local6)

-  23:

   -  local use 7 (local7 )

SyslogSev
~~~~~~~~~

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

Contains Enumeration Literals:

-  EMERGENCY:

   -  system is unusable

   -  0

-  ALERT:

   -  1

   -  action must be taken immediately

-  CRITICAL:

   -  critical conditions

   -  2

-  ERROR:

   -  3

   -  error conditions

-  WARNING:

   -  4

   -  warning conditions

-  NOTICE:

   -  normal but significant condition

   -  5

-  INFO:

   -  Informational messages

   -  6

-  DEBUG:

   -  debug-level messages

   -  7

TCACriticality
~~~~~~~~~~~~~~

Threshold Crossing Alert counter criticality - possible values of CRIT and MAJ.

Contains Enumeration Literals:

-  CRIT:

-  MAJ:

VfStatus
~~~~~~~~

Virtual function status enumeration: 'Active', 'Idle', 'Preparing to terminate', 'Ready to terminate', 'Requesting Termination'

Contains Enumeration Literals:

-  ACTIVE:

-  IDLE:

-  PREPARING_TO_TERMINATE:

-  READY_TO_TERMINATE:

-  REQUESTING_TERMINATION:
