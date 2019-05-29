.. Copyright 2019 (China Mobile)
.. This file is licensed under the CREATIVE COMMONS ATTRIBUTION 4.0 INTERNATIONAL LICENSE
.. Full license text at https://creativecommons.org/licenses/by/4.0/legalcode

Artifact Types
==============

| tosca.artifacts.nfv.SwImage: 
|   derived_from: tosca.artifacts.Deployment.Image
|   description: describes the software image which is directly loaded on the virtualisation container realizing of the VDU or is to be loaded on a virtual storage resource

| tosca.artifacts.Implementation.nfv.Mistral:
|  derived_from: tosca.artifacts.Implementation
|  description: artifacts for Mistral workflows
|  mime_type: application/x-yaml
|  file_ext: [ yaml ]

  