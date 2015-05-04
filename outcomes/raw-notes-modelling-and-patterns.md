# Modeling and Patterns

Starting seeds

* Stereotypes
* Visualization of models
* Domain modelling
* Single responsibility principles
* CQRS
* Beyond Bounded Context

## Raw Notes

Is it easier to start with a monolith?
 - "monolith as the prototype"
 - Allows reflection.. you can refactor from "Type A" Service to "Type B" Service

Refactoring microservices is hard
 - Tooling
 - Teams and communication
 - Must refactor the Organization too
 - Public APIs are hard to change --> need to design for extensibility
 - Postule's Law -- link / summary
 - Services must deal with same domain at same rate?
 - More difficult to seperate things out later.

Aggregate Pattern
 - Is this right for microservices?
 - If you can do the aggregate patter, then it's good and desrireable (but you can't always use the pattern)
 - Trade-offs
  - Can be large -- lots of parts
  - Rich domain model needed
 - Business concepts vs. Data
 - Eveyone needs to understand DDD

"Type A" vs "Type B" Services
 - Type A - Modelled
  - modeled
  - fully understood
  - agreed model
  - DDD (but can use other modelling methods as well)
 - Type B - Free Range
  - Not-DDD
  - Partially understood
  - Scenarios across services
  - exploratory
 - Can refactor from Free Range to Modelled

How do you model a system well?
 - Who creates the "system" ?
 - "A forrest of models with groves of understanding within" - Dennis
 - Clusters of understanding
 - Need for structuring principles

how do you model deployment?

Modelling desired properties such as security, disaster recovery
 - Don't know all the concerns or requirements up front
 - Quality of services
  - how much can you degred?
  - Netflix.. chaos gorilla kills a region every quarter
   - but nobody dies if you can't stream movies...
   - a few participants from telcom e.g. 911 can't go down becuase you're testing resiliancy
   - Frustration != crticiallity
 - What about modeling levels of degraded behavior?

how do I figure out what is available already?

DRY is not as high a priority
 - easier to duplicate in the cloud
 - Broken APIs are worse than duplication

Common / New Patterns across all services
 - Monitoring
 - Logging
 - Containers
 - Discovery
 - Security
 - Versioning
 - others...

Survival of the fittest?
 - Darwanism for microservices?
 - organic evolution
 - The "better" servicese will eventually win
 - Freedom and Responsibility
  - link to Diane Marsh Keynote last year
  - how do you enforce responsibility?

Dependancies from a specific perspective?
 - scenario, app, or entry point into microservices
 - Context
 - Dependancy diagrams


# Key Outcomes

Easier to start with Monolith
 - learning
 - refactoring
 - moving responsiblties is easier
 - Conway's Law -- must refactor Org

Modelled vs. Free Range Services
 - Modelled
  - Understood
  - Greater stability
  - Reasoning ability
  - Not necessarily Correct
 - Free Range Service 
  - Exploratory
  - Not fully understood
  - Mind Meld Required to understand how to use the service -- what's the model?

What is the "System" in a microservices world?
 - clusters of understanding 
 - Evolutionary - survival of the fittest
 - DRY not as important
 - Modelling desired properties
  - security, high Quality of service
  - Cautionary Note: Netflix, the "microservices poster child" doesn't have many of these concerns and so have not addressed many of the potential modelling needs.  This does not mean that they are not important.  Frustration != Critical Loss
