# golint build step for Google Container Builder

code was lifted from https://github.com/GoogleCloudPlatform/cloud-builders/tree/master/go
and slightly modified to install golint and call it

# cloudbuild.yaml

substitute your package below (use go import path) and use like so:

```yaml
steps:
- name: 'vitraum/golint-cloud-builder'
  env: ['PROJECT_ROOT=<<PACKAGE>>']
- name: 'vitraum/golint-cloud-builder'
  cmd: '/builder/govet.ash'
  env: ['PROJECT_ROOT=<<PACKAGE>>']
```

## LICENSE

Copyright 2016 Google, Inc. All rights reserved.

Licensed under the Apache License, Version 2.0 (the "License");
you may not use this file except in compliance with the License.
You may obtain a copy of the License at

   http://www.apache.org/licenses/LICENSE-2.0

Unless required by applicable law or agreed to in writing, software
distributed under the License is distributed on an "AS IS" BASIS,
WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
See the License for the specific language governing permissions and
limitations under the License.
