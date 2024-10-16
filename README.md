# Terraform Configuration for KIND Kubernetes Cluster

This repository contains Terraform configuration to provision a KIND (Kubernetes IN Docker) cluster using the `tehcyx/kind` Terraform provider and manage it using the `gavinbunney/kubectl` provider.

## Prerequisites

Before using this configuration, ensure the following tools are installed:

- [Terraform](https://www.terraform.io/downloads.html) (vX.X.X or higher)
- Docker (KIND requires Docker to run the Kubernetes cluster inside containers)
- [kubectl](https://kubernetes.io/docs/tasks/tools/install-kubectl/) (for managing Kubernetes clusters)
- Properly configured Docker environment on your machine.

## Providers

This configuration uses the following providers:
- **KIND Provider** (`tehcyx/kind`): To create a Kubernetes cluster inside Docker using KIND.
- **Kubectl Provider** (`gavinbunney/kubectl`): To interact with the Kubernetes cluster created by KIND.

## Resources

### KIND Cluster
This configuration creates a Kubernetes cluster in Docker using KIND.

- **Cluster Name**: `sandbox`
- **Node Image**: `kindest/node:v1.23.4`
- **Nodes**:
  - 1 Control-plane node
  - 3 Worker nodes

### Cluster Configuration
The KIND configuration includes the following node roles:
- 1 control-plane node
- 3 worker nodes

## Usage

1. **Initialize Terraform**:
   Run the following command to initialize the working directory and download the necessary provider plugins:
   ```bash
   terraform init

