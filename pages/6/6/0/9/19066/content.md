
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
 {#Definition}

Let $M$ be a [[model category]] and $F \colon M \to ModelCat$ a [[pseudofunctor]], where $ModelCat$ is the [[2-category]] of model categories, [[Quillen adjunctions]] pointing in the direction of their [[left adjoints]], and [[mate]]-pairs of [[natural isomorphisms]].  Assume furthermore that:

* $F$ is *[[relative functor|relative]]*, meaning that whenever $f \colon A\to B$ is a [[weak equivalence]] in $M$, then the Quillen adjunction $f_! \colon F(A) \rightleftarrows F(B) : f^*$ is a [[Quillen equivalence]].  (That is, $F$ is a [[relative functor]].)

* $F$ is "*proper*", meaning that whenever $f \colon A\to B$ is an acyclic cofibration (resp. an acyclic fibration) in $M$, then $f_!$ (resp. $f^*$) preserves [[weak equivalences]].

In the [[Grothendieck construction]] $\int F$ we define a morphism $(f,\phi) \colon (A,X) \to (B,Y)$ (where $f \colon A\to B$ in $M$ and $\phi \colon f_!(X) \to Y$ in $F(B)$), to be:

* a *weak equivalence* iff $f \colon A\to B$ is a weak equivalence in $M$ and $f_!(Q X) \to f_!(X) \xrightarrow{\phi} Y$ is a weak equivalence in $F(B)$, where $Q$ is a [[cofibrant replacement]].  

  (Since $f_!\dashv f^*$ is a Quillen equivalencen by relativeness, this is equivalent to the dual condition that $X \xrightarrow{\hat{\phi}} f^*(Y) \to f^*(R Y)$ is a weak equivalence in $F(A)$.)

* a *cofibration* iff $f$ is a cofibration in $M$ and $\phi \colon f_!(X)\to Y$ is a cofibration in $F(B)$.

* a *fibration* if $f$ is a fibration in $M$ and the [[adjunct]] $\hat{\phi} \colon X\to f^*(Y)$ is a fibration in $F(A)$.

\begin{proposition}\label{ExistenceStatement}
There classes of maps make $\int F$ a model category.
\end{proposition}
This is [Harpaz & Prasma (2015), Theorem 3.0.12](#HarpazPrasma15).

## Properties

\begin{proposition}
Given a proper relative $F:M\to ModelCat$, we can compose with the underlying [[(infinity,1)-functor|$(\infty,1)$-functor]] $Ho \colon ModelCat \to QCat$ with values in (say) [[quasicategories]].  
Since $F$ is relative, this map takes weak equivalences in $M$ to equivalences of quasicategories, so it induces a functor of quasicategories $Ho(M) \to Ho(QCat) = (\infty,1)Cat$.  The [[(∞,1)-Grothendieck construction]] of this functor is then equivalent, over $Ho(M)$, to the underlying $(\infty,1)$-category of the Grothendieck-construction model structure on $\int F$
\end{proposition}
([Harpaz & Prasma (2015), Proposition 3.1.2](#HarpazPrasma15))

## Related pages

* The [[formal duality|dual]] notion is a [[model structure on sections]]


## References

The first [[model category]] version of the [[Grothendieck construction]] was given in

* {#Roig94} [[Agustí Roig]], _Model category structures in bifibred categories_, Journal of Pure and Applied Algebra **95** 2 (1994) 203–223 &lbrack;<a href="https://doi.org/10.1016/0022-4049(94)90074-4">doi:10.1016/0022-4049(94)90074-4</a>&rbrack;

This article ([Roig 94](#Roig94)) had a mistake, which was fixed in

* {#Stanculesu12} [[Alexandru E. Stanculescu]], *Bifibrations and weak factorisation systems*, Applied Categorical Structures **20** 1 (2012) 19–30 &lbrack;<a href="https://link.springer.com/article/10.1007/s10485-009-9214-3">doi:10.1007/s10485-009-9214-3</a>&rbrack;

The construction was then generalized in

* {#HarpazPrasma15} [[Yonatan Harpaz]], [[Matan Prasma]], _The Grothendieck construction for model categories_, Advances in Mathematics **281** (2015) 1306-1363 &lbrack;[arXiv:1404.1852](https://arxiv.org/abs/1404.1852), [10.1016/j.aim.2015.03.031](https://doi.org/10.1016/j.aim.2015.03.031)&rbrack;

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

[[!redirects model structure on Grothendieck fibration]]
[[!redirects model structures on Grothendieck fibrations]]

[[!redirects model structure on a Grothendieck construction]]
[[!redirects model structure on the Grothendieck construction]]
[[!redirects model structure on Grothendieck constructions]]


