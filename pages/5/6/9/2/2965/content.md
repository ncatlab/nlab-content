
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Category Theory
+--{: .hide}
[[!include category theory - contents]]
=--
#### Topos Theory
+--{: .hide}
[[!include topos theory - contents]]
=--
=--
=--

#Contents#
* automatically generated table of contents
{:toc}

## Idea

A **small presheaf** on a category $C$ is a [[presheaf]] which is determined by a small amount of data.  If $C$ is itself [[small category|small]], then every presheaf on $C$ is small, but this is no longer true when $C$ is large.  In many cases, when $C$ is large, it is the small presheaves which seem to be more important and useful.

## Definition

Let $C$ be a [[category]] which is [[locally small category|locally small]], but possibly [[large category|large]].  A presheaf $F\colon C^{op}\to Set$ is **small** if it is the left [[Kan extension]] of some functor whose domain is a [[small category]], or equivalently if it is a small [[colimit]] of [[representable functors]] (see Proposition 4.83 of [Kelly](#Kelly82)).

Of course, if $C$ is itself small, then every presheaf is small.

## Categories of small presheaves

We write $P C$ for the category of small presheaves on $C$.  Observe that although the category of *all* presheaves on $C$ cannot be defined without the assumption of a [[Grothendieck universe|universe]], the category $P C$ can be so defined, using small diagrams in $C$ as proxies for small colimits of representable presheaves.  Moreover $P C$ is locally small, and there is a [[Yoneda embedding]] $C\hookrightarrow P C$.

Of course, if $C$ is small, then $P C$ is the usual category of all presheaves on $C$.

Since small colimits of small colimits are small colimits, $P C$ is [[cocomplete category|cocomplete]].  In fact, it is easily seen to be the [[free cocompletion]] of $C$, even when $C$ is not small.  It is not, in general, complete, but we can characterize when it is (cf. Day--Lack).

+-- {: .un_theorem}
###### Theorem
$P C$ is complete if and only if for every small diagram in $C$, the category of cones over that diagram has a small weakly terminal set, i.e. there is a small set of cones such that every cone factors through one in that set.
=--

+-- {: .un_cor}
###### Corollary
If $C$ is either complete or small, then $P C$ is complete.
=--

We also have:

+-- {: .un_theorem}
###### Theorem
If $C$ and $D$ are complete, then a functor $F\colon C\to D$ preserves small limits if and only if the functor $P F\colon P C \to P D$ (induced by left Kan extension) also preserves small limits.
=--

These results can all be generalized to [[enriched categories]], and also relativized to limits in some class $\Phi$ (which, for some purposes, we might want to assume to be "saturated").  See the paper by Day and Lack.


## References

* {#Kelly82} [[Max Kelly]], _Basic concepts of enriched category theory_, London Math. Soc. Lec. Note Series __64__, Cambridge Univ. Press (1982), Reprints in Theory and Applications of Categories **10** (2005) 1-136  &lbrack;[ISBN:9780521287029](https://www.cambridge.org/de/academic/subjects/mathematics/logic-categories-and-sets/basic-concepts-enriched-category-theory?format=PB&isbn=9780521287029), [tac:tr10](http://www.tac.mta.ca/tac/reprints/articles/10/tr10abs.html), [pdf](http://www.tac.mta.ca/tac/reprints/articles/10/tr10.pdf)&rbrack;

* [[Brian J. Day]], [[Stephen Lack]], _Limits of small functors_, Journal of Pure and Applied Algebra 210:3 (2007), 651-663.  [doi](https://doi.org/10.1016/j.jpaa.2006.10.019), [arXiv](http://arxiv.org/abs/math/0610439), [pdf](http://www.maths.usyd.edu.au/u/stevel/papers/small.pdf).

* [[Boris Chorny]], [[William Dwyer]], _The homotopy theory of small diagrams over large categories_,  Forum Math. 21:2 (2009), 167–179.  [doi](https://doi.org/10.1515/forum.2009.009), [arXiv](https://arxiv.org/abs/math/0607117)

* [[Paolo Perrone]], [[Walter Tholen]], *Kan extensions are partial colimits*, Applied Categorical Structures 30:4 (2022), 685-753. ([arXiv:2101.04531](https://arxiv.org/abs/2101.04531), [doi](https://doi.org/10.1007/s10485-021-09671-9))
  
The results of Chorny--Dwyer are cited by Rosický in 

* [[Jiří Rosický]], _Accessible categories and homotopy theory_, lecture notes for the Summer School on Contemporary Categorical Methods in Algebra and Topology (2007) [pdf](https://www.math.muni.cz/~rosicky/papers/homacc3.pdf)

See also

* [[Georg Biedermann]], [[Boris Chorny]], _Duality and small functors_, Algebraic & Geometric Topology 15 (2015) 2609--2657.  [doi](https://doi.org/10.2140/agt.2015.15.2609)

* [[Boris Chorny]], David White, _A variant of a Dwyer-Kan theorem for model categories_ (v1: _Homotopy theory of homotopy presheaves_), Algebraic & Geometric Topology __24__:4, 2185--2208 [arXiv:1805.05378](https://arxiv.org/abs/1805.05378)

On when [[finitely continuous]] [[presheaves]] are small:

* [[Jiří Adámek]], V. Koubek, and V. Trnková. *How large are left exact functors?*. Theory and Applications of Categories 8.13 (2001): 377-390. ([pdf](http://www.tac.mta.ca/tac/volumes/8/n13/n13.pdf))

[[!redirects small presheaves]]
[[!redirects small sheaf]]
[[!redirects small sheaves]]
[[!redirects small functor]]
[[!redirects small functors]]
[[!redirects small presheaf category]]
[[!redirects small presheaf categories]]
[[!redirects category of small presheaves]]
[[!redirects categories of small presheaves]]