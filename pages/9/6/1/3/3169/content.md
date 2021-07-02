
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Locality and descent
+--{: .hide}
[[!include descent and locality - contents]]
=--
#### Cohomology
+--{: .hide}
[[!include cohomology - contents]]
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

Higher monadic descent is the generalization of the notion of [[monadic descent]] from [[category theory]] to [[higher category theory]]. It relates to the [[descent]] of [[∞-stacks]] as ordinary monad descent relates to [[stack]]s.

See also [[cohomological descent]].

## Examples

### Amitsur complex, Sweedler corings, Hopf algebroids
 {#AmitsurComplex}

For $\phi \colon B \longrightarrow A$ a [[homomorphism]]
of suitable [[monoids]], there is the corresponding pull-push [[adjunction]] 
([[extension of scalars]] $\dashv$ [[restriction of scalars]]) on [[categories of modules]]


$$
  ((- )\otimes_B A \dashv \phi^\ast )
  \;\colon\;
   Mod_A
    \stackrel{\overset{(-)\otimes_B A}{\leftarrow}}{\underset{\phi^\ast}{\longrightarrow}}
   Mod_B
  \,.
$$

The [[bar construction]] of the corresponding [[monad]] is the corresponding [[Amitsur complex]].

(e.g. [Hess 10, section 6](#Hess10))

## Related concepts

* [[descent]]

  * [[cover]]

  * [[cohomological descent]]

  * [[monadic descent]], 

    * [[Sweedler coring]]

    * **higher monadic descent**

    * [[descent in noncommutative algebraic geometry]]

  * [[descent spectral sequence]]

* [[sheaf]], [[(2,1)-sheaf]], [[2-sheaf]] [[(∞,1)-sheaf]]


## References

### 2-categorical monadic descent

A monadicity theorem for [[2-monad|pseudomonads]] is proved in

* I. J. Le Creurer, F. Marmolejo, E. M. Vitale, _Beck's theorem for pseudo-monads_, J. Pure Appl. Algebra 173 (2002), no. 3, 293--313. 

In [[2-category]]-theory, a notion of 2-[[fibered category|fibered categories]] are defined in Gray's work and then again introduced and discussed at length by Claudio Hermida, who has good ideas on higher n (and I will be trilled to hear once that he found the time to return to the topic and give us good answers). An appendix in

* [[Claudio Hermida]], _Descent on 2-fibrations and strongly 2-regular 2-categories_, Appl. Categ. Structures __12__ (2004), no. 5-6, 427&#8211;459.

is discussing a 2-categorical version of Beck-Chevalley condition needed to compare it with the 2-monadic descent; there is also a version of Beck's theorem sketched there. 

### $(\infty,1)$-categorical monadic descent

A comprehensive treatment in the context of [[(∞,1)-category]]-theory,  general theory of [[(∞,1)-monad]]s and their [[monadicity theorem]] is in

* [[Jacob Lurie]], _Derived algebraic geometry II: Noncommutative algebra_, [math.CT/0702299](http://arxiv.org/abs/math/0702299), Section 3.

later absorbed as

* [[Jacob Lurie]], section 6.2.4 of _[[Higher Algebra]]_

Unfortunately, [[Maxim Kontsevich|Kontsevich]]'s [[monadicity theorem]] (July 2004) which is in the setup of [[A-infinity category|A-∞-categories]], still remains unpublished. The [[triangulated category|triangulated]] version is in Rosenberg's lectures

* [[Alexander Rosenberg|A. L. Rosenberg]], _Topics in noncommutative algebraic geometry, homological algebra and K-theory_, preprint MPIM Bonn 2008-57 [pdf](http://www.mpim-bonn.mpg.de/preblob/3589), page 36-37.

Its proof is based on [[Verdier's abelianization functor]]. 

See also, for another point of view, 

* [[Paul Balmer]], _Descent in triangulated categories_, [pdf](http://www.math.ucla.edu/~balmer/research/Pubfile/Descent.pdf)

Discussion of monadic descent for [[simplicially enriched category|simplicially enriched categories]] is in

* [[Kathryn Hess]], _A general framework for homotopic descent and codescent_, [arXiv/1001.1556](http://arxiv.org/abs/1001.1556)
 {#Hess10}

* [[Kathryn Hess]], [[Brooke Shipley]], _The homotopy theory of coalgebras over a comonad_ ([arXiv:1205.3979](http://arxiv.org/abs/1205.3979))

and for [[quasi-categories]] in 

* [[Emily Riehl]], [[Dominic Verity]], _Homotopy coherent adjunctions and the formal theory of monads_ ([arXiv:1310.8279](http://arxiv.org/abs/1310.8279))
 {#RiehlVerity13}
