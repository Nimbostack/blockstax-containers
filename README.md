# Blockstax Containers

## Overview

Blockstax-Containers is an open-source project by Nimbostack that provides Melange and Apko declarations for building container images for Permissioned Blockchain Network projects. While our long-term goal is to support multiple Blockchain projects, we currently focus on Hyperledger Fabric components. This project aims to simplify and standardize the process of creating container images for all the required images to create your network.

## Why This Approach?

1. **Reproducibility**: By using Melange and Apko, we ensure that the build process for Blockchain components is reproducible and consistent across different environments.

2. **Security**: This approach allows for better control over the container build process, enabling us to implement security best practices from the ground up.

3. **Customization**: Developers can easily modify the build declarations to suit their specific needs while maintaining compatibility with the official Blockchain repositories.

4. **Community Collaboration**: By open-sourcing this project, we invite the broader Permissioned Blockchain networks community to contribute, improve, and extend the capabilities of these container builds.

## Repository Structure

```
├── fabric/
│   ├── peer/
│   ├── orderer/
│   ├── tools/
│   └── ca/
```

Currently, the repository contains subdirectories, each with Melange and Apko declarations for building the respective Blockchain network components. As we expand to support other Blockchain projects, new directories will be added.

## How to Use

### Prerequisites:

- [apko](https://edu.chainguard.dev/open-source/build-tools/apko/getting-started-with-apko/).
- [melange](https://edu.chainguard.dev/open-source/build-tools/melange/getting-started-with-melange/).
- [cosign](https://docs.sigstore.dev/signing/quickstart/#installation).
- [crane](https://github.com/google/go-containerregistry/tree/main/cmd/crane).

### Quickstart

Before running the Melange Pipelines and Publishing/Building the applications with apko, you need to generate melange keys using (this assumes that the keys will be in the root of this directory):

```shell
 melange keygen
```

Each Blockchain project is represented by a directory containing all the components required to create the blockchain network. It is crucial to note that there is also a `Makefile` per component.

To package the components application you can run:

```shell
 make package
```

If you want to manually build the tarball for the packaged application, you can run:

```shell
 make build
```

To publish to your own container registry, you can either use:

```shell
 docker login
```

or

```shell
 apko login
```

### Signing your Images (Optional)

If you intend to sign your published images, you can use the following command to generate self-signed keys using cosign:

```shell
 cosign generate-key-pair
```

## Future Benefits for the Permissioned Blockchain Community

1. **Standardization**: This project aims to provide a standard approach to building containers for Open Source Blockchain projects, starting with Fabric. This will make it easier for organizations to adopt and maintain Private/Permissioned networks.

2. **Improved Security**: By focusing on the container build process, we can help improve the overall security posture of Cloud-Native Blockchain Network deployments.

3. **Faster Updates**: With a streamlined build process, the community can more quickly incorporate updates and security patches from official Blockchain Project repositories.

4. **Cross-Project Innovation**: As we expand to support multiple Blockchain projects, this initiative will foster innovation and knowledge sharing across different blockchain platforms within the ecosystem.

5. **Unified Tooling**: In the long term, we aim to provide a unified set of tools for building and managing containers across various Blockchain projects, simplifying the deployment and management of complex blockchain networks.

## Current Scope and Future Plans

While our current focus is on Hyperledger Fabric, we have plans to expand our support to other Blockchain projects in the future. This expansion will be driven by community needs and contributions. We encourage users and contributors to suggest and help implement support for additional Open Source Blockchain projects.
