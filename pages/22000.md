
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Foundations
+-- {: .hide}
[[!include foundations - contents]]
=--
=--
=--


# The axiom of multiple choice
* table of contents
{: toc}

This article is about a [[classical mathematics|classical]] [[set theory]] [[axiom]].  Some literature instead uses this name for an unrelated weakening of [[axiom of choice|AC]].  For that notion, see _[[axiom of multiple choice]]_.

## Idea

The **axiom of multiple choice** (AMC) weakens the [[axiom of choice]] by allowing [[choice functions]] to choose [[finite sets]], rather than particular [[elements]].

##Statement

Recall that one common statement of the [[axiom of choice]] is: 

:For every [[set]] $S$ of [[inhabited set|non-empty sets]], there is a [[function]] $f$ defined on $S$ such that $\forall X\in S$, $f(X)\in X$.

Such an $f$ is called a __choice function__ for $S$.

The axiom of multiple choice weakens the axiom of choice by allowing choice functions to pick out finite [[subsets]], rather than finite sets.  It says:

:For every set $S$ of non-empty sets, there is a function $f$ defined on $S$ such that $\forall X\in S$, $f(X)\subseteq X$ and $f(X)$ is finite.



## Relationships to other axioms

The axiom of multiple choice is [[logical equivalence|equivalent]] to the axiom of choice modulo [[ZF]] set thoery.  However, it is strictly weaker in [[ZFA]] and other similar set theories.  AMC holds in any [[permutation model]] with finite supports where each atom has a finite orbit.  For a detailed proof, see [Jech's "The Axiom of Choice"](https://www.gwern.net/docs/math/1973-jech-theaxiomofchoice.pdf), chapter 9.

The [[axiom of multiple choice|constructive axiom by the same name]] is not historically related, and the two axioms are independent.  Any permutation model will satisfy [[SVC]], which implies Rathjen proves implies the constructive axiom, but this AMC can fail in a permutation model.


## References

* Rathjen, "Choice principles in constructive and classical set theories"


* Jech, _The Axiom of Choice_ (1973), ISBN : 0444104844 (New York)


category: foundational axiom
