.. Copyright 2020 (China Mobile)
.. This file is licensed under the CREATIVE COMMONS ATTRIBUTION 4.0 INTERNATIONAL LICENSE
.. Full license text at https://creativecommons.org/licenses/by/4.0/legalcode

Atomic / Composite Service View
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

.. contents::
   :depth: 3
..


|image0|

Classes
=======

ServiceAtomicDescriptor
-----------------------

**Parent class:** ServiceDescriptor

Applied stereotypes:

-  Preliminary

-  OpenModelClass

-  **support: MANDATORY**

====================================== ==================================== ========= ================================== =====================================================================================================================================================
**Attribute Name**                     **Type**                             **Mult.** **Stereotypes**                    **Description**
====================================== ==================================== ========= ================================== =====================================================================================================================================================
\_serviceAtomicInstance                ServiceAtomicInstance                0..\*     OpenModelAttribute                 An implementation of atomic Service corresponding to a ServicecAtomicDescriptor.
                                                                                                                        
                                                                                      -  isInvariant: false             
                                                                                                                        
                                                                                      -  valueRange: no range constraint
                                                                                                                        
                                                                                      -  support: MANDATORY             
\_resourceDesc (resourcespecification) ResourceDesc (ResourceSpecification) 0..\*     OpenModelAttribute                 Resource components of constituting a serivce descriptor.
                                                                                                                        
                                                                                      -  isInvariant: false             
                                                                                                                        
                                                                                      -  valueRange: no range constraint
                                                                                                                        
                                                                                      -  support: MANDATORY             
serviceInvariantId                     Identifier                           1         Preliminary                        Constant identifier of the service model.
                                                                                                                        
                                                                                      OpenModelAttribute                
                                                                                                                        
                                                                                      -  isInvariant: false             
                                                                                                                        
                                                                                      -  valueRange: no range constraint
                                                                                                                        
                                                                                      -  support: MANDATORY             
serviceId                              Identifier                           1         Preliminary                        Versioned identifier of the service model (this uuid is changed for every major version of the service)
                                                                                                                        
                                                                                      OpenModelAttribute                
                                                                                                                        
                                                                                      -  isInvariant: false             
                                                                                                                        
                                                                                      -  valueRange: no range constraint
                                                                                                                        
                                                                                      -  support: MANDATORY             
name                                   String                               1         Preliminary                        The name of the service model designed.
                                                                                                                        
                                                                                      OpenModelAttribute                
                                                                                                                        
                                                                                      -  isInvariant: false             
                                                                                                                        
                                                                                      -  valueRange: no range constraint
                                                                                                                        
                                                                                      -  support: MANDATORY             
description                            String                               1         Preliminary                        The description of the service model designed.
                                                                                                                        
                                                                                      OpenModelAttribute                
                                                                                                                        
                                                                                      -  isInvariant: false             
                                                                                                                        
                                                                                      -  valueRange: no range constraint
                                                                                                                        
                                                                                      -  support: MANDATORY             
category                               String                               1..\*     Preliminary                        A predefined list which identifies the construct's category. There is a predefined list of service categories.
                                                                                                                        
                                                                                      OpenModelAttribute                
                                                                                                                        
                                                                                      -  isInvariant: false             
                                                                                                                        
                                                                                      -  valueRange: no range constraint
                                                                                                                        
                                                                                      -  support: MANDATORY             
version                                String                               1         Preliminary                        The service model version.
                                                                                                                        
                                                                                      OpenModelAttribute                
                                                                                                                        
                                                                                      -  isInvariant: false             
                                                                                                                        
                                                                                      -  valueRange: no range constraint
                                                                                                                        
                                                                                      -  support: MANDATORY             
serviceType                            String                               0..1      Preliminary                        An optional string field defining a generic type (like category) of the service. E.g. this field can be used for defining the service as "TRANSPORT".
                                                                                                                        
                                                                                      OpenModelAttribute                
                                                                                                                        
                                                                                      -  isInvariant: false             
                                                                                                                        
                                                                                      -  valueRange: no range constraint
                                                                                                                        
                                                                                      -  support: MANDATORY             
serviceRole                            String                               0..1      Preliminary                        An optional string field for shortcode that defines the function that the service is providing. E.g. "MISVPN" or "AIM".
                                                                                                                        
                                                                                      OpenModelAttribute                
                                                                                                                        
                                                                                      -  isInvariant: false             
                                                                                                                        
                                                                                      -  valueRange: no range constraint
                                                                                                                        
                                                                                      -  support: MANDATORY             
icon                                   String                               1         Preliminary                        The icon path of the service.
                                                                                                                        
                                                                                      OpenModelAttribute                
                                                                                                                        
                                                                                      -  isInvariant: false             
                                                                                                                        
                                                                                      -  valueRange: no range constraint
                                                                                                                        
                                                                                      -  support: MANDATORY             
====================================== ==================================== ========= ================================== =====================================================================================================================================================

ServiceAtomicInstance
---------------------

**Parent class:** ServiceInstance

Applied stereotypes:

-  Preliminary

-  OpenModelClass

-  **support: MANDATORY**

=================== ================ ========= ================================== ========================================================================================================================================================================================================================================================
**Attribute Name**  **Type**         **Mult.** **Stereotypes**                    **Description**
=================== ================ ========= ================================== ========================================================================================================================================================================================================================================================
\_resourceInstance  ResourceInstance 0..\*     OpenModelAttribute                 Resource instance components of constituting a service instance.
                                                                                 
                                               -  isInvariant: false             
                                                                                 
                                               -  valueRange: no range constraint
                                                                                 
                                               -  support: MANDATORY             
serviceInstanceId   Identifier       1         Preliminary                        Uniquely identifies this instance of a service.
                                                                                 
                                               OpenModelAttribute                
                                                                                 
                                               -  isInvariant: false             
                                                                                 
                                               -  valueRange: no range constraint
                                                                                 
                                               -  support: MANDATORY             
serviceInstanceName String           0..1      Preliminary                        The name assigned to the service-instance.
                                                                                 
                                               OpenModelAttribute                
                                                                                 
                                               -  isInvariant: false             
                                                                                 
                                               -  valueRange: no range constraint
                                                                                 
                                               -  support: OPTIONAL              
serviceType         String           0..1      Preliminary                        An optional string field defining a generic type (like category) of the service. E.g. this field can be used for defining the service as "TRANSPORT".
                                                                                 
                                               OpenModelAttribute                
                                                                                 
                                               -  isInvariant: false             
                                                                                 
                                               -  valueRange: no range constraint
                                                                                 
                                               -  support: MANDATORY             
serviceRole         String           1         Preliminary                        An optional string field for shortcode that defines the function that the service is providing. E.g. "MISVPN" or "AIM".
                                                                                 
                                               OpenModelAttribute                
                                                                                 
                                               -  isInvariant: false             
                                                                                 
                                               -  valueRange: no range constraint
                                                                                 
                                               -  support: MANDATORY             
selfLink            Uri              1         Preliminary                        URL to endpoint where more details can be gotten.
                                                                                 
                                               OpenModelAttribute                
                                                                                 
                                               -  isInvariant: false             
                                                                                 
                                               -  valueRange: no range constraint
                                                                                 
                                               -  support: MANDATORY             
orchestrationStatus String           1         Preliminary                        Orchestration status of the service instance.
                                                                                 
                                               OpenModelAttribute                
                                                                                 
                                               -  isInvariant: false             
                                                                                 
                                               -  valueRange: no range constraint
                                                                                 
                                               -  support: MANDATORY             
nsStatus            String           1         Preliminary                        Describe NS instance staus: instantiating(creating the Networek Service instance), active(the existed Network Service instance is under using), terminating(the existed Network Service instance stops using) or etc(healing and other possible status).
                                                                                 
                                               OpenModelAttribute                
                                                                                 
                                               -  isInvariant: false             
                                                                                 
                                               -  valueRange: no range constraint
                                                                                 
                                               -  support: MANDATORY             
=================== ================ ========= ================================== ========================================================================================================================================================================================================================================================

ServiceCompositeDescriptor
--------------------------

ServcieCompositeDescriptor is used to model the design time
representation of a service component or network service.

**Parent class:** ServiceDescriptor

Applied stereotypes:

-  Preliminary

-  OpenModelClass

-  **support: MANDATORY**

====================================== ==================================== ========= ================================== =====================================================================================================================================================
**Attribute Name**                     **Type**                             **Mult.** **Stereotypes**                    **Description**
====================================== ==================================== ========= ================================== =====================================================================================================================================================
\_serviceDescriptor                    ServiceDescriptor                    0..\*     OpenModelAttribute                 Describe the nested relationship between multiple Service Descriptors.
                                                                                                                        
                                                                                      -  isInvariant: false             
                                                                                                                        
                                                                                      -  valueRange: no range constraint
                                                                                                                        
                                                                                      -  support: MANDATORY             
\_serviceCompositeInstance             ServiceCompositeInstance             0..\*     OpenModelAttribute                 An implementation of composite Service corresponding to a ServiceCompositeDescriptor.
                                                                                                                        
                                                                                      -  isInvariant: false             
                                                                                                                        
                                                                                      -  valueRange: no range constraint
                                                                                                                        
                                                                                      -  support: MANDATORY             
\_resourceDesc (resourcespecification) ResourceDesc (ResourceSpecification) 0..\*     OpenModelAttribute                 Resource components of constituting a serivce descriptor.
                                                                                                                        
                                                                                      -  isInvariant: false             
                                                                                                                        
                                                                                      -  valueRange: no range constraint
                                                                                                                        
                                                                                      -  support: MANDATORY             
serviceInvariantId                     Identifier                           1         Preliminary                        Constant identifier of the service model.
                                                                                                                        
                                                                                      OpenModelAttribute                
                                                                                                                        
                                                                                      -  isInvariant: false             
                                                                                                                        
                                                                                      -  valueRange: no range constraint
                                                                                                                        
                                                                                      -  support: MANDATORY             
serviceId                              Identifier                           1         Preliminary                        Versioned identifier of the service model (this uuid is changed for every major version of the service)
                                                                                                                        
                                                                                      OpenModelAttribute                
                                                                                                                        
                                                                                      -  isInvariant: false             
                                                                                                                        
                                                                                      -  valueRange: no range constraint
                                                                                                                        
                                                                                      -  support: MANDATORY             
name                                   String                               1         Preliminary                        The name of the service model designed.
                                                                                                                        
                                                                                      OpenModelAttribute                
                                                                                                                        
                                                                                      -  isInvariant: false             
                                                                                                                        
                                                                                      -  valueRange: no range constraint
                                                                                                                        
                                                                                      -  support: MANDATORY             
description                            String                               1         Preliminary                        The description of the service model designed.
                                                                                                                        
                                                                                      OpenModelAttribute                
                                                                                                                        
                                                                                      -  isInvariant: false             
                                                                                                                        
                                                                                      -  valueRange: no range constraint
                                                                                                                        
                                                                                      -  support: MANDATORY             
category                               String                               1..\*     Preliminary                        A predefined list which identifies the construct's category. There is a predefined list of service categories.
                                                                                                                        
                                                                                      OpenModelAttribute                
                                                                                                                        
                                                                                      -  isInvariant: false             
                                                                                                                        
                                                                                      -  valueRange: no range constraint
                                                                                                                        
                                                                                      -  support: MANDATORY             
version                                String                               1         Preliminary                        The service model version.
                                                                                                                        
                                                                                      OpenModelAttribute                
                                                                                                                        
                                                                                      -  isInvariant: false             
                                                                                                                        
                                                                                      -  valueRange: no range constraint
                                                                                                                        
                                                                                      -  support: MANDATORY             
serviceType                            String                               0..1      Preliminary                        An optional string field defining a generic type (like category) of the service. E.g. this field can be used for defining the service as "TRANSPORT".
                                                                                                                        
                                                                                      OpenModelAttribute                
                                                                                                                        
                                                                                      -  isInvariant: false             
                                                                                                                        
                                                                                      -  valueRange: no range constraint
                                                                                                                        
                                                                                      -  support: MANDATORY             
serviceRole                            String                               0..1      Preliminary                        An optional string field for shortcode that defines the function that the service is providing. E.g. "MISVPN" or "AIM".
                                                                                                                        
                                                                                      OpenModelAttribute                
                                                                                                                        
                                                                                      -  isInvariant: false             
                                                                                                                        
                                                                                      -  valueRange: no range constraint
                                                                                                                        
                                                                                      -  support: MANDATORY             
icon                                   String                               1         Preliminary                        The icon path of the service.
                                                                                                                        
                                                                                      OpenModelAttribute                
                                                                                                                        
                                                                                      -  isInvariant: false             
                                                                                                                        
                                                                                      -  valueRange: no range constraint
                                                                                                                        
                                                                                      -  support: MANDATORY             
====================================== ==================================== ========= ================================== =====================================================================================================================================================

ServiceCompositeInstance
------------------------

**Parent class:** ServiceInstance

Applied stereotypes:

-  Preliminary

-  OpenModelClass

-  **support: MANDATORY**

=================== ================ ========= ================================== ========================================================================================================================================================================================================================================================
**Attribute Name**  **Type**         **Mult.** **Stereotypes**                    **Description**
=================== ================ ========= ================================== ========================================================================================================================================================================================================================================================
\_resourceInstance  ResourceInstance 0..\*     OpenModelAttribute                 Resource instance components of constituting a service instance.
                                                                                 
                                               -  isInvariant: false             
                                                                                 
                                               -  valueRange: no range constraint
                                                                                 
                                               -  support: MANDATORY             
serviceInstanceId   Identifier       1         Preliminary                        Uniquely identifies this instance of a service.
                                                                                 
                                               OpenModelAttribute                
                                                                                 
                                               -  isInvariant: false             
                                                                                 
                                               -  valueRange: no range constraint
                                                                                 
                                               -  support: MANDATORY             
serviceInstanceName String           0..1      Preliminary                        The name assigned to the service-instance.
                                                                                 
                                               OpenModelAttribute                
                                                                                 
                                               -  isInvariant: false             
                                                                                 
                                               -  valueRange: no range constraint
                                                                                 
                                               -  support: OPTIONAL              
serviceType         String           0..1      Preliminary                        An optional string field defining a generic type (like category) of the service. E.g. this field can be used for defining the service as "TRANSPORT".
                                                                                 
                                               OpenModelAttribute                
                                                                                 
                                               -  isInvariant: false             
                                                                                 
                                               -  valueRange: no range constraint
                                                                                 
                                               -  support: MANDATORY             
serviceRole         String           1         Preliminary                        An optional string field for shortcode that defines the function that the service is providing. E.g. "MISVPN" or "AIM".
                                                                                 
                                               OpenModelAttribute                
                                                                                 
                                               -  isInvariant: false             
                                                                                 
                                               -  valueRange: no range constraint
                                                                                 
                                               -  support: MANDATORY             
selfLink            Uri              1         Preliminary                        URL to endpoint where more details can be gotten.
                                                                                 
                                               OpenModelAttribute                
                                                                                 
                                               -  isInvariant: false             
                                                                                 
                                               -  valueRange: no range constraint
                                                                                 
                                               -  support: MANDATORY             
orchestrationStatus String           1         Preliminary                        Orchestration status of the service instance.
                                                                                 
                                               OpenModelAttribute                
                                                                                 
                                               -  isInvariant: false             
                                                                                 
                                               -  valueRange: no range constraint
                                                                                 
                                               -  support: MANDATORY             
nsStatus            String           1         Preliminary                        Describe NS instance staus: instantiating(creating the Networek Service instance), active(the existed Network Service instance is under using), terminating(the existed Network Service instance stops using) or etc(healing and other possible status).
                                                                                 
                                               OpenModelAttribute                
                                                                                 
                                               -  isInvariant: false             
                                                                                 
                                               -  valueRange: no range constraint
                                                                                 
                                               -  support: MANDATORY             
=================== ================ ========= ================================== ========================================================================================================================================================================================================================================================

ServiceDescriptor
-----------------

ServiceDescriptor is used to model the design time representation of a
service.

Applied stereotypes:

-  Preliminary

-  OpenModelClass

-  **support: MANDATORY**

================== ========== ========= ================================== =====================================================================================================================================================
**Attribute Name** **Type**   **Mult.** **Stereotypes**                    **Description**
================== ========== ========= ================================== =====================================================================================================================================================
serviceInvariantId Identifier 1         Preliminary                        Constant identifier of the service model.
                                                                          
                                        OpenModelAttribute                
                                                                          
                                        -  isInvariant: false             
                                                                          
                                        -  valueRange: no range constraint
                                                                          
                                        -  support: MANDATORY             
serviceId          Identifier 1         Preliminary                        Versioned identifier of the service model (this uuid is changed for every major version of the service)
                                                                          
                                        OpenModelAttribute                
                                                                          
                                        -  isInvariant: false             
                                                                          
                                        -  valueRange: no range constraint
                                                                          
                                        -  support: MANDATORY             
name               String     1         Preliminary                        The name of the service model designed.
                                                                          
                                        OpenModelAttribute                
                                                                          
                                        -  isInvariant: false             
                                                                          
                                        -  valueRange: no range constraint
                                                                          
                                        -  support: MANDATORY             
description        String     1         Preliminary                        The description of the service model designed.
                                                                          
                                        OpenModelAttribute                
                                                                          
                                        -  isInvariant: false             
                                                                          
                                        -  valueRange: no range constraint
                                                                          
                                        -  support: MANDATORY             
category           String     1..\*     Preliminary                        A predefined list which identifies the construct's category. There is a predefined list of service categories.
                                                                          
                                        OpenModelAttribute                
                                                                          
                                        -  isInvariant: false             
                                                                          
                                        -  valueRange: no range constraint
                                                                          
                                        -  support: MANDATORY             
version            String     1         Preliminary                        The service model version.
                                                                          
                                        OpenModelAttribute                
                                                                          
                                        -  isInvariant: false             
                                                                          
                                        -  valueRange: no range constraint
                                                                          
                                        -  support: MANDATORY             
serviceType        String     0..1      Preliminary                        An optional string field defining a generic type (like category) of the service. E.g. this field can be used for defining the service as "TRANSPORT".
                                                                          
                                        OpenModelAttribute                
                                                                          
                                        -  isInvariant: false             
                                                                          
                                        -  valueRange: no range constraint
                                                                          
                                        -  support: MANDATORY             
serviceRole        String     0..1      Preliminary                        An optional string field for shortcode that defines the function that the service is providing. E.g. "MISVPN" or "AIM".
                                                                          
                                        OpenModelAttribute                
                                                                          
                                        -  isInvariant: false             
                                                                          
                                        -  valueRange: no range constraint
                                                                          
                                        -  support: MANDATORY             
icon               String     1         Preliminary                        The icon path of the service.
                                                                          
                                        OpenModelAttribute                
                                                                          
                                        -  isInvariant: false             
                                                                          
                                        -  valueRange: no range constraint
                                                                          
                                        -  support: MANDATORY             
================== ========== ========= ================================== =====================================================================================================================================================

ServiceInstance
---------------

ServiceInstance is used to model the run time representation of a
service.

Applied stereotypes:

-  Preliminary

-  OpenModelClass

-  **support: MANDATORY**

=================== ========== ========= ================================== ========================================================================================================================================================================================================================================================
**Attribute Name**  **Type**   **Mult.** **Stereotypes**                    **Description**
=================== ========== ========= ================================== ========================================================================================================================================================================================================================================================
serviceInstanceId   Identifier 1         Preliminary                        Uniquely identifies this instance of a service.
                                                                           
                                         OpenModelAttribute                
                                                                           
                                         -  isInvariant: false             
                                                                           
                                         -  valueRange: no range constraint
                                                                           
                                         -  support: MANDATORY             
serviceInstanceName String     0..1      Preliminary                        The name assigned to the service-instance.
                                                                           
                                         OpenModelAttribute                
                                                                           
                                         -  isInvariant: false             
                                                                           
                                         -  valueRange: no range constraint
                                                                           
                                         -  support: OPTIONAL              
serviceType         String     0..1      Preliminary                        An optional string field defining a generic type (like category) of the service. E.g. this field can be used for defining the service as "TRANSPORT".
                                                                           
                                         OpenModelAttribute                
                                                                           
                                         -  isInvariant: false             
                                                                           
                                         -  valueRange: no range constraint
                                                                           
                                         -  support: MANDATORY             
serviceRole         String     1         Preliminary                        An optional string field for shortcode that defines the function that the service is providing. E.g. "MISVPN" or "AIM".
                                                                           
                                         OpenModelAttribute                
                                                                           
                                         -  isInvariant: false             
                                                                           
                                         -  valueRange: no range constraint
                                                                           
                                         -  support: MANDATORY             
selfLink            Uri        1         Preliminary                        URL to endpoint where more details can be gotten.
                                                                           
                                         OpenModelAttribute                
                                                                           
                                         -  isInvariant: false             
                                                                           
                                         -  valueRange: no range constraint
                                                                           
                                         -  support: MANDATORY             
orchestrationStatus String     1         Preliminary                        Orchestration status of the service instance.
                                                                           
                                         OpenModelAttribute                
                                                                           
                                         -  isInvariant: false             
                                                                           
                                         -  valueRange: no range constraint
                                                                           
                                         -  support: MANDATORY             
nsStatus            String     1         Preliminary                        Describe NS instance staus: instantiating(creating the Networek Service instance), active(the existed Network Service instance is under using), terminating(the existed Network Service instance stops using) or etc(healing and other possible status).
                                                                           
                                         OpenModelAttribute                
                                                                           
                                         -  isInvariant: false             
                                                                           
                                         -  valueRange: no range constraint
                                                                           
                                         -  support: MANDATORY             
=================== ========== ========= ================================== ========================================================================================================================================================================================================================================================

.. |image0| image:: Nested Service final for Rst.png

