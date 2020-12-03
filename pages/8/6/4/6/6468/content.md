
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Complex geometry
+--{: .hide}
[[!include complex geometry - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Definition

A **K3 surface** is a [[Calabi-Yau variety]] of [[dimension]] $2$ (a Calabi-Yau [[algebraic surface]]/[[complex surface]]). This means that the [[canonical bundle]] $\omega_X=\wedge^2\Omega_X\simeq \mathcal{O}_X$ is trivial and $H^1(X, \mathcal{O}_X)=0$.

The term "K3" is 

> in honor of Kummer, K&#228;hler, Kodaira, and the beautiful K2 mountain in Kashmir

([Weil 79, p. 546](#Weil79))

## Examples

* A cyclic cover of $\mathbb{P}^2$ branched over a curve of degree $6$.

* A nonsingular degree $4$ hypersurface in $\mathbb{P}^3$, such as the [[Fermat hypersurface|Fermat quartic]] $\{[w,x,y,z] \in \mathbb{P}^3 | w^4 + x^4 + y^4 + z^4 = 0\}$ (in fact every K3 surface over $\mathbb{C}$ is [[diffeomorphism|diffeomorphic]] to this example).

* The [[flat orbifold]] quotient of the [[4-torus]] by the sign [[involution]] on all four canonical [[coordinates]] is the flat compact 4-dimensional orbifold known as the _Kummer surface_ $T^4 \sslash \mathbb{Z}_2$, a singular [[K3-surface]] (e.g. [Bettiol-Derdzinski-Piccione 18, 5.5](Riemannian+orbifold#BettiolDerdzinskiPiccione18))



## Properties



### Compact hyperkähler structure

Over the [[complex numbers]] [[K3 surfaces]] are all [[Kähler manifold|Kähler]], and even [[hyperkähler manifold|hyperkähler]].

The only known examples of [[compact hyperkähler manifolds]] are [[Hilbert schemes of points]] $X^{[n+1]}$ (for $n \in \mathbb{N}$) for $X$ either

1. a [[K3-surface]]

1. a [[4-torus]] (in which case the [[compact hyperkähler manifolds]] is really the [[fiber]] of $(\mathbb{T}^4)^{[n]} \to \mathbb{T}^4$)

([Beauville 83](compact+hyperkähler+manifold#Beauville83))
and two exceptional examples ([O'Grady 99](compact+hyperkähler+manifold#OGrady99), [O'Grady 03](compact+hyperkähler+manifold#OGrady03)
), see [Sawon 04, Sec. 5.3](compact+hyperkähler+manifold#Sawon04).

### Homotopy

* All K3 surfaces are [[simply connected]]. 

### Cohomology

+-- {: .num_prop #IntegralCohomology}
###### Proposition
**([[integral cohomology]] of [[K3-surface]])**

The [[integral cohomology]] of a K3-surface $X$ is 

$$
  H^n(X,\mathbb{Z})
  \;\simeq\;
  \left\{
  \array{
    \mathbb{Z} &\vert& n = 0
    \\
    0 &\vert& n = 1
    \\
    \mathbb{Z}^{22} &\vert& n = 2
    \\
    0 &\vert& n = 3
    \\
    \mathbb{Z} &\vert& n = 4
  }
  \right.
$$

=--

(e.g. [Barth-Peters-Van den Ven 84, VIII Prop. 3.2](#BarthPetersVandenVen84))

+-- {: .num_prop #BettiNumbers}
###### Proposition
**([[Betti numbers]] of a [[K3-surface]])**


The [[Hodge diamond]] is completely determined (even in positive [[characteristic]]) and hence the  [[Hodge-de Rham spectral sequence]] degenerates at $E_1$. This also implies that the [[Betti numbers]] are completely determined as $1, 0, 22, 0, 1$:

$$
  \array{
    && h^{0,0}
    \\
    & h^{1,0} && h^{0,1}
    \\
    h^{2,0} & & h^{1,1} & & h^{0,2}
    \\
    & h^{2,1} & & h^{1,2}
    \\
    && h^{2,2}
  }
  \;\;\;=\;\;\;
  \array{
    && 1
    \\
    & 0 && 0
    \\
    1 & & 20 & & 1
    \\
    & 0 & & 0
    \\
    && 
    1
  }
$$

=--

(e.g. [Barth-Peters-Van den Ven 84, VIII Prop. 3.3](#BarthPetersVandenVen84))

\linebreak

### SU-Bordism
 {#SUBordism}

+-- {: .num_prop #K3SurfaceSpansSUBordismRingInDegree4}  
###### Proposition
**([[K3-surface]] spans [[SU-bordism ring]] in degree 4)**

The canonical degree-4 generator $y_4 \in \Omega^{SU}_4$ in the [[SU-bordism ring]] ([this Prop.](MSU#SUBordismRingAwayFromTwo)) is represented by minus the class of any (non-[[torus]]) [[K3-surface]]:

$$
  \Omega^{SU}_4 
    \;\simeq\; 
  \mathbb{Z}\big[ \tfrac{1}{2}\big]\big\langle -[K3] \big\rangle
  \,.
$$

=--

([LLP 17, Lemma 1.5, Example 3.1](MSU#LLP17), [CLP 19, Theorem 13.5a](MSU#CLP19), see at _[[Calabi-Yau manifolds in SU-bordism theory]]_)

\linebreak



### Characteristic classes
  {#CharacteristicClasses}

We discuss some [[characteristic classes]] of (the [[tangent bundle]] of) [[K3]], and their evaluation on (the [[fundamental class]] of) $K3$ (i.e. their [[integration]] over $K3$).

#### Of $K3$

+-- {: .num_prop #EulerCharacteristicOfK3}
###### Proposition
**([[Euler characteristic]] of [[K3]])**

The [[Euler characteristic]] of [[K3]] is 24:

$$
  \chi_4[K3] \;=\; 24
  \,.
$$

=--

+-- {: .num_prop #FirstChernClassOfK3}
###### Proposition
**([[first Chern class]] of [[K3]])**

The [[first Chern class]] of [[K3]] vanishes:

$$
  c_1(K3) \;=\; 0
  \,.
$$

=--


+-- {: .num_prop #SecondChernClassOfK3}
###### Proposition
**([[second Chern class]] of [[K3]])**

The [[second Chern class]] of [[K3]] evaluates to 24:

$$
  c_2[K3] \;=\; 24
  \,.
$$

=--

+-- {: .proof}
###### Proof

For every [[closed manifold|closed]] [[complex manifold]] the evaluation of the top degree [[Chern class]] equals the [[Euler characteristic]]. Hence the statement follows from Prop. \ref{EulerCharacteristicOfK3}.

=--


+-- {: .num_prop #FirstPontryaginClassOfK3}
###### Proposition
**([[first Chern class]] of [[K3]])**

The [[first Pontryagin class]] of [[K3]] evaluates to 48:

$$
  p_1[K3] \;=\; -48
  \,.
$$

=--

(see also e.g. [Duff-Liu-Minasian 95 (5.10)](I8#DuffLiuMinasian95))

+-- {: .proof}
###### Proof

For a [[complex manifold]] the [[first Pontryagin class]] is the following [[polynomial]] in the [[first Chern class]] and the [[second Chern class]].
By Prop. \ref{FirstChernClassOfK3} the first Chern class vanishes,
and by Prop. \ref{SecondChernClassOfK3} the second Chern class evaluates to 24:


$$
  \begin{aligned}
    p_1[K3]
      & =\;
    \underset{= 0}{\underbrace{c_1 \cup c_1}}[K3] 
    - 2 
    \underset{24}{\underbrace{c_2[K3]}}
    \\
    & = - 48
  \end{aligned}
  \,.
$$

=--

#### Of $K3 \times K3$

Now consider the [[Cartesian product|Cartesian]] [[product space]] $K3 \times K3$.

See also at _[[C-field tadpole cancellation]]_ the section _[Integrality on $K3 \times K3$](C-field+tadpole+cancellation#IntegralityOnK3TimesK3)_.


+-- {: .num_prop #EulerCharacteristicOfK3TimesK3}
###### Proposition
**([[Euler characteristic]] of [[K3]]$\times$[[K3]])**

The [[Euler characteristic]] of $K3 \times K3$ is $24^2$:

$$
  \chi_8[K3\times K3] \;=\; 24^2
  \,.
$$

=--

+-- {: .proof}
###### Proof

By the [Whitney sum formula for the Euler class](Euler%20class#EulerClassOfWhitneySumIsCupProductOfEulerClasses) we have $\chi_8[K3 \times K3] = (\chi_4[K3])^2$. Hence the statement follows by Prop. \ref{EulerCharacteristicOfK3}.

=--

+-- {: .num_prop #FirstPontryaginClassOfK3TimesK3}
###### Proposition
**([[first Pontryagin class]] of [[K3]]$\times$[[K3]])**

The [[first Pontryagin class]] evaluated on $K3 \times K3$ is:

$$
  p_1[K3 \times K3]
  \;=\;
  - 2 \times 48
$$

=--

+-- {: .proof}
###### Proof

By the general formula for [[Pontryagin classes]] of [[product spaces]] we have

$$
  \begin{aligned}
    p_1(K3 \times K3)
    & =\;
    p_0(K3) \smile p_1(K3)
    +
    p_1(K3) \smile p_0(K3)
    \\
    & = 
    2 p_1(K3)
  \end{aligned}
$$

With this, the statement follows by Prop. \ref{FirstPontryaginClassOfK3}.

=--




#### Of $K3 \times X^4$


Now consider the [[Cartesian product|Cartesian]] [[product space]] $K3 \times X^4$ of [[K3]] with some [[4-manifold]].

+-- {: .num_prop #EulerCharacteristicOfK3TimesK3}
###### Proposition
**([[Euler characteristic]] of [[K3]]$\times X^4$)**

The [[Euler characteristic]] of $K3 \times K3$ is $24$ times the Euler characteristic of $X^4$:

$$
  \chi_8[K3\times X^4] \;=\; 24 \cdot \chi_4[X^4]
  \,.
$$

=--

+-- {: .proof}
###### Proof

By the [Whitney sum formula for the Euler class](Euler%20class#EulerClassOfWhitneySumIsCupProductOfEulerClasses) we have $\chi_8[K3 \times X^4] = \chi_4[K3] \cdot \chi_4[X^4]$. Hence the statement follows by Prop. \ref{EulerCharacteristicOfK3}.

=--

+-- {: .num_prop #FirstPontryaginClassOfK3TimesK3}
###### Proposition
**([[first Pontryagin class]] of [[K3]]$\times X^4$)**

The [[first Pontryagin class]] evaluated on $K3 \times X^4$ is:

$$
  p_1[K3 \times X^4]
  \;=\;
  p_1[X^4] - 48
$$

=--

+-- {: .proof}
###### Proof

By the general formula for [[Pontryagin classes]] of [[product spaces]] we have

$$
  \begin{aligned}
    p_1[K3 \times X^4]
    & =\;
    p_0[K3] \smile p_1[X^4]
    +
    p_1[K3] \smile p_0[X^4]
    \\
    & = 
    p_1[X^4] + p_1[K3]
  \end{aligned}
$$

With this, the statement follows by Prop. \ref{FirstPontryaginClassOfK3}.

=--




### Moduli of higher line bundles and deformation theory
 {#ModuliOfHigherLineBundles}

In [[positive number|positive]] [[characteristic]] $p$:

The [[Néron-Severi group]] of a K3 is a [[free abelian group]]

The [[formal Brauer group]] is

* either the formal [[additive group]], in which case it has [[height of a formal group|height]] $h = \infty$, by definition;

* or its [[height of a formal group|height]] is $1 \leq h \leq 10$, and every value may occur

([Artin 74](#Artin74)), see also ([Artin-Mazur 77, p. 5 (of 46)](#ArtinMazur77))

[[!include moduli of higher lines -- table]]

### Relation to third stably framed bordism group

The [[third stable homotopy group of spheres]] (the third [[stable stem]]) is the [[cyclic group]] of [[order of a group|order]] 24:

$$
  \array{
    \pi_3^s &\simeq& \mathbb{Z}/24
    \\
    [h_{\mathbb{H}}] &\leftrightarrow& [1]
  }
$$

where the generator $[1] \in \mathbb{Z}/24$ is represented by the [[quaternionic Hopf fibration]] $S^7 \overset{h_{\mathbb{H}}}{\longrightarrow} S^4$.

Under the [[Pontrjagin-Thom isomorphism]], identifying the [[stable homotopy groups of spheres]] with the [[bordism ring]] $\Omega^{fr}_\bullet$ of [[stable framing|stably framed]] manifolds (see at _[[MFr]]_), this generator is represented by the [[3-sphere]] (with its left-invariant framing induced from the identification with the [[Lie group]] [[SU(2)]] $\simeq$ [[Sp(1)]] )


$$
  \array{
    \pi_3^s & \simeq & \Omega_3^{fr} 
    \\
    [h_{\mathbb{H}}] & \leftrightarrow & [S^3]
    \,.
  }
$$

Moreover, the relation $2 4 [S^3] \,\simeq\, 0$ is represented by the [[bordism]] which is the [[complement]] of 24 [[open balls]] inside [[generalized the|the]] [[K3]]-manifold ([MO:a/44885/381](https://mathoverflow.net/a/44885/381), [MO:a/218053/381](https://mathoverflow.net/a/218053/381)).


### As a fiber space in string compactifications

See 

* [[duality between heterotic and type II string theory]]

* [[F-theory on K3]]

* [[M-theory on Sp(1)-manifolds]]

## Related concepts

* [[formal Brauer group]]

* [[K3-cohomology]]

* [[F-theory]], [[F-theory on K3]]

* [[elliptic fibration]]


## References

### General

Original sources include

* {#Artin74} [[Michael Artin]], _Supersingular K3 Surfaces_, Annal. Sc. d, l'&#201;c Norm. Sup.  4e  s&#233;ries, T. 7, fasc.  4, 1974, pp. 543-568

* {#Weil79} [[Andre Weil]], Final report on contract AF 18 (603)-57. In Scientific works. Collected papers. Vol. II (1951-1964). 1979.

Textbook accounts include

* {#BarthPetersVandenVen84} W. Barth, C. Peters, A. Van den Ven, chapter VII of _Compact complex surfaces_, Springer 1984

Lecture notes include

* [[Daniel Huybrechts]], _Lectures on K3-surfaces_ ([pdf](http://www.math.uni-bonn.de/people/huybrech/K3Global.pdf))

* [[Claire Voisin]], _<a href="http://www.ams.org/mathscinet-getitem?mr=2487743">Geometry of the Moduli Space of K3 surfaces</a>_ 

* [[David Morrison]], _[The geometry of K3 surfaces](http://www.cgtp.duke.edu/ITP99/morrison/cortona.pdf)_ Lecture notes (1988)

* Viacheslav Nikulin, _Elliptic fibrations on K3 surfaces_ ([arXiv:1010.3904](http://arxiv.org/abs/1010.3904))

Discussion of the [[deformation theory]] of K3-surfaces (of their [[Picard schemes]]) is (see also at _[[Artin-Mazur formal group]]_) in 

* {#ArtinMazur77} [[Michael Artin]], [[Barry Mazur]], _Formal Groups Arising from Algebraic Varieties_, Annales scientifiques de l'&#201;cole Normale Sup&#233;rieure, S&#233;r. 4, 10 no. 1 (1977), p. 87-131  [numdam](http://www.numdam.org/item?id=ASENS_1977_4_10_1_87_0), [MR56:15663](http://www.ams.org/mathscinet-getitem?mr=56:15663)

Systematic construction of [[Ricci tensor|Ricci flat]] [[Riemannian metrics]] on [[K3]] [[orbifolds]]:

* [[Shamit Kachru]], [[Arnav Tripathy]], [[Max Zimet]], _K3 metrics_ ([arXiv:2006.02435](https://arxiv.org/abs/2006.02435))

* [[Arnav Tripathy]], [[Max Zimet]], _A plethora of K3 metrics_ ([arXiv:2010.12581](https://arxiv.org/abs/2010.12581))


### In string theory
  {#InStringTheory}

In [[string theory]], the [[KK-compactification]] of [[type IIA string theory]]/[[M-theory]]/[[F-theory]] on K3-[[fibers]] is supposed to exhibit te [[duality between M/F-theory and heterotic string theory]], originally due to

* [[Chris Hull]], [[Paul Townsend]], section 6 of _Unity of Superstring Dualities_, Nucl.Phys.B438:109-137,1995 ([arXiv:hep-th/9410167](http://arxiv.org/abs/hep-th/9410167))

* {#Witten95} [[Edward Witten]], section 4 of _[[String Theory Dynamics In Various Dimensions]]_, Nucl.Phys.B443:85-126,1995 ([arXiv:hep-th/9503124](http://arxiv.org/abs/hep-th/9503124))

Review includes

* {#Aspinwall96} [[Paul Aspinwall]], _K3 Surfaces and String Duality_, in  [[Shing-Tung Yau]] (ed.): _Differential geometry inspired by string theory_ 1-95 ([arXiv:9611137](https://arxiv.org/abs/hep-th/9611137), [spire:426102](http://inspirehep.net/record/426102))

Further discussion includes

* [[Paul Aspinwall]], [[David Morrison]], _String Theory on K3 Surfaces_, in [[Brian Greene]], [[Shing-Tung Yau]] (eds.), _Mirror Symmetry II_, International Press, Cambridge, 1997, pp. 703-716 ([arXiv:hep-th/9404151](https://arxiv.org/abs/hep-th/9404151))

* [[Paul Aspinwall]], _Enhanced Gauge Symmetries and K3 Surfaces_, Phys.Lett. B357 (1995) 329-334 ([arXiv:hep-th/9507012](http://arxiv.org/abs/hep-th/9507012))

Specifically in relation to [[orbifold]] [[string theory]]:

* {#Wendland01} [[Katrin Wendland]], _Orbifold Constructions of K3: A Link between Conformal Field Theory and Geometry_, in _[[Orbifolds in Mathematics and Physics]]_ ([arXiv:hep-th/0112006](https://arxiv.org/abs/hep-th/0112006))

Specifically in relation to the putative [[K-theory]]-classification of [[D-brane charge]]:

* {#GarciaUranga05} Inaki Garcia-Etxebarria, [[Angel Uranga]], _From F/M-theory to K-theory and back_, JHEP 0602:008,2006 ([arXiv:hep-th/0510073](https://arxiv.org/abs/hep-th/0510073))


Specifically in [[M-theory on G2-manifolds]]:

* {#AtiyahWitten01} [[Michael Atiyah]], [[Edward Witten]] section 6.4 of _$M$-Theory dynamics on a manifold of $G_2$-holonomy_, Adv. Theor. Math. Phys. 6 (2001) ([arXiv:hep-th/0107177](http://arxiv.org/abs/hep-th/0107177))

Specifically in relation to [[Moonshine]]:

* [[Miranda Cheng]], Sarah M. Harrison, Roberto Volpato, Max Zimet, _K3 String Theory, Lattices and Moonshine_ ([arXiv:1612.04404](https://arxiv.org/abs/1612.04404))

Specifically in relation to [[little string theory]]:

* [[Shamit Kachru]], Arnav Tripathy, Max Zimet, _K3 metrics from little string theory_ ([arXiv:1810.10540](https://arxiv.org/abs/1810.10540))
 

[[!redirects K3 surfaces]]

[[!redirects K3]]

[[!redirects K3-surface]]
[[!redirects K3-surfaces]]

[[!redirects Kummer surface]]
[[!redirects Kummer surfaces]]

[[!redirects generalized Kummer surface]]
[[!redirects generalized Kummer surfaces]]

