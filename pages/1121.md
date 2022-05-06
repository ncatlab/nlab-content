
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Category theory
+--{: .hide}
[[!include category theory - contents]]
=--
#### Notions of subcategory
+-- {: .hide}
[[!include notions of subcategory]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Definition

Traditionally, a **wide subcategory** of a [[category]] $C$ is a [[subcategory]] containing all the [[objects]] of $C$. 

Equivalently, it is a subcategory through which the canonical [[functor]] $disc(Obj(C)) \to C$ (from the [[discrete category]] on the collection of [[objects]]) factors, or whose inclusion functor is [[bo functor|bijective on objects]].

Notice that the condition to contain all the objects is not invariant under [[equivalence of categories]] and so the definition of wide subcategory above violates the [[principle of equivalence]].  A variant of the definition which fixes this is:

an **essentially wide subcategory** contains at least one object from each [[isomorphism class]] of objects; that is, its inclusion functor is [[essentially surjective functor|essentially surjective on objects]].


A wide subcategory is also called a **lluf subcategory** ("lluf" being "[[full subcategory|full]]" spelled backwards).

##Wide subcategory of an abelian category##

An unrelated definition of "wide subcategory" is commonly used in the study of derived categories and stability conditions. In this context, a full subcategory $\mathcal{W}$ of an abelian category $\mathcal{A}$ is called **wide** if it is closed under kernels, cokernels and extensions. See, for example, [Hovey](https://doi.org/10.1090/S0002-9947-01-02747-7), [Ingalls and Thomas](https://doi.org/10.1112/S0010437X09004023) and [Marks and Stovicek](https://arxiv.org/abs/1503.04639).

Given a wide subcategory $\mathcal{W}$, one can consider the minimal [[torsion theory|torsion class]] $T(\mathcal{W})$ containing it. Conversely, if $\mathcal{T}$ is a torsion class, define $W(\mathcal{T})$ to be the full subcategory on those $X \in \mathrm{Ob}(\mathcal{T})$ such that, for any $Y \in \mathrm{Ob}(\mathcal{T})$ and any $g: Y \to X$, the kernel of $g$ is in $\mathcal{T}$. The composition $W \circ T$ is the identity, thus exhibiting the poset of wide subcategories as a retract of the poset of torsion classes. The surjection $W$ becomes an injection when restricted to [[functorially finite]] torsion classes, and is often a bijection between functorially finite torsion classes and functorially finite wide subcategories; see [Marks and Stovicek](https://arxiv.org/abs/1503.04639).

[[!redirects wide subcategory]]
[[!redirects wide subcategories]]
[[!redirects lluf subcategory]]
[[!redirects lluf subcategories]]
[[!redirects essentially wide subcategory]]
[[!redirects essentially wide subcategories]]
[[!redirects essentially lluf subcategory]]
[[!redirects essentially lluf subcategories]]
