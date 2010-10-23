[[!redirects n-symplectic manifold]]

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### $\infty$-Lie theory
+--{: .hide}
[[!include infinity-Lie theory - contents]]
=--
=--
=--

#Contents#
* automatic table of contents goes here
{:toc}

## Idea

A [[Lie n-algebroid]] is _symplectic_ if it is equipped with a non-degenerate binary [[invariant polynomial]]. This generalizes the notion of a [[symplectic form]] on a [[symplectic manifold]], to which it reduces for $n = 0$.

## Definition

A **symplectic Lie $n$-algebroid** is a pair

$$
  (\mathfrak{a}, \langle -,- \rangle)
$$

consisting of

* a [[Lie n-algebroid]] $\mathfrak{a}$;

* a binary [[invariant polynomial]] $\langle- , - \rangle$ of degree $(n+2)$

  (an closed element in the shifted elements of the [[Weil algebra]] $W(\mathfrak{a})$)

  which is non-degenerate.  

The **Poisson tensor** of a symplect Lie $n$-algebroid is the cocycle $\nu \in CE(\mathfrak{a})$ in [[∞-Lie algebroid cohomology]] that this invariant polynomial transgresses to.

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

For a [[Poisson manifold]] $X$ with Poisson bivector $\pi \in \Gamma(T X) \wedge \Gamma(T X)$ the [[Chevalley-Eilenberg algebra]] $CE(\mathfrak{a})$ of the corresponding [[Poisson Lie algebroid]] 

$$
  \mathfrak{a} := \mathfrak{P}(X,\pi)
$$

is that of multi-vector fields on $X$, equipped with the differential $d_{CE(\mathfrak{a})} = [\pi, -]_{Sch}$ given by the [[Schouten bracket]].

If we work locally in coordinates  then $CE(\mathfrak{a})$ is generated from degree 0 elements $x^i$ and degree 1 elements $\partial_i$. The differential is

$$
  d_{CE(\mathfrak{a})} = [\pi, -]_{Sch}
  \,.
$$

The Poisson tensor is $\nu := \pi = \pi^{i j} \partial_i \wedge \partial_j$ and that this is a [[∞-Lie algebra cohomology|Lie algebroid cocycle]] is the fact that

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


## Relation to multisymplectic geometry

There is also the closely related notion  of [[multisymplectic geometry]]. See 

* [[John Baez]], [[Chris Rogers]], _Categorified Symplectic Geometry and the String Lie 2-Algebra_, ([arXiv](http://arxiv.org/abs/0901.4721))

for some relations of this to the above situation for $n = 2$. Essentially multisymplectic geometry studies the higher $n$-ary brackets induced from the binary graded symplectic form discussed here. The relation between these two pictures is the same as that between as studied in the context of [[hemistrict Lie 2-algebra]]s.

An article with more details on this:

* [[Chris Rogers]], _Courant algebroids from categorified symplectic geometry_ ([pdf](http://math.ucr.edu/~chris/2plectic-algebroid_DRAFT.pdf)).


## References

The notion originates somewhere in the school of [[Alan Weinstein]]'s school of [[higher category theory|higher categorial]] [[symplectic geometry]]. The first published appearance of the notion at least for $0 \leq n \leq 3$ is

* [[Dmitry Roytenberg]], _Courant algebroids, derived brackets and even symplectic supermanifolds_ PhD thesis ([arXiv](http://arxiv.org/abs/math/9910078))

A good writeup of this material is in

* [[Dmitry Roytenberg]], _On the structure of graded symplectic supermanifolds and Courant algebroids_ ([arXiv](http://arxiv.org/abs/math/0203110))

The idea for all $n$ was then sketched, together with many other ideas about [[L-infinity algebroid]]s in the article with the nice title

* [[Pavol ?evera]], _Some title containing the words "homotopy" and "symplectic", e.g. this one_ ([arXiv](http://arxiv.org/abs/math/0105080))

What we call $n$-symplectic manifold here is called $\Sigma_n$-manifold there.

> [[Urs Schreiber]]: I find $\Sigma_n$ too undescriptive. But logically I should then be speaking of _$n$-Poisson manifolds_ so that for $n=1$ we get the ordinary version, not for $n=0$. But I find _symplectic_ still much nicer descriptive than "Poisson", so the above choice of terminology follows aesthetics a little bit more than established terminology. But only slightly. Only by a difference of 1.

> _Toby_:  What if you changed the numbering by $1$?  Must your $n$ match the $n$ in $\Sigma_n$?

> Urs: I thought of that, but then I found it weird to have a numbering system that claims that ordinary Poisson geometry is a "2-" and hence supposed a categorified thing. In $\Sigma_n$-terminology the $n$ is indeed the degree of the Lie n-algebroid. That seems worthwhile to keep.


**Warning** This article here uses the term "$n$-symplectic" in a related but not identical sense to the one used here:

* M. de Leon, D. Martin de Diego, M. Salgado, S. Vilari&#241;o, _K-symplectic formalism on Lie algebroids_ ([arXiv](http://lanl.arxiv.org/abs/0905.4585))

A discussion of aspects of how [[multisymplectic geometry]] related to $n$-symplectic manifolds is in 

* [[Chris Rogers]], _Courant algebroids from categorified symplectic geometry_ ([pdf](http://math.ucr.edu/~chris/2plectic-algebroid_DRAFT.pdf))
<a href="http://front.math.ucdavis.edu/1001.0040">arXiv:1001.0040v1 [math-ph]</a>


