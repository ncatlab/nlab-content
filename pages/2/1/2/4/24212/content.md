
### Homotopy theory formalized in homotopy type theory
 {#HomotopyTheoryInHomotopyTyepTheoryReferences}

The following is a list of topics and results of [[homotopy theory]] that have been [[formal logic|formalized]] in [[homotopy type theory]].

\linebreak

On [[homotopy groups of spheres]]:

* [[homotopy groups of spheres in HoTT]]

On [[Whitehead's theorem]]:

* Dan's proof for [n-types](https://github.com/dlicata335/hott-agda/blob/master/homotopy/Whitehead.agda).

On  [[Eilenberg-MacLane spaces]]:

* Dan's [construction](https://github.com/dlicata335/hott-agda/blob/master/homotopy/KGn.agda).

* $K(G,n)$ is a spectrum, [formalized](https://github.com/HoTT/HoTT-Agda/blob/master/homotopy/EilenbergMacLane.agda)

On [[ordinary cohomology]]:

* [Deriving cohomology theories from spectra](https://github.com/HoTT/HoTT-Agda/blob/master/cohomology/SpectrumModel.agda)

* [Mayer-Vietoris sequence](https://github.com/HoTT/HoTT-Agda/blob/master/cohomology/MayerVietoris.agda), with [exposition](http://www.contrib.andrew.cmu.edu/~ecavallo/works/mayer-vietoris.pdf)

* [Cohomology of the n-torus](https://github.com/HoTT/HoTT-Agda/blob/master/cohomology/Torus.agda), which could be easily extended to any finite product of spheres.

* to do:

  * cohomology with finite coefficients, all we need is the boring work of defining $\mathbb{Z}/p\mathbb{Z}$ as an explicit group.

  * Calculate some more cohomology groups.

  * Compute the loop space of [this construction](https://github.com/HoTT/HoTT-Agda/blob/master/homotopy/SpaceFromGroups.agda) and use it to define spectra.


On the [[Freudenthal suspension theorem]]:

* Implies $\pi_k(S^n) = \pi_{k+1}(S^{n+1})$ whenever $k \leq 2n - 2$

* Peter's encode/decode-style proof, [formalized](https://github.com/dlicata335/hott-agda/blob/master/homotopy/Freudenthal.agda) by Dan, using a clever lemma about maps out of 2 n-connected types. This is the "95%" version, which shows that the relevant map is an equivalence on truncations.
* The full "100%" version, [formalized](https://github.com/dlicata335/hott-agda/blob/master/homotopy/FreudenthalConnected.agda) by Dan, which shows that the relevant map is $2n$-connected.

On [[homotopy limits]]:

* Jeremy Avigad, Chris Kapulkin and Peter Lumsdaine [arXiv](http://arxiv.org/abs/1304.0680) [Coq code](https://github.com/peterlefanulumsdaine/hott-limits/)

On the  [[van Kampen theorem]]:

* Mike's proofs are in the book and [Favonia formalized it](http://hott.github.com/HoTT-Agda/Homotopy.VanKampen.html). {{deadlink}}


On [[covering spaces]]:

* Favonia's proofs (link in flux due to library rewrite).

On [[Blakers-Massey theorem]]:

* Favonia/Peter/Guillaume/Dan's formalization of Peter/Eric/Dan's proof (link in flux due to library rewrite).
