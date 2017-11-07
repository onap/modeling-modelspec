.. contents::
   :depth: 3
..

1. NS&VNF Package Specification V0.4
=======================================

1.1 Scope
-------------

The scope of the present document is to describe the NS&VNF CSAR model
specification for OPENO.

1.2 Terms, Definitions and Abbreviations
----------------------------------------------

For the purposes of the present document, the following abbreviations
apply:

+-----------------------------------+-----------------------------------+
| Abbreviation                      | Definition                        |
+===================================+===================================+
| CSAR                              | TOSCA Cloud Service Archive       |
+-----------------------------------+-----------------------------------+
| CSAR Model                        | ……                                |
+-----------------------------------+-----------------------------------+
| NS                                | Network Service                   |
+-----------------------------------+-----------------------------------+
| NSD                               | Network Service Descriptor        |
+-----------------------------------+-----------------------------------+
| TOSCA                             | Topology and Orchestration        |
|                                   | Specification for Cloud           |
|                                   | Applications                      |
+-----------------------------------+-----------------------------------+
| VNF                               | Virtual Network Function          |
+-----------------------------------+-----------------------------------+
| VNFD                              | Virtual Network Function          |
|                                   | Descriptor                        |
+-----------------------------------+-----------------------------------+

1.3 NS&VNF CSAR Model Definitio
----------------------------------------

In OPENO, TOSCA language is adopted to describe the NS/VNF Package. This
document refers to “TOSCA Simple Profile YAML v1.0” and
“tosca-nfv-profile-wd04-Rev06” specification. Base on those
specifications, these clauses below focus on extension and satisfy the
open NS/VNF package requirements.

1.3.1 CSAR Introduction
~~~~~~~~~~~~~~~~~~~~~~~~

A CSAR is a zip file containing at least two directories, the
TOSCA-Metadata directory and the Definitions directory. Beyond that,
other directories MAY be contained in a CSAR, i.e. the creator of a CSAR
has all freedom to define the content of a CSAR and the structuring of
this content as appropriate for the cloud application.

The TOSCA-Metadata directory contains metadata describing the other
content of the CSAR. This metadata is referred to as TOSCA meta file.
This file is named TOSCA and has the file extension .meta.

The Definitions directory contains one or more TOSCA Definitions
documents (file extension .tosca). These Definitions files typically
contain definitions related to the cloud application of the CSAR. In
addition, CSARs can contain just the definition of elements for re-use
in other contexts. For example, a CSAR might be used to package a set of
Node Types and Relationship Types with their respective implementations
that can then be used by Service Templates provided in other CSARs. In
cases where a complete cloud application is packaged in a CSAR, one of
the Definitions documents in the Definitions directory MUST contain a
Service Template definition that defines the structure and behavior of
the cloud application.

1.3.2 NS CSAR Model Structure
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

+----------------------+----------------------+----------------------+
| Dirctory/Files       | Qualifier            | Description          |
+======================+======================+======================+
| /TOSCA-Metadata/TOSC | M                    | Describing the other |
| A.meta               |                      | content of the CSAR. |
|                      |                      |                      |
|                      |                      | The detail of        |
|                      |                      | “TOSCA.meta” format  |
|                      |                      | refers to clause     |
|                      |                      | 3.4.                 |
+----------------------+----------------------+----------------------+
| /Definitions         | M                    | Including simple     |
|                      |                      | TOSCA Type           |
|                      |                      | Definition and       |
|                      |                      | NSD/VNFD definition  |
|                      |                      | files                |
|                      |                      |                      |
|                      |                      | The detail of NSD    |
|                      |                      | format refers to <   |
|                      |                      | NSD Specification>.  |
+----------------------+----------------------+----------------------+
| /checksum.lst        | O                    | It is a txt file for |
|                      |                      | record the important |
|                      |                      | file checksum.       |
|                      |                      |                      |
|                      |                      | Such as              |
|                      |                      | SoftwareImages files |
|                      |                      | or AppSoftware       |
|                      |                      | files.               |
|                      |                      |                      |
|                      |                      | The detail of        |
|                      |                      | “checksum.lst”       |
|                      |                      | format refers to     |
|                      |                      | clause 3.6.          |
+----------------------+----------------------+----------------------+
| /Policies            | O                    | Policies Definition  |
|                      |                      | files.               |
+----------------------+----------------------+----------------------+
| /Plans               | O                    | LCM Workflow Plans   |
|                      |                      |                      |
|                      |                      | Deploy, Termination, |
|                      |                      | etc.                 |
+----------------------+----------------------+----------------------+

1.3.3 VNF CSAR Model Structure
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

+----------------------+----------------------+----------------------+
| Dirctory/Files       | Qualifier            | Description          |
+======================+======================+======================+
| /TOSCA-Metadata/TOSC | M                    | Describing the other |
| A.meta               |                      | content of the CSAR. |
|                      |                      |                      |
|                      |                      | The detail of        |
|                      |                      | “TOSCA.meta” format  |
|                      |                      | refers to clause     |
|                      |                      | 3.3.                 |
+----------------------+----------------------+----------------------+
| /Definitions         | M                    | Including simple     |
|                      |                      | TOSCA Type           |
|                      |                      | Definition and       |
|                      |                      | NSD/VNFD definition  |
|                      |                      | files                |
|                      |                      |                      |
|                      |                      | The detail of VNFD   |
|                      |                      | format refers to <   |
|                      |                      | VNFD pecification>.  |
+----------------------+----------------------+----------------------+
| /checksum.lst        | O                    | It is a txt file for |
|                      |                      | record the important |
|                      |                      | file checksum.       |
|                      |                      |                      |
|                      |                      | Such as              |
|                      |                      | SoftwareImages files |
|                      |                      | or AppSoftware       |
|                      |                      | files.               |
|                      |                      |                      |
|                      |                      | The detail of        |
|                      |                      | “checksum.lst”       |
|                      |                      | format refers to     |
|                      |                      | clause 3.4.          |
+----------------------+----------------------+----------------------+
| /SoftwareImages      | O                    | VNF Image directory. |
|                      |                      |                      |
|                      |                      | The Images can be in |
|                      |                      | a fixed URL, such as |
|                      |                      | in the catalog       |
|                      |                      | public directory on  |
|                      |                      | order to be imported |
|                      |                      | by VNFD file.        |
+----------------------+----------------------+----------------------+
| /AppSoftwares        | O                    | VNF Software         |
|                      |                      | directory            |
|                      |                      |                      |
|                      |                      | The VNF Software can |
|                      |                      | be in a fixed URL,   |
|                      |                      | such as in the       |
|                      |                      | catalog public       |
|                      |                      | directory on order   |
|                      |                      | to be imported by    |
|                      |                      | VNFD file.           |
+----------------------+----------------------+----------------------+
| /Policies            | O                    | Policies Definition  |
|                      |                      | files.               |
+----------------------+----------------------+----------------------+
| /Scripts             | O                    | LCM Scripts          |
|                      |                      |                      |
|                      |                      | Deploy, Termination, |
|                      |                      | Test, etc.           |
+----------------------+----------------------+----------------------+

1.3.4 TOSCA Meta File Definition
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

The TOSCA meta file includes metadata that allows interpreting the
various artifacts within the CSAR properly. The TOSCA.meta file is
contained in the TOSCA-Metadata directory of the CSAR.

A TOSCA meta file consists of name/value pairs. The name-part of a
name/value pair is followed by a colon, followed by a blank, followed by
the value-part of the name/value pair. The name MUST NOT contain a
colon. Values that represent binary data MUST be base64 encoded. Values
that extend beyond one line can be spread over multiple lines if each
subsequent line starts with at least one space. Such spaces are then
collapsed when the value string is read.

+-----------------+
| <name>: <value> |
+-----------------+

Each name/value pair is in a separate line. A list of related name/value
pairs, i.e. a list of consecutive name/value pairs describing a
particular file in a CSAR, is called a block. Blocks are separated by an
empty line. The first block, called block_0, is metadata about the CSAR
itself. All other blocks represent metadata of files in the CSAR.

The structure of block_0 in the TOSCA meta file is as follows:

+--------------------------------------+
| TOSCA-Meta-File-Version: digit.digit |
|                                      |
| CSAR-Version: digit.digit            |
|                                      |
| Created-By: string                   |
|                                      |
| Entry-Definitions: string ?          |
+--------------------------------------+

The name/value pairs are as follows:

-  TOSCA-Meta-File-Version: This is the version number of the TOSCA meta
   file format. The value MUST be “1.0” in the current version of the
   TOSCA specification.

-  CSAR-Version: This is the version number of the CSAR specification.
   The value MUST be “1.0” in the current version of the TOSCA
   specification.

-  Created-By: The person or vendor, respectively, who created the CSAR.

-  Entry-Definitions: This OPTIONAL name/value pair references a TOSCA
   Definitions file from the Definitions directory of the CSAR that
   SHOULD be used as entry point for processing the contents of the
   CSAR.

    Note, that a CSAR may contain multiple Definitions files. One reason
    for this is completeness, e.g. a Service Template defined in one of
    the Definitions files could refer to Node Types defined in another
    Definitions file that might be included in the Definitions directory
    to avoid importing it from external locations. The Entry-Definitions
    name/value pair is a hint to allow optimized processing of the set
    of files in the Definitions directory.

For an example:

csar_vfw.zip

+-----------------------------------------------+
| TOSCA-Meta-File-Version: 1.0                  |
|                                               |
| CSAR-Version: 1.0                             |
|                                               |
| Created-By: zte                               |
|                                               |
| Entry-Definitions: Definitions/tosca_vfw.yaml |
+-----------------------------------------------+

1.3.5 CSAR Meta File Definition
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

Describing the content of the CSAR, including type(GSAR/SSAR/NSAR/NFAR),
provider, version.

+----------------+-----------+---------------------+
| Dirctory/Files | Qualifier | Description         |
+================+===========+=====================+
| type           | M         | GSAR/SSAR/NSAR/NFAR |
+----------------+-----------+---------------------+
| provider       | M         |                     |
+----------------+-----------+---------------------+
| version        | M         |                     |
+----------------+-----------+---------------------+

For an example:

+---------------+
| Type: NSAR    |
|               |
| Provider: ZTE |
|               |
| Version: v1.0 |
+---------------+

1.3.6 Checksum File Definition
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

File Name: checksum.lst

Content:

[File related file path]:[checksum(MD5)]

For an example:

/SoftwareImages/zte_vmb_qcow2.img:8a683566bcc7801226b3d8b0cf35fd97

/AppSoftwares/zte_nf_version.zip:7b8955fbb77654635b5c8a9be3aa854
