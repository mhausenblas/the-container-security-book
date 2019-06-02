{id: ch_policies}
# Policies

{id: basics-policies}
## Basics

## Execution and Runtime

### Kubernetes--Pod Security Policies

PSP vs pod security constraints

Cory O'Daniel wrote a useful piece on [Kubernetes: Assigning Pod Security Policies with RBAC](https://medium.com/coryodaniel/kubernetes-assigning-pod-security-policies-with-rbac-2ad2e847c754)

### ECS

ECS does not have an equivalent expressive abstraction to Kubernetes' Pod Security Policies, to restrict execution and runtime properties. However, it does allow for setting the following [security-related constraints](https://docs.aws.amazon.com/AmazonECS/latest/developerguide/task_definition_parameters.html#container_definition_security) in a task definition:

- `privileged`: Allows a container elevated privileges on the host container instance, similar to the root. Do note, however that it is not supported for Windows containers or Fargate launch type.
- `user`: Sets the user name inside a (Linux) container, effectively causing `docker run` to use the `--user` option. See, for background, [this article](https://medium.com/lucjuggery/running-a-container-with-a-non-root-user-e35830d1f42a) and also note that it's not available for Windows containers.
- `dockerSecurityOptions`: Set SELinux and AppArmor custom labels. This causes `docker run` to use the `--security-opt` option and is supported for Linux containers on EC2 only. In other words, you can not use it with either Windows containers or tasks using the Fargate launch type. See, for background, [this](https://www.nearform.com/blog/securing-docker-containers-on-aws/) article and [that](https://www.oreilly.com/ideas/docker-security) article.


{id: policies-networking}
## Networking
 
Kubernetes NP and AWS security groups

see [image signing](#containers-signing) for basics

{id: policies-opa}
## Open Policy Agent (OPA)

https://www.youtube.com/watch?v=Yup1FUc2Qn0

{id: gp-policies}
## Good Practices

{id: av-policies}
## Attack Vectors



