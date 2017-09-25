#
# Copyright 2017 ZTE Corporation.
#
# Licensed under the Apache License, Version 2.0 (the "License");
# you may not use this file except in compliance with the License.
# You may obtain a copy of the License at
#
#         http://www.apache.org/licenses/LICENSE-2.0
#
# Unless required by applicable law or agreed to in writing, software
# distributed under the License is distributed on an "AS IS" BASIS,
# WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
# See the License for the specific language governing permissions and
# limitations under the License.
#

1.nfv vnfd type definiton include three layer profile definitions.

	A.simple tosca profle    : tosca_definition_1.0.yaml
                            refer:http://docs.oasis-open.org/tosca/TOSCA-Simple-Profile-YAML/v1.0/os/TOSCA-Simple-Profile-YAML-v1.0-os.docx

	B.tosca nfv profile      : tosca-simple-nfv-1.1.yaml
                            refer: draft-tosca-nfv-v1.0-wd04-rev06.doc

	C.openo extension profile: In the future

2.nfv vnfd service template should import the profiles above.