
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Algebraic Quantum Field Theory
+--{: .hide}
[[!include AQFT and operator algebra contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

In [[mathematical physics|mathematical]]/[[theoretical physics]], _semi-topological_ or _semi-holomorphic D=4 Chern-Simons theory_ is a variant of ordinary [[D=3 Chern-Simons theory]] where, roughly, one of the three [[coordinate functions]] is promoted from an ordinary real-valued coordinate to a [[holomorphic function|holomorphic coordinate]]. 

Hence semi-topological/holomorphic D=4 Chern-Simons theory is a [[field theory]] defined on [[spacetimes]] of the form $\Sigma^2 \times C$ where $\Sigma^2$ is a real [[smooth manifold]], while $C$ is a [[complex curve]], and whose [[Lagrangian density]] is schematically the ordinary [[Chern-Simons form]], but with one of the wedge factors promoted from $d x^i$ to $d z$.

Accordingly, this [[field theory]] is a [[topological field theory]] (only) with respect to $\Sigma^2$, while it behaves like a [[conformal field theory]] with respect to $C$, whence "semi-topological/holomorphic" Chern-Simons theory: If one instead promotes all three coordinates of ordinary D=3 Chern-Simons theory to holomorphic coordinates, one obtains full 6d [[holomorphic Chern-Simons theory]].

But beware that in the literature this is often referred to just as _[[D=4 Chern-Simons theory]]_.

## Properties

### Wilson lines and relation to integrable lattice models

Due to this particular property of the theory, [[Wilson line]] [[observables]] that form a network on $\Sigma^2$ but with each line located at a distinct point in the [[complex curve]] $C$ play a special role: Arranging them along the lines of a rectangular grid makes these [[observables]] behave much like those of a [[lattice model]] with their intersection points as [[vertices]], but the topological invariance of the theory with respect to $\Sigma^2$ implies certain symmetry operations on these observables, coming from invariance of the theory under moving Wilson lines across each other. These symmetries turn out to behave like [[R-matrices]] making the corresponding lattice model an [[integrable system]].

### Yangian symmetry

... [[Yangian]] ...

Consider the example when the spacetime is of the form $\mathbb{C}_w \times \mathbb{C}_z$ with subscripts to denote the respective coordinates. Pushing forward the factorization algebra for gives a locally constant factorization algebra on $\mathbb{C}_w$.

Applying Koszul duality gives a Hopf algebra because it is augmented as an $E_1$ algebra. This is a result of Tamarkin. In this case the Hopf algebra is the linear dual of the completed Yangian. This is seen by evaluating the classical limit and the first order bialgebra structure and then invoking a uniqueness result of Drinfeld.

## References

The idea of semi-topological 4d CS theory, and its relation to [[Yangians]] and [[integrable system|integrable]] [[lattice models]], is due to

* {#Costello13} [[Kevin Costello]], _Supersymmetric gauge theory and the Yangian_ ([arXiv:1303.2632](https://arxiv.org/abs/1303.2632))

* {#Witten16} [[Edward Witten]], _Integrable Lattice Models From Gauge Theory_, Adv.Theor.Math.Phys. 21 (2017) 1819-1843 ([arXiv:1611.00592](https://arxiv.org/abs/1611.00592))

* {#CostelloWittenYamazaki17} [[Kevin Costello]], [[Edward Witten]], [[Masahito Yamazaki]], _Gauge Theory and Integrability, I_, ICCM Not. 6, 46-119 (2018) ([arXiv:1709.09993](https://arxiv.org/abs/1709.09993))

* {#CostelloWittenYamazaki17} [[Kevin Costello]], [[Edward Witten]], [[Masahito Yamazaki]], _Gauge Theory and Integrability, II_, ICCM Not. 6, 120-146 (2018) ([arXiv:1802.01579](https://arxiv.org/abs/1802.01579))


* [[Kevin Costello]], [[Masahito Yamazaki]],  _Gauge Theory And Integrability, III_ ([arxiv:1908.02289](https://arxiv.org/abs/1908.02289))

* [[Meer Ashwinkumar]], _Integrable Lattice Models and Holography_, JHEP 02 (2021) 227 ([arXiv:2003.08931](https://arxiv.org/abs/2003.08931))

* [[Meer Ashwinkumar]], Jun-ichi Sakamoto, [[Masahito Yamazaki]], *Dualities and Discretizations of Integrable Quantum Field Theories from 4d Chern-Simons Theory* &lbrack;[arXiv:2309.14412](https://arxiv.org/abs/2309.14412)&rbrack;


Rigorous discussion using [[homotopy theory]] (see at [[homotopical AQFT]]):

* [[Marco Benini]], [[Alexander Schenkel]], Benoit Vicedo, _Homotopical analysis of 4d Chern-Simons theory and integrable field theories_ &lbrack;[arXiv:2008.01829](https://arxiv.org/abs/2008.01829)&rbrack;

and via [[L-infinity algebras|$L_\infty$-algebras]]:

* [[Marco Benini]], [[Alexander Schenkel]], Benoit Vicedo: *The homological algebra of 2d integrable field theories* &lbrack;[arXiv:2601.19993](https://arxiv.org/abs/2601.19993)&rbrack;

Review:

* Sylvain Lacroix, *4-dimensional Chern-Simons theory and integrable field theories* &lbrack;[arXiv:2109.14278](https://arxiv.org/abs/2109.14278)&rbrack;

* [[Masahito Yamazaki]]: *Gauge Theory and Integrability: An Overview*, Proceedings of the International Conference of Basic Science 2025 &lbrack;[arXiv:2509.07628](https://arxiv.org/abs/2509.07628)&rbrack;



Discussion of realizations of semi-holomorphic 4d Chern-Simons theory as the [[worldvolume]] theory of [[intersecting brane|intersecting]] [[D-brane]]/[[NS5-brane]] models:

* [[Meer Ashwinkumar]], [[Meng-Chwan Tan]], Qin Zhao, _Branes and Categorifying Integrable Lattice Models_ ([arXiv:1806.02821](https://arxiv.org/abs/1806.02821))

and further relating to the [[quantum geometric Langlands correspondence]]:

* [[Meer Ashwinkumar]], [[Meng-Chwan Tan]], _Unifying Lattice Models, Links and Quantum Geometric Langlands via Branes in String Theory_ ([arXiv:1910.01134](https://arxiv.org/abs/1910.01134))

Relation to the [[Berkovits superstring]]:

* [[Nathan Berkovits]], Rodrigo S. Pitombo, *4D Chern-Simons and the pure spinor $AdS_5 \times S^5$ superstring* &lbrack;[arXiv:2401.03976](https://arxiv.org/abs/2401.03976)&rbrack;

A [[higher gauge theory|higher gauge]] [[D=5 Chern-Simons theory]] analogous to semi-topological D=4 Chern-Simons theory:

* [[Alexander Schenkel]], Benoit Vicedo: *5d 2-Chern-Simons theory and 3d integrable field theories* &lbrack;[arXiv:2405.08083](https://arxiv.org/abs/2405.08083)&rbrack;

Relation of 4d semi-topological CS to special solutions of 4d [[gravity]]:

* Lewis T. Cole, Peter Weck: *Integrability in Gravity from Chern-Simons Theory* &lbrack;[arXiv:2407.08782](https://arxiv.org/abs/2407.08782)&rbrack;

Relation to [[higher dimensional WZW model|4d WZW theory]]:

* Masashi Hamanaka, Shan-Chi Huang: *Solitons in 4d Wess-Zumino-Witten models -- Towards unification of integrable systems* &lbrack;[arXiv:2408.16554](https://arxiv.org/abs/2408.16554)&rbrack;

See also 

* Wikipedia, _[Four-dimensional Chern–Simons theory](https://en.wikipedia.org/wiki/Four-dimensional_Chern%E2%80%93Simons_theory)_

[[!redirects semi-topological 4d Chern-Simons theory]]
[[!redirects semi-holomorphic D=4 Chern-Simons theory]]
[[!redirects semi-holomorphic 4d Chern-Simons theory]]



