{id: ch_cn-sec-foundations}
#  Cloud Native Security Foundations

{id: identity}
## Identity

[Identity management](https://en.wikipedia.org/wiki/Identity_management) revolves around *entities* such as people or an application and their respective digital representation. An entity can have multiple identities with different attributes attached, potentially context-dependent.

{aside}
### EXAMPLE: Identity

When you're visiting a website in your web browser, there are at least three entities involved:

- You, the human being.
- Your web browser.
- The website.

For example, when I look at `mhausenblas.info`, I'd encounter something like the following:

![Example website identity](ch2_mhausenblas.info-identity.png)

Inspecting the website's identity reveals that I'm using a self signed certificate, which is understandable given it's a GitHub page. 
{/aside}


{id: authn}
## Authentication

In the context of this book, we define:

Authentication
: The process of confirming the identity claimed by an entity.

This means, based on a claim of an entity, there is a sequence of steps that either leads to confirming the claim, or not.

{aside}
### EXAMPLE: Authentication

For example, I can claim to be an Austrian living in Ireland. The authentication processes could be as follows:

1. Show me your passport, which confirms I have a valid Austrian citizenship.
1. Provide proof of residence, for example, through an utility bill to an Irish address, in my name. This proofs (to a certain extent) that I live in Ireland.

This example also shows to things: it's always a matter of trust (in certain artifacts such as the bill) as well as that while it's possible to verify a claim, the opposite is usually not possible. How do I proof to you that I am *not* living in, say, Austria? :)
{/aside}

{id: authz}
## Authorization

In the context of this book, we define:

Authorization
: The set of *privileges* assigned to an *entity* specifying access to a *resource*.

You can simplify that to: access control for authenticated entities.

{aside}
### EXAMPLE: Authorization

Look at this file here:

```sh
~/tmp
$ ls -al MINE
-rw-------  1 mhausenblas  mhausenblas  0 30 May 14:30 MINE
```

What's the authorization regime here? Well, I as the entity (or: user) `mhausenblas` have the privileges (or: rights) to both read and write the resource (or: file) `MINE`. Needless to say that declaring this with `chmod 600 MINE` is pretty useless, if there would not be a piece of software enforcing said authorization.
{/aside}


https://www.youtube.com/watch?v=TZ73EBP2a9Q


{id: gp-foundations}
## Good Practices

{id: av-foundations}
## Attack Vectors

