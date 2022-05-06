
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

> for the moment see [[D'Auria-Fre formulation of supergravity]] for further details

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


* [[2d gravity]]

  * [[Liouville theory]]

  * [[Jackiw-Teitelboim gravity]]


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

Textbooks include

* [[Charles Misner]], [[Kip Thorne]], [[John Wheeler]], _[[Gravitation]]_, 1973

Lecture notes

* [[Matthias Blau]], _Lecture notes on general relativity_ ([web](http://www.blau.itp.unibe.ch/GRLecturenotes.html))

* Emil T. Akhmedov, _Lectures on General Theory of Relativity_ ([arXiv:1601.04996](https://arxiv.org/abs/1601.04996))

* Pietro Menotti, _Lectures on gravitation_ ([arXiv:1703.05155](https://arxiv.org/abs/1703.05155))


See also 

* {#Coley18} [[Alan Coley]], _Mathematical General Relativity_ ([arXiv:1807.08628](https://arxiv.org/abs/1807.08628))

Discussion of classical gravity via its [[perturbative quantum field theory]]:

* {#Scharf01} [[Günter Scharf]], _[[Quantum Gauge Theories -- A True Ghost Story]]_, Wiley 2001

* Gustav Uhre Jakobsen, _General Relativity from Quantum Field Theory_ ([arXiv:2010.08839](https://arxiv.org/abs/2010.08839))


This way the theory of gravity based on the standard [[Einstein-Hilbert action]] may be regarded as just an [[effective quantum field theory]], which makes some of its notorious problems be non-problems:

* [[John Donoghue]], _Introduction to the Effective Field Theory Description of Gravity_ ([arXiv:gr-qc/9512024](http://arxiv.org/abs/gr-qc/9512024))

See also the references at _[[general relativity]]_.


### Covariant phase space
 {#CovariantPhaseSpaceReferences}

The (reduced) [[covariant phase space]] of gravity (presented for instance by its [[BV-BRST complex]], see there fore more details) is discussed for instance in

* [[Romeo Brunetti]], [[Klaus Fredenhagen]], _Towards a Background Independent Formulation of Perturbative Quantum Gravity_ ([arXiv:gr-qc/0603079](http://arxiv.org/abs/gr-qc/0603079))

which is surveyed in

* Katarzyna Rejzner, _The BV formalism applied to classical gravity_ ([pdf](http://rejzner.com/talks/Karlsruhe2011.pdf))

Careful discussion of [[observables]] in gravity is in 

* {#Khavkine14} [[Igor Khavkine]],  _Local and gauge invariant observables in gravity_, talk at [Operator and Geometric Analysis on Quantum Theory](http://www.science.unitn.it/~moretti/convegno/convegno.html), preprint [arXiv:1503.03754](https://arxiv.org/abs/1503.03754)

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
