.. Copyright 2018 (China Mobile)
.. This file is licensed under the CREATIVE COMMONS ATTRIBUTION 4.0 INTERNATIONAL LICENSE
.. Full license text at https://creativecommons.org/licenses/by/4.0/legalcode

Class: SwImageDesc
==================

+-----------------------------------+-------------------+------------------+-------------------+--------------------------+
| **Attribute Name**                | **Type**          | **Multiplicity** | **Description**   | **Applied Stereotypes**  |
+===================================+===================+==================+===================+==========================+
| id                                | Identifier        | 1                | The               | support:                 |
|                                   |                   |                  | identifier        | MANDATORY                |
|                                   |                   |                  | of this           |                          |
|                                   |                   |                  | software          |                          |
|                                   |                   |                  | image.            |                          |
+-----------------------------------+-------------------+------------------+-------------------+--------------------------+
| name                              | String            | 1                | The name of       | support:                 |
|                                   |                   |                  | this              | MANDATORY                |
|                                   |                   |                  | software          |                          |
|                                   |                   |                  | image.            |                          |
+-----------------------------------+-------------------+------------------+-------------------+--------------------------+
| version                           | String            | 1                | The version       | support:                 |
|                                   |                   |                  | of this           | MANDATORY                |
|                                   |                   |                  | software          |                          |
|                                   |                   |                  | image.            |                          |
+-----------------------------------+-------------------+------------------+-------------------+--------------------------+
| checksum                          | String            | 1                | The               | support:                 |
|                                   |                   |                  | checksum of       | MANDATORY                |
|                                   |                   |                  | the               |                          |
|                                   |                   |                  | software          |                          |
|                                   |                   |                  | image file.       |                          |
+-----------------------------------+-------------------+------------------+-------------------+--------------------------+
| containerFormat                   | String            | 1                | The               | support:                 |
|                                   |                   |                  | container         | MANDATORY                |
|                                   |                   |                  | format            |                          |
|                                   |                   |                  | describes         |                          |
|                                   |                   |                  | the               |                          |
|                                   |                   |                  | container         |                          |
|                                   |                   |                  | file format       |                          |
|                                   |                   |                  | in which          |                          |
|                                   |                   |                  | software          |                          |
|                                   |                   |                  | image is          |                          |
|                                   |                   |                  | provided.         |                          |
+-----------------------------------+-------------------+------------------+-------------------+--------------------------+
| diskFormat                        | String            | 1                | The disk          | support:                 |
|                                   |                   |                  | format of a       | MANDATORY                |
|                                   |                   |                  | software          |                          |
|                                   |                   |                  | image is          |                          |
|                                   |                   |                  | the format        |                          |
|                                   |                   |                  | of the            |                          |
|                                   |                   |                  | underlying        |                          |
|                                   |                   |                  | disk image.       |                          |
+-----------------------------------+-------------------+------------------+-------------------+--------------------------+
| minDisk                           | Number            | 1                | The minimal       | support:                 |
|                                   | (recommended      |                  | disk size         | MANDATORY                |
|                                   | DM type:          |                  | requirement       |                          |
|                                   | Scalar-Unit-Size) |                  | for this          |                          |
|                                   |                   |                  | software          |                          |
|                                   |                   |                  | image. The        |                          |
|                                   |                   |                  | value of          |                          |
|                                   |                   |                  | the "size         |                          |
|                                   |                   |                  | of storage"       |                          |
|                                   |                   |                  | attribute         |                          |
|                                   |                   |                  | of the            |                          |
|                                   |                   |                  | VirtualStorageDesc|                          |
|                                   |                   |                  | referencing       |                          |
|                                   |                   |                  | this              |                          |
|                                   |                   |                  | SwImageDesc       |                          |
|                                   |                   |                  | shall not         |                          |
|                                   |                   |                  | be smaller        |                          |
|                                   |                   |                  | than the          |                          |
|                                   |                   |                  | value of          |                          |
|                                   |                   |                  | minDisk.          |                          |
+-----------------------------------+-------------------+------------------+-------------------+--------------------------+
| minRam                            | Number            | 0..1             | The minimal       | support:                 |
|                                   | (recommended      |                  | RAM               | MANDATORY                |
|                                   | DM type:          |                  | requirement       |                          |
|                                   | Scalar-Unit-Size) |                  | for this          |                          |
|                                   |                   |                  | software          |                          |
|                                   |                   |                  | image. The        |                          |
|                                   |                   |                  | value of          |                          |
|                                   |                   |                  | the "size"        |                          |
|                                   |                   |                  | attribute         |                          |
|                                   |                   |                  | of                |                          |
|                                   |                   |                  | VirtualMemoryData |                          |
|                                   |                   |                  | of the Vdu        |                          |
|                                   |                   |                  | referencing       |                          |
|                                   |                   |                  | this              |                          |
|                                   |                   |                  | SwImageDesc       |                          |
|                                   |                   |                  | shall not         |                          |
|                                   |                   |                  | be smaller        |                          |
|                                   |                   |                  | than the          |                          |
|                                   |                   |                  | value of          |                          |
|                                   |                   |                  | minRam.           |                          |
+-----------------------------------+-------------------+------------------+-------------------+--------------------------+
| size                              | Number            | 1                | The size of       | support:                 |
|                                   | (recommended      |                  | this              | MANDATORY                |
|                                   | DM type:          |                  | software          |                          |
|                                   | Scalar-Unit-Size) |                  | image.            |                          |
|                                   |                   |                  |                   |                          |
|                                   |                   |                  |                   |                          |
+-----------------------------------+-------------------+------------------+-------------------+--------------------------+
| swImage                           | Identifier        | 1                | This is a         | support:                 |
|                                   | (Reference        |                  | reference         | MANDATORY                |
|                                   | to a              |                  | to the            |                          |
|                                   | SwImage)          |                  | actual            |                          |
|                                   |                   |                  | software          |                          |
|                                   |                   |                  | image. The        |                          |
|                                   |                   |                  | reference         |                          |
|                                   |                   |                  | can be            |                          |
|                                   |                   |                  | relative to       |                          |
|                                   |                   |                  | the root of       |                          |
|                                   |                   |                  | the VNF           |                          |
|                                   |                   |                  | Package or        |                          |
|                                   |                   |                  | can be a          |                          |
|                                   |                   |                  | URL.              |                          |
+-----------------------------------+-------------------+------------------+-------------------+--------------------------+
| operatingSystem                   | String            | 0..1             | Identifies        | support:                 |
|                                   |                   |                  | the               | MANDATORY                |
|                                   |                   |                  | operating         |                          |
|                                   |                   |                  | system used       |                          |
|                                   |                   |                  | in the            |                          |
|                                   |                   |                  | software          |                          |
|                                   |                   |                  | image. This       |                          |
|                                   |                   |                  | attribute         |                          |
|                                   |                   |                  | may also          |                          |
|                                   |                   |                  | identify if       |                          |
|                                   |                   |                  | a 32 bit or       |                          |
|                                   |                   |                  | 64 bit            |                          |
|                                   |                   |                  | software          |                          |
|                                   |                   |                  | image is          |                          |
|                                   |                   |                  | used.             |                          |
+-----------------------------------+-------------------+------------------+-------------------+--------------------------+
| supportedVirtualisationEnvironment| String            | 0..N             | Identifies        | support:                 |
|                                   |                   |                  | the               | MANDATORY                |
|                                   |                   |                  | virtualisation    |                          |
|                                   |                   |                  | environments      |                          |
|                                   |                   |                  | (e.g.             |                          |
|                                   |                   |                  | hypervisor)       |                          |
|                                   |                   |                  | compatible        |                          |
|                                   |                   |                  | with this         |                          |
|                                   |                   |                  | software          |                          |
|                                   |                   |                  | image.            |                          |
+-----------------------------------+-------------------+------------------+-------------------+--------------------------+
