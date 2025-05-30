
> This article is about arbitrary types satisfying the Rezk completion condition in [[simplicial type theory]]. For synthetic pre-categories satisfying the Rezk completion condition, see [[Rezk type]]

----

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### $(\infty,1)$-Category theory
+--{: .hide}
[[!include quasi-category theory contents]]
=--
#### Internal $(\infty,1)$-Categories
+--{: .hide}
[[!include internal infinity-categories contents]]
=--
#### Directed homotopy type theory
+-- {: .hide}
[[!include directed homotopy type theory - contents]]
=--
=--
=--

\tableofcontents

## Definition

In [[simplicial type theory]], let $\mathrm{iso}_A(x, y)$ be some notion of [[isomorphism in simplicial type theory|isomorphism]]. 

\begin{definition}
A type $A$ is a **Rezk complete type** if the canonical function which by the [[J rule]] takes an identification of elements $p:x =_A y$ to an isomorphism $J(\lambda t.\mathrm{id}_A(t), x, y, p):\mathrm{iso}_A(x, y)$ is an [[equivalence of types]] for all $x:A$ and $y:A$. 

$$\mathrm{isRezkComplete}(A) \coloneqq \prod_{x:A} \prod_{y:A} \mathrm{isEquiv}(\lambda p.J(\lambda t.\mathrm{id}_A(t), x, y, p))$$ 
\end{definition}

Equivalently, let $\mathbb{E}$ denote the [[free-standing isomorphism]], for some notion of [[isomorphism in simplicial type theory|isomorphism]]. For example, the free-standing bi-invertible morphism $\mathbb{E}$ can be defined as a colimit on a diagram involving the simplicial interval $\mathbb{I}$ (see [Sterling & Ye 2025](#SterlingYe25)). [[uniqueness quantifier|There is a unique]] function $u_\mathbb{E}:\mathbb{E} \to \mathbb{I}_h$ to the homotopical [[interval type|interval]] [[higher inductive type]] $\mathbb{I}_h$ by the [[universal property]] of the [[negative type|negative]] [[unit type]] and the equivalence of $\mathbb{I}_h$ with the negative unit type. 

\begin{definition}
A type $A$ is a **Rezk complete type** if the canonical function 

$$\lambda f.f \circ u_\mathbb{E}:(\mathbb{I}_h \to A) \to (\mathbb{E} \to A)$$

is an equivalence of types

$$\mathrm{isRezkComplete}(A) \coloneqq \mathrm{isEquiv}(\lambda f.f \circ u_\mathbb{E})$$
\end{definition}

## Related concepts

* [[simplicial type theory]]
* [[isomorphism in simplicial type theory]]
* [[simplicially discrete type]]
* [[Rezk type]]
* [[gaunt type]]
* [[univalent category]]

## References

* {#BuchholtzWeinberger21} [[Ulrik Buchholtz]], [[Jonathan Weinberger]], *Synthetic fibered $(\infty,1)$-category theory* $[$[arXiv:2105.01724](https://arxiv.org/abs/2105.01724), [talk slides](https://www.uwo.ca/math/faculty/kapulkin/seminars/hottestfiles/Weinberger-2022-01-20-HoTTEST.pdf)$]$

* {#SterlingYe25} [[Jonathan Sterling]], [[Lingyuan Ye]], *Domains and Classifying Topoi* ([arXiv:2505.13096](https://arxiv.org/abs/2505.13096))

[[!redirects Rezk complete type]]
[[!redirects Rezk complete types]]

[[!redirects Rezk-complete type]]
[[!redirects Rezk-complete types]]