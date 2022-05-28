
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

Since $(\Delta^n)^{op} \star (\Delta^n)$ is preserved by taking opposites, this construction satisfies $Tw(C) = Tw(C^{op})$, and swaps the source and target maps.

The opposite convention often appears in the literature,
$$ 
  \overline{Tw}(C)_n = sSet((\Delta^n) \star (\Delta^n)^{op}, C)
$$
and comes with natural transformations
$\overline{src} : \overline{Tw}(C) \to C$ and $\overline{tgt} : \overline{Tw}(C) \to C^{op}$.

This satisfies $\overline{Tw}(C) \simeq Tw(C)^{op}$.

## Properties

If $C$ is a 1-category, then $Tw(C)$ agrees with the 1-categorical version. In the quasi-category model we have an even stronger statement

+-- {: .num_prop }
###### Proposition

If $C$ is a 1-category, there is an isomorphism $T : N(Tw(C)) \cong Tw(N(C))$ of simplicial sets, uniquely determined by the properties that $T(f) = f$ and that the projections are consistent with the obvious map $N(C^{op} \times C) \cong N(C)^{op} \times N(C)$.

=--
+-- {: .proof}
###### Proof

This is [Kerodon, prop 8.1.19](#Kerodon).

=--

For a quasi-category $C$, both $Tw(C)$ and $\overline{Tw}(C)$ are quasi-categories. This follows from the following characterization:

+-- {: .num_prop }
###### Proposition

* $Tw(C) \to C^{op} \times C$ is the left fibration classfied by the hom-space functor $C^{op} \times C \to \infty Gpd$.

* $\overline{Tw}(C) \to C \times C^{op}$ is the right fibration classified the hom-space functor $C^{op} \times C \to \infty Gpd$.

=--
+-- {: .proof}
###### Proof

This description of $\overline{Tw}(C)$ is [Lurie 4.2.5](#Lurie). The left fibration classified by a map is the opposite of the right fibration classified
by the same map. Alternatively, this is [Kerodon, Prop 8.1.1.10](#Kerodon).

=--

This means that we have the formulas $Tw(C) \simeq el(\hom_C) \simeq ({*} \downarrow \hom)$, just as in the 1-category version.


## Related concepts

* [[(∞,1)-end]]
* [[lax (∞,1)-colimit]]

## References

* {#Lurie} [[Jacob Lurie]], _[[Formal moduli problems]]_ 

* {#Kerodon} [[Kerodon]], *The Twisted Arrow Construction* [kerodon:03JF](https://kerodon.net/tag/03JF)