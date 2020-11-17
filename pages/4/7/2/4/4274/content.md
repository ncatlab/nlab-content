

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Index theory
+-- {: .hide}
[[!include index theory - contents]]
=--
#### Elliptic cohomology
+-- {: .hide}
[[!include elliptic cohomology -- contents]]
=--
#### String theory
+-- {: .hide}
[[!include string theory - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

The _Witten genus_ is a [[genus]] with [[coefficients]] in [[power series]] in one variable, playing the role of a universal [[elliptic genus]].
This arises ([Witten 87](#Witten87)) as the [[large volume limit]] of the [[partition function]] of the [[superstring]] (hence in the string worldsheet [[perturbation theory]] about constant [[worldsheet]] configurations). Specifically, for the [[type II superstring]] this reproduces the universal [[elliptic genus]] as previously introduced by [[Serge Ochanine]], while for the [[heterotic string]] it yields what is now called the Witten genus proper.
Concretely, as Witten argued, this is a formal [[power series]] in string oscillation modes of the [[A-hat genus]] of the symmetric [[tensor powers]] of the [[tangent bundle]] that these modes take values in.

In ([Witten 86](#Witten86)) it is suggested, by regarding the [[superstring]] [[sigma-model]] as [[quantum mechanics]] on the [[smooth loop space]] of its [[target space]], that the Witten genus may be thought of as the [[large volume limit]] of an $S^1$-equivariant [[A-hat genus]] on [[smooth loop space]], hence the [[index]] of the [[Dirac-Ramond operator]] in that limit.  (Ever since this suggestion people have tried to make precise the concept of Dirac operator on a [[smooth loop space]] (e.g. [Alvarez-Killingback-Mangano-Windey 87](#AlvarezKillingbackManganoWindey87)). But notice that, by the above, only the [[formal loop space]] and the [[Dirac-Ramond operator]] really appears in the definition of the Witten genus.)

A priori the [[coefficients]] of the Witten genus as a genus on [[orientation|oriented]] manifolds are [[formal power series]] over the [[rational numbers]]

$$
  w \;\colon\; M SO_\bullet \longrightarrow \mathbb{Q}[ [ q ] ]
  \,.
$$

In the construction from [[string theory|string physics]] this map is interpreted as sending a [[target space|target]] [[spacetime]] $X$ of the [[superstring]] to the function $w_X(q) = w_X(e^{2 \pi i \tau})$ which to each modulus $\tau \in \mathbb{C}$ characterizing a toroidal [[Riemann surface]] assigns the [[partition function]] of the [[superstring]] with [[worldsheet]] the [[torus]] $\mathbb{C}/(\mathbb{Z} + \mathbb{Z}\tau)$ and propagating on [[target space]] $X$.

On manifolds with [[spin structure]] the genus refines to integral power series (via the integrality of the [[A-hat genus]] ([Chudnovsky-Chudnovsky 88](#ChudnovskyChudnovsky88), [Kreck-Stolz 93](#KreckStolz93), [Hovey 91](#Hovey91)). Moreover on manifolds with rational string structure it takes values in [[modular forms]] ([Zagier 86](#Zagier86)) and crucially, on manifolds with [[string structure]] it takes values in [[topological modular forms]] 

$$
  \array{
     M String_\bullet &\longrightarrow& 
     tmf_\bullet
       \\
     \downarrow && \downarrow
     \\
     \Omega_\bullet^{String, rat} &\longrightarrow& MF_\bullet  
     \\
     \downarrow && \downarrow
     \\
     M Spin_\bullet &\longrightarrow& \mathbb{Z}[[ q ] ]
     \\
     \downarrow && \downarrow
     \\
     M SO_\bullet &\stackrel{w}{\longrightarrow}& \mathbb{Q}[ [ q ] ]
  }
  \,.
$$

(On the left is the image under forming [[Thom spectra]]/[[cobordism rings]] of the first stages in the [[Whitehead tower]] of $BO$, see also at _[[higher spin structure]]_.)

Observe here that [[topological modular forms]] are the [[coefficient]] [[ring]] 
of the [[E-∞ ring]] [[spectrum]] known as _[[tmf]]_. By the general way in which [[genera]] (see there) tend to appear as [[decategorifications]] of [[homomorphisms]] of [[E-∞ rings]] out of a [[Thom spectrum]], this suggests that the Witten genus is the value on [[homotopy groups]] of a homomorphism of [[E-∞ rings]] of the form

$$
 \sigma \colon M String \longrightarrow tmf
$$

from the [[Thom spectrum]] of [[String bordism]] to the [[tmf]]-spectrum.  This lift of the Witten genus to a universal [[orientation in generalized cohomology|orientation]] in universal [[elliptic cohomology]] indeed exists and is called the _[[sigma-orientation]]_, or the _[[string orientation of tmf]]_.

This construction has been the central motivation behind the search for and construction of [[tmf]] ([Hopkins 94](#Hopkins94)). A construction of the [[string orientation of tmf]] is given in ([Ando-Hopkins-Rezk 10](#AndoHopkinsRezk)) and it is shown that indeed it refines the Witten genus ([Ando-Hopkins-Rezk 10, prop. 15.3](#AndoHopkinsRezk)).

It is maybe noteworthy that [[tmf]] (and hence its universal string orientation) also arises canonically from just studying [[chromatic homotopy theory]] (see [Mazel-Gee 13](#tmf#MazelGee13) for a nice survey of this) a fundamental topic in [[stable homotopy theory]], hence a fundamental topic in [[mathematics]]. Therefore in the Witten genus some very fundamental pure mathematics happens to equivalently incarnate as some conjecturally very fundamental [[physics]] ([[string theory]]).


## Properties

### Characteristic series
 {#CharacteristicSeries}

The [characteristic series](genus#LogarithmAndCharacteristicSeries) of the Witten genus as a [[power series]] in $z$ with [[coefficients]] in formal power series in $q$ over $\mathbb{Q}$ is

$$
  \begin{aligned}
    K_w(z)(q)
    & = 
    \frac{z}{\exp_w(z)(q)}
    \\
    & = 
    \frac{z}{\sigma_L(z)(q)}
    \\
    & =
    \frac{z/2}{sinh(z/2)}
    \prod_{n \geq 1}
    \frac{(1-q^n)^2}{(1-q^n e^z)(1-q^n e^{-z})}
      \\
      & = 
      \exp\left(
        \sum_{k \geq 2} G_k(q) \frac{z^k}{k!}
      \right)
   \end{aligned}
  \,,
$$

where 

* $\sigma_L$ is the [[Weierstrass sigma-function]] (see e.g. [Ando Basterra 00, section 5.1](#AndoBasterra00));

* $G_k$ are the [[Eisenstein series]] ([Zagier 86, equation (14)](#Zagier86), [Ando-Hopkins-Rezk 10, prop. 10.9](#AndoHopkinsRezk10)).

This is a [[modular form]] with respect to the variable $q$, see also the the discussion below at _[Integrality and modularity](#IntegralityAndModularity)_ . Such functions which are power series of two variables $z$ and $q$ with elliptic nature in $z$ and modular nature in $q$ are called _[[Jacobi forms]]_ ([Zagier 86, p. 8](#Zagier86), [Ando-French-Ganter 08](#AndoFrenchGanter08)).

There are various further ways to equivalently re-express the above in terms of other special [[modular forms]]. Here are some:

#### In terms of Kac-Weyl characters
 {#CharacteristicSeriesInTermsOfKacWeylCharacters}

The Witten genus has a close relation to the [[Kac-Weyl character]] of [[loop group representations]].

Consider of four [[irreducible representations|irreducible]] [[level]]-1  positive energy [[Spin group|Spin]]$(2k)$-[[loop group representation]] the one denoted

$$
  \tilde S_+ - \tilde S_- \in Rep(\tilde L Spin(2k))
$$

and write its [[Kac-Weyl character]] as

$$
  \chi(\tilde S_+ - \tilde S_-) \in Rep(Spin(2k))[ [ q^{1/12} ] ]
  \,.
$$

Under passing to [[group characters]] this is ([Brylinski 90, p. 7(467)](#Brylinski90), reviewed in [KL 96, section 1.2](#KL96)) equivalently 

$$
  \chi(\tilde S_+ - \tilde S_-) = \frac{\prod_{1}^k \theta}{\eta^k}
 \,,
$$

where on the right we have the [[Jacobi theta-function]] $\theta$ divided by the [[Dedekind eta-function]] $\eta$. 

Comparison shows that in terms of this the exponential series of the Witten genus is equivalently (by the [[splitting principle]] the $k$-fold products are left implicit):

$$
  \exp_w = z/K_w = \eta^2 \, \chi(\tilde S_+ - \tilde S_-)
  \,.
$$

Notice that, by the relation (see [here](equivariant+elliptic+cohomology#RelationToLoopGroupRepresentations)) between [[equivariant elliptic cohomology]] and [[loop group representations]], over the complex numbers $\chi(\tilde S_+ - \tilde S_-)$ may be regarded as an element of the $Spin(2k)$-[[equivariant elliptic cohomology]] of the point (at the [[Tate curve]], see at [[twisted ad-equivariant Tate K-theory]]).

### Integrality and modularity
 {#IntegralityAndModularity}

A priori, the Witten genus has [[coefficients]] the [[power series]] ring $\mathbb{Q}[ [q] ]$ over the [[rational numbers]]. But under suitable conditions ([[quantum anomaly cancellation]]) it takes values in more interesting subrings.


#### For the type II superstring
 {#ModularityForTypeIISuperstring}

The genus obtained from the [[type II superstring]] in the NS-R sector is a [[modular form]] for the [[congruence subgroup]] $\Gamma_2(2)$. ([Witten 87a, below (13)](Witten87a)) See at _[congruence subgroup -- Relation to spin structures](level+structure+on+an+elliptic+curve#RelationToSpinStructures)_ for more. 

Hence, with suitable normalization, the universal Witten-Ochanine genus takes values in the subring $MF_\bullet^{\mathbb{Q}}(\Gamma_0(2)) \hookrightarrow \mathbb{Q}[ [q] ]$ of [[modular forms]] for $\Gamma_0(2)\subset SL_2(\mathbb{Z})$ with rational coefficients ([Zagier 86, item d) on page 2](#Zagier86) based on [Chudnovsky-Chudnovsky 88](#ChudnovskyChudnovsky88)).

#### For the heterotic superstring
 {#ModularityForHeteroticString}


On manifolds with [[spin structure]] the heterotic string Witten genus has integral coeffcients, hence in the ring $\mathbb{Z}[ [ q ] ]$ ([Chudnovsky-Chudnovsky 88](#ChudnovskyChudnovsky88), [Landweber 88](#Landweber88)), see also ([Kreck-Stolz 93](#KreckStolz93), [Hovey 91](#Hovey91)). 

On manifolds with rational [[string structure]] (meaning spin structure and the [[first fractional Pontryagin class]] is at most [[torsion subgroup|torsion]]), then the Witten genus takes values in actual [[modular forms]] $MF_\bullet$ ([Zagier 86, page 6](#Zagier86)).



On manifolds with actual [[string structure]], finally, the Witten genus factors through [[topological modular forms]] ([Hopkins 94](#Hopkins94), [Ando-Hopkins-Rezk 10](#AndoHopkinsRezk)).

### Relation to Dirac operators and supersymmetric QM on loop space
 {#RelationToSuSyQMOnLoopSpace}

Originally in ([Witten 87a](#Witten87a)) the elliptic genus was derived as the [[large volume limit]] of the [[index]] of the [[supercharge]] of the [[superstring]] [[worldsheet]] [[2d SCFT]]. Here the "large volume limit" is what restricts the oscillations of the string to be "small". But then in ([Witten87b](#Witten87b)) it was observed that if this supercharge -- the [[Dirac-Ramond operator]] -- would really behave like a [[Dirac operator on smooth loop space]], then the elliptic genus would be the $S^1$-equivariant [[index of a Dirac operator]], where $S^1$ acts by rigid rotationl of the parameterization of the loops, and by analogy standard formulas for equivariant indices in K-theory would imply the localization to the tangent spaces to the space of constant loops. 

Notice that the would-be [[Dirac operator on smooth loop space]] is what would realize the [[superstring]] quantum dynamics as [[supersymmetric quantum mechanics]] on [[smooth loop space]]. This observation was the original motivation for the study of [[supersymmetric quantum mechanics]] in ([Witten 82](#Witten82), [Witten 85](#Witten85)) in the presence of a given [[Killing vector field]] (correspinding to the $S^1$-action on loop space ).

### Heterotic (twisted) Witten genus, loop group representations and parameterized WZW models
 {#TwistedWittenGenus}

If the [[superstring]] in question is the [[heterotic string]] then generally there is a "[[twisted differential string-structure|twist]]" of its [[background fields]] by a [[gauge field]], hence by a $G$-[[principal bundle]] for $G$ some simply connected [[compact Lie group]] (notably [[E8]]). The partition function in this case is a "twisted Witten genus" ([Witten 87, equations (30), (31)](#Witten87), [Brylinski 90](#Brylinski90), [KL 95](#KL95)). The modularity condition then is no longer just that the [[tangent bundle]] has [[string structure]], but that together with the gauge bundle it has [[twisted string structure]], hence [[string^c 2-group|String^c]]-structure for $c$ the $G$-[[second Chern class]] (explicitly identified as such in ([Chen-Han-Zhang 10](#ChenHanZhang10)).


An elegant formulation of twisted Witten genera (and proof of their rigidity) in terms of highest weight [[loop group representations]] is given in ([KL 95](#KL95)) along the lines of ([Brylinski 90](#Brylinski90)). In ([Distler-Sharpe 07](#DistlerSharpe07)), following suggestions around ([Ando 07](#Ando07)) this is interpreted geometrically in terms of fiberwise [[index|indices]] of [[parameterized WZW models]] [[associated bundle|associated]] to the given [[string 2-group|String]]-[[principal 2-bundle]].

What should be a concrete computation of the twisted Witten genus specifically for $G =$ [[E8]] is in ([Harris 12, section 4](#Harris12)).

### As the global character of sheaves of vertex operator algebras

For $U \subset \mathbb{C}$ an [[open subset]] of the [[complex plane]] then the space $\mathcal{D}^{ch}(U)$ of [[chiral differential operators]] on $U$ is naturally a [[super vertex operator algebra]]. For $X$ a [[complex manifold]] such that its [[first Chern class]] and [[second Chern class]] vanish over the [[rational numbers]], then this assignment gives a [[sheaf of vertex operator algebras]] $\mathcal{D}^{ch}_X(-)$ on $X$. Its [[cochain cohomology]] $H^\bullet(\mathcal{D}^{ch}_X)$ is itself a [[super vertex operator algebra]] and its super-[[Kac-Weyl character]] is proportional to the [[Witten genus]] $w(X)$ of $X$:

$$
  char H^\bullet(\mathcal{D}^{ch}_X)\propto w(X)
  \,.
$$

Physically this result is understood by observing that $\mathcal{D}^{ch}_X$is the sheaf of [[quantum observables]] of the [[topological twist|topologically twisted]] [[2d (2,0)-superconformal QFT]] (see there for more on this) of which the [[Witten genus]] is (the [[large volume limit]] of) the [[partition function]].

As highlighted in ([Cheung 10, p. 2](#Cheung10)), there is a [[resolution]]  by the [[chiral Dolbeault complex]] which gives a precise sense in which over a [[complex manifold]] the Witten genus is a stringy analog of the [[Todd genus]]. See ([Cheung 10](#Cheung10)) for a brief review, where furthermore the problem of generalizing of this construction to [[sheaves of vertex operator algebras]] over more general [[string structure]] manifolds is addressed.





### Stolz conjecture

The _[[Stolz conjecture]]_ due to ([Stolz 96](#Stolz96)) asserts that if $X$ is a [[closed manifold]] with [[String structure]] which furthermore admits a [[Riemannian metric]] with [[positive number|positive]] [[Ricci curvature]], then its Witten genus vanishes.


### Relation to BPS state counting on target space
 {#RelationToBPSStateCounting}

By [[supersymmetry]] and by the same argument that controls the expression of the [[index of a Dirac operator]] in terms of [[supersymmetric quantum mechanics]], the Witten genus may be thought of as counting those string states on which the left moving [[supercharge]] acts trivially. In terms of the [[target space]] theory these are the [[BPS states]]. (reviews include [Dijkgraaf 98](#Dijkgraaf98)).

Therefore the Witten genus may also be used as a generating function for BPS state counting. As such it has for instance been used in the microscopic explanation of [[Bekenstein-Hawking entropy]] of [[black holes]], see at _[[black holes in string theory]]_.

### Relation to Cayley plane bundles

The rational Witten genus vanishes on total spaces of [[Cayley plane]]-[[fiber bundles]], and is indeed characterized by this property ([McTague 10](#McTague10), [McTague 11](#McTague11)).


## Related concepts

* [[Witten index]]

* [[Tate K-theory]]

* [[elliptic Chern character]]

* [[M5-brane elliptic genus]]

[[!include genera and partition functions - table]]

## References
 {#References}


[[!include elliptic cohomology -- references]]









[[!redirects Witten genera]]

[[!redirects twisted Witten genus]]
[[!redirects twisted Witten genera]]