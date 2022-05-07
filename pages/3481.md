
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

The **axiom of multiple choice** (AMC) is a weaker version of the [[axiom of choice]], which can hold in [[constructive mathematics]]. 


## Statement

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




## Relationships to other axioms

* Note that $P$ is a [[projective set]] if and only if the singleton family $\{P\}$ is a collection family.  Therefore, since AC is equivalent to "all sets are projective," it implies AMC.

* An extension of this argument shows that [[COSHEP]] is sufficient to imply AMC.

* The [[Reflection Principle]] (RP) is equivalent to AMC (the one called strong AMC by van den Berg). RP is motivated by the [[regular extension axiom]] (REA) from constructive set theory. RP states that every map belongs to a representable class of small maps.

* However, AMC does not imply [[countable choice]] or any of the other usual consequences of AC.

* Rathjen proves that [[SVC]] also implies AMC.  It follows that AMC holds in "most" models of set theory.

* AMC implies [[WISC]], and therefore also implies that the category of [[anafunctors]] between two [[small categories]] is [[essentially small category|essentially small]]. Thus WISC may be termed "weak axiom of multiple choice".

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
