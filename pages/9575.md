
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Category theory
+-- {: .hide}
[[!include category theory - contents]]
=--
#### Homotopy theory
+--{: .hide}
[[!include homotopy - contents]]=--
=--
=--



#Contents#
* table of contents
{:toc}

## Idea

The notion of a  **relative category** is an extremely weak version of a [[category with weak equivalences]], providing the bare minimum needed to present an [[(∞,1)-category]]. The idea was first explored in a series of papers [Dwyer & Kan 1980](#DwyerKan1980Localizations) on [[simplicial localization]] (see there for more). A [[model category]] structure on relative categories was constructed by [Barwick & Kan 2012](#BarwickKan12), presenting the [[(∞,1)-category of (∞,1)-categories]].

More generally, the notion of relative category captures the idea of having a distinguished [[wide subcategory]] of morphisms that should be preserved by functors. Relative categories are occasionally used for this purpose, unrelated to any higher categorical purpose.

## Definition

### Basic

A **relative category** $C$ is a [[pair]] $(und C, weq C)$, where $und C$ is a [[category]] and $W$ is a [[wide subcategory]]. A [[morphism]] in $weq C$ is said to be a **[[weak equivalence]]** in $C$. A **relative functor** $f : C \to D$ is a [[functor]] $f \colon und C \to und D$ that preserves weak equivalences in the obvious sense.

The **[[homotopy category]]** of a relative category $C$ is the ordinary category $Ho C$ obtained from $und C$ by [[localization|freely inverting]] the weak equivalences in $C$. 

### Refinements

* A **semi-saturated relative category** is a relative category $C$ such that every [[isomorphism]] in $und C$ is a weak equivalence in $C$.

* A [[category with weak equivalences]] is a semi-saturated relative category $C$ such that $weq C$ has the [[two-out-of-three property]].

* A [[homotopical category]] is a relative category $C$ such that $weq C$ has the [[two-out-of-six property]]; note that this automatically makes $C$ a category with weak equivalences.

* A **saturated homotopical category** is a relative category $C$ such that a morphism is a weak equivalence _if and only if_ it is invertible in $Ho C$; note that any such relative category must be a homotopical category in particular.



## Examples

Any ordinary [[category]] $C$ gives rise to three relative categories in a functorial way:

* A **minimal relative category** $min C$, in which the only weak equivalences are [[identity morphism|identities]].

* A **minimal homotopical category** $min^+ C$, in which the only weak equivalences are [[isomorphism|isomorphisms]].

* A **maximal homotopical category** $max C$, in which every morphism is a weak equivalence.




## Properties

### As enriched categories
 {#AsEnrichedCategories}

The application of relative categories as expressing the idea of having a subcategory of distinguished morphisms can be neatly packaged into viewing relative categories as [[enriched categories]] over the category of sets with distinguished subsets (see also at *[[F-category]]* for a [[2-category]]-theoretic version of this idea).

Let $PairSet$ be the [[cartesian closed category]] whose objects are pairs of small sets $(X, A)$ such that $A \subseteq X$, and whose morphisms $(X, A) \to (Y, B)$ are functions $f : X \to Y$ with $f(A) \subseteq B$.


+-- {: .num_prop}
###### Proposition

$RelCat$ is isomorphic to the category of small $PairSet$-enriched categories.

=--

+-- {: .proof} 
###### Proof 

With minimal rephrasing, a small $PairSet$-enriched category consists of the data

* A small set of objects $C$
* For objects $X,Y$, a small set $C(X,Y)$ with a subset $W(X,Y)$
* For objects $X,Y,Z$, a composition $C(Y,Z) \times C(X,Y) \to C(X,Z)$
that restricts to $W(Y,Z) \times W(X,Y) \to W(X,Z)$
* For objects $X$, a choice of identity element $id_X \in W(X,X)$

that is subject to identity and associativity relations. It's immediate that this is exactly the same data as a relative category $(C,W)$. And under this identification, enriched functors and relative functors are the same thing.

=--


### Categories of relative categories

Let $\mathbf{RelCat}$ be the [[large category]] of [[small category|small]] relative categories and relative functors. It is a [[locally presentable category|locally finitely presentable]] [[cartesian closed category]], and we refer to the [[exponential object]] $[C, D]_h$ as the **relative functor category**. $\mathbf{RelCat}$ is, in particular, a ([[strict 2-category|strict]]) [[2-category]].

Let $\mathbf{SsRelCat}$ be the full subcategory of semi-saturated relative categories. The inclusion $\mathbf{SsRelCat} \hookrightarrow \mathbf{RelCat}$ has a left [[adjoint]] that preserves finite [[product|products]], so $\mathbf{SsRelCat}$ is a [[reflective subcategory|reflective]] [[exponential ideal]] of $\mathbf{RelCat}$.

There are then the following strings of [[adjunctions]]:
$$min \dashv und \dashv max \dashv weq : \mathbf{RelCat} \to \mathbf{Cat}$$
$$Ho \dashv min^+ : \mathbf{Cat} \to \mathbf{RelCat}$$
$$Ho \dashv min^+ \dashv und \dashv max \dashv weq : \mathbf{SsRelCat} \to \mathbf{Cat}$$
Moreover, because $min^+$ embeds $\mathbf{Cat}$ as a reflective exponential ideal in $\mathbf{SsRelCat}$ and in $\mathbf{RelCat}$, the functor $Ho : \mathbf{SsRelCat} \to \mathbf{Cat}$ preserves finite products.


### Model structures

A relative category can be equipped with a [[weak model structure]],
left or right [[semimodel structure]], or a [[model structure]].
(These are listed from less restrictive to more restrictive structures.)

These structures do not change the underlying [[(∞,1)-category]].
However, the do provide constructions to perform computations
in the underlying [[(∞,1)-category]].
Different structures yield different constructions,
but all resulting answers are weakly equivalent.

### Presentation of $(\infty,1)$-categories

The theory of relative categories presents a theory of [[(∞,1)-category|(∞,1)-categories]] in the following sense:


+-- {: .num_theorem}
###### Theorem
There exists an adjunction
$$K_\xi \dashv N_\xi : \mathbf{RelCat} \to \mathbf{ssSet}$$
such that every left [[Bousfield localization of model categories|Bousfield localization]] of the [[Reedy model structure]] on the category $\mathbf{ssSet}$ of [[bisimplicial sets]] induces a [[cofibrantly generated model category|cofibrantly-generated]] [[proper model category|left proper]] [[model category|model structure]] on $\mathbf{RelCat}$ making the adjunction a [[Quillen equivalence]]. In particular, there exists a model structure on $\mathbf{RelCat}$ that is Quillen equivalent to the [[model structure for complete Segal spaces]] on $\mathbf{ssSet}$.
=--

This is discussed in further detail at [[model structure on categories with weak equivalences]].






## Related concepts

* [[simplicial localization]]

* [[F-category]]

* [[M-category]]

* [[marked simplicial set]]

## References

* {#DwyerKan1980Localizations} [[William Dwyer]], [[Daniel Kan]], _Simplicial localizations of categories_ , J. Pure Appl. Algebra 17 (1980), 267&#8211;284. ([pdf](http://www.nd.edu/~wgd/Dvi/SimplicialLocalizations.pdf))
  
* {#BarwickKan12} [[Clark Barwick]], [[Daniel Kan]], _Relative categories: Another model for the homotopy theory of homotopy theories_. Indagationes Mathematicae 23 (2012) pp. 42&#8211;68 ([arXiv:1011.1691](https://arxiv.org/abs/1011.1691))


[[!redirects relative categories]]
