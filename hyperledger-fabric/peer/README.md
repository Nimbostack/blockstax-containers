# Hyperledger Fabric Peer By Nimbostack

## Overview

NimboStack provides custom-built Hyperledger Fabric images using Melange and Apko. These images are designed to offer enhanced security, reduced size, and improved performance for Hyperledger Fabric deployments.

## What is Hyperledger Fabric Peer?

> A fundamental element of a Hyperledger Fabric blockchain network is the set of peer nodes (or, simply, peers). Peers are fundamental because they manage ledgers and smart contracts.

[Hyperledger Fabric Peer Key Concepts](https://hyperledger-fabric.readthedocs.io/en/latest/peers/peers.html)

## Usage

To use a NimboStack Hyperledger Fabric Peer image in your project, specify the desired version in your Docker commands or Kubernetes manifests:

```bash
docker pull nimbostack/hyperledger-fabric-peer:<TAG>
```

## Why use Nimbostack Images?

- Security-focused: Built using Melange and Apko, our images prioritize security from the ground up.
- Minimized attack surface: Stripped-down images contain only essential components, reducing potential vulnerabilities.
- Smaller footprint: Optimized image sizes lead to faster downloads, reduced storage costs, and quicker container start times.
- Reproducible builds: Our build process ensures consistency and traceability across image versions.

## Supported tags

NimboStack Hyperledger Fabric Peer images are available starting from version 2.5.0. Supported tags include:

- `2.5.0`
- `2.5.10`
- `3.0.0`

## Issues

These images are provided under the Apache License 2.0. See the LICENSE file for more details.
