
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Geometry
+--{: .hide}
[[!include higher geometry - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

In [[algebraic geometry]], __algebraic variety__  (not to be confused with [[variety of algebras]]) is a [[scheme]] which is [[integral scheme|integral]], [[separated]] and of [[finite type]] over an [[algebraically closed field]] $k$.

Classically, the term algebraic variety referred to a [[scheme]] as above which is further [[quasi-projective scheme|quasi-projective]], i.e. admits a locally closed embedding into [[projective space]].  Thus, these were objects which locally are cut out inside [[projective space]] as the geometric locus of zeros of a set of [[polynomial]] equations in finitely many variables.  (The first example of an algebraic variety which is not quasi-projective was given by [[Nagata]].)

Historically, there were several formalisms of various schools including the Italian school of [[algebraic geometry]] in the early 20th century (Veronese, Castelnuovo, Severi, ...), the American school between the two wars ([[Oscar Zariski]]), [[Andre Weil]]), the abstract varieties of [[Jean-Pierre Serre]] and finally the language of [[schemes]] introduced by the [[Grothendieck]] school. One should note that in the case of (esp. [[projective variety|projective]]) varieties over complex numbers there is an additional possibility to work using complex-analytic tools and complex topology.

## Definition

Given an [[algebraically closed field]] $k$, an __algebraic $k$-variety__ usually means either a quasiprojective variety or an abstract variety (in the sense of Serre). 'Quasiprojective' unifies affine, quasiaffine, [[projective variety|projective]] and embedded  quasiprojective $k$-varieties. Many modern sources by a variety mean a reduced separated scheme of finite type over a field, often requiring also irreducibility (that is integral = reduced and irreducible). 

* An embedded affine $k$-variety (or an affine algebraic set) is a set of zeros of a locus of common zeros of a set of polynomial equations in the affine space $\mathbf{A}^n_k$. By the Hilbert [[Nullstellensatz]] there is a more invariant definition. __[[affine variety|Affine]]__ $k$-varieties are [[maximal spectrum|maximal spectra]] (= sets of [[maximal ideals]]) of finitely generated [[noetherian ring|noetherian]] (commutative unital) $k$-[[commutative algebra|algebras]] without [[nilpotent element|nilpotents]] with the [[Zariski topology]]; the algebra can be recovered as the coordinate ring of the variety; this correspondence is an equivalence of categories, if the morphisms are properly defined.

  Affine varietes can be embedded as closed subvarieties into an [[affine space]] (in the sense of algebraic geometry). As topological spaces affine varieties are [[noetherian space|noetherian]]. 

* __[[projective variety|Projective]]__ $k$-varieties are obtained in a similar way from [[graded algebra|graded]] $k$-algebras, or, in embedded incarnation, as loci of zeros of a set of homogeneous polynomials in projective space $\mathbf{P}^n_k$. 

* Embedded __quasiaffine__ $k$-varieties are Zariski-open subspaces of affine $k$-varieties. 

* Embedded __quasiprojective__ $k$-varieties are Zariski-open subspaces of projective $k$-varieties. We can remove the embedding by equipping them with the sheaf of regular functions and therefore considering them as [[locally ringed space]]s. In the category of locally ringed spaces, projective, affine, and quasiaffine varieties are (isomorphic to) special cases of quasiprojective. Alternatively, we can put all 4 classes without sheaves into a category, by defining regular maps directly, and we get an isomorphic category of varieties.

  In fact, by noticing that the affine $k$-space is Zariski open in a projective space of the same dimension, we see that the quasiprojective case includes all others. 

Morphisms between varieties are so-called [[regular maps]].  

Sometimes a smooth algebraic variety may also be called __algebraic manifold__. 

An abstract $k$-prevariety in the sense of Serre is a locally ringed space which is locally isomorphic to affine $k$-variety. The category of $k$-prevarieties has a product which is obtained by locally gluing products in the category of affine $k$-varieties. This enables defining a diagonal $X\to X\to X$; a prevariety is separated, or an abstract $k$-variety if the diagonal is closed in Zariski topology (which is, of course, not a product of Zariski topologies of factors).

## Properties

### Relation to schemes

There is an [[equivalence of categories]] between the [[category]] of [[integral schemes]] of finite type over $Spec\,k$, where $k$ is an [[algebraically closed field]], and the category of (irreducible) algebraic $k$-varieties. 

Of course, given a variety the corresponding [[scheme]] and variety have different sets of points; the points in common are the closed points of the scheme. The remaining points are the generic points of subvarieties. Generic points were often used, without proper foundations, in other language, already in the works of the Italian school. 

Some modern algebraic geometers mean, by varieties, objects of certain slightly bigger categories of relative $S$-schemes of finite type (where $S$ is not necessarily $Spec\,k$ for $k$ a field); typically they are required to be [[separated scheme|separated]] [[reduced scheme|reduced]] $S$-[[relative scheme|schemes]] [[morphism of finite type|of finite type]].

## Related concepts

* [[geometric point]]

* [[singular point of an algebraic variety]]

* [[complete algebraic variety]]

* [[semialgebraic manifold]]

## References

* Igor Shafarevich, _Basic algebraic geometry_, vol. I
* J. S. Milne, _Algebraic geometry_, 2017 [pdf](http://www.jmilne.org/math/CourseNotes/AG.pdf)
* Joe Harris, _Introductory algebraic geometry_ 
* chapter I of Robin Hartshorne, _Algebraic geometry_, Springer

An amusing discussion on the differences between schemes and varieties can be found at _Secret blogging seminar_: [algebraic geometry without prime ideals](http://sbseminar.wordpress.com/2009/08/06/algebraic-geometry-without-prime-ideals).

category: algebraic geometry
[[!redirects algebraic varieties]]
[[!redirects affine algebraic variety]]
[[!redirects affine algebraic varieties]]
[[!redirects algebraic manifold]]
[[!redirects algebraic manifolds]]
[[!redirects quasiaffine variety]]
[[!redirects quasiaffine varieties]]
[[!redirects quasiaffine algebraic variety]]
[[!redirects quasiaffine algebraic varieties]]

[[!redirects quasi-projective variety]]
[[!redirects quasiprojective variety]]
[[!redirects quasi-projective varieties]]
[[!redirects quasiprojective varieties]]
[[!redirects quasi-projective algebraic variety]]
[[!redirects quasiprojective algebraic variety]]
[[!redirects quasi-projective algebraic varieties]]
[[!redirects quasiprojective algebraic varieties]]

[[!redirects quasi-projective scheme]]
[[!redirects quasi-projective scheme]]

[[!redirects Var]]
[[!redirects Varieties]]


