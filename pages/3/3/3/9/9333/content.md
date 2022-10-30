
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

This page lists examples of how [[higher differential geometry]] helps with understanding plain [[differential geometry]].

## Examples

### Foliations and PDEs

At the roots of differential geometry, prominent in the original work of [[Eli Cartan]], is [[foliation]] theory, arising in the integration of [[partial differential equations]]. 

   In the context of [[Lie groupoid]] theory, foliations have a classification -- a [[moduli stack]]: the [[Haefliger groupoid]]. The textbook ([Moerdijk-Mrcun](#MoerdijkMrcun)) discusses foliation theory from this perspective. The _[[Haefliger theorem]]_ which classifies foliations on open manifolds is proven by way of the [[Haefliger groupoid]].

   Cartan had originally encoded the [[partial differential equation|PDEs]] whose integration leads ot foliation by "[[exterior differential systems]]". These are equivalently ([[Chevalley-Eilenberg algebras]]) of [[L-∞ algebroids]]. The entire theory of integration is thereby part of higher [[Lie theory]] -- [[infinity-Lie theory]]. 

### Poisson geometry

A subtopic of this is [[Poisson geometry]], where the foliation is by [[symplectic leaves]]. A fundamental problem in Poisson geometry was the [[deformation quantization]] of [[Poisson manifolds]]. 

   The [[formal deformation quantization]] problem was solved by [[Kontsevich]], which earned in a Fields medal. [[Cattaneo]] and [[Felder]] then showed that his formula for the [[star product]] is naturally understood as an [[3-point function]] of the [[Poisson sigma model]], a [[sigma-model]] [[QFT]] whose [[target space]] is the [[Poisson Lie algebroid]] of the given Poisson manifod. 

   The strengthening of this to the [[strict deformation quantization]] problem for a large class of cases was then established by forming the [[convolution algebra]] of sections of the [[prequantum bundle|prequantization]] of the [[symplectic groupoid]] with [[Lie integration|Lie integrates]] the [[Poisson Lie algebroid]].

   (In [[QFT]] the shift into [[higher geometry]] witnessed in both these proofs is a special case of what is known as the [[holographic principle]]: the 0-categorical structure of Poisson manifolds is quantized via the 1-categorical strucure of [[Poisson Lie algebroids]] and [[symplectic groupoids]].)

The [[symplectic groupoid]] that induces the [[strict deformation quantization]] of a Poisson manifold also solves its classical desingularization problem, its _[[symplectic realization]]_.
For any [[symplectic groupoid]] $\Sigma$ with base a [[Poisson manifold]] $P$ the target map is a symplectic realization of $P$ and  the source map is a symplectic realization  of the opposite structure. Thus $\Sigma$ with its symplectic structure may be regarded as a desingularization of  $P$ with its Poisson structure. Since the [[symplectic groupoid]] is the [[Lie integration]] of the [[Poisson Lie algebroid]] of the Poisson manifold, symplectic realization is reduced to a problem in [[Lie theory]].


### Deformation theory

Apart from these Poisson structures and [[symplectic structures]], differential geoemtry studies many other kinds of smooth structures on [[smooth manifolds]], such as [[complex structures]] in [[complex geometry]]. The classification of these structures in each case is [[infinitesimal space|infinitesimally]] given by [[deformation theory]]. Since seminal work referenced at _[[model structure for L-∞ algebras]]_ it is known that deformation theory is essentially equivalently the study of [[L-∞ algebra]] in [[∞-Lie theory]]. Classical theorems in complex differential geometry such as the discussion of [[period maps]] find their natural formulation in this context. This is amplified in  ([Fiorenza-Martinengo2012](#FiorenzaMartinengo)).

### Orbifolds

Almost as basic to traditional differential geometry as [[manifolds]] are [[orbifold]], which incorporate non-free [[actions]] into the theory. Notably the [[moduli spaces]] arising in differential geometry tend to be orbifolds instead of manifolds. 

But ordifold are equivalently a [[proper Lie groupoid|proper]] [[étale Lie groupoid]].  (This relation is for some reason more famous in algebraic geometry, where the &#233;tale Lie groupoids are called [[Deligne-Mumford stacks]].)

### Lie integration

[[Lie integration]] of anything more general than a finite-dimensional [[Lie algebra]] in general goes out of the real of [[Lie groups]]. Local brackets = [[Lie algebroids]] integrate to [[Lie groupoids]] and 
infinite-dimensional Lie algebras in general to [[Lie 2-groups]].

### Derived differential geometry

[[derived differential geometry]] allows to resolve many otherwise singular limit/intersection constructions. Modern [[variational calculus]] in terms of [[jet bundle]] ("[[D-geometry]]") is formulated this way, as is [[symplectic reduction]] and the unification of both in the [[BV-BRST formalism]].

## Related pages

* [[applications of (higher) category theory]]

* [[higher category theory and physics]]

## References

The basic relation between [[foliation]] theory and [[Lie groupoid]]-theory is discussed in 

* [[Ieke Moerdijk]], [[Janez Mr?un]], _Introduction to foliations and Lie groupoids_, Cambridge Studies in Advanced Mathematics __91__, 2003. x+173 pp. ISBN: 0-521-83197-0
 {#MoerdijkMrcun}

A discussion of how [[∞-Lie theory|∞-Lie theoretic]] [[deformation theory]] neatly captures various traditional theorems is in

* [[Domenico Fiorenza]], [[Elena Martinengo]], _A short note on ∞-groupoids and the period map for projective manifolds_, Publications of the nLab [[publications:FiorenzaMartinengo2012|vol. 2 no. 1]] (2012) 


(...)
