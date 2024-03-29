+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}

### Context
#### Category theory
+-- {: .hide}
[[!include category theory - contents]]
=--
#### Topos Theory
+-- {: .hide}
[[!include topos theory - contents]]
=--
=--
=--

# Contents
* table of contents
{:toc}

[[!redirects Von Neumann regular categories]]
[[!redirects Von Neumann regular category]]
[[!redirects von Neumann regular categories]]

## Idea

**Von Neumann regular categories**, or _regular categories_ for short, are a class of [[small categories]] introduced by [[William Lawvere]] ([2002](#Law02)) in the context of his theory of dimension and [[unity of opposites]] in order to provide [[presheaf toposes]] with well-behaved [[level of a topos|levels]] which in particular admit the [[Aufhebung]] of each level.

As shown in ([Kelly-Lawvere 1989](#KL89)) essential subtoposes of presheaf toposes $\mathcal{S}^{\mathcal{C}^{op}}$ correspond to idempotent two-sided ideals $J$ of the underlying small category $\mathcal{C}$. What causes the problems for the general existence of Aufhebung at each level is the fact that an infinite intersection of such $J$ is not necessarily idempotent itself. The condition occurring in the definition of a von Neumann regular category is a simple way to enforce this.

## Definition

A small category $\mathcal{C}$ is called _von Neumann regular_ if all two-sided ideals are [[idempotent]].

## Remark

The terminology is presumably chosen in view of the concept of a _von Neumann regular ring_ $R$ i.e. one such that every $a \in R$ has a 'weak inverse' $\bar{a}$ with $a = a \bar{a} a$ as the following property illustrates. 

## Properties

* $\mathcal{C}$ is von Neumann regular iff  for any morphism $a$ in $\mathcal{C}$ there exists a reverse morphism $\bar{a}$ and two endomorphisms $x,y$ with $a=y a \bar{a} a x$. ([Lawvere 2002](#Law02))

## Related entries

* [[Aufhebung]]

* [[graphic category]]

* [[level of a topos]]

## References

* [[Francis Borceux|F. Borceux]], [[Jiri Rosicky|J. Rosicky]], _On Von Neumann Varieties_ , TAC **13** no. 1 (2004) pp.5-26. ([pdf](http://www.tac.mta.ca/tac/volumes/13/1/13-01.pdf))

* {#KL89}[[G. M. Kelly]], [[F. W. Lawvere]], _On the Complete Lattice of Essential Localizations_ , Bull.Soc.Math. de Belgique **XLI** (1989) 261-299 &lbrack;[[Kelly-Lawvere_EssentialLocalizations.pdf:file]]&rbrack;

* {#Law89b} [[F. W. Lawvere]], _Display of graphics and their applications, as exemplified by 2-categories and the Hegelian "taco"_ , Proceedings of the first international conference on algebraic methodology and software technology University of Ioowa, May 22-24 1989, Iowa City, pp.51-74. 

* {#Law02} [[F. W. Lawvere]], _Linearization of graphic toposes via Coxeter groups_ , JPAA **168** (2002) pp.425-436.