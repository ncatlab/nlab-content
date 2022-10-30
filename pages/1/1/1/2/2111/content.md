The most classical coherent states of E. Schr&#246;dinger (1926, coherent refers to the meaning in optics) are the elements in $L^2(\mathbb{R}^n)$ which are eigenfunctions $|z\rangle = |z_1,\ldots,z_n\rangle$ of the annihilation operators $a_i$, $i=1,ldots,n$; the eigenvalues $z_i$ are complex numbers and all complex numbers appear in that way; more precisely the coherent states are parametrized by numbers $z=(z_1,\ldots,z_n)$ in $\mathbb{C}^n$, and there is a measure $d\mu$ on $\mathbb{C}^n$ providing the resolution of unity formula
$$
\int_{\mathbb{C}^n} |z\rangle \langle z| d\mu = 1
$$
Coherent states however are not mutually orthogonal; they form an overcomplete family of states: not only that every vector in $L^2$ can be expressed in terms of them but rather in more than one way and we can throw certain coherent states out and not to spoil the property (how many and which is a more subtle question). Thus expressing states in terms of coherent states is sort of Fourier analysis; in fact this approach is taken in a variant called wavelet analysis. Coherent states are minimizing the uncertainty relations, closest to classical states in their behaviour; their probability density is Gaussian and formally satisfies the classical Newton equations. 

In general, projection operators $|z\rangle \langle z|$ and the scalar measure $d\mu$ do not separate, in fact instead of $|z\rangle \langle z| d\mu$ one considers more general [[projective measure]] (descriptively a "measure" with values in projective operators on a Hilbert space) on a more general geometric space $X$ replacing $\mathbb{C}^n$ which is normalized to 1 on the whole space. Symbollically we can still pretend that the projective measure is of the form $\mu(A) = \int_A |z\rangle \langle z| d\mu$ where $d\mu$ is an ordinary (scalar-valued) measure. 

The basic example of the space $X$ is the homogeneous space $G^{\mathbb {C}}/B = G/K$ where $G$ is a compact Lie group, $G^{\mathbb{C}}$ its complexification, $K\subset G$ maximal compact subgroup and $B\subset G^{\mathbb{C}}$ the Borel subgroup. Manifold $G/K$ is naturally a compact complex manifold, in fact Kaehler. Fix a unitary character $\chi:G\to S^1$ which uniquely extends to a character $\chi:G^{\mathbb{C}}\to \mathbb{C}^*$ of the complexification; let $\mathbf{C}_\chi$ be the corresponding 1-dimensional representation. Then let $L_\chi = G^{\mathbb{C}}\times_{G^{\mathbb{C}}} \mathbb{C}_\chi$ be the associated line bundle. It is equipped with a natural holomorphic structure and hermitean scalar product; the space of holomorphic (or antiholomorphic depending on conventions in the construction) sections of that bundle is finite-dimensional and irreducible by Borel-Weil theorem. __Perelomov coherent states__ on that bundle are the elements of the orbit of $G$ of the heighest (equivalently lowest) weight vector (or equivalently of $G^{\mathbb{C}}$: the real and complex orbits are equal, and the generalized uncertainty relations correspond to the expression for a quantity proportional to negative of the square of the moment map, which is naturally extremal on symplectic orbits), but they can be also realized as the duals (according to Riesz theorem, that is dual vectors in a Hilbert space) to the evaluation functionals on the space of sections: take a point $q$ in the space of a line bundle and then divide it by the value of the section on the projection of $q$ to the homogeneous space. Up to a phase coherent states do not depend on the pointgs in the line, hence this yields a holomorphic embedding of $G^{\mathbb{C}}/B$ to the projectivization of the representation space, so called __coherent states embedding__. The rays are coherent states and the choices with scalar multiple accounted for are the coherent vectors. These coherent vectors are normalized by the measure which is the push down of the measure form $G$ to $G/K$. The classical coherent states appear in noncompact case, and the group in question is the Heisenberg group.

* A. M. Perelomov, [Coherent states for arbitrary Lie groups](http://projecteuclid.org/euclid.cmp/1103858078),
Comm. Math. Phys., 26 (1972), pp. 222--236; archived as [arXiv:math-ph/0203002](http://arxiv.org/abs/math/0203002).

* A. Perelomov, _Generalized coherent states and their applications_, Springer 1986

* J. H. Rawnsley, _Coherent states and Kaehler manifolds_,
Quart. J. Math. Oxford (2), 28 (1977), pp. 403--415

* V. Bargmann, _On a Hilbert space of analytic functions and an associated integral transform_, Communications on Pure and Applied Mathematics, 14 (1961), 187-214. MR 0157250 (28:486) 

* F. A. Berezin, _Quantization_, Math. USSR Izv., 8 (1974), 1109-1163. MR 0395610 (52:16404) 

* M. Spera, _On a generalized uncertainty principle,
coherent states and the moment map_, J. of Geometry and Physics 12 (1993) 165-182.

* for physical aspects [wikipedia:Coherent_state](http://en.wikipedia.org/wiki/Coherent_state).
[[!redirects coherent state]]