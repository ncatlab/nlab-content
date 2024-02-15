
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Gravity
+--{: .hide}
[[!include gravity contents]]
=--
#### Physics
+--{: .hide}
[[!include physicscontents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

A [[field (physics)|field]] configuration of the [[physical theory]] of _gravity_ on a [[spacetime]] $X$ is equivalently

* a [[vielbein]] field, hence a [[reduction of the structure group]] of the [[tangent bundle]] along $\mathbf{B} O(n-1,1) \to \mathbf{B}GL(n)$, defining a [[pseudo-Riemannian metric]];

* a [[connection on a bundle|connection]] that is locally a [[Lie algebra-valued 1-form]] with values in the [[Poincare Lie algebra]].

  $$
    (E, \Omega) : T X \to \mathfrak{iso}(d-1,1)
  $$

  such that this is a [[Cartan connection]].

(This parameterization of the gravitational field is called the [[first-order formulation of gravity]].) The component $E$ of the connection is the [[vielbein]] that encodes a [[pseudo-Riemannian metric]] $g = E \cdot E$ on $X$ and makes $X$ a [[pseudo-Riemannian manifold]]. Its quanta are the [[graviton]]s.

The [[non-propagating field]] $\Omega$ is the [[spin connection]].

The [[action functional]] on the space of such connection which defines the [[classical field theory]] of gravity is the [[Einstein-Hilbert action]].

More generally, [[supergravity]] is a [[gauge theory]] over a [[supermanifold]] $X$ for the [[super Euclidean group|super Poincare group]]. The field of supergravity is a Lie-algebra valued form with values in the [[super Poincare Lie algebra]].

$$
  (E,\Omega, \Psi) : T X \to \mathfrak{siso}(d-1,1)
$$

The additional [[fermion]]ic field $\Psi$ is the [[gravitino]] field.

So the [[configuration space]] of gravity on some $X$ is essentially the [[moduli space of Riemannian metrics]] on $X$.

## Details

> for the moment see *[[D'Auria-Fre formulation of supergravity]]* for further details

## Related concepts

* [[Einstein-Hilbert action]], [[Einstein equation]]

* [[rubber-sheet analogy of gravity]]

* [[general covariance]]

* [[Penrose-Hawking theorem]], [[cosmic censorship hypothesis]]

* [[weak gravity conjecture]]

* [[first order formulation of gravity]]

  * [[Plebanski formulation of gravity]], [[gravity as a BF-theory]], [[teleparallel gravity]]

  * [[Chern-Simons gravity]]

* [[Einstein-Maxwell theory]], [[Einstein-Yang-Mills theory]]

* [[higher order curvature corrections]]

* [[supergravity]]


* [[D=2 gravity]]

  * [[Liouville theory]]

  * [[Jackiw-Teitelboim gravity]]

* [[D=5 gravity]]

* [[spacetime]]

  * [[black hole]]

  * [[gravitational wave]]

* gravitational entropy

  * [[Bekenstein-Hawking entropy]]

  * [[generalized second law of thermodynamics]]

* [[energy condition]]

* [[positive energy theorem]]

* [[asymptotic safety]]

* [[cosmology]]

  * [[standard model of cosmology]]

* [[MOND]]

* [[computer experiment]]: [[gevolution]]



## References

### General

Historical texts:

* {#Infeld1962} [[Leopold Infeld]] (ed.), *Relativistic Theories of Gravitation*, Proceedings of a conference held in Warsaw and Jablonna 1962, Pergamon Press (1964) &lbrack;[pdf](https://cds.cern.ch/record/2282975/files/warsaw-1962.pdf)&rbrack;

Textbook accounts:

* [[Charles Misner]], [[Kip Thorne]], [[John Wheeler]], _[[Gravitation]]_ (1973)

* [[Robert Wald]], *General Relativity*, University of Chicago Press (1984) &lbrack;[doi:10.7208/chicago/9780226870373.001.0001](https://doi.org/10.7208/chicago/9780226870373.001.0001), [pdf](http://fma.if.usp.br/~mlima/teaching/PGF5292_2021/Wald_GR.pdf)&rbrack;

* [[Pietro Fré]], *Gravity, a Geometrical Course*, Volume 1: *Development of the Theory and Basic Physical Applications*, Spinger (2013) &lbrack;[doi:10.1007/978-94-007-5361-7](https://doi.org/10.1007/978-94-007-5361-7)&rbrack;

* [[Pietro Fré]], *Gravity, a Geometrical Course*, Volume 2: *Black Holes, Cosmology and Introduction to Supergravity*, Springer (2013) &lbrack;[doi:10.1007/978-94-007-5443-0](https://doi.org/10.1007/978-94-007-5443-0)&rbrack;

  > on [[black holes]], [[cosmology]] and the ([[D'Auria-Fré formulation of supergravity|D'Auria-Fré formulation of]]) [[supergravity]]

Lecture notes:

* [[Matthias Blau]], _Lecture notes on general relativity_ ([web](http://www.blau.itp.unibe.ch/GRLecturenotes.html))

* Emil T. Akhmedov, _Lectures on General Theory of Relativity_ ([arXiv:1601.04996](https://arxiv.org/abs/1601.04996))

* Pietro Menotti, _Lectures on gravitation_ ([arXiv:1703.05155](https://arxiv.org/abs/1703.05155))

See also 

* {#Coley18} [[Alan Coley]], _Mathematical General Relativity_ ([arXiv:1807.08628](https://arxiv.org/abs/1807.08628))

On gravity in relation to [[thermodynamics]]:

* [[Thanu Padmanabhan]], *Gravity and/is Thermodynamics*,  Current Science, **109** (2015) 2236-2242 &lbrack;[doi:10.18520/v109/i12/2236-2242](https://doi.org/10.18520/v109/i12/2236-2242)&rbrack;

* [[Thanu Padmanabhan]], *Exploring the Nature of Gravity*, talk notes &lbrack;[arXiv:1602.01474](https://arxiv.org/abs/1602.01474)&rbrack;


Discussion of classical gravity via its [[perturbative quantum field theory]]:

* {#Scharf01} [[Günter Scharf]], _[[Quantum Gauge Theories -- A True Ghost Story]]_, Wiley 2001

* Gustav Uhre Jakobsen, _General Relativity from Quantum Field Theory_ ([arXiv:2010.08839](https://arxiv.org/abs/2010.08839))


This way the theory of gravity based on the standard [[Einstein-Hilbert action]] may be regarded as just an [[effective quantum field theory]], which makes some of its notorious problems be non-problems:

* [[John Donoghue]], _Introduction to the Effective Field Theory Description of Gravity_ ([arXiv:gr-qc/9512024](http://arxiv.org/abs/gr-qc/9512024))

Relation of the [[first-order formulation of gravity]] to [[BF-theory]]:

* [[Alberto S. Cattaneo]], [[Leon Menger]], [[Michele Schiavina]], *Gravity with torsion as deformed BF theory* &lbrack;[arXiv:2310.01877](https://arxiv.org/abs/2310.01877)&rbrack;


See also the references at _[[general relativity]]_.


### Covariant phase space
 {#CovariantPhaseSpaceReferences}

The (reduced) [[covariant phase space]] of gravity (presented for instance by its [[BV-BRST complex]], see there fore more details) is discussed for instance in

* [[Romeo Brunetti]], [[Klaus Fredenhagen]], _Towards a Background Independent Formulation of Perturbative Quantum Gravity_ ([arXiv:gr-qc/0603079](http://arxiv.org/abs/gr-qc/0603079))

which is surveyed in

* Katarzyna Rejzner, _The BV formalism applied to classical gravity_ ([pdf](http://rejzner.com/talks/Karlsruhe2011.pdf))

Careful discussion of [[observables]] in gravity is in 

* {#Khavkine14} [[Igor Khavkine]],  _Local and gauge invariant observables in gravity_, talk at [Operator and Geometric Analysis on Quantum Theory](http://www.science.unitn.it/~moretti/convegno/convegno.html), preprint [arXiv:1503.03754](https://arxiv.org/abs/1503.03754)

Further discussion of the phase space of gravity in [[first-order formulation of gravity|first-order formulation]] via [[BV-BFV formalism]]:

* [[Michele Schiavina]], _BV-BFV approach to general relativity_ (2015) &lbrack;[pdf](http://user.math.uzh.ch/cattaneo/schiavina.pdf), [[Schiavina-Relativity.pdf:file]]&rbrack;

* {#CattaneoSchiavina15} [[Alberto Cattaneo]], [[Michele Schiavina]], _BV-BFV approach to General Relativity, Einstein-Hilbert action_, J. Math. Phys. **57** 023515 (2016) &lbrack;[arXiv:1509.05762](https://arxiv.org/abs/1509.05762), [doi:10.1063/1.4941410](https://doi.org/10.1063/1.4941410)&rbrack;

* {#CattaneoSchiavina17a} [[Alberto Cattaneo]], [[Michele Schiavina]], _The reduced phase space of Palatini-Cartan-Holst theory_, Ann. Henri Poincaré **20** (2019) 445 &lbrack;[arXiv:1707.05351](https://arxiv.org/abs/1707.05351), [doi:10.1007/s00023-018-0733-z](https://doi.org/10.1007/s00023-018-0733-z)&rbrack;

* {#CattaneoSchiavina17b} [[Alberto Cattaneo]], [[Michele Schiavina]], *BV-BFV approach to General Relativity: Palatini-Cartan-Holst action*, Adv. Theor. Math. Phys. **23**  (2019) 1801-1835 &lbrack;[arXiv:1707.06328](https://arxiv.org/abs/1707.06328), [doi:10.4310/ATMP.2019.v23.n8.a3](https://doi.org/10.4310/ATMP.2019.v23.n8.a3)&rbrack;

* [[Alberto S. Cattaneo]], *Phase space for gravity with boundaries*, in *[[Encyclopedia of Mathematical Physics 2nd ed]]* (2023) &lbrack;[arXiv:2307.04666](https://arxiv.org/abs/2307.04666)&rbrack;

  > (following [Kijowski & Tulczyjew (2005)](phase+space#KijowskiTulczyjew05))

Discussion of flux-observables:

* [[Alberto S. Cattaneo]], Alejandro Perez, *A note on the Poisson bracket of 2d smeared fluxes in loop quantum gravity*, Class. Quant. Grav. **34** (2017) 107001 &lbrack;[arXiv:1611.08394](https://arxiv.org/abs/1611.08394), [doi:10.1088/1361-6382/aa69b4](https://doi.org/10.1088/1361-6382/aa69b4)&rbrack;


### Non-renormalizability

The result that gravity is not [[renormalizable interaction|renormalizable]] is due to:

* {#tHooftVelrman74} [[Gerard 't Hooft]], [[Martinus Veltman]], _One loop divergencies in the theory of gravitation_, Ann. Inst. Poincar &#233; 20 (1974) 69 ([numdam:AIHPA_1974__20_1_69_0](AIHPA_1974__20_1_69_0))

Review:

* [[Zvi Bern]], _Perturbative quantum gravity and its relation to gauge theory_, Living reviews in relativity, [www.livingreviews.org/Articles/Volume5/2002-5bern](www.livingreviews.org/Articles/Volume5/2002-5bern)
.
* Assaf Shomer, _A pedagogical explanation for the non-renormalizability of gravity_ ([arXiv:0709.3555](https://arxiv.org/abs/0709.3555))


[[!redirects Einstein gravity]]

[[!redirects gravitation]]

[[!redirects gravitational field]]
[[!redirects gravitational fields]]

[[!redirects D=4 gravity]]
