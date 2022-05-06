
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Model category theory
+--{: .hide}
[[!include model category theory - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

The [[Grothendieck construction]] may be lifted from [[categories]] to [[model categories]], where it serves as a presentation for the [[(infinity,1)-Grothendieck construction]].

## Definition

Let $M$ be a [[model category]] and $F:M\to ModelCat$ a [[pseudofunctor]], where $ModelCat$ is the [[2-category]] of model categories, [[Quillen adjunctions]] pointing in the direction of their left adjoints, and [[mate]]-pairs of [[natural isomorphisms]].  Assume furthermore that:

* $F$ is *relative*, meaning that whenever $f:A\to B$ is a weak equivalence in $M$, then the Quillen adjunction $f_! : F(A) \rightleftarrows F(B) : f^*$ is a [[Quillen equivalence]].  (That is, $F$ is a [[relative functor]].)

* $F$ is *proper*, meaning that whenever $f:A\to B$ is an acyclic cofibration (resp. an acyclic fibration) in $M$, then $f_!$ (resp. $f^*$) preserves weak equivalences.

On the [[Grothendieck construction]] $\int F$ we define a morphism $(f,\phi):(A,X) \to (B,Y)$, where $f:A\to B$ in $M$ and $\phi:f_!(X) \to Y$ in $F(B)$, to be:

* a *weak equivalence* if $f:A\to B$ is a weak equivalence in $M$ and $f_!(Q X) \to f_!(X) \xrightarrow{\phi} Y$ is a weak equivalence in $F(B)$, where $Q$ is a cofibrant replacement.  Since $f_!\dashv f^*$ is a Quillen equivalencen by relativeness, this is equivalent to the dual condition that $X \xrightarrow{\hat{\phi}} f^*(Y) \to f^*(R Y)$ is a weak equivalence in $F(A)$.

* a *cofibration* if $f$ is a cofibration in $M$ and $\phi : f_!(X)\to Y$ is a cofibration in $F(B)$.

* a *fibration* if $f$ is a fibration in $M$ and the [[adjunct]] $\hat{\phi} : X\to f^*(Y)$ is a fibration in $F(A)$.

Then these classes of maps make $\int F$ a model category.

## Properties

Given a proper relative $F:M\to ModelCat$, we can compose with the underlying $(\infty,1)$-category functor $Ho:ModelCat \to QCat$ with values in (say) [[quasicategories]].  Since $F$ is relative, this map takes weak equivalences in $M$ to equivalences of quasicategories, so it induces a functor of quasicategories $Ho(M) \to Ho(QCat) = (\infty,1)Cat$.  The [[(∞,1)-Grothendieck construction]] of this functor is then equivalent, over $Ho(M)$, to the underlying $(\infty,1)$-category of the Grothendieck-construction model structure on $\int F$; this is [Harpaz-Prasma, Proposition 3.1.2](#HarpazPrasma14).

## Related pages

* The dual notion is a [[model structure on sections]]


## References

The first [[model category]] version of the [[Grothendieck construction]] was given in

* {#Roig94} [[Agustí Roig]], _Model category structures in bifibred categories_, Journal of Pure and Applied Algebra 95.2, p.203–223, (1994) (<a href="https://doi.org/10.1016/0022-4049(94)90074-4">doi:10.1016/0022-4049(94)90074-4</a>)

This article ([Roig 94](#Roig94)) had a mistake, which was fixed in

* {#Stanculesu12} Alexandru E. Stanculescu, _Bifibrations and weak factorisation systems_, Applied Categorical Structures 20.1, p.19–30, (2012) (<a href="https://link.springer.com/article/10.1007/s10485-009-9214-3">doi:10.1007/s10485-009-9214-3</a>)

The construction was then generalized in

* {#HarpazPrasma14} [[Yonatan Harpaz]], [[Matan Prasma]], _The Grothendieck construction for model categories_, Advances in Mathematics, Volume 281, 20 August 2015, Pages 1306-1363 ([arXiv:1404.1852](https://arxiv.org/abs/1404.1852))

Another approach is found in

* [[Pierre Cagne]], [[Paul-André Melliès]], _On bifibrations of model categories_, ([arXiv:1709.10484](https://arxiv.org/abs/1709.10484))


For the special case of pseudofunctors with values in [[groupoids]], a [[model category]] version of the Grothendieck construction was discussed in

* [[Sharon Hollander]], _A homotopy theory for stacks_ ([arXiv:math.AT/0110247](http://arxiv.org/abs/math.AT/0110247)).


[[!redirects Grothendieck construction of model categories]]
[[!redirects model category-theoretic Grothendieck construction]]
[[!redirects integral model structure]]
[[!redirects integral model structures]]
[[!redirects lax colimit model structure]]
[[!redirects lax colimit model structures]]
[[!redirects model structure on a lax colimit]]
[[!redirects model structures on a lax colimit]]
[[!redirects model structures on lax colimits]]
