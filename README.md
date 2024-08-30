## Kubeplugin

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
### Usage

Run the plugin using the following syntax:

   ```bash
   kubectl kubeplugin <namespace> <resource_type>

    <namespace>: The Kubernetes namespace to query (e.g., kube-system).
    <resource_type>: The type of resources to query (e.g., pods, nodes).
   ```
Example

   ```bash
   kubectl kubeplugin kube-system pod
   Resource        Namespace       Name                                               CPU        Memory    
   ----------------------------------------------------------------------------------------------------
   pod             kube-system     coredns-576bfc4dc7-97g4w                           3m         18Mi      
   pod             kube-system     local-path-provisioner-6795b5f9d8-g6jhg            1m         9Mi       
   pod             kube-system     metrics-server-557ff575fb-q6gml                    4m         32Mi      
   pod             kube-system     svclb-traefik-da01c7e4-r9z5g                       0m         0Mi       
   pod             kube-system     traefik-5fb479b77-cc5tq                            1m         29Mi  
   ```
![kubeplugin-demo](kubeplugin.gif)
