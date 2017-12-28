
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### AQFT and operator algebra
+-- {: .hide}
[[!include AQFT and operator algebra contents]]
=--
#### Physics
+-- {: .hide}
[[!include physicscontents]]
=--
=--
=--

# Contents
* table of contents
{: toc}

## Idea

The _Stone--von Neumann theorem_ (due to [[Marshall Stone]] and [[John von Neumann]]) says that there is -- up to [[isomorphism]] -- a unique [[irreducible representation|irreducible]] [[unitary representation]] of the [[Heisenberg group]] on finitely many generators (equivalently: of the [[Weyl relations]] of the [[canonical commutation relations]]).

The analogous statement does _not_ hold for infinitely many generators (as they appear in [[quantum field theory]]); this is _[[Haag's theorem]]_.

Explicitly, the [[canonical commutation relations]] on two generators ([[canonical coordinate]] $q$ and [[canonical momentum]] $p$) in the form 

$$
  [q,p] = i \hbar
$$

may be represented as [[unbounded operators]] on the [[Hilbert space]] of [[square integrable functions]] $L^2(\mathbb{R})$ on the [[real line]] by defining them on the [[dense subspace]] of [[smooth functions]] $\psi \colon \mathbb{R} \to \mathbb{C}$ as

$$
  (q \psi)(x) \coloneqq x \psi(x)
  \phantom{AAAA}
  (p \psi)(x) \coloneqq -i \hbar \frac{\partial}{\partial x} \psi(x)
  \,,
$$

where on the right we have the [[derivative]] along the canonical [[coordinate function]] on $\mathbb{R}$.

This is often called the _Schrödinger representation_ (after [[Erwin Schrödinger]], e.g. [Redei](#Redei)), to be distinguished from "[[Schrödinger picture]]" which is a related but different concept.

## Related concepts

* for the Schrödinger representation obtained via [[geometric quantization]] see [there](geometric+quantization#ExamplesSchroedingerRepresentation)

## References

The original articles are

* [[John von Neumann]], _Die Eindeutigkeit der Schr&#246;dingerschen Operatoren_ ,  Mathematische Annalen (Springer Berlin / Heidelberg) 104: 570&#8211;578, 

* [[John von Neumann]], _&#220;ber Einen Satz Von Herrn M. H. Stone_ (in German), Annals of Mathematics, Second Series 33 (3): 567&#8211;573, ISSN 0003-486X

* [[Marc Rieffel]], _On the uniqueness of the Heisenberg commutation relations_ ([pdf](http://www.univie.ac.at/nuhag-php/bibtex/open_files/ri72_rieffuhcr.pdf))

Review includes

* {#Redei} [[Miklós Rédei]], _Von Neumann's proof of Uniqueness of Schrödinger representation of Heisenberg's commutation relation_ ([[RedeiCCRRepUniqueness.pdf:file]])

See also 

* Wikipedia, _[Stone-von Neumann theorem](https://en.wikipedia.org/wiki/Stone%E2%80%93von_Neumann_theorem)_

[[!redirects Stone von Neumann theorem]]
[[!redirects Stone-von Neumann theorem]]
[[!redirects Stone–von Neumann theorem]]
[[!redirects Stone--von Neumann theorem]]

[[!redirects Schrödinger representation]]
[[!redirects Schrödinger representations]]

[[!redirects Schroedinger representation]]
[[!redirects Schroedinger representations]]

