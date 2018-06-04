.. Copyright 2018 (China Mobile)
.. This file is licensed under the CREATIVE COMMONS ATTRIBUTION 4.0 INTERNATIONAL LICENSE
.. Full license text at https://creativecommons.org/licenses/by/4.0/legalcode

Class: ScaleInfo
================

+--------------------+----------------+------------------+-----------------+--------------------------+
| **Attribute Name** | **Type**       | **Multiplicity** | **Description** | **Applied Stereotypes**  |
+====================+================+==================+=================+==========================+
| aspectId           | Identifier     | 1                | Reference       | support:                 |
|                    | (Reference     |                  | to the          | MANDATORY                |
|                    | to             |                  | scaling         |                          |
|                    | ScalingAspect) |                  | aspect.         |                          |
+--------------------+----------------+------------------+-----------------+--------------------------+
| scaleLevel         | Integer        | 1                | The scale       | support:                 |
|                    |                |                  | level,          | MANDATORY                |
|                    |                |                  | greater         |                          |
|                    |                |                  | than or         |                          |
|                    |                |                  | equal to 0.     |                          |
+--------------------+----------------+------------------+-----------------+--------------------------+
