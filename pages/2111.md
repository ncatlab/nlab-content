
#Contents#
* table of contents
{:toc}

## Idea

_Coherent states_ are members of special overcomplete families of elements (usually in the projectivization) of [[Hilbert space]] of states of certain systems in [[quantum mechanics]]. This entry is mainly about Perelomov style CS, see a separate page for [[Hall coherent state]]s. Coherence in the sense of quantum optics, and in the sense of statistical density matrix is one of the features of these very specifical objects in mathematical physics (thus coherent quantum states would be states of high degree of features of coherence in those senses, rather than refering to the specific families in mathematical physics). 

## Examples

### Of the harmonic oscillator

The most classical coherent states of E. Schr&#246;dinger (1926, _coherent_ refers to its meaning in optics) are the elements in $L^2(\mathbb{R}^n)$ which are the eigenfunctions $|z\rangle = |z_1,\ldots,z_n\rangle$ of the annihilation operators $a_i$, $i=1,\ldots,n$; the eigenvalues $z_i$ are complex numbers and all complex numbers appear in that way; more precisely the coherent states are parametrized by numbers $z=(z_1,\ldots,z_n)$ in $\mathbb{C}^n$, and there is a measure $d\mu$ on $\mathbb{C}^n$ providing the resolution of unity formula
$$
\int_{\mathbb{C}^n} |z\rangle \langle z| d\mu = 1
$$

Coherent states however are not mutually orthogonal; they form an overcomplete family of states: not only that every vector in $L^2$ can be expressed in terms of them but rather in more than one way and we can throw certain coherent states out and not to spoil the property (how many and which is a more subtle question). Thus expressing states in terms of coherent states is sort of Fourier analysis; in fact this approach is taken in a variant called wavelet analysis. Coherent states are minimizing the uncertainty relations, closest to classical states in their behaviour; their probability density is Gaussian. Vectors in the Hilbert space can be represented in the coherent state representation: $|f\rangle = \int |z\rangle\langle z|f\rangle d\mu$; if $f$ is in $L^2$ then $\langle z|f\rangle$ is a holomorphic function and this passage is called the Bargmann-Segal transform (referring to [Irving Segal](http://en.wikipedia.org/wiki/Irving_Segal)); this way certain Hilbert space of holomorphic function appears, the Bargmann-Fock space. The evolution of $\langle z|f\rangle$ formally satisfies the classical Newton equations of motion. 

In general, projection operators $|z\rangle \langle z|$ and the scalar measure $d\mu$ do not separate, in fact instead of $|z\rangle \langle z| d\mu$ one considers more general [[projection measure]] (descriptively a "measure" with values in self-adjoint projection operators on a separable Hilbert space) on a more general geometric space $X$ replacing $\mathbb{C}^n$ which is normalized to 1 on the whole space. Symbollically we can still pretend that the projective measure is of the form $\mu(A) = \int_A |z\rangle \langle z| d\mu$ where $d\mu$ is an ordinary (scalar-valued) measure. 

### Over a flag manifold

The basic example of the space $X$ is the homogeneous space $G^{\mathbb {C}}/B = G/K$ where $G$ is a compact Lie group, $G^{\mathbb{C}}$ its complexification, $K\subset G$ maximal compact subgroup and $B\subset G^{\mathbb{C}}$ the Borel subgroup. Generalized [[flag manifold]] $G/K$ is naturally a compact complex manifold, in fact K&#228;hler. Fix a unitary character $\chi:G\to S^1$ which uniquely extends to a character $\chi:G^{\mathbb{C}}\to \mathbb{C}^*$ of the complexification; let $\mathbf{C}_\chi$ be the corresponding 1-dimensional representation. Then let $L_\chi = G^{\mathbb{C}}\times_{G^{\mathbb{C}}} \mathbb{C}_\chi$ be the associated line bundle. It is equipped with a natural holomorphic structure and hermitean scalar product; the space of holomorphic (or antiholomorphic depending on conventions in the construction) sections of that bundle is finite-dimensional and irreducible by [[Borel-Weil theorem]]. __Perelomov coherent states__ on that bundle are the elements of the orbit of $G$ of the heighest (equivalently lowest) weight vector (or equivalently of $G^{\mathbb{C}}$: the real and complex orbits are equal). The covariant generalized uncertainty relations (ref. by Onofri, below) correspond to the expression for a quantity proportional to negative of the square of the moment map (see ref. by Spera, below), which is naturally extremal on symplectic orbits. These coherent states can also be realized as the duals (according to Riesz theorem, that is dual vectors in a Hilbert space) to the evaluation functionals on the space of sections: take a point $q$ in the space of a line bundle and then divide it by the value of the section on the projection of $q$ to the homogeneous space. Up to a scalar, coherent states do not depend on the choice of the point on the line, hence this yields a holomorphic embedding of $G^{\mathbb{C}}/B$ to the projectivization of the representation space, so called __coherent states embedding__. The rays are the coherent states and the choices with scalar multiple accounted for are the coherent vectors. These coherent vectors are normalized by the measure which is the push down of the measure form $G$ to $G/K$. The classical coherent states appear in noncompact case where the group in question is the Heisenberg group, and the covariant uncertainty relations are the usual ones. 

## Related concepts

* [[quasi-free quantum state]]

* [[coherent state (in geometric quantization)]], 

* [[Hall coherent state]]

* [[Berezin quantization]]

* [[wavelet]], [[curvelet]]

## References


* A. M. Perelomov, [Coherent states for arbitrary Lie groups](http://projecteuclid.org/euclid.cmp/1103858078),
Comm. Math. Phys., 26 (1972), pp. 222--236; archived as [arXiv:math-ph/0203002](http://arxiv.org/abs/math-ph/0203002).

* A. Perelomov, _Generalized coherent states and their applications_, Springer 1986

* J. H. Rawnsley, _Coherent states and K&#228;hler manifolds_,
Quart. J. Math. Oxford (2), 28 (1977), pp. 403--415

* V. Bargmann, _On a Hilbert space of analytic functions and an associated integral transform_, Communications on Pure and Applied Mathematics __14__ (1961) 187-214 [MR0157250](http://www.ams.org/mathscinet-getitem?mr=157250) [doi](ttp://dx.doi.org/10.1002/cpa.3160140303)

* F. A. Berezin, _Quantization_, Math. USSR Izv., 8 (1974), 1109-1163. MR 0395610 (52:16404) 

* M. Spera, _On a generalized uncertainty principle,
coherent states and the moment map_, J. of Geometry and Physics 12 (1993) 165-182.

* Enrico Onofri, _A note on coherent state representations of Lie groups_, J. Math. Phys. __16__:5, 1087-1089, may 1975. 

* for physical aspects [wikipedia:Coherent_state](http://en.wikipedia.org/wiki/Coherent_state).

* V. V. Kisil, _Integral representations and coherent states_,
Bulletin of the Belgian Mathematical Society, v. 2 (1995), No 5, pp. 529-540.

* Thomas Appl,  Diethard H Schiller, _Generalized hypergeometric coherent states_, J. Phys A37:7 (2004) 2731 [doi](https://doi.org/10.1088/0305-4470/37/7/015)

Coherent states can be generalized to [[noncommutative geometry]], most notably for [[quantum groups]]:

* H. Sazdjian, Y.S. Stanev, I.T. Todorov, _SU(3)-coherent state
operators and invariant correlation functions and their quantum group
counterparts_, J. Math. Phys. __36__ (1995), pp. 2030--2052.

* [[Branislav Jurčo|B. Jurčo]], P. &#352;tovi&#269;ek, [Coherent states for quantum compact groups](http://projecteuclid.org/euclid.cmp/1104288026), Comm. Math. Phys. __182__ (1996), pp. 221--251; [hep-th/9403114](http://arXiv.org/abs/hep-th/9403114)

* [[Zoran Škoda|Z. Škoda]], [Coherent states for Hopf algebras](http://dx.doi.org/10.1007/s11005-007-0166-y), Letters in Mathematical Physics __81__, N.1, pp. 1-17, July 2007; distinct earlier version, arXiv: [math.QA/0303357](http://arXiv.org/abs/math/0303357)

* N. Aizawa, R. Chakrabarti, _Coherent state on $SU_q(2)$ homogeneous space_, J. Phys. A __42__:29 [arXiv:0905.0194](http://arxiv.org/abs/0905.0194).

[[!redirects coherent states]]

[[!redirects coherent quantum state]]
[[!redirects coherent quantum states]]



