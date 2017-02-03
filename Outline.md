# Behavior Driven Development

__What We Do Today__
- Examples of different styles of tests
  - naming, assertions, etc
- Less-than-meaningful tests
- focus only on unit tests

__Introduction / History__
- Dan North ~2006
- Quick recap of TDD
- Define BDD as development methodology in which we focus on the behavior of an application from an outside in point of view.
  - Unit tests confirm that you built it right, whereas acceptance tests (BDD) confirm you built the right thing.

__5 Whys__
- Asking why repeatedly help uncover the root cause of a problem.

__Focus__
- system behavior
- test scope
- test naming

__Benefits__
- Naming conventions help keep tests small and in the right place
- BDD reinforces the ubiquitous language between developers, testers, and domain experts
- End up with executable requirements
- Better prioritization of work
    - puts us in the mindset of "what's the next most important thing the system should do?"

__Requirements are Behavior__
```
As a [role],
I want to [action / feature],
So that [benefit / value]
```
- A story's behavior is its acceptance criteria. If a feature fulfills its acceptance criteria, then it is behaving correctly.

# Executable Specifications
_Description of behavior in natural language, but with a defined structure_
Translate criteria understood by business into testable code
  - Business gains more confidence system is working correctly.

__Different tests for different stakeholders__
- feature tests for product owner
- technical tests for architect (how)
- negative tests for unusual/invalid uses

__The Domain-Specific Language of BDD__
```
Given [context],
  And [more context],
When [event],
Then [outcome],
  And [another outcome]
```
__Given:__ The purpose of givens is to put the system in a known state before the user starts interacting with the system.<br/>
__When:__ The purpose of When steps is to describe the key action the user performs.<br/>
__Then:__ The purpose of Then steps is to observe outcomes.

### __User Stories and Scenarios__
- User story example (Consultant re-enrollment)
- Break sub-tasks into BDD scenarios

# [__SpecFlow__](http://specflow.org/getting-started/)
- BDD testing framework that is part of Cucumber family and uses Gherkin parser
- Allows us to write our acceptance criteria using DSL and map to executable code
- [Features, Scenarios](https://github.com/cucumber/cucumber/wiki/Feature-Introduction), and [steps](https://github.com/cucumber/cucumber/wiki/Given-When-Then)
  - feature files and step definitions
- Regex in Given-When-Then
  - allow reuse with minimal effort
- tags (@myTag)
  - used to filter scenarios and control execution (BeforeScenario)
- [hooks](http://specflow.org/documentation/Hooks/)
  - same type of setup/tear-down as other testing frameworks

Implement example for user story above (Consultant re-enrollment)
