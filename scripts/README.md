## Kubeplugin Usage Instructions

### Description

The `kubeplugin` script is a custom `kubectl` plugin that provides CPU and memory usage statistics for Kubernetes resources in a specified namespace.

### Installation

1. Clone the repo and make the script executable:
   ```bash
   chmod +x scripts/kubeplugin
   ```
2. Move it to your PATH:
   ```bash
   sudo mv scripts/kubeplugin /usr/local/bin/kubectl-kubeplugin
   ```
Usage

Run the plugin using the following syntax:

   ```bash
   kubectl kubeplugin <namespace> <resource_type>

    <namespace>: The Kubernetes namespace to query (e.g., kube-system).
    <resource_type>: The type of resources to query (e.g., pods, nodes).

Example

   ```bash
   kubectl kubeplugin kube-system pods
   ```
