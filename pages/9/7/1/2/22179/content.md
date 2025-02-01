
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

By [Kerodon, tag 03K9](#Kerodon), this definition respects equivalences between quasi-categories, and thus descends to a functor $Tw : (\infty,1)Cat \to (\infty,1)Cat$.

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

If $C$ is a 1-category, there is an isomorphism $T : N(Tw(C)) \cong Tw(N(C))$ of simplicial sets, uniquely determined by the properties that $T(f) = f$ and that the source and target maps are consistent with the obvious map $N(C^{op} \times C) \cong N(C)^{op} \times N(C)$.

=--
+-- {: .proof}
###### Proof

This is [Kerodon, tag 03JN](#Kerodon).

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
by the same map. Alternatively, this is [Kerodon, tag 03JQ](#Kerodon).

=--

This means that we have the formulas $Tw(C) \simeq el(\hom_C) \simeq ({*} \downarrow \hom)$, just as in the 1-category version.

We can say more:

+-- {: .num_prop }
###### Proposition

If $C \to D$ is an inner fibration of simplicial sets, then 
the universal map
$$Tw(C) \to (C^{op} \times C) \times_{D^{\op} \times D} Tw(D)$$
is a left fibration.

=--
+-- {: .proof}
###### Proof

This is [Kerodon, tag 03JT](#Kerodon).

=--

+-- {: .num_cor}
###### Corollary

$Tw : sSet \to sSet$ is a right Quillen functor with respect to the [[model structure for quasicategories ]]

=--
+-- {: .proof}
###### Proof

Let $L$ be the left adjoint. $L$ preserves monomorphisms, so we need to show it preserves trivial cofibrations. The [[model structure for quasicategories ]] is a Cisinski model structure, so a map is a trivial cofibration iff it has the left lifting property against fibrations between fibrant objects, which in this case are the categorical fibrations between quasicategories.

Suppose $i$ is a trivial cofibration, and let $f : C \to D$ be a categorical fibration between quasi-categories. Since [[left Kan fibrations]] are categorical fibrations, the previous lemma implies $Tw(f)$ is a categorical fibration between quasicategories, so $i \perp Tw(f)$, and thus $L(i) \perp f$.

=--

## Related concepts

* [[(∞,1)-end]]

* [[lax (∞,1)-colimit]]

* [[twisted arrow category]]

* [[twisted arrow modality]]

## References

* {#Lurie} [[Jacob Lurie]], _[[Formal moduli problems]]_ 

* {#Kerodon} [[Kerodon]], *The Twisted Arrow Construction* $[$[kerodon:03JF](https://kerodon.net/tag/03JF)$]$

* {#MR22} [[Chirantan Mukherjee]], [[Nima Rasekh]], *Twisted Arrow Construction for Segal Spaces* ([arXiv:2203.01788](https://arxiv.org/abs/2203.01788))

[[!redirects twisted arrow (∞,1)-categories]]

[[!redirects twisted arrow (infinity,1)-category]]
[[!redirects twisted arrow (infinity,1)-categories]]

[[!redirects twisted arrow construction]]
[[!redirects twisted arrow constructions]]

[[!redirects twisted arrows construction]]
[[!redirects twisted arrows constructions]]