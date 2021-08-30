# CS 351 Lecture 3: Hello Crypto My Old Friend...I've Come to Talk to You Again

We're gonna cover modern crypto on speed mode, so expect a treatment but not a strictly *thorough* treatment. Subsequent lectures will be much more thorough than this...

## What Even is Cryptography?

* The study of techniques to communicate securely in the presence of some *adversary*.
* Traditional scenario:
  * Alice and Bob want to establish a dedicated, private connection but some eavesdropper (Eve?) wants to listen in
* Eve's objectives are as follows
  * Observe *what* Alice and Bob are communicating
    * Attacks on "confidentiality" or "secrecy"
  * Observe *that* Alice and Bob are communicating, or *how much* they're communicating
    * This is called "traffic analysis"
    * Sometimes just knowing where the messages are going is good enough...
  * *Modify* the communication between Alice and Bob
    * Attacks on *integrity*
  * *Impersonate* Alice to Bob, or vice versa
  * *Deny* Alice and Bob the ability to communicate
    * *Denial of Service*
  * Cryptography traditionally focuses on preventing observation and detecting modification and impersonation!

## Who is the Adversary?

* For our study, we don't care *who* the attacker is, but we care about their resources.
  * The adversary's computational power
  * The resources in the adversary's environment at his disposal
* Alice, Bob, and the adversary are usually modeled as *probabilistic polynomial-time (PPT) Turing machines*
  * For some fixed polynomial `p`, machine halts in `p(|x|)` steps on input `x`
  * Machine can "flip coins" i.e, select from a set of possible transitions randomly
* Cryptographic algos are typically specified in terms of a *security parameter* lambda that specifies the length of inputs.
* Ergo, we want cryptographic algos that such that: 
  * Alice and Bob can compute efficiently, i.e. in time p(lambda) for some polynomial `p`
  * No (PPT) adversary can defeat with more than "negligible probability" for sufficiently large lambda.
    * What is negligible probability then?
      * A function v: N ==> R is negligible if for every positive polynomial `p` there exists an `N` such that for all lambda > `N`: v(lambda) < 1/p(lambda)
      * Any event that occurs with negligible probability would still occur with negligible probability if the experiment were repeated polynomially many times (in lambda)

## One-Way Functions

A *collection* of one-way functions is a set of functions such that for every PPT `A` there is a negligible v_A such that the probability of the adversary succeeding is bounded from above for all lambda large enough.