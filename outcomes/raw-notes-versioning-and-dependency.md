# Versioning and Dependency 

## Key Outcomes

Microservices Architecture is not for everyone
* Costs vs Benefits
* Change has a cost

Critical Enablers
* Have different costs
* Determines how well / fast you can change
* Determines which versioning strategies to use

Versioning Strategies
* See raw notes below...

Version is a run time idea
* Implications -- you don't know what to test until runtime
* Tools
* Testing will not save you
* Configuration vs. code

## Raw Notes

Starting seed -- versioning and dependency 

* Feature Toggling
* Distributed Big Balls of Mud
* Tools
 - We have them but we don't like them = Monoliths
 - We don't have them and we don't like them = Microservices
* Smart Endpoints, Dumb Pipes
* Cycles and dependency loops

Data...
* Mutable vs immutable
* Schemas vs validation


* Encapsulation and Abstraction
* Who has to deal with updates?
 - service -- all internal
 - caller - API (e.g. request version you want)
* What drives change?
 - Bug fixes
 - Changing APIs

Versioning strategy
* Copy it all
 - API, data, model, code in lock step
 - Simple, full backwards compatibility
 - Good for slower moving environments 
  - May not get as much out of microservices
* Always run latest
* Make the service deal with the change
* Major.minor versions
 - Minor versions remains backwards compatible within major
 - Major versions can be breaking

Foundations for choosing a versioning strategy
* Tests
* Metrics, monitoring
* Incremental Roll out / roll back
* consequences of failure - relative?
 - safety critical is assumed out of scope
* Role of required / desired change
* How easy / fast to recover
* Culture, responsibility
* Risk tolerance
* Routing of different services, difference versions
* Data infrastructure - relational vs. schema-less
* size of deployable units

What makes versioning / dependency manage different in microservices?
* tools
 - runtime in microservices
 - design time in traditional / monolithic
* more loosely coupled? not necessarily
* run time considerations


Raw notes

![Raw notes captured during group discussion](/outcomes/images/versioning-and-dependency-notes.jpg)


Summary poster of key outcomes from Breakout session.

![summary poster](/outcomes/images/versioning-and-dependancy-poster.jpg)


Gregor presenting the group poster

![Gregor presenting the group findings](/outcomes/images/afternoon-poster-group-1.jpg)
