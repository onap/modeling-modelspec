.. Copyright 2019
.. This file is licensed under the CREATIVE COMMONS ATTRIBUTION 4.0 INTERNATIONAL LICENSE
.. Full license text at https://creativecommons.org/licenses/by/4.0/legalcode

VES Datatype Definition
-----------------------

.. contents::
   :depth: 3
..

ArrayOfSchemaObject datatype
^^^^^^^^^^^^^^^^^^^^^^^^^^^^

**Qualified Name:** Ves::TypeDefinitions::ArrayOfSchemaObject

**Description:**

arrayOfSchemaObject - The arrayOfSchemaObject datatype provides an array of json objects, each of which is described by name, schema and other meta-information.

Note: The VES Spec has this as a Json based object.

**Applied Stereotypes:**

-  Preliminary

**Table** **Attributes for Data Type ArrayOfSchemaObject**

=================== ============ ========= ============================================================================================================================================================= ==================================
**Attribute Name**  **Type**     **Mult.** **Description**                                                                                                                                               **Stereotypes**
=================== ============ ========= ============================================================================================================================================================= ==================================
arrayOfSchemaObject SchemaObject 1..\*     arrayOfSchemaObject - arrayOfSchemaObject datatype provides an array of SchemaObjects, each of which is described by name, schema and other meta-information. OpenModelAttribute
                                                                                                                                                                                                        
                                                                                                                                                                                                         -  isInvariant: false
                                                                                                                                                                                                        
                                                                                                                                                                                                         -  valueRange: no range constraint
                                                                                                                                                                                                        
                                                                                                                                                                                                         -  support: MANDATORY
                                                                                                                                                                                                        
                                                                                                                                                                                                         Preliminary
=================== ============ ========= ============================================================================================================================================================= ==================================

ArrayofNamedHashMap datatype
^^^^^^^^^^^^^^^^^^^^^^^^^^^^

**Qualified Name:** Ves::TypeDefinitions::ArrayofNamedHashMap

**Description:**

Array of named hashMaps

**Applied Stereotypes:**

-  Preliminary

**Table** **Attributes for Data Type ArrayofNamedHashMap**

=================== ============ ========= ======================= ==================================
**Attribute Name**  **Type**     **Mult.** **Description**         **Stereotypes**
=================== ============ ========= ======================= ==================================
arrayOfNamedHashmap NamedHashMap 1..\*     Array of named hashMaps OpenModelAttribute
                                                                  
                                                                   -  isInvariant: false
                                                                  
                                                                   -  valueRange: no range constraint
                                                                  
                                                                   -  support: MANDATORY
                                                                  
                                                                   Preliminary
=================== ============ ========= ======================= ==================================

HashMap datatype
^^^^^^^^^^^^^^^^

**Qualified Name:** Ves::TypeDefinitions::HashMap

**Description:**

The hashMap datatype is an 'associative array', which is an unordered collection of key-value pairs of the form "key": "value", where each key and value are strings. Keys must use camel casing to separate words and acronyms; only the first letter of each acronym shall be capitalized.

**Applied Stereotypes:**

-  Preliminary

**Table** **Attributes for Data Type HashMap**

================== ============ ========= ======================================================== ==================================
**Attribute Name** **Type**     **Mult.** **Description**                                          **Stereotypes**
================== ============ ========= ======================================================== ==================================
hashmapEntry       KeyValuePair 0..\*     A given entry in the hashmap, which is a key/value pair. OpenModelAttribute
                                                                                                  
                                                                                                   -  isInvariant: false
                                                                                                  
                                                                                                   -  valueRange: no range constraint
                                                                                                  
                                                                                                   -  support: MANDATORY
                                                                                                  
                                                                                                   Preliminary
================== ============ ========= ======================================================== ==================================

NamedHashMap datatype
^^^^^^^^^^^^^^^^^^^^^

**Qualified Name:** Ves::TypeDefinitions::NamedHashMap

**Description:**

namedHashMap [ ] - The namedHashmap datatype is a hashMap which is associated with and described by a name.

**Applied Stereotypes:**

-  Preliminary

**Table** **Attributes for Data Type NamedHashMap**

================== ======== ========= =========================================================================== ==================================
**Attribute Name** **Type** **Mult.** **Description**                                                             **Stereotypes**
================== ======== ========= =========================================================================== ==================================
name               String   1         name - Name for the array of name-value pairs.                              OpenModelAttribute
                                                                                                                 
                                                                                                                  -  isInvariant: false
                                                                                                                 
                                                                                                                  -  valueRange: no range constraint
                                                                                                                 
                                                                                                                  -  support: MANDATORY
                                                                                                                 
                                                                                                                  Preliminary
hashMap            HashMap  1         hashMap - One or more key:value pairs.                                      OpenModelAttribute
                                      Note: in ATTServiceSpecification - VesEventListener v5.4.1 type = field [].
                                                                                                                  -  isInvariant: false
                                                                                                                 
                                                                                                                  -  valueRange: no range constraint
                                                                                                                 
                                                                                                                  -  support: MANDATORY
                                                                                                                 
                                                                                                                  Preliminary
================== ======== ========= =========================================================================== ==================================

ProcessStats datatype
^^^^^^^^^^^^^^^^^^^^^

**Qualified Name:** Ves::TypeDefinitions::ProcessStats

SchemaObject datatype
^^^^^^^^^^^^^^^^^^^^^

**Qualified Name:** Ves::TypeDefinitions::SchemaObject

**Description:**

SchemaObject - The SchemaObject datatype provides an object schema, name and other meta-information along with one or more object instances that conform to the schema.

Note: The VES Spec has this as a Json based object.

**Applied Stereotypes:**

-  Preliminary

**Table** **Attributes for Data Type SchemaObject**

===================== ==================== ========= ============================================================================================================================================================================================= ==================================
**Attribute Name**    **Type**             **Mult.** **Description**                                                                                                                                                                               **Stereotypes**
===================== ==================== ========= ============================================================================================================================================================================================= ==================================
objectInstances       SchemaObjectInstance 1..\*     objectInstances - Contains one or more instances of the SchemaObjectInstance object.                                                                                                          OpenModelAttribute
                                                                                                                                                                                                                                                  
                                                                                                                                                                                                                                                   -  isInvariant: false
                                                                                                                                                                                                                                                  
                                                                                                                                                                                                                                                   -  valueRange: no range constraint
                                                                                                                                                                                                                                                  
                                                                                                                                                                                                                                                   -  support: MANDATORY
                                                                                                                                                                                                                                                  
                                                                                                                                                                                                                                                   Preliminary
objectName            String               1         objectName - Name of the object.                                                                                                                                                              OpenModelAttribute
                                                                                                                                                                                                                                                  
                                                                                                                                                                                                                                                   -  isInvariant: false
                                                                                                                                                                                                                                                  
                                                                                                                                                                                                                                                   -  valueRange: no range constraint
                                                                                                                                                                                                                                                  
                                                                                                                                                                                                                                                   -  support: MANDATORY
                                                                                                                                                                                                                                                  
                                                                                                                                                                                                                                                   Preliminary
objectSchema          String               0..1      objectSchema - schema for the object.                                                                                                                                                         OpenModelAttribute
                                                                                                                                                                                                                                                  
                                                                                                                                                                                                                                                   -  isInvariant: false
                                                                                                                                                                                                                                                  
                                                                                                                                                                                                                                                   -  valueRange: no range constraint
                                                                                                                                                                                                                                                  
                                                                                                                                                                                                                                                   -  support: MANDATORY
                                                                                                                                                                                                                                                  
                                                                                                                                                                                                                                                   Preliminary
objectSchemaUrl       String               0..1      objectSchemaUrl - URL to the schema for the object.                                                                                                                                           OpenModelAttribute
                                                                                                                                                                                                                                                  
                                                                                                                                                                                                                                                   -  isInvariant: false
                                                                                                                                                                                                                                                  
                                                                                                                                                                                                                                                   -  valueRange: no range constraint
                                                                                                                                                                                                                                                  
                                                                                                                                                                                                                                                   -  support: MANDATORY
                                                                                                                                                                                                                                                  
                                                                                                                                                                                                                                                   Preliminary
nfSubcribedObjectName String               0..1      nfSubscribedObjectName - Name of the object associated with the nfSubscriptionId.                                                                                                             OpenModelAttribute
                                                                                                                                                                                                                                                  
                                                                                                                                                                                                                                                   -  isInvariant: false
                                                                                                                                                                                                                                                  
                                                                                                                                                                                                                                                   -  valueRange: no range constraint
                                                                                                                                                                                                                                                  
                                                                                                                                                                                                                                                   -  support: MANDATORY
                                                                                                                                                                                                                                                  
                                                                                                                                                                                                                                                   Preliminary
nfSubcriptionId       String               0..1      nfSubscriptionId - Identifies an OpenConfig telemetry subscription on a network function, which configures the network function to send complex object data associated with the SchemaObject. OpenModelAttribute
                                                                                                                                                                                                                                                  
                                                                                                                                                                                                                                                   -  isInvariant: false
                                                                                                                                                                                                                                                  
                                                                                                                                                                                                                                                   -  valueRange: no range constraint
                                                                                                                                                                                                                                                  
                                                                                                                                                                                                                                                   -  support: MANDATORY
                                                                                                                                                                                                                                                  
                                                                                                                                                                                                                                                   Preliminary
===================== ==================== ========= ============================================================================================================================================================================================= ==================================

SchemaObjectInstance datatype
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

**Qualified Name:** Ves::TypeDefinitions::SchemaObjectInstance

**Description:**

SchemaObjectInstance [ ] - The SchemabjectInstance datatype provides meta-information about an instance of a SchemaObject along with the actual object instance.

Note: The VES Spec has this as a Json based object.

**Applied Stereotypes:**

-  Preliminary

**Table** **Attributes for Data Type SchemaObjectInstance**

=========================== ============ ========= ====================================================================================================================================================================== ==================================
**Attribute Name**          **Type**     **Mult.** **Description**                                                                                                                                                        **Stereotypes**
=========================== ============ ========= ====================================================================================================================================================================== ==================================
schemaObject                SchemaObject 0..\*     SchemaObject - Optional recursive specification on SchemaObject                                                                                                        OpenModelAttribute
                                                                                                                                                                                                                         
                                                                                                                                                                                                                          -  isInvariant: false
                                                                                                                                                                                                                         
                                                                                                                                                                                                                          -  valueRange: no range constraint
                                                                                                                                                                                                                         
                                                                                                                                                                                                                          -  support: MANDATORY
                                                                                                                                                                                                                         
                                                                                                                                                                                                                          Preliminary
objectInstance              Object       0..1      objectInstance - Contains an instance conforming to the SchemaObject schema                                                                                            OpenModelAttribute
                                                                                                                                                                                                                         
                                                                                                                                                                                                                          -  isInvariant: false
                                                                                                                                                                                                                         
                                                                                                                                                                                                                          -  valueRange: no range constraint
                                                                                                                                                                                                                         
                                                                                                                                                                                                                          -  support: MANDATORY
                                                                                                                                                                                                                         
                                                                                                                                                                                                                          Preliminary
objectInstanceEpochMicrosec UnixEpoch    0..1      objectInstanceEpochMicrosec - the unix time, aka epoch time, associated with this objectInstance--as microseconds elapsed since 1 Jan 1970 not including leap seconds. OpenModelAttribute
                                                                                                                                                                                                                         
                                                                                                                                                                                                                          -  isInvariant: false
                                                                                                                                                                                                                         
                                                                                                                                                                                                                          -  valueRange: no range constraint
                                                                                                                                                                                                                         
                                                                                                                                                                                                                          -  support: MANDATORY
                                                                                                                                                                                                                         
                                                                                                                                                                                                                          Preliminary
objectKeys                  Key          0..\*     objectKeys - An ordered set of keys that identifies this particular instance of SchemaObject (e.g., that places it in a hierarchy).                                    OpenModelAttribute
                                                                                                                                                                                                                         
                                                                                                                                                                                                                          -  isInvariant: false
                                                                                                                                                                                                                         
                                                                                                                                                                                                                          -  valueRange: no range constraint
                                                                                                                                                                                                                         
                                                                                                                                                                                                                          -  support: MANDATORY
                                                                                                                                                                                                                         
                                                                                                                                                                                                                          Preliminary
=========================== ============ ========= ====================================================================================================================================================================== ==================================

ThresholdCrossingAlertCounter datatype
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

**Qualified Name:** Ves::TypeDefinitions::ThresholdCrossingAlertCounter

**Applied Stereotypes:**

-  Preliminary

**Table** **Attributes for Data Type ThresholdCrossingAlertCounter**

================== ============== ========= ============================================================================ ==================================
**Attribute Name** **Type**       **Mult.** **Description**                                                              **Stereotypes**
================== ============== ========= ============================================================================ ==================================
criticality        TCACriticality 1         Enumeration: 'CRIT', 'MAJ'                                                   OpenModelAttribute
                                                                                                                        
                                                                                                                         -  isInvariant: false
                                                                                                                        
                                                                                                                         -  valueRange: no range constraint
                                                                                                                        
                                                                                                                         -  support: MANDATORY
                                                                                                                        
                                                                                                                         Preliminary
hashMap            HashMap        1         Key is the name of the counter and value is the current value of the counter OpenModelAttribute
                                                                                                                        
                                                                                                                         -  isInvariant: false
                                                                                                                        
                                                                                                                         -  valueRange: no range constraint
                                                                                                                        
                                                                                                                         -  support: MANDATORY
                                                                                                                        
                                                                                                                         Preliminary
thresholdCrossed   String         1         Last threshold that was crossed                                              OpenModelAttribute
                                                                                                                        
                                                                                                                         -  isInvariant: false
                                                                                                                        
                                                                                                                         -  valueRange: no range constraint
                                                                                                                        
                                                                                                                         -  support: MANDATORY
                                                                                                                        
                                                                                                                         Preliminary
================== ============== ========= ============================================================================ ==================================
