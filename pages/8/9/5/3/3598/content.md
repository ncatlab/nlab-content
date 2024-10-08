
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Type theory
+-- {: .hide}
[[!include type theory - contents]]
=--
#### Bundles
+-- {: .hide}
[[!include bundles - contents]]
=--
=--
=--

# Contents
* table of contents
{: toc}

## Idea

In [[type theory]], a **display map** &lbrack;[Taylor 1983-7, §4.3.2](#Taylor87)&rbrack; is a [[morphism]] $p\colon B\to A$ in a [[category]] which represents a [[dependent type]] under [[categorical semantics of dependent type theory]].

That is, $B$ represents (interprets) a [[type]] [[dependent type|dependent]] on a [[variable]] of type $A$, usually written syntactically as $x\colon A \vdash B(x)\colon Type$.  The intended intuition is that $B(x)$ is the [[fiber]] of the map $p$ over $x\colon A$.

More specifically, the [[syntactic category]] of a type theory is naturally equipped with a class of maps called "display maps" which come from its type dependencies, while [[models]] for such a [[theory]] can be studied in any other category equipped with a suitable class of maps called "display maps."  By the [usual](type%20theory#CategoricalSemantics) [[adjunction]], such models are then equivalent to functors out of the syntactic category which preserve the relevant structure, including the display maps.

Since the most common dependent type theories include [[dependent product]] types, and any display map in a category that represents semantics for such a theory must be [[exponentiable morphism|exponentiable]], the term **display map** is sometimes used to mean any exponentiable morphism.

Sometimes all maps are display maps.  This happens particularly in 
[[extensional type theory]], such as versions of the [[internal logic]] of categories that include dependent types.

In the context of _[[homotopy type theory]]_ display maps are [[fibrations]], for instance in a [[type-theoretic model category]].


## Definition

+-- {: .num_defn #CategoryWithDisplays}
###### Definition

For $\mathcal{C}$ a [[category]], a [[class]] $D \subset Mor(\mathcal{C})$ of [[morphisms]] of $\mathcal{C}$ is called a **class of displays** if 

* All [[pullbacks]] of elements of $D$ exist and belong to $D$.
=--

It follows automatically that the [[full subcategory]] on $D$ of the [[arrow category]] $\Arr(\mathcal{C})$ is [[replete subcategory|replete]]; in other words, the [[property]] of $\mathcal{C}$-morphisms given by membership in $D$ respects the [[principle of equivalence]].


+-- {: .num_defn #well-rooted}
###### Definition

The category with displays is called **well rooted** if it has a [[terminal object]] $1$ and all the morphisms to $1$ are display maps.
=--

It follows that binary [[products]] exist and their [[projections]] are display maps.


+-- {: .num_defn #closed}
###### Definition

Often (which simplifies matters) $D$ is __closed under composition__:

1. Every [[identity morphism]] (and hence every [[isomorphism]]) belongs to $D$.

2. The [[composite]] of a [[composable pair]] of elements of $D$ belongs to $D$.
=--


+-- {: .num_defn #interpretation}
###### Definition

An __interpretation__ or __[[model]]__ of a category with class of displays $(\mathcal{C}, D)$ in another category with displays $(\mathcal{C}', D')$ is a  [[functor]]
$$
  S\colon \mathcal{C} \to \mathcal{C}'
$$
which preserves display maps and their pullbacks.
=--

This appears as ([Taylor 1999, def. 8.3.2](#Taylor99)).


## Examples

+-- {: .num_example}
###### Examples

Examples of categories with displays, def. \ref{CategoryWithDisplays}, include

1. One extreme: any [[locally cartesian category]] $\mathcal{C}$ with the class of all morphisms. (This is well rooted ---if $\mathcal{C}$ has a terminal object--- and closed under composition.) 

2. Another extreme: any category with the empty class of no morphisms.

3. Modifying (2) for an extreme case closed under composition: any category with the class of [[isomorphisms]].

4. Modifying (2) for an extreme well-rooted case: A category $\mathcal{C}$ with finite [[products]] and $D$ the class of product [[projections]] $X \times A \to X$. (This is also closed under composition.)

5. A [[locally cartesian category]] $\mathcal{C}$ (such as a [[topos]]) equipped with its class of [[monomorphisms]]. (This is closed under composition.)

6. A category equipped with a [[singleton pretopology]]. (This is closed under composition.)

7. (...) 
=--

See also [Taylor 1999, Exp. 8.3.6](#Taylor99).


## Related pages

* [[clan]]

* [[bundle]]

* [[categorical semantics of dependent type theory]]

* [[dominion]]

## References

The notion is due to

* {#Taylor87} [[Paul Taylor]], §4.3.2 in: *Recursive Domains, Indexed Category Theory and Polymorphism*, Cambridge (1983-7) &lbrack;[[Taylor-IndexedCategoryTheory.pdf:file]]&rbrack;

* {#Taylor99} [[Paul Taylor]], Section 8.3 in: _[[Practical Foundations of Mathematics]]_, Cambridge University Press (1999) &lbrack;[webpage](http://www.paultaylor.eu/~pt/prafm/index.html)&rbrack;
  



[[!redirects category with display map]]
[[!redirects category with display maps]]
[[!redirects display map]]
[[!redirects display maps]]
[[!redirects display morphism]]
[[!redirects display morphisms]]



