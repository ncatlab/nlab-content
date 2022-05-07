#Contents#
* table of contents
{:toc}

## Idea

The _motivic Thom spectrum_ $MGL$ is the [[motivic spectrum]] in the [[stable motivic homotopy category]] representing [[algebraic cobordism]].  It is the algebraic or [[motives|motivic]] analogue of the [[Thom spectrum]] in the [[stable homotopy category]] which represents [[complex cobordism]].

## Definition

In analogy with the [[complex cobordism]] spectrum $MU$, [Voevodsky](#Voevodsky98) defined the algebraic cobordism spectrum $MGL_S$ in the [[stable motivic homotopy category]] by the formula

$$ MGL_S = colim_{n\to\infty} \Omega^n_{\mathbf{P}^1} Th(V_n), $$

where $S$ is the base scheme, $Th(V_n)$ is the (infinite suspension of) the [[Thom space]] of the tautological vector bundle $V_n$ over the infinite Grassmannian of $n$-planes $Gr(n)$. More precisely, $Gr(n)$ is defined as the colimit of the smooth $S$-schemes $Gr(n,k)$ as $k\to\infty$, and $V_n$ is similarly the colimit of the tautological vector bundles over $Gr(n,k)$.
The notation $\Omega^n_{\mathbf{P}^1}$ denotes the $n$th $\mathbf{P}^1$-loop space.

## Properties

Like the [[motivic Eilenberg-Mac Lane spectrum]] $H\mathbf{Z}$ and the [[algebraic K-theory]] spectrum $KGL$, $MGL$ is an $E_\infty$-motivic [[ring spectrum]].

The spectrum $MGL$ was used by Voevodsky in his proof of the [[Bloch-Kato conjecture]]. It is also the starting point of [[chromatic motivic homotopy theory]].

## Related concepts

* [[algebraic cobordism]]
* [[complex cobordism]]
* [[Thom spectrum]]
* [[motivic homotopy theory]]
* [[Snaith's theorem]]
* [[motivic Eilenberg-Mac Lane spectrum]]
* [[algebraic K-theory]]

## References

* {#Voevodsky98} [[Vladimir Voevodsky]], _$\mathbf{A}^1$-Homotopy Theory_, Doc. Math., Extra Vol. ICM 1998(I), 417-442, [web](http://www.mathematik.uni-bielefeld.de/documenta/xvol-icm/00/Voevodsky.MAN.html).

* [[Ivan Panin]], K. Pimenov, [[Oliver Röndigs]], _A universality theorem for Voevodsky's algebraic cobordism spectrum_, Homology, Homotopy and Applications, 2008, 10(2), 211-226, [arXiv](http://arxiv.org/abs/0709.4116).

* [[Ivan Panin]], K. Pimenov, [[Oliver Röndigs]], _On the relation of Voevodsky's algebraic cobordism to Quillen's K-theory_, Inventiones mathematicae, 2009, 175(2), 435-451, [DOI](http://citeseerx.ist.psu.edu/viewdoc/summary?doi=10.1.1.244.7301), [arXiv](http://arxiv.org/abs/0709.4124).

* [[Markus Spitzweck]], _Algebraic cobordism in mixed characteristic_, [arXiv](http://arxiv.org/abs/1404.2542).

* [[Marc Hoyois]], _From algebraic cobordism to motivic cohomology_, [pdf](http://math.mit.edu/~hoyois/papers/hopkinsmorel.pdf), [arXiv](http://arxiv.org/abs/1210.7182).

* {#GepnerSnaith08} [[David Gepner]], [[Victor Snaith]], _On the motivic spectra representing algebraic cobordism and algebraic K-theory_, Documenta Math.  2008 ([arXiv:0712.2817](http://arxiv.org/abs/0712.2817)).

A discussion on MathOverflow:

* _Interdependence between A^1-homotopy theory and algebraic cobordism_, [MO/36659](http://mathoverflow.net/questions/36659/interdependence-between-a1-homotopy-theory-and-algebraic-cobordism/36698#36698).

[[!redirects algebraic Thom spectrum]]
[[!redirects algebraic Thom complex]]
[[!redirects motivic cobordism spectrum]]
[[!redirects MGL]]