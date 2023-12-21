
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
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
 {#Idea}

The *Gauss law* is, originally, one of the [[equations of motion]] of [[electromagnetism]], specifically of its [[electric field]]-sector, relating the [[divergence]] of the [[electric field]] to the [[electric charge]] density at each point of space. But the name has come to be commonly used also more generally for the corresponding equation of [[Yang-Mills theory]] and also for [[higher gauge theories]], all of which are closely similar equations when formulated via [[differential forms]] in [[exterior calculus]].

In the [[Hamiltonian mechanics|Hamiltonian]] formulation of these theories, the Gauss law appears as a [[first class constraint]] on the [[canonical phase space]] whose [[Hamiltonian vector field]] is that which generates the [[gauge transformations]].

In form analogous to the Gauss law is a dual statement for the [[magnetic field]], accordingly also known as the *magnetic Gauss law* and as such also part of [[Maxwell's equations]]. However, in traditional [[Hamiltonian mechanics|Hamiltonian]] [[phase space]]-formulation of [[electromagnetism]], where the magnetic but not the electric field is assumed to have a [[gauge potential]], the symmetry between these two laws is broken (the magnetic Gauss law is not a phase space constraint but a differential [[Bianchi identity]] implied by the existence of a gauge potential).

## Statement

### In electromagnetism
 {#InElectromagnetism}

In its original form (named after [Gauß 1877](#Gauß1877)), the *Gauß law* of [[electromagnetism]] asserts that the total [[flux]] of the [[electric field]] through any [[closed manifold|closed]] [[surface]] (in physical space) is proportional to the total [[electric charge]] enclosed by that surface, otherwise irrespective of the charge distribution. In its differential form, the Gauss law is part of what later became [[Maxwell's equations]] of [[electromagnetism]].

In terms of modern [[differential geometry]], with 

* $X^3$ denoting the [[dimension of a manifold|3-dimensional]] [[smooth manifold]] representing physical space (in this context often but not necessarily assumed to be the [[Euclidean space]] $\mathbb{R}^3$), 

* $E \,\in\, \Omega^2_{dR}(\mathbb{R}^4)$ denoting the [[differential 2-form]] which representes the electric field's [[flux density]]

  (beware that this 2-form is the spatial [[Hodge dual]] of the electric [[vector field]] 1-form used elsewhere),

* $\Sigma^3 \hookrightarrow X^3$ denoting an [[orientation|orientable]] 3-[[dimension of a manifold|dimensional]] [[submanifold]] [[manifold with boundary|with boundary]],

* $\partial \Sigma^3 = \Sigma^2 \hookrightarrow X^3$ denoting its [[boundary]], a [[closed manifold|closed]] [[orientation|orientable]] 2-[[dimension of a manifold|dimensional]] [[submanifold]],

* $Q \in \mathbb{R}$ denoting the **total [[electric charge]] on $\Sigma^3$**,

* $\int_{\Sigma^2} E$ denoting the [[integration of differential forms|integral]] of $E$ over $\Sigma$, hence the **total electric [[flux]] through $\Sigma^2$**,

the Gauss law in its original **integral form** states that the last two quantities are proportional to each other:

\[
  \label{IntegralFormOfEMGaussLaw}
  \textstyle{\int_{\Sigma^2}} E
  \;\;\propto\;\;
  Q
  \,,
\]

with the constant of proportionality depending on conventions but typically being the inverse of the [[permittivity of the vacuum]].

By the [[Stokes theorem]] and with

* $\rho \,\in\, \Omega^3_{dR}(X^3)$ denoting a [[differential 3-form]] representing the electric charge density, i.e. such that 

* $\int_{\Sigma^3} \rho \,=\, Q$,

* $\mathrm{d} E$ denoting the [[de Rham differential]] of the electric flux density, representing its [[divergence]],

the integral law (eq:IntegralFormOfEMGaussLaw) is equivalent to the following **differential form** of the Gauss law:

\[
  \label{DifferentialFormOfEMGaussLaw}
  \mathrm{d} E \,=\, \rho
  \,.
\]

It is in this differential form that the Gauss law is part of the modern form of [[Maxwell's equations]] (see their formulation in [[exterior calculus]] [here](Maxwell's+equations#InTermsOfFaradayTensor)). 



### In Yang-Mills theory
 {#InYangMillsTheory}

The differential form of the Gauss law (eq:DifferentialFormOfEMGaussLaw) generalizes immediately to [[Yang-Mills theory]] with [[gauge group|gauge]] [[Lie algebra]] $mathfrak{g}$ by enhancing the [[de Rham differential]] to the corresponding [[covariant derivative|covariant differential]]  with respect to the given [[gauge potential]].


(...)

### In higher gauge theory

The generalization of Gauss laws to [[higher gauge theory]] may transparently be understood, in broad generality, by casting the corresponding higher Maxwell-type [[equations of motion]] into "[[duality-symmetric gauge theory|duality-symmetric form]]:

Consider

* $D \in \mathbb{N}_{\geq 2}$,

* $X^D$ a $D$-dimensional [[spacetime]] manifold,

  with [[Hodge star]]-operator on [[differential forms]]

  $$
    \star \,\colon\,
    \Omega^p_{dR}(X^D) \to \Omega^{D-p}_{dR}(X^D)
  $$

  satisfying (see [there](Hodge+star+operator#eq:HodgeSquareOnRiemannian))

  $$
    \star \, \star = - (-1)^{p(D-p)}
  $$

* $I \,\in\, Set$ an [[index set]] of flux species 

  (subsuming both electric fluxes and magnetic fluxes, both now allowed to appear in various degrees)

* $\big( deg_i \,\in\, \mathbb{N}_{\geq 1} \big)_{i \in I}$ an [[indexed set]] of degrees,

* $\vec F \,\equiv\,\big( F^{(i)} \,\in\, \Omega^{deg_i}_{dR}(X^D) \big)_{i \in I}$ an [[indexed set]] of [[flux densities]]

* $\vec P = \big( P^{(i)}  \big)_{i \in I}$ an [[indexed set]] of graded-symmetric [[polynomials]] in $I$ [[variables]],

* $\vec \mu$ an [[invertible matrix|invertible]] $I \times I$-[[matrix]] 

then

(...)


## Related concepts

* [[constrained mechanics]]

* [[first class constraint]]

* [[uncertainty of fluxes]]

## References


### General

Named after:

* {#Gauß1877} [[Carl F. Gauß]], *Theoria attractionis corporum sphaeroidicorum ellipticorum homogeneorum, methodo nova tractata*, Commentationes Societatis Regiae Scientiarum G&ouml;ttingensis Recentiores. Comm. Class. Math. **2** (1813) 1–24 &lbrack;[PPN35283028X_0002_2NS](http://resolver.sub.uni-goettingen.de/purl?PPN35283028X_0002_2NS)&rbrack;

  reprinted in: *Carl Friedrich Gauss -- Werke* **5**, Springer (1877) 2-22 &lbrack;[doi:10.1007/978-3-642-49319-5_1](https://doi.org/10.1007/978-3-642-49319-5_1)&rbrack;

For more see any of the references at *[[Maxwell's equations]]*, such as:

* [[Friedrich W. Hehl]], [[Yuri N. Obukhov]], I.1 & B1.45 in: *Foundations of Classical Electrodynamics -- Charge, Flux, and Metric*, Progress in Mathematical Physics **33**, Springer (2003) &lbrack;[doi:10.1007/978-1-4612-0051-2](https://doi.org/10.1007/978-1-4612-0051-2)&rbrack;

See also:

* Wikipedia, *[Gauss's law](https://en.wikipedia.org/wiki/Gauss%27s_law)*


### As a phase space constraint

Discussion of the Gauss law as a [[first-class constraint|first-class]] [[constrained mechanics|constraint]] on [[phase space]]:

In [[Maxwell theory]]:

* {#BlaschkeGieres21} [[Daniel N. Blaschke]], [[François Gieres]], equation (5.8) in: *On the canonical formulation of gauge field theories and Poincaré transformations*, Nuclear Physics B **965** (2021) 115366 &lbrack;[doi:10.1016/j.nuclphysb.2021.115366](https://doi.org/10.1016/j.nuclphysb.2021.115366), [arXiv:2004.14406](https://arxiv.org/abs/2004.14406)&rbrack;


In [[Yang-Mills theory]]:

* {#FriedmanPapastamatiou83} [[John L. Friedman]], Nicholas J. Papastamatiou, equation (3.9) in: *On the canonical quantization of Yang-Mills theories*, Nuclear Physics B **219** 1 (1983) 125-142 \[<a href="https://doi.org/10.1016/0550-3213(83)90431-5">doi:10.1016/0550-3213(83)90431-5</a>\]

Textbok account for abelian YM ([[electromagnetism]], [[Maxwell theory]]):

* [[Marc Henneaux]], [[Claudio Teitelboim]], p. 456 in: *[[Quantization of Gauge Systems]]*, Princeton University Press 1992 &lbrack;[ISBN:9780691037691](https://press.princeton.edu/books/paperback/9780691037691/quantization-of-gauge-systems), [jstor:j.ctv10crg0r](https://www.jstor.org/stable/j.ctv10crg0r)&rbrack;


[[!redirects Gauss's law]]
[[!redirects Gauss' law]]
[[!redirects Gauß law]]

[[!redirects magnetic Gauss law]]
[[!redirects magnetic Gauss' law]]
[[!redirects magnetic Gauß law]]

[[!redirects electric Gauss law]]
[[!redirects electric Gauss' law]]
[[!redirects electric Gauß law]]


