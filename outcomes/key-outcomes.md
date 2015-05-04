# Key Outcomes

## What is a microservice?

The SOA Architectureal style, roughly consistent of these constraints:
* Communication via messages
* Each service is indepentently deliverable
* Loosely coupled

Plus organizational constraints
* Decentralized design authority
 * Architect is a coach
 * Architecture is enforced through tooling (see note below regrading runtime ermergent properties)
* limited team size 

In order to
* Sustain high delivery velocity by removing contention between teams and allowing rapid evolution (i.e. business agility and responding to change)

## How big should your microservice be?

Size of a microservice is a function of
* team size
* costs
* agility
* domain model

## Key enablers for microservices

* Process (deployment, development, testing, ...)
* Culture
* Tools

## ROI is a huge factor in choosing to use microservices

There is a cost to being able to develop software in this way.  But you get benefits such as shipping faster, innovation, scalability, and independence. Do the benefits make sense in terms of the costs in your specific case?

* Agility as a strongly desired quality attribute
* Rate of change vs. risk tolerance
* Cost vs. Benefits

## Microservices make traditionally static things dynamic

* Cannot see the system until fully deployed -- and only at run time
* Linking is not only dynamic but often distributed
-- configuration
-- communication to components
* Versions of modules become dynamic dispatch of versions of services.
