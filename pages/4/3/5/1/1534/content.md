
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Higher algebra
+--{: .hide}
[[!include higher algebra - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

A _factorization algebra_ is like an [[algebra over an operad]] where the [[operad]] in question is like the [[E-k operad]], but with each disk embedded into a given [[manifold]] $X$.

This way a factorization algebra is an assignment of a [[object]] (in the standard case a vector space) $V_D$ to each ball $D \subset X$ embedded in $X$, and for each collection of non-intersecting embedded balls $D_1 , \cdots, D_n \subset D \subset X$ sitting inside a bigger embedded ball $D$ in $X$ a morphism

$$
  V_{D_1} \otimes V_{D_2} \otimes \cdots \otimes V_{D_n} \to V_{D}
$$

such that for every collection of further nested balls inside balls, all the different ways to bracket

$$
  V_{D_{11}} \otimes V_{D_{12}} \otimes \cdots \otimes V_{D_{1 n}}
  \otimes V_{D_{21}} \otimes V_{D_{2 2}} \otimes \cdots \to V_D
  \,.
$$
+-- {: .standout}
Is there a condition missing here? I don't understand the definition. Maarten Bergvelt 
=--
This is pretty much like saying that the factorization algebra is an extended [[FQFT]] of genus 0 [[cobordisms]] that are embedded into $X$.

Indeed, such factorization algebras serve to describe [[quantum field theories]] on $X$, pretty much in a way that generalizes the familiar way that 2-dimensional [[conformal field theory]] is given by [[vertex operator algebras]]. See also the comments on the references below.


## Related concepts

Factorization algebras have some similarity with 

* [[blob homology]]

* [[local net]]s in [[AQFT]].


## References

This may be regarded as a slight variation on the concept _chiral algebra_ originally introduced by Beilinson and Drinfeld.

A definition appears in section 4.1 _Topological Chiral Homology_ of

* [[Jacob Lurie]], _[[On the Classification of Topological Field Theories]]_

There it is demonstrated how factorization algebras can be used to construct extended [[FQFT]]s.

Concrete constructions of formal algebras for familiar [[quantum field theory|quantum field theories]] are described in 

* [[Kevin Costello]] (with [[Owen Gwilliam]]), _Factorizaton algebras in perturbative quantum field theory_ in [[Oberwolfach Workshop, June 2009 -- Strings, Fields, Topology|Strings, Field, Topology]], Oberwolfach report No 28, 2009 ([pdf](http://www.mfo.de/programme/schedule/2009/24/OWR_2009_28.pdf#page=12))

This can also be found mentioned in the talk notes of the [[Northwestern TFT Conference 2009]], see in particular

* notes by  [[Christoph Wockel]], [[costello.pdf:file]]

* notes by Evan Jenkins on the same talk: [Factorization algebras in perturbative quantum gravity](http://www.math.uchicago.edu/~ejenkins/notes/nwtft/25may-kc.pdf)

More is at

* [[Kevin Costello]], [[Owen Gwilliam]], _Factorization algebras in perturbative quantum field theory_ ([wiki](http://math.northwestern.edu/~costello/factorization_public.html))

There seems to be a close relation between the description of [[quantum field theory]] by factorization algebras and the proposal presented in 

* Stefan Hollands ([arXiv](http://arxiv.org/abs/0802.2198))

[[!redirects factorization algebras]]