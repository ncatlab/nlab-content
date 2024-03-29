[[!redirects family of (∞,1)-operads]]

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Higher algebra
+--{: .hide}
[[!include higher algebra - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Definition

For the following we model [[(∞,1)-operads]] $\mathcal{O}$ specifically by their [[(∞,1)-categories of operators]] $\mathcal{O}^\otimes$ and these specifically as [[quasi-categories]].

Let $\mathcal{C}$ be an [[(∞,1)-category]]. A **$\mathcal{C}$-family of [[(∞,1)-operads]]**, is a [[fibration]] in the [[model structure for quasi-categories]]

$$
  p \colon \mathcal{O}^{\otimes}  \to \mathcal{C} \times FinSet_*
$$

such that

* For $C \in \mathcal{C}$ any [[object]], for $X \in \mathcal{O}^\otimes_C$ over $\langle n\rangle \in FinSet_*$, and for $\alpha \colon \langle n\rangle \to \langle k\rangle$ any [[inert morphism]], then there exists a $p$-[[coCartesian morphism]] $\overline \alpha \colon X \to Y$ in $\mathcal{O}^\otimes_C$.

([Lurie, 2.3.2.10](#Lurie))

## Properties

### Relation to generalized $(\infty,1)$-operads

For $\mathcal{C}$ an [[(∞,1)-category]], a  [[fibration]] $\mathcal{O}^\otimes \to \mathcal{C} \times FinSet_*$ in the [[model structure for quasi-categories]] is a $\mathcal{C}$-family of $(\infty,1)$-operads precisely if it is a fibration of [[generalized (∞,1)-operads]] such that the underlying map $\mathcal{O}^\otimes_{\langle 0\rangle} \to \mathcal{C}$ is an [[acyclic Kan fibration]].

## References

* [[Jacob Lurie]], _[[Higher Algebra]]_
 {#Lurie}

[[!redirects families of (∞,1)-operads]]
