
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Homotopy theory
+--{: .hide}
[[!include homotopy - contents]]
=--
#### Cohomology
+--{: .hide}
[[!include cohomology - contents]]
=--
#### Duality
+--{: .hide}
[[!include duality - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}


## Idea

[[Beno Eckmann|Eckmann]] and [[Peter Hilton|Hilton]] noticed that a number of notions and theorems in the [[homotopy theory]] of [[pointed spaces]] can be dualized in the sense of certain expanding dictionary:

* [[homotopy]] -- [[cohomology]]

* [[fibration]]  -- [[cofibration]]

* [[mapping cylinder]] -- [[mapping cocylinder]]

* [[suspension]] $\Sigma X$ -- [[loop space]] $\Omega X$

* [[homotopy lifting property]] -- [[homotopy extension property]]

The "duality" in their work has been just a heuristic rather than a systematic algorithm to [[duality|dualize]] constructions and theorems. It has a little flavour of working with [[adjoint functors]], though it does not reduce to Kan adjointness. It has also the flavour of the usual arrow reversal duality, as is commented below.

Later some versions have been made rigorous, the most well-known being Fuks duality in homotopy theory.

## Fuks duality

D. B. Fuks considers the category $End(k Top_*)$ of [[endofunctors]] on the category $k Top_*$ of pointed [[compactly generated space|compactly generated]] Hausdorff spaces. He enriches this category in $k Top_*$ as follows: Let $S,T$ be two endofunctors, then the set $\{S\to T\}$ of isomorphism classes of natural transformations $S\to T$ is equipped with the weakest topology in which all maps $\alpha_X$, $X\in k Top_*$, of taking components $\{S\to T\}\mapsto Map(S(X),T(X))\in kTop_*$ are [[continuous map|continuous]]. Recall that the topology on the set of maps $S(X)\to T(X)$ in $k Top_*$ is obtained by first taking the [[compact-open topology]] and then performing the [[kaonization]] of the space so obtained. 

Notice that if $[-,A]$ is a [[representable functor]] in the classical homotopy category of $k Top_*$, then for any endofunctors $S$ and $T$ we have 

$$\{[-,A]\to S\} = S A,$$ 

$$ [ \{S\to T\},A ] = \{S\to [T(-),A]\} = \{ A \wedge S\to T\}.$$ 

A **Fuks duality** is any functor $D: End(k Top_*)\to End(k Top_*)$ such that 

1. for any two functors $S,T\in End(k Top_*)$, $\{S\to D T\}$ is binaturally homeomorphic to
$\{D S\to T\}$ 

2. $D\Sigma =\Omega$, $D\Omega = \Sigma$.

+-- {: .un_theorem}
###### Theorem (D. B. Fuks)
There exists a unique Fuks duality functor. Moreover it is given by $DS:A\mapsto \{S\to [-,A]\}$ where $[,]$ denotes the homotopy classes and $\{,\}$ is defined as above.
=--

Notice that $D^2 = D\circ D$ is **not** isomorphic to the [[identity functor|identity]] in general, though it is identical when applied to a number of natural endofunctors in homotopy theory. Fuks duality can be extended suitably to functors of many arguments. 

This duality to some extent resembles the usual categorical duality for objects by **arrow reversal**. The reason is seen in the formula for $D S$ above, which can be interpreted as arrow reversal for representable functors. 
In a more perfect world, like [[model categories]], the axioms are self-dual and a true categorical duality of the usual categorical kind holds for basic model-categorical notions. On the other hand Eckmann--Hilton duality is not only about the notions entering the axioms of model categories but there are dualities among a number of interesting homotopy theoretical functors in topological context. 

One can see this in the fact that [[cohomology group]]s (for [[integral cohomology|ordinary cohomology]] using the [[Eilenberg-Mac Lane spectrum]]) consist of [[homotopy]] classes of maps into a space with a single nontrivial [[homotopy group]], while homotopy groups consist of homotopy classes of maps from a space with a single nontrivial cohomology group:

* $H^n(X, \mathbb{Z}) \cong [X, K(\mathbb{Z},n)]$
* $\pi_n(X) \cong [S^n, X]$

Here, $K(\mathbb{Z},n)$ is an [[Eilenberg-Mac Lane space]], whose only interesting homotopy group is $\pi_n(K(\mathbb{Z},n)) = \mathbb{Z}$, while $S^n$ is a [[sphere]], whose only interesting ordinary cohomology group is the $H^n(S^n,\mathbb{Z}) = \mathbb{Z}$.

Note, though, that the arrow reversal duality does not hold perfectly in [[Top]] (the arrow reversal "dual" theorems are not necessarily true).
For example, a [[pullback]] of a cofibration by a fibration is a cofibration, but a pushforward of a fibration by a cofibration is not a fibration.

## References

* D. B. Fuks, On duality in homotopy theory, Soviet Math. Dokl. 2 (1961), 1575--1578.

* D. B. Fuks, Eckmann--Hilton duality and the theory of functors in the category of topological spaces, 1966 Russ. Math. Surv. 21 1--33 [doi](http://dx.doi.org/10.1070/RM1966v021n02ABEH004149), [free Russian original pdf](http://www.mathnet.ru/php/getFT.phtml?jrnid=rm&paperid=5847&what=fullt&option_lang=rus)

* R. Nakagawa, On Fuks homotopy duality, Sci. Rep. Tokyo Kyoiku Daigaku Sect. A 8 (1963), 93--98. 

* Encyclopedia of Mathematics: [Eckmann-Hilton duality](http://eom.springer.de/E/e120020.htm)

Some blog discussion on Eckmann-Hilton duality is
[here](http://golem.ph.utexas.edu/category/2008/09/group_cocycles_and_simplices.html#c019087),
[here](http://golem.ph.utexas.edu/category/2008/09/mathematical_miniatures.html#c019103),
and
[here](http://golem.ph.utexas.edu/category/2009/06/cohomology_and_homotopy.html#c024807)


[[!redirects Fuks duality]]
[[!redirects Fuchs duality]]
[[!redirects Eckmann–Hilton duality]]
[[!redirects Eckmann--Hilton duality]]