
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Topos Theory
+-- {: .hide}
[[!include topos theory - contents]]
=--
=--
=--


# Contents
* table of contents
{:toc}

## Definition

A **Boolean topos** is a [[topos]] that is also a [[Boolean category]].

There are several conditions on a topos that are necessary and sufficient to be Boolean:

* Every [[subobject]] has a complement (the general definition of Boolean category).
* Every [[subobject poset|subobject lattice]] is a [[Boolean algebra]].
* The [[subobject classifier]] $\Omega$ is an [[internalization|internal]] Boolean algebra.
* The maps $\top, \bot: 1 \to \Omega$ are a [[coproduct]] cone (so in particular, $\Omega \cong 1 + 1$, and in fact this is enough, because the map $[\top, \bot]: 1 + 1 \to \Omega$ is always a monomorphism, and any monic endomorphism of $\Omega$ is an automorphism).
* Every [[pointed object]] is a [[free object|free]] pointed object. This was proven [here](https://golem.ph.utexas.edu/category/2023/01/freedom.html#c062002) by [[Morgan Rogers]]. 

### Warning

Let $C$ be a Boolean pretopos, i.e. a [[pretopos]] in which is also a [[Boolean category]], and let $Sh(C)$ be the [[classifying topos]] for $C$. Then it does *not* follow that $Sh(C)$ is Boolean. In fact, this is rarely the case, even if $C$ is the classifying pretopos for a theory in classical first-order logic. See [Blass and Scedrov](#BlassScedrov75) for a characterization of which classical first-order theories have Boolean classifying topoi -- in particular, any such theory is $\aleph_0$-[[categoricity|categorical]]. Nevertheless, as discussed below, [[Barr's theorem]] shows that any topos admits a surjection from a Boolean topos.

## Properties

### As a context for foundations

The [[internal logic]] of a Boolean topos with [[natural numbers object]] can serve as [[foundations]] for "ordinary" mathematics, except for that which relies on the [[axiom of choice]].  If you add the axiom of choice, then you get (an internal version of) [[ETCS]]; conversely, if you use an arbitrary topos, then you get [[constructive mathematics]].  (For some high-powered work, you may also need to add a version of the [[axiom of replacement]] or an axiom of [[Grothendieck universe]]s.)

Every [[cartesian closed category|cartesian closed]] Boolean [[pretopos]] is in fact a topos.  This is why 'generalised [[predicative mathematics|predicativism]]' (with function types but not power types) is necessarily a feature of [[constructive mathematics]] only.

### Some characterisations

+-- {: .num_prop}
###### Proposition

For $\mathcal{E}$ a [[topos]], then the following are equivalent:

1. $\mathcal{E}$ is a Boolean topos;

1. Every [[subtopos]] of $\mathcal{E}$ is Boolean.

1. Every [[subtopos]] of $\mathcal{E}$ is an [[open subtopos]].

1. Every [[subtopos]] of $\mathcal{E}$ is a [[closed subtopos]].

=--

([Johnstone, prop. A 4.5.22](#Johnstone))


+--{: .num_prop}
###### Proposition
Let $j$ be a [[Lawvere-Tierney topology]] on $\mathcal{E}$. Then $\mathcal{E}_j$ is Boolean iff there exists a [[subterminal object]] $U$ such that $j$ is the largest topology such that $U\rightarrowtail 1$ is $j$-closed, or equivalently, that $U$ is a $j$-sheaf.
=--

Topologies $j$ satisfying the latter condition are called **quasi-closed** and sometimes denoted $q(U)$. They can also be described by the Heyting algebra operations on $\Omega$ as the composite

$$\Omega\simeq\Omega\times 1\overset{1\times(\chi_U,\chi_U)}{\to}\Omega\times\Omega\times\Omega\overset{\Rightarrow\times 1}{\to}\Omega\times \Omega\overset{\Rightarrow}{\to}\Omega\quad .$$
The corresponding quasi-closed subtoposes $Sh_{q(U)}(\mathcal{E})$ are the double negation subtoposes $Sh_{\neg\neg}(Sh_{c(U)}(\mathcal{E}))$ of the [[closed subtopos|closed subtoposes]] $Sh_{c(U)}(\mathcal{E})$ corresponding to the [[subterminal object]] $U$.

For a proof of the proposition and the other assertions see [(Johnstone 2002, p.220)](#Johnstone). We can deduce from this a description of the ordering on Boolean subtoposes.

+--{: .num_prop}
###### Proposition
$\mathcal{E}_{q(U)} \subseteq \mathcal{E}_{q(U')}$ as subtoposes of $\mathcal{E}$ if and only if $U \supseteq U'$ and $U = (U \Rightarrow U') \Rightarrow U'$.
=--

**Proof**. The closure of $\mathcal{E}_{q(U)}$ (meaning the smallest closed subtopos containing it) is $\mathcal{E}_{c(U)}$, so the ordering on the $q(U)$ must be a sub-ordering of that on the closed subtoposes, which is the opposite of that on the subterminals of $\mathcal{E}$ indexing them. Conversely, given $U \supseteq U'$, the inclusion $\mathcal{E}_{c(U)} \subseteq \mathcal{E}_{c(U')}$ restricts to the double-negation subtoposes if and only if it is [[skeletal geometric morphism|skeletal]], which by [Johnstone, Lemma D4.6.10](#Johnstone) requires that the exterior of the corresponing Lawvere-Tierney topology in $\mathcal{E}_{c(U')}$ is a $\neg\neg$-closed subterminal object. The exterior is simply $U$; asking that $U = \neg\neg U$ in $\mathcal{E}_{c(U')}$ translates to asking that $U = (U \Rightarrow U') \Rightarrow U'$ in the Heyting algebra of subterminal objects of $\mathcal{E}$.

+--{: .num_prop}
###### Proposition
$\mathcal{E}$ is Boolean iff the only dense subtopos of $\mathcal{E}$ is $\mathcal{E}$ itself.
=-- 

**Proof**.  Suppose $\mathcal{E}$ is Boolean. $\mathcal{E}_{\neg\neg}=\mathcal{E}$ is the smallest dense subtopos (cf. [[double negation]]{#boolean_subtopos}).
Conservely, suppose $\mathcal{E}$ is not Boolean then $\mathcal{E}_{\neg\neg}$ is a second dense subtopos.

+-- {: .num_prop}
###### Proposition

In a [[lattice of subtoposes]] the 2-valued Boolean toposes are the [[atoms]]. 

=--

See [this proposition](subtopos#BooleantoposesAreAtoms).

+-- {: .num_prop}
###### Proposition

Let $\mathcal{E}$ be a topos. Then automorphisms of $\Omega$ correspond bijectively to [[closed subtopos|closed]] Boolean subtoposes. The group operation on $Aut(\Omega)$ corresponds to symmetric difference of subtoposes.

=--

This result appears in [Johnstone (1979)](#Johnstone79). (See also [Johnstone (2002)](#Johnstone), A1.6.11 pp.66-67.)

## Examples

- With [[excluded middle]] in the meta-logic, every [[well-pointed topos]] is a Boolean topos. This includes [[Set]] and models of [[ETCS]]. 

- The topos of [[G-sets]] for a group $G$ is always a Boolean topos, because the set-theoretic complement of a sub-$G$-set is itself a sub-$G$-set.

- More generally, a [[presheaf topos]] on a category $C$ is Boolean if and only if $C$ is a [[groupoid]].

- The topos of sheaves on a [[Boolean algebra]] $B$ for the [[coherent category|coherent topology]] is Boolean if and only if the Boolean algebra is finite. Indeed, in $Sh(B)$ the sections of $\Omega$ over $b \in B$ are the ideals of $\downarrow b \leqslant B$, while those of $1+1$ are the principal ideals, and these coincide just when $B$ is finite.

- The topos of [[canonical topology|canonical]] sheaves on a complete [[Boolean algebra]] is Boolean (note this includes the finite case above). 

- If $\mathcal{E}$ is any topos, the category of [[sheaf|sheaves]] for the [[double negation|double-negation topology]] is a Boolean [[subtopos]] of $\mathcal{E}$. 

- Any topos satisfying the [[axiom of choice]] is Boolean. This result is due to R. Diaconescu ([1975](#Diaconescu75)); see [[excluded middle]] for a brief discussion. 

- [[Barr's theorem]] implies that any topos $\mathcal{E}$ can be covered by a Boolean topos $\mathcal{F}$, in the sense of there being a [[surjective geometric morphism]] $f \colon \mathcal{F} \to \mathcal{E}$. 

## Relation to measure theory

Boolean toposes are closely related to [[measurable spaces]] (e.g [Jackson 06](#Jackson06), [Henry 14](#Henry14)).

## Related entries

* [[Boolean category]]

* [[Boolean domain]]

* [[excluded middle]]

* [[double negation]]

* [[axiom of choice]]

* [[de Morgan topos]]

## References

### General

* {#BlassScedrov75} [[Andreas Blass]], Andrej Scedrov, _Boolean Classifying Topoi_ , JPAA **28** (1983) pp.15-30.

* {#Diaconescu75}Radu Diaconescu, _Axiom of Choice and Complementation_ , Trans. AMS **51** no.1 (1975) pp.176-178. ([pdf](http://www.ams.org/journals/proc/1975-051-01/S0002-9939-1975-0373893-X/S0002-9939-1975-0373893-X.pdf))


* {#Johnstone79}[[Peter Johnstone]], _Automorphisms of $\Omega$_ , Algebra Universalis **9** (1979) pp.1-7.

* {#Johnstone} [[Peter Johnstone]], _[[Sketches of an Elephant]] vols. I,II_, Oxford UP 2002. (A4.5.22, D3.4, D4.5)

### Relation to measure theory
 {#ReferencesRelationToMeasureTheory}

On relation of Boolean toposes to [[measure theory]]:

* {#Jackson06} Matthew Jackson, _A sheaf-theoretic approach to measure theory_, 2006. ([pdf](http://www.andrew.cmu.edu/~awodey/students/jackson.pdf), [d-scholarship:7348](http://d-scholarship.pitt.edu/7348))

* {#Henry14} [[Simon Henry]], _Measure theory over boolean toposes_, Mathematical Proceedings of the Cambridge Philosophical Society, 2016 ([arXiv:1411.1605](https://arxiv.org/abs/1411.1605))

* [[Asgar Jamneshan]], [[Terence Tao]], _Foundational aspects of uncountable measure theory: Gelfand duality, Riesz representation, canonical models, and canonical disintegration_ ([arXiv:2010.00681](arXiv:2010.00681))

 

[[!redirects Boolean topos]]
[[!redirects boolean topos]]
[[!redirects Boolean topoi]]
[[!redirects boolean topoi]]
[[!redirects Boolean toposes]]
[[!redirects boolean toposes]]