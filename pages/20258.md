
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Differential geometry
+--{: .hide}
[[!include synthetic differential geometry - contents]]
=--
#### Spheres
+--{: .hide}
[[!include spheres -- contents]]
=--
=--
=--



#Contents#
* table of contents
{:toc}

## Idea

A [[topological manifold|topological]] [[7-sphere]] equipped with an [[exotic smooth structure]] is called an _exotic 7-sphere_.

## Milnor's construction
 {#Construction}

[Milnor (1956)](#Milnor1956) gave the first examples of exotic smooth structures on the [[7-sphere]], finding at least seven. 

The [[exotic 7-spheres]] constructed in [Milnor 1956](#Milnor1956) are all examples of [[fibre bundles]] over the [[4-sphere]] $S^4$ with [[fibre]] the [[3-sphere]] $S^3$, with [[structure group]] the [[special orthogonal group]] [[SO(4)]] (see also at _[[8-manifold]]_ the section _[With exotic boundary 7-spheres](8-manifold#ExoticBoundary7Spheres)_):

By the classification of bundles on spheres via the [[clutching construction]], these correspond to [[homotopy classes]] of maps $S^3 \to SO(4)$, i.e. elements of $\pi_3(SO(4))$. From the table at [orthogonal group -- Homotopy groups](orthogonal+group#HomotopyGroups), this latter group is $\mathbb{Z}\oplus\mathbb{Z}$. Thus any such bundle can be described, up to [[isomorphism]], by a [[pair]] of [[integers]] $(n,m)$. When $n+m=1$, then one can show there is a [[Morse function]] with exactly two [[critical points]] on the total space of the bundle, and hence this 7-manifold is [[homeomorphic]] to a sphere.

The  [[fractional first Pontryagin class]] $\frac{p_1}{2} \in H^4(S^4) \simeq \mathbb{Z}$ of the bundle is given by $n-m$. Milnor constructs, using [[cobordism theory]] and [[Hirzebruch's signature theorem]] for [[8-manifolds]], a [[modulo]]-7 [[diffeomorphism]] [[invariant]] of the manifold, so that it is the standard 7-sphere precisely when $\frac{p_1}{2}^2 -1 = 0 (mod\,7)$.

By using the [[connected sum]] operation, the set of smooth, non-diffeomorphic structures on the $n$-sphere has the structure of an [[abelian group]]. 
For the [[7-sphere]], it is the [[cyclic group]] $\mathbb{Z}/{28}$ and Brieskorn (1966) found the generator $\Sigma$ so that $\underbrace{\Sigma\#\cdots\#\Sigma}_28$ is the standard sphere.

Review includes ([Kreck 10, chapter 19](#Kreck10), [McEnroe 
15](#McEnroe15), [Joachim-Wraith](#JoachimWraith)). 

## Examples

* [[Gromoll-Meyer sphere]]


## Properties

### As near-horizon geometries of black M2-branes
 {#AsNearHorizonGeometriesOfBlackM2Branes}


From the point of view of [[M-theory on 8-manifolds]], these [[8-manifolds]] $X$ with (exotic) [[7-sphere]] [[boundaries]] in [Milnor's construction](#Construction) correspond to [[near horizon limits]] of [[black brane|black]] [[M2 brane]] spacetimes $\mathbb{R}^{2,1} \times X$, where the [[M2-branes]] themselves would be sitting at the center of the [[7-spheres]] (if that were included in the spacetime, see also [[Dirac charge quantization]]).

([Morrison-Plesser 99, section 3.2](#MorrisonPlesser99), [[schreiber:Twisted Cohomotopy implies M-theory anomaly cancellation|FSS 19, 4.6]]))



## References

### General

* {#Milnor1956} [[John Milnor]], _On manifolds homeomorphic to the 7-sphere_, Annals of Mathematics 64 (2): 399&#8211;405 (1956) ([pdf](https://www.maths.ed.ac.uk/~v1ranick/papers/exotic.pdf), [doi:10.1142/9789812836878_0001](https://doi.org/10.1142/9789812836878_0001))



* {#Kreck10} [[Matthias Kreck]], chapter 19 of _Exotic 7-spheres_ of  _Differential Algebraic Topology -- From Stratifolds to Exotic Spheres_, AMS 2010

* {#McEnroe15} Rachel McEnroe, _Milnor' construction of exotic 7-spheres_, 2015 ([pdf](http://math.uchicago.edu/~may/REU2015/REUPapers/McEnroe.pdf))

* {#JoachimWraith} [[Michael Joachim]], D. J. Wraith, _Exotic spheres and curvature_ ([pdf](https://ivv5hpp.uni-muenster.de/u/joachim/exo.pdf))

* [[Niles Johnson]], _Visualizing 7-manifolds_, 2012 ([nilesjohnson.net/seven-manifolds.html](https://nilesjohnson.net/seven-manifolds.html))

* {#CrowleyEscher03} [[Diarmuid Crowley]], [[Christine Escher]], _A classification of $S^3$-bundles over $S^4$_, Differential Geometry and its Applications Volume 18, Issue 3, May 2003, Pages 363-380 (<a href="https://doi.org/10.1016/S0926-2245(03)00012-3">doi:10.1016/S0926-2245(03)00012-3</a>))

See also

* Wikipedia, _[Exotic sphere](https://en.wikipedia.org/wiki/Exotic_sphere)_

### In M-theory

* {#MorrisonPlesser99} [[David Morrison]], [[M. Ronen Plesser]], section 3.2 of _Non-Spherical Horizons, I_, Adv. Theor. Math. Phys. 3:1-81, 1999 ([arXiv:hep-th/9810201](https://arxiv.org/abs/hep-th/9810201))


[[!redirects exotic 7-spheres]]


[[!redirects Brieskorn sphere]]
[[!redirects Brieskorn spheres]]

[[!redirects Milnor sphere]]
[[!redirects Milnor spheres]]

