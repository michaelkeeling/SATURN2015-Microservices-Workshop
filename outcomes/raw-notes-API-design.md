Breakout session: API Design

* Topics: REST, async/sync, stateful/stateless
* API’s should be immutable.  Extensions are OK.  Can publish more than one version, so introduce a new API instead of making a breaking change.  
* Semanic versioning: x.y.z numbering  http://semver.org/
* Concurrent deployment of multiple versions.
* API data representation vs API interaction model: major theme of our group
* Should there be multiple resources per API?
* API’s and orchestration/coordination
* Governance and sunsetting of API versions / APIs
* Feature toggles to introduce new versions.  Must sunset toggles or crazy complexity.
* HATEOS, Richardson maturity model.
* Protobufs: all fields now optional to facilitate API evolution (no required fields)
* Danger: pushing logic into clients  Non-HATEOS, UPDATE validation.
* Meters vs Feet in API integers
* How do we hide internal complexity from API users?  Example of failure:  WSDL on top of IDOC/RPC at SAP
* Sadly, there is no good advice yet on how to define (1) resources or (2) representations based on business analysis, domain analysis, DDD, bounded contexts.  Particularly annoying that the literature treats this as a simple “exercise left to the reader” when it’s really hard.
* Q:  Should we assume that business analysis should not be entangled with microservices?  Or is a good ontology a precondition?
* What does it take to make microservices work?  (1) Ontoogy, (2) communication protocols, (3) Infra: monitoring, governance, cataloging, discovery.
* Big theme: microservices shifts the needle (different QA tradeoffs) compared to SPA
 * From cataloging to discovery / search
 * To ants vs command-and-control (thousand flowers bloom)
 * A priori is easier, but discovering collisions and fixing works too and allows dev teams to avoid contention and run full speed.
 * Refactoring is expensive
 * Microservice collisions are localized.  But perhaps assumptions are baked in?  Is refactoring easier because smaller?  Can we develop tools for distributed systems that work like IDE refactoring?  
* How to avoid distributed big ball of mud?
* Humans deal well with ambiguity.  Web is inherently unstructured and uncontrolled.  Microservices embraces this -- but how does this play with corporate agendas and need to coordinate?
* Metaphor: corp governance as IETF?
* WSDL is a poor subset, noisy, and dead?
* Microservice contracts as less formal.
* Open topic: exception handling.  RMI forced RemoteException but nobody knows what to do with it.  Must embrace errors in distributed computing.
