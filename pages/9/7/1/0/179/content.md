
> under construction

<div class="rightHandSide toc">
[[!include infinity-Lie theory - contents]]
</div>


#Contents#
* automatic table of contents goes here
{:toc}

## Idea

**$L_\infty$-algebroids** or **Lie $\infty$-algebroids** are to [[Lie ∞-groupoids]] as [[Lie algebras]] are to [[Lie groups]]. Hence $L_\infty$-algebroids are a [[horizontal categorification]] and [[vertical categorification]] of Lie algebras: they encompass $L_\infty$-[[L-∞-algebras|algebras]] as well as [[Lie algebroids]].

A Lie $\infty$-algebroid is a [[complex]] $g$ of [[modules]] over a [[ring]] $A_0$, satisfying some (complicated) conditions. It turns out that it is easier to formulate these conditions in terms of the [[Chevalley?Eilenberg algebra]] $CE(g)$ of $g$. This is a certain type of graded super commutative algebra constructed from $g$.


## Definition

Let $dgAlg_{\mathbb{R}}^{op}$ be the [[opposite category]] of [[dg-algebra]]s equipped with the standard [[model structure on dg-algebras]]. An **$\infty$-Lie algebroid** is effectively a (fibrant) object in this category.

See also [[rational homotopy theory in an (∞,1)-topos]].


...

> ...this here needs polishing...

### Definition in terms of differential algebra


+-- {: .un_defn}
###### Definition (Lie $\infty$ Algebroid)

A Lie $\infty$-algebroid $\mathfrak{a}$ of finite type over a [[smooth manifold]] $X$ is the following data:

* A commutative algebra $A = \mathfrak{a}_0$, thought of as the ring of functions on a manifold $X$.

* a non-positively graded complex $\mathfrak{a}$ of (finitely generated projective) $A$-modules

$$
\dots \to \mathfrak{a}_{n}\to \mathfrak{a}_{n-1} \to \dots \to \mathfrak{a}_0.
$$

* A degree 1 derivation $Q$ on the [[Chevalley-Eilenberg algebra]] $CE(\mathfrak{a})=\wedge^\bullet_{A} \mathfrak{a}^* = \wedge^\bullet \mathfrak{a}^*$ of $\mathfrak{a}^*$, such that $Q^2=0$.
=--

The Chevalley-Eilenberg algebra $CE(\mathfrak{a})$ of a Lie $\infty$-algebroid is a commutative [[semifree dga]], and any such (of non negative degree) is of the form $CE(\mathfrak{a})$ for some Lie $\infty$ algebroid.

A morphism of Lie $\infty$ algebroids $g\to h$ is a linear map $\phi\colon CE(\mathfrak{h})\to CE(\mathfrak{g})$ of the  Chevalley-Eilenberg algebras in the opposite direction, respecting the grading and the differentials. 

Notice that the first few terms of $\wedge^\bullet g^*$ in degree 0, 1 and 2, respectively, are
$$
  \wedge^\bullet g^*
  =
  \mathfrak{a}_0 \oplus \mathfrak{a}_1^* \oplus  (\mathfrak{a}_1^* \wedge_A \mathfrak{a}_1 \oplus \mathfrak{a}_2) \oplus \cdots 
  \,.
$$

+-- {: .un_example}
###### Example
Take $\mathfrak{a} = \Gamma(T X)$ to be the $C^\infty(X)$-module of [[tangent vector fields]] on $X$, then $\wedge^\bullet_{C^\infty(X)} \mathfrak{a}^* = \wedge^\bullet_{C^\infty(X)} \Omega^1(X) = \Omega^\bullet(X)$. 
=--

+-- {: .un_remark}
###### Remark
There is plenty of room to fuss about the grading conventions. 
=--


### The Chevalley-Eilenberg functor on Lie $\infty$-algebroids

A Lie $\infty$-algebroid $g$ is a complex of $A_0$-modules, so corresponds to a bunch of [[vector bundles]] $E_i\to X_0$ over the underlying manifold $X_0$, where $g_i=\Gamma(E_i)$, and the differential of the complex gives fibrations 

$$
\dots \to E_{-n}\to E_{-n+1}\to \dots \to E_0\to X_0
$$

So one can think of a Lie $\infty$-algebroid as a rather intricate classical geometric structure: vector bundles with [[extra stuff]]. These form a category. But taking the Chevalley--Ehresmann algebra gives a functor

$$
  Lie \infty Algebroids \stackrel{CE(-)}{\to} sDGCAs
$$

from the category of Lie $\infty$-algebroids to the category of semi free Differential Graded Commutative algebras (sDGCAs).

Each SDGCA is the algebras of functions on a supermanifold, more precisely an [[NQ-supermanifold]]. So the CE functor gives a remarkable connection between classical geometry and super geometry.


## Remarks

* The definition of a Lie $\infty$-structure in terms of a dual differential graded-commutative algebra is the higher graded version of the definition of Lie algebras in terms of [Lie coalgebras](http://en.wikipedia.org/wiki/Lie_coalgebra).


## Special Cases

* a Lie $\infty$-algebroid over a point, $X = pt$ is an **$L_\infty$-[[L-infinity-algebra|algebra]]**;

* an Lie $\infty$-algebroid $g$ with generators for $CE(g)$ concentrated in the first $n$ degrees is a **Lie $n$-algebroid**;

* an Lie $\infty$-algebroid the differential of whose CE algebra is "co-binary", i.e. $d : \mathfrak{g}^* \to g^* \oplus g^* \wedge g^*$, is **strict**.

So in particular

* a Lie 1-algebroid is a **[[Lie algebroid]]**;

* a Lie 1-algebroid over the point is a **Lie algebra**;

* a Lie $n$-algebroid over a point is a **[[Lie n-algebra]]**.

* a _[[BRST-complex]]_ is the [[Chevalley-Eilenberg algebra]]
  of an action-$\infty$-Lie algebroid of the 
  [[action]] of an $L_\infty$-algebra, see [[Lie ∞-algebroid representation]];

  more generally, the complexes appearing in [[BV-BRST formalism]] are 
  derived $\infty$-Lie algebroids, whose Chevalley-Eilenberg algebra may have generators in negative degree.

* a [[Courant algebroid]] is a certain Lie 2-algebroid.

* more  generally an [[n-symplectic manifold]] is a Lie $n$-algebroid.

* Standard examples of [[exterior differential system]]s are [[Chevalley?Eilenberg algebras]] of $L_\infty$-algebroids.


## References

The term "Lie $\infty$-algebroid" or "$L_\infty$-algebroid" as such is not as yet established in the literature, as most authors working with these objects think of them entirely in terms of [[NQ-supermanifolds]] and either ignore the relation to [[Lie theory]] or take it more or less for granted. 

Possibly the first explicit appearance of the idea of $\infty$-Lie algebroids recognized in their full [[Lie theory|Lie theoretic]] meaning is

* Pavol &Scaron;evera, _Some title containing the words "homotopy" and "symplectic", e.g. this one_ ([arXiv](http://arxiv.org/abs/math.SG/0105080))

which uses "[[NQ-supermanifolds]]". Of course, as this article also points out, in hindsight one finds that much of this is already implicit in the much older theory of [[Sullivan model|Sullivan models]] in [[rational homotopy theory]], which is concerned with modelling _spaces_ by qDGCAs. That these spaces can be regarded as [[∞-groupoids]] and as [[Lie ∞-groupoids]] in particular is clear in hindsight, but was possibly first explicitly realized in the above reference. See also [[Lie integration]].

[[!redirects L-infinity-algebroid]]
[[!redirects L-infinity algebroid]]
[[!redirects L-infinity Lie algebroid]]

[[!redirects L-∞-algebroid]]
[[!redirects L-∞ algebroid]]
[[!redirects L-∞ Lie algebroid]]


[[!redirects Lie-∞-algebroid]]
[[!redirects Lie-∞-algebroids]]
[[!redirects Lie-∞ algebroid]]
[[!redirects Lie-∞ algebroids]]
[[!redirects Lie ∞-algebroid]]
[[!redirects Lie ∞-algebroids]]
[[!redirects L-infinity-algebroids]]
[[!redirects L-infinity algebroids]]
[[!redirects L-infinity Lie algebroids]]

[[!redirects ∞-Lie algebroid]]
[[!redirects ∞-Lie algebroids]]