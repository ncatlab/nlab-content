
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Equality and Equivalence
+-- {: .hide}
[[!include equality and equivalence - contents]]
=--
#### Category theory
+-- {: .hide}
[[!include category theory - contents]]
=--
=--
=--

# Equivalence
* table of contents
{: toc}

## Idea

In general two objects are considered _equivalent_ if they may be replaced by one another in all contexts under consideration (see also the *[[principle of equivalence]]*).

At the propositional level, the general theory of equivalence is discussed at [[equivalence relation]], but that leaves us with the question of the correct definition of equivalence in various situations.  Furthermore, we can work on a higher level and ask what the equivalences are, not just whether things are equivalent.


## In higher category theory

In [[higher category theory]] an **equivalence** often means a morphism which is invertible in a maximally weak sense (that is, up to all higher equivalences).  Two objects are **equivalent** if there is an equivalence between them.  For example:

* In a [[set]] (a $0$-[[0-category|category]]), equivalence is just [[equality]].

* In a [[category]] (a $1$-[[1-category|category]]), an equivalence is an [[isomorphism]].

* In a (possibly weak) $2$-[[2-category|category]], an equivalence is a morphism $f : x \to y$ such that there exists a morphism $g : y\to x$ and $2$-cell isomorphisms $f g \cong 1_y$ and $g f \cong 1_x$.  In the $2$-category [[Cat]] this reduces to the usual notion of [[equivalence of categories]] (although one must define $\Cat$ carefully using [[anafunctor]]s if one wants to avoid the [[axiom of choice]]).

* In a (possibly weak) $3$-[[3-category|category]], an equivalence is a morphism $f : x \to y$ such that there exists a morphism $g : y\to x$ and 2-cells $f g \to 1_y$ and $g f \to 1_x$ which are equivalences in the appropriate hom-2-categories.  In the (weak) 3-category $Bicat$ of [[bicategory|bicategories]], pseudofunctors, pseudonatural transformations, and modifications, such equivalences are often called _biequivalences_, and that term is sometimes also used for an equivalence in any $3$-category.

* In a (possibly weak) $\infty$-[[infinity-category|category]], an equivalence is a morphism $f : x \to y$ such that there exists a morphism $g : y\to x$ and 2-cells $f g \to 1_y$ and $g f \to 1_x$ which are equivalences in the appropriate hom-$\infty$-categories.  This can be made rigorous as a [[corecursion|corecursive definition]].

There is also the more structured/coherent notion of an [[adjoint equivalence]], but one hopes to have a theorem that any equivalence can be improved to an adjoint one.  This is known in some cases, including 2-categories, 3-categories, strict $\omega$-categories, and some models for $(\infty,1)$-categories.

In addition to this, there is the notion of [[equivalence of categories]] (and higher categories), which is on a separate page.  But it is related: properly done, two $n$-categories are equivalent if and only if they\'re equivalent as objects in the $(n+1)$-category of $n$-categories.


## In homotopy theory 

In the category [[Top]] of topological spaces, notions weaker than isomorphism become very important: [[homotopy equivalence]] and [[weak homotopy equivalence]].  The latter notion is generalized to [[weak equivalence]] for objects in any [[model category]].  There is also a notion of equivalence between model categories: [[Quillen equivalence]].  

These can be understood to some extent using higher categories.  For example, topological spaces should be weakly homotopy-equivalent if and only if they have equivalent [[fundamental infinity-groupoid|fundamental infinity-groupoids]].  Similarly, Quillen equivalent model categories give rise to equivalent [[(infinity,1)-category|(infinity,1)-categories]].

See [[equivalence in an (infinity,1)-category]].


## In homotopy type theory

In [[homotopy type theory]] equivalences can be axiomatized as those [[terms]] of [[function types]] all whose [[homotopy fibers]] are [[contractible]].

See _[[equivalence in homotopy type theory]]_.


## Related concepts

* [[principle of equivalence]]

* [[identity morphism]]

* [[identity type]]

* [[identity of indiscernibles]]

* [[equality]]

* [[isomorphism]], [[natural isomorphism]]

* **equivalence**, [[natural equivalence]]

* [[weak equivalence]]

* [[logical equivalence]]

* [[equivalence of groupoids]], [[equivalence of categories]]

* [[equivalence in a 2-category]]

* [[equivalence of 2-categories]], [[equivalence of (2,1)-categories]]

* [[homotopy equivalence]], [[weak homotopy equivalence]], [[Quillen equivalence]]

* [[Bousfield equivalence]]

* [[equivalence in an (∞,1)-category]]

* [[equivalence in homotopy type theory]]

* [[equivalence of (∞,1)-categories]]

[[!include logic symbols -- table]]


[[!redirects equivalence]]
[[!redirects equivalences]]
[[!redirects equivalent]]
