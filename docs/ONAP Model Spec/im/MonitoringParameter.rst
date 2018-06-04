.. Copyright 2018 (China Mobile)
.. This file is licensed under the CREATIVE COMMONS ATTRIBUTION 4.0 INTERNATIONAL LICENSE
.. Full license text at https://creativecommons.org/licenses/by/4.0/legalcode

Class: MonitoringParameter
==========================

+-------------------+-------------+------------------+-----------------+---------------+
| **Attribute       | **Type**    | **Multiplicity** | **Description** | **Applied     |
| Name**            |             |                  |                 | Stereotypes** |
+===================+=============+==================+=================+===============+
| id                | Identifier  | 1                | Unique          | support:      |
|                   |             |                  | identifier      | MANDATORY     |
|                   |             |                  | of the          |               |
|                   |             |                  | monitoring      |               |
|                   |             |                  | parameter.      |               |
+-------------------+-------------+------------------+-----------------+---------------+
| name              | String      | 0..1             | Human           | support:      |
|                   |             |                  | readable        | MANDATORY     |
|                   |             |                  | name of the     |               |
|                   |             |                  | monitoring      |               |
|                   |             |                  | parameter.      |               |
+-------------------+-------------+------------------+-----------------+---------------+
| performanceMetric | String      | 1                | Identifies      | support:      |
|                   |             |                  | the             | MANDATORY     |
|                   |             |                  | virtualised     |               |
|                   |             |                  | resource        |               |
|                   |             |                  | performance     |               |
|                   |             |                  | metric.         |               |
+-------------------+-------------+------------------+-----------------+---------------+
| collectionPeriod  | Not         | 0..1             | An              | support:      |
|                   | specified   |                  | attribute       | MANDATORY     |
|                   |             |                  | that            |               |
|                   | Editor's    |                  | describes       |               |
|                   | note: need  |                  | the             |               |
|                   | to be       |                  | recommended     |               |
|                   | specified   |                  | periodicity     |               |
|                   |             |                  | at which to     |               |
|                   |             |                  | collect the     |               |
|                   |             |                  | performance     |               |
|                   |             |                  | information.    |               |
|                   |             |                  |                 |               |
|                   |             |                  | VNFM            |               |
|                   |             |                  | determines      |               |
|                   |             |                  | if this         |               |
|                   |             |                  | parameter       |               |
|                   |             |                  | is              |               |
|                   |             |                  | considered.     |               |
|                   |             |                  |                 |               |
|                   |             |                  | The vendor      |               |
|                   |             |                  | may provide     |               |
|                   |             |                  | this            |               |
|                   |             |                  | information     |               |
|                   |             |                  | as a            |               |
|                   |             |                  | guidance        |               |
|                   |             |                  | for             |               |
|                   |             |                  | creating        |               |
|                   |             |                  | PmJobs if       |               |
|                   |             |                  | needed.         |               |
|                   |             |                  |                 |               |
|                   |             |                  | NOTE: The       |               |
|                   |             |                  | MANO or         |               |
|                   |             |                  | NFVI may        |               |
|                   |             |                  | not support     |               |
|                   |             |                  | the             |               |
|                   |             |                  | recommended     |               |
|                   |             |                  | collectionPeriod|               |
|                   |             |                  | based on        |               |
|                   |             |                  | their           |               |
|                   |             |                  | functionalities,|               |
|                   |             |                  | and can         |               |
|                   |             |                  | reject the      |               |
|                   |             |                  | requests        |               |
|                   |             |                  | based on        |               |
|                   |             |                  | the             |               |
|                   |             |                  | recommended     |               |
|                   |             |                  | collectionPeriod|               |
|                   |             |                  | in this         |               |
|                   |             |                  | case.           |               |
+-------------------+-------------+------------------+-----------------+---------------+
