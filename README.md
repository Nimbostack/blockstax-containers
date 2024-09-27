# Blockstax Containers

## Overview

Blockstax-Containers is an open-source project by Nimbostack that provides Melange and Apko declarations for building container images for Permissioned Blockchain Network projects. While our long-term goal is to support multiple Blockchain projects, we currently focus on Hyperledger Fabric components. This project aims to simplify and standardize the process of creating container images for all the required images to create your network.

## 🌟 Features

- **Reproducible Builds**: Consistent environments across deployments
- **Enhanced Security**: Built-in best practices from the ground up
- **Customizable**: Easily modify build declarations for your needs
- **Community-Driven**: Open-source collaboration for continuous improvement
- **No Dockerfiles**: Eliminates the need for maintaining complex Dockerfiles

## 📁 Repository Structure

```
blockstax-containers/
├── fabric/
│   ├── peer/
│   ├── orderer/
│   ├── tools/
│   └── ca/
└── README.md
```

Currently, the repository contains subdirectories, each with Melange and Apko declarations for building the respective Blockchain network components. As we expand to support other Blockchain projects, new directories will be added.

## 🔧 How to Use

## 🛠️ Prerequisites

- [apko](https://edu.chainguard.dev/open-source/build-tools/apko/getting-started-with-apko/)
- [melange](https://edu.chainguard.dev/open-source/build-tools/melange/getting-started-with-melange/)
- [cosign](https://docs.sigstore.dev/signing/quickstart/#installation)
- [crane](https://github.com/google/go-containerregistry/tree/main/cmd/crane)

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

## 🔮 Future Plans

- Expand support to other Blockchain projects
- Provide unified tooling across various Blockchain platforms
- Foster cross-project innovation within the ecosystem

## 📄 License

This project is licensed under the Apache License 2.0 - see the [LICENSE](LICENSE) file for details.

## 🙏 Acknowledgements

- [Hyperledger Fabric](https://www.hyperledger.org/use/fabric)
- [Melange](https://github.com/chainguard-dev/melange)
- [Apko](https://github.com/chainguard-dev/apko)

⭐️ If you find this project useful, please consider giving it a star! ⭐️
