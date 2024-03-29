
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
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

To the extent that a [[monoidal functor]] is analogous to a [[monoid]], a _module over a monoidal functor_ is analogous to a [[module]] over (hence an [[action]] of) that monoid.

## Definition

+-- {: .num_defn}
###### Definition

Let 

1. $\mathcal{C},\mathcal{D}$ be [[monoidal categories]], hence equipped with tensor product functors $\otimes_{\mathcal{C}}\colon \mathcal{C} \times \mathcal{C}\to \mathcal{C}$ and $\otimes_{\mathcal{D}}\colon \mathcal{D} \times \mathcal{D}\to \mathcal{D}$;

1. $\mathcal{N}$ be a left [[module category]] over $\mathcal{C}$, hence equipped with a compatible [[action]] functor $\rho \colon \mathcal{C}\times\mathcal{N} \to \mathcal{N}$;

1. $F \colon \mathcal{C}\to \mathcal{D}$ a [[lax monoidal functor]].

Then a _left module_ over $F$ is 

1. a functor $N \colon \mathcal{N} \longrightarrow \mathcal{D}$ 

1. a [[natural transformation]]

   $\alpha \colon F(-)  \otimes_{\mathcal{D}} N(-)  \longrightarrow N(\rho(-,-))$

satisfying the evident [[categorification]] of the [[action]]-property.
Analogously for right modules and bimodules. (e.g. [Yetter 01, def. 39](#Yetter01)).

=--

## Example

* For $(\mathcal{C},\otimes)$ a [[symmetric monoidal category]] and the [[functor category]] $([\mathcal{C},Set],\otimes_{Day})$ equipped with the induced [[Day convolution]] product, then a [[monoid object]] with respect to $\otimes_{Day}$ is equivalently a [[lax monoidal functor]] from $\mathcal{C}$ to itself, and a [[module object]] over that monoid is equivalently a module over that functor in the above sense. See [there](Day+convolution#Monoids) for more.

## References

* {#Yetter01} [[David Yetter]], _Abelian categories of modules over a (Lax) monoidal functor_ ([arXiv:math/0112307](http://arxiv.org/abs/math/0112307))

[[!redirects modules over a monoidal functor]]

[[!redirects modules over monoidal functors]]
