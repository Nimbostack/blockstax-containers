# Hyperledger Fabric Orderer By Nimbostack

## Overview

NimboStack provides custom-built Hyperledger Fabric images using Melange and Apko. These images are designed to offer enhanced security, reduced size, and improved performance for Hyperledger Fabric deployments.

## What is Hyperledger Fabric Orderer?

> Hyperledger features a node called an orderer (it’s also known as an “ordering node”) that does transaction ordering, which along with other orderer nodes forms an ordering service.

[Hyperledger Fabric Ordering Service Key Concepts](https://hyperledger-fabric.readthedocs.io/en/latest/orderer/ordering_service.html)

## Usage

To use a NimboStack Hyperledger Fabric Orderer image in your project, specify the desired version in your Docker commands or Kubernetes manifests:

```bash
docker pull nimbostack/hyperledger-fabric-orderer:2.5.0
```

## Why use Nimbostack Images?

- Security-focused: Built using Melange and Apko, our images prioritize security from the ground up.
- Minimized attack surface: Stripped-down images contain only essential components, reducing potential vulnerabilities.
- Smaller footprint: Optimized image sizes lead to faster downloads, reduced storage costs, and quicker container start times.
- Reproducible builds: Our build process ensures consistency and traceability across image versions.

## Supported tags

NimboStack Hyperledger Fabric Orderer images are available starting from version 2.5.0. Supported tags include:

- `2.5.0`

## Issues

These images are provided under the Apache License 2.0. See the LICENSE file for more details.
