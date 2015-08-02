
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

The concept of a **open subtopos** generalizes the concept of a open subspace from topology to toposes.

## Definition

Let $U$ be a [[subterminal object]] of a [[topos]].  Then $o_U(V)\coloneqq (U\Rightarrow V)$ defines a [[Lawvere-Tierney topology]] on $\mathcal{E}$, whose corresponding [[subtopos]] is called the _open subtopos_ associated to $U$.

The reflector into the topos of sheaves can be constructed explicitly as $O_U(X) = X^U$.

A _topology_ that is of this form for some subterminal object $U$ is called _open_.

## Example

In case $\mathcal{E}=Sh(X)$ is the topos of sheaves on a topological space $X$, a subterminal object is just an open subset $U$ of $X$ and the open subtopos corresponding to it is equivalent to $Sh(U)$.

### Remark

The [[subterminal object]] $U$ in $\mathcal{E}$ is associated with a [[closed subtopos]] $Sh_{c(U)}(\mathcal{E})$ as well e.g. in the case of $\mathcal{E}=Sh(X)$ on a space $X$ this yields $Sh(X\setminus U)$.

Moreover, given a [[Lawvere-Tierney topology]] $j$ on a topos $\mathcal{E}$ with corresponding subtopos $Sh_j(\mathcal{E})\hookrightarrow\mathcal{E}$, we a get a canonical [[subterminal object]] $ext(j)$  associated to $j$ by taking the $j$-closure of $O\rightarrowtail 1$. The corresponding closed and open subtoposes associated to $ext(j)$ provide a '_closure_' $Sh_{c(ext(j))}(\mathcal{E})$, respectively, an '_exterior_' $Sh_{o(ext(j))}(\mathcal{E})$ for $Sh_j(\mathcal{E})$ (cf. [SGA4](#SGA4), p.461).

## Properties

+-- {: .num_prop}
###### Proposition
Let $Sh_j(\mathcal{E})\hookrightarrow\mathcal{E}$ be a subtopos with corresponding topology $j$. The following are equivalent:

* $j$ is open.
* The [[associated sheaf functor]] $L:\mathcal{E}\to Sh_j(\mathcal{E})$ is [[logical functor|logical]].
* $Sh_j(\mathcal{E})\hookrightarrow\mathcal{E}$ is an [[open geometric morphism]].

=--

See Johnstone ([1980](#Johnstone80), pp.219-220; [2002](#Johnstone02), pp.609-610).

+-- {: .num_prop}
###### Proposition
Let $U$ a [[subterminal object]] and $Sh_{c(U)}(\mathcal{E})$ and $Sh_{o(U)}(\mathcal{E})$ the corresponding closed, resp. open subtoposes. Then $Sh_{c(U)}(\mathcal{E})$ and $Sh_{o(U)}(\mathcal{E})$ are [[complement|complements]] for each other in the [[lattice of subtoposes]].
=--

See Johnstone [(2002, pp.212,215)](#Johnstone).

## Related pages

* [[open geometric morphism]]
* [[locally closed subtopos]]
* [[closed subtopos]]
* [[dense subtopos]]
* [[Artin gluing]]
* [[co-Heyting boundary]]

## References

* {#SGA4}[[M. Artin]], [[A. Grothendieck]], [[J. L. Verdier]], _Th&#233;orie des Topos et Cohomologie Etale des Sch&#233;mas ([[SGA4]])_, LNM **269** Springer Heidelberg 1972. (Expos&#233; IV 9.2, 9.3.4-9.4., pp.451ff)

* [[Francis Borceux|F. Borceux]], M. Korostenski, _Open Localizations_ , JPAA **74** (1991) pp.229-238.

* {#Johnstone77}[[Peter Johnstone]], _Topos Theory_ , Academic Press New York 1977. (Dover reprint 2014, pp.93-95)

* {#Johnstone80}[[Peter Johnstone]], _Open maps of toposes_ , Manuscripta Math. **31** (1980) pp.217-247. ([gdz](http://gdz.sub.uni-goettingen.de/dms/load/img/?PPN=GDZPPN002222744))

* {#Johnstone} [[Peter Johnstone]], _[[Sketches of an Elephant]] vols. I,II_, Oxford UP 2002. (A4.5., pp.204-220; C3.1.5-7, pp.609f)

[[!redirects open subtoposes]]
[[!redirects open topology]]
