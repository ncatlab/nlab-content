
#Contents#
* table of contents
{:toc}

## Idea

_Algebraic cobordism_ is the algebraic or [[motives|motivic]] analogue of [[complex cobordism]].  It was constructed by [[Vladimir Voevodsky]] as the [[generalized cohomology theory]] represented by a certain [[motivic spectrum]] $MGL$, called the _motivic Thom spectrum_.

Over fields of characteristic zero, a geometric description of the $(2n,n)$-graded part of algebraic cobordism, via [[cobordism]] classes, was given by [[Marc Levine]] and [[Fabien Morel]].

## Definition

### The motivic spectrum

In analogy with the [[complex cobordism]] spectrum $MU$, Voevodsky defined the algebraic cobordism spectrum $MGL_S$ in the [[stable motivic homotopy category]] by

$$ MGL_S = colim_{n\to\infty} \Sigma_T^{\infty-n} V_n/V_n^\times, $$

where $S$ is the base scheme, $T = \mathbf{A}^1/\mathbf{G}_m$ is the [[Tate sphere]], and $V_n$ is the tautological vector bundle over the infinite Grassmannian of $n$-planes $Gr(n)$. More precisely, $Gr(n)$ is defined as the colimit of the smooth $S$-schemes $Gr(n,k)$ as $k\to\infty$, and $V_n$ is similarly the colimit of the tautological vector bundles over $Gr(n,k)$.
See [Voevodsky 98](#Voevodsky98).

Like the [[motivic Eilenberg-Mac Lane spectrum]] $H\mathbf{Z}$ and the [[algebraic K-theory]] spectrum $KGL$, $MGL$ is an $E_\infty$-motivic [[ring spectrum]].

The spectrum $MGL$ was used by Voevodsky in his proof of the [[Bloch-Kato conjecture]]. It is also the starting point of [[chromatic motivic homotopy theory]].

### The oriented cohomology theory

Over a field $k$ of characteristic zero, a geometric description of the $(2n,n)$-graded part of the [[generalized cohomology theory]] represented by $MGL_k$ was given by [[Marc Levine]] and [[Fabien Morel]].  More precisely, [Levine-Morel](#LevineMorel) constructed the universal _oriented cohomology theory_ $\Omega^* : \Sm_k \to CRing^*$.  Here _oriented_ means the existence of [[direct image]] or [[Gysin homomorphisms]] for [[proper morphisms of schemes]].  This implies the existence of[[Chern classes]] for [[vector bundles]].

+-- {: .num_theorem}
###### Theorem ([Levine-Morel](#LevineMorel))
There is a canonical isomorphism of graded rings
  $$ \mathbf{L}^* \stackrel{\sim}{\longrightarrow} \Omega^*(\Spec(k)) $$
where $\mathbf{L}^*$ denotes the [[Lazard ring]] with an appropriate grading.
=--

+-- {: .num_theorem}
###### Theorem ([Levine-Morel](#LevineMorel))
Let $i : Z \hookrightarrow X$ be a [[closed immersion]] of smooth $k$-schemes and $j : U \hookrightarrow X$ the complementary [[open immersion]].  There is a canonical exact sequence of graded abelian groups
  $$ \Omega^{*-d}(Z) \stackrel{i_*}{\to} \Omega^*(X) \stackrel{j^*}{\to} \Omega^*(U) \to 0, $$
where $d = \codim(Z, X)$.
=--

+-- {: .num_theorem}
###### Theorem ([Levine-Morel](#LevineMorel))
Given an embedding $k \hookrightarrow \mathbf{C}$, the canonical homomorphism of graded rings
  $$ \Omega^*(k) \longrightarrow MU^{2*}(pt) $$
is invertible.
=--

+-- {: .num_theorem}
###### Theorem ([Levine 2008](#Levine2008))
The canonical homomorphisms of graded rings
  $$ \Omega^*(X) \longrightarrow MGL^{2*,*}(X) $$
are invertible for all $X \in \Sm_k$.
=--

## Related concepts

* [[Snaith's theorem]]
* [[motivic homotopy theory]]
* [[complex cobordism]]
* [[motivic cohomology]]
* [[algebraic K-theory]]

## References

### The motivic spectrum

* {#Voevodsky98} [[Vladimir Voevodsky]], _$\mathbf{A}^1$-Homotopy Theory_, Doc. Math., Extra Vol. ICM 1998(I), 417-442, [web](http://www.mathematik.uni-bielefeld.de/documenta/xvol-icm/00/Voevodsky.MAN.html).

* [[Ivan Panin]], K. Pimenov, [[Oliver Röndigs]], _A universality theorem for Voevodsky's algebraic cobordism spectrum_, Homology, Homotopy and Applications, 2008, 10(2), 211-226, [arXiv](http://arxiv.org/abs/0709.4116).

* [[Ivan Panin]], K. Pimenov, [[Oliver Röndigs]], _On the relation of Voevodsky's algebraic cobordism to Quillen's K-theory_, Inventiones mathematicae, 2009, 175(2), 435-451, [DOI](http://citeseerx.ist.psu.edu/viewdoc/summary?doi=10.1.1.244.7301), [arXiv](http://arxiv.org/abs/0709.4124).

* [[Markus Spitzweck]], _Algebraic cobordism in mixed characteristic_, [arXiv](http://arxiv.org/abs/1404.2542).

* [[Marc Hoyois]], _From algebraic cobordism to motivic cohomology_, [pdf](http://math.mit.edu/~hoyois/papers/hopkinsmorel.pdf), [arXiv](http://arxiv.org/abs/1210.7182).

* {#GepnerSnaith08} [[David Gepner]], [[Victor Snaith]], _On the motivic spectra representing algebraic cobordism and algebraic K-theory_, Documenta Math.  2008 ([arXiv:0712.2817](http://arxiv.org/abs/0712.2817)).

A discussion on MathOverflow:

* _Interdependence between A^1-homotopy theory and algebraic cobordism_, [MO/36659](http://mathoverflow.net/questions/36659/interdependence-between-a1-homotopy-theory-and-algebraic-cobordism/36698#36698).


### The oriented cohomology theory


* [[Marc Levine]], [[Fabien Morel]], _Cobordisme alg&#233;brique I_, Note aux C.R. Acad. Sci. Paris, 332 S&#233;rie I, p. 723--728, 2001 ([doi](http://dx.doi.org/10.1016/S0764-4442(01)01833-X)); _Cobordisme alg&#233;brique II_, Note aux C.R. Acad. Sci. Paris, 332 S&#233;rie I, p. 815--820, 2001 ([doi](http://dx.doi.org/10.1016/S0764-4442(01)01832-8)).

* {#LevineMorel} [[Marc Levine]], [[Fabien Morel]], _Algebraic cobordism_, Springer 2007, [pdf](https://www.uni-due.de/~bm0032/publ/AlgCobordBook4.pdf).

* [[Marc Levine]], _A survey of algebraic cobordism_, [pdf](http://www.uni-due.de/~bm0032/publ/SurveyAlgCobord.pdf&#8206;)

* [[Marc Levine]], _Algebraic cobordism_, Proceedings of the ICM, Beijing 2002, vol. 2, 57--66, [math.KT/0304206](http://arxiv.org/abs/math/0304206)

* [[Marc Levine]], _Three lectures on algebraic cobordism_, University of Western Ontario Mathematics Department, 2005, [Lecture I](http://www.uni-due.de/~bm0032/publ/CobordismLec1LS.pdf), [Lecture II](http://www.uni-due.de/~bm0032/publ/CobordismLec2LS.pdf), [Lecture III](http://www.uni-due.de/~bm0032/publ/CobordismLec4LS.pdf).

* M. Levine, F. Morel, [[Oberwolfach]] Arbeitsgemeinschaft mit aktuellem Thema, April 2005 [report](http://www.ems-ph.org/journals/show_abstract.php?issn=1660-8933&vol=2&iss=2&rank=2), [notes](http://www.ems-ph.org/journals/show_pdf.php?issn=1660-8933&vol=2&iss=2&rank=2)

A simpler construction was given in

* M. Levine, R. Pandharipande, _Algebraic cobordism revisited_, [math.AG/0605196](http://arxiv.org/abs/math/0605196)

A [[Borel-Moore homology]] version of $MGL^{*,*}$ is considered in

* [[Marc Levine]], _Oriented cohomology, Borel-Moore homology and algebraic cobordism_, [arXiv](http://arxiv.org/abs/0807.2257).

The comparison with $MGL^{2*,*}$ is in

* {#Levine2008} [[Marc Levine]], _Comparison of cobordism theories_, Journal of Algebra, 322(9), 3291-3317, 2009, [arXiv](http://arxiv.org/abs/0807.2238).

The construction was extended to [[derived algebraic geometry|derived schemes]] in the paper

* [[Parker Lowrey]], [[Timo Schuerg]].  _Derived algebraic bordism_, 2012, [arXiv:1211.7023](http://arxiv.org/abs/1211.7023).

The close connection of algebraic cobordism with [[K-theory]] is discussed in

* Jos&#233; Luis Gonz&#225;lez, Kalle Karu.  _Universality of K-theory_.  2013.  [arXiv:1301.3815](http://arxiv.org/abs/1301.3815).

An algebraic analogue of h-cobordism:

* Aravind Asok, Fabien Morel, _Smooth varieties up to $\mathbb{A}^1$-homotopy and algebraic h-cobordisms_, [arXiv:0810.0324](http://arxiv.org/abs/0810.0324)

[[!redirects algebraic cobordism spectrum]]
[[!redirects motivic Thom spectrum]]
[[!redirects algebraic Thom complex]]
[[!redirects MGL]]