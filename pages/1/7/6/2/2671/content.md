
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

The "non-propagating field" $\Omega$ is the [[spin connection]].

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

* [[Hořava–Lifshitz gravity]]

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

* [[Albert Einstein]], [[Marcel Grossmann]]: *Entwurf einer verallgemeinerten Relativitätstheorie und einer Theorie der Gravitation*, Teubner (2013) &lbrack;[[EinsteinGrossmann-Entwurf.pdf:file]]&rbrack;

* {#Infeld1962} [[Leopold Infeld]] (ed.), *Relativistic Theories of Gravitation*, Proceedings of a conference held in Warsaw and Jablonna 1962, Pergamon Press (1964) &lbrack;[pdf](https://cds.cern.ch/record/2282975/files/warsaw-1962.pdf)&rbrack;

On the early history of the idea:

* {#EarmanGlymor78} John Earman, Clark Glymour: *Lost in the tensors: Einstein's struggles with covariance principles 1912–1916*, Studies in History and Philosophy of Science Part A Volume 9, Issue 4, (1978) 251-278 \[<a href="https://doi.org/10.1016/0039-3681(78)90008-0">doi:10.1016/0039-3681(78)90008-0</a>\]


Monographs:

* [[Robert Geroch]]: *General Relativity -- 1972 Lecture Notes*, Minkowski Institute Press (2013) &lbrack;[ISBN:78-0-9879871-7-4](https://www.minkowskiinstitute.com/one/#!/products/r-0x2e--robert-geroch-0x2c--general-relativity), [pdf](http://strangebeautiful.com/other-texts/geroch-gr.pdf)&rbrack;


* [[Steven Weinberg]]: *Gravitation and Cosmology: Principles and Applications of the General Theory of Relativity*, Wiley  (1972, 2013) &lbrack;[ISBN:978-0-471-92567-5](https://www.wiley.com/en-us/Gravitation+and+Cosmology%3A+Principles+and+Applications+of+the+General+Theory+of+Relativity-p-9780471925675), [ark:/13960/t13n7rw1f](https://archive.org/details/WeinbergS.GravitationAndCosmology..PrinciplesAndApplicationsOfTheGeneralTheoryOf/page/n1/mode/2up), [spire:1410180](https://inspirehep.net/literature/1410180)&rbrack;

* [[Charles Misner]], [[Kip Thorne]], [[John Wheeler]], _[[Gravitation]]_ (1973)

* [[Theodore Frankel]]: *Gravitational Curvature*, Freeman, San Francisco (1979) &lbrack;[ark:13960/t58d7nn19](https://archive.org/details/gravitationalcur0000fran/)&rbrack;

* [[Robert Wald]], *General Relativity*, University of Chicago Press (1984) &lbrack;[doi:10.7208/chicago/9780226870373.001.0001](https://doi.org/10.7208/chicago/9780226870373.001.0001), [pdf](http://fma.if.usp.br/~mlima/teaching/PGF5292_2021/Wald_GR.pdf)&rbrack;

* [[Garth Warner]]: *Mathematical Aspects of General Relativity*, EPrint Collection, University Of Washington (2006) &lbrack;[hdl:1773/2637](http://hdl.handle.net/1773/2637), [pdf](https://sites.math.washington.edu//~warner/MAGR_Warner.pdf), [[Warner-GeneralRelativity.pdf:file]]&rbrack;

* [[Thanu Padmanabhan]], *Gravitation -- Foundations and Frontiers*, Cambridge University Press (2012) &lbrack;[doi:10.1017/CBO9780511807787](https://doi.org/10.1017/CBO9780511807787), [spire:852758](https://inspirehep.net/literature/852758), toc: [pdf](https://web.iucaa.in/~paddy/books/GRTOC.pdf)&rbrack;

* [[Pietro Fré]], *Gravity, a Geometrical Course*, Volume 1: *Development of the Theory and Basic Physical Applications*, Spinger (2013) &lbrack;[doi:10.1007/978-94-007-5361-7](https://doi.org/10.1007/978-94-007-5361-7)&rbrack;

* [[Pietro Fré]], *Gravity, a Geometrical Course*, Volume 2: *Black Holes, Cosmology and Introduction to Supergravity*, Springer (2013) &lbrack;[doi:10.1007/978-94-007-5443-0](https://doi.org/10.1007/978-94-007-5443-0)&rbrack;

  > on [[black holes]], [[cosmology]] and the ([[D'Auria-Fré formulation of supergravity|D'Auria-Fré formulation of]]) [[supergravity]]

Background on [[pseudo-Riemannian manifolds|pseudo-]][[Riemannian geometry]]:

* [[Barrett O'Neill]], *Semi-Riemannian Geometry With Applications to Relativity*, Pure and Applied Mathematics **103**, Academic Press (1983) &lbrack;[ISBN:9780125267403](https://shop.elsevier.com/books/semi-riemannian-geometry-with-applications-to-relativity/oneill/978-0-12-526740-3)&rbrack;

* [[Shlomo Sternberg]], *Semi-Riemannian Geometry and General Relativity* (2003) &lbrack;[pdf](https://people.math.harvard.edu/~shlomo/docs/semi_riemannian_geometry.pdf), [ark:/13960/t5m927d2v](https://archive.org/details/Shlomo_Sternberg__SemiRiemann_Geometry_and_General_Relativity/)&rbrack;

* [[Shlomo Sternberg]], *Curvature in Mathematical Physics*, Dover (2012) &lbrack;[ISBN:9780486478555](https://store.doverpublications.com/products/9780486478555)&rbrack;


Lecture notes:

* [[Matthias Blau]], _Lecture notes on general relativity_ ([web](http://www.blau.itp.unibe.ch/GRLecturenotes.html))

* Emil T. Akhmedov, _Lectures on General Theory of Relativity_ ([arXiv:1601.04996](https://arxiv.org/abs/1601.04996))

* Pietro Menotti, _Lectures on gravitation_ ([arXiv:1703.05155](https://arxiv.org/abs/1703.05155))

* [[Daniel Baumann]], *[General Relativity](http://cosmology.amsterdam/general-relativity/)* (2021-24) &lbrack;[pdf](http://cosmology.amsterdam/wp-content/uploads/2021/10/GR-Oct19.pdf), [pdf](https://cdn.prod.website-files.com/65c089cfdfce11a0392e5c42/67469a196f855821380fffa4_GR-2024.pdf)&rbrack;

* [[Edward Witten]], *Light Rays, Singularities, and All That*, Rev. Mod. Phys. **92** 45004 (2020) &lbrack;[arXiv:1901.03928](https://arxiv.org/abs/1901.03928), [doi:10.1103/RevModPhys.92.045004](https://doi.org/10.1103/RevModPhys.92.045004), lecture: [video 1](https://www.youtube.com/watch?v=-vS_WIa0vYo), [2](https://www.youtube.com/watch?v=4kEiNotDhck), [3](https://www.youtube.com/watch?v=Qje1ak6XF20), [4](https://www.youtube.com/watch?v=tzt25nkGg3Q), [5](https://www.youtube.com/watch?v=yC5BHqPw38Q), [6](https://www.youtube.com/watch?v=GHPL2_aomo8), [7](https://www.youtube.com/watch?v=tDeQ9ght3aI), [8](https://www.youtube.com/watch?v=fsmcGpKFbFU), [9](https://www.youtube.com/watch?v=Z_crNwSKpW0)&rbrack;
  > (with focus on [[causal structure]], the [[Penrose singularity theorem]] and related aspects)

* [[Kirill Krasnov]], *Formulations of General Relativity*, PIRSA lecture series (Feb 2019) &lbrack;part 1:[doi:10.48660/19020079](https://doi.org/10.48660/19020079), 2:[doi:10.48660/19020080](https://doi.org/10.48660/19020080), 3:[doi:10.48660/19020081](https://doi.org/10.48660/19020081), 4:[doi:10.48660/19020082](https://doi.org/10.48660/19020082)&rbrack;


* Peter Hayman: *A Lean and Mean Introduction to Modern General Relativity* &lbrack;[arXiv:2412.08026](https://arxiv.org/abs/2412.08026)&rbrack;


See also 

* {#Coley18} [[Alan Coley]], _Mathematical General Relativity_ ([arXiv:1807.08628](https://arxiv.org/abs/1807.08628))

With focus on methods of [[conformal geometry]] ([[conformal boundaries]], [[conformal compactification]]):

* [[Juan A. Valiente Kroon]]: *Conformal Methods in General Relativity*, Cambridge University Press (2017, 2022) &lbrack;[doi:10.1017/9781009291309](https://doi.org/10.1017/9781009291309), [oapen:20.500.12657/59217](https://library.oapen.org/handle/20.500.12657/59217), [pdf](https://library.oapen.org/bitstream/id/548cfabe-a25b-4562-b95e-aa2894525f32/9781009291309.pdf)&rbrack;



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
