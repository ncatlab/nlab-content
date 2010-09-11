
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Cohomology
+--{: .hide}
[[!include cohomology - contents]]
=--
=--
=--


#Contents#
* automatic table of contents goes here
{:toc}

## Idea

A (smooth) prinicpal bibundle is a (smooth) [[principal bundle]] and notably a [[groupoid principal bundle]] with compatible [[actions]] on both the left and right.

They arise in two related situations: as the objects used to define [[nonabelian bundle gerbe]]s and as [[anafunctor]]-like morphisms between [[Lie groupoid]]s. The former is a special case of the latter. The general concept of [[bundle]] has no action and so there is nothing to do to make it a bibundle.  However, suppose that $G$ is a [[group]] and you are interested in [[G-bundle]]s.  Then a __$G$-bibundle__ is a bundle that is simultaneously a left $G$-bundle and a right $G$-bundle, such that the left and right actions of $G$ commute. This is a bibundle in the first sense. 

A __principal bibundle__ is a [[principal bundle|principal]] $G$-bundle with commuting left and right $G$-actions.

More generally, a __right principal bibundle__ between two groupoids $G$ and $H$ is a set $P$ with a $G$-$H$ [[biaction]] such that the map from $P$ to the objects of $G$ is a surjective submersion and such that the fibers are acted on by $H$ freely and transitively. See [discussion](http://sbseminar.wordpress.com/2007/07/23/a-bicategory-of-groupoids/).

This subsumes the notion of principal  bibundle defined above. A principal $G$-bibundle is the same as __right principal bibundle__ from the Lie groupoid $X$ (thought of as a [[discrete groupoid]] with only identity morphisms) to the underlying groupoid of the [[automorphism 2-group]] $(Aut(G), G)$. See Example 14 of Chris Schommer-Pries _Central Extensions of Smooth 2-Groups and a Finite-Dimensional String 2-Group_ [arXiv:0911.2483](http://arxiv.org/abs/0911.2483/).  

Similarly, let $(H, G)$&#8230; be a [[strict 2-group]]. Then an __$(H, G)$&#8230;-bibundle__ is a (right) principal $G$-bundle with an equivariant map $\phi: P \to H$. See [Murray's talk](http://www.mpim-bonn.mpg.de/digitalAssets/7050_Murray.pdf).

For a [[Lie groupoid]] $G$, a left (right) $G$-bundle $E$ over $X$ (equipped with  $\tau: X \to M$) is a left (right) $G$-action on $E$, and a $G$-invariant map
$\pi: E  \to M$. Then a __$G$-$H$-bibundle__ $E$ is a left $G$-bundle and a right $H$-bundle. See [Morton's talk](http://www.math.uwo.ca/~jmorton9/seminar/gpdrep.pdf).


The description of principal bibundles as maps to a [[2-group]] shows that there is an induced structure of a 2-group on the category of principal bibundles over a space. In fact this holds whenever the muliplication of the target $2$-group is given by a _bibundle_, and this allows the concept of a non-abelian [[bundle gerbe]] to be generalized past the classical setting of strict [[Lie 2-group]]s $(H,G)$. A general discussion occurs in Chris Schommer-Pries' [Central Extensions of Smooth 2-Groups and a Finite-Dimensional String 2-Group](http://arxiv.org/abs/0911.2483/) in section 3.3,  see especially Example 61. 


Now let $G$ and $H$ be Lie groupoids. A [[manifold]] $M$ with a left $G$-action and a right $H$-action which commute, i.e., $(g \cdot m) \cdot h = g \cdot (m \cdot h)$, whenever defined, is called a __smooth $G$-$H$ bibundle__. See Definition 2.8 in _[Stacky Lie Groupoids](http://arxiv.org/abs/math/0702399)_.


## References
* [[Chris Schommer-Pries]] _Central Extensions of Smooth 2-Groups and a Finite-Dimensional String 2-Group_ [arXiv:0911.2483](http://arxiv.org/abs/0911.2483/) 

* [[Michael Murray]], _Bispaces and bibundles_ ([pdf slides](http://www.mpim-bonn.mpg.de/digitalAssets/7050_Murray.pdf))


[[!redirects bibundle]]
[[!redirects bibundles]]
