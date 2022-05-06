
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

This article is about an axiom of constructive mathematics.  Some set thoery literature instead uses this name for an unrelated weakening of [[axiom of choice|AC]].  For that notion, see [[(classical) axiom of multiple choice]]

## Idea

The **axiom of multiple choice** (AMC) can refer to one several weaker versions of the [[axiom of choice]]. Two categorical ones are weakenings of [[COSHEP]], which can hold in [[constructive mathematics]]. There is also an older set theoretic axiom by the same name, which is historically unrelated and not equivalent (as far as I know).  Other nlab pages typically refer to a categorical version.


## Statement (Categorical Version)

A set-indexed family $\{D_c\}_{c\in C}$ of sets is said to be a *collection family* if for any $c\in C$ and any [[surjection]] $E\twoheadrightarrow D_c$, there exists a $c'\in C$ and a surjection $D_{c'}\twoheadrightarrow D_c$ which factors through $E$.

Depending on the author, the *axiom of multiple choice* is one of the following statements:

1. for every set $X$, there exists a collection family $\{D_c\}_{c\in C}$ such that $X\cong D_c$ for some $c$ ([[Michael Rathjen]]'s formulation, attributed to [[Peter Aczel]] and [[Alex Simpson]]), or

1. for every set $X$, there exists a collection family $\{D_c\}_{c\in C}$, with $C$ inhabited, and a family of surjections $\{D_c \to X\}_{c\in C}$ (the formulation originally given by [[Ieke Moerdijk]] and [[Erik Palmgren]]), or 

1. for every set $X$, the full subcategory $(Set/X)_{surj}$ of the slice category $Set/X$ consisting of the surjections has a weakly initial set (in [[Benno van den Berg]]'s formulation; this is also called [[WISC]]).

The nLab uses the initialization AMC to cover either the first two formulations.

+--{: .query}
[[Mike Shulman]]: Are the first two the same?  If not, why are they given the same name?

[[Peter LeFanu Lumsdaine]]: Yes, they are equivalent.  For any $X$, given a collection family $\{D_c\}_{c \in C}$ including $X$, then the family $\{D_c\}_{(c \in C, f : D_c \twoheadrightarrow X)}$” is an inhabited collection family equipped with surjections to $X$.  Conversely, given an inhabited collection family equipped with surjections to $X$, throwing $X$ into the family gives a collection family including $X$. 
=--

The third is a weaker condition, and while some may refer to as a "weak axiom of multiple choice", van den Berg obviously does not; he calls his the AMC and the Moerdijk-Palmgren formulation rather the "strong axiom of multiple choice". 


##Statement (Set-Theoretic Version)

One common statement of the axiom of choice is: 

:For every set $S$ of non-empty sets, there is a function $f$ defined on $S$ such that $\forall X\in S$, $f(X)\in X$.

Such an $f$ is called a __choice function__ for $S$.

The axiom of multiple choice weakens the axiom of choice by allowing choice functions to pick out finite subsets, rather than finite sets.  It says:

:For every set $S$ of non-empty sets, there is a function $f$ defined on $S$ such that $\forall X\in S$, $f(X)\subseteq X$ and $f(X)$ is finite.

The axiom of multiple choice is actually equivalent to the axiom of choice modulo [[ZF]] set thoery.  However, it is strictly weaker in [[ZFA]] and other similar set theories.  More details can be found in [Jech's "The Axiom of Choice](https://www.gwern.net/docs/math/1973-jech-theaxiomofchoice.pdf)
+--{: .query}
[[Brian Pinsky]]: Does someone know an appropriate version of this statement to make in more general topoi than $\textsc{Set}$?  I'd like to flesh out the relationship of this axiom to others weakenings of AC more

=--


## Relationships to other axioms

* Note that $P$ is a [[projective set]] if and only if the singleton family $\{P\}$ is a collection family.  Therefore, since AC is equivalent to "all sets are projective," it implies categorical AMC.

* An extension of this argument shows that [[COSHEP]] is sufficient to imply AMC.

* The [[Reflection Principle]] (RP) is equivalent to AMC (the one called strong AMC by van den Berg). RP is motivated by the regular extension principle (REA) from constructive set theory. RP states that every map belongs to a representable class of small maps.

* However, none of these AMC does not imply [[countable choice]] or any of the other usual consequences of AC.

* Rathjen proves that [[SVC]] also implies categorical AMC.  It follows that AMC holds in "most" models of set theory.

* categorical AMC implies [[WISC]], and therefore also implies that the category of [[anafunctors]] between two [[small categories]] is [[essentially small category|essentially small]]. Thus WISC may be termed "weak axiom of multiple choice".

* A [[ΠW-pretopos]] satisfying the (weak) axiom of multiple choice is a _[[predicative topos]]_, or removing the word "weak", we may speak of a strong predicative topos.

## References

* [[Ieke Moerdijk]], [[Erik Palmgren]], _Type theories, toposes and constructive set theory: predicative aspects of AST_ (2000) ([web](http://citeseerx.ist.psu.edu/viewdoc/summary?doi=10.1.1.34.8934))

* Rathjen, "Choice principles in constructive and classical set theories"

In 

* [[Benno van den Berg]], _Predicative toposes_ ([arXiv:1207.0959](http://arxiv.org/abs/1207.0959))
 {#vdBerg}


[[WISC]] is called the "axiom of multiple choice".

* Jech, _The Axiom of Choice_ (1973), ISBN : 0444104844 (New York)


category: foundational axiom

[[!redirects axiom of multiple choice]]
[[!redirects multiple choice]]
[[!redirects AMC]]
