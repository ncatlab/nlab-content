[[!redirects higher differential geometry applied to plain differential geometry]]

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

First we list some examples of how tools from [[higher differential geometry]] help to understand and resolve problems in plain traditional [[differential geometry]]:

* _[Applications of higher DG to plain DG](#ApplicationsOfHigherDGToPlanDG)_

However, much of the genuine motivation for developing [[higher differential geometry]] came and increasingly comes from structures in fundamental [[physics]], in [[quantum field theory]] and [[string theory]], which are intrinsically of [[higher geometry|higher geometric]] nature, hence for which no adequate description in plain [[differential geometry]] even exists (this is in fact already true for traditional local gauge theory, see [below](#FieldBundles)). 

This we disuss in 

* [Motivation of higher DG from physics](#MotivationOfHigherDGFromPhysics)


## Applications of higher DG to plain DG
{#ApplicationsOfHigherDGToPlanDG}

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

   Cartan had originally encoded the [[partial differential equation|PDEs]] whose integration leads ot foliation by "[[exterior differential systems]]". These are equivalently ([[Chevalley-Eilenberg algebras]]) of [[L-∞ algebroids]]. The entire theory of integration is thereby part of higher [[Lie theory]] -- [[infinity-Lie theory]]. 

### Poisson and symplectic geometry
 {#PoissonGeometry}

A subtopic of this is [[Poisson geometry]], where the foliation is by [[symplectic leaves]]. A fundamental problem in Poisson geometry was the [[deformation quantization]] of [[Poisson manifolds]]. 

   The [[formal deformation quantization]] problem was solved by [[Kontsevich]], which earned in a Fields medal. [[Cattaneo]] and [[Felder]] then showed that his formula for the [[star product]] is naturally understood as an [[3-point function]] of the [[Poisson sigma model]], a [[sigma-model]] [[QFT]] whose [[target space]] is the [[Poisson Lie algebroid]] of the given Poisson manifod. 

   The strengthening of this to the [[strict deformation quantization]] problem for a large class of cases was then established by forming the [[convolution algebra]] of sections of the [[prequantum bundle|prequantization]] of the [[symplectic groupoid]] with [[Lie integration|Lie integrates]] the [[Poisson Lie algebroid]].

   (In [[QFT]] the shift into [[higher geometry]] witnessed in both these proofs is a special case of what is known as the [[holographic principle]]: the 0-categorical structure of Poisson manifolds is quantized via the 1-categorical strucure of [[Poisson Lie algebroids]] and [[symplectic groupoids]].)

The [[symplectic groupoid]] that induces the [[strict deformation quantization]] of a Poisson manifold also solves its classical desingularization problem, its _[[symplectic realization]]_.
For any [[symplectic groupoid]] $\Sigma$ with base a [[Poisson manifold]] $P$ the target map is a symplectic realization of $P$ and  the source map is a symplectic realization  of the opposite structure. Thus $\Sigma$ with its symplectic structure may be regarded as a desingularization of  $P$ with its Poisson structure. Since the [[symplectic groupoid]] is the [[Lie integration]] of the [[Poisson Lie algebroid]] of the Poisson manifold, symplectic realization is reduced to a problem in [[Lie theory]].


### Deformation theory
 {#DeformationTheory}

Apart from these Poisson structures and [[symplectic structures]], differential geoemtry studies many other kinds of smooth structures on [[smooth manifolds]], such as [[complex structures]] in [[complex geometry]]. The classification of these structures in each case is [[infinitesimal space|infinitesimally]] given by [[deformation theory]]. Since seminal work referenced at _[[model structure for L-∞ algebras]]_ it is known that deformation theory is essentially equivalently the study of [[L-∞ algebra]] in [[∞-Lie theory]]. Classical theorems in complex differential geometry such as the discussion of [[period maps]] find their natural formulation in this context. This is amplified in  ([Fiorenza-Martinengo2012](#FiorenzaMartinengo)).

### Orbifolds
 {#Orbifolds}

Almost as basic to traditional differential geometry as [[manifolds]] are [[orbifold]], which incorporate non-free [[actions]] into the theory. Notably the [[moduli spaces]] arising in differential geometry tend to be orbifolds instead of manifolds. 

But ordifold are equivalently a [[proper Lie groupoid|proper]] [[étale Lie groupoid]].  (This relation is for some reason more famous in algebraic geometry, where the &#233;tale Lie groupoids are called [[Deligne-Mumford stacks]].)

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

## Motivation of higher DG from physics
 {#MotivationOfHigherDGFromPhysics}

... _[[geometry of physics]]_ ...


## Related pages

* [[motivation for sheaves, cohomology and higher stacks]]

* [[applications of (higher) category theory]]

* [[higher category theory and physics]]

* [[motivation for cohesion]]

## References

The basic relation between [[foliation]] theory and [[Lie groupoid]]-theory is discussed in 

* [[Ieke Moerdijk]], [[Janez Mr?un]], _Introduction to foliations and Lie groupoids_, Cambridge Studies in Advanced Mathematics __91__, 2003. x+173 pp. ISBN: 0-521-83197-0
 {#MoerdijkMrcun}

The identification of [[orbifolds]] as (proper) [[etale Lie groupoids]] is due to

* [[Ieke Moerdijk]], [[Dorette Pronk]], _Orbifolds, sheaves and groupoids_, K-theory 12 3-21 (1997) ([pdf](http://www.math.colostate.edu/~renzo/teaching/Orbifolds/pronk.pdf))
  {#MoerdijkPronk}

A discussion of how [[∞-Lie theory|∞-Lie theoretic]] [[deformation theory]] neatly captures various traditional theorems is in

* [[Domenico Fiorenza]], [[Elena Martinengo]], _A short note on ∞-groupoids and the period map for projective manifolds_, Publications of the nLab [[publications:FiorenzaMartinengo2012|vol. 2 no. 1]] (2012) 


(...)
