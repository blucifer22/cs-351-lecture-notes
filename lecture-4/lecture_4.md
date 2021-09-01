# CS 351 Lecture 4: More Crypto Challenges

## On the Issue of Oracles

* The adversary doesn't do their work in a vacuum
  * The adversary may be able to sign a message as Bob by just tricking Bob into signing it for him
* The environment of the adversary may be augmented with oracles that compute certain functions for the adversary
  * Formally a PPT adversary is augmented with new query and response tapes for each oracle
  * Notation: If A is an adversary, then A' is an adversary with access to an oracle for function f

## Attacks Against Digital Signature Schemes

* Types of Attacks
  * Key-Only Attack: Adversary only knows K
  * Known Signature Attack: The adversary knows K and has seen <m, sigma> pairs made by Sk-1, but not chosen by the adversary
  * Chosen Message Attack: The adversary knows K and is given an oracle for Sk-1
* When does the adversary succeed?
  * Existential Forgery: There exists a forged message, not strictly of their choice
  * Selective Forgery: The adversary successfully forges the signature of some message of his choice
  * Universal Forgery: The adversary is able to forge any arbitrary signature.
  * Total Break: The adversary gets the key. 100% compromised.
  