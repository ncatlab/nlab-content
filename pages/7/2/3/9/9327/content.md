
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### $(\infty,1)$-Category theory
+--{: .hide}
[[!include quasi-category theory contents]]
=--
#### Monoidal categories
+--{: .hide}
[[!include monoidal categories - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

A _cartesian symmetric monoidal (∞,1)-category_ is a [[symmetric monoidal (∞,1)-category]] whose [[tensor product]] is given by the categorical [[product]]. 
This is dual to the notion of [[cocartesian symmetric monoidal (∞,1)-category]].

In the special case that the underlying [[(∞,1)-category]] is equivalent to just a [[1-category]], then this is equivalently a [[cartesian symmetric monoidal category]].

## Definition

\begin{definition}
  A [[symmetric monoidal ∞-category]] $\mathcal{C}^{\otimes}$ is **Cartesian** if the following conditions are satisfied:

1. The unit object $1_{\mathcal{C}} \in \mathcal{C}$ is final, and

2. For every pair of objects $C,D \in \mathcal{C}$, the canonical maps
$$
  C \simeq C \otimes 1_{\mathcal{C}} \leftarrow C \otimes D \rightarrow 1_{\mathcal{C}} \otimes D \simeq D
$$
exhibit $C \otimes D$ as the product $C \times D$.

\end{definition}

Equivalently, for $n \geq 0$, we stipulate that the $n$-ary tensor product $\otimes:\mathcal{C}^n \rightarrow \mathcal{C}$ is [[right adjoint]] to the $n$-ary diagonal map $\Delta:\mathcal{C} \rightarrow \mathcal{C}^n$.

## Properties
### Rigidity
[HA 2.4.1.5](#Lurie) constructs a [[Cartesian symmetric monoidal ∞-category]] structure $\mathcal{C}^\times$ on $\mathcal{C}$ whenever $\mathcal{C}$ has all finite products, and by unwinding definitions, $\mathcal{C}$ has all finite products if it attains a Cartesian symmetric monoidal structure.

Additionally, [HA 2.4.1.7](#Lurie) characterizes functors from Cartesian symmetric monoidal $\infty$-categories to the particular construction of [HA 2.4.1.5](#2.4.1.5), including constructing a canonical equivalence.
We may summarize these results as the following, wherein $\mathrm{Cat}_\infty^\times$ denotes the subcategory of $\mathrm{Cat}_\infty$ whose objects are $\infty$-categories possessing finite products and whose morphisms are product-preserving functors.
\begin{theorem}
  Lurie's construction yields a fully faithful functor $(-)^\times:\mathrm{Cat}_\infty^{\times} \hookrightarrow \mathrm{Cat}_\infty^{\otimes}$ whose image is spanned by the Cartesian symmetric monoidal $\infty$-categories.
\end{theorem}

### $\mathcal{O}$-algebras as $\mathcal{O}$-monoids 
{#O-monoids}
Given $\mathcal{O}^{\otimes}$ an [[∞-operad]] and $\mathcal{C}$ an [[∞-category]], we say that a functor $\mathcal{O}^{\otimes} \rightarrow \mathcal{C}$ is an **$\mathcal{O}$-monoid** if, given an object $\mathbf{X} = (X_i \in \mathcal{O})_{i \leq n} \in \mathcal{O}_{\langle n \rangle}$ the canonical maps
$$
  \left\{M(\mathbf{X}) \rightarrow M(X_i) \right\}
$$
induced by cocartesian transport in $\mathcal{O}^\otimes$ exhibit $M(\mathbf{X})$ as a product $M(\mathbf{X}) \simeq \prod_{i \leq n}(M(x_i))$.The following is [HA 2.4.2.5](#Lurie).

\begin{proposition} 
  If $\mathcal{C}$ has finite products, then the forgetful functor $\mathrm{Alg}_{\mathcal{O}}(\mathcal{C}^{\times}) \rightarrow \mathrm{Fun}(\mathcal{O}^{\otimes}, \mathcal{C})$ is fully faithful with image spanned by the $\mathcal{O}$-monoids.
\end{proposition}


### Coalgebra objects
 {#CoalgebraObjects}

 Every object in a Cartesian monoidal $\infty$-category is canonically a [[comonoid object]] via the [[diagonal map]] (just as in the 1-categorical case [here](comonoid#InACartesianMonoidalCategory)). 

See also at _[[(infinity,n)-category of correspondences]]_ the section _[Via coalgebras](%28infinity%2Cn%29-category+of+correspondences#DefinitionViaCoalgebras)_.]

## Related concepts

* [[cocartesian monoidal (infinity,1)-category]]


## References

Section 2.4 of 

* {#Lurie} [[Jacob Lurie]], _[[Higher Algebra]]_
 
[[!redirects cartesian monoidal (infinity,1)-categories]]


[[!redirects cartesian monoidal (∞,1)-category]]
[[!redirects cartesian monoidal (∞,1)-categories]]


[[!redirects Cartesian monoidal (infinity,1)-category]]
[[!redirects Cartesian monoidal (infinity,1)-categories]]

[[!redirects Cartesian monoidal (∞,1)-category]]
[[!redirects Cartesian monoidal (∞,1)-categories]]

[[!redirects cartesian monoidal infinity,1-category]]
[[!redirects cartesian monoidal infinity,1-categories]]


[[!redirects Cartesian monoidal infinity,1-category]]
[[!redirects Cartesian monoidal infinity,1-categories]]

[[!redirects Cartesian symmetric monoidal ∞-category]]
[[!redirects Cartesian symmetric monoidal ∞-categories]]

[[!redirects cartesian symmetric monoidal ∞-category]]
[[!redirects cartesian symmetric monoidal ∞-categories]]


[[!redirects Cartesian symmetric monoidal (∞,1)-category]]
[[!redirects Cartesian symmetric monoidal (∞,1)-categories]]

[[!redirects cartesian symmetric monoidal (∞,1)-category]]
[[!redirects cartesian symmetric monoidal (∞,1)-categories]]