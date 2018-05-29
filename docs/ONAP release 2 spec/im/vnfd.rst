.. Copyright 2018 (China Mobile)
.. This file is licensed under the CREATIVE COMMONS ATTRIBUTION 4.0 INTERNATIONAL LICENSE
.. Full license text at https://creativecommons.org/licenses/by/4.0/legalcode

Class: Vnfd
===========

+-----------------------------+-----------------------------+------------------+---------------------+------------------------------------------------------+
| **Attribute  Name**         | **Type**                    | **Multiplicity** | **Description**     | **Applied Stereotypes**                              |
+=============================+=============================+==================+=====================+======================================================+
| vnfdId                      | Identifier                  | 1                | Identifier          | support:                                             |
|                             |                             |                  | of this             | MANDATORY                                            |
|                             |                             |                  | VNFD                |                                                      |
|                             |                             |                  | information         |                                                      |
|                             |                             |                  | element.            |                                                      |
|                             |                             |                  | This                |                                                      |
|                             |                             |                  | attribute           |                                                      |
|                             |                             |                  | shall be            |                                                      |
|                             |                             |                  | globally            |                                                      |
|                             |                             |                  | unique.             |                                                      |
|                             |                             |                  |                     |                                                      |
|                             |                             |                  | NOTE: The           |                                                      |
|                             |                             |                  | VNFD                |                                                      |
|                             |                             |                  | Identifier          |                                                      |
|                             |                             |                  | shall be            |                                                      |
|                             |                             |                  | used as the         |                                                      |
|                             |                             |                  | unique              |                                                      |
|                             |                             |                  | identifier          |                                                      |
|                             |                             |                  | of the VNF          |                                                      |
|                             |                             |                  | Package             |                                                      |
|                             |                             |                  | that                |                                                      |
|                             |                             |                  | contains            |                                                      |
|                             |                             |                  | this VNFD.          |                                                      |
|                             |                             |                  |                     |                                                      |
|                             |                             |                  | Any                 |                                                      |
|                             |                             |                  | modification        |                                                      |
|                             |                             |                  | of the              |                                                      |
|                             |                             |                  | content of          |                                                      |
|                             |                             |                  | the VNFD or         |                                                      |
|                             |                             |                  | the VNF             |                                                      |
|                             |                             |                  | Package             |                                                      |
|                             |                             |                  | shall               |                                                      |
|                             |                             |                  | result in a         |                                                      |
|                             |                             |                  | new VNFD            |                                                      |
|                             |                             |                  | Identifier.         |                                                      |
+-----------------------------+-----------------------------+------------------+---------------------+------------------------------------------------------+
| vnfProvider                 | String                      | 1                | Provider of         | support:                                             |
|                             |                             |                  | the VNF and         | MANDATORY                                            |
|                             |                             |                  | of the              |                                                      |
|                             |                             |                  | VNFD.               |                                                      |
+-----------------------------+-----------------------------+------------------+---------------------+------------------------------------------------------+
| vnfProductName              | String                      | 1                | Name to             | support:                                             |
|                             |                             |                  | identify            | MANDATORY                                            |
|                             |                             |                  | the VNF             |                                                      |
|                             |                             |                  | Product.            |                                                      |
|                             |                             |                  | Invariant           |                                                      |
|                             |                             |                  | for the VNF         |                                                      |
|                             |                             |                  | Product             |                                                      |
|                             |                             |                  | lifetime.           |                                                      |
+-----------------------------+-----------------------------+------------------+---------------------+------------------------------------------------------+
| vnfSoftwareVersion          | String                      | 1                | Software            | support:                                             |
|                             |                             |                  | version of          | MANDATORY                                            |
|                             |                             |                  | the VNF.            |                                                      |
|                             |                             |                  | This is             |                                                      |
|                             |                             |                  | changed             |                                                      |
|                             |                             |                  | when there          |                                                      |
|                             |                             |                  | is any              |                                                      |
|                             |                             |                  | change to           |                                                      |
|                             |                             |                  | the                 |                                                      |
|                             |                             |                  | software            |                                                      |
|                             |                             |                  | that is             |                                                      |
|                             |                             |                  | included in         |                                                      |
|                             |                             |                  | the VNF             |                                                      |
|                             |                             |                  | Package.            |                                                      |
+-----------------------------+-----------------------------+------------------+---------------------+------------------------------------------------------+
| vnfdVersion                 | String                      | 1                | Identifies          | support:                                             |
|                             |                             |                  | the version         | MANDATORY                                            |
|                             |                             |                  | of the              |                                                      |
|                             |                             |                  | VNFD.               |                                                      |
+-----------------------------+-----------------------------+------------------+---------------------+------------------------------------------------------+
| vnfProductInfoName          | String                      | 0..1             | Human               | support:                                             |
|                             |                             |                  | readable            | MANDATORY                                            |
|                             |                             |                  | name for            |                                                      |
|                             |                             |                  | the VNF             |                                                      |
|                             |                             |                  | Product.            |                                                      |
|                             |                             |                  | Can change          |                                                      |
|                             |                             |                  | during the          |                                                      |
|                             |                             |                  | VNF Product         |                                                      |
|                             |                             |                  | lifetime.           |                                                      |
+-----------------------------+-----------------------------+------------------+---------------------+------------------------------------------------------+
| vnfProductInfoDescription   | String                      | 0..1             | Human               | support:                                             |
|                             |                             |                  | readable            | MANDATORY                                            |
|                             |                             |                  | description         |                                                      |
|                             |                             |                  | of the VNF          |                                                      |
|                             |                             |                  | Product.            |                                                      |
|                             |                             |                  | Can change          |                                                      |
|                             |                             |                  | during the          |                                                      |
|                             |                             |                  | VNF Product         |                                                      |
|                             |                             |                  | lifetime.           |                                                      |
+-----------------------------+-----------------------------+------------------+---------------------+------------------------------------------------------+
| vnfmInfo                    | String                      | 0..N             | Identifies          | support:                                             |
|                             |                             |                  | VNFM(s)             | MANDATORY                                            |
|                             |                             |                  | compatible          |                                                      |
|                             |                             |                  | with the            | valueRange:                                          |
|                             |                             |                  | VNF                 | use the                                              |
|                             |                             |                  | described           | name of                                              |
|                             |                             |                  | in this             | micro-service                                        |
|                             |                             |                  | version of          | of the vnfm                                          |
|                             |                             |                  | the VNFD.           | drive. For                                           |
|                             |                             |                  |                     | vendor                                               |
|                             |                             |                  |                     | specific                                             |
|                             |                             |                  |                     | VNFM, the                                            |
|                             |                             |                  |                     | value                                                |
|                             |                             |                  |                     | composes of                                          |
|                             |                             |                  |                     | "vendorname"                                         |
|                             |                             |                  |                     | and                                                  |
|                             |                             |                  |                     | "vnfmdriver",                                        |
|                             |                             |                  |                     | e.g.                                                 |
|                             |                             |                  |                     | "mycompanyvnfmdriver";                               |
|                             |                             |                  |                     | for generic                                          |
|                             |                             |                  |                     | VNFM, the                                            |
|                             |                             |                  |                     | value is                                             |
|                             |                             |                  |                     | "gvnfmdriver".                                       |
+-----------------------------+-----------------------------+------------------+---------------------+------------------------------------------------------+
| localizationLanguage        | String                      | 0..N             | Information         | support:                                             |
|                             |                             |                  | about               | MANDATORY                                            |
|                             |                             |                  | localization        |                                                      |
|                             |                             |                  | languages           | valueRange:                                          |
|                             |                             |                  |                     | refer to                                             |
|                             |                             |                  | of the VNF          | ISO936 \                                             |
|                             |                             |                  | (includes           | `https://www.iso.org/iso-639-language-codes.html     |
|                             |                             |                  | e.g.                | <https://www.iso.org/iso-639-language-codes.html>`__ |
|                             |                             |                  | strings in          |                                                      |
|                             |                             |                  | the VNFD).          |                                                      |
|                             |                             |                  |                     |                                                      |
|                             |                             |                  | NOTE: This          |                                                      |
|                             |                             |                  | allows to           |                                                      |
|                             |                             |                  | provide one         |                                                      |
|                             |                             |                  | or more             |                                                      |
|                             |                             |                  | localizatio         |                                                      |
|                             |                             |                  | n                   |                                                      |
|                             |                             |                  | languages           |                                                      |
|                             |                             |                  | to support          |                                                      |
|                             |                             |                  | selecting a         |                                                      |
|                             |                             |                  | specific            |                                                      |
|                             |                             |                  | localizatio         |                                                      |
|                             |                             |                  | n                   |                                                      |
|                             |                             |                  | language at         |                                                      |
|                             |                             |                  | VNF                 |                                                      |
|                             |                             |                  | instantiati         |                                                      |
|                             |                             |                  | on                  |                                                      |
|                             |                             |                  | time.               |                                                      |
+-----------------------------+-----------------------------+------------------+---------------------+------------------------------------------------------+
| defaultLocalizationLanguage | String                      | 0..1             | Default             | support:                                             |
|                             |                             |                  | localization        | MANDATORY                                            |
|                             |                             |                  | language            |                                                      |
|                             |                             |                  | that is             | valueRange:                                          |
|                             |                             |                  | instantiated        | refer to                                             |
|                             |                             |                  | if no               | ISO936 \                                             |
|                             |                             |                  | information         | `https://www.iso.org/iso-639-language-codes.html     |
|                             |                             |                  | about               | <https://www.iso.org/iso-639-language-codes.html>`__ |
|                             |                             |                  | selected            |                                                      |
|                             |                             |                  | localization        | condition:                                           |
|                             |                             |                  | language is         | Shall be                                             |
|                             |                             |                  | available.          | present if                                           |
|                             |                             |                  |                     | "localizationLanguage"                               |
|                             |                             |                  |                     | is present                                           |
|                             |                             |                  |                     | and shall                                            |
|                             |                             |                  |                     | be absent                                            |
|                             |                             |                  |                     | otherwise.                                           |
+-----------------------------+-----------------------------+------------------+---------------------+------------------------------------------------------+
| vdu                         | Vdu                         | 1..N             | Virtualisation      | support:                                             |
|                             |                             |                  | Deployment          | MANDATORY                                            |
|                             |                             |                  | Unit.               |                                                      |
+-----------------------------+-----------------------------+------------------+---------------------+------------------------------------------------------+
| virtualComputeDesc          | VirtualComputeDesc          | 1..N             | Defines             | support:                                             |
|                             |                             |                  | descriptors         | MANDATORY                                            |
|                             |                             |                  | of virtual          |                                                      |
|                             |                             |                  | compute             |                                                      |
|                             |                             |                  | resources           |                                                      |
|                             |                             |                  | to be used          |                                                      |
|                             |                             |                  | by the VNF.         |                                                      |
+-----------------------------+-----------------------------+------------------+---------------------+------------------------------------------------------+
| virtualStorageDesc          | VirtualStorageDesc          | 0..N             | Defines             | support:                                             |
|                             |                             |                  | descriptors         | MANDATORY                                            |
|                             |                             |                  | of virtual          |                                                      |
|                             |                             |                  | storage             |                                                      |
|                             |                             |                  | resources           |                                                      |
|                             |                             |                  | to be used          |                                                      |
|                             |                             |                  | by the VNF.         |                                                      |
+-----------------------------+-----------------------------+------------------+---------------------+------------------------------------------------------+
| intVirtualLinkDesc          | VirtualLinkDesc             | 0..N             | Represents          | support:                                             |
|                             |                             |                  | the type of         | MANDATORY                                            |
|                             |                             |                  | network             |                                                      |
|                             |                             |                  | connectivity        |                                                      |
|                             |                             |                  | mandated by         |                                                      |
|                             |                             |                  | the VNF             |                                                      |
|                             |                             |                  | provider            |                                                      |
|                             |                             |                  | between two         |                                                      |
|                             |                             |                  | or more CPs         |                                                      |
|                             |                             |                  | which               |                                                      |
|                             |                             |                  | includes at         |                                                      |
|                             |                             |                  | least one           |                                                      |
|                             |                             |                  | internal            |                                                      |
|                             |                             |                  | CP.                 |                                                      |
+-----------------------------+-----------------------------+------------------+---------------------+------------------------------------------------------+
| vnfReservedCpd              | VduCpd                      | 0..N             | Reserved IP         | support:                                             |
|                             |                             |                  | Address for         | MANDATORY                                            |
|                             |                             |                  | VNF which           |                                                      |
|                             |                             |                  | is not              |                                                      |
|                             |                             |                  | bounded to          |                                                      |
|                             |                             |                  | any                 |                                                      |
|                             |                             |                  | specific            |                                                      |
|                             |                             |                  | VNFC, but           |                                                      |
|                             |                             |                  | assigned            |                                                      |
|                             |                             |                  | manually            |                                                      |
|                             |                             |                  | from                |                                                      |
|                             |                             |                  | outside and         |                                                      |
|                             |                             |                  | potentially         |                                                      |
|                             |                             |                  | shared as a         |                                                      |
|                             |                             |                  | floating IP         |                                                      |
|                             |                             |                  | among               |                                                      |
|                             |                             |                  | VNFCs.              |                                                      |
+-----------------------------+-----------------------------+------------------+---------------------+------------------------------------------------------+
| vnfExtCpd                   | VnfExtCpd                   | 1..N             | Describes           | support:                                             |
|                             |                             |                  | external            | MANDATORY                                            |
|                             |                             |                  | interface(s)        |                                                      |
|                             |                             |                  | exposed by          |                                                      |
|                             |                             |                  | this VNF            |                                                      |
|                             |                             |                  | enabling            |                                                      |
|                             |                             |                  | connection          |                                                      |
|                             |                             |                  | with a VL.          |                                                      |
+-----------------------------+-----------------------------+------------------+---------------------+------------------------------------------------------+
| deploymentFlavour           | VnfDf                       | 1..N             | Describes           | support:                                             |
|                             |                             |                  | specific            | MANDATORY                                            |
|                             |                             |                  | DF(s) of a          |                                                      |
|                             |                             |                  | VNF with            |                                                      |
|                             |                             |                  | specific            |                                                      |
|                             |                             |                  | requirements        |                                                      |
|                             |                             |                  | for                 |                                                      |
|                             |                             |                  | capacity            |                                                      |
|                             |                             |                  | and                 |                                                      |
|                             |                             |                  | performance.        |                                                      |
+-----------------------------+-----------------------------+------------------+---------------------+------------------------------------------------------+
| configurableProperties      | VnfConfigurableProperties   | 0..1             | Describes           | support:                                             |
|                             |                             |                  | the                 | MANDATORY                                            |
|                             |                             |                  | configurable        |                                                      |
|                             |                             |                  | properties          |                                                      |
|                             |                             |                  | of the VNF          |                                                      |
|                             |                             |                  | (e.g.               |                                                      |
|                             |                             |                  | related to          |                                                      |
|                             |                             |                  | auto                |                                                      |
|                             |                             |                  | scaling and         |                                                      |
|                             |                             |                  | auto                |                                                      |
|                             |                             |                  | healing).           |                                                      |
+-----------------------------+-----------------------------+------------------+---------------------+------------------------------------------------------+
| modifiableAttributes        | VnfInfoModifiableAttributes | 0..1             | Describes           | support:                                             |
|                             |                             |                  | the                 | MANDATORY                                            |
|                             |                             |                  | modifiable          |                                                      |
|                             |                             |                  | attributes          |                                                      |
|                             |                             |                  | of the VNF.         |                                                      |
|                             |                             |                  |                     |                                                      |
+-----------------------------+-----------------------------+------------------+---------------------+------------------------------------------------------+
| lifeCycleManagementScript   | LifeCycleManagementScript   | 0..N             | Includes a          | support:                                             |
|                             |                             |                  | list of             | MANDATORY                                            |
|                             |                             |                  | events and          |                                                      |
|                             |                             |                  | corresponding       |                                                      |
|                             |                             |                  | management          |                                                      |
|                             |                             |                  | scripts             |                                                      |
|                             |                             |                  | performed           |                                                      |
|                             |                             |                  | for the             |                                                      |
|                             |                             |                  | VNF.                |                                                      |
+-----------------------------+-----------------------------+------------------+---------------------+------------------------------------------------------+
| elementGroup                | VnfdElementGroup            | 0..N             | Describes           | support:                                             |
|                             |                             |                  | the                 | MANDATORY                                            |
|                             |                             |                  | associated          |                                                      |
|                             |                             |                  | elements of         |                                                      |
|                             |                             |                  | a VNFD for          |                                                      |
|                             |                             |                  | a certain           |                                                      |
|                             |                             |                  | purpose             |                                                      |
|                             |                             |                  | during VNF          |                                                      |
|                             |                             |                  | lifecycle           |                                                      |
|                             |                             |                  | management.         |                                                      |
+-----------------------------+-----------------------------+------------------+---------------------+------------------------------------------------------+
| vnfIndicator                | VnfIndicator                | 0..N             | Declares            | support:                                             |
|                             |                             |                  | the VNF             | MANDATORY                                            |
|                             |                             |                  | indicators          |                                                      |
|                             |                             |                  | that are            |                                                      |
|                             |                             |                  | supported           |                                                      |
|                             |                             |                  | by this             |                                                      |
|                             |                             |                  | VNF.                |                                                      |
+-----------------------------+-----------------------------+------------------+---------------------+------------------------------------------------------+
| logo                        | String                      | 0..1             | File path           | support:                                             |
|                             |                             |                  | of the              | MANDATORY                                            |
|                             |                             |                  | vendor              |                                                      |
|                             |                             |                  | specified           |                                                      |
|                             |                             |                  | logo.               |                                                      |
+-----------------------------+-----------------------------+------------------+---------------------+------------------------------------------------------+
| guide                       | String                      | 0..1             | UUID of the         | support:                                             |
|                             |                             |                  | vendor              | MANDATORY                                            |
|                             |                             |                  | guide/documentation |                                                      |
|                             |                             |                  | which is            |                                                      |
|                             |                             |                  | attached to         |                                                      |
|                             |                             |                  | VNF and can         |                                                      |
|                             |                             |                  | be                  |                                                      |
|                             |                             |                  | downloaded          |                                                      |
|                             |                             |                  | from the            |                                                      |
|                             |                             |                  | model.              |                                                      |
+-----------------------------+-----------------------------+------------------+---------------------+------------------------------------------------------+
