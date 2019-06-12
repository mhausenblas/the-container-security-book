{id: ch_containers}
# Containers

[containers](http://containerz.info/) including container images and how to build them (CI pipelines)

{id: basics-containers}
## Basics

cgroups, namespaces, seccomp
### seccomp

`seccomp` or secure computing mode is a computer security facility in Linux kernel. Seccomp monitors syscalls.


{id: containers-images}
### Container Runtimes
runc, containerd, and RuntimeClass that can use kata, gVisor, Firecracker for better container isolation.

## Container Images

{id: containers-build}
## Building Container Images Securely

{id: containers-delivery}
## Distributing Container Images Securely

{id: containers-registries}
### Using A Container Registry

Docker Hub, Quay, Harbor, ECR

{id: containers-cd}
### Continuous Delivery

GitOps/flagger, Spinnaker

{id: containers-signing}
### Image Signing

#### TUF and Notary

https://www.youtube.com/watch?v=PSujE86JvBk

#### Tooling

* Porteris
* ???

{id: gp-containers}
## Good Practices

{id: av-containers}
## Attack Vectors
