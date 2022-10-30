
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Complex geometry
+--{: .hide}
[[!include complex geometry - contents]]
=--
#### Cohomology
+--{: .hide}
[[!include cohomology - contents]]
=--
=--
=--
> under construction

## Idea

For some algebraic [[site]]/[[(∞,1)-site]] such as the [[étale site]] or the [[étale (∞,1)-site]], write $\mathcal{B}$ for the [[(∞,1)-topos of (∞,1)-sheaves]] over that site. For $S\in \mathcal{B}$ any object, write $\mathcal{B}_{/S}$ for its [[slice (∞,1)-topos]].
 
Here $\mathcal{B}$ contains a canonical [[group object in an (∞,1)-category|group object]] $\mathbb{G}_m \in Grp(\mathbf{B})$, the absolute [[multiplicative group]] given as an [[(∞,1)-presheaf]] by the assignment which sends any [[commutative ring]]/[[E-∞ ring]] to its [[group of units]]/[[∞-group of units]]

$$
  \mathbb{G}_m \;\colon\; R \mapsto R^\times
  \,.
$$

The [[inverse image]] of $\mathbb{G}_m$ under [[base change]] along $S \to \ast$ we will still denote by $\mathbb{G}_m \in Grp(\mathcal{B})$.

Write $\mathbf{B}\mathbb{G}_m$ for the [[delooping]] of $\mathbb{G}_m$. 

For $X \in \mathcal{B}_{/X}$ any object, then morphisms

$$
  X \longrightarrow \mathbf{B}\mathbb{G}_m
$$

modulate $\mathbb{G}_m$-[[principal ∞-bundles]] on $X$, whose canonically [[associated ∞-bundles]] are $\mathbb{G}_a$-[[∞-line bundles]]. (...)

The [[internal hom]]/[[mapping stack]]

$$
  \mathbf{Pic}(X) \coloneqq \underset{X}{\prod} [X,\mathbf{B}\mathbb{G}_m]
  \in 
  \mathcal{S}
$$

is the _Picard stack_ of $X$.

In good cases its [[truncated object in an (∞,1)-topos|0-truncation]] is a [[scheme]], in which case it is called the _[[Picard scheme]]_.

## References

* [[The Stacks Project]], _[The Picard stack](http://stacks.math.columbia.edu/tag/0372)_



[[!redirects Picard stack]]
[[!redirects Picard stacks]]
