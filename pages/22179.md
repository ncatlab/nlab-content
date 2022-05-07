
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Category theory
+-- {: .hide}
[[!include category theory - contents]]
=--
=--
=--

#Contents#
* table of contents
{: toc}

## Idea

This is the generalization of [[twisted arrow category]] to (∞,1)-categories.

## Definition

In the case of [[quasi-category|quasicategories]], we can give an explicit definition. For a quasi-category $C$ we define the twisted arrow quasi-category $Tw(C)$ to be 
$$ 
  Tw(C)_n = sSet((\Delta^n)^{op} \star (\Delta^n), C)
$$
The insertions into the components of the join determine natural transformations
$src : Tw(C) \to C^{op}$ and $tgt : Tw(C) \to C$.

The alternate convention often appears in the literature,
$$ 
  \overline{Tw}(C)_n = sSet((\Delta^n) \star (\Delta^n)^{op}, C)
$$
and comes with natural transformations
$\overline{src} : \overline{Tw}(C) \to C$ and $\overline{tgt} : \overline{Tw}(C) \to C^{op}$.

These two constructions are related by

* $\overline{Tw}(C) = Tw(C^{op})^{op}$
* $\overline{src}_C = tgt_{C^{op}}^{op}$
* $\overline{tgt}_C = src_{C^{op}}^{op}$

## Properties

If $C$ is a 1-category, then $Tw(C)$ agrees with the 1-categorical version.

For a quasi-category $C$, both $Tw(C)$ and $\overline{Tw}(C)$ are quasi-categories.

+-- {: .num_prop }
###### Proposition

* $Tw(C) \to C^{op} \times C$ is the left fibration classfied by the hom-space functor $C^{op} \times C \to \infty Gpd$.

* $\overline{Tw}(C) \to C \times C^{op}$ is the right fibration classified the hom-space functor $C^{op} \times C \to \infty Gpd$.

=--
+-- {: .proof}
###### Proof

This description of $\overline{Tw}(C)$ is [Lurie 4.2.5](#Lurie). By the relationship between $Tw$ and $\overline{Tw}$, we have that $Tw(C)$ is classified by $(x,y) \mapsto C^{op}(y,x)$.
=--

This means that we have the formulas $Tw(C) \simeq el(\hom_C) \simeq ({*} \downarrow \hom)$, just as in the 1-category version.


## Related concepts

* [[(∞,1)-end]]
* [[lax (∞,1)-colimit]]

## References

* {#Lurie} [[Jacob Lurie]], _[[Formal moduli problems]]_ 