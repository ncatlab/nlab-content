
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Physics
+--{: .hide}
[[!include physicscontents]]
=--
#### Differential cohomology
+--{: .hide}
[[!include differential cohomology - contents]]
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
 {#InHigherGaugeTheory}

The generalization of Gauss laws to [[higher gauge theory]] may transparently be understood, in broad generality, by casting the corresponding higher Maxwell-type [[equations of motion]] into "[[duality-symmetric gauge theory|duality-symmetric]]" form (we follow [SS23](#SS23)):

Consider:

* $D = 1 + d \in \mathbb{N}_{\geq 2}$ the [[spacetime]] dimension,

* $X^D$ a $D$-dimensional [[spacetime]] [[smooth manifold|manifold]],

* with [[Hodge star]]-operator on [[differential forms]]

  $$
    \star \,\colon\,
    \Omega^p_{dR}(X^D) \to \Omega^{D-p}_{dR}(X^D)
  $$

  satisfying (see [there](Hodge+star+operator#eq:HodgeSquareOnRiemannian))

  $$
    \star \, \star = - (-1)^{p(D-p)}
    \,,
  $$

* $I \,\in\, Set$ an [[index set]] of flux species 

  (subsuming both electric fluxes and magnetic fluxes, both now allowed of further different species),

* $\big( deg_i \,\in\, \mathbb{N}_{\geq 1} \big)_{i \in I}$ an [[indexed set]] of degrees,

* $\vec F \,\equiv\,\big( F^{(i)} \,\in\, \Omega^{deg_i}_{dR}(X^D) \big)_{i \in I}$ an [[indexed set]] of [[flux densities]]

* $\vec P = \big( P^{(i)}  \big)_{i \in I}$ an [[indexed set]] of graded-symmetric [[polynomials]] in $I$ [[variables]],

* $\vec \mu$ an [[invertible matrix|invertible]] $I \times I$-[[matrix]] 

then: 

\begin{definition}\label{HigherMaxwellInDualitySymmetricForm}
The corresponding **higher Maxwell-type equations** on these [[differential forms]]/[[flux densities]] are, in [[duality-symmetric higher gauge theory|duality-symmetric form]]: 

1. the system of [[Bianchi identity]] [[differential equations]]

   \[
     \label{HigherBianchiIdentities}
     \mathrm{d}\,\vec F 
     \,=\,
     \vec P\big(
       \vec F
     \big)
   \]

1. the self-[[Hodge duality]] condition

   \[
     \label{HigherSelfDuality}
     \star \, \vec F
     \,=\,
     \vec \mu\big(\vec F\big)
     \,.
   \]

\end{definition}

To extract a Gauss law from such a system of equations, consider the case that the [[spacetime]] $X^D$ is [[globally hyperbolic spacetime|globally hyperbolic]] with associated (by [this Prop.](Cauchy+surface#FoliationOfGloballyHyperbolicSpacetimes)) smooth [[foliation]] by [[spacelike]] [[Cauchy surfaces]] $X^d$ exhibited by a [[diffeomorphism]]:

$$
  X^D 
  \,\simeq\,
  \mathbb{R} \times X^d
  \,.
$$

This identifies the [[de Rham differential]] with the [[total differential]] of a [[double complex]] of [[differential forms]], bigraded by spatial and by temporal degree:

$$
  \mathrm{d}
  \,=\,
  \mathrm{d}_t + \mathrm{d}_s
  \,,
  \;\;\;\;\;
  \mathrm{d}_t \circ \mathrm{d}_t \,=\, 0
  \,,
  \;\;\;\;\;
  \mathrm{d}_s \circ \mathrm{d}_s \,=\, 0
  \,,
  \;\;\;\;\;
  \mathrm{d}_s \circ \mathrm{d}_t \,=\, 
  - 
  \mathrm{d}_t \circ \mathrm{d}_s
  \,. 
$$

Denoting by

$$
  \Omega^p_{dR}\big(
    X^D
  \big)_{\iota_{\partial_t}}
  \hookrightarrow
  \Omega^p_{dR}\big(
    X^D
  \big)_{\iota_{\partial_t}}
$$

the [[kernel]] of the [[tensor contraction|contraction]] with the corresponding [[timelike]] [[vector field]] $\partial_t$, every [[flux density]] now has a unique decomposition into a summand that has none and a summand that has one factor of $\mathrm{d}t$:

$$
  \vec F
  \;=\;
  \vec B
  \,+\,
  \star
  \vec E
  \,,
  \;\;\;\;
  \text{for}
  \;
  \left\{
  \,
  \begin{array}{l}
    \vec B \,\equiv\,
    \big(   
      B^{(i)} 
        \in 
     \Omega^{deg_i}_{dR}(X^D)_{\iota_{\partial_t} = 0}
    \big)
    \\
    \vec E \,\equiv\,
    \big(   
      E^{(i)} 
        \in 
     \Omega^{deg_i}_{dR}(X^D)_{\iota_{\partial_t} = 0}
    \big)
    \,.
  \end{array}
  \right.
$$

In terms of these components, the higher [[Bianchi identities]] (eq:HigherBianchiIdentities) are equivalent to the following system of [[differential equations]]:

* **higher Gauss laws**

  \[
    \label{HigherGaussLaw}
    \mathrm{d}_s
    \,
    \vec B
    \;=\;
    \vec P\big( \vec B \big)
  \]

* **higher Faraday-Amp&egrave;re laws**

  \[
    \label{HigherFaradayAmpereLaw}
    \mathrm{d}_t
    \,
    \vec B
    \;=\;
    - 
    \mathrm{d}_s \, 
    \star \vec E
    \,+\,
    \mathrm{d}_s
    \,
    \big(\star E^{(i)}\big)
    \wedge
    \frac{\delta}{\delta B^{(i)}}
    \vec P\big(
      \vec B
    \big)
    \,.
  \]

Hence in the [[duality-symmetric gauge theory|duality-symmetric formulation]] of [[higher gauge theory]], the Gauss law is just the spatial component of the [[Bianchi identity]].

Moreover, one finds that the higher Gauss law (eq:HigherGaussLaw) is a [[first class constraint]] in that it is preserved by the time evolution presribed by the higher Faraday-Amp&egrave;re law (eq:HigherGaussLaw), so that the solution space of the higher Maxwell equations is identified with the space of flux densities on any [[Cauchy surface]] 
$$
  \iota
  \,\colon\,
  X^d \hookrightarrow X^D
$$
that satisfy (just) the higher Gauss law:

<center>
<img src="/nlab/files/HigherGaussLaw-231221.jpg" width="800">
</center>

In examples relevant in practice, the [[functor|functorial]] assignment of these canonical solution spaces is [[representable functor|representable]] by the [[formal duality|formal dual]] of a [[dgc-algebra]] which embodies the [[Bianchi identities]] as abstract dg-algebraic relations:

\[
  \label{CharacteristicCEAlgebra}
  CE(\mathfrak{a})
  \;\coloneqq\;
  \mathbb{R}\Big[
    \vec b
    \,\equiv\,
    \big(
      b^{(i)}_{deg_i}
    \big)
  \Big]
  \Big/
  \Big(
    \mathrm{d} \vec b \,=\, \vec P(\vec b)
  \Big)
  \,,
\]

as

$$
  \Big\{
  \vec B
  \,\in\,
  \big(
    B^{(i)}
    \,\in\,
    \Omega^{deg_i}_{dR}(-)
  \big)_{i \in I}
  \,\Big\vert\,
  \mathrm{d}\, \vec B \,=\, \vec P\big(\vec B\big)
  \Big\}
  \;\;\;
  \simeq
  \;\;\;
  Hom_{dgAlg}\big(
    CE(\mathfrak{a})
    ,\,
    \Omega^{\bullet}_{dR}(-)
  \big)
  \,.
$$

This is equivalently the [[Chevalley-Eilenberg algebra]] of a characteristic [[L-infinity algebra|$L_\infty$-algebra]] $\mathfrak{a}$ (by the discussion [there](L-infinity-algebra#ReformulationInTermsOfSemifreeDGAlgebra)), making the right hand side the [[flat L-infinity-algebra valued differential forms|flat $L_\infty$-algebra valued differential forms]]:

$$
  SolSpace
  \;\simeq\;
  \Omega_{dR}\big(
    X^d
    ;\, 
    \mathfrak{a}
  \big)_{flat}
  \,,
$$

with the higher Gauss law being exactly the flatness condition.

\begin{example}
**(ordinary Gauss law as special case of higher Gauss law)**
\linebreak
  The ordinary case ([above](#InElectromagnetism)) of the Gauss law in [[vacuum]] [[electromagnetism]] (ie. with vanishing [[electric charge]] density) is obtained from Def. \ref{HigherMaxwellInDualitySymmetricForm} by setting

* $D \equiv 4$

* $I \equiv \{el, mag\}$

* $\vec P \equiv 0$

* $\vec \mu \equiv \left[\array{ 0 & -1 \\ 1 & 0 }\right]$.

This gives the electric and magnetic Gauss laws as

* $\mathrm{d} B^{(el)} \,=\, 0$

* $\mathrm{d} B^{(mag)} \,=\, 0$

where self-duality constraint identifies the elctric flux density equivalently as $B^{(el)} \,=\, E^{(mag)}$.
\end{example}

\begin{example}
**([[chiral boson]] in 2d)**
\linebreak
(...)
\end{example}


\begin{example}
**([[RR-fields]] in [[D=10 supergravity]])**
\linebreak
(...)
\end{example}

\begin{example}
**([[supergravity C-field|C-field]] in [[D=11 supergravity]])**
\linebreak
(...)
\end{example}


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

* [[Marc Henneaux]], [[Claudio Teitelboim]], p. 456 in: *[[Quantization of Gauge Systems]]*, Princeton University Press 1992 &lbrack;[ISBN:9780691037691](https://press.princeton.edu/books/paperback/9780691037691/quantization-of-gauge-systems), [jstor:j.ctv10crg0r](https://www.jstor.org/stable/j.ctv10crg0r)&rbrack;

In [[Yang-Mills theory]]:

* {#FriedmanPapastamatiou83} [[John L. Friedman]], Nicholas J. Papastamatiou, equation (3.9) in: *On the canonical quantization of Yang-Mills theories*, Nuclear Physics B **219** 1 (1983) 125-142 \[<a href="https://doi.org/10.1016/0550-3213(83)90431-5">doi:10.1016/0550-3213(83)90431-5</a>\]

In [[higher gauge theory]]:

* {#SS23} [[Hisham Sati]], [[Urs Schreiber]], *[[schreiber:Flux Quantization on Phase Space]]* &lbrack;[arXiv:2312.12517](https://arxiv.org/abs/2312.12517)&rbrack;




[[!redirects Gauss's law]]
[[!redirects Gauss' law]]
[[!redirects Gauß law]]

[[!redirects magnetic Gauss law]]
[[!redirects magnetic Gauss' law]]
[[!redirects magnetic Gauß law]]

[[!redirects electric Gauss law]]
[[!redirects electric Gauss' law]]
[[!redirects electric Gauß law]]


