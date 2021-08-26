.. Copyright 2021
.. This file is licensed under the CREATIVE COMMONS ATTRIBUTION 4.0 INTERNATIONAL LICENSE
.. Full license text at https://creativecommons.org/licenses/by/4.0/legalcode

VES Datatype Definition
-----------------------

.. contents::
   :depth: 3
..

Data Types
----------

ArrayOfSchemaObject
~~~~~~~~~~~~~~~~~~~

arrayOfSchemaObject - The arrayOfSchemaObject datatype provides an array of json objects, each of which is described by name, schema and other meta-information.

Note: The VES Spec has this as a Json based object.

Applied stereotypes:

-  Preliminary

=================== ============ ========= ========== ================================== =============================================================================================================================================================
**Attribute Name**  **Type**     **Mult.** **Access** **Stereotypes**                    **Description**
arrayOfSchemaObject SchemaObject 1..\*     RW         Preliminary                        arrayOfSchemaObject - arrayOfSchemaObject datatype provides an array of SchemaObjects, each of which is described by name, schema and other meta-information.
                                                                                        
                                                      OpenModelAttribute                
                                                                                        
                                                      -  isInvariant: false             
                                                                                        
                                                      -  valueRange: no range constraint
                                                                                        
                                                      -  support: MANDATORY             
=================== ============ ========= ========== ================================== =============================================================================================================================================================

ArrayofNamedHashMap
~~~~~~~~~~~~~~~~~~~

Array of named hashMaps

Applied stereotypes:

-  Preliminary

=================== ============ ========= ========== ================================== =======================
**Attribute Name**  **Type**     **Mult.** **Access** **Stereotypes**                    **Description**
arrayOfNamedHashmap NamedHashMap 1..\*     RW         Preliminary                        Array of named hashMaps
                                                                                        
                                                      OpenModelAttribute                
                                                                                        
                                                      -  isInvariant: false             
                                                                                        
                                                      -  valueRange: no range constraint
                                                                                        
                                                      -  support: MANDATORY             
=================== ============ ========= ========== ================================== =======================

AttributeList
~~~~~~~~~~~~~

Applied stereotypes:

-  Experimental

================== ======== ========= ========== ================================== ===============
**Attribute Name** **Type** **Mult.** **Access** **Stereotypes**                    **Description**
atributeName       String   1         RW         OpenModelAttribute                
                                                                                   
                                                 -  isInvariant: false             
                                                                                   
                                                 -  valueRange: no range constraint
                                                                                   
                                                 -  support: MANDATORY             
newAttributeValue  String   1         RW         OpenModelAttribute                
                                                                                   
                                                 -  isInvariant: false             
                                                                                   
                                                 -  valueRange: no range constraint
                                                                                   
                                                 -  support: MANDATORY             
NewAttributeType   String   1         RW         OpenModelAttribute                
                                                                                   
                                                 -  isInvariant: false             
                                                                                   
                                                 -  valueRange: no range constraint
                                                                                   
                                                 -  support: MANDATORY             
oldAttributeValue  String   1         RW         OpenModelAttribute                
                                                                                   
                                                 -  isInvariant: false             
                                                                                   
                                                 -  valueRange: no range constraint
                                                                                   
                                                 -  support: MANDATORY             
oldAttributeType   String   1         RW         OpenModelAttribute                
                                                                                   
                                                 -  isInvariant: false             
                                                                                   
                                                 -  valueRange: no range constraint
                                                                                   
                                                 -  support: MANDATORY             
================== ======== ========= ========== ================================== ===============

HashMap
~~~~~~~

The hashMap datatype is an 'associative array', which is an unordered collection of key-value pairs of the form "key": "value", where each key and value are strings. Keys must use camel casing to separate words and acronyms; only the first letter of each acronym shall be capitalized.

Applied stereotypes:

-  Preliminary

================== ============ ========= ========== ================================== ========================================================
**Attribute Name** **Type**     **Mult.** **Access** **Stereotypes**                    **Description**
hashmapEntry       KeyValuePair 0..\*     RW         Preliminary                        A given entry in the hashmap, which is a key/value pair.
                                                                                       
                                                     OpenModelAttribute                
                                                                                       
                                                     -  isInvariant: false             
                                                                                       
                                                     -  valueRange: no range constraint
                                                                                       
                                                     -  support: MANDATORY             
================== ============ ========= ========== ================================== ========================================================

NamedHashMap
~~~~~~~~~~~~

namedHashMap [ ] - The namedHashmap datatype is a hashMap which is associated with and described by a name.

Applied stereotypes:

-  Preliminary

================== ======== ========= ========== ================================== ===========================================================================
**Attribute Name** **Type** **Mult.** **Access** **Stereotypes**                    **Description**
name               String   1         RW         Preliminary                        name - Name for the array of name-value pairs.
                                                                                   
                                                 OpenModelAttribute                
                                                                                   
                                                 -  isInvariant: false             
                                                                                   
                                                 -  valueRange: no range constraint
                                                                                   
                                                 -  support: MANDATORY             
hashMap            HashMap  1         RW         Preliminary                        hashMap - One or more key:value pairs.
                                                                                    Note: in ATTServiceSpecification - VesEventListener v5.4.1 type = field [].
                                                 OpenModelAttribute                
                                                                                   
                                                 -  isInvariant: false             
                                                                                   
                                                 -  valueRange: no range constraint
                                                                                   
                                                 -  support: MANDATORY             
================== ======== ========= ========== ================================== ===========================================================================

.. _processstats-1:

ProcessStats
~~~~~~~~~~~~

Applied stereotypes:

SchemaObject
~~~~~~~~~~~~

SchemaObject - The SchemaObject datatype provides an object schema, name and other meta-information along with one or more object instances that conform to the schema.

Note: The VES Spec has this as a Json based object.

Applied stereotypes:

-  Preliminary

===================== ==================== ========= ========== ================================== =============================================================================================================================================================================================
**Attribute Name**    **Type**             **Mult.** **Access** **Stereotypes**                    **Description**
objectInstances       SchemaObjectInstance 1..\*     RW         Preliminary                        objectInstances - Contains one or more instances of the SchemaObjectInstance object.
                                                                                                  
                                                                OpenModelAttribute                
                                                                                                  
                                                                -  isInvariant: false             
                                                                                                  
                                                                -  valueRange: no range constraint
                                                                                                  
                                                                -  support: MANDATORY             
objectName            String               1         RW         Preliminary                        objectName - Name of the object.
                                                                                                  
                                                                OpenModelAttribute                
                                                                                                  
                                                                -  isInvariant: false             
                                                                                                  
                                                                -  valueRange: no range constraint
                                                                                                  
                                                                -  support: MANDATORY             
objectSchema          String               0..1      RW         Preliminary                        objectSchema - schema for the object.
                                                                                                  
                                                                OpenModelAttribute                
                                                                                                  
                                                                -  isInvariant: false             
                                                                                                  
                                                                -  valueRange: no range constraint
                                                                                                  
                                                                -  support: MANDATORY             
objectSchemaUrl       String               0..1      RW         Preliminary                        objectSchemaUrl - URL to the schema for the object.
                                                                                                  
                                                                OpenModelAttribute                
                                                                                                  
                                                                -  isInvariant: false             
                                                                                                  
                                                                -  valueRange: no range constraint
                                                                                                  
                                                                -  support: MANDATORY             
nfSubcribedObjectName String               0..1      RW         Preliminary                        nfSubscribedObjectName - Name of the object associated with the nfSubscriptionId.
                                                                                                  
                                                                OpenModelAttribute                
                                                                                                  
                                                                -  isInvariant: false             
                                                                                                  
                                                                -  valueRange: no range constraint
                                                                                                  
                                                                -  support: MANDATORY             
nfSubcriptionId       String               0..1      RW         Preliminary                        nfSubscriptionId - Identifies an OpenConfig telemetry subscription on a network function, which configures the network function to send complex object data associated with the SchemaObject.
                                                                                                  
                                                                OpenModelAttribute                
                                                                                                  
                                                                -  isInvariant: false             
                                                                                                  
                                                                -  valueRange: no range constraint
                                                                                                  
                                                                -  support: MANDATORY             
===================== ==================== ========= ========== ================================== =============================================================================================================================================================================================

SchemaObjectInstance
~~~~~~~~~~~~~~~~~~~~

SchemaObjectInstance [ ] - The SchemabjectInstance datatype provides meta-information about an instance of a SchemaObject along with the actual object instance.

Note: The VES Spec has this as a Json based object.

Applied stereotypes:

-  Preliminary

=========================== ============ ========= ========== ================================== ======================================================================================================================================================================
**Attribute Name**          **Type**     **Mult.** **Access** **Stereotypes**                    **Description**
schemaObject                SchemaObject 0..\*     RW         Preliminary                        SchemaObject - Optional recursive specification on SchemaObject
                                                                                                
                                                              OpenModelAttribute                
                                                                                                
                                                              -  isInvariant: false             
                                                                                                
                                                              -  valueRange: no range constraint
                                                                                                
                                                              -  support: MANDATORY             
objectInstance              Object       0..1      RW         Preliminary                        objectInstance - Contains an instance conforming to the SchemaObject schema
                                                                                                
                                                              OpenModelAttribute                
                                                                                                
                                                              -  isInvariant: false             
                                                                                                
                                                              -  valueRange: no range constraint
                                                                                                
                                                              -  support: MANDATORY             
objectInstanceEpochMicrosec UnixEpoch    0..1      RW         Preliminary                        objectInstanceEpochMicrosec - the unix time, aka epoch time, associated with this objectInstance--as microseconds elapsed since 1 Jan 1970 not including leap seconds.
                                                                                                
                                                              OpenModelAttribute                
                                                                                                
                                                              -  isInvariant: false             
                                                                                                
                                                              -  valueRange: no range constraint
                                                                                                
                                                              -  support: MANDATORY             
objectKeys                  Key          0..\*     RW         Preliminary                        objectKeys - An ordered set of keys that identifies this particular instance of SchemaObject (e.g., that places it in a hierarchy).
                                                                                                
                                                              OpenModelAttribute                
                                                                                                
                                                              -  isInvariant: false             
                                                                                                
                                                              -  valueRange: no range constraint
                                                                                                
                                                              -  support: MANDATORY             
=========================== ============ ========= ========== ================================== ======================================================================================================================================================================

ThresholdCrossingAlertCounter
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

Applied stereotypes:

-  Preliminary

================== ============== ========= ========== ================================== ============================================================================
**Attribute Name** **Type**       **Mult.** **Access** **Stereotypes**                    **Description**
criticality        TCACriticality 1         RW         Preliminary                        Enumeration: 'CRIT', 'MAJ'
                                                                                         
                                                       OpenModelAttribute                
                                                                                         
                                                       -  isInvariant: false             
                                                                                         
                                                       -  valueRange: no range constraint
                                                                                         
                                                       -  support: MANDATORY             
hashMap            HashMap        1         RW         Preliminary                        Key is the name of the counter and value is the current value of the counter
                                                                                         
                                                       OpenModelAttribute                
                                                                                         
                                                       -  isInvariant: false             
                                                                                         
                                                       -  valueRange: no range constraint
                                                                                         
                                                       -  support: MANDATORY             
thresholdCrossed   String         1         RW         Preliminary                        Last threshold that was crossed
                                                                                         
                                                       OpenModelAttribute                
                                                                                         
                                                       -  isInvariant: false             
                                                                                         
                                                       -  valueRange: no range constraint
                                                                                         
                                                       -  support: MANDATORY             
================== ============== ========= ========== ================================== ============================================================================
