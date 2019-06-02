{id: ch_containers}
# Containers

[containers](http://containerz.info/) including container images and how to build them (CI pipelines)

{id: basics-containers}
## Basics

cgroups, namespaces, seccomp

{id: containers-images}
## Container Images

{id: containers-build}
## Building Container Images Securely

There are a number of [continuous integration](https://www.martinfowler.com/articles/continuousIntegration.html) tools available, including but not limited to the following: [Argo](https://argoproj.github.io/), AWS [CodePipeline](https://aws.amazon.com/codepipeline/), [CircleCI](https://www.circle.com/), [Codeship](http://codeship.com/), GitHub [Actions](https://jasonet.co/posts/use-github-actions-for-ci/), GitLab [Continuous Integration](https://about.gitlab.com/product/continuous-integration/), [Jenkins](https://jenkins.io/), [TeamCity](https://www.jetbrains.com/teamcity/), [Travis](https://travis-ci.org/), and shell scripts invoking `docker build`.

{id: containers-delivery}
## Distributing Container Images Securely

{id: containers-registries}
### Using A Container Registry

Docker Hub, Quay, Harbor, ECR

{id: containers-cd}
### Continuous Delivery

[Argo](https://argoproj.github.io/), flagger, Spinnaker

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