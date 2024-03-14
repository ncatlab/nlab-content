

#Contents#
* table of contents
{:toc}


## Idea

**Optics** are constructions used in [[computer science]] as bidirectional data accessors. They include [[lens (in computer science)|lenses]] and prisms, used to access and modify, respectively, components of product data types and components of coproduct data types.

Unlike [[lens (in computer science)|lenses]], in general optics do not require a cartesian structure to be present. That's replaced by a bi-[[actegory|actegorical]] structure and a quotient which 'ties' residual and incoming views.

## Definition

Let $(\mathbf M, I, \otimes)$ be a symmetric monoidal category. Let $\mathbf C$ and $\mathbf D$ be $\mathbf M$-[[actegories]], i.e. there are pseudoactions $\bullet$ and $\ast$ of $\mathbf M$ acting on $\mathbf C$ and $\mathbf D$, respectively.

\begin{definition}
The category of $(\mathbf C, \mathbf D)$-mixed optics $\mathrm{Optic}_{\bullet, \ast}(\mathbf C, \mathbf D)$ has objects given by pairs $(X : \mathbf C,Y : \mathbf D)$ and hom-sets given by
$$
  \mathrm{Optic}_{\bullet, \ast}(\mathbf C, \mathbf D)((S,T),(A,B)) = \int^{M : \mathbf M} \mathbf C(S, M \bullet A) \times \mathbf D(M \ast B, T)
$$
Optics are morphisms in this category. See [Riley 2018](#Riley18) for the composition rule.
\end{definition}

\begin{remark}
Concretely, an optic $(S,T) \to (A,B)$ is specified by a triple of $(l, M, r)$ where $M : \mathbf M$ is called *residual*, $l : S \to M \bullet A$ is called 'view' or 'get' or 'forward part' or 'left part', and $r : M \ast B \to T$ is called 'update' or 'put' or 'backward part' or 'right part'.
\end{remark}

\begin{remark}
  In the non-mixed case $\mathbf M = \mathbf C = \mathbf D$, the category of optics is defined exactly as the 'double' of $\mathbf C$ as introduced by Pastro and Street in [PS07](#PS07). Their theory has been extended to the mixed case in [CEGLMPR20](#CEGLMPR20). This provides the fundamental link between optics and the theory of [[Tambara modules]], which gives to mixed-optics the alternative name of 'profunctor optics'. See ['Profunctor representation'](#Profunctor+representation).
\end{remark}

The [[coend]] in the above definition has the effect of making two optics $(l, M, r)$ and $(l', M', r')$ (with same boundaries) equal if there exists a morphism $\alpha : M \to M'$ such that $(\alpha' \bullet A) \circ l = l'$ or a morphism $\beta:M' \to M$ such that $r = r' \circ (\beta \ast B)$.

One says optics are defined _up to sliding_ along the residual, a terminology suggested by the graphical representation of optics as open diagrams, see ([Román](#Roman)).

## Profunctor representation

Let $(\mathbf M, I, \otimes)$ be a monoidal V-category with two monoidal actions $(\bullet) \colon \mathbf{M} \otimes \mathbf{C} \to \mathbf{C}$ and $(\ast) \colon \mathbf{M} \otimes \mathbf{D} \to \mathbf{D}$. 
A generalized **Tambara module** is a V-profunctor $P \colon \mathbf{C}^{op} \otimes \mathbf{D} \to \mathbf{V}$ endowed with a family of morphisms
  \[t_{M,A,B} \colon P(A,B) \to P(M \bullet A, M \ast B)\]
V-natural in $A \in \mathbf{C}$ and $B \in \mathbf{D}$ and V-dinatural in $M \in \mathbf{M}$, which additionally satisfies some axioms, see [PS07](#PS07).

Generalized Tambara modules are the copresheaves of the category of optics, see [CEGLMPR20](#CEGLMPR20). 

## References

A brief account of the purpose of optics is in:

* [[Bartosz Milewski]], _Optics for the Working Mathematician_, ([blog post](https://bartoszmilewski.com/2021/09/08/optics-for-the-working-mathematician/))

A similar, but more detailed account, is in:

* Emily Pillmore, [[Mario Román]], _Profunctor Optics: The Categorical View_, ([blog post](https://golem.ph.utexas.edu/category/2020/01/profunctor_optics_the_categori.html#more))

Articles:

* {#Riley18} [[Mitchell Riley]], *Categories of optics*, &lbrack;[arXiv:1809.00738](https://arxiv.org/abs/1809.00738), video:[YT](https://www.youtube.com/watch?v=Qy7Y4-mgwbw)&rbrack;

* {#CEGLMPR20} [[Bryce Clarke]], Derek Elkins, [[Jeremy Gibbons]], [[Fosco Loregian]], [[Bartosz Milewski]], Emily Pillmore, [[Mario Román]], _Profunctor optics: a categorical update_, Compositionality **6** 1 (2024) ([arXiv:2001.07488](https://arxiv.org/abs/2001.07488), [doi:10.32408/compositionality-6-1](https://doi.org/10.32408/compositionality-6-1))

* {#Roman} [[Mario Román]], _Open Diagrams via Coend Calculus_, Electronic Proceedings in Theoretical Computer Science **333** (2021) 65-78 ([doi:10.4204/EPTCS.333.5](https://doi.org/10.4204/EPTCS.333.5))

[[!redirects optics (in computer science)]]




