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

The Open Container Initiative (OCI) is a lightweight, open governance structure, formed under the auspices of the Linux Foundation, for the express purpose of creating open industry standards around container formats and runtime.

Established in June 2015 by Docker, CoreOS and other leaders in the container industry, the OCI currently contains two specifications: the Runtime Specification ([runtime-spec](https://github.com/opencontainers/runtime-spec)) and the Image Specification ([image-spec](https://github.com/opencontainers/image-spec)). The Runtime Specification outlines how to run a “filesystem bundle” that is unpacked on disk. At a high-level an OCI implementation would download an OCI Image then unpack that image into an OCI Runtime filesystem bundle. At this point the OCI Runtime Bundle would be run by an OCI Runtime.

### runc

[`runc`](https://github.com/opencontainers/runc) is a tool for spawning and running containers according to the OCI specification. `runc` can be used to generate an OCI specification using the command below. runc provides a spec command to generate a base template spec that you are then able to edit. To find features and documentation for fields in the spec please refer to the specs repository.

### containerd and containerd-shim

[containerd](https://github.com/containerd/containerd) is an industry-standard container runtime with an emphasis on simplicity, robustness and portability. It is available as a daemon for Linux and Windows, which can manage the complete container lifecycle of its host system: image transfer and storage, container execution and supervision, low-level storage and network attachments.


### Ongoing efforts in container isolation - Kata Containers, FireCracker, gVisor and rust-vmm

<To add details and diagrams to explain the container isolation approaches by these projects>


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
