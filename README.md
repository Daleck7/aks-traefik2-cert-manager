# AKS + Traefik v2 + Cert-Manager

## Requirements 

- Azure Kuberetes Services 1.17.x
- Traefik v2.2
- Cert-Manager v1.0

## Deploy Azure Kubernetes Cluster

```
az aks create -g MyResourceGroup -n MyClusterName \
--kubernetes-version 1.17.9 \
--node-count 2 \
--node-vm-size Standard_D2s_v3
```
