
<div class="rightHandSide toc">
[[!include physicscontents]]
</div>

#Contents#
* automatic table of contents goes here
{:toc}


## Idea

Recall that a [[sigma-model]] is a [[quantum field theory]] that is induced from certain [[differential geometry|differential geometric]] and [[differential cohomology|differential cohomological]] data, to be thought of as describing the propagation of quantum objects of dimension $d$ in some space.

The operation of **T-duality** is a map that interchanges pairs of such geometric data for 2-dimensional [[conformal field theory]] [[sigma-model]]s, such that the induced QFTs are equivalent.


More specifically the space of [[differential geometry|differential geometric]] data consisting of

* a smooth [[manifold]] $X$ 

* equipped with the structure of a $k$-torus [[bundle]] $X \simeq Y \times T^k$; -- the total space of this bundle modelling [[spacetime]];

* and equipped with a [[Riemannian metric]] $g$ -- modelling the field of [[gravity]];

* and a $U(1)$-[[gerbe]] with connection $G$; -- modelling the [[Kalb-Ramond field]]

admits a certain operation that, roughly, inverts the Riemannian circumference of the torus fibers and mixes the metric with the gerbe data. This is the operation called **T-duality**.

It was noticed originally in the study of [[conformal field theory|conformal field theories]] in the context of [[string theory]]: the conformal field theory [[sigma-model]]s with target space $X$ turn out to be equivalent as [[quantum field theory|quantum field theories]] for T-dual backgrounds $(X,g,G)$ and $(X',g',G')$ (at least to the approximate degree to which these are realized as full CFTs in the first place).

Further generalisations let $X$ be a nontrivial torus bundle, but the T-dual is then generically a bundle of [[noncommutative torus|non-commutative tori]]. (cite Mathai, Rosenberg and Hannabus)

## Path integral heuristics deriving T-duality

The state of the art is still mostly that [[sigma-model]] [[QFT]]s are
handled in terms of the [[path integral]] formulation, where the 
[[action functional]] is a natural [[functional]] on the space of 
differential geometric background data.

We indicate how one can see T-duality from formal manipulaitons
of the path integral for the [[string theory|string]].

...


## Topological T-duality 

It turns out to be possible and useful to discuss just the _topological_ aspects of T-duality, meaning all the aspects that depend on the $X$ as a [[topological space]], on the topological class of the [[gerbe]] and of its 3-form curvature, but not on the [[Riemannian metric]] and not on the precise connection on the gerbe (there may be several inequivalent one for a given curvature)!

This sub-phenomenon is discussed in more detail at [[topological T-duality]].


## Geometric T-duality in generalized complex geometry {#TdualityIngcg}

Another approach to the study of T-duality takes a somewhat complementary point of view and ignores the  [[Eilenberg-MacLane spectrum|integral cohomology]] class in $H^3(X,\mathbb{Z})$ of the [[gerbe]] but does consider the [[Riemannian metric]].

In this context T-duality is described as an isomorphism of [[standard Courant algebroid]]s. This picture emerged in the study of [[generalized complex geometry]].

### References

T-duality is identified as an [[isomorphism]] of [[standard Courant algebroid]]s in section 4 of

* Cavalcanti, [[Marco Gualtieri|Gualtieri]], _Generalized complex geometry and T-duality_ ([pdf](http://www.math.uu.nl/people/cavalcan/homepage/Research_files/t-duality.pdf))

A discussion of the [[sigma-model]] description of T-duality in this context is in

* Jonas Persson, _T-duality and Generalized Complex Geometry_ ([arXiv](http://arxiv.org/abs/hep-th/0612034))

Further references are

* Willie Carl Merrell, _Application of superspace techniques to effective actions, complex geometry and T-duality in String theory_ ([pdf](http://www.lib.umd.edu/drum/bitstream/1903/6865/1/umi-umd-4355.pdf))

* Peggy Kao, _T-duality and Poisson-Lie T-duality in generalized geometry_ ([pdf](http://tpsrv.anu.edu.au/Members/bouwknegt/Kao.pdf))