// Exmpale 
# Microservices in a monorepo

* Status: <Draft, To be discussed, Under Consideration, Accepted>
* Deciders: [names]
* Date: <date>

## Context and Problem Statement

There will be two teams working on one FE, one GraphQL API and multiple BE microservices. We are about to take the learnings from the PoA into a the MVP product, by starting one monorepo or multiple repos per service.

## Considered Options

1) One repository containing one service per root directory
2) A repository per service

## Decision Outcome

A monorepo has been chosen, because all code is moving quickly in the beginning of the project and we don't want blocking dependencies or an inefficient development workflow.
Since we will implement User Stories end to end, a single developer usually has to work in multiple services simultaneously, which is easier in a monorepo.

We will evaluate the decision after two Sprints.

### Positive Consequences

* A monorepo will speed up development.
* Package dependencies can be managed using tools like Lerna or NX.
* We think it is easier to move from monorepo into multiple repos than to merge multiple repos into a monorepo.

### Negative Consequences

* There is a risk of coupling we don't want with microservices.
* The unfiltered git history is mixed for the different services.
* Every developer gets access to all code, even when they are assigned to work on one service.
