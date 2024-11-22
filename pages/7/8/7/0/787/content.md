
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### $\infty$-Lie theory
+--{: .hide}
[[!include infinity-Lie theory - contents]]
=--
#### Symplectic geometry
+--{: .hide}
[[!include symplectic geometry - contents]]
=--
=--
=--



#Contents#
* table of contents
{:toc}


## Idea

A **Courant algebroid**  -- or better: **Courant Lie 2-algebroid** -- (named after [[Theodore Courant]]) is precisely a [[symplectic Lie n-algebroid|symplectic Lie 2-algebroid]] ([Roytenberg](#RoytenbergStructure)):

it is a [[L-infinity algebroid|Lie 2-algebroid]] $\mathfrak{P}$ whose [[Chevalley-Eilenberg algebra]] $CE(\mathfrak{P})$ is equipped with the structure of a [[Poisson n-algebra|Poisson 3-algebra]] whose Poisson bracket

$$
  \{-,-\} : CE(\mathfrak{P})\otimes CE(\mathfrak{P})
  \to 
  CE(\mathfrak{P})
$$

of degree -2 is non-degenerate. 

Therefore the [[differential]] $d_{CE(\mathfrak{P})}$ on $CE(\mathfrak{P})$ has a [[Hamiltonian]] with respect to this bracket in that there is an element $\Theta \in CE(\mathfrak{P})$ such that

$$
  d_{CE(\mathfrak{P})} = \{\Theta, -\}
  \,.
$$

## History

The concept of Courant algebroids was originally introduced by [[Irene Dorfman]] and [[Ted Courant]] to study [[geometric quantization]] in the presence of constraints. Later it was considered by Liu, [[Alan Weinstein]] and [[Ping Xu]] in the study of [[double Lie algebroids]].

In these parts of the literature Courant algebroids are considered in the form of [[Lie algebroid]]s with relaxed axioms on the bracket. Even of this type there are two different definitions:

* in one there is a skew-symmetric bracket which fails to satisfy a Jacobi identity by a coherent term -- this is the Courant bracket definition proper;

* in the other there is a bracket which satisfies a Jacobi identity but is skew-symmetric only up to a correction term -- this is the Dorfman version.

So there are several different ways to present the structure encoded in a Courant algebroid. The picture that seems to be emerging is that the _true_ meaning of the notoin of Courant algebroids is given by the notion of [[n-symplectic manifold|2-symplectic manifold]]s.

Moreover, the way [[Lie algebroid]]s may be expressed in terms of [[Lie-Rinehart algebra]]s, Courant algebroids yield [[Courant-Dorfman algebra]]s.


***

(... need to say more about the way the Courant Lie algebroid is obtained from a Lie bialgebroid by derived brackets ...)

***

## Examples

### Lie algebras of compact type

A Courant Lie 2-algebroid over the point is precisely an ordinary [[Lie algebra]] $\mathfrak{g}$ that is equipped with a quadratic and non-degenerate [[invariant polynomial]].

### Standard Courant algebroid and $U(1)$-gerbes

The [[standard Courant algebroid]] of a [[manifold]] $X$ is the one which 

* as a [[vector bundle]] with extra structure is $E = T X\oplus T^* X$, the fiberwise direct sum of the [[tangent bundle]] and the cotangent bundle; with 

  * bilinear form 

    $$
      \langle X + \xi , Y +\eta \rangle = \eta(X) + \xi(Y)
    $$

  for $X,Y \in \Gamma(T X)$ and $\xi, \eta \in \Gamma(T^* X)$

  * brackets

    $$
      [X + \xi, Y + \eta] = [X,Y] + \mathcal{L}_X \eta 
      - \mathcal{L}_Y \xi + \frac{1}{2} d (\eta(X) - \xi(Y))
    $$

    where $\mathcal{L}_X \eta = \{d,\iota_X\} \eta$ denotes the [[Lie derivative]] of the 1-form $\eta$ by the vector field $X$.

* as a [[dg-manifold]] is $T^*[2] T[1] X$, the shifted cotangent bundle of the [[shifted tangent bundle]],

  where the [[differential]] is on each local [[coordinate patch]] $\mathbb{R}^n \simeq U \subset X$ with coordinates $\{x^i\}$ in degree 0, $\{d x^i\}$ and $\{\theta_i\}$ in degree 1 and $\{p_i\}$ in degree 2 given by

  $$
    \begin{aligned}
      d_C &= d_{dR} + p_i \frac{\partial}{\partial \theta_i}
      \\
      &= dx^i \frac{\partial}{\partial x^i }
       + p_i \frac{\partial}{\partial \theta_i}
    \end{aligned}
    \,.
  $$

Such a standard Courant algebroid may be understood as the higher analog of the  [[Atiyah Lie algebroid]] of a line bundle. See below in _[Relation to Atiyah groupoids](#RelationToAtiyahGroupoids)_.

## Properties

### Generalized complex geometry

The study of Courant algebroids is to a large extent known as [[generalized complex geometry]], where the Courant algebroid appears as the [[generalized tangent bundle]].

### Chern-Simons element and Courant $\sigma$-model

As every [[symplectic Lie n-algebroid]] the defining [[invariant polynomial]] on a Courant Lie 2-algebroid transgresses to a cocycle in [[∞-Lie algebroid cohomology]] and this transgression is witnessed by a [[Chern-Simons element]]. The [[schreiber:∞-Chern-Simons theory]] induced by this element is the [[Courant sigma-model]].

### Lagrangian submanifolds and Dirac structures

The [[Lagrangian dg-submanifolds]] of a Courant Lie 2-algebroid corespond to its [[Dirac structures]]. 


### Relation to Atiyah Lie 2-algebroid and quantomorphism 2-group
 {#RelationToAtiyahGroupoids}

We discuss how the following tower of notions works

| [[circle n-bundle]] with $(n-1)$-form connection | [[Lie n-algebra]] of [[group of bisections|of bisections]] of Atiyah Lie n-group |
|--|--|
|  [[circle bundle]] |  [[Lie algebra]] of [[sections]] of [[Atiyah Lie algebroid]] |
|  [[circle 2-bundle]] with 1-form connection | [[Lie 2-algebra]] of [[sections]] of [[Courant Lie 2-algebroid]]

For $n,k \in \mathbb{N}$ and $k \leq n$ write

$$
  \mathbf{B}^n U(1)_{conn^k}
  \coloneqq
  DK\left[
    U(1) \stackrel{d log}{\to}
    \Omega^1
    \stackrel{d}{\to}
    \cdots
    \stackrel{d}{\to} 
     \Omega^{k-1}
    \stackrel{d}{\to} \Omega^k
     \to 
     \underbrace{
     0
     \to 0
     \to \cdots
     \to 0
     }_{n-k}
  \right]
$$

for the [[smooth ∞-groupoid]] which is presented under the [[Dold-Kan correspondence]] by the [[sheaf]] of [[chain complexes]], as indicated (see also at _[differential cohomology diagram -- Examples -- Deligne coefficients](differential+cohomology+diagram#DeligneCoefficients)_). This is such that for $k = n$ we have the [[Deligne complex]], representing the [[moduli ∞-stack]] of [[circle n-bundles with connection]]

$$
  \mathbf{B}^n U(1)_{conn^n} \simeq \mathbf{B}^n U(1)_{conn}
$$

and for $k = 0$ we have the moduli $\infty$-stack for plain [[circle n-group]] [[principal ∞-bundles]]

$$
  \mathbf{B}^n U(1)_{conn^0} \simeq \mathbf{B}^n U(1)
  \,.
$$

For $k_2 \lt k_1$ there are evident truncation maps

$$
  \mathbf{B}^n U(1)_{conn^{k_1}}
  \to 
  \mathbf{B}^n U(1)_{conn^{k_2}}
  \,.
$$

Now for $X \in $ [[SmthMfd]] $\hookrightarrow$ [[Smooth∞Grpd]] a [[smooth manifold]], a map

$$
  \nabla \;\colon\; X \to \mathbf{B}^n U(1)_{conn}
$$

modulates a [[circle n-bundle with connection]] ([[bundle gerbe|bundle (n-1)-gerbe]]), which we may think of as a _[[prequantum circle n-bundle]]_. Regarding this as an [[object]] in the [[slice (∞,1)-topos]] $\mathbf{H}_{/\mathbf{B}^n U(1)}$ this has an [[automorphism ∞-group]]. The [[concretification]] of this (...) is the [[quantomorphism n-group]] $QuantMorph(\nabla)$.

$$
  \mathbf{QuantMorph}(\nabla)
  \coloneqq
  conc\mathbf{Aut}(\nabla)
  =
  \left\{
    \array{
      X && \underoverset{\simeq}{\phi}{\to} && X
      \\
      & {}_{\mathllap{\nabla}}\searrow &\swArrow_{\simeq}& \swarrow_{\mathrlap{\nabla}}
      \\
      && \mathbf{B}^n U(1)_{conn}
    }
  \right\}
  \,.
$$

But we can also first forget the $n$-form pieces of the prequantum $n$-bundle away and consider

$$
  \nabla_{n-1} 
    \;\colon\;
   X 
    \stackrel{\nabla}{\to}
   \mathbf{B}^n U(1)_{conn}
   \simeq 
   \mathbf{B}^n U(1)_{conn^n}
   \to
   \mathbf{B}^n U(1)_{conn^{n-1}} 
  \,.
$$

For $n = 2$ this is sometimes known in the literature as a "bundle gerbe with connective structure but without curving".

The concretified [[automorphism ∞-group]] of that truncated connection is the [[n-group]] of [[group of bisections|of bisection]] of the [[Atiyah n-groupoid]]

$$
  conc \mathbf{Aut}(\nabla_{n-1}) \in Grp(Smooth \infty Grpd)
  \,.
$$

For $n = 1$ this is the [[group of bisections]] of the [[Atiyah Lie groupoid]] of the underlying [[circle principal bundle]] $\nabla_0 \colon X \to \mathbf{B} U(1)$. Hence its [[Lie differentiation]] is the [[Lie algebra]] of sections of the corresponding [[Atiyah Lie algebroid]].

For $n = 2$ the [[Lie differentiation]] of this [[Lie 2-group]] is the [[Lie 2-algebra]] of sections of the corresponding Courant Lie 2-algebroid. With a little bit of translation, this is what is shown in ([Collier](#Collier)).

Finally notice that the forgetful map $\mathbf{B}^n U(1)_{conn} \to \mathbf{B}^n U(1)_{conn^{n-1}}$ induces an [[homomorphism]] of [[∞-groups]]

$$
  conc \mathbf{Aut}(\nabla) \to conc \mathbf{Aut}(\nabla_{n-1})
$$

hence an embedding of the [[quantomorphism n-group]] into the $n$-[[group of bisections]] of the Atiyah n-groupoid. For $n = 2$ and after [[Lie differentiation]], this is an embedding of the [[Poisson Lie 2-algebra]] into the sections of the Courant Lie 2-algebroid. This embedding had been observed in ([Rogers](#Rogers)).

## Related concepts

[[!include higher Atiyah groupoid - table]]

* [[string algebroid]]

* [[symplectic Lie n-algebroid]]

  * [[symplectic manifold]]

  * [[Poisson Lie algebroid]]
 
  * **Courant algebroid**

* [[Dirac structure]]

* [[Courant sigma-model]]

[[!include infinity-CS theory for binary non-degenerate invariant polynomial - table]]


## References

The original references in order of appearance are

* [[Pavol Ševera]], _Letters to A. Weinstein_ ([web](http://sophia.dtp.fmph.uniba.sk/~severa/letters/), [arXiv:1707.00265](https://arxiv.org/abs/1707.00265))

* [[Dmitry Roytenberg]], [[Alan Weinstein]], _Courant algebroids and strongly homotopy Lie algebras_, Lett. Math. Physics __46__(1):81-93, 1998.

* [[Dmitry Roytenberg]], _Courant algebroids, derived brackets and even symplectic supermanifolds_  PhD
thesis, University of California, Berkeley, 1999.
([math.DG/9910078](http://arxiv.org/abs/math.DG/9910078))

* [[Pavol Ševera]], _Some title containing the words "homotopy" and "symplectic", e.g. this one_, In Travaux
math&#233;matiques. Fasc. XVI, chapter Trav. Math., XVI, pp. 121-137. Univ. Luxembourg, 2005.

* [[Dmitry Roytenberg]], _On the structure of graded symplectic supermanifolds and Courant algebroids_, pp. 169--185. in Contemporary Mathematics __315__, _Quantization, Poisson brackets and beyond_ (Manchester, 2001), Theodore Voronov, editor, Amer. Math. Soc. 2002.
([arXiv:math/0203110](http://arxiv.org/abs/math/0203110))
{#RoytenbergStructure}

* [[Dmitry Roytenberg]], _Quasi-Lie bialgebroids and twisted Poisson manifolds_ , Letters in Mathematical
Physics, 61(2):123-137 (2002) ([arXiv:math/0112152](http://arxiv.org/abs/math/0112152))

Another useful summary of the theory of Courant algebroids is in  of

* [[Marco Gualtieri]], [section 3](http://arxiv.org/PS_cache/math/pdf/0401/0401221v1.pdf#page=19) of: _Generalized complex geometry_ ([arXiv:math/0401221](http://arxiv.org/abs/math/0401221))

On the [[morphisms]] between Courant algebroids:

* [[Jan Vysoky]], _Hitchhiker's Guide to Courant Algebroid Relations_ ([arXiv:1910.05347](https://arxiv.org/abs/1910.05347))


A discussion of Courant algebroids with an eye towards the relation of the [[standard Courant algebroid]] to [[bundle gerbes]] is 

* [[Paul Bressler]], Alexander Chervov, _Courant algebroids_ ([hep-th/0212195](http://arxiv.org/abs/hep-th/0212195))

The identification of the Lie 2-algebra of sctions of a Courant Lie 2-algebroid associated with a [[circle 2-bundle with connection]] as its Lie algebra of automorphisms after forgetting the "curving" is in

* [[Braxton Collier]], _Infinitesimal Symmetries of Dixmier-Douady Gerbes_ ([arXiv:1108.1525](http://arxiv.org/abs/1108.1525))
 {#Collier}

The embedding of the [[Poisson Lie 2-algebra]] of a given [[2-plectic geometry]] into the [[Lie 2-algebra]] of sections of the Courant Lie 2-algebroid of the corresponding [[prequantum 2-bundle]] is observed in 

* [[Chris Rogers]], _Courant algebroids from categorified symplectic geometry_, ([arXiv:1001.0040](http://arxiv.org/abs/1001.0040))
 {#Rogers}

This is developed further in 

* [[Domenico Fiorenza]], [[Chris Rogers]], [[Urs Schreiber]], _[[schreiber:L-∞ algebras of local observables from higher prequantum bundles]]_ ([arXiv:1304.6292](http://arxiv.org/abs/1304.6292))

See also 

* Wikipedia, _[Courant algebroid](http://en.wikipedia.org/wiki/Courant_algebroid)_


The relation between the two different Lie-algebroid-like  definition of Courant algebroids, one with skew, the other with non-skew brackets inspired on the level of [[L-infinity algebra|Lie 2-algebras]] the treatment

* [[Dmitry Roytenberg]], _On weak Lie 2-algebras_ ([arXiv/0712.3461](http://arxiv.org/abs/0712.3461))

* [[Chris Rogers]], _2-plectic geometry, Courant algebroids, and categorified prequantization_, ([arxiv:1009.2975](http://arxiv.org/abs/1009.2975))

A proposal for a higher analog of the [[standard Courant algebroid]] with the [[generalized tangent bundle]] $T X \oplus T^* X$ replaced by $T X \oplus \wedge^n T^* X$ -- for a notion of standard [[higher Courant Lie algebroid]] -- is discussed in

* [[Marco Zambon]], _$L_\infty$-algebras and higher analogues of Dirac structures and Courant algebroids_, J. Symplectic Geometry, J. Sympl. Geom. __10__:4 (2012) 563--599 [arXiv:1003.1004](https://arxiv.org/abs/1003.1004) [Zbl:1260.53134](https://zbmath.org/?q=an:1260.53134) [doi](https://doi.org/10.4310/JSG.2012.v10.n4.a4)

The relation to [[schreiber:∞-Chern-Simons theory]] is discussed in 

* [[Domenico Fiorenza]], [[Chris Rogers]], [[Urs Schreiber]], _[[schreiber:Higher Chern-Weil Derivation of AKSZ Sigma-Models]]_

Discussion of [[Riemannian geometry]] on Courant algebroids and relation to [[supergravity]] [[equations of motion]] is in 

* [[Branislav Jurco]], [[Jan Vysoky]], _Courant Algebroid Connections and String Effective Actions_, Proceedings of Tohoku Forum for Creativity, Special volume: Noncommutative Geometry and Physics IV ([arXiv:1612.01540](https://arxiv.org/abs/1612.01540))

See also

* Xu Xiaomeng, _Twisted Courant algebroids and coisotropic Cartan geometries_ ([arXiv:1206.2282](http://arxiv.org/abs/1206.2282))


[[!redirects Courant Lie algebroid]]
[[!redirects Courant Lie algebroids]]

[[!redirects Courant algebroids]]

[[!redirects Courant Lie 2-algebroid]]
[[!redirects Courant Lie 2-algebroids]]

[[!redirects Courant bracket]]
[[!redirects Courant brackets]]