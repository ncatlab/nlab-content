
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

The [[Grothendieck construction]] may be lifted from [[categories]] to [[model categories]], where it serves as a presentation for the [[(infinity,1)-Grothendieck construction|$\infty$-Grothendieck construction]].

## Definition
 {#Definition}

Let $\mathcal{M}$ be a [[model category]] and

\[
  \label{ThePseudofunctor}
  \array{
    \mathcal{M} &\longrightarrow& Mod Cat
    \\
    X &\mapsto& F(X)
    \\
    \Big\downarrow\mathrlap{{}^{f}}
    &&
    \mathllap{^{f^\ast}}\Big\uparrow
    \Big\downarrow\mathrlap{{}^{f_!}}
    \\
    Y &\mapsto& F(Y)
  }
\]

a [[pseudofunctor]], where [[ModCat|$ModelCat$]] is the [[2-category]] of [[model categories]], [[Quillen adjunctions]] (pointing in the direction of their [[left adjoints]] $f_!$), and [[conjugate transformations of adjoints]] ([[mate]]-pairs of [[natural isomorphisms]]).

We say that:

\begin{definition}\label{RelativePseudoFunctor}
$F$ is *[[relative functor]]* if for any [[weak equivalence]] $f$ in $M$, the associated Quillen adjunction $f_! \dashv f^*$ is a [[Quillen equivalence]].
\end{definition}

\begin{definition}\label{ProperPseudofunctor}
$F$ is "*proper*", if when $f \colon A\to B$ is an [[acyclic cofibration]] (resp. an [[acyclic fibration]]) in $\mathcal{M}$ then $f_!$ (resp. $f^*$) preserves all [[weak equivalences]].
\end{definition}

\begin{definition}\label{IntegralModelStructure}
**(integral model structure)**
\linebreak
Given a [[pseudofunctor]] as in (eq:ThePseudofunctor),
we say that a morphism
$$
  (f,\phi)
   \;\colon\;
  (X,A) \longrightarrow (Y,B)
$$
in its [[Grothendieck construction]] $\int_{X \in \mathcal{M}} F(X)$
(where $f \colon X\to Y$ in $\mathcal{M}$ and $\phi \colon f_!(A) \to B$ in $F(Y)$) is:

* an *integral equivalence* iff

  1. $f \colon X \to Y$ is a [[weak equivalence]] in $\mathcal{M}$

  2. $f_!(Q A) \to f_!(A) \xrightarrow{\phi} B$ is a [[weak equivalence]] in $F(Y)$, where $Q(-)$ denotes [[cofibrant replacement]].

     (Since $f_!\dashv f^*$ is a Quillen equivalence by relativeness, this is equivalent to the [[adjunct]] condition that $A \xrightarrow{\widetilde{\phi}} f^*(B) \to f^*(R B)$ is a weak equivalence in $F(X)$ for [[fibrant replacement]] $R(-)$.)

* an *integral cofibration* iff

  1. $f$ is a [[cofibration]] in $\mathcal{M}$

  1. $\phi \colon f_!(A) \to B$ is a [[cofibration]] in $F(Y)$.

* an *integral fibration* iff

  1. $f$ is a [[fibration]] in $\mathcal{M}$

  1. the [[adjunct]] $\widetilde{\phi} \colon A \to f^*(B)$ is a [[fibration]] in $F(X)$.

\end{definition}

\begin{proposition}\label{ExistenceStatement}
If the pseudofunctor (eq:ThePseudofunctor) is relative (Def. \ref{RelativePseudoFunctor}) and proper (Def. \ref{ProperPseudofunctor}) then the classes of maps in Def. \ref{IntegralModelStructure}
make $\int_{X \in \mathcal{M}} F(X)$ a [[model category]].
\end{proposition}
This is [Harpaz & Prasma (2015), Theorem 3.0.12](#HarpazPrasma15).

## Properties

\begin{proposition}
Given a proper relative $F \colon \mathcal{M} \to ModelCat$, we can compose with the underlying [[(infinity,1)-functor|$(\infty,1)$-functor]] $Ho \colon ModelCat \to QCat$ with values in (say) [[quasicategories]].
Since $F$ is relative, this map takes weak equivalences in $\mathcal{M}$ to [[equivalences of quasicategories]], so it induces a functor of quasicategories $Ho(M) \to Ho(QCat) = (\infty,1)Cat$.  The [[(∞,1)-Grothendieck construction]] of this functor is then equivalent, over $Ho(M)$, to the underlying $(\infty,1)$-category of the Grothendieck-construction model structure on $\int F$
\end{proposition}
([Harpaz & Prasma (2015), Proposition 3.1.2](#HarpazPrasma15))





\linebreak

## Related pages

* The [[formal duality|dual]] notion is a [[model structure on sections]]

* [[tangent (infinity,1)-topos]]

* [[Joyal locus]]

* [[parameterized homotopy theory]]

* [[parameterized stable homotopy theory]]


## References

The first [[model category]] version of the [[Grothendieck construction]] was given in

* {#Roig94} [[Agustí Roig]], _Model category structures in bifibred categories_, Journal of Pure and Applied Algebra **95** 2 (1994) 203–223 &lbrack;<a href="https://doi.org/10.1016/0022-4049(94)90074-4">doi:10.1016/0022-4049(94)90074-4</a>&rbrack;

This article ([Roig 94](#Roig94)) had a mistake, which was fixed in

* {#Stanculesu12} [[Alexandru E. Stanculescu]], *Bifibrations and weak factorisation systems*, Applied Categorical Structures **20** 1 (2012) 19–30 &lbrack;<a href="https://link.springer.com/article/10.1007/s10485-009-9214-3">doi:10.1007/s10485-009-9214-3</a>&rbrack;

The construction was then generalized in

* {#HarpazPrasma15} [[Yonatan Harpaz]], [[Matan Prasma]], _The Grothendieck construction for model categories_, Advances in Mathematics **281** (2015) 1306-1363 &lbrack;[arXiv:1404.1852](https://arxiv.org/abs/1404.1852), [10.1016/j.aim.2015.03.031](https://doi.org/10.1016/j.aim.2015.03.031)&rbrack;

and further in

* [[Pierre Cagne]], [[Paul-André Melliès]], *On bifibrations of model categories*, Advances in Mathematics **370** (2020) 107205 &lbrack;[arXiv:1709.10484](https://arxiv.org/abs/1709.10484), [doi:10.1016/j.aim.2020.107205](https://doi.org/10.1016/j.aim.2020.107205)&rbrack;


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
[[!redirects model structures on Grothendieck constructions]]


