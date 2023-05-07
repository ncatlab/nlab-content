
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Monoidal categories
+--{: .hide}
[[!include monoidal categories - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Definition

A **pivotal category** is an [[autonomous category]] equipped with a [[monoidal natural transformation|monoidal natural isomorphism]] $A \to (A^*)^*$.  Pivotal categories have also been called "sovereign categories."  This is a kind of [[category with duals]].

A right autonomous category with such an isomorphism is automatically left autonomous too, so the right/left distinction does not apply to pivotal categories. Note additionally that for the double dual to really be a functor we are assuming that every object has a distinguished dual element.

## Intuition

In an autonomous category $\mathscr{C}$, left duals and right duals have no reason to agree. That is, given an object $A\in\mathscr{C}$ we may not necessarily have $A\cong A^{**}$ (See [this MO post](https://mathoverflow.net/questions/303245/the-dual-of-a-dual-in-a-rigid-tensor-category) for a discussion). Even if we do (like in semisimple categories and braided monoidal categories) there is no a-priori reason for this isomorphism to be natural.

For this isomorphism to be natural we need a pivotal structure. Interestingly enough, if a pivotal structure exists then it will be unique up to precomposing with an element of the group $\text{Aut}^{\otimes}(\text{id}_{\mathscr{C}})$ of monoidal natural automorphisms of the identity ([Bartlett, Prop. 5.7, Lemma 6.2](#Bartlett2009)).

In the case of fusion categories, we have that $\text{Aut}^{\otimes}(\text{id}_{\mathscr{C}})\cong \text{Hom}(U_{\mathscr{C}},\mathbb{C}^{\times})$ where $U_{\mathscr{C}}$ is the universal grading group. Hence, there will be only finitely many choices of pivotal structures by a result of [Gelaki](#Gelaki2006).

## Explicit compatibility conditions

Our intuition for pivotal categories is that right duals should also be left duals in a natural/compatible way. This can be made explicit, and gives an alternative definition of pivotal. Namely, a pivotal category is a (right) rigid monoidal category equipped with morphisms

$$\text{ev}^{\text{rev}}_{A}:A^*\otimes A \to 1,$$

$$\text{coev}^{\text{rev}}_A:1\to A\otimes A^*$$

giving $A^*$ the structure of a left dual for $A$, such that $\text{ev}_A$,$\text{coev}_A$,$\text{ev}^{\text{rev}}_A$, $\text{coev}^{\text{rev}}_A$ satisfy appropriate compatibility conditions. The exact conditions feel unmotivated and clunky when written out explicitly in terms of compositions, and hence they are best stated in the language of [[string diagrams]].

\begin{proposition} Let $\mathscr{C}$ be a pivotal category, with natural isomorphism $i:\text{id}_{\mathscr{C}}\to (-)^{**}$. We graphically define the distinguished morphisms

\begin{imagefromfile}
"file_name": "pivotal-eval-coeval.png",
"width": 400,
"unit": "px"
\end{imagefromfile}

The following properties are satisfied:


* These morphisms satisfy the rigidity axioms. This is, for all $A\in \mathscr{C}$

\begin{imagefromfile}
"file_name": "rigidity-reprise.png",
"width": 300,
"unit": "px"
\end{imagefromfile}

* For all $A,B\in \mathscr{C}$,

\begin{imagefromfile}
"file_name": "something-property.png",
"width": 300,
"unit": "px"
\end{imagefromfile}

* For all $A,B\in \mathscr{C}$, $f:A\to B$,

\begin{imagefromfile}
"file_name": "morphism-duals-agree.png",
"width": 200,
"unit": "px"
\end{imagefromfile}

Conversely, any rigid category with duals satisfying these axioms will be pivotal under the functor

\begin{imagefromfile}
"file_name": "duals-to-pivotal.png",
"width": 200,
"unit": "px"
\end{imagefromfile}

This gives a bijection between pivotal categories and rigid categories with duals satisfying these axioms.

\end{proposition}
\begin{proof} See [Bartlett](#Bartlett2009) Section 5.1.
\end{proof}

## Related concepts

* {#Gelaki2006} [[Shlomo Gelaki]], _Nilpotent fusion categories_, Advances in Mathematics, [arXiv](https://arxiv.org/abs/math/0610726)

* {#Bartlett2009} [[Bruce Bartlett]], _On unitary 2-representations of finite groups and topological quantum field theory_, PhD thesis, [arXiv](https://arxiv.org/abs/0901.3975)

* [[fusion category]]

* **pivotal category

* [[spherical category]]


[[!redirects pivotal category]]
[[!redirects pivotal categories]]
[[!redirects sovereign category]]
[[!redirects sovereign categories]]
[[!redirects pivotal structure]]
[[!redirects pivotal structures]]
