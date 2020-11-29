# AKS + Traefik v2 + Cert-Manager

## Requirements 

- Azure Kuberetes Services 1.17.x
- Traefik v2.2
- Cert-Manager v1.0

## Deploy Azure Kubernetes Cluster

```
az aks create -g MyResourceGroup -n MyClusterName \
--kubernetes-version 1.17.13 \
--node-count 2 \
--node-vm-size Standard_D2s_v3
```

## Deploy Traefik v2.3

```
kubectl apply -f ./traefik
```

## Deploy Cert-Manager 1.0

Installing manifests
```
kubectl apply --validate=false -f https://github.com/jetstack/cert-manager/releases/download/v1.0.4/cert-manager.yaml
```

Apply Let's Encrypt Cluster Issuer
```
kubectl apply -f ./cert-manager
```
