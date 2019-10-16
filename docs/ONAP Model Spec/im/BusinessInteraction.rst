.. Copyright 2019
.. This file is licensed under the CREATIVE COMMONS ATTRIBUTION 4.0 INTERNATIONAL LICENSE
.. Full license text at https://creativecommons.org/licenses/by/4.0/legalcode

Business Interaction Model
==========================

.. contents::
   :depth: 3
..

Class Definition
----------------

BusinessInteractionItemRelationship class
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

**Qualified Name:** Common::Business Interaction::ObjectClasses:: BusinessInteractionItemRelationship

**Applied Stereotypes:**

-  OpenModelClass

-  support: MANDATORY

-  Preliminary

-  Reference

-  reference: From TMF SID

**Table** **Attributes for Class BusinessInteractionItemRelationship**

================== ========== ========= ===================================================== =====================
**Attribute Name** **Type**   **Mult.** **Description**                                       **Stereotypes**
================== ========== ========= ===================================================== =====================
type               String     1         The type of relationship such as contains, relies on. OpenModelAttribute
                                                                                             
                                                                                              -  partOfObjectKey: 0
                                                                                             
                                                                                              -  uniqueSet:
                                                                                             
                                                                                              -  isInvariant: false
                                                                                             
                                                                                              -  unsigned: false
                                                                                             
                                                                                              -  counter: NA
                                                                                             
                                                                                              -  support: MANDATORY
                                                                                             
                                                                                              Preliminary
validFor           TimePeriod 1         Time period for which the relationship is valid       OpenModelAttribute
                                                                                             
                                                                                              -  partOfObjectKey: 0
                                                                                             
                                                                                              -  uniqueSet:
                                                                                             
                                                                                              -  isInvariant: false
                                                                                             
                                                                                              -  unsigned: false
                                                                                             
                                                                                              -  counter: NA
                                                                                             
                                                                                              -  support: MANDATORY
                                                                                             
                                                                                              Preliminary
================== ========== ========= ===================================================== =====================

Agreement class
^^^^^^^^^^^^^^^

**Qualified Name:** Common::Business Interaction::ObjectClasses::Agreement

**Description:**

A type of BusinessInteraction that represents a contract or arrangement, either written or verbal and sometimes enforceable by law.

**Parent class:** BusinessInteraction

**Applied Stereotypes:**

-  OpenModelClass

-  support: MANDATORY

-  Preliminary

-  Reference

-  reference: From TMF SID

**Table** **Attributes for class Agreement**

================== ========== ========= ====================================================================================================================================================================================================================================================================================================================================================================== =====================
**Attribute Name** **Type**   **Mult.** **Description**                                                                                                                                                                                                                                                                                                                                                        **Stereotypes**
================== ========== ========= ====================================================================================================================================================================================================================================================================================================================================================================== =====================
documentNumber     String     1         A reference number assigned to an Agreement that follows a prescribed numbering system.                                                                                                                                                                                                                                                                                OpenModelAttribute
                                                                                                                                                                                                                                                                                                                                                                                                              
                                                                                                                                                                                                                                                                                                                                                                                                               -  partOfObjectKey: 0
                                                                                                                                                                                                                                                                                                                                                                                                              
                                                                                                                                                                                                                                                                                                                                                                                                               -  uniqueSet:
                                                                                                                                                                                                                                                                                                                                                                                                              
                                                                                                                                                                                                                                                                                                                                                                                                               -  isInvariant: false
                                                                                                                                                                                                                                                                                                                                                                                                              
                                                                                                                                                                                                                                                                                                                                                                                                               -  unsigned: false
                                                                                                                                                                                                                                                                                                                                                                                                              
                                                                                                                                                                                                                                                                                                                                                                                                               -  counter: NA
                                                                                                                                                                                                                                                                                                                                                                                                              
                                                                                                                                                                                                                                                                                                                                                                                                               -  support: MANDATORY
                                                                                                                                                                                                                                                                                                                                                                                                              
                                                                                                                                                                                                                                                                                                                                                                                                               Preliminary
statementOfIntent  String     1         An overview and goals of the Agreement.                                                                                                                                                                                                                                                                                                                                OpenModelAttribute
                                                                                                                                                                                                                                                                                                                                                                                                              
                                                                                                                                                                                                                                                                                                                                                                                                               -  partOfObjectKey: 0
                                                                                                                                                                                                                                                                                                                                                                                                              
                                                                                                                                                                                                                                                                                                                                                                                                               -  uniqueSet:
                                                                                                                                                                                                                                                                                                                                                                                                              
                                                                                                                                                                                                                                                                                                                                                                                                               -  isInvariant: false
                                                                                                                                                                                                                                                                                                                                                                                                              
                                                                                                                                                                                                                                                                                                                                                                                                               -  unsigned: false
                                                                                                                                                                                                                                                                                                                                                                                                              
                                                                                                                                                                                                                                                                                                                                                                                                               -  counter: NA
                                                                                                                                                                                                                                                                                                                                                                                                              
                                                                                                                                                                                                                                                                                                                                                                                                               -  support: MANDATORY
                                                                                                                                                                                                                                                                                                                                                                                                              
                                                                                                                                                                                                                                                                                                                                                                                                               Preliminary
StartDate          DateTime   1         Date interaction initiated                                                                                                                                                                                                                                                                                                                                             OpenModelAttribute
                                                                                                                                                                                                                                                                                                                                                                                                              
                                                                                                                                                                                                                                                                                                                                                                                                               -  partOfObjectKey: 0
                                                                                                                                                                                                                                                                                                                                                                                                              
                                                                                                                                                                                                                                                                                                                                                                                                               -  uniqueSet:
                                                                                                                                                                                                                                                                                                                                                                                                              
                                                                                                                                                                                                                                                                                                                                                                                                               -  isInvariant: false
                                                                                                                                                                                                                                                                                                                                                                                                              
                                                                                                                                                                                                                                                                                                                                                                                                               -  unsigned: false
                                                                                                                                                                                                                                                                                                                                                                                                              
                                                                                                                                                                                                                                                                                                                                                                                                               -  counter: NA
                                                                                                                                                                                                                                                                                                                                                                                                              
                                                                                                                                                                                                                                                                                                                                                                                                               -  support: MANDATORY
                                                                                                                                                                                                                                                                                                                                                                                                              
                                                                                                                                                                                                                                                                                                                                                                                                               Preliminary
endDate            DateTime   1         The date on which an interaction is closed or completed.                                                                                                                                                                                                                                                                                                               OpenModelAttribute
                                                                                                                                                                                                                                                                                                                                                                                                              
                                                                                                                                                                                                                                                                                                                                                                                                               -  partOfObjectKey: 0
                                                                                                                                                                                                                                                                                                                                                                                                              
                                                                                                                                                                                                                                                                                                                                                                                                               -  uniqueSet:
                                                                                                                                                                                                                                                                                                                                                                                                              
                                                                                                                                                                                                                                                                                                                                                                                                               -  isInvariant: false
                                                                                                                                                                                                                                                                                                                                                                                                              
                                                                                                                                                                                                                                                                                                                                                                                                               -  unsigned: false
                                                                                                                                                                                                                                                                                                                                                                                                              
                                                                                                                                                                                                                                                                                                                                                                                                               -  counter: NA
                                                                                                                                                                                                                                                                                                                                                                                                              
                                                                                                                                                                                                                                                                                                                                                                                                               -  support: MANDATORY
                                                                                                                                                                                                                                                                                                                                                                                                              
                                                                                                                                                                                                                                                                                                                                                                                                               Preliminary
Status             String     0..1      The current condition of an interaction, such as open, in research, closed, and so forth                                                                                                                                                                                                                                                                               OpenModelAttribute
                                                                                                                                                                                                                                                                                                                                                                                                              
                                                                                                                                                                                                                                                                                                                                                                                                               -  partOfObjectKey: 0
                                                                                                                                                                                                                                                                                                                                                                                                              
                                                                                                                                                                                                                                                                                                                                                                                                               -  uniqueSet:
                                                                                                                                                                                                                                                                                                                                                                                                              
                                                                                                                                                                                                                                                                                                                                                                                                               -  isInvariant: false
                                                                                                                                                                                                                                                                                                                                                                                                              
                                                                                                                                                                                                                                                                                                                                                                                                               -  unsigned: false
                                                                                                                                                                                                                                                                                                                                                                                                              
                                                                                                                                                                                                                                                                                                                                                                                                               -  counter: NA
                                                                                                                                                                                                                                                                                                                                                                                                              
                                                                                                                                                                                                                                                                                                                                                                                                               -  support: MANDATORY
                                                                                                                                                                                                                                                                                                                                                                                                              
                                                                                                                                                                                                                                                                                                                                                                                                               Preliminary
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

BusinessInteraction class
^^^^^^^^^^^^^^^^^^^^^^^^^

**Qualified Name:** Common::Business Interaction::ObjectClasses::BusinessInteraction

**Description:**

A BusinessInteraction is an arrangement, contract, communication or joint activity between one or more PartyRoles, ResourceRoles, or CustomerAccounts. A BusinessInteraction may consist of one or more BusinessInteractionItems. A BusinessInteractionItem may refer to a Product, Service, Resource, or one of their specifications. A BusinessInteraction is further defined by one or more Places. One BusinessInteraction may reference another BusinessInteraction and one BusinessInteractionItem may reference another BusinessInteractionItem on the same or different BusinessInteraction. Types of BusinessInteractions include : Requests, Responses, Notifications, and Agreements.

This class is abstract.

**Parent class:** RootEntity

**Applied Stereotypes:**

-  OpenModelClass

-  support: MANDATORY

-  Preliminary

-  Reference

-  reference: From TMF SID

**Table** **Attributes for class BusinessInteraction**

================== ========== ========= ====================================================================================================================================================================================================================================================================================================================================================================== =====================
**Attribute Name** **Type**   **Mult.** **Description**                                                                                                                                                                                                                                                                                                                                                        **Stereotypes**
================== ========== ========= ====================================================================================================================================================================================================================================================================================================================================================================== =====================
StartDate          DateTime   1         Date interaction initiated                                                                                                                                                                                                                                                                                                                                             OpenModelAttribute
                                                                                                                                                                                                                                                                                                                                                                                                              
                                                                                                                                                                                                                                                                                                                                                                                                               -  partOfObjectKey: 0
                                                                                                                                                                                                                                                                                                                                                                                                              
                                                                                                                                                                                                                                                                                                                                                                                                               -  uniqueSet:
                                                                                                                                                                                                                                                                                                                                                                                                              
                                                                                                                                                                                                                                                                                                                                                                                                               -  isInvariant: false
                                                                                                                                                                                                                                                                                                                                                                                                              
                                                                                                                                                                                                                                                                                                                                                                                                               -  unsigned: false
                                                                                                                                                                                                                                                                                                                                                                                                              
                                                                                                                                                                                                                                                                                                                                                                                                               -  counter: NA
                                                                                                                                                                                                                                                                                                                                                                                                              
                                                                                                                                                                                                                                                                                                                                                                                                               -  support: MANDATORY
                                                                                                                                                                                                                                                                                                                                                                                                              
                                                                                                                                                                                                                                                                                                                                                                                                               Preliminary
endDate            DateTime   1         The date on which an interaction is closed or completed.                                                                                                                                                                                                                                                                                                               OpenModelAttribute
                                                                                                                                                                                                                                                                                                                                                                                                              
                                                                                                                                                                                                                                                                                                                                                                                                               -  partOfObjectKey: 0
                                                                                                                                                                                                                                                                                                                                                                                                              
                                                                                                                                                                                                                                                                                                                                                                                                               -  uniqueSet:
                                                                                                                                                                                                                                                                                                                                                                                                              
                                                                                                                                                                                                                                                                                                                                                                                                               -  isInvariant: false
                                                                                                                                                                                                                                                                                                                                                                                                              
                                                                                                                                                                                                                                                                                                                                                                                                               -  unsigned: false
                                                                                                                                                                                                                                                                                                                                                                                                              
                                                                                                                                                                                                                                                                                                                                                                                                               -  counter: NA
                                                                                                                                                                                                                                                                                                                                                                                                              
                                                                                                                                                                                                                                                                                                                                                                                                               -  support: MANDATORY
                                                                                                                                                                                                                                                                                                                                                                                                              
                                                                                                                                                                                                                                                                                                                                                                                                               Preliminary
Status             String     0..1      The current condition of an interaction, such as open, in research, closed, and so forth                                                                                                                                                                                                                                                                               OpenModelAttribute
                                                                                                                                                                                                                                                                                                                                                                                                              
                                                                                                                                                                                                                                                                                                                                                                                                               -  partOfObjectKey: 0
                                                                                                                                                                                                                                                                                                                                                                                                              
                                                                                                                                                                                                                                                                                                                                                                                                               -  uniqueSet:
                                                                                                                                                                                                                                                                                                                                                                                                              
                                                                                                                                                                                                                                                                                                                                                                                                               -  isInvariant: false
                                                                                                                                                                                                                                                                                                                                                                                                              
                                                                                                                                                                                                                                                                                                                                                                                                               -  unsigned: false
                                                                                                                                                                                                                                                                                                                                                                                                              
                                                                                                                                                                                                                                                                                                                                                                                                               -  counter: NA
                                                                                                                                                                                                                                                                                                                                                                                                              
                                                                                                                                                                                                                                                                                                                                                                                                               -  support: MANDATORY
                                                                                                                                                                                                                                                                                                                                                                                                              
                                                                                                                                                                                                                                                                                                                                                                                                               Preliminary
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

BusinessInteractionItem class
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

**Qualified Name:** Common::Business Interaction::ObjectClasses::BusinessInteractionItem

**Description:**

The purpose for the BusinessInteraction expressed in terms of a ProductSpecification, ProductOffering, ServiceSpecification or ResourceSpecification or may refer to a Product, Service, or Resource.

This class is abstract.

**Applied Stereotypes:**

-  OpenModelClass

-  support: MANDATORY

-  Preliminary

-  Reference

-  reference: From TMF SID

**Table** **Attributes for class BusinessInteractionItem**

================== ======== ========= ======================================================================= =====================
**Attribute Name** **Type** **Mult.** **Description**                                                         **Stereotypes**
================== ======== ========= ======================================================================= =====================
quantity           Integer  1         Quantity of an interaction item involved in an interaction.             OpenModelAttribute
                                                                                                             
                                                                                                              -  partOfObjectKey: 0
                                                                                                             
                                                                                                              -  uniqueSet:
                                                                                                             
                                                                                                              -  isInvariant: false
                                                                                                             
                                                                                                              -  unsigned: false
                                                                                                             
                                                                                                              -  counter: NA
                                                                                                             
                                                                                                              -  support: MANDATORY
                                                                                                             
                                                                                                              Preliminary
action             String   1         The action to take for an InteractionItem, such as add, change, remove. OpenModelAttribute
                                                                                                             
                                                                                                              -  partOfObjectKey: 0
                                                                                                             
                                                                                                              -  uniqueSet:
                                                                                                             
                                                                                                              -  isInvariant: false
                                                                                                             
                                                                                                              -  unsigned: false
                                                                                                             
                                                                                                              -  counter: NA
                                                                                                             
                                                                                                              -  support: MANDATORY
                                                                                                             
                                                                                                              Preliminary
================== ======== ========= ======================================================================= =====================

BusinessInteractionRelationship class
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

**Qualified Name:** Common::Business Interaction::ObjectClasses::BusinessInteractionRelationship

**Description:**

An association between two Interactions. For example, a Notification sent to customers affected by a problem contained on a Trouble Report; a response to a request, an agreement and the interactions that led up to the agreement.

**Applied Stereotypes:**

-  OpenModelClass

-  support: MANDATORY

-  Preliminary

-  Reference

-  reference: From TMF SID

**Table** **Attributes for class BusinessInteractionRelationship**

================== ========== ========= =============================================================================== =====================
**Attribute Name** **Type**   **Mult.** **Description**                                                                 **Stereotypes**
================== ========== ========= =============================================================================== =====================
type               String     1         A categorization of the relationship, such as bulk, parent/child, and so forth. OpenModelAttribute
                                                                                                                       
                                                                                                                        -  partOfObjectKey: 0
                                                                                                                       
                                                                                                                        -  uniqueSet:
                                                                                                                       
                                                                                                                        -  isInvariant: false
                                                                                                                       
                                                                                                                        -  unsigned: false
                                                                                                                       
                                                                                                                        -  counter: NA
                                                                                                                       
                                                                                                                        -  support: MANDATORY
                                                                                                                       
                                                                                                                        Preliminary
validFor           TimePeriod 1         Time period for which the relationship is valid                                 OpenModelAttribute
                                                                                                                       
                                                                                                                        -  partOfObjectKey: 0
                                                                                                                       
                                                                                                                        -  uniqueSet:
                                                                                                                       
                                                                                                                        -  isInvariant: false
                                                                                                                       
                                                                                                                        -  unsigned: false
                                                                                                                       
                                                                                                                        -  counter: NA
                                                                                                                       
                                                                                                                        -  support: MANDATORY
                                                                                                                       
                                                                                                                        Preliminary
================== ========== ========= =============================================================================== =====================

BusinessInteractionSpec class
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

**Qualified Name:** Common::Business Interaction::ObjectClasses::BusinessInteractionSpec

**Description:**

The invariant characteristics (attributes in the business view, and methods, constraints, relationships, and behavior in the system view) and behavior of a BusinessInteraction. This is done by optionally defining a set of BusinessInteractionSpecItems, each of which aggregates one or more other types of Specifications. This helps to ensure that different BusinessInteractions have the same basic characteristics and behavior by deriving them from the same BusinessInteractionSpec.

**Applied Stereotypes:**

-  OpenModelClass

-  support: MANDATORY

-  Preliminary

-  Reference

-  reference: From TMF SID

BusinessInteractionVersion class
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

**Qualified Name:** Common::Business Interaction::ObjectClasses::BusinessInteractionVersion

**Description:**

Version of the business interaction.

**Applied Stereotypes:**

-  OpenModelClass

-  support: MANDATORY

-  Preliminary

-  Reference

-  reference: From TMF SID

Notification class
^^^^^^^^^^^^^^^^^^

**Qualified Name:** Common::Business Interaction::ObjectClasses::Notification

**Description:**

A communication that informs about something that has or will happen. A Notification is typically one-sided, in that no Response is expected. A Notification can be created as the result of a Request; for example, a Trouble Report may result in Notifications being sent to affected Parties. A Notification is a type of Business Interaction.

This class is abstract.

**Parent class:** BusinessInteraction

**Applied Stereotypes:**

-  OpenModelClass

-  support: MANDATORY

-  Preliminary

-  Reference

-  reference: From the TMF SID

Request class
^^^^^^^^^^^^^

**Qualified Name:** Common::Business Interaction::ObjectClasses::Request

**Description:**

The act of asking that something be done that typically involves a Response. Request is a type of Business Interaction.

This class is abstract.

**Parent class:** BusinessInteraction

**Applied Stereotypes:**

-  OpenModelClass

-  support: MANDATORY

-  Preliminary

-  Reference

-  reference: From the TMF SID

Response class
^^^^^^^^^^^^^^

**Qualified Name:** Common::Business Interaction::ObjectClasses::Response

**Description:**

A reply to a Request

This class is abstract.

**Parent class:** BusinessInteraction

**Applied Stereotypes:**

-  OpenModelClass

-  support: MANDATORY

-  Preliminary

-  Reference

-  reference: From the TMF SID
