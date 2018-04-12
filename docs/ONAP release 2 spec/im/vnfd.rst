.. contents::
   :depth: 3
..

Class: VNFD/VNFDesc
===================

+---------------------+-------------+------------------+-----------------+------------------------+
| **Attribute  Name** | **Type**    | **Multiplicity** | **Description** | **Applied Stereotypes**|
+=====================+=============+==================+=================+========================+
| vnfdId              | Identifier  | 1                | Identifier      | support:               |
|                     |             |                  | of this         | MANDATORY              |
|                     |             |                  | VNFD            |                        |
|                     |             |                  | information     |                        |
|                     |             |                  | element.        |                        |
|                     |             |                  | This            |                        |
|                     |             |                  | attribute       |                        |
|                     |             |                  | shall be        |                        |
|                     |             |                  | globally        |                        |
|                     |             |                  | unique.         |                        |
|                     |             |                  |                 |                        |
|                     |             |                  | NOTE: The       |                        |
|                     |             |                  | VNFD            |                        |
|                     |             |                  | Identifier      |                        |
|                     |             |                  | shall be        |                        |
|                     |             |                  | used as the     |                        |
|                     |             |                  | unique          |                        |
|                     |             |                  | identifier      |                        |
|                     |             |                  | of the VNF      |                        |
|                     |             |                  | Package         |                        |
|                     |             |                  | that            |                        |
|                     |             |                  | contains        |                        |
|                     |             |                  | this VNFD.      |                        |
|                     |             |                  |                 |                        |
|                     |             |                  | Any             |                        |
|                     |             |                  | modificatio     |                        |
|                     |             |                  | n               |                        |
|                     |             |                  | of the          |                        |
|                     |             |                  | content of      |                        |
|                     |             |                  | the VNFD or     |                        |
|                     |             |                  | the VNF         |                        |
|                     |             |                  | Package         |                        |
|                     |             |                  | shall           |                        |
|                     |             |                  | result in a     |                        |
|                     |             |                  | new VNFD        |                        |
|                     |             |                  | Identifier.     |                        |
+---------------------+-------------+------------------+-----------------+------------------------+
| vnfProvider         | String      | 1                | Provider of     | support:               |
|                     |             |                  | the VNF and     | MANDATORY              |
|                     |             |                  | of the          |                        |
|                     |             |                  | VNFD.           |                        |
+---------------------+-------------+------------------+-----------------+------------------------+
| vnfProductN         | String      | 1                | Name to         | support:               |
| ame                 |             |                  | identify        | MANDATORY              |
|                     |             |                  | the VNF         |                        |
|                     |             |                  | Product.        |                        |
|                     |             |                  | Invariant       |                        |
|                     |             |                  | for the VNF     |                        |
|                     |             |                  | Product         |                        |
|                     |             |                  | lifetime.       |                        |
+---------------------+-------------+------------------+-----------------+------------------------+
| vnfSoftware         | String      | 1                | Software        | support:               |
| Version             |             |                  | version of      | MANDATORY              |
|                     |             |                  | the VNF.        |                        |
|                     |             |                  | This is         |                        |
|                     |             |                  | changed         |                        |
|                     |             |                  | when there      |                        |
|                     |             |                  | is any          |                        |
|                     |             |                  | change to       |                        |
|                     |             |                  | the             |                        |
|                     |             |                  | software        |                        |
|                     |             |                  | that is         |                        |
|                     |             |                  | included in     |                        |
|                     |             |                  | the VNF         |                        |
|                     |             |                  | Package.        |                        |
+---------------------+-------------+------------------+-----------------+------------------------+
| vnfdVersion         | String      | 1                | Identifies      | support:               |
|                     |             |                  | the version     | MANDATORY              |
|                     |             |                  | of the          |                        |
|                     |             |                  | VNFD.           |                        |
+---------------------+-------------+------------------+-----------------+------------------------+
| vnfProductI         | String      | 0..1             | Human           | support:               |
| nfoName             |             |                  | readable        | MANDATORY              |
|                     |             |                  | name for        |                        |
|                     |             |                  | the VNF         |                        |
|                     |             |                  | Product.        |                        |
|                     |             |                  | Can change      |                        |
|                     |             |                  | during the      |                        |
|                     |             |                  | VNF Product     |                        |
|                     |             |                  | lifetime.       |                        |
+---------------------+-------------+------------------+-----------------+------------------------+
| vnfProductI         | String      | 0..1             | Human           | support:               |
| nfoDescript         |             |                  | readable        | MANDATORY              |
| ion                 |             |                  | description     |                        |
|                     |             |                  | of the VNF      |                        |
|                     |             |                  | Product.        |                        |
|                     |             |                  | Can change      |                        |
|                     |             |                  | during the      |                        |
|                     |             |                  | VNF Product     |                        |
|                     |             |                  | lifetime.       |                        |
+---------------------+-------------+------------------+-----------------+------------------------+
| vnfmInfo            | String      | 0..N             | Identifies      | support:               |
|                     |             |                  | VNFM(s)         | MANDATORY              |
|                     |             |                  | compatible      |                        |
|                     |             |                  | with the        | valueRange:            |
|                     |             |                  | VNF             | use the                |
|                     |             |                  | described       | name of                |
|                     |             |                  | in this         | micro-servi            |
|                     |             |                  | version of      | ce                     |
|                     |             |                  | the VNFD.       | of the vnfm            |
|                     |             |                  |                 | drive. For             |
|                     |             |                  |                 | vendor                 |
|                     |             |                  |                 | specific               |
|                     |             |                  |                 | VNFM, the              |
|                     |             |                  |                 | value                  |
|                     |             |                  |                 | composes of            |
|                     |             |                  |                 | "vendorname            |
|                     |             |                  |                 | "                      |
|                     |             |                  |                 | and                    |
|                     |             |                  |                 | "vnfmdriver            |
|                     |             |                  |                 | ",                     |
|                     |             |                  |                 | e.g.                   |
|                     |             |                  |                 | "mycompanyv            |
|                     |             |                  |                 | nfmdriver";            |
|                     |             |                  |                 | for generic            |
|                     |             |                  |                 | VNFM, the              |
|                     |             |                  |                 | value is               |
|                     |             |                  |                 | "gvnfmdrive            |
|                     |             |                  |                 | r".                    |
+---------------------+-------------+------------------+-----------------+------------------------+
| localizatio         | String      | 0..N             | Information     | support:               |
| nLanguage           |             |                  | about           | MANDATORY              |
|                     |             |                  | localizatio     |                        |
|                     |             |                  | n               | valueRange:            |
|                     |             |                  | languages       | refer to               |
|                     |             |                  | of the VNF      | ISO936 \ `h            |
|                     |             |                  | (includes       | ttps://www.            |
|                     |             |                  | e.g.            | iso.org/iso            |
|                     |             |                  | strings in      | -639-langua            |
|                     |             |                  | the VNFD).      | ge-codes.ht            |
|                     |             |                  |                 | ml <https:/            |
|                     |             |                  | NOTE: This      | /www.iso.or            |
|                     |             |                  | allows to       | g/iso-639-l            |
|                     |             |                  | provide one     | anguage-cod            |
|                     |             |                  | or more         | es.html>`__            |
|                     |             |                  | localizatio     |                        |
|                     |             |                  | n               |                        |
|                     |             |                  | languages       |                        |
|                     |             |                  | to support      |                        |
|                     |             |                  | selecting a     |                        |
|                     |             |                  | specific        |                        |
|                     |             |                  | localizatio     |                        |
|                     |             |                  | n               |                        |
|                     |             |                  | language at     |                        |
|                     |             |                  | VNF             |                        |
|                     |             |                  | instantiati     |                        |
|                     |             |                  | on              |                        |
|                     |             |                  | time.           |                        |
+---------------------+-------------+------------------+-----------------+------------------------+
| defaultLoca         | String      | 0..1             | Default         | support:               |
| lizationLan         |             |                  | localizatio     | MANDATORY              |
| guage               |             |                  | n               |                        |
|                     |             |                  | language        | valueRange:            |
|                     |             |                  | that is         | refer to               |
|                     |             |                  | instantiate     | ISO936 \ `h            |
|                     |             |                  | d               | ttps://www.            |
|                     |             |                  | if no           | iso.org/iso            |
|                     |             |                  | information     | -639-langua            |
|                     |             |                  | about           | ge-codes.ht            |
|                     |             |                  | selected        | ml <https:/            |
|                     |             |                  | localizatio     | /www.iso.or            |
|                     |             |                  | n               | g/iso-639-l            |
|                     |             |                  | language is     | anguage-cod            |
|                     |             |                  | available.      | es.html>`__            |
|                     |             |                  |                 |                        |
|                     |             |                  |                 | condition:             |
|                     |             |                  |                 | Shall be               |
|                     |             |                  |                 | present if             |
|                     |             |                  |                 | "localizati            |
|                     |             |                  |                 | onLanguage"            |
|                     |             |                  |                 | is present             |
|                     |             |                  |                 | and shall              |
|                     |             |                  |                 | be absent              |
|                     |             |                  |                 | otherwise.             |
+---------------------+-------------+------------------+-----------------+------------------------+
| vdu                 | VDU/VDUDesc | 1..N             | Virtualisat     | support:               |
|                     |             |                  | ion             | MANDATORY              |
|                     |             |                  | Deployment      |                        |
|                     |             |                  | Unit.           |                        |
+---------------------+-------------+------------------+-----------------+------------------------+
| virtualComp         | VirtualComp | 1..N             | Defines         | support:               |
| uteDesc             | uteDesc     |                  | descriptors     | MANDATORY              |
|                     |             |                  | of virtual      |                        |
|                     |             |                  | compute         |                        |
|                     |             |                  | resources       |                        |
|                     |             |                  | to be used      |                        |
|                     |             |                  | by the VNF.     |                        |
+---------------------+-------------+------------------+-----------------+------------------------+
| virtualStor         | VirtualStor | 0..N             | Defines         | support:               |
| ageDesc             | ageDesc     |                  | descriptors     | MANDATORY              |
|                     |             |                  | of virtual      |                        |
|                     |             |                  | storage         |                        |
|                     |             |                  | resources       |                        |
|                     |             |                  | to be used      |                        |
|                     |             |                  | by the VNF.     |                        |
+---------------------+-------------+------------------+-----------------+------------------------+
| intVirtualL         | VirtualLink | 0..N             | Represents      | support:               |
| inkDesc             | Desc/VnfVir |                  | the type of     | MANDATORY              |
|                     | tualLinkDes |                  | network         |                        |
|                     | c           |                  | connectivit     |                        |
|                     |             |                  | y               |                        |
|                     |             |                  | mandated by     |                        |
|                     |             |                  | the VNF         |                        |
|                     |             |                  | provider        |                        |
|                     |             |                  | between two     |                        |
|                     |             |                  | or more CPs     |                        |
|                     |             |                  | which           |                        |
|                     |             |                  | includes at     |                        |
|                     |             |                  | least one       |                        |
|                     |             |                  | internal        |                        |
|                     |             |                  | CP.             |                        |
+---------------------+-------------+------------------+-----------------+------------------------+
| vnfReserved         | VduCpd      | 0..N             | Reserved IP     | support:               |
| Cpd                 |             |                  | Address for     | MANDATORY              |
|                     |             |                  | VNF which       |                        |
|                     |             |                  | is not          |                        |
|                     |             |                  | bounded to      |                        |
|                     |             |                  | any             |                        |
|                     |             |                  | specific        |                        |
|                     |             |                  | VNFC, but       |                        |
|                     |             |                  | assigned        |                        |
|                     |             |                  | manually        |                        |
|                     |             |                  | from            |                        |
|                     |             |                  | outside and     |                        |
|                     |             |                  | potentially     |                        |
|                     |             |                  | shared as a     |                        |
|                     |             |                  | floating IP     |                        |
|                     |             |                  | among           |                        |
|                     |             |                  | VNFCs.          |                        |
+---------------------+-------------+------------------+-----------------+------------------------+
| vnfExtCpd           | VnfExtCpd/V | 1..N             | Describes       | support:               |
|                     | NFExtCPDesc |                  | external        | MANDATORY              |
|                     |             |                  | interface(s     |                        |
|                     |             |                  | )               |                        |
|                     |             |                  | exposed by      |                        |
|                     |             |                  | this VNF        |                        |
|                     |             |                  | enabling        |                        |
|                     |             |                  | connection      |                        |
|                     |             |                  | with a VL.      |                        |
+---------------------+-------------+------------------+-----------------+------------------------+
| deploymentF         | VnfDf/VNFDe | 1..N             | Describes       | support:               |
| lavour              | ploymentFla |                  | specific        | MANDATORY              |
|                     | vor         |                  | DF(s) of a      |                        |
|                     |             |                  | VNF with        |                        |
|                     |             |                  | specific        |                        |
|                     |             |                  | requirement     |                        |
|                     |             |                  | s               |                        |
|                     |             |                  | for             |                        |
|                     |             |                  | capacity        |                        |
|                     |             |                  | and             |                        |
|                     |             |                  | performance     |                        |
|                     |             |                  | .               |                        |
+---------------------+-------------+------------------+-----------------+------------------------+
| configurabl         | VnfConfigur | 0..1             | Describes       | sup    port:           |
| eProperties         | ablePropert |                  | the             | MAN    DATORY          |
|                     | ies         |                  | configurabl     |                        |
|                     |             |                  | e               |                        |
|                     |             |                  | properties      |                        |
|                     |             |                  | of the VNF      |                        |
|                     |             |                  | (e.g.           |                        |
|                     |             |                  | related to      |                        |
|                     |             |                  | auto            |                        |
|                     |             |                  | scaling and     |                        |
|                     |             |                  | auto            |                        |
|                     |             |                  | healing).       |                        |
+---------------------+-------------+------------------+-----------------+------------------------+
| modifiableA         | VnfInfoModi | 0..1             | Describes       | sup    port:           |
| ttributes           | fiableAttri |                  | the             | MAN    DATORY          |
|                     | butes       |                  | modifiable      |                        |
|                     |             |                  | attributes      |                        |
|                     |             |                  | of the VNF.     |                        |
|                     |             |                  |                 |                        |
|                     |             |                  | Editor's        |                        |
|                     |             |                  | note: need      |                        |
|                     |             |                  | check the       |                        |
|                     |             |                  | usage of        |                        |
|                     |             |                  | this            |                        |
|                     |             |                  | attribute       |                        |
+---------------------+-------------+------------------+-----------------+------------------------+
| lifeCycleMa         | LifeCycleMa | 0..N             | Includes a      | sup    port:           |
| nagementScr         | nagementScr |                  | list of         | MAN    DATORY          |
| ipt                 | ipt/LifeCyc |                  | events and      |                        |
|                     | leManagemen |                  | correspondi     |                        |
|                     | tOperationD |                  | ng              |                        |
|                     | esc         |                  | management      |                        |
|                     |             |                  | scripts         |                        |
|                     |             |                  | performed       |                        |
|                     |             |                  | for the         |                        |
|                     |             |                  | VNF.            |                        |
+---------------------+-------------+------------------+-----------------+------------------------+
| elementGrou         | VnfdElement | 0..N             | Describes       | sup    port:           |
| p                   | Group       |                  | the             | MAN    DATORY          |
|                     |             |                  | associated      |                        |
|                     |             |                  | elements of     |                        |
|                     |             |                  | a VNFD for      |                        |
|                     |             |                  | a certain       |                        |
|                     |             |                  | purpose         |                        |
|                     |             |                  | during VNF      |                        |
|                     |             |                  | lifecycle       |                        |
|                     |             |                  | management.     |                        |
+---------------------+-------------+------------------+-----------------+------------------------+
| vnfIndicato         | VnfIndicato | 0..N             | Declares        | support:               |
| r                   | r           |                  | the VNF         | MANDATORY              |
|                     |             |                  | indicators      |                        |
|                     |             |                  | that are        |                        |
|                     |             |                  | supported       |                        |
|                     |             |                  | by this         |                        |
|                     |             |                  | VNF.            |                        |
+---------------------+-------------+------------------+-----------------+------------------------+
| logo                | String      | 0..1             | File path       | support:               |
|                     |             |                  | of the          | MANDATORY              |
|                     |             |                  | vendor          |                        |
|                     |             |                  | specified       |                        |
|                     |             |                  | logo.           |                        |
+---------------------+-------------+------------------+-----------------+------------------------+
| guide               | String      | 0..1             | UUID of the     | support:               |
|                     |             |                  | vendor          | MANDATORY              |
|                     |             |                  | guide/docum     |                        |
|                     |             |                  | entation        |                        |
|                     |             |                  | which is        |                        |
|                     |             |                  | attached to     |                        |
|                     |             |                  | VNF and can     |                        |
|                     |             |                  | be              |                        |
|                     |             |                  | downloaded      |                        |
|                     |             |                  | from the        |                        |
|                     |             |                  | model.          |                        |
+---------------------+-------------+------------------+-----------------+------------------------+
|                     |             |                  |                 |                        |
+---------------------+-------------+------------------+-----------------+------------------------+
