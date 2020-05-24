.. Copyright 2019
.. This file is licensed under the CREATIVE COMMONS ATTRIBUTION 4.0 INTERNATIONAL LICENSE
.. Full license text at https://creativecommons.org/licenses/by/4.0/legalcode

PnfdModel 
~~~~~~~~~

Classes
-------

Pnf
~~~

An implementation of a NF via a tightly coupled software and hardware system.

**Parent class:** NetworkFunction

Applied stereotypes:

-  Future

-  OpenModelClass

-  **support: MANDATORY**

================== ======== ========= ================================== ============================================
**Attribute Name** **Type** **Mult.** **Stereotypes**                    **Description**
================== ======== ========= ================================== ============================================
\_pnfExtCp         PnfExtCp 1..\*     OpenModelAttribute                 External CP of the PNF.
                                                                        
                                      -  isInvariant: false             
                                                                        
                                      -  valueRange: no range constraint
                                                                        
                                      -  support: MANDATORY             
id                 String   1         Experimental                       Identifier of the network function
                                                                        
                                      OpenModelAttribute                
                                                                        
                                      -  isInvariant: false             
                                                                        
                                      -  valueRange: no range constraint
                                                                        
                                      -  support: MANDATORY             
name               String   0..1      Experimental                      
                                                                        
                                      OpenModelAttribute                
                                                                        
                                      -  isInvariant: false             
                                                                        
                                      -  valueRange: no range constraint
                                                                        
                                      -  support: MANDATORY             
type               String   1         Experimental                       Description of the type of network function
                                                                        
                                      OpenModelAttribute                
                                                                        
                                      -  isInvariant: false             
                                                                        
                                      -  valueRange: no range constraint
                                                                        
                                      -  support: MANDATORY             
description        String   0..1      Experimental                       Description of the network function
                                                                        
                                      OpenModelAttribute                
                                                                        
                                      -  isInvariant: false             
                                                                        
                                      -  valueRange: no range constraint
                                                                        
                                      -  support: MANDATORY             
role               String   1         Experimental                       Role the network function will be providing.
                                                                        
                                      OpenModelAttribute                
                                                                        
                                      -  isInvariant: false             
                                                                        
                                      -  valueRange: no range constraint
                                                                        
                                      -  support: MANDATORY             
================== ======== ========= ================================== ============================================

PnfExtCp
~~~~~~~~

External CP of the PNF.

**Parent class:** Cp

Applied stereotypes:

-  Future

-  OpenModelClass

-  **support: MANDATORY**

================== ============= ========= ================================== ========================================================================================================================================================================
**Attribute Name** **Type**      **Mult.** **Stereotypes**                    **Description**
================== ============= ========= ================================== ========================================================================================================================================================================
cpd                invalid       1         OpenModelAttribute                 Cpd used to deploy this PNF CP.
                                                                             
                                           -  isInvariant: false             
                                                                             
                                           -  valueRange: no range constraint
                                                                             
                                           -  support: MANDATORY             
cpId               Identifier    1         OpenModelAttribute                 Identifier of the connection point instance.
                                                                             
                                           -  isInvariant: false             
                                                                             
                                           -  valueRange: no range constraint
                                                                             
                                           -  support: MANDATORY             
cpName             String        1         OpenModelAttribute                 Name of the Cp instance.
                                                                             
                                           -  isInvariant: false             
                                                                             
                                           -  valueRange: no range constraint
                                                                             
                                           -  support: MANDATORY             
cpNameAlt          String        1         OpenModelAttribute                 alternative name of the Cp instance.
                                                                             
                                           -  isInvariant: false             
                                                                             
                                           -  valueRange: no range constraint
                                                                             
                                           -  support: MANDATORY             
cpType             String        1         OpenModelAttribute                 Generic description of the type of Cp
                                                                             
                                           -  isInvariant: false             
                                                                             
                                           -  valueRange: no range constraint
                                                                             
                                           -  support: MANDATORY             
cpRole             String        1         OpenModelAttribute                 Role in the network this Cp will be providing
                                                                             
                                           -  isInvariant: false             
                                                                             
                                           -  valueRange: no range constraint
                                                                             
                                           -  support: MANDATORY             
cpFunction         String        1         OpenModelAttribute                 English description of the function this specific Cp will be providing
                                                                             
                                           -  isInvariant: false             
                                                                             
                                           -  valueRange: no range constraint
                                                                             
                                           -  support: MANDATORY             
cpDescription      String        1         OpenModelAttribute                 Cp description
                                                                             
                                           -  isInvariant: false             
                                                                             
                                           -  valueRange: no range constraint
                                                                             
                                           -  support: MANDATORY             
cpBandwidth        String        1         OpenModelAttribute                 Cp assigned (actual) bandwidth
                                                                             
                                           -  isInvariant: false              Cp (max? assigned?) bandwidth
                                                                             
                                           -  valueRange: no range constraint
                                                                             
                                           -  support: MANDATORY             
provStatus         String        1         OpenModelAttribute                 provisioning status, used as a trigger for operational monitoring of this resource by service assurance systems valid value example: PROVISIONED, PREPROVISIONED, CAPPED
                                                                             
                                           -  isInvariant: false             
                                                                             
                                           -  valueRange: no range constraint
                                                                             
                                           -  support: MANDATORY             
adminsStatus       String        1         OpenModelAttribute                 Administrative status of the connection point.
                                                                             
                                           -  isInvariant: false             
                                                                             
                                           -  valueRange: no range constraint
                                                                             
                                           -  support: MANDATORY             
protocol           String        1         OpenModelAttribute                 Protocol used by the Cp
                                                                             
                                           -  isInvariant: false             
                                                                             
                                           -  valueRange: no range constraint
                                                                             
                                           -  support: MANDATORY             
trunkMode          Boolean       1         OpenModelAttribute                 Indicator whether the Cp is in trunk mode
                                                                             
                                           -  isInvariant: false             
                                                                             
                                           -  valueRange: no range constraint
                                                                             
                                           -  support: MANDATORY             
addressType        String        1         OpenModelAttribute                 Type of address: MAC address or IP address
                                                                             
                                           -  isInvariant: false             
                                                                             
                                           -  valueRange: no range constraint
                                                                             
                                           -  support: MANDATORY             
L2addressData      L2AddressData 0..1      OpenModelAttribute                 Only present when addressType is MAC address
                                                                             
                                           -  isInvariant: false             
                                                                             
                                           -  valueRange: no range constraint
                                                                             
                                           -  support: MANDATORY             
L3addressData      L3AddressData 0..1      OpenModelAttribute                 Only present when addressType is IP address
                                                                             
                                           -  isInvariant: false             
                                                                             
                                           -  valueRange: no range constraint
                                                                             
                                           -  support: MANDATORY             
================== ============= ========= ================================== ========================================================================================================================================================================

PnfExtCpd
~~~~~~~~~

A PnfExtCpd is a type of Cpd and describes the characteristics of an external interface, a.k.a external CP, where to connect the PNF to a VL.

**Parent class:** ExtCpd

Applied stereotypes:

-  OpenModelClass

-  **support: MANDATORY**

-  Preliminary

PnfProfile
~~~~~~~~~~

The PnfProfile class describes additional data for a given PNF instance used in a DF.

Applied stereotypes:

-  Future

-  OpenModelClass

-  **support: MANDATORY**

========================== ========================= ========= ================================== ========================================================================================================================================
**Attribute Name**         **Type**                  **Mult.** **Stereotypes**                    **Description**
========================== ========================= ========= ================================== ========================================================================================================================================
pnfProfileId               Identifier                1         OpenModelAttribute                 Identifier of this PnfProfile class. It uniquely identifies a PnfProfile.
                                                                                                 
                                                               -  isInvariant: false             
                                                                                                 
                                                               -  valueRange: no range constraint
                                                                                                 
                                                               -  support: MANDATORY             
pnfVirtualLinkConnectivity NsVirtualLinkConnectivity 1..\*     OpenModelAttribute                 Defines the connection information of the PNF, it contains connection relationship between a PNF connection point and a NS virtual Link.
                                                                                                 
                                                               -  isInvariant: false             
                                                                                                 
                                                               -  valueRange: no range constraint
                                                                                                 
                                                               -  support: MANDATORY             
========================== ========================= ========= ================================== ========================================================================================================================================

Pnfd
~~~~

The Pnfd class is a deployment template enabling on-boarding PNFs and referencing them from an NSD. It focuses on connectivity aspects only.

**Parent class:** NetworkFunctionDesc

Applied stereotypes:

-  OpenModelClass

-  **support: MANDATORY**

-  Preliminary

=================== ================== ========= ================================== ====================================================================================================================
**Attribute Name**  **Type**           **Mult.** **Stereotypes**                    **Description**
=================== ================== ========= ================================== ====================================================================================================================
pnfdId              Identifier         1         OpenModelAttribute                 Identifier of this Pnfd class. It uniquely identifies the PNFD.
                                                                                   
                                                 -  isInvariant: false             
                                                                                   
                                                 -  valueRange: no range constraint
                                                                                   
                                                 -  support: MANDATORY             
                                                                                   
                                                 Preliminary                       
provider            String             1         OpenModelAttribute                 Identifies the provider of the PNFD. NOTE: The provider of the PNFD might be different from the provider of the PNF.
                                                                                   
                                                 -  isInvariant: false             
                                                                                   
                                                 -  valueRange: no range constraint
                                                                                   
                                                 -  support: MANDATORY             
                                                                                   
                                                 Preliminary                       
version             Version            1         OpenModelAttribute                 Identifies the version of the PNFD
                                                                                   
                                                 -  isInvariant: false             
                                                                                   
                                                 -  valueRange: no range constraint
                                                                                   
                                                 -  support: MANDATORY             
                                                                                   
                                                 Preliminary                       
security            SecurityParameters 0..1      OpenModelAttribute                 Provides a signature to prevent tampering.
                                                                                   
                                                 -  isInvariant: false             
                                                                                   
                                                 -  valueRange: no range constraint
                                                                                   
                                                 -  support: MANDATORY             
                                                                                   
                                                 Preliminary                       
functionDescription String             1         OpenModelAttribute                 Describes the PNF function.
                                                                                   
                                                 -  isInvariant: false             
                                                                                   
                                                 -  valueRange: no range constraint
                                                                                   
                                                 -  support: MANDATORY             
                                                                                   
                                                 Preliminary                       
pnfdInvariantId     Identifier         1         OpenModelAttribute                 Identifies a PNFD in a version independent manner. This attribute is invariant across versions of PNFD.
                                                                                   
                                                 -  isInvariant: true              
                                                                                   
                                                 -  valueRange: no range constraint
                                                                                   
                                                 -  support: MANDATORY             
                                                                                   
                                                 Preliminary                       
name                String             1         OpenModelAttribute                 Provides the human readable name of the PNFD.
                                                                                   
                                                 -  isInvariant: false             
                                                                                   
                                                 -  valueRange: no range constraint
                                                                                   
                                                 -  support: MANDATORY             
                                                                                   
                                                 Preliminary                       
\_pnfExtCpd         PnfExtCpd          1..\*     OpenModelAttribute                 Specifies the characteristics of one or more connection points where to connect the PNF to a VL.
                                                                                   
                                                 -  isInvariant: false             
                                                                                   
                                                 -  valueRange: no range constraint
                                                                                   
                                                 -  support: MANDATORY             
=================== ================== ========= ================================== ====================================================================================================================

Data Types
----------

SwVersion
~~~~~~~~~

The software versions associated with the pnfd

Applied stereotypes:

-  Future

================== ======== ========= ========== ================================== =====================
**Attribute Name** **Type** **Mult.** **Access** **Stereotypes**                    **Description**
================== ======== ========= ========== ================================== =====================
active             String   1         RW         OpenModelAttribute                 The active software
                                                                                   
                                                 -  isInvariant: false             
                                                                                   
                                                 -  valueRange: no range constraint
                                                                                   
                                                 -  support: MANDATORY             
passive            String   0..\*     RW         OpenModelAttribute                 The passive software
                                                                                   
                                                 -  isInvariant: false             
                                                                                   
                                                 -  valueRange: no range constraint
                                                                                   
                                                 -  support: MANDATORY             
recovery           String   0..\*     RW         OpenModelAttribute                 The recovery software
                                                                                   
                                                 -  isInvariant: false             
                                                                                   
                                                 -  valueRange: no range constraint
                                                                                   
                                                 -  support: MANDATORY             
================== ======== ========= ========== ================================== =====================