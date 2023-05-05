
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

  $$
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
  $$

then a [[pair]] of [[natural transformations]] between the adjoints of the same chirality, of this form

$$
  \lambda \,\colon\, L_1 \to L_2
  \;\;\;\;\;\;
  \rho \,\colon\, R_2 \to R_1
$$
is called *conjugate for* &lbrack;[MacLane (1971), §IV.7 (5)](#MacLane71)&rbrack; or a *pseudo-transformation of* &lbrack;[Harpaz & Prasma (2015), Sec. 2.2](#HarpazPrasma15)&rbrack; the given adjunctions if they make the following [[diagram]] of [[natural transformations]] between [[hom-sets]] [[commuting diagram|commute]]:
\[
  \label{ConjugacyConditionOnAdjoints}
  \array{
    \mathcal{C}\big(
      L_2(-)
      ,\,
      (-)
    \big)
    &\overset{\sim}{\longrightarrow}&
    \mathcal{D}\big(
      (-)
      ,\,
      R_2(-)
    \big)
    \\
    \mathllap{{}^{
      \mathcal{C}\big(\lambda_{(-)},\,id_{(-)}\big)
    }}
    \Big\downarrow
    &&
    \Big\downarrow
    \mathrlap{{}^{
      \mathcal{C}\big(id_{(-)},\,\rho_{(-)}\big)
    }}
    \\
    \mathcal{C}\big(
      L_1(-)
      ,\,
      (-)
    \big)
    &\overset{\sim}{\longrightarrow}&
    \mathcal{D}\big(
      (-)
      ,\,
      R_1(-)
    \big)
    \mathrlap{\,,}
  }
\]
where the horizontal maps are the given hom-isomorphisms (see [there](adjoint+functor#eq:HomIsomorphismForAdjointFunctors)).
\end{definition}

\begin{proposition}
\label{ConjugacyMeansMated}
**(conjugate pairs are mates)**
\linebreak
  The conjugacy condition (eq:ConjugacyConditionOnAdjoints) means equivalently that $\lambda$ and $\rho$ are *[[mates]]* in the sense of [[2-category theory]].
\end{proposition}
This is [MacLane (1971) IV.7 Thm. 2 (6), p. 98](#MacLane71) (not using the "[[mate]]"-terminology, though, which is due to [Kelly & Street (2006)](mate#KellyStreet06)).

Conjugacy of transformations is compatible with [[horizontal composition|horizontal]] and [[vertical composition]] of [[natural transformations]] as [[2-morphisms]] in [[Cat]] and hence yields:

\begin{definition}\label{CatAdj}
The ([[very large category|very large]]) [[wide subcategory|wide]] and [[locally full sub-2-category]] of [[Cat]]
\[
  \label{CatAdjInsideCat}
  Cat_{Adj} \longrightarrow Cat
\]
whose 

* [[objects]] are categories,

* [[1-morphisms]] are [[left adjoint]] [[functors]]

* [[2-morphisms]] are [[natural transformations]] which are conjugate in the sense of Def. \ref{ConjugateTransformationOfAdjoints}.

\end{definition}

## Properties

### Relation to bifibrations

\begin{proposition}
  Under the [[Grothendieck construction]], the [[Grothendieck fibrations]] which arise from [[pseudofunctors]] $\mathcal{B} \longrightarrow Cat$ that factor through $Cat_{Adj}$ (eq:CatAdjInsideCat) are equivalently the [[bifibrations]].
\end{proposition}
This statment may be [[category theory]] [[folklore]]; a proof has been spelled out in [Harpaz & Prasma (2015), Prop. 2.2.1](#HarpazPrasma15).

## Related concepts

* [[bifibration]]

* [[model structures on Grothendieck fibrations]]

* [[double category of model categories]]

## References

* {#MacLane71} [[Saunders MacLane]], Section IV.7 of: _[[Categories Work|Categories for the working mathematician]]_, Graduate texts in mathematics, Springer (1971) &lbrack;[doi:10.1007/978-1-4757-4721-8](https://link.springer.com/book/10.1007/978-1-4757-4721-8)&rbrack;

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




