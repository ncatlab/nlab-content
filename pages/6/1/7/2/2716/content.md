
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

A [[Lie n-algebroid]] is _symplectic_ if it is equipped with a non-degenerate binary [[invariant polynomial]]. This generalizes the notion of a [[symplectic form]] on a [[symplectic manifold]], to which it reduces for $n = 0$.

## Definition

+-- {: .num_defn}
###### Definition


A **symplectic Lie $n$-algebroid** is a pair

$$
  (\mathfrak{a}, \langle -,- \rangle)
$$

consisting of

* a [[Lie n-algebroid]] $\mathfrak{a}$;

* a binary [[invariant polynomial]] $\langle- , - \rangle$ of degree $(n+2)$

  (a closed element in the shifted elements of the [[Weil algebra]] $W(\mathfrak{a})$)

  which is non-degenerate.  

=--


## Properties



The [[Chern-Simons element]] that witnesses this transgression is the Lagrangian of the corresponding [[AKSZ theory]] [[sigma-model]] with $\mathfrak{a}$ as its target space and the invariant polynomial $\langle -,- \rangle$ as the ([[curvature]] of) its background [[gauge field]].

## Examples

### $n=0$: symplectic manifold

A 0-Lie algebroid is just a [[smooth manifold]] $X$.

Its [[Chevalley-Eilenberg algebra]] is the algebra of smooth functions on $X$

$$
  CE(X) = C^\infty(X)
  \,.
$$

The [[Weil algebra]] of $X$ is

$$
  W(X) = \Omega^\bullet(X)
$$

the [[de Rham complex|de Rham algebra]] of $X$. A degree 2-[[invariant polynomial]] on $X$ is therefore a non-degenerate closed [[differential form|2-form]] $\omega \in \Omega^2(X)$, a [[symplectic manifold|symplectic 2-form]].

+-- {: .standout}

A [[symplectic manifold]], being a pair

$$
  (X,\;\; \omega)
$$

consisting of a  [[smooth manifold]] $X$ and a symplectic 2-form $\omega$, is a symplectic Lie 0-algebroid.

=--

### $n=1$: Poisson manifold 
 {#PoissonManifolds}

For a [[Poisson manifold]] $X$ with Poisson bivector $\pi \in \Gamma(T X) \wedge \Gamma(T X)$ the [[Chevalley-Eilenberg algebra]] $CE(\mathfrak{a})$ of the corresponding [[Poisson Lie algebroid]] 

$$
  \mathfrak{a} \coloneqq \mathfrak{P}(X,\pi)
$$

is that of multi-vector fields on $X$, equipped with the differential $d_{CE(\mathfrak{a})} = [\pi, -]_{Sch}$ given by the [[Schouten bracket]].

If we work locally in coordinates  then $CE(\mathfrak{a})$ is generated from degree 0 elements $x^i$ and degree 1 elements $\partial_i$. The differential is

$$
  d_{CE(\mathfrak{a})} = [\pi, -]_{Sch}
  \,.
$$

The Poisson tensor is $\nu \coloneqq \pi = \pi^{i j} \partial_i \wedge \partial_j$ and that this is a [[∞-Lie algebra cohomology|Lie algebroid cocycle]] is the fact that

$$
  d_{CE(\mathfrak{a})} \pi = [\pi,\pi]_{Sch} = 0
  \,.
$$


By definition the [[Weil algebra]] $W(\mathfrak{a})$ is generated from the $x^i$, the $\partial_i$ and their shifted partners $\mathbf{d}x^i$ and $\mathbf{d}\partial_i$. The differential here is

$$
  d_{W(\mathfrak{a})} = [\pi , - ] + \mathbf{d}
  \,.
$$

+-- {: .un_prop}
###### Proposition

The [[invariant polynomial]] $\omega$ that is in transgression with the cocycle  $\nu = \pi$ is

$$
  \omega = (\mathbf{d} x^i) \wedge (\mathbf{d} \partial_i)
  \;\;\;
  \in inv(\mathfrak{a})
  \,.
$$

=--

+-- {: .proof}
###### Proof


One checks directly that the element

$$
  cs_\omega = 
  \pi^{i j} \partial_i \wedge \partial_j
  +
  x^i \wedge \mathbf{d} \partial_i
$$

is a Chern-Simons transgression element for $\nu$ and $\omega$,

i.e. $d_{W(\mathfrak{a})} cs(\omega) = \omega$. The restriction of $cs_\omega$ to $CE(\mathfrak{a})$ is evidently the Poisson tensor $\pi$.

=--

More details on this at [[Chern-Simons element]].

+-- {: .standout}

For a [[Poisson manifold]] $X$ with Poisson tensor $\pi = \pi^{i j} \partial_i \wedge \partial_j$, the pair 

$$
  (\mathfrak{P}(X,\pi), \;\;\;
\omega = (\mathbf{d} x^i) \wedge (\mathbf{d} \partial_i))
$$

consisting of the [[Poisson Lie algebroid]] $\mathfrak{P}(X,\pi)$ and of the [[invariant polynomial]] $\omega$ that is in transgression with its canonical 2-cocycle $\nu = \pi$ (the Poisson tensor) is a symplectic [[Lie algebroid]].

=--


### $n=2$: Courant algebroid

A $2$-symplectic manifold encodes and is encoded by the structure of a [[Courant algebroid]].

A Courant 2algebroid over the point if given by a [[semisimple Lie algebra]] with the symplectic form being the [[Killing form]]. The coresponding Poisson tensor is the canonical 3-cocycle $\langle -, [-,-] \rangle$ on a semisimple Lie algebra. The extension classified by this is the [[string Lie 2-algebra]].

## Relation to other concepts

### To $\infty$-Chern-Simons theory

Since the symplectic form on a symplectic Lie $n$-Algebroid may be understood [[Lie theory|Lie theoretically]] as an [[invariant polynomial]] on an [[L-∞ algebroid]], every symplectic Lie $n$-algebroid serves as a [[target space]] for an [[schreiber:∞-Chern-Simons theory]]: this is [[AKSZ theory]]. 

We have

* for $n = 1$ the [[Poisson sigma-model]];
* for $n = 2$ the [[Courant sigma model]]
* and so on.

### To multisymplectic geometry

There is also the closely related notion  of [[multisymplectic geometry]]. See 

* [[John Baez]], [[Chris Rogers]], _Categorified Symplectic Geometry and the String Lie 2-Algebra_, ([arXiv](http://arxiv.org/abs/0901.4721))

for some relations of this to the above situation for $n = 2$. Essentially multisymplectic geometry studies the higher $n$-ary brackets induced from the binary graded symplectic form discussed here. The relation between these two pictures is the same as that between as studied in the context of [[hemistrict Lie 2-algebra]]s.

An article with more details on this:

* [[Chris Rogers]], _Courant algebroids from categorified symplectic geometry_ ([pdf](http://math.ucr.edu/~chris/2plectic-algebroid_DRAFT.pdf)).


## Related concepts

* [[L-∞ algebroid]]

* [[symplectic groupoid]]

[[!include infinity-CS theory for binary non-degenerate invariant polynomial - table]]

## References

The notion originates somewhere in the school of [[Alan Weinstein]]'s school of [[higher category theory|higher categorial]] [[symplectic geometry]]. The first published appearance of the notion at least for $0 \leq n \leq 3$ is

* [[Dmitry Roytenberg]], _Courant algebroids, derived brackets and even symplectic supermanifolds_, PhD thesis &lbrack;[arXiv:9910078](http://arxiv.org/abs/math/9910078)&rbrack;

A good writeup of this material is in

* [[Dmitry Roytenberg]], _On the structure of graded symplectic supermanifolds and Courant algebroids_, in: [[Theodore Voronov]] (ed.),  _Quantization, Poisson Brackets and Beyond_, Contemp. Math. **315**, Amer. Math. Soc. (2002) &lbrack;[arXiv:0203110](http://arxiv.org/abs/math/0203110), [ISBN:978-0-8218-7905-4](https://bookstore.ams.org/conm-315)&rbrack;

The idea for all $n$ was then sketched, together with many other ideas about [[L-infinity algebroid]]s in the article with the nice title

* [[Pavol Ševera]], _Some title containing the words "homotopy" and "symplectic", e.g. this one_ ([arXiv](http://arxiv.org/abs/math/0105080))

What we call $n$-symplectic manifold here is called $\Sigma_n$-manifold there.

**Warning** This article here uses the term "$n$-symplectic" in a related but not identical sense to the one used here:

* M. de Leon, D. Martin de Diego, M. Salgado, S. Vilari&#241;o, _K-symplectic formalism on Lie algebroids_ ([arXiv](http://lanl.arxiv.org/abs/0905.4585))

A discussion of aspects of how [[multisymplectic geometry]] related to $n$-symplectic manifolds is in 

* [[Chris Rogers]], _Courant algebroids from categorified symplectic geometry_ ([pdf](http://math.ucr.edu/~chris/2plectic-algebroid_DRAFT.pdf))
<a href="http://front.math.ucdavis.edu/1001.0040">arXiv:1001.0040v1 [math-ph]</a>

* [[Chris Rogers]], _Higher symplectic geometry_ PhD thesis (2011) ([arXiv:1106.4068](http://arxiv.org/abs/1106.4068))

A discussion of symplectic Lie n-algebroids from an [[infinity-Lie theory]] perspective as discussed here is in 

* [[Domenico Fiorenza]], [[Chris Rogers]], [[Urs Schreiber]], _[[schreiber:AKSZ Sigma-Models in Higher Chern-Weil Theory]]_, Int. J. Geom. Methods Mod. Phys. 10 (2013) 1250078 ([arXiv:1108.4378](http://arxiv.org/abs/1108.4378))

The [[H-cohomology]] of graded symplectic forms is considered in

* {#Severa05} [[Pavol Severa]], p. 1 of _On the origin of the BV operator on odd symplectic supermanifolds_, Lett Math Phys (2006) 78: 55. ([arXiv:0506331](https://arxiv.org/abs/math/0506331))


[[!redirects symplectic Lie n-algebroids]]

[[!redirects n-symplectic manifold]]