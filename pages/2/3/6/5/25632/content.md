
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Category theory
+--{: .hide}
[[!include category theory - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

There are several notions of [[homomorphisms]] between [[pairs]] of [[adjoint functors]], notably the notion of pairs of *conjugate* [[natural transformations]] (Def. \ref{ConjugateTransformationOfAdjoints} below).


## Definition

There are several layers of generality at which one may consider a notion of [[homomorphism]] *between* adjoint functors. 

Here is a basic but important notion:

\begin{definition}\label{ConjugateTransformationOfAdjoints}
  **(conjugate transformations of adjoints)**
  \linebreak
  Given a [[pair]] of pairs of adjoint functors between the same [[categories]]

  \[
    \label{PairOfPairsOfAdjointFunctors}
    \array{
    \mathcal{C}
      \underoverset
        {\underset{R_1}{\longleftarrow}}
        {\overset{L_1}{\longrightarrow}}
        {\;\;\; \bot \;\;\;}
    \mathcal{D}
    \\
    \mathcal{C}
      \underoverset
        {\underset{R_2}{\longleftarrow}}
        {\overset{L_2}{\longrightarrow}}
        {\;\;\; \bot \;\;\;}
    \mathcal{D}
    }
  \]
then a [[pair]] of [[natural transformations]] between the adjoints of the same chirality, of this form
\[
  \label{PairOfTransformations}
  \lambda \,\colon\, L_1 \to L_2
  \;\;\;\;\;\;
  \rho \,\colon\, R_2 \to R_1
  \,,
\]
is called *conjugate for* &lbrack;[MacLane (1971), §IV.7 (5)](#MacLane71)&rbrack; or a *pseudo-transformation of* &lbrack;[Harpaz & Prasma (2015), Sec. 2.2](#HarpazPrasma15)&rbrack; the given adjunctions if they make the following [[diagram]] of [[natural transformations]] between [[hom-sets]] [[commuting diagram|commute]]:
\begin{tikzcd}
  \mathcal{D}(L_{2}(-),(-)) \ar[r, "\sim"] \ar[d, "{\mathcal{D}(\lambda_{(-)},(-))}"']  & \mathcal{C}((-),R_{2}(-)) \ar[d, "{\mathcal{C}((-),\rho_{(-)})}"] \\
  \mathcal{D}(L_{1}(-),(-)) \ar[r, "\sim"] & \mathcal{C}((-),R_{1}(-))
\end{tikzcd}
where the horizontal maps are the given hom-isomorphisms (see [there](adjoint+functor#eq:HomIsomorphismForAdjointFunctors)).

Such pairs of conjugate transformation [[composition|compose]] via composition of their component [[natural transformations]] (cf. *[[functor category]]*) to yields a [[category]]
\[
  \label{CatAdjCD}
  Cat_{adj}(\mathcal{C},\mathcal{D})
\]
whose

* [[objects]] are the [[left adjoint functors]] $\mathcal{C} \to \mathcal{D}$

* [[morphisms]] are the conjugate transformations between these

* [[composition]] is the composition of component [[natural transformations]].

\end{definition}

\begin{proposition} 
  \label{UniqueConjugateMate}
  Given a pair of pairs of adjunctions as in (eq:PairOfPairsOfAdjointFunctors) and given (just) $\lambda$ as in (eq:PairOfTransformations) then there exists a unique $\rho$ as in (eq:PairOfTransformations) such that the conjugacy condition (eq:ConjugacyConditionOnAdjoints) holds.

In other words, the evident [[forgetful functor]] from $Cat_{adj}(\mathcal{C},\,\mathcal{D})$ (eq:CatAdjCD) to the [[hom-category]] $\Cat(\mathcal{C},\,\mathcal{D})$ (i.e. the [[functor category]]) is a [[fully faithful functor]] exhibiting a [[full subcategory]]-inclusion:
\[
  \label{FullInclusionOfConjugateTransformations}
  \mathcal{C},\,\mathcal{D} \,\in\, Obj(Cat)
  \;\;\;\;\;\;
  \vdash
  \;\;\;\;\;\;
  Cat_{adj}(\mathcal{C},\,\mathcal{D})
  \hookrightarrow
  Cat(\mathcal{C},\,\mathcal{D})
  \,.
\]
\end{proposition}
&lbrack;[Mac Lane (1971), p. 98](#MacLane71)&rbrack;

In fact:
\begin{proposition}
\label{ConjugacyMeansMated}
**(conjugate pairs are mates)**
\linebreak
  The conjugacy condition (eq:ConjugacyConditionOnAdjoints) means equivalently that $\lambda$ and $\rho$ are *[[mates]]* in the sense of [[2-category theory]].
\end{proposition}
This is [MacLane (1971) IV.7 Thm. 2 (6), p. 98](#MacLane71) (not using the "[[mate]]"-terminology, though, which is due to [Kelly & Street 2006](mate#KellyStreet06)).

Moreover: 
\begin{proposition}
\label{HorizontalCompositionOfConjugateTransformations}
Conjugacy of transformations is compatible with [[horizontal composition]] $(-)\cdot(-)$ of [[natural transformations]] as [[2-morphisms]] in [[Cat]] ("[[whiskering]]"), so that (eq:FullInclusionOfConjugateTransformations) extends to a [[horizontal composition]]-[[functor]]:
$$
  \mathcal{C}
  ,\,
  \mathcal{D}
  ,\,
  \mathcal{E}
  \;\in\;
  Cat
  \;\;\;\;\;\;\;\;\;\;
    \vdash
  \;\;\;\;\;\;\;\;\;\;
  \array{
  Cat_{adj}(\mathcal{D},\,\mathcal{E})
  \times
  Cat_{adj}(\mathcal{C},\,\mathcal{D})
  &\overset{}{\longrightarrow}&
  Cat_{adj}(\mathcal{C},\,\mathcal{E})
  \\
  \big(
    (\lambda, \rho)
    ,\,
    (\lambda', \rho')
  \big)  
  &\mapsto&
  \big(
    \lambda' \cdot \lambda
    ,\,
    \rho \cdot \rho'
  \big)
  }
  \,.
$$
\end{proposition}
&lbrack;[MacLane (1971), §IV.8 Thm. 2 & Exc. 1 (p. 102)](#MacLane71)&rbrack;

Therefore, from Prop. \ref{UniqueConjugateMate} and Prop. \ref{HorizontalCompositionOfConjugateTransformations} we have:
\begin{definition}\label{CatAdj}
The ([[very large category|very large]]) [[wide subcategory|wide]] and [[locally full sub-2-category]] [[CatAdj|$Cat_{adj}$]] of [[Cat]]
\[
  \label{CatAdjInsideCat}
  Cat_{adj} \longrightarrow Cat
\]
whose 

* [[objects]] are categories,

* [[1-morphisms]] are [[left adjoint]] [[functors]]

* [[2-morphisms]] are [[natural transformations]] which are conjugate in the sense of Def. \ref{ConjugateTransformationOfAdjoints}.

\end{definition}
&lbrack;[MacLane (1971), §IV.8 below (1), p. 102](#MacLane71)&rbrack;

## Properties

### Relation to bifibrations

\begin{proposition}
  Under the [[Grothendieck construction]], the [[Grothendieck fibrations]] which arise from [[pseudofunctors]] $\mathcal{B} \longrightarrow Cat$ that factor through [[CatAdj|$Cat_{adj}$]] (eq:CatAdjInsideCat) are equivalently the [[bifibrations]].
\end{proposition}
\begin{proof}
A Grothendieck construction on a pseudofunctor yielding a bifibration is fairly immediately equivalent to all base change functors having an adjoint on the respective side (e.g. [Jacobs (1998), Lem. 9.1.2](bifibration#Jacobs98)). By the fact that $Cat_{adj} \to Cat$ is a [[locally full sub-2-category]] (Prop. \ref{UniqueConjugateMate}) this already means that the given pseudofunctor factors through  $Cat_adj$, and essentially uniquely so.
\end{proof}
See also [Harpaz & Prasma (2015), Prop. 2.2.1](#HarpazPrasma15).

## Related concepts

* [[monad transformation]]

* [[bifibration]]

* [[model structures on Grothendieck fibrations]]

* [[double category of model categories]]

## References

* {#MacLane71} [[Saunders MacLane]], Sections IV.7-8 of: _[[Categories Work|Categories for the working mathematician]]_, Graduate Texts in Mathematics, Springer (1971) &lbrack;[doi:10.1007/978-1-4757-4721-8](https://link.springer.com/book/10.1007/978-1-4757-4721-8)&rbrack;

See also:

* {#HarpazPrasma15} [[Yonatan Harpaz]], [[Matan Prasma]], Section 2.2. of: _The Grothendieck construction for model categories_, Advances in Mathematics **281** (2015) 1306-1363 &lbrack;[arXiv:1404.1852](https://arxiv.org/abs/1404.1852), [10.1016/j.aim.2015.03.031](https://doi.org/10.1016/j.aim.2015.03.031)&rbrack;

  > (in the context of [[model structures on Grothendieck constructions]])

[[!redirects transformations of adjoints]]

[[!redirects conjugate transformation of adjoints]]
[[!redirects conjugate transformations of adjoints]]


[[!redirects transformation of adjoint functors]]
[[!redirects transformations of adjoint functors]]

[[!redirects conjugate transformation of adjoint functors]]
[[!redirects conjugate transformations of adjoint functors]]


[[!redirects natural transformation of adjoint functors]]
[[!redirects natural transformations of adjoint functors]]


[[!redirects conjugate natural transformation of adjoint functors]]
[[!redirects conjugate natural transformations of adjoint functors]]




