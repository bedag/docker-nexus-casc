<!-- - Copyright © 2021 Bedag Informatik AG Licensed under the Apache License, Version 2.0 (the "License"); you may not use this file except in compliance with the License. You may obtain a copy of the License at http://www.apache.org/licenses/LICENSE-2.0 Unless required by applicable law or agreed to in writing, software distributed under the License is distributed on an "AS IS" BASIS, WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied. See the License for the specific language governing permissions and limitations under the License. -->

# Nexus CASC Docker 

[![License](https://img.shields.io/badge/License-Apache%202.0-blue.svg)](https://opensource.org/licenses/Apache-2.0) ![docker-publish](https://github.com/bedag/docker-nexus-casc/workflows/docker-publish/badge.svg) [![Dockerhub](https://img.shields.io/docker/pulls/bedag/nexus-casc?style=plastic)](https://hub.docker.com/r/bedag/nexus-casc)

![Bedag](https://www.bedag.ch/wGlobal/wGlobal/layout/images/logo.svg)

This Docker image extends the [Sonatype Nexus3 Docker Image](https://hub.docker.com/r/sonatype/nexus3) with the Nexus plugin [CASC](https://github.com/AdaptiveConsulting/nexus-casc-plugin). This plugin allows to configure nexus with a declartive configuration file, which makes nexus more controllable for kubernetes deployments.

Feel free the create a new Issue if you have any problems with the image.

## Configuration

All the configuration are supported from the original images:

  * [https://hub.docker.com/r/sonatype/nexus3](https://hub.docker.com/r/sonatype/nexus3)
  * [https://github.com/AdaptiveConsulting/nexus-casc-plugin](https://github.com/AdaptiveConsulting/nexus-casc-plugin)

The Default configuration being used can be found [here](./nexus_default.yml). Mount your own Configuration under `/opt/nexus.yml`. You can also change the CASC Coonfig location via `NEXUS_CASC_CONFIG` environment variable.


## Build

Docker builds are created with [bedag/image-build](https://github.com/bedag/image-build).
Every Sunday(`0 0 * * SUN`) we automatically update all [supported tags](#Tags) with the current upstream image.

## Tags 

Supported tags are:

* `latest`
* `3.30.1`, `3.30.0`, `3.29.0`

## Security Notice 

Security scans are performed via [trivy](https://github.com/aquasecurity/trivy) and reported in [github](./security). Scans are only performed to the `latest` tag, which should include all libs vulnerabilities from all possible tags.

## Contributing

We'd love to have you contribute! Please refer to our [contribution guidelines](CONTRIBUTING.md) for details.

**By making a contribution to this project, you agree to and comply with the [Developer's Certificate of Origin](./DCO).**

## License

[Apache 2.0 License](./LICENSE).