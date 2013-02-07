---
layout: default
title: Philosophy
---

# <a name="philosophy">Philosophy</a>

## <a name="philosophy-embrace">Datomic principles, without compromise</a>
Datomisca is a thin layer around Datomic aimed at exposing Datomic functionalities and leveraging its full power.

Datomic features we really love are:

- Immutable & temporal nature of Datomic
- Atomic facts creation/update
- Lazy entity structure just based on Datom IDs (and namespaces)
- Datalog queries & custom rules definition
- Queries as reusable static structures
- Schema to constrain data types
- Entity bi-directional relations
- Database temporal exploration
- Database state simulation without commit

In our design, we are also deeply aware of the architecture of Datomic:

- Single remote asynchronous transactor
- Multiple local peers high-speed cache


<br/>
## <a name="philosophy-enhance">Datomic features with a Scala flavor</a>

Datomisca uses Scala concepts to enhance Datomic experience for Scala developers:

- Type-safety, 
- Asynchronism & non-blocking patterns, 
- Advanced Functional programming
- Scala 2.10 Macros Compile-time enhancement

Datomic Java API is also quite poor in terms of typing because it tends to return `List[List[Object]]`. In Datomisca, we provide tools to convert those too generic types into Scala generic typers.

An important feature about Datomic is that entities have no real representation but Datoms having common entity ID. This means it's really **easy to manipulate entity in a very atomic way, field by field**.  

So we wanted to preserve this atomic nature. That's why **we don't focus on Entity mapping to/from Scala case-classes**. We provide it but as an extension because people will want it but we believe this is not necessarily the best approach against Datomic.