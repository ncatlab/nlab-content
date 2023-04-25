+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Topos theory
+--{: .hide}
[[!include topos theory - contents]]
=--
#### Cohomology
+--{: .hide}
[[!include cohomology - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

A **quaternionic set** is a [[simplicial set]] with a [[quaternion group|quarternionic]] symmetry, in other words it is a [[presheaf]] on the quaternionic simplex category $\Delta Q$ which contains the ordinary [[simplex category]] $\Delta$ and an opposite [[quaternion group]] $Q_{n+1}^{op}$ as the automorphism group at the objects $[n]$, whence quaternionic sets are an example of an [[skew-simplicial set|crossed simplicial object]].

## Definition

Let $Q_n$ be the [[group]] given by the [[group presentation|presentation]] $\{x,y| x^n  = y^2\;,y x y^{-1}=x^{-1}\}$, hence the $n$th [[quaternion group]], also called a *[[binary dihedral group]]*.

\begin{definition}\label{Definition}
The **quaternionic simplex category**[^term] $\Delta Q$ has objects $[n],\; n\geq 0\;$, contains the (topologists’) [[simplex category]] $\Delta$ as a (non-[[full subcategory|full]]) [[wide subcategory]] and each [[object]] $[n]$ has as [[automorphism group]] the ([[opposite group|opposite]] of the) $n+1$st [[quaternion group]]: $Aut_{\Delta Q}([n]) = Q_{n+1}^{op}$. 

Furthermore, any [[morphism]] $\varphi:[m]\to [n]$ in $\Delta Q$ can be uniquely factored as $\varphi = s\circ q$ with $s:[m]\to [n]\in \Delta$ and $q\in Q_{m+1}^{op}$. 

A **quaternionic set** is a [[presheaf]] on $\Delta Q$.
\end{definition}

[^term]: Since $\Delta Q$ encapsulates exactly the structure of $Q_*$ (i.e. the simplicial set that has fibers $Q_{n+1}$ at $[n]$ together with simplicially compatible actions) it is also referred to as the _quaternionic crossed simplicial group_. The terminology used at [[crossed group]] would refer to it as the _total category_ of the [[skew-simplicial set|crossed simplicial group]] $Q_*$.

## Properties

* According to the classification of [[crossed group|crossed simplicial groups]], $\Delta Q$ or, more precisely, the equivalent crossed group $Q_*$ corresponds to the [[exact sequence]] of crossed groups $1\to \mathbb{Z}/2\to Q_*\to D_*\to 1\; .$ Whence it is of _dihedral type_ and, accordingly, the [[model category]] techniques for planar crossed simplicial groups apply (cf. [Spaliński](#Spalinski95), [Balchin](#Balchin18)).

* The [[geometric realization]] of $Q_*$ is the normalizer of $S^1$ in $S^3$ (cf. [Loday](#Loday87)).

* As usual for [[crossed group|crossed groups]] (or, more generally, for functors between small categories that are surjective on objects; cf. [[Sheaves in Geometry and Logic|Moerdijk-Maclane]], pp.359, 377f), the inclusion $i:\Delta\to \Delta Q$ induces by [[Kan extension]] an [[essential geometric morphism|essential]] [[surjective geometric morphism]] $i_!\vdash i^*\vdash i_*: Set^{\Delta^{op}}\to Set^{\Delta Q^{op}}\;$. Here the [[inverse image]] $i^*:Set^{\Delta Q^{op}}\to Set^{\Delta^{op}}$ extends a presheaf $P$ on $\Delta Q$ to one on $\Delta$ by precompostion: $i^*(P)=P\circ i^{op}\,$.

* Just like in the [[cyclic set|cyclic]] and [[dihedral set|dihedral]] cases, $\Delta Q$ is _self-dual_: $\Delta Q\cong \Delta Q^{op}$ (cf. [Dunn](#Dunn89), prop.1.4).

* Since $i:Set^{\Delta^{op}}\to Set^{\Delta Q^{op}}$ is surjective, it follows again by generalities (e.g. [[Sheaves in Geometry and Logic|Moerdijk-Maclane]], p.372) that $Set^{\Delta Q^{op}}$ is (equivalent to) the category of coalgebras for a [[left exact]] [[comonad]] on $Set^{\Delta^{op}}$ whence quaternionic sets are indeed [[simplicial set|simplicial sets]] enhanced with a quaternionic coalgebra structure. (For an explicit description of the free [[skew-simplicial set]] on a [[simplicial set]] and the corresponding monad for general crossed groups $G_*$ see [Krasauskas](#Krasauskas87).)

* Truncating $\Delta Q$ at $[1]$ and taking presheaves, one obtains a _category of quaternionic graphs_ $Set^{\Delta Q_{\leq 1}^{op}}$ with a $Q_2$ action, just like [[graphic category|reflexive graphs]] result from $\Delta_1$, resp. reversible graphs from truncating $\Delta S$ in the [[symmetric set|symmetric simplex category]].

## Related entries

* [[skew-simplicial set]]

* [[crossed group]]

* [[cyclic set]]

* [[dihedral set]]

* [[quaternion]]


## References

* {#Loday87}[[Jean-Louis Loday]], _Homologies diédrale et quaternionique_, Adv. in Math. **66** (1987) pp.119-148.

* {#Dunn89}Gerald Dunn, _Dihedral and Quaternionic Homology and Mapping Spaces_, K-theory **3** (1989) pp.141-161.

* {#Spalinski95}[[Jan Spalinski|Jan Spaliński]], _Homotopy theory of dihedral and quaternionic sets_, Topology **39** (1995) pp.35-52.

* {#Krasauskas87}R. Krasauskas, _Skew-simplicial groups_, Lithuanian Math. J. **27** pp.47-54 (1987).

* {#FL91}Zbigniew Fiedorowicz, [[Jean-Louis Loday]], _Crossed simplicial groups and their associated homology_, Trans. AMS **326** pp.57-87 (1991).

* [[Tobias Dyckerhoff]], [[Mikhail Kapranov]], _Crossed simplicial groups and structured surfaces_, arXiv:1403.5799 (2014). ([abstract](https://arxiv.org/abs/1403.5799))

* {#Balchin18}[[Scott Balchin]], _Homotopy of planar Lie group equivariant presheaves_, J. Homotopy Relat. Struct. **13** (2018) pp.555-580. ([doi](https://doi.org/10.1007/s40062-017-0193-z))



