
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Foundations
+-- {: .hide}
[[!include foundations - contents]]
=--
=--
=--

# Principle of Unique Choice
* table of contents
{: toc}

## Idea

The __principle of unique choice__, also known as __function comprehension__, is the principle that every [[total relation|total]] [[functional relation|functional]] [[relation]] determines a (necessarily unique) function. 

This is true in [[classical logic]] and most forms of [[intuitionistic logic]] (for example the [[internal language]] of any [[topos]]), but fails in weaker systems such as the internal language of a [[tripos]], or one of the internal languages of a [[quasitopos]].

## 2-Categorical Formulation

A total, functional relation is precisely an [[adjunction]] in the [[bicategory]] of relations [[Rel]]. So the principle of unique choice can be seen as a functor $Adj(Rel) \to Set$, in fact, an [[equivalence of categories]]. For this reason, bicategories modeling relations such as [[cartesian bicategories]] or [[allegories]] can be used to model functions as well by using the adjoint pairs of relations.

However, note that a generalization from [[Rel]] to the bicategory [[Prof]] of categories and [[profunctors]] is not possible: in general an adjoint pair of profunctors determines only a [[semifunctor]], which can be improved to a [[functor]] if the codomain category is [[Cauchy complete]]. For this reason, sometimes people use algebraic structures modeling profunctors such as [[proarrow equipments]] and [[virtual double categories]] that include notions of functor in addition to profunctor.

## In dependent type theory

In dependent type theory, the **type-theoretic principle of unique choice** states that the dependent product type of a family of contractible types is pointed. 

$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma, x:A \vdash B(x) \; \mathrm{type} \quad \Gamma, x:A \vdash p(x):\mathrm{isContr}(B(x))}{\Gamma\vdash \mathrm{uniquechoice}(\lambda x.p(x)):\prod_{x:A} B(x)}$$

The [[principle of unique choice]] is not equivalent to [[weak function extensionality]]. Weak function extensionality states that the dependent product type of a family of contractible types is contractible.

$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma, x:A \vdash B \; \mathrm{type} \quad \Gamma, x:A \vdash p(x):\mathrm{isContr}(B(x))}{\Gamma\vdash \mathrm{weakfunext}(\lambda x.p(x)):\mathrm{isContr}\left(\prod_{x:A} B(x)\right)}$$

## Related concepts

* [[anafunction]]

## References

* *Homotopy Type Theory: Univalent Foundations of Mathematics*, The [[Univalent Foundations Project]], Institute for Advanced Study, 2013. ([web](http://homotopytypetheory.org/book/), [pdf](http://hottheory.files.wordpress.com/2013/03/hott-online-323-g28e4374.pdf))

[[!redirects principle of unique choice]]
[[!redirects function comprehension principle]]
[[!redirects function comprehension]]
[[!redirects axiom of unique choice]]
[[!redirects unique choice]]

[[!redirects set theoretic principle of unique choice]]
[[!redirects set-theoretic principle of unique choice]]

[[!redirects set theoretic axiom of unique choice]]
[[!redirects set-theoretic axiom of unique choice]]

[[!redirects type theoretic principle of unique choice]]
[[!redirects type-theoretic principle of unique choice]]

[[!redirects type theoretic axiom of unique choice]]
[[!redirects type-theoretic axiom of unique choice]]