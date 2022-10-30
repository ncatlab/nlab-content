
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Bundles
+-- {: .hide}
[[!include bundles - contents]]
=--
#### Complex geometry
+--{: .hide}
[[!include complex geometry - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

A [[complex numbers|complex]] [[vector bundle]] over a [[complex manifold]] such that it admits [[transition functions]] that are [[holomorphic functions]].

## Properties

### As complex vector bundles with flat holomorphic connection
 {#AsComplexVectorBundlesWithHolomorphicFlatConnection}

+-- {: .num_theorem #KoszulMalgrangeTheorem}
###### Theorem 
**([[Koszul-Malgrange theorem]])**

Holomorphic vector bundles over a [[complex manifold]] are equivalently [[complex vector bundles]] which are equipped with a holomorphic [[flat connection]]. Under this identification the [[Dolbeault operator]] $\bar \partial$ acting on the [[sections]] of the holomorphic vector bundle is identified with the holomorphic component of the [[covariant derivative]] of the given connection.

The analogous statement is true for generalization of vector bundles to [[chain complexes]] of [[module sheaves]] with [[coherent cohomology]].

=--

For [[complex vector bundles]] over [[complex varieties]] this statement is due to [[Alexander Grothendieck]] and ([Koszul-Malgrange 58](#KoszulMalgrange58)), recalled for instance as ([Pali 06, theorem 1](#Pali06)). It may be understood as a special case of the [[Newlander-Nirenberg theorem]], see ([Delzant-Py 10, section 6](#DelzantPy10)), which also generalises the proof to [[infinite-dimensional manifold|infinite-dimensional]] vector bundles. Over [[Riemann surfaces]], see [below](#OverRiemannSurfaces), the statement was highlighted in ([Atiyah-Bott 83](#AtiyahBott83)) in the context of the [[Narasimhan?Seshadri theorem]]. 

The generalization from [[vector bundles]] to  [[coherent sheaves]] is due to ([Pali 06](#Pali06)). In the genrality of [[(∞,1)-categories of chain complexes]] ([[dg-categories]]) of holomorphic vector bundles the statement is discussed in ([Block 05](#Block05)).

+-- {: .num_remark}
###### Remark

The equivalence in theorem \ref{KoszulMalgrangeTheorem} serves to relate a fair bit of [[differential geometry]]/[[differential cohomology]] with constructions in [[algebraic geometry]]. For instance [[intermediate Jacobians]] arise in [[differential geometry]] and [[quantum field theory]] as [[moduli spaces of flat connections]] equipped with [[symplectic structure]] and [[Kähler polarization]], all of which in terms of [[algebraic geometry]] directly comes down [[moduli spaces]] of [[abelian sheaf cohomology]] with [[coefficients]] in the [[structure sheaf]] (and/or some variants of that, under the exponential exact sequence).

=--
 
### Over Riemann surfaces
 {#OverRiemannSurfaces}

Over [[Riemann surfaces]] holomorphic vector bundles are a central part of the theory of the [[moduli space of flat connections]]. See at _[[Narasimhan-Seshadri theorem]]_.

A key observation here is ([Atiyah-Bott 83, section 7](#AtiyahBott83)), that a $U(n)$-[[principal connection]] induces a holomorphic structure on the [[associated bundle|associated]] [[complex vector bundle]] by taking the $(0,1)$-part of the connection 1-form as the [[Dolbeault operator]]. For review of the statement and its proof see ([Evans, lecture 10](#Evans)).

## Related concepts

* [[Kodaira vanishing theorem]]

* [[Kähler polarization]]

* [[stable vector bundle]]

## References

### General

* Wikipedia, _[holomorphic vector bundle](http://en.wikipedia.org/wiki/Holomorphic_vector_bundle)_

### Relation to complex vector bundles with flat holomorphic connection

The classical statement of theorem \ref{KoszulMalgrangeTheorem} is due to [[Alexander Grothendieck]] and

* {#KoszulMalgrange58} [[Jean-Louis Koszul]], [[Bernard Malgrange]], _Sur certaine structures fibr&#233;es complexes_, arch. mat, vol IX, 1958

Over [[Riemann surfaces]] and in the context of the [[moduli space of flat connections]]:

* {#AtiyahBott83} [[Michael Atiyah]], [[Raoul Bott]], _The Yang-Mills equations over Riemann surfaces_, Philosophical Transactions of the Royal Society of London. Series A, Mathematical and Physical Sciences
Vol. 308, No. 1505 (Mar. 17, 1983), pp. 523-615 ([jstor](http://www.jstor.org/stable/37156), [lighning summary](http://math.stackexchange.com/a/295505/58526))

* {#Evans} [[Jonathan Evans]], _[Aspects of Yang-Mills theory](http://www.homepages.ucl.ac.uk/~ucahjde/yangmills.htm)_, lecture notes, ([lecture 10](http://www.homepages.ucl.ac.uk/~ucahjde/YM-lectures/lecture10.pdf), [lecture 11](http://www.homepages.ucl.ac.uk/~ucahjde/YM-lectures/lecture11.pdf), [lecture 12](http://www.homepages.ucl.ac.uk/~ucahjde/YM-lectures/lecture12.pdf))

Generalization to [[coherent sheaves]] is due to 

* {#Pali06} N. Pali, _Faisceaux $\bar \partial$-cohrents sur les vari&#233;t&#233; complexes_ ( _$\bar \partial$-Coherent sheaves on complex manifolds) Math.
Ann. 336 (2006), no. 3, 571&#8211;615 ([arXiv:math/0305422](http://arxiv.org/abs/math/0305422))

Further Generalization to [[chain complexes]] of holomorphic vector bundles is discussed in 

* {#Block05} [[Jonathan Block]], _Duality and equivalence of module categories in noncommutative geometry I_ ([arXiv:0509284](http://arxiv.org/abs/math/0509284))


in terms of [[Lie infinity-algebroid representations]] of the holomorphic [[tangent Lie algebroid]].

Generalization to [[infinite-dimensional manifold|infinite-dimensional]] vector bundles is in 

* {#DelzantPy10} Thomas Delzant, Pierre Py, _K&#228;hler groups, real hyperbolic spaces and the Cremona group_, Compositio Math. 148, no. 1 (2012), 153--184 ([arXiv:1012.1585](http://arxiv.org/abs/1012.1585))

[[!redirects holomorphic vector bundles]]


[[!redirects holomorphic line bundle]]
[[!redirects holomorphic line bundles]]

[[!redirects holomorphic section]]
[[!redirects holomorphic sections]]