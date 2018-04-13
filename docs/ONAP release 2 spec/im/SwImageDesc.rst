.. Copyright 2018 (China Mobile)
.. This file is licensed under the CREATIVE COMMONS ATTRIBUTION 4.0 INTERNATIONAL LICENSE
.. Full license text at https://creativecommons.org/licenses/by/4.0/legalcode

.. contents::
   :depth: 3
..

Class: SwImageDesc
==================

+-------------------+-------------+------------------+-----------------+--------------------------+
| **Attribute Name**| **Type**    | **Multiplicity** | **Description** | **Applied Stereotypes**  |
+===================+=============+==================+=================+==========================+
| id                | Identifier  | 1                | The             | support:                 |
|                   |             |                  | identifier      | MANDATORY                |
|                   |             |                  | of this         |                          |
|                   |             |                  | software        |                          |
|                   |             |                  | image.          |                          |
+-------------------+-------------+------------------+-----------------+--------------------------+
| name              | String      | 1                | The name of     | support:                 |
|                   |             |                  | this            | MANDATORY                |
|                   |             |                  | software        |                          |
|                   |             |                  | image.          |                          |
+-------------------+-------------+------------------+-----------------+--------------------------+
| version           | String      | 1                | The version     | support:                 |
|                   |             |                  | of this         | MANDATORY                |
|                   |             |                  | software        |                          |
|                   |             |                  | image.          |                          |
+-------------------+-------------+------------------+-----------------+--------------------------+
| checksum          | String      | 1                | The             | support:                 |
|                   |             |                  | checksum of     | MANDATORY                |
|                   |             |                  | the             |                          |
|                   |             |                  | software        |                          |
|                   |             |                  | image file.     |                          |
+-------------------+-------------+------------------+-----------------+--------------------------+
| containerFo       | String      | 1                | The             | support:                 |
| rmat              |             |                  | container       | MANDATORY                |
|                   |             |                  | format          |                          |
|                   |             |                  | describes       |                          |
|                   |             |                  | the             |                          |
|                   |             |                  | container       |                          |
|                   |             |                  | file format     |                          |
|                   |             |                  | in which        |                          |
|                   |             |                  | software        |                          |
|                   |             |                  | image is        |                          |
|                   |             |                  | provided.       |                          |
+-------------------+-------------+------------------+-----------------+--------------------------+
| diskFormat        | String      | 1                | The disk        | support:                 |
|                   |             |                  | format of a     | MANDATORY                |
|                   |             |                  | software        |                          |
|                   |             |                  | image is        |                          |
|                   |             |                  | the format      |                          |
|                   |             |                  | of the          |                          |
|                   |             |                  | underlying      |                          |
|                   |             |                  | disk image.     |                          |
+-------------------+-------------+------------------+-----------------+--------------------------+
| minDisk           | Number      | 1                | The minimal     | support:                 |
|                   | (recommende |                  | disk size       | MANDATORY                |
|                   | d           |                  | requirement     |                          |
|                   | DM type:    |                  | for this        |                          |
|                   | Scalar-Unit |                  | software        |                          |
|                   | -Size)      |                  | image. The      |                          |
|                   |             |                  | value of        |                          |
|                   |             |                  | the "size       |                          |
|                   |             |                  | of storage"     |                          |
|                   |             |                  | attribute       |                          |
|                   |             |                  | of the          |                          |
|                   |             |                  | VirtualStor     |                          |
|                   |             |                  | ageDesc         |                          |
|                   |             |                  | referencing     |                          |
|                   |             |                  | this            |                          |
|                   |             |                  | SwImageDesc     |                          |
|                   |             |                  | shall not       |                          |
|                   |             |                  | be smaller      |                          |
|                   |             |                  | than the        |                          |
|                   |             |                  | value of        |                          |
|                   |             |                  | minDisk.        |                          |
+-------------------+-------------+------------------+-----------------+--------------------------+
| minRam            | Number      | 0..1             | The minimal     | support:                 |
|                   | (recommende |                  | RAM             | MANDATORY                |
|                   | d           |                  | requirement     |                          |
|                   | DM type:    |                  | for this        |                          |
|                   | Scalar-Unit |                  | software        |                          |
|                   | -Size)      |                  | image. The      |                          |
|                   |             |                  | value of        |                          |
|                   |             |                  | the "size"      |                          |
|                   |             |                  | attribute       |                          |
|                   |             |                  | of              |                          |
|                   |             |                  | VirtualMemo     |                          |
|                   |             |                  | ryData          |                          |
|                   |             |                  | of the Vdu      |                          |
|                   |             |                  | referencing     |                          |
|                   |             |                  | this            |                          |
|                   |             |                  | SwImageDesc     |                          |
|                   |             |                  | shall not       |                          |
|                   |             |                  | be smaller      |                          |
|                   |             |                  | than the        |                          |
|                   |             |                  | value of        |                          |
|                   |             |                  | minRam.         |                          |
+-------------------+-------------+------------------+-----------------+--------------------------+
| size              | Number      | 1                | The size of     | support:                 |
|                   | (recommende |                  | this            | MANDATORY                |
|                   | d           |                  | software        |                          |
|                   | DM type:    |                  | image.          |                          |
|                   | Scalar-Unit |                  |                 |                          |
|                   | -Size)      |                  |                 |                          |
+-------------------+-------------+------------------+-----------------+--------------------------+
| swImage           | Identifier  | 1                | This is a       | support:                 |
|                   | (Reference  |                  | reference       | MANDATORY                |
|                   | to a        |                  | to the          |                          |
|                   | SwImage)    |                  | actual          |                          |
|                   |             |                  | software        |                          |
|                   |             |                  | image. The      |                          |
|                   |             |                  | reference       |                          |
|                   |             |                  | can be          |                          |
|                   |             |                  | relative to     |                          |
|                   |             |                  | the root of     |                          |
|                   |             |                  | the VNF         |                          |
|                   |             |                  | Package or      |                          |
|                   |             |                  | can be a        |                          |
|                   |             |                  | URL.            |                          |
+-------------------+-------------+------------------+-----------------+--------------------------+
| operatingSy       | String      | 0..1             | Identifies      | support:                 |
| stem              |             |                  | the             | MANDATORY                |
|                   |             |                  | operating       |                          |
|                   |             |                  | system used     |                          |
|                   |             |                  | in the          |                          |
|                   |             |                  | software        |                          |
|                   |             |                  | image. This     |                          |
|                   |             |                  | attribute       |                          |
|                   |             |                  | may also        |                          |
|                   |             |                  | identify if     |                          |
|                   |             |                  | a 32 bit or     |                          |
|                   |             |                  | 64 bit          |                          |
|                   |             |                  | software        |                          |
|                   |             |                  | image is        |                          |
|                   |             |                  | used.           |                          |
+-------------------+-------------+------------------+-----------------+--------------------------+
| supportedVi       | String      | 0..N             | Identifies      | support:                 |
| rtualisatio       |             |                  | the             | MANDATORY                |
| nEnvironmen       |             |                  | virtualisat     |                          |
| t                 |             |                  | ion             |                          |
|                   |             |                  | environment     |                          |
|                   |             |                  | s               |                          |
|                   |             |                  | (e.g.           |                          |
|                   |             |                  | hypervisor)     |                          |
|                   |             |                  | compatible      |                          |
|                   |             |                  | with this       |                          |
|                   |             |                  | software        |                          |
|                   |             |                  | image.          |                          |
+-------------------+-------------+------------------+-----------------+--------------------------+
