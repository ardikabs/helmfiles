# helmfiles
Helmfile is a Dockerfile for `helm` manifest.

## Prerequisites
* [Helm v3.2+](https://github.com/helm/helm/releases)
* [Helmfile](https://github.com/roboll/helmfile/releases)

## Apply `helmfile`
```bash
# EKS cluster
helmfile --environment eks -f clusters/eks apply

# KOPS cluster
helmfile --environment kops -f clusters/kops apply

# GKE cluster
helmfile --environment gke -f clusters/gke apply
```
