# CS 351 Lecture 2: Basic Concepts and Principles (Terminology Day!!!)

## What is Computer Security?

* There's not necessarily a simple answer
  * "Defending data and its processing from unintended disclosure, misuse, or interference"
  * Protecting computer-related assets from unauthorized actions/consequences by either preventing said actions or detecting and recovering from them.
* What are some supporting ideas?
  * *Authentication:* The belief that a principal, data, or software is genuine relative to the expectations from appearances/context.
    * Cryptography is a critical aspect of authentication
  * *Accountability:* The ability to identify the principals responsible for past actions. AKA *attribution*.
  * *Trustworthy:* A principal, data, or software that will reliably meet expectations. (A good thing.)
  * *Trusted:* A principal, data, or software is depended upon to meet expectations (Not a good thing.)
  * *Privacy:* Assurance that *personally sensitive* information will be protected and its use will be controlled.
* Security policy
  * Specifies the design intent of a system's rules and practices (Read the Duke ones!!!)
* Vulnerabilities and Attacks
  * *Attack(s):* The deliberate execution of one or more steps intended to cause a security violation.
  * *Attack Vector:* Specific methods or sequences of steps by which attacks are carried out.
  * *Vulnerability:* A system characteristic that enables an attack to succeed in violating policy.
  * *Adversary:* The principal (typically a person or org) that conducts the attack

## Applying the terminology

* Risk Assessment
  * Predicting losses due to future security threats is notoriously difficult
  * Doing this for intelligent human attackers is damn near hopeless.
    * Capabilities and motivations evolve over time.
    * This is especially true for targeted attacks.
  * Attaching a value to an intangible asset is...imprecise to say the least.
* Security Evaluations
  * It is more tractable to just try and find vulnerabilities
  * Security evals can take many different forms
    * Third party evaluation labs
    * Penetration testing (red teaming)
    * Automated/manual analysis of software artifacts to identify weaknesses
      * E.g. fuzzing
