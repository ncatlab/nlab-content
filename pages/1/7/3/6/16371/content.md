
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

The concept of an **open subtopos** generalizes the concept of an open subspace from topology to toposes.

## Definition

Let $U$ be a [[subterminal object]] of a [[topos]].  Then $o_U(V)\coloneqq (U\Rightarrow V)$ defines a [[Lawvere-Tierney topology]] on $\mathcal{E}$, whose corresponding [[subtopos]] is called the _open subtopos_ associated to $U$.

The reflector into the topos of sheaves can be constructed explicitly as $O_U(X) = X^U$.

A _topology_ that is of this form for some subterminal object $U$ is called _open_.

## Example

In case $\mathcal{E}=Sh(X)$ is the topos of sheaves on a topological space $X$, a subterminal object is just an open subset $U$ of $X$ and the open subtopos corresponding to it is equivalent to $Sh(U)$.

As one would expect from the topological situation, for any topos $\mathcal{E}$, the empty subtopos (given by $o(V) \coloneqq (\bot \Rightarrow V) = \top$) and $\mathcal{E}$ itself (given by $o(V) \coloneqq (\top \Rightarrow V) = V$) are open subtoposes of $\mathcal{E}$.

### Remark

The [[subterminal object]] $U$ in $\mathcal{E}$ is associated with a [[closed subtopos]] $Sh_{c(U)}(\mathcal{E})$ as well e.g. in the case of $\mathcal{E}=Sh(X)$ on a space $X$ this yields $Sh(X\setminus U)$.

Moreover, given a [[Lawvere-Tierney topology]] $j$ on a topos $\mathcal{E}$ with corresponding subtopos $Sh_j(\mathcal{E})\hookrightarrow\mathcal{E}$, we a get a canonical [[subterminal object]] $ext(j)$  associated to $j$ by taking the $j$-closure of $O\rightarrowtail 1$. The corresponding closed and open subtoposes associated to $ext(j)$ provide a '_closure_' $Sh_{c(ext(j))}(\mathcal{E})$, respectively, an '_exterior_' $Sh_{o(ext(j))}(\mathcal{E})$ for $Sh_j(\mathcal{E})$ (cf. [SGA4](#SGA4), p.461). More on this [below](#ext_int).

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

### Remark

Whereas, general [[open geometric morphisms|open morphisms]] are only bound to preserve [[first order logic]], open _inclusions_ preserve also [[higher order logic]] since their [[inverse image|inverse images]] are logical.

That the inverse image is logical is a special case of the general fact that the pullback functor $\mathcal{E}\to\mathcal{E}/X$ along $X\to 1$ is logical for arbitrary objects $X$. In particular, $Sh_{o(U)}(\mathcal{E})\cong\mathcal{E}/U$.

## Open localizations

Subtoposes of a topos $\mathcal{E}$ correspond to [[localization|localizations]] of $\mathcal{E}$ i.e. replete, reflective subcategories whose reflector preserves finite limits. Just as this notion makes sense more generally for categories with finite limits, the notion of open localization makes sense more generally for [[locally presentable category|locally presentable categories]]:

Given a locally $\alpha$-presentable category $\mathcal{C}$ with subcategory of $\alpha$-presentable objects $\mathcal{P}$, the subobject $\Omega_\mathcal{C}$ of the subobject classifier of $Set^{\mathcal{P}^{op}}$ given by $\Omega_\mathcal{C}(P):=$ set of $\alpha$-exact subpresheaves of $\mathcal{P}(\text{_},P)$, classifies subobjects of $\mathcal{C}$. Furthermore, localizations of $\mathcal{C}$ correspond to topologies $j:\Omega_\mathcal{C}\to\Omega_\mathcal{C}$.

At this level of generality, an open subtopos of a Grothendieck topos corresponds to the notion of an **open localization** of a [[locally presentable category]] that is studied in [Borceux-Korotenski (1991)](#BK91). The main result in their paper is the following

+-- {: .num_prop}
###### Proposition
Let $l\dashv i: \mathcal{D}\hookrightarrow\mathcal{C}$ be a localization of a [[locally presentable category]] $\mathcal{C}$. The localization is called _open_ if the following equivalent conditions are satisfied:

* The corresponding [[closure operator]] admits a universal dense interior operator.

* The associated [[Lawvere-Tierney topology|topology]] $j_\mathcal{D}:\Omega_\mathcal{C}\to\Omega_\mathcal{C}$ has a left adjoint.

* The localization is [[essential geometric morphism|essential]] with $k\dashv l$ and, additionally, the first of the following diagrams[^adj] being a pullback implies the second being a pullback, too:

$$\array{
D&\overset{d}{\to}&D'\\
f\downarrow&p.b.&\downarrow g\\
lC&\underset{lc}{\to}&lC'
}

\qquad\Rightarrow
\qquad

\array{
kD&\overset{kd}{\to}&kD'\\
\bar{f}\downarrow&p.b.&\downarrow \bar{g}\\
C&\underset{c}{\to}&C'
}\quad .$$ 
=--

[^adj]: Here $f$ corresponds to $\bar{f}$, resp. $g$ to $\bar{g}$, under the adjunction $k\dashv l$.

In case $\mathcal{C}$ is a topos, $i:\mathcal{D}\hookrightarrow\mathcal{C}$ is an open subtopos.

Open localizations are special cases of **essential localizations**, and are in general better behaved than the latter. For example, the meet of two essential localizations in the lattice of essential localizations does not coincide with their meet in the lattice of localizations. Compare this with the following 

+-- {: .num_prop}
###### Proposition
Let $\mathcal{C}$ a [[locally presentable category]]. The meet of two open localizations in the lattice of localizations is an open localization.
=--

cf. [Borceux-Korotenski (1991, p.235)](#BK91).

+-- {: .num_prop #open_supremum}
###### Proposition
Let $\mathcal{C}$ a [[locally presentable category]] where unions are [[universal colimit|universal]]. The supremum of a family of open localizations in the lattice of all localizations is again an open localization.
=--

cf. [Borceux-Korotenski (1991, p.236)](#BK91).

This applies e.g. to Grothendieck toposes since they are locally presentable and colimits are universal.

+-- {: .num_prop #open_supremum}
###### Proposition
Let $\mathcal{C}$ a [[locally presentable category]] where unions are [[universal colimit|universal]]. The open localizations in $\mathcal{C}$ constitute a [[locale]].
=--

cf. [Borceux-Korotenski (1991, p.237)](#BK91).

The following proposition closes the circle and recovers the primordial example of sheaf subtoposes $Sh(U)$ on open subsets $U$ as a special case:

+-- {: .num_prop}
###### Proposition
Let $\mathcal{C}$ a [[locally presentable category]] in which colimits are [[universal colimit|universal]]. Then the [[locale]] of open localizations of $\mathcal{C}$ is isomorphic to the locale of [[subterminal object|subterminal objects]] of $\mathcal{C}$.
=--

cf. [Borceux-Korotenski (1991, p.238)](#BK91).

## Open subtoposes associated to a subtopos {#ext_int}

Let $Sh_j(\mathcal{E})\hookrightarrow\mathcal{E}$ be a subtopos of a (Grothendieck) topos with corresponding [[Lawvere-Tierney topology|topology]] $j$. From [prop. \ref{open_supremum}](#open_supremum) it follows that the supremum of the family of all open subtoposes contained in $Sh_j(\mathcal{E})$ is open again and, since it coincides with the supremum in the lattice of all localizations, is contained in $Sh_j(\mathcal{E})$. Clearly, it is the biggest open subtopos contained in $Sh_j(\mathcal{E})$ and therefore called the **interior** of $Sh_j(\mathcal{E})$, denoted by $Sh_{o(int(j))}(\mathcal{E})$ and the corresponding [[subterminal object]] by $int(j)$.

Whereas the other open subtopos $Sh_{o(ext(j))}(\mathcal{E})$ connected with $Sh_j(\mathcal{E})$ corresponding to $ext(j)$ is the biggest open subtopos disjoint from $Sh_j(\mathcal{E})$ i.e. its exterior. Then the sum $Sh_{o(ext(j))}(\mathcal{E}) \vee Sh_{o(int(j))}(\mathcal{E})$ is open again and corresponds to the subterminal object $ext(j)\vee int(j)$. Its closed complement $Sh_{c(ext(j)\vee int(j))}(\mathcal{E})$ is called the boundary of $Sh_j(\mathcal{E})$ in ([SGA 4](#SGA4), p. 461).
 
For some further details see at [[dense subtopos]].

## Related pages

* [[open geometric morphism]]
* [[locally closed subtopos]]
* [[closed subtopos]]
* [[dense subtopos]]
* [[localization]]
* [[level]]
* [[Artin gluing]]
* [[co-Heyting boundary]]

## References

* {#SGA4}[[M. Artin]], [[A. Grothendieck]], [[J. L. Verdier]], _Th&#233;orie des Topos et Cohomologie Etale des Sch&#233;mas ([[SGA4]])_, LNM **269** Springer Heidelberg 1972. (Expos&#233; IV 9.2, 9.3.4-9.4., pp.451ff)

* {#BK91}[[Francis Borceux|F. Borceux]], M. Korostenski, _Open Localizations_ , JPAA **74** (1991) pp.229-238.

* C. Getz, M. Korostenski, _Open Localizations and Factorization Systems_ , Quest. Math. **17** no.2 (1994) pp.225-230.

* {#Johnstone77}[[Peter Johnstone]], _Topos Theory_ , Academic Press New York 1977. (Dover reprint 2014, pp.93-95)

* {#Johnstone80}[[Peter Johnstone]], _Open maps of toposes_ , Manuscripta Math. **31** (1980) pp.217-247. ([gdz](http://gdz.sub.uni-goettingen.de/dms/load/img/?PPN=GDZPPN002222744))

* {#Johnstone} [[Peter Johnstone]], _[[Sketches of an Elephant]] vols. I,II_, Oxford UP 2002. (A4.5., pp.204-220; C3.1.5-7, pp.609f)

[[!redirects open subtoposes]]
[[!redirects open topology]]
[[!redirects open localization]]
[[!redirects open localisation]]