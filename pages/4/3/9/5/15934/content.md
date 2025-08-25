
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Manifolds and cobordisms
+--{: .hide}
[[!include manifolds and cobordisms - contents]]
=--
=--
=--


\tableofcontents


## Definition

A _Seifert 3-manifold_ is a [[3-manifold]] which is the total space of a [[circle]]-[[fiber bundle]] ([[circle bundle]]) over a 2-dimensional [[orbifold]]. Since the circle-fibration [[structure]] may not be unique, one also speaks, more explicitly, of *Seifert-fibered manifolds*.

If already the total space is a 3-[[orbifold]], one correspondingly speaks of a *Seifert orbifold* etc. (e.g. [Mecchia & Seppi 2020 Def. 2.6](#MecchiaSeppi20)).

Fully generally one speaks of *Seifert fibrations*. 

> (Beware that there is also the *un-related* notion of *[[Seifert surfaces]]*, also considered in higher dimensions: These are [[coboundaries]] of [[knots]].)

{#LocalStructure} Accordingly, a general Seifert fibration is locally an [[orbifold quotient]] [[fibration]] of the form

$$
  \big(
    D^2 \times S^1
  \big)
  \sslash
  \mathbb{Z}_n
  \xrightarrow{
    pr_{D^2} \sslash \mathbb{Z}_n
  }
  D^2
  \sslash
  \mathbb{Z}_n
  \,,
$$

where the [[cyclic group]] $\mathbb{Z}_n \coloneqq \mathbb{Z}/n$ [[group action|acts]] [[diagonal action|diagonally]] via [[rotations]] by 

1. the [[angle]] $2\pi\tfrac{1}{a}$ on the [[2-disk]] $D^2 = \big\{ z \in \mathbb{C} \,\big\vert\, {\vert z\vert} \lt 1 \big\}$,

1. an [[angle]] $-2\pi\tfrac{b}{a}$ on the [[circle]] $S^1 \simeq \big\{ \xi \in \mathbb{C} \,\big\vert\, {\vert \xi \vert} = 1 \big\}$,

$$
  (z, \xi)
  \,\sim\,
  \big(
    z \, q
    ,\,
    \xi \, q^{-b}
  \big)
  \,,
  \;\;\;\;
  q \coloneqq \exp\big(2\pi \mathrm{i} \tfrac{1}{a}\big)
  \,.
$$

with $a,b  \in \mathbb{Z}$, $a \geq 2$ (not necessarily [[coprime integer|coprime]]), their [[fraction]] $b/a$ also called the *slope modulo 1* of the fibration at this point:


This [[orbifold quotient]] is a non-singular (Seifert-fibered) [[smooth manifold]] iff $a$ and $b$ are [[coprime integers]], otherwise it is an [[orbifold]] whose orbi-singular ([[fixed point|fixed]]) locus has [[isotropy group]] $\mathbb{Z}_{gcd}$ determined by the [[greatest common divisor]] $gcd \coloneqq gcd(a,b)$.

([Bonahon & Siebenmann 2010 p 36 (18 of 67)](#BonahonSiebenmann10))



## Related concepts

* [[lens space]]

Beware that there is also the *un-related* concept of 

* [[Seifert surfaces]]


## References

### Seifert 3-manifolds

The original article:

* [[Herbert Seifert]]: *Topology of 3-dimensional fibered spaces*, in: *A textbook of topology*, Pure Appl. Math. **89**, Academic Press (1980) 139–152 &lbrack;[pdf](https://www.math.csi.cuny.edu/abhijit/k3m/Seifert-FiberedSpaces-english.pdf)&rbrack;

Review:

* Mark Jankins, Walter Neumann: *Lectures on Seifert Manifolds*, Brandeis University (1981) &lbrack;[pdf](https://www.math.columbia.edu/department/neumann/preprints/neumann_lectures%20on%20seifert%20manifolds.pdf), [[JankinsNeumann-SeifertManifolds.pdf:file]]&rbrack;

* [[Peter Scott]], section  3 in: *The Geometries of 3-Manifolds*, Bulletin of the LMS **15** 5 (1983) 401-487 &lbrack;[doi:10.1112/blms/15.5.401](https://doi.org/10.1112/blms/15.5.401), [hdl:2027.42/135276](https://hdl.handle.net/2027.42/135276)&rbrack;


Monographs:

* [[Kyung Bai Lee]], [[Frank Raymond]]: *Seifert Fiberings*, Mathematical Surveys and Monographs (2010) **166** &lbrack;[doi:10.1090/surv/166](https://doi.org/10.1090/surv/166), toc:[pdf](https://www.ams.org/books/surv/166/surv166-endmatter.pdf)&rbrack;



Further survery:

* [[Kyung Bai Lee]], [[Frank Raymond]]: *Seifert Manifolds* &lbrack;[arXiv:math/0108188](https://arxiv.org/abs/math/0108188)&rbrack;

Discussion via [[diffeological spaces]]:

* [[Patrick Iglesias-Zemmour]], Jean-Paul Mohsen: *Seifert Orbifolds* (2015) &lbrack;[pdf](http://math.huji.ac.il/~piz/documents/DBlog-Rmk-SeifO.pdf), [[IglesiasZemmour-Mohsen-SeifertOrbifolds.pdf:file]]&rbrack;

See also:

* Wikipedia, _[Seifert fiber space](http://en.wikipedia.org/wiki/Seifert_fiber_space)_

* [[Encyclopedia of Mathematics]]: *[Seifert fibration](https://encyclopediaofmath.org/index.php?title=Seifert_fibration)*


### Seifert 3-orbifolds

Generalization to the case that already the total space is an [[orbifold]] (not just its $S^1$-quotient):

* {#BonahonSiebenmann10} [[Francis Bonahon]], [[Laurent C. Siebenmann]]: *The classification of Seifert fibred 3-orbifolds*, in: *Low Dimensional Topology*, Cambridge University Press (2010) 19-85 &lbrack;[doi:10.1017/CBO9780511662744.002]( https://doi.org/10.1017/CBO9780511662744.002)&rbrack;

See also:

* {#MecchiaSeppi20} Mattia Mecchia, Andrea Seppi: *On the diffeomorphism type of Seifert fibered spherical 3-orbifolds*, Rend. Istit. Mat. Univ. Trieste **52** (2020) 1-39 &lbrack;[arXiv:2005.12023](https://arxiv.org/abs/2005.12023), [doi:10.13137/2464-8728/30920](https://doi.org/10.13137/2464-8728/30920)&rbrack;



### In field theory

On the [[3d-3d correspondence]] for Seifert manifolds:

* [[Sergei Gukov]], [[Du Pei]], pp 7 in: *Equivariant Verlinde formula from fivebranes and vortices*, Commun. Math. Phys. **355** (2017) 1–50 &lbrack;[arXiv:1501.01310](https://arxiv.org/abs/1501.01310), [doi:10.1007/s00220-017-2931-9](https://doi.org/10.1007/s00220-017-2931-9)&rbrack;

* [[Du Pei]]: *3d-3d correspondence for Seifert manifolds*, PhD thesis (2016) &lbrack;[spire:1469350](https://inspirehep.net/literature/1469350), [pdf](https://inspirehep.net/files/d509ff9e32448da3a5674f286b93224a)&rbrack;


Claim of [[geometric engineering of QFT|geometric engineering]] of [[topological order]] on [[M5-branes]] in the guise of [[fusion categories]]:

* Gil Young Cho, [[Dongmin Gang]], Hee-Cheol Kim: *M-theoretic Genesis of Topological Phases*, J. High Energ. Phys. **2020** 115 (2020) \[<a href="https://arxiv.org/abs/2007.01532">arXiv:2007.01532</a>, <a href=" https://doi.org/10.1007/JHEP11(2020)115">doi:10.1007/JHEP11(2020)115</a>\]
  > (by [[wrapped brane|wrapping]] [[M5-branes]] on, among others, Seifert manifolds)

* [[Shawn X. Cui]], [[Yang Qiu]], [[Zhenghan Wang]], *From Three Dimensional Manifolds to Modular Tensor Categories*, Commun. Math. Phys. **397** (2023) 1191–1235 \[<a href="https://doi.org/10.1007/s00220-022-04517-4">doi:10.1007/s00220-022-04517-4</a>, [arXiv:2101.01674](https://arxiv.org/abs/2101.01674)\]

* [[Federico Bonetti]], [[Sakura Schäfer-Nameki]], Jingxiang Wu: *$MTC[M_3,G]$: 3d Topological Order Labeled by Seifert Manifolds* &lbrack;[arXiv:2403.03973](https://arxiv.org/abs/2403.03973)&rbrack;

See also:

* Nathan Paul Moore: *String Theory, Chern-Simons Theory and the Fractional Quantum Hall Effect*, PhD thesis (2014) &lbrack;[spire:1783390](https://inspirehep.net/literature/1783390)&rbrack;


[[!redirects Seifert fibrations]]

[[!redirects Seifert fiber space]]
[[!redirects Seifert fiber spaces]]

[[!redirects Seifert-fibered manifold]]
[[!redirects Seifert-fibered manifolds]]

[[!redirects Seifert manifold]]
[[!redirects Seifert manifolds]]


[[!redirects Seifert 3-manifold]]
[[!redirects Seifert 3-manifolds]]


[[!redirects Seifert orbifold]]
[[!redirects Seifert orbifolds]]

[[!redirects Seifert 3-orbifold]]
[[!redirects Seifert 3-orbifolds]]


