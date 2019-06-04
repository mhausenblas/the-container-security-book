{id: ch_containers}
# Containers

[containers](http://containerz.info/) including container images and how to build them (CI pipelines)

{id: basics-containers}
## Basics

![Linux containers are process groups using cgroups and namespaces](ch3_containers.png)

cgroups, namespaces, CoW file systems

{id: containers-runtimes}
## Container Runtimes

OCI runtime, containerd, etc.

seccomp, etc.

{id: containers-images}
## Container Images

OCI image, etc.

{id: containers-build}
## Building Container Images Securely

There are a number of [continuous integration](https://www.martinfowler.com/articles/continuousIntegration.html) tools available, including but not limited to the following: [Argo](https://argoproj.github.io/), AWS [CodePipeline](https://aws.amazon.com/codepipeline/), [CircleCI](https://www.circle.com/), [Codeship](http://codeship.com/), GitHub [Actions](https://jasonet.co/posts/use-github-actions-for-ci/), GitLab [Continuous Integration](https://about.gitlab.com/product/continuous-integration/), [Jenkins](https://jenkins.io/), [TeamCity](https://www.jetbrains.com/teamcity/), [Travis](https://travis-ci.org/), and shell scripts invoking `docker build`.

You could also have a look at [DockerSlim](https://dockersl.im) which promises not only to reduce the size of the container image but also to auto-generate SECCOMP and Apparmor profiles.

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

* Porteris
* ???

{id: gp-containers}
## Good Practices

{id: av-containers}
## Attack Vectors