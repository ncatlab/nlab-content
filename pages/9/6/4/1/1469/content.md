
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Geometry
+--{: .hide}
[[!include higher geometry - contents]]
=--
#### Algebra
+--{: .hide}
[[!include higher algebra - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Overview

__Algebraic geometry__ is, in origin, a [[geometry|geometric study]] of solutions of systems of [[polynomial]] equations and generalizations.

The set of zeros of a set of polynomial equations in finitely many variables over a [[field]] is called an __affine [[algebraic variety|variety]]__ and it is equipped with a particular topology called [[Zariski topology]], whose closed sets are subvarieties. The system of polynomial equations defines an [[ideal]] in the ring of polynomials over the [[ground field]]; one of the first insights of algebraic geometry is that the ideal is a more invariant notion than the original set of equations. The [[quotient object|quotient]] of the ring of polynomials by the defining ideal is the ring of coordinate functions of the affine variety; a basic theorem asserts that this ring is [[noetherian ring|Noetherian]] algebra over the ground field. This ring determines the variety up to a natural notion of [[isomorphism]] of varieties. __Projective varieties__ are zeroes of systems of homogeneous polynomial equations in projective $n$-dimensional space; if the coordinates are rescaled by a common nonzero multiple, then by definition they still define the same point in projective space. Zariski open subsets of affine (or projective) varieties are called __quasiprojective varieties__.

It is often useful to take a [[pullback]] along a morphism of fields, usually called [[base change]]. Since [[Alexander Grothendieck|Grothendieck]], one generalizes the coordinate rings of affine varieties to arbitrary commutative unital rings, not necessarily Noetherian nor finitely generated; and interprets the [[opposite category]] of the category of commutative rings as a category of affine [[scheme]]s $\mathrm{Aff}$; affine schemes are traditionally constructed by the affine [[spectrum]] functor $\mathrm{Spec}:\mathrm{CommRing}^{\mathrm{op}}\to\mathrm{lrSp}$ into the category of locally [[ringed space|ringed]] topological spaces. Points of the affine spectrum are the prime ideals of the ring. Assuming the [[axiom of choice]], every affine scheme corresponding to a ring with $0 \neq 1$ has therefore at least one point. The slice category $\mathrm{Aff}/(\mathrm{Spec} F)$ over a spectrum of a fixed field $F$ contains the category of varieties over $F$ as a full subcategory. However the points of an affine variety and of the corresponding affine spectrum do not coincide: only *maximal* ideals are points of usual varieties. Affine schemes have a natural topology, also called a Zariski topology; the ringed spaces locally isomorphic to affine schemes are called __schemes__. Schemes include projective schemes and more generally quasiprojective schemes; if they are relative over a fixed [[ground field]], then they contain the subcategories of projective (resp. quasiprojective) varieties over the same field.

Although [[Grothendieck]] in the late 1950s envisioned many generalizations of [[scheme]] theory, his coauthor Dieudonn&#233; wrote later in EGA that algebraic geometry is the study of algebraic and [[formal schemes]], which is clearly a too dogmatic definition. Grothendieck's school studied in addition locally affine spaces in various [[Grothendieck topology|Grothendieck topologies]] on $\mathrm{Aff}$ (including [[algebraic space]]s), [[algebraic stack]]s ([[Deligne-Mumford stack]]s and [[Artin stack]]s), [[ind-object|ind-schemes]] and so on; in SGA the study of ringed spaces is replaced by more general [[ringed site]]s and [[ringed topos|ringed topoi]]. Modern generalizations include derived schemes, almost schemes (with the theory of almost rings of Gabber developing after some ideas of [Faltings](http://de.wikipedia.org/wiki/Gerd_Faltings)), generalized schemes of [[Nikolai Durov]], so-called schemes over the '[[field of one element]]' $F_1$ of various authors, dg-schemes, slightly noncommutative [[D-scheme]]s etc. Many ideas of scheme theory and the spectral theory of rings have influenced parallel developments in the analytic setup (Stein manifolds ([see the English Wikipedia](http://en.wikipedia.org/wiki/Stein_manifold)), rigid [[analytic geometry|analytic spaces]], etc.) and in the noncommutative setup give rise to [[noncommutative algebraic geometry]]. Deligne has also suggested how to do algebraic geometry in an arbitrary symmetric monoidal category. 


## Perspective of structured $(\infty,1)$-toposes 

Grothendieck took the viewpoint that the schemes, algebraic spaces etc. are sheaves on $Aff$ in some subcanonical Grothendieck topology (functor of points point of view). 

Algebraic geometry starts with study of [[space]]s that are locally modeled on ([[object]]s in the [[category]]) Aff = [[CRing]]${}^{op}$ -- main categories being of algebraic [[scheme]]s and of [[algebraic space]]s; one also allows infinitesimal thickenings leading to formal schemes and other ind-objects in schemes. Hakim, [[Deligne]] and [[Ofer Gabber|Gabber]] extend the setup internally to a symmetric monoidal category, where $Aff$ is replaced by the opposite to the category of monoids in that category; [[Nikolai Durov|Durov]] on the other side takes monoids in the category of endofunctors in [[Set]], i.e. [[monad]]s as the opposite to the local objects in a generalized scheme theory.

This is to be compared to and contrasted with for instance [[differential geometry]], that studies [[space]]s locally modeled on ([[object]]s in the [[category]]) [[CartSp]] -- called (smooth) [[manifold]]s.

The general formalization of the notion of [[space]] and hence, by the general lore of [[space and quantity]], that of [[sheaf]], [[stack]], [[∞-stack]] has originally been crucially inspired by [[Grothendieck]]'s work on algebraic geometry and is more recently being greatly revived and further extended by the developments in [[derived algebraic geometry]] by people like [[Bertrand Toen]] and [[Jacob Lurie]].

In particular in [[Structured Spaces]] Lurie presents a general formalism of [[generalized scheme]]s that encompasses the [[space]]s studied in algebraic geometry and [[derived algebraic geometry]] just as well as ordinary [[smooth manifold]]s, [[derived smooth manifold]] and harmonizes with other axiomatizations such as in [[synthetic differential geometry]]: all of these [[space]] object are realized as special cases of [[structured (∞,1)-topos]]es, differing only in the choice of [[geometry (for structured (∞,1)-toposes)]] that they are modeled on.

From this perspective,

* ordinary algebraic geometry is the study of [[structured (∞,1)-topos]]es for the [[geometry (for structured (∞,1)-toposes)|Zariski or etale geometry]] $\mathcal{G}_{Zar}$, $\mathcal{G}_{et}$ on [[CRing]]${}^{op}$. In fact one has as series of geometries for every integer $n\geq 0$, where classical case is at level $0$ and derived at level $\infty$. Cf. 4.2.9 in [[Structured Spaces]]. The fully faithful embedding of schemes into derived schemes does not commute with limits, what is relevant e.g. for intersection theory.

* [[derived algebraic geometry]] is the study of [[structured (∞,1)-topos]]es for the [[geometry (for structured (∞,1)-toposes)|Zariski or etale pre-geometry]] $\mathcal{T}_{Zar}$, $\mathcal{T}_{et}$ on [[CRing]]${}^{op}$.

Despite of this, an axiomatic formulation of algebraic geometry along the lines of [[synthetic differential geometry]], that would de-emphasize the peculiarities of $CRing^{op}$ and emphasize structural aspects such as to facilitate for instance the transportation or interpretation of results in algebraic geometry to other geometries, is currently hardly to be found in the elementary literature. [[SGA]], specially SGA IV was written however to reflect "algebraic" geometry over any topos. 

>Maybe we could talk more about [[synthetic differential geometry applied to algebraic geometry]] to unify perspective of algebraic with differential geometry.

## Related pages

* [[synthetic algebraic geometry]]

* [[contributors to algebraic geometry]]

* [[books in algebraic geometry]], 

* [pages in the category "algebraic geometry"](http://www.ncatlab.org/nlab/list/algebraic+geometry)

* [[functorial geometry]]

* [[derived algebraic geometry]]

* [[noncommutative geometry]]

## References
 {#References}

Original references: [[EGA]] and [[SGA]].

Textbook accounts:

* {#ShafarevichVol1} [[Igor Shafarevich]], *Basic Algebraic Geometry 1 -- Varieties in Projective Space*, Springer (1977, 1994, 2013) &lbrack;[pdf](http://userpage.fu-berlin.de/aconstant/Alg2/Bib/Shafarevich.pdf), [doi:10.1007/978-3-642-57908-0](https://link.springer.com/book/10.1007/978-3-642-57908-0)&rbrack;

* [[James Milne]]: *Algebraic Geometry* (1996-) &lbrack;[webpage](https://www.jmilne.org/math/CourseNotes/ag.html), [pdf 2008](https://www.jmilne.org/math/CourseNotes/AG510.pdf)&rbrack;

* [[Siegfried Bosch]], *Algebraic Geometry and Commutative Algebra*, Universitext, Springer (2017) &lbrack;[doi:10.1007/978-1-4471-4829-6](https://doi.org/10.1007/978-1-4471-4829-6)&rbrack;

*  Ulrich Görtz, Torsten Wedhorn, *Algebraic Geometry I: Schemes*, Springer (2020) &lbrack;[doi:10.1007/978-3-658-30733-2](https://doi.org/10.1007/978-3-658-30733-2)&rbrack; ; *Algebraic Geometry II: Cohomology of Schemes*, Springer 2023


* [[Robin Hartshorne]], Algebraic Geometry, Graduate Texts in Mathematics __52__, Springer 1977. &lbrack;[doi:10.1007/978-1-4757-3849-0](https://doi.org/10.1007/978-1-4757-3849-0)&rbrack;

Lecture notes:

* [[Ravi Vakil]], _Foundations of algebraic geometry_, Course notes ([web](http://math.stanford.edu/~vakil/216blog/))

See also the references at _[[functorial geometry]]_.

and see

* _[[The Stacks Project]]_

On [[synthetic algebraic geometry]], i.e. via the [[internal logic]] of the [[sheaf topos]] over a [[scheme]] ([[Zariski topos]]/[[étale topos]]):

* {#Blechschmidt15} [[Ingo Blechschmidt]], _Using the internal language of toposes in algebraic geometry_, talk at [Toposes at IHES](https://indico.math.cnrs.fr/event/747/), November 2015 ([pdf](https://github.com/iblech/internal-methods/blob/master/slides-ihes2015.pdf), [recording](https://www.youtube.com/watch?v=7S8--bIKaWQ))

* [[Ingo Blechschmidt]], *Using the internal language of toposes in algebraic geometry*, PhD thesis (2017) &lbrack;[pdf](https://rawgit.com/iblech/internal-methods/master/notes.pdf), [[Blechschmidt-InternalLanguage.pdf:file]]&rbrack;

* [[Felix Cherubini]], [[Thierry Coquand]], [[Matthias Hutzler]], *A Foundation for Synthetic Algebraic Geometry* (2023) &lbrack;[arXiv:2307.00073](https://arxiv.org/abs/2307.00073)&rbrack;

* [[Felix Cherubini]], *A Foundation for Synthetic Algebraic Geometry*, talk at *[Homotopy Type Theory Electronic Seminar Talks](https://www.uwo.ca/math/faculty/kapulkin/seminars/hottest.html)* (Oct 2023) &lbrack;slides:[pdf](https://www.uwo.ca/math/faculty/kapulkin/seminars/hottestfiles/Cherubini-2023-10-18-HoTTEST.pdf), video:[YT](https://www.youtube.com/watch?v=lp4kcmQ0ueY)&rbrack;

For more see:

* [[Ingo Blechschmidt]], _Internal methods_ &lbrack;[github](https://github.com/iblech/internal-methods)&rbrack;


category: algebraic geometry

[[!redirects algebraic geometer]]