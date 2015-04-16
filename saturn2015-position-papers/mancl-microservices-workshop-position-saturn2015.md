# Microservices Workshop position paper - SATURN 2015

Dennis Mancl, Alcatel-Lucent
dennis.mancl@alcatel-lucent.com


I am interested the potential future benefits and problems for Microservices.  Here are some of my thoughts about this topic.

Many of the benefits are related to architecture and design issues.

 - an opportunity for more decoupled software design (building applications from components rather than building monolithic systems)
 - development savings through software reuse - both planned reuse and ad hoc reuse
 - in a multiple-application environment, the applications can build on the same set of small services in order to have a consistent approach for infrastructure - such as authentication, temporary data storage, logging, and transaction handling

Many of the problems are connected to integration, testing, deployment, and operations.

 - management of multiple versions of components and interfaces
 - data migration issues when updated components have a modified data model
 - testing individual services, especially if they are stateful
 - testing end-to-end scenarios - the basic problem of testing composite services
 - design documentation (and documentation standards) in a large complex services environment

I am also interested in how Microservices can be used in a hybrid way -- how incorporate a cluster of small services into a conventional application.  Most software development organizations are "building on top of a large legacy code base", so it is impractical to throw everything away to build new applications based on all new technology.  Microservices might be flexible enough to support attaching new functionality to an existing application base.
