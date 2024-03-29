
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Higher algebra
+--{: .hide}
[[!include higher algebra - contents]]
=--
#### Stable Homotopy theory
+--{: .hide}
[[!include stable homotopy theory - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

An _orthogonal ring spectrum_ is a [[ring spectrum]] modeled as an [[orthogonal spectrum]]. Equivalently this is a [[monoid object]] with respect to the [[symmetric monoidal smash product of spectra]], for orthogonal spectra.
Morever, if we regard orthogonal spectra as $\mathbb{S}_{orth}$-[[modules]], as discussed at _[[model structure on orthogonal spectra]]_, then this, in turn, is equivalent to a $\mathbb{S}_{orth}$-algebra, where $\mathbb{S}_{orth}$ is the standard model of the [[sphere spectrum]] as an orthogonal spectrum.

There is a [[model structure for ring spectra|model structure for orthogonal ring spectra]] ([MMSS 00](#MandellMaySchwedeShipley01)) under which orthogonal ring spectra represent genuine [[A-infinity rings]], and commutative orthogonal ring spectra represent genuine [[E-infinity rings]]. This fact is one of the key motivation for passing from [[sequential spectra]] to the richer model of [[orthogonal spectra]].

Despite all this, the component expression of the structure in an orthgonal ring spectrum, in the fashion of _[[functors with smash product]]_, is rather straightforward, and directly analogous to the structure in a [[dg-algebra]]: essentially there is for all pairs of indices $n_1, n_2$ a pairing between the component spaces of the spectrum in these degrees

$$
  E_{n_1}\wedge E_{n_2}\longrightarrow E_{n_1 + n_2}
$$

such that this respects the given action of the [[orthogonal groups]] and of [[suspensions]], and such that it is is [[associativity|associative]] and [[unitality|unital]] in the evident way.

## Definition

The definition is directly analogous to that of _[[symmetric ring spectrum]]_, just with the [[symmetric groups]] replaced by [[orthogonal groups]] throughout.


## References

* {#MandellMaySchwedeShipley01} [[Michael Mandell]], [[Peter May]], [[Stefan Schwede]], [[Brooke Shipley]], _[[Model categories of diagram spectra]]_, Proceedings of the London Mathematical Society, 82 (2001), 441-512 ([pdf](http://www.math.uchicago.edu/~may/PAPERS/mmssLMSDec30.pdf))


[[!redirects orthogonal ring spectra]]
