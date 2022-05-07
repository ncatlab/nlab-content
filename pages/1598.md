
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Group Theory
+-- {: .hide}
[[!include group theory - contents]]
=--
#### Differential geometry
+--{: .hide}
[[!include synthetic differential geometry - contents]]
=--
#### $\infty$-Lie theory
+--{: .hide}
[[!include infinity-Lie theory - contents]]
=--
=--
=--



# Contents
* table of contents
{:toc}

## Idea

A **Lie group** is a [[group]] with [[smooth structure]]. Lie groups form a category, [[LieGrp]].


## Definition

+-- {: .num_defn}
###### Definition

A **Lie group** is a [[smooth manifold]] whose [[forgetful functor|underlying]] [[set]] of [[elements]] is equipped with the [[structure]] of a [[group]] such that the [[magma|group multiplication]] and [[inverse]]-assigning [[functions]] are [[smooth functions]].  

In other words, a Lie group is a [[group object]] [[internalization|internal to]] the [[category]] [[SmthMfd]] of [[smooth manifolds]].

=--

Usually the [[smooth manifold]] is assumed to be defined over the [[real numbers]] and to be of [[finite number|finite]] [[dimension]] (f.d.), but extensions of the definition to some other [[ground fields]]  or to -[[infinite-dimensional manifolds]] are also relevant, sometimes under other names (such as [[Fréchet Lie group]] when the underlying manifold is an infinite-dimensional [[Fréchet manifold]]). 

A real Lie group is called a _[[compact Lie group]]_ (or _connected_, _simply connected_ Lie group, etc) if its underlying [[topological space]] is [[compact space|compact]] (or [[connected space|connected]], [[simply connected space|simply connected]], etc). 

Every connected finite dimensional real Lie group is [[homeomorphism|homeomorphic]] to a [[product]] of a [[compact Lie group]] (its [[maximal compact subgroup]]) and a [[Euclidean space]]. 

Every [[abelian group|abelian]] connected compact finite dimensional real Lie group is a [[torus]] (a product of [[circles]] $T^n = S^1\times S^1 \times \ldots \times S^1$).

There is an [[infinitesimal space|infinitesimal]] version of a Lie group, a so-called [[local Lie group]], where the multiplication and the inverse are only partially defined, namely if the arguments of these operations are in a sufficiently small neighborhood of identity. There is a natural equivalence of local Lie groups by means of agreeing (topologically and algebraically) on a smaller neighborhood of the identity. The category of local Lie groups is equivalent to the category of connected and simply connected Lie groups. 

The first order [[infinitesimal object|infinitesimal]] approximation to a Lie group is its [[Lie algebra]].




## Properties

### Lie's three theorems

[[Sophus Lie]] has proved several theorems -- [[Lie's three theorems]] -- on the relationship between [[Lie algebra]]s and Lie groups. What is called [[Lie's third theorem]] is about the [[equivalence of categories]] of f.d. real Lie algebras and local Lie groups. [[Élie Cartan]] has extended this to a global integrability theorem called the Cartan-Lie theorem, nowadays after Serre also called Lie's third theorem.


### Classification

+-- {: .num_prop}
###### Prposition

Every connected finite-dimensional real Lie group is [[homeomorphism|homeomorphic]] to a [[product]] of a compact Lie group and a [[Cartesian space|Euclidean space]]. Every abelian connected compact f.d. real Lie group is a [[torus]] (a product of circles $T^n = S^1\times S^1 \times \ldots \times S^1$).

=--

The [[simple Lie group]]s have a classification into infinite series of 

* [[classical Lie group]]s

and a finite snumber o

* [[exceptional Lie group]]s


### Different Lie group structures on a group

For $G$ a bare [[group]] (without smooth structure) there may be more than one way to equip it with the [[stuff, structure, property|structure]] of a Lie group.

+-- {: .num_example}
###### Example

As bare [[abelian group]]s, the  [[Cartesian space]]s $\mathbb{R}^n$ are, for all $n$, [[vector space]]s over the [[rational number]]s $\mathbb{Q}$ whose [[dimension]] is the [[cardinality]] of the [[continuum]], $2^{\aleph_0}$.

Therefore these are all [[isomorphic]] as bare group. But equipped with their canonical Lie group structure (as in the [Examples](#Examples)) they are of course not isomorphic.

=--

### Different topologies on a Lie group

* Linus Kramer, _The topology of a simple Lie group is essentially unique_, ([arXiv](http://arxiv.org/abs/1009.5457))

> Abstract: We study locally compact group topologies on simple Lie groups. We show that the Lie group topology on such a group $S$ is very rigid: every 'abstract' isomorphism between $S$ and a locally compact and $\sigma$-compact group $\Gamma$ is automatically a homeomorphism, provided that $S$ is absolutely simple. If $S$ is complex, then non-continuous field automorphisms of the complex numbers have to be considered, but that is all. 

### Which topological groups admit Lie group structure?

* _[[Hilbert's fifth problem]]_

### Homotopy groups

List of [[homotopy groups]] of the manifolds underlying the classical [[Lie groups]] are for instance in ([Abanov 09](#Abanov09)).




## Applications

### In differential geometry

A central concept of [[differential geometry]] is that of a $G$-[[principal bundle]] $P \to X$ over a [[smooth manifold]] $X$ for $G$ a Lie group.

### In gauge theory

In the [[physics]] of [[gauge field]]s -- [[gauge theory]] -- Lie groups appear as local [[gauge group]]s parameterizing [[gauge transformation]]s: notably the [[Yang-Mills field]] is modeled by a $G$-[[principal bundle]] with [[connection on a bundle|connection]] for some Lie group $G$. For models that describe experimental observations the group $G$ in question is a quotient of a product of [[special unitary group]]s and the [[circle group]]. For details see [[standard model of particle physics]]


## In higher category theory

The notion of [[group]] generalizes in [[higher category theory]] to that of [[2-group]], ... [[∞-group]].

Accordingly, so does the notion of Lie group generalize to [[Lie 2-group]], ... [[∞-Lie group]]. For details see [[∞-Lie groupoid]].

## Examples 
 {#Examples}

### Basic examples

* The [[real line]] $\mathbb{R}$ with its standard [[smooth structure]] and the group operation being addition is a Lie group. So is every [[Cartesian space]] $\mathbb{R}^n$ with the componentwise addition of real numbers.

* The [[quotient]] of $\mathbb{R}$ by the subgroup of [[integer]]s $\mathbb{Z} \hookrightarrow \mathbb{R}$ is the [[circle group]] $S^1 = \mathbb{R}/\mathbb{Z}$. The quotient $\mathbb{R}^n/\mathbb{Z}^n$ is the $n$-[[dimension|dimensional]] [[torus]].

* The [[automorphism group]] of any Lie group is canonically itself a Lie group: the _[[automorphism Lie group]]_.

### Classical Lie groups

The [[classical Lie groups]] include

* the [[general linear group]] $GL(n)$

* the [[orthogonal group]] $O(n)$ and [[special orthogonal group]] $SO(n)$;

* the [[unitary group]] $U(n)$ and [[special unitary group]] $SU(n)$;

* the [[symplectic group]] $Sp(2n)$.

### Exceptional Lie groups

The [[exceptional Lie groups]] incude

* [[G2]], [[F4]], [[E6]], [[E7]] [[E8]],

### Infinite-dimensional examples

* [[stable unitary group]]

* [[loop group]]

* [[diffeomorphism group]]

  * [[symplectomorphism group]], [[quantomorphism group]]


## Related concepts

* [[semisimple Lie group]], [[simple Lie group]], [[exceptional Lie group]]

* [[real form]]

* [[compact Lie group]], [[maximal compact subgroup]]

* [[maximal torus]]

* [[rank of a Lie group]]

* [[conjugacy class]], [[Cartan-Dirac structure on a Lie group]]

* [[Weyl group]]

* [[Inönü-Wigner group contraction]]

* [[infinite-dimensional Lie group]]

* [[orbit method]]

* [[Hamiltonian dynamics on Lie groups]]

* [[complex Lie group]]

* [[Poisson Lie group]]

* [[invariant differential form]], [[Maurer-Cartan form]]

[[!include infinitesimal and local - table]]


## References

### General

* {#Bredon72} [[Glen Bredon]], Section 0.5 of: _[[Introduction to compact transformation groups]]_, Academic Press  1972 ([ISBN 9780080873596](https://www.elsevier.com/books/introduction-to-compact-transformation-groups/bredon/978-0-12-128850-1), [pdf](http://www.indiana.edu/~jfdavis/seminar/Bredon,Introduction_to_Compact_Transformation_Groups.pdf))

  > (in the context of [[topological groups]])


* {#Onishchik93} A. L. Onishchik (ed.) _Lie Groups and Lie Algebras_

  * *I.* A. L. Onishchik, E. B.  Vinberg, _Foundations of Lie Theory_,

  * *II.* V. V. Gorbatsevich, A. L. Onishchik, _Lie Transformation Groups_ 

  Encyclopaedia of Mathematical Sciences, Volume 20, Springer 1993


* [[Hans Duistermaat]], J. A. C. Kolk, _Lie groups_, 2000

* {#HilgertNeeb12} Joachim Hilgert, [[Karl-Hermann Neeb]], _Structure and Geometry of Lie Groups_, Springer Monographs in Mathematics, Springer-Verlag New York, 2012 ([doi:10.1007/978-0-387-84794-8](https://link.springer.com/book/10.1007/978-0-387-84794-8))


* Mark Haiman, lecture notes by [[Theo Johnson-Freyd]], _Lie groups_, Berkeley 2009 ([pdf](http://math.berkeley.edu/~theojf/LieGroups.pdf))

* [[Eckhard Meinrenken]], _Lie groups and Lie algebas_, Lecture notes 2010 ([pdf](http://www.math.toronto.edu/mein/teaching/LectureNotes/lie.pdf))

### Homotopy groups

* Alexander Abanov, Homotopy groups of Lie groups 2009 ([pdf](http://felix.physics.sunysb.edu/~abanov/Teaching/Spring2009/Notes/abanov-cpA1-upload.pdf))
  {#Abanov09}


### On infinite-dimensional Lie groups
 {#ReferencesOnInfiniteDimensionalLieGroups}

References on [[infinite-dimensional Lie groups]]

* [[Andreas Kriegl]], [[Peter Michor]], _Regular infinite dimensional Lie groups_ Journal of Lie Theory
Volume 7 (1997) 61-99 ([pdf](http://www.heldermann-verlag.de/jlt/jlt07/MICHPL.PDF))

* Rudolf Schmid, _Infinite-Dimensional Lie Groups and Algebras in Mathematical Physics_ Advances in Mathematical Physics Volume 2010, ([pdf](http://www.emis.de/journals/HOA/AMP/Volume2010/280362.pdf))

* Josef Teichmann, _Infinite dimensional Lie Theory from the point of view of Functional Analysis_ ([pdf](http://www.math.ethz.ch/~jteichma/diss.pdf))

* [[Karl-Hermann Neeb]], _Monastir summer school: Infinite-dimensional Lie groups_ ([pdf](http://www.math.uni-hamburg.de/home/wockel/data/monastir.pdf))

[[!redirects Lie groups]]

[[!redirects classical group]]
[[!redirects classical groups]]


[[!redirects classical Lie group]]
[[!redirects classical Lie groups]]