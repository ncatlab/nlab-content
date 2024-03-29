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

## Idea

The concept of a **closed subtopos** generalizes the concept of a [[closed subspace]] from topology to toposes.

## Definition

Let $U$ be a [[subterminal object]] of a [[topos]] $\mathcal{E}$.  Then $c_U(V) \coloneqq U\cup V$ defines a [[Lawvere-Tierney topology]] on $\mathcal{E}$, whose corresponding [[subtopos]] is called the _closed subtopos_ associated to $U$.

The reflector into the sheaves can be constructed explicitly as the [[join]] with $U$, i.e. $C_U(X)$ is the [[pushout]] of $X$ and $U$ under $X\times U$.

A _topology_ $j$ that is of this form for some [[subterminal object]] $U$ is called _closed_.

## Example

In case $\mathcal{E}=Sh(X)$ is the topos of sheaves on a topological space $X$, a subterminal object is just an open subset $U$ of $X$ and the closed subtopos corresponding to it is equivalent to $Sh(X\setminus U)$.

## Remark

The [[subterminal object]] $U$ in $\mathcal{E}$ is associated with an [[open subtopos]] $Sh_{o(U)}(\mathcal{E})$ as well e.g. in the case of $\mathcal{E}=Sh(X)$ on a space $X$ this yields $Sh(U)$.

Moreover, given a [[Lawvere-Tierney topology]] $j$ on a topos $\mathcal{E}$ with corresponding subtopos $Sh_j(\mathcal{E})\hookrightarrow\mathcal{E}$, we a get a canonical [[subterminal object]] $ext(j)$  associated to $j$ by taking the $j$-closure of $O\rightarrowtail 1$. The corresponding closed and open subtoposes associated to $ext(j)$ provide a '_closure_' $Sh_j(\mathcal{E})\hookrightarrow Sh_{c(ext(j))}(\mathcal{E})$, called _l'adh&#233;rence_ in ([[SGA4]], p.461), respectively, an '_exterior_' $Sh_{o(ext(j))}(\mathcal{E})$ for $Sh_j(\mathcal{E})$.

## Properties

+-- {: .num_prop}
###### Proposition
Let $U$ a [[subterminal object]] and $Sh_{c(U)}(\mathcal{E})$ and $Sh_{o(U)}(\mathcal{E})$ the corresponding closed, resp. open subtoposes. Then $Sh_{c(U)}(\mathcal{E})$ and $Sh_{o(U)}(\mathcal{E})$ are [[complement|complements]] for each other in the [[lattice of subtoposes]].
=--

For the proof see ([Johnstone (2002)](#Johnstone), pp.212,215).

Closed subtoposes that are [[Boolean topos|Boolean]] are parametrized by automorphisms of the [[subobject classifier]] as the next proposition documents:

+-- {: .num_prop}
###### Proposition

Let $\mathcal{E}$ be a topos. Then automorphisms of $\Omega$ correspond bijectively to closed Boolean subtoposes. The group operation on $Aut(\Omega)$ corresponds to symmetric difference of subtoposes.

=--

This result appears in [Johnstone (1979)](#Johnstone79).

The following result is a part of the so called [[(dense,closed)-factorization]].

+-- {: .num_prop #dense-closed}
###### Proposition
Let $i:Sh_{c(U)}(\mathcal{E})\hookrightarrow\mathcal{E}$ be dominant and a closed inclusion at the same time. Then $i$ is an isomorphism.
=--

**Proof**: Recall that $X\in\mathcal{E}$ are in the closed subtopos precisely when they satisfy $X\times U\cong U$ with $U$ the [[subterminal object]] associated to $i$. But $i$ is dominant, or what comes to the same for inclusions: dense, hence $\emptyset$ is in $Sh_{c(U)}(\mathcal{E})$ and therefore $\emptyset\times U\cong U$ . From this follows $U\cong\emptyset$, which in turn implies that all $X\in\mathcal{E}$ are in $Sh_{c(U)}(\mathcal{E})$ . $\qed$

This says that the only closed subtopos of a topos $\mathcal{E}$ that is dense, is $\mathcal{E}$ itself.

It follows e.g. that [[Boolean toposes|Boolean toposes]] have no non-trivial dense subtoposes since all their subtoposes are closed (and open, as well). Of course, this follows also from the fact that a Boolean topos coincides with its [[double negation|double negation subtopos]] and the latter is the _smallest dense_ subtopos!

## Related pages

* [[(dense,closed)-factorization]]
* [[open subtopos]]
* [[locally closed subtopos]]
* [[dense subtopos]]
* [[Artin gluing]]
* [[closed subspace]]

## References

* {#SGA4}[[M. Artin]], [[A. Grothendieck]], [[J. L. Verdier]], _Th&#233;orie des Topos et Cohomologie Etale des Sch&#233;mas ([[SGA4]])_, LNM **269** Springer Heidelberg 1972. (Expos&#233; IV 9.3.4-9.4., pp.456ff)

* [[Peter Johnstone]], _Topos Theory_ , Academic Press New York 1977. (Dover reprint 2014, pp.93-95)

* {#Johnstone79}[[Peter Johnstone]], _Automorphisms of $\Omega$_ , Algebra Universalis **9** (1979) pp.1-7.

* {#Johnstone} [[Peter Johnstone]], _[[Sketches of an Elephant]] vol. I_, Oxford UP 2002. (A4.5., pp.204-220)

[[!redirects closed subtoposes]]
[[!redirects closed topology]]
