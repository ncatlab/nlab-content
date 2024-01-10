
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Enriched category theory
+--{: .hide}
[[!include enriched category theory contents]]
=--
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Categorical algebra
+-- {: .hide}
[[!include categorical algebra -- contents]]
=--
=--
=--
=--
=--

# Contents
* table of contents
{: toc}

## Idea

When we define [[internal categories]] of some category $\mathcal{C}$ as [[monads]] in the [[category of spans]] $\mathrm{Span}(\mathcal{C})$, there is a subtlety concerning the definition of [[internal functors]]. It is not the case that the morphisms of monads (namely [[colax morphism|colax]] monad morphisms) give us [[internal functors]] directly: we need to ask that the 1-cell of the morphism is a [[left adjoint]] in $\mathrm{Span}(\mathcal{C})$ (which corresponds to asking that the left leg of the span be the identity, or an isomorphism). (This is related to the [[profunctor#Properties|behaviour of profunctors]] in that they correspond to functors (via the [[Yoneda embedding]]) exactly when they are [[left adjoints]].)  If in considering morphisms of monads in $Span(\mathcal{C})$ we _don't_ require this left-adjoint condition then we end up constructing **Mealy morphisms** between internal categories. 

'Mealy morphisms' are  named after [[Mealy machines]], which, in turn, were named after  [[George H. Mealy]].

## Definition

Let $\mathbf{A}$ and $\mathbf{B}$ be [[categories]] [[enriched category|enriched]] in a [[monoidal category]] $(\mathbf{V}, I, \otimes)$. 

A *Mealy morphism* $(F, \phi) \colon \mathbf{A} \rightarrow \mathbf{B}$ 
consists of a [[pair]] of [[functions]] $F \colon Ob\mathbf{A} \rightarrow Ob\mathbf{B}$ and $\phi \colon \mathbf{A} \rightarrow \mathbf{V}$, 
and for each [[pair]] of [[objects]] $A, A'$ in $\mathbf{A}$ a function
\[
\phi(A, A') \colon \mathbf{A}(A, A') \otimes \phi(A) \longrightarrow \phi(A') \otimes \mathbf{B}(FA, FA')
\]
satisfying the following commutative diagrams. 
\begin{tikzcd}
I \otimes \phi(A) 
\arrow[d, "\cong"']
\arrow[r, "{j_{A} \otimes 1}"]
& \mathbf{A}(A, A) \otimes \phi(A)
\arrow[d, "{\phi(A, A)}"]
\\
\phi(A) \otimes I
\arrow[r, "{1 \otimes j_{FA}}"']
& \phi(A) \otimes \mathbf{B}(FA, FA)
\end{tikzcd}
\begin{tikzcd}
\mathbf{A}(A', A'') \otimes \mathbf{A}(A, A') \otimes \phi(A)
\arrow[r, "{\circ_{A, A', A''} \otimes \phi(A)}"]
\arrow[d, "1 \otimes {\phi(A, A')}"']
&[+3em] \mathbf{A}(A, A'') \otimes \phi(A)
\arrow[dd, "{\phi(A, A'')}"]
\\
\mathbf{A}(A', A'') \otimes \phi(A') \otimes \mathbf{B}(FA, FA')
\arrow[d, "{\phi(A', A'') \otimes 1}"']
& 
\\
\phi(A'') \otimes \mathbf{B}(FA', FA'') \otimes  \mathbf{B}(FA, FA')
\arrow[r, "1 \otimes \circ_{FA, FA', FA''}"']
& \phi(A'') \otimes \mathbf{B}(FA, FA'')
\end{tikzcd}

## Properties

- There is a [[bicategory]] of small $V$-enriched categories, Mealy morphisms, and Mealy cells. It is the [[Kleisli bicategory]] for the [[free cocompletion]] of a small $V$-category under [[copowers]]. This is analogous to the universal property of the bicategory [[Prof]] of [[profunctors]] as the Kleisli bicategory for the free cocompletion of a small category under [[small colimits]]. This is proven in [Paré 2012](#Pare12).

## References

The notion of Mealy morphism between [[enriched categories]] was introduced in the paper: 

* {#Pare12} [[Robert Paré]], _Mealy Morphisms of Enriched Categories_, Applied Categorical Structures **20** (2012) pp 251--273, doi:[10.1007/s10485-010-9238-8](https://doi.org/10.1007/s10485-010-9238-8).

Mealy morphisms are mentioned in Example 16.8 and Example 16.27 in the paper: 

* {#GarnerShulman16} [[Richard Garner]], [[Michael Shulman]], _Enriched categories as a free cocompletion_, Advances in Mathematics, 289, 2016 ([arXiv:1301.3191](https://arxiv.org/abs/1301.3191), [doi:10.1016/j.aim.2015.11.012](https://doi.org/10.1016/j.aim.2015.11.012))

Mealy morphisms are also considered under the name "two-dimensional partial map" (a notion attributed to [[Lawvere]]) in the Appendix of the paper: 

* {#LackStreet02} [[Stephen Lack]], [[Ross Street]], _The formal theory of monads II_, Journal of Pure and Applied Algebra, 175, 2002 ( [doi:10.1016/S0022-4049(02)00137-8](https://doi.org/10.1016/S0022-4049%2802%2900137-8))

Some talk slides which mention Mealy morphisms: 

* [[Robert Paré]], [Mealy Morphisms for Tensor Categories](https://www.mscs.dal.ca/~pare/June2010.pdf) 

[[!redirects Mealy morphisms]]