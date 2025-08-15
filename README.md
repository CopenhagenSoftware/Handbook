# Custom Built Solutions - Handbook
The custom built software handbook is a collection of philosophies and principles, that the CBS team adheres to.

If you feel that changes are needed, please open a PR and tag several reviewers, once approved, it will be a part of the team handbook.

## Working methods of Custom Built Solutions

In Custom Built Solutions we strive for software excellence. 
Therefore, we value what clever people have done for research into creating more robust and maintainable software. 
This results in the following principles for how we work.

* We do extensive reviews of all things
* We test everything, preferably through automation
* We code defensively
* We take ownership of the full build and release pipeline for both code and platform
* We use discussion as a tool for problem solving

We know that these methods all require more work, and therefore a higher cost upfront but are confident that they will pay back down the road.

## We do extensive reviews of all things

Reviews serve to spot errors and share knowledge between colleagues.<br>
It is important that the reviewer points out everything that raises an eyebrow. 

` Nothing too big or too small. `

Doing reviews can take up several hours of a workday.

Reviews should be a priority, we should strive to avoid bottlenecks.<br>
If the review cannot be done within the same day, the reviewer must give a timeframe for when the review will be completed.

This requires that one person can never work alone, and that on every project there will always be at least 1 developer and 1 reviewer.

<i> Reviews apply to all forms of work, including code, documentation, architecture, and design. </i>

## We test everything, preferably through automation

Every bit of work must have been tested before it hits production.

Every piece of logic must have a complimentary unit test.

Unit and integration tests, by default, do not replace a confirming manual test.

We encourage test-driven development, but do not enforce it.

For unit tests in C#, we prefer the following tools: 
* xUnit
* AutoFixture
* Moq
* FluentAssertions.

Unit tests must be written in the Arrange, Act, Assert pattern.<br>

## We code defensively

We code for robustness; this means we need to have a strong defence against the possibility of common pitfall errors.

We embrace the following techniques for defensive coding

* Immutability
* Parse, don’t validate
* Fail early, fail fast
* Composition instead of inheritance
* Factories for object creation

## We take ownership of the full build and release pipeline for both code and platform

When we take over a new project, setting up automated CI/CD is of the highest priority.

We do Infrastructure as Code as extensively as possible.

We ensure build and deployment tools are maintained and updated.

We react to failures in CI/CD pipelines.

## We use discussion as a tool for problem solving

In all things, take the time to make sure involved parties are informed and that the communication is constructive.

Rushing communication, and especially code reviews, leads to misunderstandings and mistakes.

This will likely end up in more work in the end, and therefore is not a time saver.

## We make changes in pairs where regulare review is unavailable

Whenever we change something in production we have a colleague observe to validate we do as we intend to do.

The term Production covers any live running system where invalid changes could cause downtime - this includes deployment pipelines. 

The term Changes covers any modification not covered by normal review, normally things not in source control.

[Two-Person rule](https://en.wikipedia.org/wiki/Two-person_rule)
