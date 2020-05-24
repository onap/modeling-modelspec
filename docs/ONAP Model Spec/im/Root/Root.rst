.. Copyright 2019
.. This file is licensed under the CREATIVE COMMONS ATTRIBUTION 4.0 INTERNATIONAL LICENSE
.. Full license text at https://creativecommons.org/licenses/by/4.0/legalcode

Root Model
==========

.. contents::
   :depth: 3
..

Overview
--------

**Qualified Name:** Common::Root

**Description:**

A set of common business entities that collectively serve as the foundation of the ONAP Information Model. This set of root classess enable the entities in different domains of the Information Model to be associated with each other, providing greater overall coherence.

Class Definition
----------------

DesignEntity class
^^^^^^^^^^^^^^^^^^

**Qualified Name:** Common::Root::RootObjectClasses::DesignEntity

**Description:**

A template which describes an OperationalEntity in terms of deployment and operational behavior requirements.

This class is abstract.

**Parent class:** Entity

**Applied Stereotypes:**

-  OpenModelClass

-  support: MANDATORY

-  Preliminary

**Table** **Attributes for class DesignEntity**

================== ========== ========= ====================================================================================================================================================================================================================================================================================================================================================================== =====================
**Attribute Name** **Type**   **Mult.** **Description**                                                                                                                                                                                                                                                                                                                                                        **Stereotypes**
================== ========== ========= ====================================================================================================================================================================================================================================================================================================================================================================== =====================
validFor           TimePeriod 1         The period during which the design entity is valid.                                                                                                                                                                                                                                                                                                                    OpenModelAttribute
                                                                                                                                                                                                                                                                                                                                                                                                              
                                                                                                                                                                                                                                                                                                                                                                                                               -  partOfObjectKey: 0
                                                                                                                                                                                                                                                                                                                                                                                                              
                                                                                                                                                                                                                                                                                                                                                                                                               -  uniqueSet:
                                                                                                                                                                                                                                                                                                                                                                                                              
                                                                                                                                                                                                                                                                                                                                                                                                               -  isInvariant: false
                                                                                                                                                                                                                                                                                                                                                                                                              
                                                                                                                                                                                                                                                                                                                                                                                                               -  unsigned: false
                                                                                                                                                                                                                                                                                                                                                                                                              
                                                                                                                                                                                                                                                                                                                                                                                                               -  counter: NA
                                                                                                                                                                                                                                                                                                                                                                                                              
                                                                                                                                                                                                                                                                                                                                                                                                               -  support: MANDATORY
                                                                                                                                                                                                                                                                                                                                                                                                              
                                                                                                                                                                                                                                                                                                                                                                                                               Preliminary
status             String     1         The condition of the specification, such s active, inactive, or planned.                                                                                                                                                                                                                                                                                               OpenModelAttribute
                                                                                                                                                                                                                                                                                                                                                                                                              
                                                                                                                                                                                                                                                                                                                                                                                                               -  partOfObjectKey: 0
                                                                                                                                                                                                                                                                                                                                                                                                              
                                                                                                                                                                                                                                                                                                                                                                                                               -  uniqueSet:
                                                                                                                                                                                                                                                                                                                                                                                                              
                                                                                                                                                                                                                                                                                                                                                                                                               -  isInvariant: false
                                                                                                                                                                                                                                                                                                                                                                                                              
                                                                                                                                                                                                                                                                                                                                                                                                               -  unsigned: false
                                                                                                                                                                                                                                                                                                                                                                                                              
                                                                                                                                                                                                                                                                                                                                                                                                               -  counter: NA
                                                                                                                                                                                                                                                                                                                                                                                                              
                                                                                                                                                                                                                                                                                                                                                                                                               -  support: MANDATORY
                                                                                                                                                                                                                                                                                                                                                                                                              
                                                                                                                                                                                                                                                                                                                                                                                                               Preliminary
name               String     1         Represents a user-friendly identifier of an object. It is a (possibly ambiguous) name by which the object is commonly known in some limited scope (such as an organization) and conforms to the naming conventions of the country or culture with which it is associated. It is NOT used as a naming attribute (i.e., to uniquely identify an instance of the object). OpenModelAttribute
                                                                                                                                                                                                                                                                                                                                                                                                              
                                                                                                                                                                                                                                                                                                                                                                                                               -  partOfObjectKey: 0
                                                                                                                                                                                                                                                                                                                                                                                                              
                                                                                                                                                                                                                                                                                                                                                                                                               -  uniqueSet:
                                                                                                                                                                                                                                                                                                                                                                                                              
                                                                                                                                                                                                                                                                                                                                                                                                               -  isInvariant: false
                                                                                                                                                                                                                                                                                                                                                                                                              
                                                                                                                                                                                                                                                                                                                                                                                                               -  unsigned: false
                                                                                                                                                                                                                                                                                                                                                                                                              
                                                                                                                                                                                                                                                                                                                                                                                                               -  counter: NA
                                                                                                                                                                                                                                                                                                                                                                                                              
                                                                                                                                                                                                                                                                                                                                                                                                               -  support: MANDATORY
                                                                                                                                                                                                                                                                                                                                                                                                              
                                                                                                                                                                                                                                                                                                                                                                                                               Preliminary
description        String     1         Defines a textual free-form description of the object.                                                                                                                                                                                                                                                                                                                 OpenModelAttribute
                                                                                                                                                                                                                                                                                                                                                                                                              
                                                                                                                                                                                                                                                                                                                                                                                                               -  partOfObjectKey: 0
                                                                                                                                                                                                                                                                                                                                                                                                              
                                                                                                                                                                                                                                                                                                                                                                                                               -  uniqueSet:
                                                                                                                                                                                                                                                                                                                                                                                                              
                                                                                                                                                                                                                                                                                                                                                                                                               -  isInvariant: false
                                                                                                                                                                                                                                                                                                                                                                                                              
                                                                                                                                                                                                                                                                                                                                                                                                               -  unsigned: false
                                                                                                                                                                                                                                                                                                                                                                                                              
                                                                                                                                                                                                                                                                                                                                                                                                               -  counter: NA
                                                                                                                                                                                                                                                                                                                                                                                                              
                                                                                                                                                                                                                                                                                                                                                                                                               -  support: MANDATORY
                                                                                                                                                                                                                                                                                                                                                                                                              
                                                                                                                                                                                                                                                                                                                                                                                                               Preliminary
id                 Identifier 1         Unambiguously distinguishes different object instances. It is the naming attribute of the object.                                                                                                                                                                                                                                                                      OpenModelAttribute
                                                                                                                                                                                                                                                                                                                                                                                                              
                                        Identifier of this information element. This attribute shall be globally unique.                                                                                                                                                                                                                                                                                       -  partOfObjectKey: 0
                                                                                                                                                                                                                                                                                                                                                                                                              
                                                                                                                                                                                                                                                                                                                                                                                                               -  uniqueSet:
                                                                                                                                                                                                                                                                                                                                                                                                              
                                                                                                                                                                                                                                                                                                                                                                                                               -  isInvariant: false
                                                                                                                                                                                                                                                                                                                                                                                                              
                                                                                                                                                                                                                                                                                                                                                                                                               -  unsigned: false
                                                                                                                                                                                                                                                                                                                                                                                                              
                                                                                                                                                                                                                                                                                                                                                                                                               -  counter: NA
                                                                                                                                                                                                                                                                                                                                                                                                              
                                                                                                                                                                                                                                                                                                                                                                                                               -  support: MANDATORY
                                                                                                                                                                                                                                                                                                                                                                                                              
                                                                                                                                                                                                                                                                                                                                                                                                               Preliminary
================== ========== ========= ====================================================================================================================================================================================================================================================================================================================================================================== =====================

Domain class
^^^^^^^^^^^^

**Qualified Name:** Common::Root::RootObjectClasses::Domain

**Description:**

Defines a collection of entities that share a common purpose. In addition, each constituent Entity in an Domain is both uniquely addressable and uniquely identifiable within that Domain

**Parent class:** RootEntity

**Applied Stereotypes:**

-  Experimental

-  OpenModelClass

-  support: MANDATORY

Entity class
^^^^^^^^^^^^

**Qualified Name:** Common::Root::RootObjectClasses::Entity

**Description:**

This is an abstract class that extends the RootEntity class and represents characteristics and behaviors of concepts that pertain to the NFV managed environment.

This class is abstract.

**Parent class:** RootEntity

**Applied Stereotypes:**

-  OpenModelClass

-  support: MANDATORY

-  Preliminary

ManagedEntity class
^^^^^^^^^^^^^^^^^^^

**Qualified Name:** Common::Root::RootObjectClasses::ManagedEntity

**Description:**

A ManagedEntity is used to specify that an Entity is manageable by electronic means.

**Applied Stereotypes:**

-  Experimental

-  OpenModelClass

-  support: MANDATORY

**Table** **Attributes for class ManagedEntity**

========================= ======== ========= ================================================================================================================= =====================
**Attribute Name**        **Type** **Mult.** **Description**                                                                                                   **Stereotypes**
========================= ======== ========= ================================================================================================================= =====================
managementMethodCurrent   Integer  1         This is an enumerated integer that defines the particular type of management method that is currently being used. OpenModelAttribute
                                             Permitted Values:                                                                                                
                                             0: Unknown                                                                                                        -  partOfObjectKey: 0
                                             1: None                                                                                                          
                                             2: CLI                                                                                                            -  uniqueSet:
                                             3: SNMP                                                                                                          
                                             4: TL1                                                                                                            -  isInvariant: false
                                             5: CMIP                                                                                                          
                                             6: Proprietary                                                                                                    -  unsigned: false
                                                                                                                                                              
                                                                                                                                                               -  counter: NA
                                                                                                                                                              
                                                                                                                                                               -  support: MANDATORY
managementMethodSupported Integer  1..\*     This is an array of integers that define the different management methods that are supported by this object.      OpenModelAttribute
                                             Permitted Values:                                                                                                
                                             0: Unknown                                                                                                        -  partOfObjectKey: 0
                                             1: None                                                                                                          
                                             2: CLI                                                                                                            -  uniqueSet:
                                             3: SNMP                                                                                                          
                                             4: TL1                                                                                                            -  isInvariant: false
                                             5: CMIP                                                                                                          
                                             6: Proprietary                                                                                                    -  unsigned: false
                                                                                                                                                              
                                                                                                                                                               -  counter: NA
                                                                                                                                                              
                                                                                                                                                               -  support: MANDATORY
========================= ======== ========= ================================================================================================================= =====================

OperationalEntity class
^^^^^^^^^^^^^^^^^^^^^^^

**Qualified Name:** Common::Root::RootObjectClasses::OperationalEntity

**Description:**

An OperationalEntity is a deployment in a NFV environment of a DesignEntity.

This class is abstract.

**Parent class:** Entity

**Applied Stereotypes:**

-  OpenModelClass

-  support: MANDATORY

-  Preliminary

RootEntity class
^^^^^^^^^^^^^^^^

**Qualified Name:** Common::Root::RootObjectClasses::RootEntity

**Description:**

This is the top of the ONAP class hierarchy. The purpose of the RootEntity is to define a set of attributes that are common to all entities that derive from it. These properties enable us to name, describe, and identify all objects in the environment.

This class is abstract.

**Applied Stereotypes:**

-  OpenModelClass

-  support: MANDATORY

-  Preliminary

**Table** **Attributes for class RootEntity**

================== ========== ========= ====================================================================================================================================================================================================================================================================================================================================================================== =====================
**Attribute Name** **Type**   **Mult.** **Description**                                                                                                                                                                                                                                                                                                                                                        **Stereotypes**
================== ========== ========= ====================================================================================================================================================================================================================================================================================================================================================================== =====================
name               String     0..1      Represents a user-friendly identifier of an object. It is a (possibly ambiguous) name by which the object is commonly known in some limited scope (such as an organization) and conforms to the naming conventions of the country or culture with which it is associated. It is NOT used as a naming attribute (i.e., to uniquely identify an instance of the object). OpenModelAttribute
                                                                                                                                                                                                                                                                                                                                                                                                              
                                                                                                                                                                                                                                                                                                                                                                                                               -  partOfObjectKey: 0
                                                                                                                                                                                                                                                                                                                                                                                                              
                                                                                                                                                                                                                                                                                                                                                                                                               -  uniqueSet:
                                                                                                                                                                                                                                                                                                                                                                                                              
                                                                                                                                                                                                                                                                                                                                                                                                               -  isInvariant: false
                                                                                                                                                                                                                                                                                                                                                                                                              
                                                                                                                                                                                                                                                                                                                                                                                                               -  unsigned: false
                                                                                                                                                                                                                                                                                                                                                                                                              
                                                                                                                                                                                                                                                                                                                                                                                                               -  counter: NA
                                                                                                                                                                                                                                                                                                                                                                                                              
                                                                                                                                                                                                                                                                                                                                                                                                               -  support: MANDATORY
                                                                                                                                                                                                                                                                                                                                                                                                              
                                                                                                                                                                                                                                                                                                                                                                                                               Preliminary
description        String     0..1      Defines a textual free-form description of the object.                                                                                                                                                                                                                                                                                                                 OpenModelAttribute
                                                                                                                                                                                                                                                                                                                                                                                                              
                                                                                                                                                                                                                                                                                                                                                                                                               -  partOfObjectKey: 0
                                                                                                                                                                                                                                                                                                                                                                                                              
                                                                                                                                                                                                                                                                                                                                                                                                               -  uniqueSet:
                                                                                                                                                                                                                                                                                                                                                                                                              
                                                                                                                                                                                                                                                                                                                                                                                                               -  isInvariant: false
                                                                                                                                                                                                                                                                                                                                                                                                              
                                                                                                                                                                                                                                                                                                                                                                                                               -  unsigned: false
                                                                                                                                                                                                                                                                                                                                                                                                              
                                                                                                                                                                                                                                                                                                                                                                                                               -  counter: NA
                                                                                                                                                                                                                                                                                                                                                                                                              
                                                                                                                                                                                                                                                                                                                                                                                                               -  support: MANDATORY
                                                                                                                                                                                                                                                                                                                                                                                                              
                                                                                                                                                                                                                                                                                                                                                                                                               Preliminary
id                 Identifier 1         Unambiguously distinguishes different object instances. It is the naming attribute of the object.                                                                                                                                                                                                                                                                      OpenModelAttribute
                                                                                                                                                                                                                                                                                                                                                                                                              
                                        Identifier of this information element. This attribute shall be globally unique.                                                                                                                                                                                                                                                                                       -  partOfObjectKey: 0
                                                                                                                                                                                                                                                                                                                                                                                                              
                                                                                                                                                                                                                                                                                                                                                                                                               -  uniqueSet:
                                                                                                                                                                                                                                                                                                                                                                                                              
                                                                                                                                                                                                                                                                                                                                                                                                               -  isInvariant: false
                                                                                                                                                                                                                                                                                                                                                                                                              
                                                                                                                                                                                                                                                                                                                                                                                                               -  unsigned: false
                                                                                                                                                                                                                                                                                                                                                                                                              
                                                                                                                                                                                                                                                                                                                                                                                                               -  counter: NA
                                                                                                                                                                                                                                                                                                                                                                                                              
                                                                                                                                                                                                                                                                                                                                                                                                               -  support: MANDATORY
                                                                                                                                                                                                                                                                                                                                                                                                              
                                                                                                                                                                                                                                                                                                                                                                                                               Preliminary
================== ========== ========= ====================================================================================================================================================================================================================================================================================================================================================================== =====================

Enumeration definition
----------------------

CompositeOperator enumeration
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

**Qualified Name:** Common::Root::RootTypeDefinitons::CompositeOperator

**Description:**

The operator being applied to to some group of selectoin critiera.

**Applied Stereotypes:**

-  Preliminary

**Contains Enumeration Literals:**

-  AND

-  OR

-  XOR

Operator enumeration
^^^^^^^^^^^^^^^^^^^^

**Qualified Name:** Common::Root::RootTypeDefinitons::Operator

**Description:**

The operator being applied to some atomic selection critera.

**Applied Stereotypes:**

-  Preliminary

**Contains Enumeration Literals:**

-  MORETHAN

-  LESSTHAN

-  EQUAL

Priority enumeration
^^^^^^^^^^^^^^^^^^^^

**Qualified Name:** Common::TypeDefinitions::Priority

**Description:**

priority - processing priority.

**Applied Stereotypes:**

-  Preliminary

**Contains Enumeration Literals:**

-  HIGH

-  MEDIUM

-  NORMAL

-  LOW

RuleScope enumeration
^^^^^^^^^^^^^^^^^^^^^

**Qualified Name:** Common::TypeDefinitions::RuleScope

**Description:**

Defines the scope of the rule.

**Applied Stereotypes:**

-  Preliminary

**Contains Enumeration Literals:**

-  NFVI_POP

-  ZONE

-  ZONE_GROUP

-  NFVI_NODE

RuleType enumeration
^^^^^^^^^^^^^^^^^^^^

**Qualified Name:** Common::TypeDefinitions::RuleType

**Description:**

Specifies the type of rule.

**Applied Stereotypes:**

-  Preliminary

**Contains Enumeration Literals:**

-  AFFINITY

-  ANTI_AFFINITY

Datatype definition
-------------------

ConfigurableProperties datatype
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

**Qualified Name:** Common::Root::RootTypeDefinitons:: ConfigurableProperties

**Description:**

Dynamic, configurable properites of some entity.

**Applied Stereotypes:**

-  Experimental

**Table** **Attributes for Data Type ConfigurableProperties**

================== ============ ========= ==================================================== ==================================
**Attribute Name** **Type**     **Mult.** **Description**                                      **Stereotypes**
================== ============ ========= ==================================================== ==================================
properties         KeyValuePair 0..\*     The specific configurable properties of some entity. Experimental
                                                                                              
                                                                                               OpenModelAttribute
                                                                                              
                                                                                               -  isInvariant: false
                                                                                              
                                                                                               -  valueRange: no range constraint
                                                                                              
                                                                                               -  support: MANDATORY
================== ============ ========= ==================================================== ==================================

DateTime primitive type
^^^^^^^^^^^^^^^^^^^^^^^

**Qualified Name:** Common::TypeDefinitions::DateTime

**Description:**

DateTime - RFC 2822 standard date/time format.

RFC 2822 format

day-of-week, dd MM yyyy HH':'mm':'ss 'GMT'

e.g. Tue, 21 Jun 2016 14:05:20 GMT

File primitive type
^^^^^^^^^^^^^^^^^^^

**Qualified Name:** Common::TypeDefinitions::File

**Description:**

A primitive Type

**Applied Stereotypes:**

-  Experimental

Identifier datatype
^^^^^^^^^^^^^^^^^^^

**Qualified Name:** Common::TypeDefinitions::Identifier

**Applied Stereotypes:**

-  Preliminary

Key datatype
^^^^^^^^^^^^

**Qualified Name:** Common::TypeDefinitions::Key

**Description:**

key - the key datatype is a tuple which provides the name of a key along with its value and relative order.

**Applied Stereotypes:**

-  Preliminary

**Table** **Attributes for Data Type Key**

================== ======== ========= ============================================================================== ==================================
**Attribute Name** **Type** **Mult.** **Description**                                                                **Stereotypes**
================== ======== ========= ============================================================================== ==================================
keyName            String   1         keyName - Name of the key.                                                     OpenModelAttribute
                                                                                                                    
                                                                                                                     -  isInvariant: false
                                                                                                                    
                                                                                                                     -  valueRange: no range constraint
                                                                                                                    
                                                                                                                     -  support: MANDATORY
keyOrder           Integer  0..1      keyOrder - Relative sequence or order of the key (with respect to other keys). OpenModelAttribute
                                                                                                                    
                                                                                                                     -  isInvariant: false
                                                                                                                    
                                                                                                                     -  valueRange: no range constraint
                                                                                                                    
                                                                                                                     -  support: MANDATORY
keyValue           String   0..1      keyValue - Value of the key.                                                   OpenModelAttribute
                                                                                                                    
                                                                                                                     -  isInvariant: false
                                                                                                                    
                                                                                                                     -  valueRange: no range constraint
                                                                                                                    
                                                                                                                     -  support: MANDATORY
================== ======== ========= ============================================================================== ==================================

KeyValuePair datatype
^^^^^^^^^^^^^^^^^^^^^

**Qualified Name:** Common::TypeDefinitions::KeyValuePair

**Applied Stereotypes:**

-  Preliminary

**Table** **Attributes for Data Type KeyValuePair**

================== ======== ========= =============== ==================================
**Attribute Name** **Type** **Mult.** **Description** **Stereotypes**
================== ======== ========= =============== ==================================
key                String   1                         OpenModelAttribute
                                                     
                                                      -  isInvariant: false
                                                     
                                                      -  valueRange: no range constraint
                                                     
                                                      -  support: MANDATORY
value              String   1                         OpenModelAttribute
                                                     
                                                      -  isInvariant: false
                                                     
                                                      -  valueRange: no range constraint
                                                     
                                                      -  support: MANDATORY
================== ======== ========= =============== ==================================

Number primitive type
^^^^^^^^^^^^^^^^^^^^^

**Qualified Name:** Common::TypeDefinitions::Number

**Description:**

This primitive type is a superset of the standard UML numbering primitives, e.g. Integer and Real.

**Applied Stereotypes:**

-  Preliminary

Object primitive type
^^^^^^^^^^^^^^^^^^^^^

**Qualified Name:** Common::TypeDefinitions::Object

**Description:**

object - objects are model elements that represent instances of a class or of classes

**Applied Stereotypes:**

-  Preliminary

Rule primitive type
^^^^^^^^^^^^^^^^^^^

**Qualified Name:** Common::TypeDefinitions::Rule

**Description:**

Primitive type describing a rule.

**Applied Stereotypes:**

-  Preliminary

SecurityParameters datatype
^^^^^^^^^^^^^^^^^^^^^^^^^^^

**Qualified Name:** Common::TypeDefinitions::SecurityParameters

**Description:**

The SecurityParameters contains the signature of a NSD, VLD, PNFD or VNFFGD instance together with information required to validate the signature.

**Applied Stereotypes:**

-  Preliminary

**Table** **Attributes for Data Type SecurityParameters**

================== ======== ========= ========================================================================================================= ==================================
**Attribute Name** **Type** **Mult.** **Description**                                                                                           **Stereotypes**
================== ======== ========= ========================================================================================================= ==================================
signature          String   1         Provides the signature of the signed part of the descriptor.                                              OpenModelAttribute
                                                                                                                                               
                                                                                                                                                -  isInvariant: false
                                                                                                                                               
                                                                                                                                                -  valueRange: no range constraint
                                                                                                                                               
                                                                                                                                                -  support: MANDATORY
algorithm          String   1         Identifies the algorithm used to compute the signature.                                                   OpenModelAttribute
                                                                                                                                               
                                                                                                                                                -  isInvariant: false
                                                                                                                                               
                                                                                                                                                -  valueRange: no range constraint
                                                                                                                                               
                                                                                                                                                -  support: MANDATORY
certificate                 0..1      Provides a certificate or a reference to a certificate to validate the signature.                         OpenModelAttribute
                                      NOTE: Cardinality of 0 corresponds to the case where the certificate is provided by means outside the NSD
                                                                                                                                                -  isInvariant: false
                                                                                                                                               
                                                                                                                                                -  valueRange: no range constraint
                                                                                                                                               
                                                                                                                                                -  support: MANDATORY
================== ======== ========= ========================================================================================================= ==================================

TimePeriod datatype
^^^^^^^^^^^^^^^^^^^

**Qualified Name:** Common::TypeDefinitions::TimePeriod

**Description:**

A base / value business entity used to represent a period of time, between two timepoints

**Applied Stereotypes:**

-  Preliminary

**Table** **Attributes for Data Type TimePeriod**

================== ======== ========= ================================================= ==================================
**Attribute Name** **Type** **Mult.** **Description**                                   **Stereotypes**
================== ======== ========= ================================================= ==================================
startDateTime      DateTime 1         An instant of time, starting at the TimePeriod    OpenModelAttribute
                                      Notes:                                           
                                      If null, then represents to the beginning of time -  isInvariant: false
                                                                                       
                                                                                        -  valueRange: no range constraint
                                                                                       
                                                                                        -  support: MANDATORY
endDateTime        DateTime 1         An instant of time, ending at the TimePeriod:     OpenModelAttribute
                                      Notes:                                           
                                      If null, then represents to the end of time       -  isInvariant: false
                                                                                       
                                                                                        -  valueRange: no range constraint
                                                                                       
                                                                                        -  support: MANDATORY
================== ======== ========= ================================================= ==================================

UnixEpoch primitive type
^^^^^^^^^^^^^^^^^^^^^^^^

**Qualified Name:** Common::TypeDefinitions::UnixEpoch

**Description:**

the latest unix time aka epoch time associated with the event from any component--as microseconds elapsed since 1 Jan 1970 not including leap seconds

Uri primitive type
^^^^^^^^^^^^^^^^^^

**Qualified Name:** Common::TypeDefinitions::Uri

**Description:**

type string;

The uri type represents a Uniform Resource Identifier (URI) as defined by STD 66.

Objects using the uri type MUST be in US-ASCII encoding, and MUST be normalized as described by RFC 3986 Sections 6.2.1, 6.2.2.1, and 6.2.2.2. All unnecessary percent-encoding is removed, and all case-insensitive characters are set to lowercase except for hexadecimal digits, which are normalized to uppercase as described in Section 6.2.2.1.

The purpose of this normalization is to help provide unique URIs. Note that this normalization is not sufficient to provide uniqueness. Two URIs that are textually distinct after this normalization may still be equivalent.

Objects using the uri type may restrict the schemes that they permit. For example, 'data:' and 'urn:' schemes might not be appropriate.

A zero-length URI is not a valid URI. This can be used to express 'URI absent' where required.

In the value set and its semantics, this type is equivalent to the Uri SMIv2 textual convention defined in RFC 5017.

reference

RFC 3986: Uniform Resource Identifier (URI): Generic Syntax

RFC 3305: Report from the Joint W3C/IETF URI Planning Interest Group: Uniform Resource Identifiers (URIs), URLs, and Uniform Resource Names (URNs): Clarifications and Recommendations

RFC 5017: MIB Textual Conventions for Uniform Resource Identifiers (URIs);

**Applied Stereotypes:**

-  Preliminary

Uuid primitive type
^^^^^^^^^^^^^^^^^^^

**Qualified Name:** Common::TypeDefinitions::Uuid

**Description:**

type string {

pattern

'[0-9a-fA-F]{8}-[0-9a-fA-F]{4}-[0-9a-fA-F]{4}-[0-9a-fA-F]{4}-[0-9a-fA-F]{12}'; }

A Universally Unique IDentifier in the string representation defined in RFC 4122. The canonical representation uses lowercase characters.

The following is an example of a UUID in string representation: f81d4fae-7dec-11d0-a765-00a0c91e6bf6;

reference

RFC 4122: A Universally Unique IDentifier (UUID) URN Namespace;

**Applied Stereotypes:**

-  Preliminary

Version primitive type
^^^^^^^^^^^^^^^^^^^^^^

**Qualified Name:** Common::TypeDefinitions::Version

**Description:**

This primitive type defines the version of an element.

**Applied Stereotypes:**

-  Preliminary