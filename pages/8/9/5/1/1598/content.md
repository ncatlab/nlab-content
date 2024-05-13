
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

[[Sophus Lie]] proved several theorems, known as [[Lie's three theorems]], on the relationship between [[Lie algebras]] and Lie groups. Lie's third theorem is about the [[equivalence of categories]] of finite-dimensional real Lie algebras and local Lie groups. Because [[Élie Cartan]] extended this to a global integrability theorem, Lie's third theorem is also called the Cartan-Lie theorem.

### Lie subgroups


\begin{prop}\label{CartanClosedSubgroupTheorem}
**([[Cartan's closed subgroup theorem]])**

If $H \subset G$ is a [[closed subgroup]] of a ([[finite number|finite]] [[dimension of a manifold|dimensional]]) [[Lie group]], then $H$ is a sub-Lie group, hence a [[smooth manifold|smooth]] [[submanifold]] such that its group operations are [[smooth functions]] with respect to the the [[submanifold]] [[smooth structure]].
\end{prop}


### Classification

\begin{prop}

Every connected finite-dimensional real Lie group is [[homeomorphism|homeomorphic]] to a [[product]] of a [[compact Lie group]] and a [[Cartesian space|Euclidean space]]. Every abelian connected compact f.d. real Lie group is a [[torus]] (a product of circles $T^n = S^1\times S^1 \times \ldots \times S^1$).

\end{prop}

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


### Relation to topological groups

* [[continuous homomorphisms of Lie groups are smooth]]


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

  > (in the broader context of [[topological groups]])

* [[Nicolas Bourbaki]], _Lie groups and Lie algebras -- Chapters 1-3_, Springer (1975, 1989) &lbrack;[ISBN:9783540642428](https://link.springer.com/book/9783540642428)&rbrack;


* {#Adams82} [[Frank Adams]], *Lectures on Lie groups*, University of Chicago Press, 1982 ([ISBN:9780226005300](https://press.uchicago.edu/ucp/books/book/chicago/L/bo3614673.html), [gbooks](https://www.google.com/books/edition/Lectures_on_Lie_Groups/TC7d3ZcqjfsC?hl=en))

* {#Onishchik93} A. L. Onishchik (ed.) _Lie Groups and Lie Algebras_

  * *I.* A. L. Onishchik, E. B.  Vinberg, _Foundations of Lie Theory_,

  * *II.* V. V. Gorbatsevich, A. L. Onishchik, _Lie Transformation Groups_ 

  Encyclopaedia of Mathematical Sciences, Volume 20, Springer 1993

* [[Tammo tom Dieck]], [[Theodor Bröcker]], Ch. I of: *Representations of compact Lie groups*, Springer 1985 ([doi:10.1007/978-3-662-12918-0](https://link.springer.com/book/10.1007/978-3-662-12918-0))

  > (in the context of [[representation theory]])

* [[José de Azcárraga]], [[José M. Izquierdo]], *[[Lie Groups, Lie Algebras, Cohomology and Some Applications in Physics]]*, Cambridge Monographs of Mathematical Physics, Cambridge University Press (1995) &lbrack;[doi:10.1017/CBO9780511599897](https://doi.org/10.1017/CBO9780511599897)&rbrack;

* [[Howard Georgi]], *Lie Algebras In Particle Physics*, Westview Press (1999), CRC Press (2019) &lbrack;[doi:10.1201/9780429499210](https://doi.org/10.1201/9780429499210)&rbrack;

  > with an eye towards application to (the [[standard model of particle physics|standard model]] of) [[particle physics]]


* [[Hans Duistermaat]], [[Johan A. C. Kolk]], *Lie groups*, Springer (2000) &lbrack;[doi:10.1007/978-3-642-56936-4](https://doi.org/10.1007/978-3-642-56936-4)&rbrack;

* Mark Haiman, lecture notes by [[Theo Johnson-Freyd]], _Lie groups_, Berkeley 2009 ([pdf](http://math.berkeley.edu/~theojf/LieGroups.pdf))

* [[Eckhard Meinrenken]], _Lie groups and Lie algebas_, Lecture notes 2010 ([pdf](http://www.math.toronto.edu/mein/teaching/LectureNotes/lie.pdf))

* {#HilgertNeeb12} [[Joachim Hilgert]], [[Karl-Hermann Neeb]], _Structure and Geometry of Lie Groups_, Springer Monographs in Mathematics, Springer-Verlag New York, 2012 ([doi:10.1007/978-0-387-84794-8](https://link.springer.com/book/10.1007/978-0-387-84794-8))

* {#Hall15} [[Brian C. Hall]], *Lie Groups, Lie Algebras, and Representations*, Springer 2015 ([doi:10.1007/978-3-319-13467-3](https://doi.org/10.1007/978-3-319-13467-3))

* {#GallierQuaintance20a} [[Jean Gallier]], [[Jocelyn Quaintance]],  *Differential Geometry and Lie Groups -- A computational perspective*, Geometry and Computing **12**, Springer (2020) &lbrack;[doi:10.1007/978-3-030-46040-2](https://doi.org/10.1007/978-3-030-46040-2), [webpage](https://www.cis.upenn.edu/~jean/gbooks/manif.html)&rbrack;

* {#GallierQuaintance20b} [[Jean Gallier]], [[Jocelyn Quaintance]],  *Differential Geometry and Lie Groups -- A second course*, Geometry and Computing **13**, Springer (2020) &lbrack;[doi:10.1007/978-3-030-46047-1](https://doi.org/10.1007/978-3-030-46047-1), [webpage](https://www.cis.upenn.edu/~jean/gbooks/manif.html)&rbrack;

* [[Pavel Etingof]], *Lie groups and Lie algebras* &lbrack;[arXiv:2201.09397](https://arxiv.org/abs/2201.09397)&rbrack;


In the generality of [[Lie semigroups]]:

* [[Joachim Hilgert]], [[Karl-Hermann Neeb]], *Lie Semigroups and their Applications*. Lecture Notes in Mathematics **1552**, Springer 1993 ([doi:10.1007/BFb0084640](https://link.springer.com/book/10.1007/BFb0084640))

In the generality of [[quantum groups]]:

* [[Richard Borcherds]], [[Mark Haiman]], [[Theo Johnson-Freyd]], [[Nicolai Reshetikhin]], [[Vera Serganova]], *Berkeley Lectures on Lie Groups and Quantum Groups*, 2020 ([pdf](http://categorified.net/LieQuantumGroups.pdf))


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

### Spaces of homomorphisms

On [[mapping spaces]] of [[continuous function|continuous]] [[homomorphisms]] from [[topological groups]] to [[Lie groups]]:

for maps out of [[finitely generated group|finitely generated]] [[discrete groups]]":

* [[Frederick R. Cohen]], [[Mentor Stafa]], *A survey on spaces of homomorphisms to Lie groups*,  In: Callegaro F., Cohen F., De Concini C., Feichtner E., Gaiffi G., Salvetti M. (eds.) *Configuration Spaces*, INdAM Series, vol 14, Springer 2016 ([arXiv:1412.5668](https://arxiv.org/abs/1412.5668), [doi:10.1007/978-3-319-31580-5_15](https://doi.org/10.1007/978-3-319-31580-5_15)) 

for maps out of [[compact Lie groups]] and the fact that [[nearby homomorphisms from compact Lie groups are conjugate]]:

* [[Pierre Conner]], [[Edwin Floyd]], Ch. III, Lem. 38.1 in: _Differentiable periodic maps_, Ergebnisse der Mathematik und ihrer Grenzgebiete **33**, Springer 1964 ([doi:10.1007/978-3-662-41633-4](https://link.springer.com/book/10.1007/978-3-662-41633-4))

* [[Charles Rezk]], *Nearby homomorphisms from compact Lie groups are conjugate* ([MO:q/123624](https://mathoverflow.net/q/123624/381))

* {#Rezk14} [[Charles Rezk]], Rem. 2.2.1 in: *[[Global Homotopy Theory and Cohesion]]*, 2014 ([pdf](http://www.math.uiuc.edu/~rezk/global-cohesion.pdf), [[Rezk14.pdf:file]])


[[!redirects Lie groups]]

[[!redirects classical group]]
[[!redirects classical groups]]

