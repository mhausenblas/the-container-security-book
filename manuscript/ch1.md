# Introduction

## Why This Book?

Containers themselves are a relatively new species, really going mainstream only in the last few years, starting around 2014. 

The first wave kicked off when Docker (nee dotCloud) starting in 2013 and really taking off in 2014 found a way to make them useable by defining a nice packaging format and an abstraction level allowing developers to use them in a straight forward manner.
All you had to learn was `docker build` and `docker run` and the Docker Hub would supply you with tons of apps and tools, ready to use.

Then, the container orchestration wars, roughly 2015 to 2017, happened. Many of the early approaches turned out to be niche players and what at time of writing is used are mainly Kubernetes (cross-environment), Amazon Elastic Container Service (ECS), and Nomad.

Then came the third wave: the era of the service meshes began in roughly began in early 2016 when Buoyant released its first iteration of Linkerd. Others followed, including Istio and AWS App Mesh and in early 2019 we witnessed the effort to start standardizing services meshes via the Service Mesh Interface (SMI).

In all of the phases above, the security angle sometimes was handled as a secondary issue, sometimes neglected, and oftentimes underappreciated. You will find great talks, blog posts, and articles in many places, but still, few good practices are documented, comprehensively, in a central location.

This book is an attempt to change this.

## Scope Of The Book

In scope for this book are the following topics:

- [Cloud native security foundations](#ch_cn-sec-foundations): identity, authentication, and authorization.
- Containers at large, including container runtimes, images, and how to build them (CI pipelines).
- Widely used container orchestrators, that is, Kubernetes, ECS, and Nomad.
- Policy handling, including networking and workflow, with a focus on the Open Policy Agent.
- Dealing with sensitive information in and with containers (aka: secrets).
- Service meshes, that is, security features and considerations of Istio, App Mesh, Linkerd as well as the Service Mesh Interface.
- Container-level penetration testing.

## The Audience

Cloud native adopters. Developers. Container management system users and administrators. Security teams.

## How Can I Contribute?

Send in a pull request (PR) against the repo [mhausenblas/the-container-security-book](https://github.com/mhausenblas/the-container-security-book) or raise an issue. If the PR is accepted, your name will be added to the list of authors on the front page.