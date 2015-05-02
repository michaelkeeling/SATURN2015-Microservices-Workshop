#Breakout session on testing

##Summary
* Microservices move much testing from static to dynamic
* And they are harder to test
* Old testing
 * Hermetic test of statically linked monolith
* Microservices testing
 * Hermetic testing not possible for whole system
 * Prod testing may be necessary
 * Exogenous factors hard to test (eg your website may be hit by a web spider that you did not write)
 * PAAS is an enabler including automated/scripted deploy and test
* However, there is a sharp line: Does the service have access to prod data?
* Our terminology is insufficient
 * For traditional testing, we hvae mocks, fakes, stubs, environments, etc.
 * For microservices
  * Much testing is at meta/infra level: do deployment scripts work, handle errors.  How do you test meta-infrastructure?  Feels like the shift from first order logic to higher order functions.
  * Much testing is done via data configuration, not code -- how do we refer to that test config?  How do you test config data?
  * What is the new equivalent (if any) of an environment?  Things seem to smear.
* There was an IPv4 flag day where the internet switchted to v4, but for IPv6 it's a messy transition.  Old testing seems more like the former and testing microservices more like the latter.

##Raw Notes
* What are we really testing?
 * The microservice itself, as a unit?
 * Higher, interaction flow between services?
 * Contract verifications?
 * Scenarios spanning services?
 * Live production test, canary?
* In context of microservices, unit tests are not enough.  Much logic is in the configuration of the services and represents the intent of the developers.
* More configuration work in microservices, less configuration in the code units.
* Test environments are harder
 * More deployent units
 * Non-determinism of complex environment (think "flaky integration tests")
 * Hard to say what a "test environment" is exactly, with microservices.
 * Blending of prod and non-prod services (eg auth)
* 3 Categories questions: Tests, Rules (who tests), Environments (when and where to test)
* How much value are we getting from unit tests?  What is a "unit test" -- ie what is the unit, a class, a service, a module?
* Kinds of testing: A/B, Beta testing (compare with canary)
* No IPv6 flag day
* Quality attribute testing (not just functional)
* What are the test environments and how are they configured?  Our current environments are fairly standardized (local, devel, QA live, prod).
 * What terminology do we use for microservice tests?  Today we use mock, fake, etc.  But with nearly-live services, what are the key ideas and terms?  We don't have the vocabulary to talk about it yet.
 * However, there is a sharp line between prod and non-prod data.
* Automation in PAAS solve many environment issues.  
* Example of exogenous factors that you cannot control in prod environment: a Web Spider.
* What is adequate testing?
 * Unit, integration, quality attribute?
 * Need metadata for microservices (eg version, compatability)
 * Are we testing the configuration (which might just be data) or the environment?
 * E.g., don't configure to use no-op auth service.
* Who owns the configuration?  Individual teams may run full-speed on their services, but how is the whole system assembled in a way that makes sense?  Is the configuration part of the environment of a service, or a separate thing?
* Configuration vs convention (eg in frameworks)
* Dependency injection at service level?
* In our experience with using OSS (eg apache, mysql, hadoop), most problems arise from configuration errors.
* Some things cannot be tested outside of production.  (Minor example of a "wicked problem").
* Testing is more effort because it is a system-of-systems (see SEI research on this topic).
* Service responsible for some of its testing
* Microservices changes the challenge from a static one (eg static linking of modules into a single binary) into a dynamic one (runtime reconfiguration of many services into a system-of-systems).
