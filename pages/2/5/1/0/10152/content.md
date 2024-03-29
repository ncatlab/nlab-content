+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Homotopy theory
+--{: .hide}
[[!include homotopy - contents]]
=--
#### Model category theory
+--{: .hide}
[[!include model category theory - contents]]
=--
#### $(\infty,1)$-Limits and colimits
+--{: .hide}
[[!include infinity-limits - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}


## Idea

The **simplicial bar construction** is a way of building a cofibrant [[resolution]] of a diagram, suitable for computing [[homotopy colimit|homotopy colimits]] in [[simplicial model category|simplicial model categories]].

## Definition

Let $\mathcal{V}$ be a [[cocomplete category|cocomplete]] [[symmetric monoidal category|symmetric]] [[monoidal closed category]] and let $\mathbb{C}$ be a small $\mathcal{V}$-[[enriched category|category]]. We define a [[simplicial object]] $W_\bullet (c', \mathbb{C}, c)$ for each pair $(c', c)$ of objects in $\mathbb{C}$ by
$$W_n (c', \mathbb{C}, c) = \coprod_{(c_0, \ldots, c_n)} \mathbb{C} (c_n, c') \otimes \mathbb{C} (c_{n-1}, c_n) \otimes \cdots \otimes \mathbb{C} (c_0, c_1) \otimes \mathbb{C} (c, c_0)$$
with the obvious face and degeneracy operators induced by the composition and identities of $\mathbb{C}$. Note that $W_\bullet (\blank, \mathbb{C}, \blank)$ is a $\mathcal{V}$-functor $\mathbb{C}^{op} \otimes \mathbb{C} \to [\mathbf{\Delta}^{op}, \mathcal{V}]$.

Let $\mathcal{M}$ be a [[copower|tensored]] $\mathcal{V}$-category. The **two-sided simplicial bar construction** of a $\mathcal{V}$-diagram $F : \mathbb{C} \to \mathcal{M}$ weighted by a $\mathcal{V}$-functor $G : \mathbb{C}^{op} \to \mathcal{V}$ is a simplicial object $B_\bullet (G, \mathbb{C}, F)$ equipped with isomorphisms
$$\mathcal{M} (B_n (G, \mathbb{C}, F), M) \cong \int_{(c', c) : \mathbb{C}^{op} \otimes \mathbb{C}} \mathcal{V} (W_n (c', \mathbb{C}, c), \mathcal{M}(G c' \odot F c, M))$$
that are natural in $n$ and $\mathcal{V}$-natural in $M$, where the integral sign on the right hand side denotes a $\mathcal{V}$-[[end]].

Now suppose a [[cosimplicial object]] $\Delta^\bullet : \mathbf{\Delta} \to \mathcal{V}$ is given, so that we may define the [[realisation]] of a simplicial object $X_\bullet$ in a $\mathcal{V}$-category as the [[weighted colimit]] $\left| X_\bullet \right| = \Delta^\bullet \star X_\bullet$. The **two-sided bar construction** of $F : \mathbb{C} \to \mathcal{M}$ weighted by $G : \mathbb{C}^{op} \to \mathcal{V}$ is then defined to be the geometric realisation of the two-sided simplicial bar construction:
$$B (G, \mathbb{C}, F) = \left| B_\bullet (G, \mathbb{C}, F) \right|$$

## Properties

+-- {: .num_prop}
###### Proposition

If $\mathcal{M}$ is a tensored $\mathcal{V}$-category and has coproducts for small families of objects, then $\mathcal{M}$ has two-sided simplicial bar constructions for all diagrams and weights. If $\mathcal{M}$ is moreover $\mathcal{V}$-cocomplete, then $\mathcal{M}$ also has two-sided bar constructions.

=--

+-- {: .num_prop}
###### Proposition

If $\mathcal{M}$ is a tensored $\mathcal{V}$-category and has coproducts for small families of objects, then:

* For each $\mathcal{V}$-diagram $F : \mathbb{C} \to \mathcal{M}$, the $\mathcal{V}$-functor $B_n (-, \mathbb{C}, F) : [\mathbb{C}^{op}, \mathcal{V}] \to \mathcal{M}$ has a right $\mathcal{V}$-[[adjoint functor|adjoint]].

If $\mathcal{M}$ is also _cotensored_, then:

* For each weight $G : \mathbb{C}^{op} \to \mathcal{V}$, the $\mathcal{V}$-functor $B_n (G, \mathbb{C}, -) : [\mathbb{C}, \mathcal{M}] \to \mathcal{M}$ has a right $\mathcal{V}$-adjoint.

=--

+-- {: .num_prop}
###### Proposition

Let $W (c', \mathbb{C}, c)$ be the realisation of $W_\bullet (c', \mathbb{C}, c)$. If $\mathcal{M}$ is a cotensored $\mathcal{V}$-cocomplete $\mathcal{V}$-category, then there are isomorphisms
$$\mathcal{M} (B (G, \mathbb{C}, F), M) \cong \int_{(c', c) : \mathbb{C}^{op} \otimes \mathbb{C}} \mathcal{V} (W (c', \mathbb{C}, c), \mathcal{M} (G c' \odot F c, M))$$
that are $\mathcal{V}$-natural in $M$.

=--

The next theorem is essentially a version of the Fubini theorem for coends.

+-- {: .num_prop}
###### Theorem

Let $F : \mathbb{C} \to \mathcal{M}$, $G : \mathbb{D}^{op} \to \mathcal{V}$, and $H : \mathbb{C}^{op} \times \mathbb{D} \to \mathcal{V}$ be $\mathcal{V}$-functors. If $\mathcal{M}$ is a _cotensored_  $\mathcal{V}$-cocomplete $\mathcal{V}$-category, then we have the following isomorphism:
$$B (B (G, \mathbb{D}, H), \mathbb{C}, F) \cong B (G, \mathbb{D}, B (H, \mathbb{C}, F))$$

=--

## Applications

As stated in the introduction, the two-sided simplicial bar construction can be used to compute homotopy colimits.

Let us write $y c$ for the representable $\mathcal{V}$-functor $\mathbb{C}(-, c)$ and $B (\mathbb{C}, \mathbb{C}, F)$ for the diagram $c \mapsto B (y c, \mathbb{C}, F)$. 

+-- {: .num_prop}
###### Theorem

Let $\mathcal{M}$ be a [[simplicial model category]] and let $\mathbb{C}$ be a small category.

1. For each diagram $F : \mathbb{C} \to \mathcal{M}$, there is a [[weak equivalence]] $B (y c, \mathbb{C}, F) \to F c$ that is natural in $F$ and $c$.
2. The functor $colim : [\mathbb{C}, \mathcal{M}] \to \mathcal{M}$ preserves weak equivalences between diagrams of the form $B (\mathbb{C}, \mathbb{C}, F)$ where $F$ is a diagram such that each $F c$ is a cofibrant object in $\mathcal{M}$.
3. The functor $B (1, \mathbb{C}, Q -) : [\mathbb{C}, \mathcal{M}] \to \mathcal{M}$, where $Q : \mathcal{M} \to \mathcal{M}$ is a cofibrant replacement functor, is a left [[derived functor]] for $colim : [\mathbb{C}, \mathcal{M}] \to \mathcal{M}$, i.e. it computes [[homotopy colimit|homotopy colimits]].

=--

## References

* [[Mike Shulman|Shulman, M.]], _Homotopy limits and colimits and enriched homotopy theory_ ([arXiv:math/0610194](http://arxiv.org/abs/math/0610194)).
