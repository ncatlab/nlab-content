
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Rational homotopy theory
+--{: .hide}
[[!include differential graded objects - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

In [[rational homotopy theory]], given a [[rational space]] modeled by a [[Sullivan model]] [[dg-algebra]], there is an explicit description of the Sullivan model of its [[free loop space]].

## Construction

+-- {: .num_prop #SullivanModelForTheFreeLoopSpace}
###### Proposition

Let $(\wedge^\bullet V, d)$ be a [[semifree dg-algebra]] being a [[minimal Sullivan model]] of a [[rational space|rational]] [[simply connected space]] $X$. Then a Sullivan model for the [[free loop space]] $\mathcal{L} X$ is given by

$$
  (\wedge^\bullet( V \oplus s V ), d')
  \,,
$$

where

* $s V$ is the [[graded vector space]] obtained from $V$ by shifting degrees down by one: $deg(s v) = deg(v)-1$;

* $d'$ is defined on elements $v$ of $V$ by 


  $$
    d' v \coloneqq d v
  $$

  and on elements $s v$ of $s V$ by

  $$
    d' s v \coloneqq - s ( d v )
    \,,
  $$

  where on the right $s \colon V \to s V$ is extended as a graded [[derivation]] $s \colon \wedge^2 V \to \wedge^\bullet (V \oplus s V) $.

=--

This is due to ([Vigu&#233;-Sullivan 76](#VigueSullivan76)). Review includes ([Felix-Halperin-Thomas 00, p. 206](#FelixHalperinThomas00), [Hess 06, example 2.5](#Hess06), [F&#233;lix-Oprea-Tanre 08, theorem 5.11](#FelixOpreaTanre08)).

+-- {: .num_remark}
###### Remark


The formula in prop. \ref{SullivanModelForTheFreeLoopSpace} is the same as that for the [[Weil algebra]] of the [[L-infinity algebra]] of wich $(\wedge^\bullet V,d)$ is the [[Chevalley-Eilenberg algebra]], except that here $s$ shifts _down_ whereas for the Weil algebra it shifts _up_.

=--

## Related concepts

* [[Hochschild homology]]

## References

* {#VigueSullivan76} [[Micheline Vigué-Poirrier]], [[Dennis Sullivan]], _The homology theory of the closed geodesic problem_, J. Differential Geometry 11 (1976) 633-644.

* {#VigueBurghelea85} [[Micheline Vigué-Poirrier]], Dan Burghelea, _A model for cyclic homology and algebraic K-theory of 1-connected topological spaces_, J. Differential Geom. Volume 22, Number 2 (1985), 243-253 ([Euclid](https://projecteuclid.org/euclid.jdg/1214439821))

* {#FelixHalperinThomas00} [[Yves Félix]], [[Steve Halperin]] and J.C. Thomas, _Rational Homotopy Theory_, Graduate Texts in Mathematics, 205, Springer-Verlag, 2000. 

* {#Hess06} [[Kathryn Hess]], _Rational homotopy theory: a brief introduction_ ([arXiv](http://arxiv.org/abs/math.AT/0604626))

* {#FelixOpreaTanre08} [[Yves Félix]], John Oprea, Daniel Tanre, _Algebraic models in geometry_, Oxford graduate texts in mathematics 17 (2008)

* A. Yu. Onishchenko and Th. Yu. Popelensky, _Rational cohomology of the free loop space of a simply connected 4-manifold_, J. Fixed Point Theory Appl. 12 (2012) 69&#8211;9 ([DOI 10.1007/s11784-013-0100-0](http://link.springer.com/article/10.1007/s11784-013-0100-0))

[[!redirects Sullivan models of free loop space]]

[[!redirects Sullivan model of the free loop space]]
[[!redirects Sullivan models of the free loop space]]

[[!redirects Sullivan model of a free loop space]]
[[!redirects Sullivan models of a free loop space]]

[[!redirects Sullivan models of free loop spaces]]
