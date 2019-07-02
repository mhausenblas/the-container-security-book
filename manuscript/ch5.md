{id: ch_policies}
# Policies

{id: basics-policies}
## Basics

OPA, https://kyverno.io/

## Execution and Runtime

### Kubernetes--Pod Security Policies

PSP vs pod security constraints

Further resources:

- Cory O'Daniel wrote a useful piece on [Kubernetes: Assigning Pod Security Policies with RBAC](https://medium.com/coryodaniel/kubernetes-assigning-pod-security-policies-with-rbac-2ad2e847c754)
- Peter Balogh has some great, visual explanations in [An illustrated deepdive into Pod Security Policies](https://banzaicloud.com/blog/pod-security-policy/).

### ECS

ECS does not have an equivalent expressive abstraction to Kubernetes' Pod Security Policies, to restrict execution and runtime properties. However, it does allow for setting the following [security-related constraints](https://docs.aws.amazon.com/AmazonECS/latest/developerguide/task_definition_parameters.html#container_definition_security) in a task definition:

- `privileged`: Allows a container elevated privileges on the host container instance, similar to the root. Do note, however that it is not supported for Windows containers or Fargate launch type.
- `user`: Sets the user name inside a (Linux) container, effectively causing `docker run` to use the `--user` option. See, for background, [this article](https://medium.com/lucjuggery/running-a-container-with-a-non-root-user-e35830d1f42a) and also note that it's not available for Windows containers.
- `dockerSecurityOptions`: Set SELinux and AppArmor custom labels. This causes `docker run` to use the `--security-opt` option and is supported for Linux containers on EC2 only. In other words, you can not use it with either Windows containers or tasks using the Fargate launch type. See, for background, [this](https://www.nearform.com/blog/securing-docker-containers-on-aws/) article and [that](https://www.oreilly.com/ideas/docker-security) article.


{id: policies-networking}
## Networking
 
Kubernetes NP and AWS security groups

https://glasnostic.com/blog/mitigating-deployment-risk-in-microservice-architectures-quarantine

see [image signing](#containers-signing) for basics

https://cloudonaut.io/more-than-25-ssl-certificates-with-ecs/

{id: policies-opa}
## Open Policy Agent (OPA)

https://www.youtube.com/watch?v=Yup1FUc2Qn0

https://play.openpolicyagent.org/

{id: tm-policies}
## Threat Model

{id: gp-policies}
## Good Practices



