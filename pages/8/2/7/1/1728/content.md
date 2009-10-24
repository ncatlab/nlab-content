#Contents#
* automatic table of contents goes here
{:toc}

#Idea#

Recall that an $n$-dimensional [[FQFT]] is a [[symmetric monoidal functor|symmetric monoidal]] $(\infty,n)$-[[n-functor|functor]] from the [[(infinity,n)-category of cobordisms]]. 

$$  
  Z : Bord_n \to C
  \,.
$$

If one replaces plain [[cobordism]]s here with cobordisms that are _colored_ in that they are equipped with certain partitions labeled in a certain index set $Def$, one calls a morphism

$$
  Z : Bord_n^{Def} \to C
$$

a TQFT _with defects_.

The reason is that such a morphism will behave like encoding 

* for each label in $Def$ of codimension 0 regions one ordinary TQFT;

* for each label in $Def$ of codimension 1 data on how to "connect" the two TQFTs on both sides

* etc.

So one may think of the codimension $k$ colors as _defects_ where the TQFT that one is looking at changes its nature.

In particular, when the QFT on one side of the defect is trivial, then the defect behaves like a _boundary condition_ for the remaining QFT. Since at least for $n=2$ QFT such bounary conditions are also called [[brane]]s, defects are also called [[bi-brane]]s.

#Examples#

* An old example is the calss of [[Turaev-Reshetikhin TQFT]], which is a functor on 3-dimensional [[cobordisms]] with codimension 3 and 2 defects. This is supposed to be the would-be result of [[Chern-Simons theory]], where the defect lines are the original [[Wilson lines]] in this context.

* Defects in 2-dimensional [[conformal field theory]] have a long history in real-world application, for instance

  * _Kramers-Wannier duality from conformal defects_

  * Fr&#246;lich, Fuchs, Runkel, Schweigert, _Duality and defects in rational conformal field theory_ ([arXiv](http://arxiv.org/abs/hep-th/0607247))

* Defects in 2-dimension TFT have been studied a lot in the context of genus-0 TFT, where they are described using the language of [[planar algebra]]s. 

  * See the discussion at [Planar Algebras, TFTs with Defects](http://golem.ph.utexas.edu/category/2008/09/planar_algebras_tfts_with_defe.html) for a start.

#Formulation in terms of transformations of TQFTs#

Based on techniques used in his work on the [[2-category of 2-dimensional cobordisms]], [[Chris Schommer-Pries]] shows that a [[TQFT]] with given collection of defects is the same as collection of natural transformations between ordinary [[FQFT|functorial QFTs]] (functors on an [[(infinity,n)-category of cobordisms]]):

* [[Chris Schommer-Pries]], _Tpological Defects and Classification of Local TQFTs in Low Dimension_, [[Oberwolfach Workshop, June 2009 -- Strings, Fields, Topology]] ([pdf](http://sites.google.com/site/chrisschommerpriesmath/Home/Slides-MFO-6-11-09.pdf?attredirects=0))

This in particular connects to the attempt at

* [Towards 2-functorial CFT](http://golem.ph.utexas.edu/category/2007/08/dbranes_from_tin_cans_part_x.html)

to encode the decoration prescription in the FFRS description of [[conformal field theory]] in terms of the components of transformations of the Reshetikhin-Turaev 3d TFT functor.