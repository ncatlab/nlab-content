
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

## In braided monoidal categories

It is a general principle that rigidity behaves much better in [[braided monoidal categories]]. For instance, every braided rigid category will automatically have two-sided duals ([Joyal and Street](#Joyal1993), Proposition 7.2). However, there is no a-priori reason for a pivotal structure to exist. What is true is that pivotal structures can be quantified explicitly in terms of _twists_:

\begin{proposition}[Deligne] Let $\mathscr{C}$ be a braided monoidal category. Given any natural isomorphism $\theta:\id_{\mathscr{C}}\to\id_{\mathscr{C}}$ such that $\theta_{A\otimes B}=\beta_{B,A}\circ \beta_{A,B}\circ (\theta_A\otimes \theta_B)$ for all $A,B\in \mathscr{C}$, the distinguished morphisms

\begin{imagefromfile}
"file_name": "co-dual.png",
"width": 300,
"unit": "px"
\end{imagefromfile}

give $\mathscr{C}$ the structure of a pivotal category. This map induces a canonical bijection between the set of pivotal structures on $\mathscr{C}$ and the set of natural isomorphism $\theta$ satisfying $\theta_{A\otimes B}=\beta_{B,A}\circ \beta_{A,B}\circ (\theta_A\otimes \theta_B)$ for all $A,B\in \mathscr{C}$.
\end{proposition}
\begin{proof} An exposition can be found in this article of [Yetter](#Yetter1992).
\end{proof}

This result is explained morally as follows:

>"The lemma is remarkable because the concept of a braided autonomous category does not include any assumption relating the braided structure to the autonomous structure. Moreover, the axioms for a twist depend only on the braided structure, whereas the axioms for a pivotal structure depend only on the autonomous structure. Yet, they are equivalent if $\mathscr{C}$ is braided autonomous" - Peter Selinger

Given a pivotal structure, the twist can be recovered explicitly using graphical language as follows:

\begin{imagefromfile}
"file_name": "graphical-twist.png",
"width": 300,
"unit": "px"
\end{imagefromfile}

The proof of this result is a simple untangling:

\begin{imagefromfile}
"file_name": "graphical-twist-proof.png",
"width": 300,
"unit": "px"
\end{imagefromfile}

## In fusion categories

In every fusion category, we automatically have that every object is isomorphic to its double dual. This is because fusion categories are semisimple, so $A\otimes A^{*}$ admitting a non-zero morphism into $1$ is the same as there being a $1$ in the simple object decomposition of $A\otimes A^{*}$, which in turn is the same as $1$ admitting a non-zero morphism into $A\otimes A^{*}$.

It is a deep conjecture of Etingof, Nikshych, and Ostrik that every fusion category is pivotal. This conjecture was proposed in their seminal work, [On fusion categories](#Etingof2005). What one gets a-priori, however, is a natural isomorphism between every object and its _quadruple_ dual, called the Radford isomorphism. This weaker isomorphism is already every powerful, and serves as an important tool in the theory of fusion categories.

## Related concepts

* **pivotal category

* [[rigid category]]

* [[fusion category]]

* [[spherical category]]

## References

* {#Etingof2005} [[Pavel Etingof]], [[Dmitri Nikshych]], [[Viktor Ostrik]], _On fusion categories_, Annals of Mathematics, [arXiv](https://arxiv.org/abs/math/0203060)

* {#Joyal1993} [[Andre Joyal]], [[Ross Street]], _Braided tensor categories_, Advances in Mathematics, [pdf](https://core.ac.uk/reader/82681130)

* {#Gelaki2006} [[Shlomo Gelaki]], _Nilpotent fusion categories_, Advances in Mathematics, [arXiv](https://arxiv.org/abs/math/0610726)

* {#Yetter1992} [[David Yetter]], _Framed tangles and a theorem of Deligne on braided deformations of tannakian categories_, Contemporary Mathematics, [web](http://www.ams.org/books/conm/134/)

* {#Bartlett2009} [[Bruce Bartlett]], _On unitary 2-representations of finite groups and topological quantum field theory_, PhD thesis, [arXiv](https://arxiv.org/abs/0901.3975)


[[!redirects pivotal category]]
[[!redirects pivotal categories]]
[[!redirects sovereign category]]
[[!redirects sovereign categories]]
[[!redirects pivotal structure]]
[[!redirects pivotal structures]]
