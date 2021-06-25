[[!redirects Shrinking wedge of circles]]

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Topology
+--{: .hide}
[[!include topology - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}


## Idea

<div style="float:right;margin:0 10px 10px 0;">
<a href="https://upload.wikimedia.org/wikipedia/commons/thumb/7/71/Hawaiian_earrings.svg/440px-Hawaiian_earrings.svg.png">
<img src="https://upload.wikimedia.org/wikipedia/commons/thumb/7/71/Hawaiian_earrings.svg/440px-Hawaiian_earrings.svg.png" width="160">
</a>
</div>


The [[topological space]] which is the [[union]] of an infinite number of [[circles]] in the [[plane]], of decreasing radius and all sharing exactly one point, has commonly been known as the *Hawaiian earring space* (apparently following [Dudley 61](#Dudley61), though the space appears earlier in [Griffiths 56](#Griffiths56)). Other terminology is “clamshell” (also [Dudley 61](#Dudley61)) or, more recently, “infinite earring” or “shrinking wedge of circles”.


In [[algebraic topology]] this space has been of interest mainly as a counterexample, showing the need for care in hypotheses for a good theory of [[covering spaces]] -- see at *[Properties](#Properties)* below.

<div style="float:right;margin:0 10px 10px 0;">
<a href="https://www.qvc.com/Italian-Silver-Nested-Circles-Dangle-Earrings.product.J482016.html">
<img src="https://ncatlab.org/nlab/files/ItalianNestedCircleEarrings.jpg" width="285"></a>
</div>





## Definition

The (Hawaiian) earring space is the [[topological space]] defined to be the set 

$$
  \bigcup_{n \in \mathbb{N}} \{(x, y) \in \mathbb{R}^2: (x - 1/2^n)^2 + y^2 = 1/2^{2n}\}
$$

endowed with [[subspace topology]] inherited from the [[Euclidean topology]] of the [[plane]] $\mathbb{R}^2$. 

More abstractly: the earring space can be described up to [[homeomorphism]] as the [[one-point compactification]] of a [[coproduct]] (in [[Top]]; a [[disjoint union space]]) of [[countably infinite set|countably]] many open [[intervals]] (e.g. section 2.1 of ([Cannon-Conner 2000](#CannonConner00))). This shows that the specific radii converging to zero (which was taken to be $1/2^n$ above) don't actually matter. Equivalently, the earring space is [[homeomorphic]] to the [[one-point compactification]] of the [[product space]] $\mathbb{N}\times \mathbb{R}$, where the space of [[real numbers]] $\mathbb{R}$ has the [[Euclidean space|Euclidean topology]] and that of [[natural numbers]] $\mathbb{N}$ has the [[discrete topology]].

Another topological characterisation is as the [[suspension]] of the [[one-point compactification]] of $\mathbb{N}$ with the [[discrete topology]] (that is, the "free convergent sequence").

## Properties
 {#Properties}

Every [[neighborhood]] of $(0, 0)$ in the Hawaiian earring space has non-contractible [[loops]] inside it (this would not be the case under the CW topology, i.e., the evident [[quotient space]] of countably many circles with the [[coproduct]] or [[disjoint union topological space|disjoint sum topology]], making the result a countable bouquet of circles). This means that the space is not
[[semi-locally simply connected space|semi-locally simply connected]].

Viewed in terms of [[general topology]], it would be hard to sell the earring space as a genuinely "pathological space": as it is a [[compactum|compact, Hausdorff]], [[connected space|connected and locally path-connected]] [[metric space]], etc. It's really through the lens of [[algebraic topology]] and particularly the classical theory of [[covering spaces]] that it seems strange: it is not a [[CW complex]], it is not 
[[semi-locally simply connected space|semi-locally simply connected]] and its [[fundamental group]] is hard to compute. 

## Related concepts

* [[Warsaw circle]]



## References

An early paper discussing the concept without giving it any specific name is:

* {#Griffiths56} H. B. Griffiths, _Infinite Products of Semi-Groups and Local Connectivity_, Proceedings of the London Mathematical Society, s3-6 (1956) 455-480 ([doi:10.1112/plms/s3-6.3.455](https://doi.org/10.1112/plms/s3-6.3.455))

The name _Hawaiian earring_ seems to be due to:

* {#Dudley61} R. M. Dudley, _Continuity of homomorphisms_, Duke Math. J. 28:4 (1961), 587-594 ([doi:10.1215/S0012-7094-61-02859-9](https://doi.org/10.1215/S0012-7094-61-02859-9))

See also:

* Wikipedia, *[Hawaiian earring](https://en.m.wikipedia.org/wiki/Hawaiian_earring)*

The following discusses the combinatorial structure of the fundamental group of the earring space.

* {#CannonConner00}  J. W. Cannon and G. R. Conner, _The combinatorial structure of the Hawaiian earring group_, Topology and its Applications **106** (2000) pp 225–271 (doi:[10.1016/S0166-8641(99)00103-0](https://doi.org/10.1016/S0166-8641%2899%2900103-0))




[[!redirects Hawaiian earring spaces]]
[[!redirects Hawaiian earring]]
[[!redirects Hawaiian earrings]]
[[!redirects clamshell]]
[[!redirects clamshells]]
[[!redirects shrinking wedge of circles]]
[[!redirects shrinking wedges of circles]]
[[!redirects infinite earring]]
[[!redirects infinite earrings]]
[[!redirects infinite earring space]]
[[!redirects infinite earring spaces]]
