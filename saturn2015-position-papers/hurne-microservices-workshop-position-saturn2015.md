Microservices are not micro
---------------------------
Jim Hurne

I am a technical lead for a "services" team within IBM Watson.  My team is
responsible for developing some of the microservices which will be used to
create new cognitive computing applications. Even though I am responsible for
making important technological choices, I am very much a "developer in the
trenches" and contribute daily to the growing codebase of my team's
services.

I hope to bring my perspective and experience as a software developer to the microservices
architecture workshop.

Below are some of my thoughts around microservices:

## "Micro" does not equal "easy"

Despite the term, a microservice is not easy to implement. Microservice
developers must consider:

   * The API the service exposes

   * How the service will be deployed

   * How the service will be monitored and measured

   * How the service can be scaled up and down

   * How the service can be safely upgraded

   * Security within and around the service

   * The environment and surrounding infrastructure the service will live within

All of this, of course, is above and beyond the basic functionality of the
service.

In a "traditional" monolithic application, many of these concerns only need to
be solved once. For example, deployment of a monolithic application only needs
to be considered once for the entire application.  In a microservices
architecture, each service must solve these problems.

In an attempt to make microservice implementation easier, several organizations
have developed frameworks and libraries, and some of the organizations have
open-sourced their frameworks.  For example, [Netflix has contributed much of
their internal libraries and frameworks to the
community](http://netflix.github.io/). Twitter and LinkedIn have also
contributed frameworks and libraries (see
[here](https://engineering.twitter.com/opensource) and
[here](https://engineering.linkedin.com/tags/open-source), respectively).

While such frameworks successfully reduce duplication and make some things
easier, they still put a great burden on service teams. Many of the frameworks
have steep learning curves. It can easily take a new microservice team many
months to master the sheer number of frameworks and libraries.

I wonder if teams and organizations fully understand the costs
involved with selecting the microservices architecture. The amount of effort my
team has spent on many of the aforementioned concerns has certainly surprised me.

## Microservice architecutures are not new

I first learned about microservices in 2006 when I listened to [Software Engineering
Radio Episode
40: Interview Werner Vogels](http://www.se-radio.net/2006/12/episode-40-interview-werner-vogels/). Of
course, at the time, the term "microservices" did not yet exist. Back in 2006, the
industry was fixated on SOA.

In the interview, Werner Vogels, the then-and-now CT of Amazon, described how
Amazon had broken up their system into a set of small, loosely coupled
services. Werner's description was nearly identical to how many people describe
microservices today.

My next close encounter with microservices was when I met a few of the Netflix
engineers while attending the [JavaPosse
Roundup](http://www.mindviewinc.com/Conferences/JavaPosseRoundup/) in 2011 (now
known as the Winter Tech Forum). The Netflix engineers described to me how
their entire architecture was broken up into small services. What they
described to me sounded very much like what Amazon has been doing for some
time.

The fact that the ideas behind "microservices" have existed for a long time
give the architectural style credibility.  Is microservices a rebranding of SOA
and distributed computing? Perhaps it is just a new label for a proven
architecture that successful companies like Amazon and Neflix have been
applying for many years.

## Microservices and organizational structure

Many of the organizations that have successfully applied the microservices
style (e.g. Amazon, Netflix) have had a similar internal
team structure:

   * Teams are responsible for one or more services

   * No service is owned by more than one team

   * Teams are relatively autonomous and are free to make independent
     implementation choices, so long as they adhere to the agreed-upon APIs and
     service contracts.

   * Teams contain the complete skill set necessary to support a service from
     inception to deployment (product management, development, operations,
     database administration, production support, etc).

   * While teams are loosely coupled from internal implementation
     details, they are tightly aligned on overall organizational goals.

An interesting question worth exploring is whether or not an organization can
successfully employ the microservices architecture style without also having an
internal team structure like the one described above.

## Questions

   * Can microservices be made easier to implement?

   * Is a particular organizational structure critical to successfully
     implementing a microservices-based application?

   * Do the benefits of a microservices architecture truly outweigh the costs?

