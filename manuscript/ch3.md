{id: ch_containers}
# Containers

[containers](http://containerz.info/) including container images and how to build them (CI pipelines)

{id: basics-containers}
## Basics

![Linux containers are process groups using cgroups and namespaces](ch3_containers.png)

cgroups, namespaces, CoW file systems
{id: security-basics}
### Security basics

### seccomp

`seccomp` or secure computing mode is a computer security facility in Linux kernel. `seccomp` introduces the capability of restricting system calls. The system call is a fundamental interface between an application and the Linux kernel. System calls are not invoked directly, but rather via wrapper functions like `glibc` (or perhaps some other library).

In relation to containers, `seccomp` profiles allows an overarching layer of security to restrict the interactions that a container can have with the kernel. `seccomp` is a lower level security control that can be used as a finer security mechanism within a defense in depth model for containers.

As an example, Docker has an [opinionated approach](https://docs.docker.com/engine/security/seccomp/) to `seccomp` where the default docker container runs with a set of whitelisted syscalls. Syscalls like `clone` and `mount` are blocked to prevent escalated privileges to the container processes and child processes.

### Capabilities

<More content on Capabilities to be added here in relation to the seccomp section above>

{id: containers-runtimes}
## Container Runtimes


The Open Container Initiative (OCI) is a lightweight, open governance structure, formed under the auspices of the Linux Foundation, for the express purpose of creating open industry standards around container formats and runtime.

Established in June 2015 by Docker, CoreOS and other leaders in the container industry, the OCI currently contains two specifications: the Runtime Specification ([runtime-spec](https://github.com/opencontainers/runtime-spec)) and the Image Specification ([image-spec](https://github.com/opencontainers/image-spec)). The Runtime Specification outlines how to run a “filesystem bundle” that is unpacked on disk. At a high-level an OCI implementation would download an OCI Image then unpack that image into an OCI Runtime filesystem bundle. At this point the OCI Runtime Bundle would be run by an OCI Runtime.

### runc

[`runc`](https://github.com/opencontainers/runc) is a tool for spawning and running containers according to the OCI specification. `runc` can be used to generate an OCI specification using the command below. runc provides a spec command to generate a base template spec that you are then able to edit. To find features and documentation for fields in the spec please refer to the specs repository.

### containerd and containerd-shim

[containerd](https://github.com/containerd/containerd) is an industry-standard container runtime with an emphasis on simplicity, robustness and portability. It is available as a daemon for Linux and Windows, which can manage the complete container lifecycle of its host system: image transfer and storage, container execution and supervision, low-level storage and network attachments.

### Ongoing efforts in container isolation - Kata Containers, FireCracker, gVisor and rust-vmm

<To add details and diagrams to explain the container isolation approaches by these projects>
{id: lsms}
## Linux Security Modules

### Security Enhanced Linux (SELinux)

### AppArmor

### Other LSMs

## Rootless Containers


{id: containers-images}
## Container Images

OCI image, etc.

https://blog.bitnami.com/2019/04/trusting-images-from-docker-hub.html

{id: containers-build}
## Building Container Images Securely

There are a number of [continuous integration](https://www.martinfowler.com/articles/continuousIntegration.html) 
tools and approaches available, including but not limited to the following:

- [Argo](https://argoproj.github.io/)
- AWS [CodePipeline](https://aws.amazon.com/codepipeline/)
- [CircleCI](https://www.circle.com/)
- [Codeship](http://codeship.com/)
- GitHub [Actions](https://jasonet.co/posts/use-github-actions-for-ci/)
- GitLab [Continuous Integration](https://about.gitlab.com/product/continuous-integration/)
- [Jenkins](https://jenkins.io/)
- [TeamCity](https://www.jetbrains.com/teamcity/)
- [Travis](https://travis-ci.org/)
- Shell scripts invoking `docker build` directly

You could also have a look at [DockerSlim](https://dockersl.im) which promises 
not only to reduce the size of the container image but also to auto-generate 
SECCOMP and Apparmor profiles.

As one would expect, there are a number of challenges in the context of 
[CI/CD pipelines](https://thenewstack.io/the-biggest-security-risks-lurking-in-your-ci-cd-pipeline).

{id: containers-delivery}
## Distributing Container Images Securely


{id: containers-registries}
### Using A Container Registry

Docker Hub, Quay, Harbor, ECR

{id: containers-cd}
### Continuous Delivery

In alphabetical order:

- [Argo](https://argoproj.github.io/)
- [Codefresh](https://codefresh.io/)
- [flagger](https://flagger.app/)
- [Gitkube](https://gitkube.sh/), for example, with [EKS](https://aws.amazon.com/blogs/opensource/git-push-deploy-app-eks-gitkube/))
- [Harness](https://harness.io/)
- [Razee](https://github.com/razee-io/Razee)
- [Spinnaker](https://www.spinnaker.io/)

TODO: create table comparing above offerings along: SaaS/OSS, security, model (pull/push), supports (Kube, others)

Notable: https://securityboulevard.com/2019/05/20-best-continuous-integration-tools-a-guide-to-optimizing-your-ci-cd-processes/

{id: containers-signing}
### Image Signing

#### TUF and Notary

https://www.youtube.com/watch?v=PSujE86JvBk

#### Tooling

* [Porteris](https://github.com/IBM/portieris), a Kubernetes admission controller for verifying image trust with Notary. 
* [Docker Content Trust (DCT)](https://docs.docker.com/engine/security/trust/content_trust/)

{id: tm-containers}
## Threat Model

{id: gp-containers}
## Good Practices