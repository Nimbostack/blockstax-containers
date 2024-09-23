# Hyperledger Fabric Tools By Nimbostack

## Overview

NimboStack provides custom-built Hyperledger Fabric images using Melange and Apko. These images are designed to offer enhanced security, reduced size, and improved performance for Hyperledger Fabric deployments.

## What is Hyperledger Fabric Tools?

The Hyperledger Fabric CLI tools allow you to interact with deployed chaincode, submit transactions, and perform various administrative tasks related to your Fabric network.

## Usage

To use a NimboStack Hyperledger Fabric Tools image in your project, specify the desired version in your Docker commands or Kubernetes manifests:

```bash
docker pull nimbostack/hyperledger-fabric-tools:2.5.0
```

## Why use Nimbostack Images?

- Security-focused: Built using Melange and Apko, our images prioritize security from the ground up.
- Minimized attack surface: Stripped-down images contain only essential components, reducing potential vulnerabilities.
- Smaller footprint: Optimized image sizes lead to faster downloads, reduced storage costs, and quicker container start times.
- Reproducible builds: Our build process ensures consistency and traceability across image versions.

## Supported tags

NimboStack Hyperledger Fabric Tools images are available starting from version 2.5.0. Supported tags include:

- `2.5.0`

## Issues

These images are provided under the Apache License 2.0. See the LICENSE file for more details.
