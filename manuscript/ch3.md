{id: ch_containers}
# Containers

[containers](http://containerz.info/) including container images and how to build them (CI pipelines)

{id: basics-containers}
## Basics

cgroups, namespaces

{id: security-basics}
### Security basics

### seccomp

`seccomp` or secure computing mode is a computer security facility in Linux kernel. `seccomp` introduces the capability of restricting system calls. The system call is a fundamental interface between an application and the Linux kernel. System calls are not invoked directly, but rather via wrapper functions like `glibc` (or perhaps some other library).

In relation to containers, `seccomp` profiles allows an overarching layer of security to restrict the interactions that a container can have with the kernel. `seccomp` is a lower level security control that can be used as a finer security mechanism within a defense in depth model for containers.

As an example, Docker has an [opinionated approach](https://docs.docker.com/engine/security/seccomp/) to `seccomp` where the default docker container runs with a set of whitelisted syscalls. Syscalls like `clone` and `mount` are blocked to prevent escalated privileges to the container processes and child processes.

### Capabilities

<More content on Capabilities to be added here in relation to the seccomp section above>

{id: containers-images}
## Container Images

{id: container-runtimes}
## Container Runtimes


runc, containerd, and RuntimeClass that can use kata, gVisor, Firecracker for better container isolation.


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
