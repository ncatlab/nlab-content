
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Homotopy theory
+--{: .hide}
[[!include homotopy - contents]]
=--
#### Representation theory
+-- {: .hide}
[[!include representation theory - contents]]
=--
#### Rational homotopy theory
+--{: .hide}
[[!include differential graded objects - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}


## Definition


Let $G$ be a [[finite group]] (or more generally a [[compact Lie group]]). 

Say that an equivariantly [[connected topological space|connected]] and [[nilpotent topological space|nilpotent]] [[topological G-space]] $Y$ (i.e. all [[fixed loci]] $X^H$ are connected and nilpotent, for $H \subset_{clsd} G$, with a common bound of nilpotency as $H$ ranges) is _rational_ if all its [[equivariant homotopy groups]] $\pi_n\big( X^H \big)$ (for $n \in \mathbb{N}$ and $H \subset_{cld} G$) admit the [[mathematical structure|structure]] of [[rational vector spaces]].


Given any [[topological G-space]] $X$, a _rationalization_ of $X$ is a morphism (a $G$-[[equivariant function|equivariant]] [[continuous function]]) 

$$
  X 
    \overset{
      \;\;\; \eta^{\mathbb{Q}}_X \;\;\;
    }{\longrightarrow}
  L_{\mathbb{Q}}X
$$  

to a rational $G$-space $L_{\mathbb{Q}}X$ which induces [[isomorphisms]] on all rationalized equivariant homotopy groups:

$$
  \big(
    \eta^{\mathbb{Q}}_X(G/H)
  \big)_\ast
  \;\colon\;
  \pi_\bullet( X^H )
  \otimes \mathbb{Q}
  \overset{\simeq}{\longrightarrow}
  \pi_\bullet
  \Big(
     \big(
       L_{\mathbb{Q}}X
     \big)^H
  \Big)
  \,.
$$

## Properties

### Via Elmendorf's theorem

In other words, after regarding them, via [[Elmendorf's theorem]], as [[(∞,1)-presheaves]] on the [[orbit category]] $G Orbits$ of $G$, the [[equivariant homotopy types]] of rational $G$-spaces and their rationalizations are equivalently stage-wise over $G/H \in G Orbits$ plain [[rational spaces]] and [[rationalizations]], respectively.

It follows from the [[fundamental theorem of dg-algebraic equivariant rational homotopy theory]] that, at least on equivariantly [[simply connected topological space|simply connected]] [[topological G-spaces]], equivariant rationalization is given by the [[derived adjunction|derived]] [[adjunction unit]] of the [[equivariant PL de Rham complex]]-[[Quillen adjunction]].



## Related concepts

* [[rational equivariant homotopy theory]]

* [[rational stable equivariant homotopy theory]]


## References

* {#May96} [[Peter May]], Section II.3 in: _Equivariant homotopy and cohomology theory_, CBMS Regional Conference Series in Mathematics, vol. 91, Published for the Conference Board of the Mathematical Sciences, Washington, DC, 1996. With contributions by M. Cole, G. Comezana, S. Costenoble, A. D. Elmenddorf, J. P. C. Greenlees, L. G. Lewis, Jr., R. J. Piacenza, G. Triantafillou, and S. Waner. ([ISBN: 978-0-8218-0319-6](https://bookstore.ams.org/cbms-91/?startBookmarkIdx=200)  [pdf](https://web.math.rochester.edu/people/faculty/doug/otherpapers/alaska1.pdf), [[MayEtAlEquivariant96.pdf:file]])


* [[Georgia Triantafillou]], Section 2.6 in _Equivariant minimal models_, Trans. Amer. Math. Soc. vol 274 pp 509-532 (1982) ([jstor:1999119](http://www.jstor.org/stable/1999119))

* [[Laura Scull]], p. 11 of: _A model category structure for equivariant algebraic models_, Transactions of the American Mathematical Society 360 (5), 2505-2525, 2008 ([doi:10.1090/S0002-9947-07-04421-2](https://doi.org/10.1090/S0002-9947-07-04421-2))


[[!redirects equivariant rationalizations]]

[[!redirects rational G-space]]
[[!redirects rational G-spaces]]


[[!redirects rational topological G-space]]
[[!redirects rational topological G-spaces]]

