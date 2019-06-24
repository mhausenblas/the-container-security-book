# Introduction

Welcome to The Container Security Book (TCSB) and thanks for reading it.
This is a free book, aiming to bring good practices around container security, from container images to runtime challenges to policies, and service mesh security to as many practitioners as possible. If you have feedback or want to discuss something, please visit the book's [forum](https://community.leanpub.com/c/container-secur).

## Why This Book?

Containers themselves are a relatively new species, really going mainstream only in the last few years, starting around 2014. 

The first wave kicked off when Docker (nee dotCloud) starting in 2013 and really taking off in 2014 found a way to make them useable by defining a nice packaging format and an abstraction level allowing developers to use them in a straight forward manner.
All you had to learn was `docker build` and `docker run` and the Docker Hub would supply you with tons of apps and tools, ready to use.

Then, the container orchestration wars, roughly 2015 to 2017, happened. Many of the early approaches turned out to be niche players and what at time of writing is used are mainly Kubernetes (cross-environment), Amazon Elastic Container Service (ECS), and Nomad.

Then came the third wave: the era of the service meshes began in roughly began in early 2016 when Buoyant released its first iteration of Linkerd. Others followed, including Istio and AWS App Mesh and in early 2019 we witnessed the effort to start standardizing services meshes via the Service Mesh Interface (SMI). Also, starting in late 2018, we saw the formation of a Special Interest Group (SIG) [Security](https://github.com/cncf/sig-security) at the Cloud Native Computing Foundation (CNCF) to which many of the book's authors are contributing to.

In all of the phases above, the security angle sometimes was handled as a secondary issue, sometimes neglected, and oftentimes underappreciated. You will find great talks, blog posts, and articles in many places, but still, few good practices are documented, comprehensively, in a central location.

This book is an attempt to change this.

## Scope Of The Book

In scope for this book are the following topics:

- [Cloud native security foundations](#ch_cn-sec-foundations): principles like defense in depth, policies, identity, authentication, authorization, and threat modelling.
- [Containers](#ch_containers) at large, including container runtimes, images, and how to build and distribute them securely, in an automated fashion.
- Security aspects of widely used [container orchestrators](#ch_co), that is, Kubernetes, ECS, and Nomad.
- [Policies](#ch_policies), including networking and workflow, with a focus on the Open Policy Agent.
- Dealing with [sensitive information](#ch_secrets) in and with containers (aka: secrets).
- [Service mesh security](#ch_meshes): security features and considerations of Istio, App Mesh, Linkerd as well as the Service Mesh Interface.
- Container-level [penetration testing](#ch_pentesting).

Not in scope, for now:

- Lambda
- WASM

## Tenets

This book has three tenets:

1. Security should be *accessible*. Both in the sense of understandable, even and especially for non-experts, as well as the content should be available for everyone, everywhere, for free.
2. Not just with but *ahead of times*. Books have a tendency to rot. We believe that a living book, something that evolves and grows over time is the right approach to security. Also, some of the processes and tools discussed here have not yet enjoyed wide adoption. Doesn't matter, gotta be where the puck is going.
3. Panta Rhei--everything flows. Security is a *never-ending process*, with all hands on deck. It's not the sole responsibility of your security team. Developers, architects, devops folks, SRE folks, networking folks, managers, your aunt and her dog. We all are responsible, all the time.

### Audience
The Audience: Cloud native adopters. Developers. Container management system users and administrators. Security teams.

### How To Use This Book

Each chapter provides an introduction to get everyone on the same page, then discusses relevant concepts and tooling, and finally walks you trough good practices and attack vectors.

Self-container

### How Can I Contribute?

If you want to report a mistake, or want to contribute to this book, then please do the following:

1. Create an issue on the book's [GitHub repo](https://github.com/mhausenblas/the-container-security-book). If you want to contribute (at least a section) to the book, suggest what it is about and where to locate it (chapter-level).
2. Send in a pull request (PR) against the repo, which should include your name and some social handle added to the [AUTHORS](https://github.com/mhausenblas/the-container-security-book/blob/master/AUTHORS) file.
3. If the PR is accepted, your name will be added to the list of authors on the cover page of the book; if it's a minor contribution, a simple suggestion or a bug report, we will add it to the acknowledgements section here in this first chapter.

## Acknowledgements

In reverse order (newest on top):

* Duffie Cooley
* Justin Cormack
