
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Limits and colimits
+--{: .hide}
[[!include infinity-limits - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Definition

A _finite product_ is a [[product]] ([[Cartesian product]]) of a [[finite number]] of factors.

Finite products are generated from the empty product (the [[terminal object]]) and binary products (those with two factors, often -- but not always -- understood by default under "product".)

Similarly a _finite coproduct_ is a [[coproduct]] of a [[finite number]] of summands. This is generated from the empty coproduct (the [[initial object]]) and binary coproducts.

## Properties

+-- {: .num_example #CategoriesWithFiniteProductsAreCosifted}
###### Example
**([[categories with finite products are cosifted]])**

Let $\mathcal{C}$ be a [[small category]] which has [[finite products]]. Then $\mathcal{C}$ is a _[[cosifted category]]_, equivalently its [[opposite category]] $\mathcal{C}^{op}$ is a _[[sifted category]]_, equivalently [[colimits]] over $\mathcal{C}^{op}$ with values in [[Set]] are _[[sifted colimits]]_, equivalently [[colimits]] over $\mathcal{C}^{op}$ with values in [[Set]] _[[limits commuting with colimits|commute]] with [[finite products]]_, as follows:

For $\mathbf{X}, \mathbf{Y} \in [\mathcal{C}^{op}, Set]$ to [[functors]] on the [[opposite category]] of $\mathcal{C}$ (hence two [[presheaves]] on $\mathcal{C}$) we have a [[natural isomorphism]]

$$
  \underset{\underset{\mathcal{C}^{op}}{\longrightarrow}}{\lim}
  \left(
    \mathbf{X} \times \mathbf{Y}
  \right)
  \;\simeq\;
  \left(
    \underset{\underset{\mathcal{C}^{op}}{\longrightarrow}}{\lim}
    \mathbf{X}
  \right)
  \times
  \left(
    \underset{\underset{\mathcal{C}^{op}}{\longrightarrow}}{\lim}
    \mathbf{Y}
  \right)
  \,.
$$ 

=--


## Related concepts

* [[finite limit]]

* [[Lawvere theory]], [[essentially algebraic theory]]




[[!redirects finite product]]
[[!redirects finite products]]

[[!redirects finite co-product]]
[[!redirects finite co-products]]

[[!redirects finite coproduct]]
[[!redirects finite coproducts]]

[[!redirects binary product]]
[[!redirects binary products]]


