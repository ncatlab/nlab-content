
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Knot theory
+--{: .hide}
[[!include knot theory - contents]]
=--
#### Arithmetic geometry
+--{: .hide}
[[!include arithmetic geometry - contents]]
=--
=--
=--

## Contents
* table of contents
{:toc}

## Idea

**Arithmetic topology** is a theory describing some surprising [[analogies]] between [[low-dimensional topology|3-dimensional topology]] and [[number theory]] ([[arithmetic]]), where [[knots]] embedded in a [[3-manifold]] behave like [[prime ideals]] in a [[ring of algebraic integers]]. See also at _[Spec(Z) -- As a 3d space containing knots](Spec%28Z%29#As3dSpaceContainingKnots)_.

Under this analogy, the [[3-sphere]], $S^3$ corresponds to the ring of [[rational numbers]] $\mathbb{Q}$, or rather (the closure of) $spec(\mathcal{O}_{\mathbb{Q}})$ (i.e., $spec(\mathbb{Z})$), since the 3-sphere has no non-trivial ([[branched cover|unbranched]]) covers while $\mathbb{Q}$ has no non-trivial [[unramified extensions]]. The [[linking number]] between two embedded knots in the 3-sphere then corresponds to the [[Legendre symbol]] between two primes in the ordinary integers.

The so-called _M^2KR dictionary_ (Mazur-Morishita-Kapranov-Reznikov) relates terms from each side of the analogy (see sec 2.2 of [Sikora](#Sikora)).

## The dictionary

### Version of Mazur-Morishita-Kapranov-Reznikov (M^2KR)
 {#VersionOfM^2KR}
 
1. [[closed manifold|Closed]], [[orientation|orientable]], [[connected topological space|connected]] [[3-manifolds]] correspond to (the closure of) schemes $Spec \mathcal{O}_K$ for number fields $K$.
1. Links correspond to ideals in $\mathcal{O}_K$ and knots correspond to prime ideals (tame in both cases). Knots can be represented by immersions of $S^1$ into $M$, and prime ideals in $\mathcal{O}_K$ can be identified with closed immersions $Spec \mathbb{F} \to Spec \mathcal{O}_K$, where $\mathbb{F}$'s are finite fields. Each link decomposes uniquely as a union of knots and each ideal decomposes uniquely as a product of primes.
1. An algebraic integer corresponds to an embedded surface (possibly with boundary), and the operation $a \to (a)$ corresponds to taking its boundary. Closed embedded surfaces correspond to units in $\mathcal{O}_K$. Ideals of the form $(a)$ represent the identity in $Cl(K)$, and the links of the form $\partial S$ represent the identity in $H_1(M,\mathbb{Z})$.
1. $Cl(K)$ corresponds to the torsion component of first integral homology.
The free component of $H_1(M,\mathbb{Z})$ corresponds to the group of units
in $\mathcal{O}_K$ after removing the torsion (roots of unity).
1. Finite extensions of number fields correspond to finite branched coverings.
1. $S^3$ is supposed to correspond to $\mathbb{Q}$. Notice that $S^3$ has no nontrivial unbranched covers, and similarly $\mathbb{Q}$ has no nontrivial unramified extensions.
1. A Galois extension $L/K$ with Galois group $G$ induces a morphism
$Spec \mathcal{O}_L \to (Spec \mathcal{O}_L)/G = Spec \mathcal{O}_K$. Such maps correspond to the quotient maps $M \to M/G$ induced by orientation preserving actions of finite groups $G$ on 3-manifolds $M$. One can show that $M/G$ is always a 3-manifold and that the maps $M \to M/G$ are branched
coverings.
1. Let $q = p^n$. Consider the cyclotomic extension $\mathbb{Q}(\zeta_q)$. It is ramified only at $p$. These correspond to cyclic branched covers of knots in $S^3$. The union of these as $q$ ranges over all powers of $p$ should correspond to the universal abelian cover of $S^3 \setminus K$. There is a natural action of $\mathbb{Z}$ on the first homology group of the infinite cyclic cover of the knot complement corresponding to the natural action of the $p$-adic integers on the $p$-torsion of $Cl(\mathbb{Q}(\zeta_{p^{\infty}}))$. This concerns the [[Alexander polynomial]] of the knot and [[Iwasawa theory]]. ([Sikora, pp. 5-6](#Sikora), [Koberda08, pp. 32-33](#Koberda08))

Note: Regarding (4), some have argued that $Cl(K)$ should correspond to the full first integral homology group, (see, e.g., [Goundaroulis & Kontogeorgis](#Goundaroulis)).

The correspondence between $\pi^{et}_1(\mathbb{Z} -\{p\})$ and $\pi_1(S^3 \setminus K)$ can be developed to relate the Legendre symbol for two primes to the linking number of two knots, and further to the R&#233;dei symbol for three primes and Milner's triple linking number. Thus we can find a 'Borromean link' of primes, such as $(13, 61, 397)$, where each pair is unlinked. 

#### Disanalogies

1. The algebraic translation of the Poincar&#233; Conjecture is false. $\mathbb{Q}$ is not the only number field with no unramified extensions. Nevertheless, $\hat{H}^i(Spec \mathcal{O}_K, \mathbb{Z}/n\mathbb{Z}) = \hat{H}^i(Spec \mathbb{Z}, \mathbb{Z}/n\mathbb{Z}) (i \in \mathbb{Z}, n \geq 2)$ if and only if $\mathcal{O}_K = \mathbb{Z}$.
1. Let $M_1 \to M$ be a covering of 3-manifolds. A knot $K$ in $M$ does not necessarily lift to a knot in $M_1$, while every prime ideal $p \triangleleft \mathcal{O}_K$ gives rise to an ideal $p \mathcal{O}_L$, where $L/K$ is a Galois number field extension. ([Goundaroulis & Kontogeorgis](#Goundaroulis)).

### Version of Deninger

Similar to M^2KR, but with the introduction of a 2-dimensional foliation on the 3-manifold and a flow such that finite primes $p$ correspond to periodic orbits of length $log N p$ and the infinite primes correspond to the fixed points of the flow ([Deninger02](#Deninger02)). (See also the work of [Baptiste Morin](http://www.math.uni-muenster.de/reine/u/baptiste.morin/) on the Weil-&#233;tale topos.)

### Version of Reznikov
 {#ReznikovVariant}

Reznikov has modified the dictionary ([Reznikov 00, section 12](#Reznikov00)) so as to associate a number field with what he calls a $3\frac{1}{2}$-manifold, that is a closed three-manifold $M$, bounding a four-manifold $N$, such that the map of fundamental groups $\pi_1(M) \to \pi_1(N)$ is surjective.

##Explanations for the analogy

[[Barry Mazur]] observed that for an affine spectrum $X = Spec(D)$ of the ring of integers $D$ in a number field, the groups $H^n_{et}(X, \mathbb{G}_{m, X})$ vanish (up to 2-torsion) for $n \gt 3$, and is equal to $\mathbb{Q}/\mathbb{Z}$ for $n = 3$, where $\mathbb{G}_{m, X}$ is the &#233;tale sheaf on $X$ defined by associating to a connected finite &#233;tale covering $Spec(B) \to X$ the multiplicative group $\mathbb{G}_{m, X}(Y) = B^{\times}$.

Also, there is a non-degenerate pairing for any constructible abelian sheaf $M$,

$$
H^r_{et}(X,M^{'}) \times Ext^{3-r}_X(M,\mathbb{G}_{m, X}) \to H^3_{et}(X,\mathbb{G}_{m, X})\simeq \mathbb{Q}/\mathbb{Z},
$$

where $M^{'} = Hom(M, \mathbb{G}_{m, X})$. This resembles Poincar&#233; duality for 3-manifolds.

[[Minhyong Kim]] argues that the normal bundle of an embedding of a circle corresponding to a prime in $Spec(\mathbb{Z})$ is 2-dimensional ([Kim](#Kim)).

[[Baptiste Morin]] claims to provide a unified treatment via equivariant etale cohomology ([Morin06](#Morin06)).

## Related concepts

* [[Alexander polynomial]]

* [[function field analogy]]

* The [[virtually fibered conjecture]] says that every [[closed manifold|closed]], [[irreducible manifold|irreducible]], [[atoroidal 3-manifold|atoroidal]] [[3-manifold]] with infinite [[fundamental group]] has a [[finite cover]] which is a [[surface]] [[fiber bundle]] over the [[circle]].

* [[arithmetic Chern-Simons theory]]

##References
* {#Deninger02} [[Christopher Deninger]], _A note on arithmetic topology and dynamical systems_, ([arxiv:0204274](http://arxiv.org/abs/math/0204274))

* {#Goundaroulis} Dimoklis Goundaroulis, Aristides Kontogeorgis, _On the Principal Ideal Theorem in Arithmetic Topology_, ([talk](http://users.uoa.gr/~kontogar/talks/GkountPSATHA.pdf), [paper](http://arxiv.org/abs/0705.3937))

* {#Kim} Minhyong Kim, [note](http://minhyongkim.files.wordpress.com/2013/05/baez13-12.pdf)

* {#Koberda08} Thomas Koberda, _Class Field Theory and the MKR Dictionary
for Knots_, ([pdf](http://users.math.yale.edu/users/koberda/minorthesis.pdf))

* {#Morin06} [[Baptiste Morin]], _Applications of an Equivariant Etale Cohomology to Arithmetic Topology_, [arxiv:0602064](http://arxiv.org/abs/math/0602064) and  Utilisation d'une cohomologie étale équivariante en topologie arithmétique, Compositio Math. 144 (2008), no. 1, 32-60.

* {#Morishita09} Masanori Morishita, _Analogies between Knots and Primes, 3-Manifolds and Number Rings_, ([arxiv:0904.3399](http://arxiv.org/abs/0904.3399))

* {#Reznikov00} Alexander Reznikov, _Embedded incompressible surfaces and homology of ramified coverings of three-manifolds_, Selecta Math. 6(2000), 1&#8211;39

* {#Sikora} Adam Sikora, _Analogies between group actions on 3-manifolds and number fields_, ([arxiv](http://arxiv.org/abs/math/0107210))


* {#KohnoMorishita06} [[Toshitake Kohno]], [[Masanori Morishita]] (eds.), _Primes and Knots_, Contemporary Mathematics, AMS 2006 ([conm:416](http://www.ams.org/bookstore-getitem/item=CONM-416))


* {#Morishita12} [[Masanori Morishita]], _Knots and Primes: An Introduction to Arithmetic Topology_, 2012, Springer, ([web](https://books.google.co.uk/books?id=DOnkGOTnI78C&pg=PA156#v=onepage&q&f=false))

* Claudio Gómez-Gonzáles, [[Jesse Wolfson]], _Problems in Arithmetic Topology_ ([arXiv:2012.15434](https://arxiv.org/abs/2012.15434))




[[!redirects MKR dictionary]]
[[!redirects MKR analogy]]