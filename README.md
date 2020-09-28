# helmfiles
Helmfile is a manager for your helm releases.

## Prerequisites
* [Helm v3.2+](https://github.com/helm/helm/releases)
* [Helmfile](https://github.com/roboll/helmfile/releases)
* [Kustomize](https://kubectl.docs.kubernetes.io/pages/examples/kustomize.html)

## How-to
This helmfile management repository is implementing `helmfile.d` approach to manage helm releases across kubernetes cluster environment. The helm releases are separated across namespaces, you can take look on `helmfile.d/<namespace_name>`, and the chart values on `values.d/<namespace_name>/<release_name>`.

This repository also contains a helper command one of which is `helmize` to help helmfile managed the `kustomize` resources which could be seen on [bin/](bin/) directory. Thus helper command are intended to work with helmfile through hook [the helmfile events](https://github.com/roboll/helmfile#hooks).

## References
* [helmify-kustomize](https://gist.github.com/mumoshu/f9d0bd98e0eb77f636f79fc2fb130690)
* [helmfile - it's like helm for your helm!](https://medium.com/@naseem_60378/helmfile-its-like-a-helm-for-your-helm-74a908581599)