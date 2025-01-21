


+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Geometry
+--{: .hide}
[[!include higher geometry - contents]]
=--
#### Algebra
+--{: .hide}
[[!include higher algebra - contents]]
=--
=--
=--


> This entry is about the formal dual [[topological space]] of a [[commutative ring]]. For the very different notion of a similar name in [[higher algebra]] see at [[ring spectrum]]. For more see at _[[spectrum - disambiguation]]_.

#Contents#
* table of contents
{:toc}

## Idea

Given a [[commutative ring]] $R$, its *Zariski spectrum* (or just _spectrum_) is the [[topological space]] $Spec(R)$ whose points are the [[prime ideals]] of $R$ and whose [[topology]] is the [[Zariski topology]] on these prime ideals. This topological case is also called the __[[prime spectrum]]__ of $R$, the latter terminology however applies to [[noncommutative rings]] as well.

However, usually by $Spec(R)$ one means more: the [[locally ringed space]] which is obtained by equipping the above topological space by a unique sheaf of commutative local rings $\mathcal{O}$ such that for every principal localization of commutative rings $R\to R[f^{-1}]$ we have $\mathcal{O}(Spec R[f^{-1}]) = R[f^{-1}]$ and the restrictions $\mathcal{O}(Spec R)\to\mathcal{O}(Spec R[f^{-1}])$ and $\mathcal{O}(Spec R[g^{-1}])\to\mathcal{O}(Spec R[f^{-1}])$ where $f$ divides $g$ are the corresponding localizations of rings. Global sections functor assigns to every ringed space the ring of global sections. Restrict this functor to the functor of global sections from the subcategory of commutative locally ringed spaces to the category of commutative rings. This functor has its right adjoint and this is precisely the Spec-functor.

If the prime spectrum is taken with a structure of a locally ringed space then one usually says the __affine spectrum__ (this terminology never used just for the underlying topological space or a set).

Every locally ringed space isomorphic to an affine spectrum is said to be an [[affine scheme]]. 


## Related concepts

* [[projective spectrum]]

* [[spectrum (geometry)]]

  * [[prime spectrum]]

  * [[formal spectrum]]

* [[modules over a ring are equivalent to quasicoherent sheaves over its spectrum]]

* [[prime spectrum of a monoidal stable (∞,1)-category]]

* [[affine scheme]]

* [[spectral topological space]]

## References

* Wikipedia, _[Spectrum of a ring](http://en.wikipedia.org/wiki/Spectrum_of_a_ring)_

[[!redirects affine spectrum]]
[[!redirects spectrum of a ring]]

[[!redirects spectra of commutative rings]]

[[!redirects spectra of rings]]

[[!redirects prime spectrum of a commutative ring]]
[[!redirects prime spectra of commutative rings]]

[[!redirects Zariski spectrum]]
[[!redirects Zariski spectra]]


