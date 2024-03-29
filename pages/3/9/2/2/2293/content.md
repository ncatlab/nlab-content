
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Higher geometry
+--{: .hide}
[[!include higher geometry - contents]]
=--
#### Higher algebra
+--{: .hide}
[[!include higher algebra - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

_Derived algebraic geometry_ is the specialization of [[higher geometry]] and [[homotopical algebraic geometry]] to the [[(infinity,1)-category]] of [[simplicial commutative rings]] (or sometimes, coconnective commutative [[dg-algebras]]).
Hence it is a generalization of ordinary [[algebraic geometry]] where instead of [[commutative rings]], [[derived schemes]] are locally modelled on [[simplicial commutative rings]].

Derived algebraic geometry is the correct setting for certain problems arising in [[algebraic geometry]] that involve [[intersection theory]] and [[deformation theory]] (see below).

## Terminology

Sometimes the term _derived algebraic geometry_ is also used for the related subject of [[spectral algebraic geometry]], where [[commutative ring spectra]] are used instead of [[simplicial commutative rings]].  Sometimes it may also refer to the subject of [[derived noncommutative algebraic geometry]].

## Motivation

There are several motivations for the study of derived algebraic geometry.

1.  The [[hidden smoothness principle]] of [[Maxim Kontsevich]], which conjectures that in classical [[algebraic geometry]], the non-[[smoothness]] of certain [[moduli spaces]] is a consequence of the fact that they are in fact truncations of [[derived moduli stacks]] (which are quasi-[[smooth]]).

1.  [[intersection theory|Intersection theory]]: a [[geometric]] interpretation of the [[Serre intersection formula]] for non-transverse [[intersections]].

1.  [[deformation theory|Deformation theory]]: a [[geometric]] interpretation of the [[cotangent complex]]: the "total space" of the cotangent complex $\mathbb{L}_X$ of $X$ makes sense as an object of derived algebraic geometry (a [[derived stack]]), namely it can be regarded as a derived vector bundle which specializes to the [[cotangent bundle]] $T^*X$ when $X$ is smooth.

For more detail on the final two points, see [(Vezzosi, 2011)](#VezzosiWhatIs).

## History

The idea of developing a theory of schemes where structure sheaves are sheaves of dg-algebras was first proposed by [[Maxim Kontsevich]]. The first rigorous approach to such a theory was via [[dg-schemes]], introduced by  [[Ionut Ciocan-Fontanine]] and [[Mikhail Kapranov]], who used it to construct the first examples of [[derived moduli spaces]] (derived [[Hilbert scheme]] and derived [[Quot scheme]]).  However, this theory was relatively restrictive because dg-schemes were equipped with an embedding into an ambient smooth scheme by definition (hence in particular one could not model the correct notion of morphisms of derived schemes in this language), and because dg-algebras need to be replaced by [[simplicial commutative rings]] in positive or mixed characteristic.

[[Bertrand Toen]] and [[Gabriele Vezzosi]] developed [[homotopical algebraic geometry]], which is [[algebraic geometry]] in any [[HAG context]], i.e. over any [[symmetric monoidal model category]] satisfying certain assumptions.  As special cases they recover the [[algebraic geometry]] of [[Grothendieck]] and the [[higher stacks]] of [[Carlos Simpson]], and also develop new theories of [[derived algebraic geometry]], [[complicial algebraic geometry]], and [[brave new algebraic geometry]].

In his thesis [[Jacob Lurie]] also developed fundamentals of derived algebraic geometry, using the language of [[structured (infinity,1)-toposes]] where [[Bertrand Toen|Toen]]-[[Gabriele Vezzosi|Vezzosi]] used [[model toposes]].  He also developed a version of derived algebraic geometry which is locally modelled on [[E-∞ rings]], called [[spectral algebraic geometry]].
 
## Terminology "derived" versus "$\infty$-"

The adjective "derived" means pretty much the same as the "$\infty$-" in [[∞-category]], so this is higher algebraic geometry in the sense being locally represented by higher algebras. The word stems from the use of "derived" as in [[derived functor]]. This came from the study of derived moduli problem. Namely to parametrize the moduli, one first looks at some space of "cochains" which are candidates for structures to parametrize. then one cuts those which indeed satisfy the axioms ("equations") for the structures. Satisfying these equations is a limit-type construction, hence left exact and one is lead to right derived functors to improve;
exactness on the right; this leads to use cochain complexes.
The obtained moduli is too big as there are many isomorphic structures, so one needs to quotient by the automorphisms; this is a colimit type construction hence right exact. The improved quotient is the left derived functor, what is obtained by passing to stacks. 


## Definitions

### structured $(\infty,1)$-toposes ##

In [Lurie, Structured spaces](#LurieStructured) a definition of [[derived algebraic scheme]] and [[derived Deligne-Mumford stack]] is given in the wider context of [[generalized scheme]]s realized as locally affine [[structured (∞,1)-topos]]es.

See these links for more details.

+-- {: .num_remark}
###### Remark (derived scheme are $(\infty,1)$-toposes)

This definition is based on the observation that it is a deficiency of the ordinary definition of [[scheme]] to demand that underlying a scheme is a [[topological space]] and that a better definition is obtained by demanding it to have an underlying [[locale]]. But a [[locale]] is a [[0-topos]]. This motivates then the definition of a [[generalized scheme]] as a (locally affine, [[structured (infinity,1)-topos|structured]]) [[(∞,1)-topos]]. 

=--

## Relation to derived noncommutative geometry
 {#RelationToDerivedNoncommutativeGeometry}

Under some conditions, [[derived schemes]] $X$ in the sense of ([[Structured Spaces|Lurie, Structured Spaces]]) are faithfully encoded by their [[stable (∞,1)-categories]] $QCoh(X)$ of [[quasicoherent sheaves]]. This is the content of [[Tannaka duality for geometric stacks]], ([[Quasi-Coherent Sheaves and Tannaka Duality Theorems|Lurie, Quasi-Coherent Sheaves and Tannaka Duality Theorems]]). Therefore one can turn this around and declare that a suitable [[stable (∞,1)-category]] $\mathcal{A}$ which is not of the form $QCoh(X)$ for an actual [[derived scheme]] $X$ represents a generalized, "noncommutative" derived scheme. This is much like a [[2-category theory]] or rather [[(∞,2)-category]] theory analog of how in [[algebraic geometry]] the opposite of the category of [[monoids]] (algebras) is regarded as a category of generalized spaces. This might be (and has been) called _[[2-algebraic geometry]]_.

Accordingly, one can decide to regard the [[opposite (∞,1)-category]] of suitable (e.g. [[monoidal (∞,1)-category|monoidal]]) [[stable (∞,1)-categories]]  as being a category of "noncommutative derived schemes". This is effectively the perspective on [[noncommutative algebraic geometry]] that [[Maxim Kontsevich]] has been promoting.

Often and traditionally, all this is expressed in terms of certain presentations for these [[stable (∞,1)-categories]] by [[triangulated category|triangulated]] [[derived categories]] or better, [[dg-enhancement|enhancements]] as [[dg-categories]].

In this fashion then in [[derived noncommutative algebraic geometry]], a [[space]] is by definition a [[dg-category]] that is smooth and proper in an appropriate sense.  The relation between [[noncommutative algebraic geometry]] and [[derived algebraic geometry]] may then be summed up by the adjunction
  $$ Pf : \DSt(k)^{op} \rightleftarrows NCSp(k) : \mathcal{M}_- $$
where $Pf(X)$ denotes the [[dg-category]] of [[perfect complexes]] on the [[derived stack]] $X$, and $\mathcal{M}_\mathcal{C}$ denotes the [[derived moduli stack of objects in a dg-category|derived moduli stack of objects]] in the [[dg-category]] $\mathcal{C}$.  See [[derived moduli stack of objects in a dg-category]] for details.

## Related concepts

* [[homotopical algebraic geometry]]
* [[E-∞ geometry]]
* [[dg-geometry]]
* [[spectral algebraic geometry]]
* [[brave new algebraic geometry]]
* [[higher stacks]]
* [[higher differential geometry]]
* [[derived category of coherent sheaves]]
* [[derived noncommutative algebraic geometry]]

## References 

(For references on [[dg-schemes]], the historical precursor to [[derived schemes]], see there.)

The main references are

* [[Jacob Lurie]], [[Derived Algebraic Geometry]]

* {#LurieStructured} [[Jacob Lurie]], _[[structured (∞,1)-topos|Structured Spaces]]_


* {#ToenVezzosi04} [[Bertrand Toën]], [[Gabriele Vezzosi]], _Homotopical algebraic geometry II: geometric stacks and applications_, Memoirs of the AMS **193** (2008) &lbrack;[arXiv:math/0404373](http://arxiv.org/abs/math/0404373), [ams:memo-193-902](https://bookstore.ams.org/memo-193-902)&rbrack;


* {#TV-HAG-to-DAG} [[Bertrand Toën]], [[Gabriele Vezzosi]], _From HAG to DAG: derived moduli stacks_, in Axiomatic, enriched and motivic homotopy theory, 173--216,
NATO Sci. Ser. II Math. Phys. Chem., 131, Kluwer (2004) &lbrack;[math.AG/0210407](http://arxiv.org/abs/math/0210407)&rbrack;
 

The following notes deal with the theory modelled on coconnective [[commutative dg-algebras]].

* [[Dennis Gaitsgory]], _Notes on geometric Langlands: stacks_, [pdf](http://www.math.harvard.edu/~gaitsgde/GL/Stackstext.pdf).

* J. Eugster and J. P. Pridham. _An introduction to derived (algebraic) geometry_.
[arXiv](http://arxiv.org/abs/2109.14594).

The following notes deal with the theory modelled on [[E-infinity ring spectra]] ([[E-infinity geometry]]):

* [[Clark Barwick]], _Applications of derived algebraic geometry to homotopy theory_, lecture notes, mini-course in Salamanca, 2009, [pdf](https://dl.dropboxusercontent.com/u/1741495/papers/salamanca.pdf).

See also the surveys

* [[Bertrand Toën]], _Higher and derived stacks: a global overview_, In: _Algebraic Geometry Seattle 2005_, Proceedings of Symposia in Pure Mathematics, Vol. 80.1, AMS 2009 ([arXiv:math/0604504](http://arxiv.org/abs/math/0604504), [doi:10.1090/pspum/080.1](https://doi.org/10.1090/pspum/080.1))

* {#VezzosiWhatIs} [[Gabriele Vezzosi]], _What is a derived stack?_, 2011, [pdf](http://www.ams.org/notices/201107/rtx110700955p.pdf).


* [[Bertrand Toën]], _Derived algebraic geometry_, [arxiv/1401.1044](http://arxiv.org/abs/1401.1044)

Discussion of [[derived noncommutative algebra]] over [[E-n algebras]] is in 

* [[John Francis]], _Derived algebraic geometry over $\mathcal{E}_n$-Rings_ ([pdf](http://math.northwestern.edu/~jnkf/writ/thezrev.pdf))

* [[John Francis]], _The tangent complex and Hochschild cohomology of $\mathcal{E}_n$-rings_ ([pdf](http://math.northwestern.edu/~jnkf/writ/cotangentcomplex.pdf))

