.. Copyright 2018 (China Mobile)
.. This file is licensed under the CREATIVE COMMONS ATTRIBUTION 4.0 INTERNATIONAL LICENSE
.. Full license text at https://creativecommons.org/licenses/by/4.0/legalcode

Class: InstantiationLevel
=========================

+------------------------+-------------------------+------------------+-------------------+--------------------------+
| **Attribute Name**     | **Type**                | **Multiplicity** | **Description**   | **Applied Stereotypes**  |
+========================+=========================+==================+===================+==========================+
| levelId                | Identifier              | 1                | Uniquely          | support:                 |
|                        |                         |                  | identifies        | MANDATORY                |
|                        |                         |                  | a level           |                          |
|                        |                         |                  | with the DF.      |                          |
+------------------------+-------------------------+------------------+-------------------+--------------------------+
| description            | String                  | 1                | Human             | support:                 |
|                        |                         |                  | readable          | MANDATORY                |
|                        |                         |                  | description       |                          |
|                        |                         |                  | of the level.     |                          |
+------------------------+-------------------------+------------------+-------------------+--------------------------+
| vduLevel               | VduLevel                | 1..N             | Indicates         | support:                 |
|                        |                         |                  | the number        | MANDATORY                |
|                        |                         |                  | of instance       |                          |
|                        |                         |                  | of this VDU       |                          |
|                        |                         |                  | to deploy         |                          |
|                        |                         |                  | for this level.   |                          |
+------------------------+-------------------------+------------------+-------------------+--------------------------+
| virtualLinkBitRateLevel| VirtualLinkBitRateLevel | 0..N             | Specifies         | support:                 |
|                        |                         |                  | bitrate           | MANDATORY                |
|                        |                         |                  | requirements      |                          |
|                        |                         |                  | applicable        |                          |
|                        |                         |                  | to virtual links  |                          |
|                        |                         |                  | created from      |                          |
|                        |                         |                  | particular        |                          |
|                        |                         |                  | virtual link      |                          |
|                        |                         |                  | descriptors       |                          |
|                        |                         |                  | for this level.   |                          |
|                        |                         |                  |                   |                          |
|                        |                         |                  | NOTE: If not      |                          |
|                        |                         |                  | present, it       |                          |
|                        |                         |                  | is assumed        |                          |
|                        |                         |                  | that the bitrate  |                          |
|                        |                         |                  | requirements      |                          |
|                        |                         |                  | can be derived    |                          |
|                        |                         |                  | from those        |                          |
|                        |                         |                  | specified in the  |                          |
|                        |                         |                  | VduCpd instances  |                          |
|                        |                         |                  | applicable        |                          |
|                        |                         |                  | to the internal   |                          |
|                        |                         |                  | VL. If            |                          |
|                        |                         |                  | present in        |                          |
|                        |                         |                  | both the          |                          |
|                        |                         |                  | InstantiationLevel|                          |
|                        |                         |                  | and the VduCpd    |                          |
|                        |                         |                  | instances         |                          |
|                        |                         |                  | applicable        |                          |
|                        |                         |                  | to the            |                          |
|                        |                         |                  | internal VL, the  |                          |
|                        |                         |                  | highest           |                          |
|                        |                         |                  | value takes       |                          |
|                        |                         |                  | precedence.       |                          |
+------------------------+-------------------------+------------------+-------------------+--------------------------+
| scaleInfo              | ScaleInfo               | 0..N             | Represents        | support:                 |
|                        |                         |                  | for each          | MANDATORY                |
|                        |                         |                  | aspect the        |                          |
|                        |                         |                  | scale level that  |                          |
|                        |                         |                  | corresponds       |                          |
|                        |                         |                  | to this           |                          |
|                        |                         |                  | instantiation     |                          |
|                        |                         |                  | level.            |                          |
|                        |                         |                  | scaleInfo         |                          |
|                        |                         |                  | shall be          |                          |
|                        |                         |                  | present if        |                          |
|                        |                         |                  | the VNF           |                          |
|                        |                         |                  | supports scaling. |                          |
+------------------------+-------------------------+------------------+-------------------+--------------------------+
