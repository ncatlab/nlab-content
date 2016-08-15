
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

Let $(\wedge^\bullet V, d)$ be a [[semifree dg-algebra]] being a [[Sullivan model]] of a [[rational space|rational]] [[simply connected space]] $X$. Then a Sullivan model for the [[free loop space]] $\mathcal{L} X$ is given by

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

(e.g. [F&#233;lix-Oprea-Tanre 08](#FelixOpreaTanre08), [Felix-Halperin-Thomas 00, p. 206](#FelixHalperinThomas00))

+-- {: .num_remark}
###### Remark


The formula in prop. \ref{SullivanModelForTheFreeLoopSpace} is the same as that for the [[Weil algebra]] of the [[L-infinity algebra]] of wich $(\wedge^\bullet V,d)$ is the [[Chevalley-Eilenberg algebra]], except that here $s$ shifts _down_ whereas for the Weil algebra it shifts _up_.

=--

## References

* {#FelixOpreaTanre08} [[Yves Félix]], John Oprea, Daniel Tanre, _Algebraic models in geometry_, Oxford graduate texts in mathematics 17 (2008)

* {#FelixHalperinThomas00} [[Yves Félix]], [[Steve Halperin]] and J.C. Thomas, _Rational Homotopy Theory_, Graduate Texts in Mathematics, 205, Springer-Verlag, 2000. 

[[!redirects Sullivan models of free loop space]]

[[!redirects Sullivan model of the free loop space]]
[[!redirects Sullivan models of the free loop space]]

[[!redirects Sullivan model of a free loop space]]
[[!redirects Sullivan models of a free loop space]]

[[!redirects Sullivan models of free loop spaces]]
