
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

## Examples
 {#Examples}

### Basic examples
 {#BasicExamples}

\begin{example}\label{ModelStructureOnIndexedSetsOfObjects}
**(model structure on indexed sets of objects)**
\linebreak
  For $\mathcal{C}$ any [[model category]], consider the [[pseudofunctor]] on [[Set]] which assigns categories of [[indexed sets]] of objects of $\mathcal{C}$, equipped with the [product model structure](model+category#ProductModelStructure):
$$
  \array{
    Set 
    &\longrightarrow&
    ModCat
    \\
    S 
      &\mapsto& 
    \underset{s \in S}{\prod} \mathcal{C}
    \\
    \Big\downarrow{{}^\mathrlap{f}}
    &&
    \mathllap{{}^{f^\ast}}\Big\uparrow
    \Big\downarrow\mathrlap{{}^{f_!}}
    \\
    T 
      &\mapsto& 
    \underset{s \in S}{\prod} \mathcal{C}
  }
$$  
Here $f_!$ forms [[coproducts]] of objects in the same [[fibers]] of $f$.

If we regard [[Set]] as equipped with its [[trivial model structure]] (whose [[weak equivalences]] are the [[isomorphisms]] and all morphisms are both [[fibrations]] as well as [[cofibrations]]) then this is evidently a relative and proper functor in the sense of Def. \ref{RelativePseudoFunctor},  Def. \ref{ProperPseudofunctor} (since with weak equivalences $f$ in $Set$ being isomorphisms, the associated functors $f_!, f^\ast$ are certainly [[Quillen equivalences]] but in fact are plain [[equivalences of categories]] compatible with the model structure and hence also preserve all weak equivalences).


Therefore with Prop. \ref{ExistenceStatement} the integral model structure on the [[Grothendieck construction]]
\[
  \label{GrothConstForObjectsParameterizedOverSets}
  \int_{S \in Set} 
    \underset{s \in S}{\prod} \mathcal{C}
  \;\;\;\;
  =
  \;\;\;\;
  \left\{
  \begin{array}{ccc}
    \underset{s \in S}{\coprod} X_s
    &\overset{\phi}{\longrightarrow}&
    \underset{t \in T}{\coprod} Y_t
    \\
    \big\downarrow
    &&
    \big\downarrow
    \\
    S &\underset{f}{\longrightarrow}& T
  \end{array}
  \right\}
\]
exists, where on the right we are indicating how the [[objects]] in this Grothendieck construction may be thought of as [[bundles]] of $\mathcal{C}$-objects over sets (under the unique [[coproduct]]-[[preserved colimit|preserving]] embedding $Set \hookrightarrow \mathcal{C}$) and the [[morphisms]] as morphisms of such bundles covering possibly non-trivial maps of base sets.

Unwinding the definition \ref{IntegralModelStructure} of the integral model structure in this case, gives that such a morphism $\phi_f$ in this Grothendieck construction is:

* a fibration iff all the components $X_s \longrightarrow Y_{f(s)}$ are fibrations in $\mathcal{C}$ for all $s \in S$,

* a cofibration iff all the co-components $\underset{s \in f^{-1}(\{t\})}{\coprod}  X_s \longrightarrow Y_t$ are cofibrations in $\mathcal{C}$, for all $t \in T$,

* a weak equivalence iff $f$ is a [[bijection]] of index sets and all the (co)components maps --- which in this case are all of the form $X_s \longrightarrow X_{f(s)}$ --- are weak equivalences in $\mathcal{C}$

  (here the composition with (co)fibrant replacements can be omitted, since, as above, $f_!, f^\ast$ preserve such resolution weak equivalences).


\end{example}

\begin{example}
**(model structure on skeletal simplicial groupoids)**
As a special case of Exp. \ref{ModelStructureOnIndexedSetsOfObjects}, consider $\mathcal{C} \coloneqq sGrpd$ the [[model structure on simplicial groups]].

Notice that forming simplicial [[delooping groupoids]] is a [[fully faithful functor]] from [[sGrp]] to the *[[1-category]]* of [[sSet]]-[[enriched groupoids]] (Dwyer-Kan's"[[simplicial groupoids]]")
$$
  \array{
    sGrp &\longrightarrow& sSet\text{-}Grpd
    \\
    \mathcal{G} &\mapsto& \mathbf{B}\mathcal{G}
  }
$$
which extends to identify the [[Grothendieck construction]] (eq:GrothConstForObjectsParameterizedOverSets) in the present case with the [[full subcategory]] of [[disjoint unions]] of simplicial [[delooping groupoids]], hence with that of simplicial [[skeletal groupoids]]:
\[
  \label{InclusionOfSkeletalSimplicialGroupoids}
  \array{
    \int_S \underset{s \in S}{\prod} sGrp
    &\;\simeq\;&
    sSet\text{-}Grpd_{skl}
    &\xhookrightarrow{\phantom{--}}& 
    sSet\text{-}Grpd
    \\
    \big(\mathcal{G}_s\big)_{s \in S} 
      &\mapsto& 
    \underset{s \in S}{\coprod} 
      \mathbf{B}\mathcal{G}_s
  }
\]

Since (assuming the [[axiom of choice]] in the [[underlying]] [[Sets]]) every [[sSet]]-[[enriched groupoid]] is [[Dwyer-Kan equivalence|DK-equivalent]] to a skeletal simplicial groupoid, the [[full subcategory]] inclusion (eq:InclusionOfSkeletalSimplicialGroupoids) is also a [[Dwyer-Kan equivalence]] of [[sSet-enriched categories]]. 

Moreover, if we consider on $sSet\text{-}Grpd$ the usual [[model structure on simplicial groupoids]], then the inclusion functor
$$
  sSet\text{-}Grpd_{skl}
  \hookrightarrow
  sSet\text{-}Grpd  
$$
preserves [[weak equivalences]] and [[fibrations]]. However, since there is no [[left adjoint]] to this functor (due to the choices involved in passing to a [[skeleton]] such an adjoint exists only as a [[pseudofunctor]], hence on the level of [[2-category theory]]) this is *not* a [[right Quillen functor]], and in particular *not* a [[Quillen equivalence]].


\end{example}


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


