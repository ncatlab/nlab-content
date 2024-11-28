
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Differential geometry
+--{: .hide}
[[!include synthetic differential geometry - contents]]
=--
#### Higher geometry
+--{: .hide}
[[!include higher geometry - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

Traditional [[differential geometry]] is the field of [[mathematics]] that studies the [[geometry]] of [[smooth spaces]] which are equipped with a notion of [[differentiation]]. There is a refinement of this traditional theory to the general context of "[[higher geometry]]" -- this is accordingly called _[[higher differential geometry]]_.

In higher differential geometry, [[geometry]] is paired with [[homotopy theory]]. Accordingly, [[smooth spaces]] are refined to "smooth [[homotopy types]]" -- often called _[[smooth infinity-groupoids]]_ or _[[infinity-stacks]]_ -- and [[function algebras]] of [[smooth functions]] are refined to [[strong homotopy algebras]], often called _[[infinity-algebra over an (infinity,1)-operad|infinity-algebras]]_.

Here we give an informal overview of what motivates this generalization and what it is good for.

First we list some examples of how tools from [[higher differential geometry]] help to understand plain traditional [[differential geometry]]:

* _[I) Applications of higher DG to plain DG](#ApplicationsOfHigherDGToPlainDG)_

Besides illuminating traditional DG where it exists, higher DG naturally extends plain DG to regions where it breaks down due to [[singularities]]:

* _[II) Resolution of singularities in plain DG](#ResolutionOfSingularities)_

However, much of the genuine motivation for developing [[higher differential geometry]] came and increasingly comes from structures in fundamental [[physics]], in [[quantum field theory]] and [[string theory]], which are intrinsically of [[higher geometry|higher geometric]] nature, hence for which no adequate description in plain [[differential geometry]] even exists (this is in fact already true for traditional local gauge theory, see [below](#FieldBundles)). 
This we discuss in:

* [III) Motivation of higher DG from physics](#MotivationOfHigherDGFromPhysics)


## **I)** Applications of higher DG to plain DG
{#ApplicationsOfHigherDGToPlainDG}

This section lists examples of how [[higher differential geometry]] helps with understanding plain [[differential geometry]].

* [Foliations and PDEs](#FoliationsAndPDEs)

* [Poisson and symplectic geometry](#PoissonGeometry)

* [Deformation theory](#DeformationTheory)

* [Orbifolds](#Orbifolds)

* [Field bundles for local gauge theory](#FieldBundles)

* [Lie integration](#LieIntegration)

* [Variational calculus and symplectic reduction](#VariationalCalculusAndSymplecticReduction)



### Foliations and PDEs
 {#FoliationsAndPDEs}

At the roots of differential geometry, prominent in the original work of [[Eli Cartan]], is [[foliation]] theory, arising in the integration of [[partial differential equations]]. 

   In the context of [[Lie groupoid]] theory, foliations have a classification -- a [[moduli stack]]: the [[Haefliger groupoid]]. The textbook ([Moerdijk-Mrcun](#MoerdijkMrcun)) discusses foliation theory from this perspective. The _[[Haefliger theorem]]_ which classifies foliations on open manifolds is proven by way of the [[Haefliger groupoid]].

   Cartan had originally encoded the [[partial differential equation|PDEs]] whose integration leads to foliation by "[[exterior differential systems]]". These are equivalently ([[Chevalley-Eilenberg algebras]]) of [[L-∞ algebroids]]. The entire theory of integration is thereby part of higher [[Lie theory]] -- [[infinity-Lie theory]]. 

### Poisson and symplectic geometry
 {#PoissonGeometry}

A subtopic of this is [[Poisson geometry]], where the foliation is by [[symplectic leaves]]. A fundamental problem in Poisson geometry was the [[deformation quantization]] of [[Poisson manifolds]]. 

   The [[formal deformation quantization]] problem was solved by [[Kontsevich]], which earned him a Fields medal. [[Cattaneo]] and [[Felder]] then showed that his formula for the [[star product]] is naturally understood as a [[3-point function]] of the [[Poisson sigma model]], a [[sigma-model]] [[QFT]] whose [[target space]] is the [[Poisson Lie algebroid]] of the given Poisson manifold. 

   The strengthening of this to the [[strict deformation quantization]] problem for a large class of cases was then established by forming the [[convolution algebra]] of sections of the [[prequantum bundle|prequantization]] of the [[symplectic groupoid]] with [[Lie integration|Lie integrates]] the [[Poisson Lie algebroid]].

   (In [[QFT]] the shift into [[higher geometry]] witnessed in both these proofs is a special case of what is known as the [[holographic principle]]: the 0-categorical structure of Poisson manifolds is quantized via the 1-categorical strucure of [[Poisson Lie algebroids]] and [[symplectic groupoids]].)

The [[symplectic groupoid]] that induces the [[strict deformation quantization]] of a Poisson manifold also solves its classical desingularization problem, its _[[symplectic realization]]_.
For any [[symplectic groupoid]] $\Sigma$ with base a [[Poisson manifold]] $P$ the target map is a symplectic realization of $P$ and  the source map is a symplectic realization  of the opposite structure. Thus $\Sigma$ with its symplectic structure may be regarded as a desingularization of  $P$ with its Poisson structure. Since the [[symplectic groupoid]] is the [[Lie integration]] of the [[Poisson Lie algebroid]] of the Poisson manifold, symplectic realization is reduced to a problem in [[Lie theory]].


### Deformation theory
 {#DeformationTheory}

Apart from these Poisson structures and [[symplectic structures]], differential geometry studies many other kinds of smooth structures on [[smooth manifolds]], such as [[complex structures]] in [[complex geometry]]. The classification of these structures in each case is [[infinitesimal space|infinitesimally]] given by [[deformation theory]]. Since seminal work referenced at _[[model structure for L-∞ algebras]]_ it is known that deformation theory is essentially equivalently the study of [[L-∞ algebra]] in [[∞-Lie theory]]. Classical theorems in complex differential geometry such as the discussion of [[period maps]] find their natural formulation in this context. This is amplified in  ([Fiorenza-Martinengo2012](#FiorenzaMartinengo)).

### Orbifolds
 {#Orbifolds}

Almost as basic to traditional differential geometry as [[manifolds]] are [[orbifold]], which incorporate non-free [[actions]] into the theory. Notably the [[moduli spaces]] arising in differential geometry tend to be orbifolds instead of manifolds. 

But orbifolds are equivalently a [[proper Lie groupoid|proper]] [[étale Lie groupoid]].  (This relation is for some reason more famous in algebraic geometry, where the &#233;tale Lie groupoids are called [[Deligne-Mumford stacks]].)

### Field bundles for local gauge theory
 {#FieldBundles}

Differential geometry shares much of its origin and history with [[physics]]: [[tensor fields]] and [[Riemannian geometry]] grew out of the theory of [[gravity]] and [[Chern-Weil theory]] and [[differential cohomology]] out of the study of [[gauge theory]]. [[Maxwell's equations]] influenced the study of [[de Rham cohomology]].

Out of this tradition has grown the formalization of [[physical fields]] as [[sections]] of a [[fiber bundle]] over [[spacetime]] called the _[[field bundle]]_. But this notion is insufficient: there cannot be a field bundle for _both_ [[gauge field theory]] and [[local quantum field theory]]. This problem is typically not felt in [[perturbation theory]], but it affects all attempts to go beyond. 

The reason is that a [[gauge field]], including its underlying [[instanton sector]]/[[charge]] sector, is not a section of a fiber bundle but of a [[fiber infinity-bundle|fiber 2-bundle]], the anolog in higher differential geometry. Detailed discussion of this is at _[[field (physics)]]_ and in the corresponding section at _[[geometry of physics]]_.


### Lie integration
 {#LieIntegration}

[[Lie integration]] of anything more general than a finite-dimensional [[Lie algebra]] in general goes out of the real of [[Lie groups]]. Local brackets = [[Lie algebroids]] integrate to [[Lie groupoids]] and 
infinite-dimensional Lie algebras in general to [[Lie 2-groups]].

(...)

### Variational calculus and symplectic reduction
 {#VariationalCalculusAndSymplecticReduction}

[[derived differential geometry]] allows to resolve many otherwise singular limit/intersection constructions. Modern [[variational calculus]] in terms of [[jet bundle]] ("[[D-geometry]]") is formulated this way, as is [[symplectic reduction]] and the unification of both in the [[BV-BRST formalism]].

## **II)** Resolution of singularities in plain DG
 {#ResolutionOfSingularities}

[[singularity|Singularities]] arise in [[differential geometry]] if the two kinds of [[universal constructions]] fail to exist as [[smooth manifolds]]:

1. if an _intersection_ (in [[category theory]]: a [[limit]]) fails to exist this is resolved by passing from [[critical loci]] to [[derived critical loci]]:

   [Resolution of singular intersection](#ResolutionOfSingularIntersections)

1. if a _[[quotient]]_ (in [[category theory]]: a [[colimit]]) fails to exist, this is resolved by passing to [[homotopy quotients]]:

   [Resolution of singular quotients: stacks quotients](#ResolutionOfSingularQuotients)

   

### Resolution of singular qotients: stacky quotients
 {#ResolutionOfSingularQuotients}


... [[stack]] ... [[homotopy quotient]] ... [[quotient stack]] ... [[differentiable stack]] ...


### Resolution of singular intersections: derived intersections
 {#ResolutionOfSingularIntersections}

The [[category]] of [[smooth manifolds]] does not have many [[limits]]. Accordingly many constructions that one would like to perform in traditional differential geometry simply fail to exist. For instance the [[critical locus]] of a [[smooth function]] -- of central relevance in [[variational calculus]] -- rarely is again a [[smooth manifold]] and hence cannot be treated with tools of differential geometry, in general.

In the "[[derived differential geometry]]"-flavor of [[higher differential geometry]] (technically: the not-[[n-localic (infinity,1)-topos|1-localic]]) this problem is resolved by replacig [[function algebras]] of [[smooth functions]] by [[simplicial algebras]], which essentially amounts to refining [[smooth manifolds]] by [[dg-manifolds]]. This refinement resolves previously singular (hence: non-existing in DG) by the method of [[resolution]] familiar from [[homological algebra]]: a singular intersection is realized as the [[homology group]] of a [[chain complex]] of perfectly smooth manifolds (or rather their function algebras).

Applied the concept of [[critical locus]] this leads to the notion of _[[derived critical locus]]_. This is actually a construction secretly with a long tradition in differential geometry, known as the _[[BV-BRST formalism]]_. Higher and [[derived differential geometry]] provide a theoretical framework for handling [[BV-BRST formalism]] systematically.



## **III)** Motivation of higher DG from physics
 {#MotivationOfHigherDGFromPhysics}

To a large extent, [[differential geometry]] had been co-evolving with the description of [[physics]] in terms of _[[field (physics)|fields]]_. We have already seen above in _[Field bundles for local gauge theory](#FieldBundles)_ that an accurate formulation even of traditional notions of such fields requires [[higher differential geometry]] to degree 1. But modern developments in [[quantum field theory]] require notions of [[physical fields]] and [[quantum states]] that probe much more deeply into the realm of geometric [[homotopy theory]]. We indicate here some aspects. For comprehensive introductory lecture notes on this topic see at 

* _[[geometry of physics]]_.

A more technical survey of is in [FSS 13](#FSS).

Below we first discuss how combining the notion of [[local quantum field theory]] in its modern incarnation as [[extended quantum field theory]] with [[prequantum field theory|Lagrangian]] quantum field theory necessitates higher differential geometric structures:

* [Extended prequantum field theory](#ExtendedPrequantumFieldTheory)

Then we turn to modern proposals for [[theory (physics)|theories]] that go beyond the [[standard model of particle physics]] and which inherently contain higher geometric fields already in their non-localized formalization:

* [Higher gauge fields](#HigherGaugeFields)

(...)

### The higher orbit method -- Extended prequantum field theory
 {#ExtendedPrequantumFieldTheory}

A high point of traditional [[differential geometry]] is its impact on [[representation theory]] via the _[[orbit method]]_. This is actually a construction deeply rooted in [[quantum mechanics]]:  given a [[symplectic manifold]] equipped with [[Hamiltonian action]] by a [[Lie group]], regarding this as a [[mechanical system]] and then applying the differential-geometric process of [[geometric quantization]] to its yields a [[space of states]] on which the group is represented. A large class of [[representations]] arises this way and the [[orbit method]] sheds light on the corresponding [[representation theory]].

But speaking of [[physics]] in the first place, certainly the [[quantum mechanics]] governing the [[orbit method]] is just the simplest fragment of the foundational theory of [[physics]], which is [[quantum field theory]] in arbitrary [[dimension]]. Quantum mechanics can be thought of as quantum field theory in dimension 1 ("on the [[worldline]]"). Passing in [[geometric quantization]]/[[orbit method]] from dimension 1 to higher dimensional quantum field theory corresponds precisely, as we discuss now, to passing to [[higher differential geometry]]: "[[extended prequantum field theory|extended prequantum geometry]]".


The notion of _[[quantum field theory]]_ exists without reference to any predefined notion of _[[configuration space]]_ of _[[quantum fields]]_, _[[action functional]]_, _[[phase space]]_ etc.: 

A [[quantum field theory]] in [[FQFT]]-[[axiomatization]] is simply a consistent assignment of [[spaces of quantum states]], whereas in [[AQFT]]-[[axiomatization]] it is a consistent assignment of [[algebras of quantum observables]], and that's it. 

However, most (or maybe all?) quantum field theories of interest in actual [[physics]] (as opposed to as devices of pure [[mathematics]]) are not random models of these axioms, but do arise under a process called [[quantization]] from a ([[local Lagrangian|local]]/[[extended Lagrangian|extended]]) [[Lagrangian]], hence from an [[action functional]], defined on a [[configuration space]] of [[quantum fields]], or else arise as [[holographic duals]] of quantum field theories that arise by quantization. Moreover, the extra information provided by the Lagrangian is commonly used (and is maybe strictly necessary) to interpret the mathematical structure of the axiomatic QFT in actual [[physics]] (though notably in [[AQFT]] there are results that re-extract at least parts of this data from the axiomatic QFT, for instance the [[Doplicher-Roberts reconstruction theorem]] which extract the [[global gauge group]] from the [[local net of quantum observables]]).

There are in turn two formalizations of the notion of [[quantization]]: _algebraic [[deformation quantization]]_ and _[[geometric quantization]]_. In the latter one speaks of _[[prequantization]]_ when referring to a precursor step to the actual quantization step, in which the [[symplectic form]] on [[phase space]] is lifted from to [[differential cohomology]], hence to a [[prequantum bundle]]. But in the context of [[higher geometry]] and [[higher geometric quantization]] this prequantization step is already part of the data of the [[Lagrangian]] itself: an [[extended Lagrangian]] already encodes not just the [[action functional]] but also the [[prequantum bundle]] and all the [[prequantum n-bundle|prequantum (n-k)-bundles]] in each [[dimension]] $k$. The action functional itself is the _[[prequantum 0-bundle]]_  in this context.

Therefore, in the refined picture of [[higher geometry]]/[[extended quantum field theory]] it makes good sense to refer in a unified way to **prequantum field theory** for all of the data related to [[Lagrangians]] that is not yet the final [[quantum field theory]]. 

In particular, an **extended prequantum field theory** of [[dimension]] $n$ is a rule that assigns

* to every (suitably [[orientation|oriented]]) [[closed manifold]] of [[dimension]] $k$ a [[prequantum n-bundle|prequantum (n-k)-bundle]]

* to every (suitably [[orientation|oriented]]) [[compact topological space|compact]] [[manifold with boundary]] $\Sigma_k$ a [[section]] of the prequantum $(n-k+1)$-bundle assigned to the [[boundary]] $\partial \Sigma_k$ and pulled back to the space of fields over $\Sigma_k$

such that this data is related suitably under [[transgression]].

The actual [[extended quantum field theory]] would be obtained from such a data by passing from the assignment of a given prequantum $(n-k)$-bundle to that of the [[n-vector space|(n-k)-vector space]] of [[polarization|polarized]] [[sections]] of a suitable [[associated infinity-bundle|associated]] [[fiber infinity-bundle|fiber bundle]].

This is summarized in the following table:

[[!include extended prequantum field theory - table]]


### Higher gauge fields
 {#HigherGaugeFields}


Beyond the [[prequantum n-bundles]] involved in any [[extended prequantum field theory]], there are various [[theory (physics)|theories]] in physics that involve [[field (physics)|fields]] which themselves are already given by higher geometric structure, notably [[higher gauge fields]] given by [[connection on an infinity-bundle|higher connections]] on [[principal infinity-bundle|higher principal bundles]]. These arise notably in higher dimensional [[supergravity]] [[theory (physics)|theories]] and their [[UV-completion]]: [[string theory]]. 

The first example along these lines is the [[Kalb-Ramond field]] or [[B-field]], which is a higher order version of the [[electromagnetic field]]. In order to fully capture the nature of these fields, one needs to describe them in higher geometry. Notably [[quantum anomaly]] cancellation conditions can lead to fairly intricate structures of the [[moduli infinity-stacks]] of such fields. For instance anomaly-free [[heterotic string theory|heterotic]]  [[background gauge fields]] are given by moduli 2-stacks of [[twisted differential string structures]]. 

[[!include table of branes]]


## Related pages

* [[geometry of physics]]

* [[fiber bundles in physics]]

* [[higher category theory and physics]]

* [[string theory FAQ]]

* [[twisted smooth cohomology in string theory]]

* [[motives in physics]]

* [[Hilbert's sixth problem]]

* [[model theory and physics]]

* [[L-infinity algebras in physics]]

* [[motivation for sheaves, cohomology and higher stacks]]

* [[applications of (higher) category theory]]

* [[motivation for higher differential geometry]]

* [[motivation for cohesion]]



## References

The basic relation between [[foliation]] theory and [[Lie groupoid]]-theory is discussed in 

* [[Ieke Moerdijk]], [[Janez Mrčun]], _Introduction to foliations and Lie groupoids_, Cambridge Studies in Advanced Mathematics __91__, 2003. x+173 pp. ISBN: 0-521-83197-0
 {#MoerdijkMrcun}

The identification of [[orbifolds]] as (proper) [[etale Lie groupoids]] is due to

* [[Ieke Moerdijk]], [[Dorette Pronk]], _Orbifolds, sheaves and groupoids_, K-theory 12 3-21 (1997) ([pdf](http://www.math.colostate.edu/~renzo/teaching/Orbifolds/pronk.pdf))
  {#MoerdijkPronk}

A discussion of how [[∞-Lie theory|∞-Lie theoretic]] [[deformation theory]] neatly captures various traditional theorems is in

* [[Domenico Fiorenza]], [[Elena Martinengo]], _A short note on ∞-groupoids and the period map for projective manifolds_, Publications of the nLab [[publications:FiorenzaMartinengo2012|vol. 2 no. 1]] (2012) 

For a survey of how higher differential geometry serves to capture subtle aspects of [[prequantum field theory]] see

* _[[schreiber:A higher stacky perspective on Chern-Simons theory]]_ 
 {#FSS}

(...)

[[!redirects higher differential geometry applied to plain differential geometry]]
