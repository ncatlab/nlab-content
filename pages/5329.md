
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### $(\infty,1)$-Category theory
+--{: .hide}
[[!include quasi-category theory contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Definition

+-- {: .num_defn }
###### Definition

An [[(∞,1)-category]] is **sifted** if a [[quasi-category]] $K \in sSet$ modelling it has the property that

1. it is not empty, $K \neq \emptyset$

1. The diagonal $K \to K \times K$ (in [[sSet]]) models a [[cofinal (∞,1)-functor]].

=--

## Properties

+-- {: .num_prop }
###### Proposition

Let $C$ be an [[(∞,1)-category]] such that [[products]] preserve [[sifted (∞,1)-colimits]] (for instance an [[(∞,1)-topos]], see [[universal colimits]]).

Then [[sifted (∞,1)-colimits]] preserve [[finite products]].

=--

This is ([Lurie, lemma 5.5.8.11](#Lurie)).




## Examples

### General

\begin{proposition}
The [[opposite category]] $\Delta^{op}$ of the [[simplex category]] is a sifted $(\infty,1)$-category.
\end{proposition}
([Lurie HTT, prop. 5.5.8.4](#LurieHTT)).

\begin{proposition}

Every [[filtered (∞,1)-category]] is sifted.

\end{proposition}
([Lurie HTT, prop. 5.3.1.20](#LurieHTT)).

### In categories of commutative monoids

+-- {: .num_prop }
###### Proposition


In a category of commutative monoids in a symmetric monoidal $(\infty,1)$-category, sifted colimits are computed as sifted colimits in the underlying $(\infty,1)$-category. 

=--

See [[commutative monoid in a symmetric monoidal (∞,1)-category]] for details.



## Related concepts

* [[sifted category]], **sifted $(\infty,1)$-category**

* [[filtered category]], [[filtered (∞,1)-category]]

## References
 

* {#LurieHTT} [[Jacob Lurie]], Section 5.5.8 of: _[[Higher Topos Theory]]_
  

[[!redirects sifted (infinity,1)-categories]]
[[!redirects sifted (∞,1)-category]]
[[!redirects sifted (∞,1)-categories]]

[[!redirects cosifted (infinity,1)-category]]
[[!redirects cosifted (infinity,1)-categories]]
[[!redirects cosifted (∞,1)-category]]
[[!redirects cosifted (∞,1)-categories]]
