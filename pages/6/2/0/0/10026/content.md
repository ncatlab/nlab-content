[[!redirects structures in presheaf toposes]]

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Topos Theory
+-- {: .hide}
[[!include topos theory - contents]]
=--
#### Model theory
+-- {: .hide}
[[!include model theory - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Statement

+-- {: .num_prop}
###### Proposition

Let $\mathbb{T}$ be a [[geometric theory]] over a [[signature (in logic)|signature]] $\Sigma$ and let $\mathcal{C}$ be a [[small category]]. Then there is an [[equivalence of categories]]

$$
  \mathbb{T}Mod([\mathcal{C}, Set])
  \simeq
  [\mathcal{C}, \mathbb{T}Mod(Set)]
$$

between the [[category of models]] in the [[presheaf topos]] over $\mathcal{C}^{op}$ and the [[category of presheaves]] with values in $\mathbb{T}$-models.

=--

For instance ([Johnstone, cor. D1.2.14](#Johnstone)).

Note that this continues to work for theories which involve infinitary limits as well. (The key observation is just that limits in $[\mathcal{C}, Set]$ are taken pointwise.)

## Examples

+-- {: .num_example}
###### Example

A _[[group object]]_ in a [[presheaf topos]] is equivalently a presheaf of [[groups]]. This is a fact used a lot for instance in [[homological algebra]] (for [[abelian groups]]). See at _[[group object]]_ for more.

=--

## Related concepts

* [[categorical semantics]]


## References

Around cor. D1.2.14 in

* [[Peter Johnstone]], _[[Sketches of an Elephant]]_
 {#Johnstone}