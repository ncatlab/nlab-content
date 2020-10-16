
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Topos Theory
+-- {: .hide}
[[!include topos theory - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}
## Idea
An atomic topos is a topos $\mathcal{E}$ where the global sections functor $\Gamma: \mathcal{E} \to Set$ is [[atomic geometric morphism|atomic]]. In the case where $\mathcal{E}$ is a Grothendieck topos, there are some (arguably more explicit) alternative characterizations of atomic toposes, as in Theorem \ref{EquivChar}, which make it clearer why they are called "atomic".

## Definition

Recall that a [[geometric morphism]] $f$ is called [[atomic geometric morphism|atomic]] if its [[inverse image functor]] $f^*$ is [[logical functor|logical]].

+-- {: .num_defn}
###### Definition

A [[topos]] over a [[base topos]] $\Gamma : \mathcal{E} \to \mathcal{S}$ is called an **atomic topos** if $\Gamma$ is [[atomic geometric morphism|atomic]]. Unless otherwise specified, the base topos will be taken to be $Set$.
=--

+-- {: .num_defn}
###### Definition
A non-zero object $A$ of a topos $\mathcal{E}$ is an [[atom]] if its only subobjects are $A$ and $0$.
=--

+-- {: .num_theorem #EquivChar}
###### Theorem
Let $\mathcal{E}$ be a [[Grothendieck topos]]. Then the following are equivalent:

1. $\mathcal{E}$ is an atomic topos.

1. $\mathcal{E}$ is the [[category of sheaves]] on an [[atomic site]].

1. The [[subobject lattice]] of every object of $\mathcal{E}$ is a [[complete lattice|complete]] [[atomic Boolean algebra]].

1. $\mathcal{E}$ has a [[small set|small]] [[generating set]] of atoms.

1. Every object of $\mathcal{E}$ can be written as a disjoint union of atoms.
=--

+-- {: .proof}
###### Proof
See [Johnstone, C3.5.8](#Johnstone) and [Barr-Diaconescu, Theorem A](#Barr-Diaconescu80).
=--

## Properties
+-- {: .num_prop}
###### Proposition
Let $\mathcal{E}$ be an atomic topos. Then $\mathcal{E}$ is Boolean.
=--

This appears as one direction of ([Johnstone, cor. C3.5.2](#Johnstone)).

+-- {: .proof}
###### Proof

If $\Gamma^*$ is logical then it preserves the isomorphism $* \coprod * \simeq \Omega$ characterizing a [[Boolean topos]].
=--

+-- {: .num_prop}
###### Proposition

Let $\mathcal{E}$ be a [[Boolean topos|Boolean]] [[Grothendieck topos]] with [[point of a topos|enough points]]. Then $\mathcal{E}$ is an atomic topos.
=--

+-- {: .proof}
###### Proof
See ([Johnstone, cor. C3.5.2](#Johnstone))
=--

+-- {: .num_prop}
###### Proposition
Atomic Grothendieck toposes $Sh(\mathcal{C}, J_{at})$ for $(\mathcal{C}, J_{at})$ an [[atomic site]] are precisely the [[double negation|double negation subtoposes]] $Sh_{\neg\neg}(Set^{\mathcal{C}^{op}})$ for a [[De Morgan topos|De Morgan]] [[presheaf topos]] $Set^{\mathcal{C}^{op}}$. 
=--
+-- {: .proof}
###### Proof
For the argument see at [[atomic site]].
=--

### Decomposition of atomic toposes

Atomic toposes decompose as [[disjoint unions]] of [[connected topos|connected]] atomic toposes. Connected atomic toposes with a [[point of a topos|point]] are the [[classifying toposes]] of [[localic groups]].

An example of a connected atomic topos without a [[point of a topos|point]] is given in ([Johnstone, example D3.4.14](#Johnstone})).

## Examples

*  A [[category of presheaves]] $Set^{\mathcal{C}^{op}}$ is atomic precisely iff $\mathcal{C}$ is a groupoid (cf. [Barr-Diaconescu (1980)](#Barr-Diaconescu80)).

* Another example of an atomic Grothendieck topos is the [[Schanuel topos]]. More generally, any [[category of G-sets]] is an atomic Grothendieck topos.


## Related concepts

* [[atomic geometric morphism]]

* [[atomic site]]

* [[connected topos]]

## References

* {#Barr-Diaconescu80}[[Michael Barr]], [[Radu Diaconescu]], _Atomic Toposes_ , JPAA **17** (1980) pp.1-24. ([pdf](http://www.math.mcgill.ca/barr/papers/atom.top.pdf))

* [[Olivia Caramello]], _Atomic toposes and countable categoricity_ , Appl. Cat. Struc. **20** no. 4 (2012) pp.379-391. ([arXiv:0811.3547](http://arxiv.org/abs/0811.3547))

* {#Johnstone}[[Peter Johnstone]], _[[Sketches of an Elephant]] vol. 2_ , Oxford UP 2002. (section C3.5, pp.684-695)

[[!redirects Atomic topos]]
[[!redirects atomic toposes]]
[[!redirects atomic topoi]]