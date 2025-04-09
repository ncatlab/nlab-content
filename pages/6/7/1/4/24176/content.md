
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Category theory
+-- {: .hide}
[[!include category theory - contents]]
=--
#### Homotopy theory
+--{: .hide}
[[!include homotopy - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea ##

There is a canonical way to turn any [[category]] in [[homotopy type theory]] into a [[weak equivalence|weakly equivalent]] [[univalent category]]. This can be thought of as an analogue of [[univalence]] but for [[isomorphisms]] instead of [[equivalence]].

Intuitively, the Rezk completion is a "strictification via Yoneda" type result, in the style of [[Yoneda lemma for bicategories|strictification for bicategories via Yoneda]]. One starts with a category that may not have nice strictness properties, embeds it into the category of presheaves, which does have the nice strictness properties, and then restricts to representables, which gives something equivalent to the original category, but retains the nice strictness properties.

Another intuition is that the Rezk completion is a [[vertical
categorification]] of the construction of a [[quotient]] of a type by
an [[equivalence relation]] by taking [[equivalence classes]]. That
is, we can think of a type $X$ equipped with an equivalence relation
as a [[boolean]]-enriched groupoid, and a boolean-valued presheaf is
equivalently a predicate on $X$ that respects the equivalence
relation. Then the representable presheaves are those predicates that
are furthermore inhabited, i.e., precisely equivalence classes.

## Construction ##

We work in a [[dependent type theory]] where [[UIP]] or [[axiom K]] cannot be proven. These results are from [UFP13](#UFP13). Note: [UFP13](#UFP13)  calls a [[category]] a "[[precategory]]" and a [[univalent category]] a "category", but here we shall refer to the standard terminology of "category" and "univalent category" respectively. 

\begin{theorem}\label{Theorem995}
**(Theorem 9.9.5 in [UFP13](#UFP13))**
For any [[category]] $A$, there is a [[univalent category]] $\hat{A}$ and a [[weak equivalence]] $A\to \hat{A}$.
\end{theorem}
\begin{proof}
Let $\hat{A}_0$ be the type of [[representable]] objects of $\mathit{Set}^{A^{\mathrm{op}}}$, with hom-sets inherited from $\mathit{Set}^{A^{\mathrm{op}}}$. Then the inclusion $\hat{A} \to \mathit{Set}^{A^{\mathrm{op}}}$ is [[fully faithful]] and an [[embedding]] on [[objects]]. Since $\mathit{Set}^{A^{\mathrm{op}}}$ is a category by Theorem 9.2.5 (see [[functor category]]), $\hat{A}$ is also a category. Let $A \to \hat{A}$ be the [[Yoneda embedding]]. This is [[fully faithful]] by corollary 9.5.6 (See [[Yoneda embedding]]), and [[essentially surjective]] by definition of $\hat{A}_0$. Thus it is a [[weak equivalence]].
\end{proof}

* $\hat{A}_0\equiv \sum_{(F : \mathit{Set}^{A^{\mathrm{op}}})} \sum_{(a:A)} \mathbf{y} a \cong F$

This has the unfortunate side effect of raising the [[universe]] level. If $A$ is a [[univalent category]] in a universe $\mathcal{U}$, then in this proof $\mathit{Set}$ must at least be as large as $\mathit{Set}_{\mathcal{U}}$. Hence the univalent category $\mathit{Set}_{\mathcal{U}}$ is in a higher universe than $\mathcal{U}$ hence $\mathit{Set}^{A^{\mathrm{op}}}$ must also be in a higher universe and finally $\hat{A}$ is also in a higher universe than $\mathcal{U}$.

Now this can all be avoided by constructing a [[higher inductive type]] $\hat{A}$ with constructors:

* A function $i : A_0 \to \hat{A}_0$.
* For each $a,b:A$ and $e: a \cong b$, an equality $j e : i a = i b$
* For each $a : A$, an equality $j(1_a)=refl_{i a}$.
* For each $a,b,c:A$, $f : a \cong b$, and $g : b \cong c$, an equality $j(g \circ f)=j(f) \cdot j(g).$
* 1-truncation: for all $x,y:\hat{A}_0$ and $p,q: x = y$ and $r,s : p = q$, an equality $r=s$.

If we ignore the last constructor we could also write the above as $\| \hat{A}_0 \|_1$.

We now go on to build a univalent category $\hat{A}$ with a [[weak equivalence]] $A \to \hat{A}$ by taking the type of objects as $\hat{A}_0$ and defining hom-sets by double [[induction]]. The advantage of this approach is that it preserves [[universe]] levels, there are a lot of things to check but it is an easy proof. The kind of proof that is well suited to a proof assistant. For the complete proof see Theorem 9.9.5 of the [[HoTT book]].

## Related concepts
 
* [[Segal completion]]

* [[category theory]]

* [[Yoneda lemma]]

* [[weak equivalence]]

* [[higher inductive type]]

## References ##

The relation between [[complete Segal space|Segal completeness]] (now often "Rezk completion") for [[internal categories in HoTT]] and the [[univalence axiom]] had been pointed out in:

* [[Urs Schreiber]], _[Segal completenes and Univalence](https://golem.ph.utexas.edu/category/2012/05/segalcompleteness_and_univalen.html)_ (2012)

This was developed in

* {#AhrensKapulkinShulman13} [[Benedikt Ahrens]], [[Chris Kapulkin]], [[Michael Shulman]], _Univalent categories and the Rezk completion_, Mathematical Structures in Computer Science **25** 5 (*From type theory and homotopy theory to Univalent Foundations of Mathematics*),  (2015) 1010-1039   $[$[arXiv:1303.0584](https://arxiv.org/abs/1303.0584), [doi:10.1007/978-3-319-21284-5_14](https://doi.org/10.1007/978-3-319-21284-5_14)$]$

See also:

* {#UFP13} [[Univalent Foundations Project]], *[[HoTT book|Homotopy Type Theory – Univalent Foundations of Mathematics]]* (2013)

* {#Rijke17} [[Egbert Rijke]], *The join construction*, 26 Jan 2017, ([arXiv:1701.07538](https://arxiv.org/abs/1701.07538))

[[!redirects Rezk complete]]
[[!redirects Rezk completeness]]

category: category theory