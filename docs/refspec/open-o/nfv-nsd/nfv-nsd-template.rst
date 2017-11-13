.. contents::
   :depth: 3
..

========================================================================

Copyright 2017 ZTE Corporation.

Licensed under the Apache License, Version 2.0 (the "License");

you may not use this file except in compliance with the License.

You may obtain a copy of the License at

    http://www.apache.org/licenses/LICENSE-2.0

Unless required by applicable law or agreed to in writing, software

distributed under the License is distributed on an "AS IS" BASIS,

WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.

See the License for the specific language governing permissions and

limitations under the License.

========================================================================

1.nfv-nsd type definiton include three layer profile definitions.

    A.simple tosca profle    : tosca_definition_1.0.yaml
      refer: http://docs.oasis-open.org/tosca/TOSCA-Simple-Profile-YAML/v1.0/os/TOSCA-Simple-Profile-YAML-v1.0-os.docx

    B.tosca nfv profile      : TOSCA_definition_nfv_ns_1_0.yaml
      refer: http://docs.oasis-open.org/tosca/tosca-nfv/v1.0/csd03/tosca-nfv-v1.0-csd03.doc

    C.openo extension profile: TOSCA_definition_ns_ext_1_0.yaml
      refer: Open-O definition

2.nfv-nsd service template should import the profiles above.
