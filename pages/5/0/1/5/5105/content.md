
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### 2-Category theory
+-- {: .hide}
[[!include 2-category theory - contents]]
=--
#### Equality and Equivalence
+--{: .hide}
[[!include equality and equivalence - contents]]
=--
=--
=--

\tableofcontents



## Definition

An **equivalence of $2$-categories** is the appropriate notion of [[equivalence of categories|equivalence]] between [[2-categories]]. This consists of:

* [[2-functors]] ${}\;F\colon C\to D$ and $G\colon D\to C$, and
* [[pseudonatural transformations]] ${}\;G \circ F \to Id_C$ and $F \circ G \to Id_D$ which are themselves [[equivalences]], i.e. there are pseudonatural transformations forming their inverses up to isomorphism.

The definition makes sense, and is used, both in the case that $F$ is strict, and in the case that it is weak. Note however that in this case $G$ should be allowed to be weak: see Example 3.1 in [Lack2002](#Lack2002).

In the literature this sort of equivalence is often called a **biequivalence**, as it has traditionally been associated with [[bicategories]], the standard algebraic definition of weak $2$-category.  There is a stricter notion of equivalence for strict $2$-categories, which traditionally is called just a *$2$-equivalence* and which on the nLab is called a [[strict 2-equivalence]].

A (weak or strict) 2-functor can be made into part of an equivalence iff it is essentially surjective on objects, essentially full on 1-cells (i.e. essentially surjective on Hom-categories), and fully faithful on 2-cells.

## Properties


\begin{prop}\label{CharacterizationOfEquivalencesOf2Categories}
**(recognition of [[equivalences of 2-categories]] assuming the [[axiom of choice]])**
\linebreak
  Assuming the [[axiom of choice]], a 2-functor $F \,\colon\, \mathcal{C} \xrightarrow{\;} \mathcal{D}$ is an [[equivalence of 2-categories]] precisely if it is

1. **essentially surjective**:  

   [[surjection|surjective]] on [[equivalence in a 2-category|equivalence]] [[equivalence classes|classes]] of [[objects]]: $\pi_0(F) \;\colon\; \pi_0(\mathcal{C}) \twoheadrightarrow \pi_0(\mathcal{D})\;$,

1. **fully faithful**:

   for each [[pair]] of [[objects]] $X,\, Y \in \mathcal{C}$ the component functor is an [[equivalence of categories|equivalence of]] [[hom-categories]] $F_{X,Y} \,\colon\, \mathcal{C}(X,Y) \xrightarrow{\simeq} \mathcal{D}\big(F(X), F(Y)\big)$, 

   which by the analogous theorem for 1-functors ([this Prop.](equivalence+of+categories#ViaEssentiallySurjectiveAndFullyFaithful)) means equivalently that $F$ is

   1. **essentially full on 1-cells**:

      namely that each component functor $F_{X,Y}$ is an [[essentially surjective functor]];

   1. **fully faithful on 2-cells**:

      namely that each component functor $F_{X,Y}$ is a [[fully faithful functor]].

\end{prop}

This is classical. It may be found made explicit in [Johnson & Yau 2020, Thm. 7.4.1 with Def. 7.0.1](#JohnsonYau20). 


## Internalization

Just as the notion of [[equivalence of categories]] can be [[internalization|internalized]] in any $2$-category, the notion of equivalence for $2$-categories can be internalized in any $3$-category in a straightforward way.  The version above for $2$-categories then results from specializing this general definition to the (weak) $3$-category $2 Cat$ of $2$-categories, (weak) $2$-functors, pseudonatural transformations, and modifications.

There is one warning to keep in mind here.  Every $3$-category is equivalent to a [[semi-strict n-category|semi-strict]] sort of $3$-category called a [[Gray-category]], since it is a category [[enriched category|enriched]] over the monoidal category [[Gray]] of strict $2$-categories and strict $2$-functors.  Of course $Gray$ itself is a Gray-category, but as such it is [not](http://arxiv.org/abs/math/0612299) equivalent to the weak $3$-category $2 Cat$ of weak $2$-categories and *weak* $2$-functors.

In particular, an "internal (bi)equivalence" in $Gray$ consists of *strict* $2$-functors $F,G$ together with pseudonatural equivalences relating $G F$ and $F G$ to identities.  This is a semistrict notion of equivalence, intermediate between the fully weak notion and the fully strict one.

## Related concepts

* [[equality]], [[isomorphism]], [[equivalence]]

* [[weak equivalence]], [[homotopy equivalence]], [[weak homotopy equivalence]]

* [[homotopy equivalence of toposes]]

* [[equivalence in an (∞,1)-category]]

* [[equivalence of categories]], [[adjoint functor]]

* **equivalence of 2-categories**, [[2-adjunction]]

* [[equivalence of (2,1)-categories]]

* [[equivalence of (∞,1)-categories]], [[adjoint (∞,1)-functor]]

[[!include properties of functors -- contents]]


## References

* {#Lack2002} [[Stephen Lack]], _A Quillen model structure for 2-categories_, K-Theory 26, No. 2, 171-205 (2002). [Zentralblatt review](https://zbmath.org/?q=an%3A1017.18005) [author's webpage](http://maths.mq.edu.au/~slack/papers/qmc2cat.html) 

* {#Zheng12} Weizhe Zheng, prop. 1.6 of _Gluing pseudofunctors via $n$-fold categories_ ([arXiv:1211.1877](http://arxiv.org/abs/1211.1877))

* {#JohnsonYau20} [[Niles Johnson]], [[Donald Yau]], Section 7 of: _2-Dimensional Categories_, Oxford University Press 2021 ([arXiv:2002.06055](http://arxiv.org/abs/2002.06055), [doi:10.1093/oso/9780198871378.001.0001](https://oxford.universitypressscholarship.com/view/10.1093/oso/9780198871378.001.0001/oso-9780198871378))


[[!redirects equivalence of 2-categories]]
[[!redirects equivalences of 2-categories]]
[[!redirects equivalence of bicategories]]
[[!redirects equivalences of bicategories]]

[[!redirects eqivalence of 2-categories]]
[[!redirects eqivalences of 2-categories]]

[[!redirects equivalence of 2-groupoids]]
[[!redirects equivalences of 2-groupoids]]
[[!redirects equivalence of bigroupoids]]
[[!redirects equivalences of bigroupoids]]

[[!redirects biequivalence]]
[[!redirects biequivalences]]