

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Quantum field theory
+--{: .hide}
[[!include functorial quantum field theory - contents]]
=--
#### Physics
+-- {: .hide}
[[!include physicscontents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

A **topological quantum field theory** is a [[quantum field theory]] which 
-- as a [[FQFT|functorial quantum field theory]] -- is a functor on a flavor of the  [[(∞,n)-category of cobordisms]] $Bord_n^S$, where the [[n-morphism]]s are [[cobordism]]s without any non-topological further structure $S$ -- for instance no [[Riemannian metric]] structure -- but possibly some "topological structure", such as  [[Spin structure]] or similar.

For more on the general idea and its development, see [[FQFT]] and [[extended topological quantum field theory]]. 


+-- {: .num_remark }
###### Remark

Often topological _quantum_ field theories are just called _topological field theories_ and accordingly the abbreviation TQFT is reduced to TFT. Strictly speaking this is a misnomer, which is however convenient and very common. It should be noted, however, that TQFTs may have classical counterparts which would better deserve to be called TFTs. But they are not usually.

=--

## Non-topological QFTs

In contrast to topological QFTs, non-topological quantum field theories in the [[FQFT]] description are $n$-functors on $n$-categories $Bord^S_n$ whose morphisms are manifolds with extra $S$-structure, for instance

* $S =$ conformal structure $\to$ [[conformal field theory]]

* $S =$ [[Riemannian manifold|Riemannian structure]] $\to$ "euclidean QFT"

* $S =$ [[pseudo-Riemannian metric|pseudo-Riemannian structure]] $\to$ "relativistic QFT"

## Examples

* [[2d TQFT]]

  * [[TCFT]]

  * [[2d Chern-Simons theory]]

* [[3d TQFT]]

  * [[Dijkgraaf-Witten theory]]

  * [[Chern-Simons theory]]

  * [[Reshetikhin-Turaev model]]

  * [[Turaev-Viro model]]

* [[4d TQFT]]

  * [[4d Chern-Simons theory]]

  * [[Yetter model]]  

## Homotopy QFTs

These somehow lie between the previous two types. There is some simple extra structure in the form of a 'characteristic map' from the manifolds and bordisms to a 'background space' $X$. 
In many of the simplest examples, this is taken to be the [[classifying space]] of a group, but this is not the only case that can be considered.  The topic is explored more fully in [[HQFT]]. 

## Related concepts

* [[cohomological field theory]], [[TCFT]]

* [[FQFT]], [[extended topological quantum field theory]]

* [[topological quantum computation]]

## Literature 

An introduction to 2D TQFTs can be found in

* [[Joachim Kock]], _Frobenius algebras and 2D topological quantum field theories_, No. 59 of LMSST, Cambridge University Press, 2003., (full information [here](http://mat.uab.es/~kock/TQFT.html)).

Further literature includes:

* [[Anton Kapustin]], _Topological field theory, higher categories, and their applications_, survey for ICM 2010, [arxiv/1004.2307](http://arxiv.org/abs/1004.2307)

* [[Daniel Freed]], [[Michael Hopkins]], [[Jacob Lurie]], [[Constantin Teleman]], _[[Topological Quantum Field Theories from Compact Lie Groups]]_

On the [[cobordism theorem]]:

* [[Jacob Lurie]], [[On the Classification of Topological Field Theories]]; _TQFT and the Cobordism Hypothesis_ ([video](http://www.ma.utexas.edu/video/dafr/lurie/), [notes](http://www.ma.utexas.edu/users/plowrey/dev/rtg/notes/perspectives_TQFT_notes.html))
* see also [[cobordism hypothesis]] and references therein

* Mark Feshbach, Alexander A. Voronov, _A higher category of cobordisms and topological quantum field theory_, [arxiv/1108.3349](http://arxiv.org/abs/1108.3349) 

* {#Teleman14} [[Constantin Teleman]], _Five lectures on topological field theory_, 2014 ([pdf](http://math.berkeley.edu/~teleman/math/barclect.pdf))

[[!redirects topological quantum field theories]]
[[!redirects TQFT]]
[[!redirects TQFTs]]
[[!redirects TFT]]
[[!redirects TFTs]]

[[!redirects topological field theory]]
[[!redirects topological field theories]]
