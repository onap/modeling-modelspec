.. Copyright 2018 (China Mobile)
.. This file is licensed under the CREATIVE COMMONS ATTRIBUTION 4.0 INTERNATIONAL LICENSE
.. Full license text at https://creativecommons.org/licenses/by/4.0/legalcode

Interface Types
===============

| **tosca.interfaces.nfv.vnf.lifecycle.Nfv**
|   derived_from: tosca.interfaces.Root 
|   instantiate:
|     description: Invoked upon receipt of an Instantiate VNF request
|   instantiate_start:
|     description: Invoked before instantiate
|   instantiate_end:
|     description: Invoked after instantiate
|   terminate:
|     description: Invoked upon receipt Terminate VNF request
|   terminate_start:
|     description: Invoked before terminate
|   terminate_end:
|     description: Invoked after terminate
|   modify_information:
|     description: Invoked upon receipt of a Modify VNF Information request
|   modify_information_start:
|     description: Invoked before modify_information
|   modify_information_end:
|     description: Invoked after modify_information
|   change_flavour:
|     description: Invoked upon receipt of a Change VNF Flavour request
|   change_flavour_start:
|     description: Invoked before change_flavour
|   change_flavour_end:
|     description: Invoked after change_flavour
|   change_external_connectivity:
|     description: Invoked upon receipt of a Change External VNF Connectivity request
|   change_external_connectivity_start:
|     description: Invoked before change_external_connectivity
|   change_external_connectivity_end:
|     description: Invoked after change_external_connectivity
|   operate:
|     description: Invoked upon receipt of an Operate VNF request
|   operate_start:
|     description: Invoked before operate
|   operate_end:
|     description: Invoked after operate
|   heal:
|     description: Invoked upon receipt of a Heal VNF request
|   heal_start:
|     description: Invoked before heal
|   heal_end:
|   description: Invoked after heal
|   scale:
|     description: Invoked upon receipt of a Scale VNF request
|   scale_start:
|     description: Invoked before scale
|   scale_end:
|     description: Invoked after scale  
|   scale_to_level:
|     description: Invoked upon receipt of a Scale VNF to Level request
| scale_to_level_start:
|     description: Invoked before scale_to_level
|   scale_to_level_end:
|     description: Invoked after scale_to_level
| #  indicator_changed:
| #    description: On receiving a VNF indicator value change notification