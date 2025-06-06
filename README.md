# Custom Software - Handbook
The custom software handbook is a collection of philosophies and principles, that the CS team adheres to.
If you feel that changes are needed, please open a PR and tag several reviewers, once approved, it will be a part of the team handbook.

## Working methods of Custom Software

In Custom Software we strive for software excellence. 
Therefore, we value what clever people have done for research into creating more robust and maintainable software. 
This results in the following principles for how we work.

* We do extensive review of everything
* We test everything, preferably through automation
* We code defensively
* We take ownership of the full build and release pipeline for both code and platform

We know that these methods all require more work and therefore cost upfront but are confident that they will pay back down the road.
The consequences for these principles are described below.

## We do extensive review of everything

This sets the requirement that one developer can never work alone. 
On every project there will always be at least 1 developer and 1 reviewer.

Reviews are done to spot error and share knowledge. 
It is important that the reviewer points out everything that raises an eyebrow. 
Nothing too big or small.

Doing reviews can take up several hours of a workday.

Reviews should be done with high urgency as to not stop a person from doing work. 
If the review cannot be done within a day the reviewer must state when the review will be done.

## We test everything, preferably through automation

Every bit of work must have been tested before it hits production.

Every piece of logic must have a complimentary unit test.

Unit and integration tests do not replace a confirming manual test.

We do not do test-driven development as a principle, but are open for it.

For unit tests in C#, we prefer the following tools: xUnit, AutoFixture, Moq andFluentAssertions.

Unit tests must be written in the Arrange, Act, Assert pattern.

## We code defensively

We code for robustness; this means we need to have a strong defence against the possibility of common pitfall errors.

We embrace the following techniques for defensive coding

* Immutability
* Parse, don’t validate
* Fail early, fail fast
* Composition instead of inheritance 

## We take ownership of the full build and release pipeline forboth code and platform

Taking over a new project setting up automated CI/CD is of highest priority.

We do Infrastructure as Code as extensively as possible.

We ensure build and deployment tools are maintained and updated.

We react to failures in CI/CD pipelines.
