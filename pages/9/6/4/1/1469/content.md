#Contents#
* automatic table of contents goes here
{:toc}

#Overview

__Algebraic geometry__ is, in origin, a [[geometry|geometric study]] of solutions of systems of [[polynomial]] equations and generalizations.

The set of zeros of a set of polynomial equations in finitely many variables over a [[field]] is called an __affine [[algebraic variety|variety]]__ and it is equipped with a particular topology called [[Zariski topology]], whose closed sets are subvarieties. The system of polynomial equations defines an [[ideal]] in the ring of polynomials over the [[ground field]]; one of the first insights of algebraic geometry is that the ideal is a more invariant notion than the original set of equations. The [[quotient object|quotient]] of the ring of polynomials by the defining ideal is the ring of coordinate functions of the affine variety; a basic theorem asserts that this ring is [[noetherian ring|Noetherian]] algebra over the ground field. This ring determines the variety up to a natural notion of [[isomorphism]] of varieties. __Projective varieties__ are zeroes of systems of homogeneous polynomial equations in projective $n$-dimensional space; if the coordinates are rescaled by a common nonzero multiple, then by definition they still define the same point in projective space. Zariski open subsets of affine (or projective) varieties are called __quasiprojective varieties__.

It is often useful to take a [[pullback]] along a morphism of fields, usually called [[base change]]. Since [[Alexander Grothendieck|Grothendieck]], one generalizes the coordinate rings of affine varieties to arbitrary commutative unital rings, not necessarily Noetherian nor finitely generated; and interprets the [[opposite category]] of the category of commutative rings as a category of affine [[scheme]]s $\mathrm{Aff}$; affine schemes are traditionally constructed by the affine [[spectrum]] functor $\mathrm{Spec}:\mathrm{CommRing}^{\mathrm{op}}\to\mathrm{lrSp}$ into the category of locally [[ringed space|ringed]] topological spaces. Points of the affine spectrum are the prime ideals of the ring. Assuming the [[axiom of choice]], every affine scheme corresponding to a ring with $0 \neq 1$ has therefore at least one point. The slice category $\mathrm{Aff}/(\mathrm{Spec} F)$ over a spectrum of a fixed field $F$ contains the category of varieties over $F$ as a full subcategory. However the points of an affine variety and of the corresponding affine spectrum do not coincide: only *maximal* ideals are points of usual varieties. Affine schemes have a natural topology, also called a Zariski topology; the ringed spaces locally isomorphic to affine schemes are called __schemes__. Schemes include projective schemes and more generally quasiprojective schemes; if they are relative over a fixed [[ground field]], then they contain the subcategories of projective (resp. quasiprojective) varieties over the same field.

Although [[Grothendieck]] in the late 1950s envisioned many generalizations of [[scheme]] theory, his coauthor Dieudonn&#233; wrote later in EGA that algebraic geometry is the study of algebraic and [[formal schemes]], which is clearly a too dogmatic definition. Grothendieck's school studied in addition locally affine spaces in various [[Grothendieck topology|Grothendieck topologies]] on $\mathrm{Aff}$ (including [[algebraic space]]s), [[algebraic stack]]s ([[Deligne-Mumford stack]]s and [[Artin stack]]s), [[ind-object|ind-schemes]] and so on; in SGA the study of ringed spaces is replaced by more general [[ringed site]]s and [[ringed topos|ringed topoi]]. Modern generalizations include derived schemes, almost schemes (with the theory of almost rings of Gabber developing after some ideas of [Faltings](http://de.wikipedia.org/wiki/Gerd_Faltings)), generalized schemes of [[Nikolai Durov]], so-called schemes over the 'field of one element' $F_1$ of various authors, dg-schemes, slightly noncommutative $D$-schemes etc. Many ideas of scheme theory and the spectral theory of rings have influenced parallel developments in the analytic setup (Stein manifolds ([see the English Wikipedia](http://en.wikipedia.org/wiki/Stein_manifold)), rigid [[analytic geometry|analytic spaces]], etc.) and in the noncommutative setup give rise to [[noncommutative algebraic geometry]]. Deligne has also suggested how to do algebraic geometry in an arbitrary symmetric monoidal category. 


#Perspective of structured $(\infty,1)$-toposes #

Grothendieck took the viewpoint that the schmees, algebraic spaces etc. are sheaves on $Aff$ in some subcanonical Grothendieck topology (functor of points point of view). 

Algebraic geometry studies [[space]]s that are locally modeled on ([[object]]s in the [[category]]) [[CRing]]${}^{op}$ -- called [[algebraic space]]s or [[scheme]]s.

+--{.query}
Zoran: Not entirely true, this is far too limited point of view. For example [[formal schemes]] are in this functorial viewpoint the functors on pairs (ring, nilpotent ideal); for generalized schemes of Durov you need monads and so on...By the way, we already have SEVERAL sections about the spaces as sheaves, about the viewpoint of functor of points, why to repeat all that general nonsense instead of focusing to the specifics of the subject which is by algebaric geometers called algebraic geometry ? I prefer that algebraic geometry page has specifics about the numerous facets of the subject, not only about some specific general and current formalism. On the other hand, there should be separate entries on quantities, functor of points viewpoint etc.
=--

This is to be compared to and contrasted with for instance [[differential geometry]], that studies [[space]]s locally modeled on ([[object]]s in the [[category]]) [[CartSp]] -- called (smooth) [[manifold]]s.

The general formalization of the notion of [[space]] and hence, by the general lore of [[space and quantity]], that of [[sheaf]], [[stack]], [[∞-stack]] has originally been crucially inspired by [[Grothendieck]]'s work on algebraic geometry and is more recently being greatly revived and further extended by the developments in [[derived algebraic geometry]] by people like [[Bertrand Toen]] and [[Jacob Lurie]].

In particular in [[Structured Spaces]] Lurie presents a general formalism of [[generalized scheme]]s that encompasses the [[space]]s studied in algebraic geometry and [[derived algebraic geometry]] just as well as ordinary [[manifold|smooth manifold]]s, [[derived smooth manifold]] and harmonizes with other axiomatizations such as in [[synthetic differential geometry]]: all of these [[space]] object are realized as special cases of [[structured (∞,1)-topos]]es, differing only in the choice of [[geometry (for structured (∞,1)-toposes)]] that they are modeled on.

From this perspective,

* ordinary algebraic geometry is the study of [[structured (∞,1)-topos]]es for the [[geometry (for structured (∞,1)-toposes)|Zariski or etale geometry]] $\mathcal{G}_{Zar}$, $\mathcal{G}_{et}$ on [[CRing]]${}^{op}$


+--{.query}
Zoran: We are still not sure if this is true (you keep saying this) but I am not sure that this is correct. 

[[Urs Schreiber]]: this is prop 4.2.9 in [[Structured Spaces]], currently recalled on the page [[derived scheme]].

=--



* [[derived algebraic geometry]] is the study of [[structured (∞,1)-topos]]es for the [[geometry (for structured (∞,1)-toposes)|Zariski or etale pre-geometry]] $\mathcal{T}_{Zar}$, $\mathcal{T}_{et}$ on [[CRing]]${}^{op}$.

Despite of this, an axiomatic formulation of algebraic geometry along the lines of [[synthetic differential geometry]], that would de-emphasize the peculiarities of $CRing^{op}$ and emphasize structural aspects such as to facilitate for instance the transportation or interpretation of results in algebraic geometry to other geometries, is currently hardly to be found in the literature,

+--{.query}
Zoran: so what is SGA IV about ?

[[Urs Schreiber]]: please write a paragraph on what it is about. 
=--

 leading to an unfortunate and unnecessary gap between for instance the fields of algebraic geometry and [[differential geometry]].

>Maybe we can change this by talking about [[synthetic differential geometry applied to algebraic geometry]].

