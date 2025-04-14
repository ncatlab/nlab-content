
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

The _Stone--von Neumann theorem_ --- due to [Stone 1930](#Stone1930), [von Neumann 1931](vonNeumann1931)/[32](vonNeumann1932) and [Mackey 1949](#Mackey1949) ---  says that there is -- up to [[isomorphism]] -- a unique [[irreducible representation|irreducible]] [[unitary representation]] of the [[Heisenberg group]] on finitely many generators (equivalently: of the [[Weyl algebra]], [[Weyl relations]], [[canonical commutation relations]]).

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

This is often called the _Schrödinger representation_, after [[Erwin Schrödinger]], cf. eg. [Redei](#Redei) (to be distinguished from "[[Schrödinger picture]]" which is a related but different concept).


## Related concepts

* [[Weyl relation]], [[Weyl algebra]]

* [[canonical commutation relation]]

* For the Schrödinger representation obtained via [[geometric quantization]] see [there](geometric+quantization#ExamplesSchroedingerRepresentation).



## References

The original articles:

* {#Stone1930} [[Marshall H. Stone]]: *Linear transformations in Hilbert space. III. Operational methods and group theory*, Proceedings of the National Academy of Sciences of the United States of America, **16** (1930) 172–175 &lbrack;[jstor:85485](https://www.jstor.org/stable/85485), [doi:10.1073/pnas.16.2.172](https://doi.org/10.1073/pnas.16.2.172)&rbrack;

* {#vonNeumann1931} [[John von Neumann]], *Die Eindeutigkeit der Schrödingerschen Operatoren*, Mathematische Annalen **104**  (1931) 570–578 &lbrack;[doi:10.1007/BF01457956](https://doi.org/10.1007/BF01457956)&rbrack;
 
* {#vonNeumannNeu1932} [[John von Neumann]], _Über Einen Satz Von Herrn M. H. Stone_, Annals of Mathematics, Second Series **33** 3 (1932) 567-573 &lbrack;[doi:10.2307/1968535](https://doi.org/10.2307/1968535), [jstor:1968535](https://www.jstor.org/stable/1968535)&rbrack;

* {#Mackey1949} [[George W. Mackey]]: *A theorem of Stone and von Neumann*, Duke Mathematical Journal, **16** (1949) 313–326 &lbrack;[doi:10.1215/S0012-7094-49-01631-2](https://projecteuclid.org/journals/duke-mathematical-journal/volume-16/issue-2/A-theorem-of-Stone-and-von-Neumann/10.1215/S0012-7094-49-01631-2.short)&rbrack;

Review:

* [[Amritanshu Prasad]]: *An easy proof of the Stone-von Neumann-Mackey theorem*, Expositiones Mathematicae **29** (2011) 110-118 &lbrack;[arXiv:0912.0574](https://arxiv.org/abs/0912.0574), [doi:10.1016/j.exmath.2010.06.001](https://doi.org/10.1016/j.exmath.2010.06.001)&rbrack;

* {#Redei} [[Miklós Rédei]]: _Von Neumann's proof of Uniqueness of Schrödinger representation of Heisenberg's commutation relation_ &lbrack;[[RedeiCCRRepUniqueness.pdf:file]]&rbrack;


Further discussion:

* [[Marc Rieffel]], _On the uniqueness of the Heisenberg commutation relations_, Duke Math. J. **39**  4 (1972) 745-752 &lbrack;[doi:10.1215/S0012-7094-72-03982-8](https://projecteuclid.org/journals/duke-mathematical-journal/volume-39/issue-4/On-the-uniqueness-of-the-Heisenberg-commutation-relations/10.1215/S0012-7094-72-03982-8.short)&rbrack;


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

