
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Categorical algebra
+-- {: .hide}
[[!include categorical algebra -- contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Defintion


Given a [[monad]] $T \;\colon\; \mathcal{C} \to \mathcal{C}$, its **unit** is the [[natural transformation]] 

$$
  \epsilon \;\colon\; id_{\mathcal{C}} \to T
$$ 

which is part of the definition of _[[monad]]_. Hence for every [[object]] $X \in \mathcal{C}$ the component of the unit on $X$ is a [[morphism]] 

$$
  \epsilon_X \;\colon\; X \to T(X)
$$

in $\mathcal{C}$.

[[duality|Dually]], there is a _counit of a comonad_.

## Properties

### Relation to adjunctions

If $(L \dashv R)$ is an [[adjunction]] that gives rise to the monad $T$ as $T \simeq R \circ L$, then the unit of the monad is equivalently the [[unit of an adjunction|unit of the adjunction]].

## Related concepts

* [[unit]]

  * [[unit object]]

  * [[unit of an adjunction]]

  * **unit of a monad**


[[!redirects counit of a comonad]]

[[!redirects monad unit]]
[[!redirects monad units]]
