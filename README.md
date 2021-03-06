# Abstract

This article shows how to sketch a transactional application architecture based on the [CQRS](https://en.wikipedia.org/wiki/Command%E2%80%93query_separation#Command_query_responsibility_segregation) pattern using [WebApi](https://en.wikipedia.org/wiki/Web_API) [netcore](https://en.wikipedia.org/wiki/.NET_Core) technology according to the [SOLID](https://en.wikipedia.org/wiki/SOLID) principles. This results in a highly generic and robust architecture which, according to the [Aspect Oriented Programming](https://en.wikipedia.org/wiki/Aspect-oriented_programming) methodology, addresses the problems of data validation, authorization, logging and audit trail, performance monitoring. In other words, all the [cross-cutting concerns](https://en.wikipedia.org/wiki/Cross-cutting_concern) are managed through a thorough infrastructure configuration. Here, the role played by the [Dependency Injection](https://en.wikipedia.org/wiki/Dependency_injection) container is of paramount importance, definitely allowing to robustly and elegantly orchestrate the chain of objects in charge of fully executing the action together with-cross cutting concerns.

# Introduction

A big class of today's applications falls in the category of the Transactional Applications, also known as [Online Transaction Processing](https://en.wikipedia.org/wiki/Online_transaction_processing) applications. Basically, this kind of applications continuously execute atomic actions; each action mutates a state (typically stored within a database). Examples of such applications are:

* [Human Resource Management](https://en.wikipedia.org/wiki/Human_resource_management) (HRM) applications;
* [Enterprise Resource Planning](https://en.wikipedia.org/wiki/Enterprise_resource_planning) (ERP) applications;
* [Content Management Systems](https://en.wikipedia.org/wiki/Content_management_system) (CMS);
* [Enterprise Content Management](https://en.wikipedia.org/wiki/Enterprise_content_management) (ECM) applications.
