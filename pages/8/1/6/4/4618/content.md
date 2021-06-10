
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Model category theory
+--{: .hide}
[[!include model category theory - contents]]
=--
#### Enriched category theory
+--{: .hide}
[[!include enriched category theory contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Definition

A _simplicial Quillen adjunction_ is an [[sSet]]-[[enriched Quillen adjunction]]: an [[enriched adjunction]] 

$$
  (L \dashv R) : C \stackrel{\leftarrow}{\to} D
$$

of [[sSet]]-[[enriched functor]]s between [[simplicial model categories]] $C$ and $D$, such that the underlying adjunction of ordinary functors is a [[Quillen adjunction]] between the [[model category]] structures underlying the simplicial model categories.

## Properties

### Presentation of $\infty$-adjunctions

Simplicial Quillen adjunctions model pairs of [[adjoint (∞,1)-functor]]s in a fairly immediate manner: their restriction to fibrant-cofibrant objects is the [[sSet]]-[[enriched functor]] that presents the $(\infty,1)$-[[derived functor]] under the model of [[(∞,1)-categories]] by [[simplicially enriched categories]]. 

+-- {: .un_prop}
###### Proposition

Let $C$ and $D$ be [[simplicial model categories]] and let 

$$
  (L \dashv R) 
  \;\colon\; 
  C \stackrel{\overset{L}{\leftarrow}}{\underset{R}{\to}} D 
$$

be an [[sSet]]-[[enriched category theory|enriched]] [[adjunction]] whose underlying ordinary adjunction is a Quillen adjunction. Let $C^\circ$ and $D^\circ$ be the [[(∞,1)-categories]] presented by $C$ and $D$ (the [[Kan complex]]-enriched full [[sSet]]-subcategories on fibrant-cofibrant objects). Then the Quillen adjunction lifts to a pair of [[adjoint (∞,1)-functors]] 

$$
  (\mathbb{L} \dashv \mathbb{R}) 
  \;\colon\; 
  C^\circ \stackrel{\leftarrow}{\to} D^{\circ}
  \,. 
$$

On the [[decategorification|decategorified]] level of the [[homotopy category|homotopoy categories]] these are the total left and right [[derived functors]], respectively, of $L$ and $R$.

=--

+-- {: .proof}
###### Proof

This is proposition 5.2.4.6 in [[Higher Topos Theory|HTT]].

=--

### Recognition {#Recognition}

The following proposition states conditions under which a simplicial Quillen adjunction may be detected already from knowing of the right adjoint only that it preserves fibrant objects (instead of all fibrations).


+-- {: .un_prop}
###### Proposition

If $C$ and $D$ are [[simplicial model categories]] and $D$ is a left [[proper model category]], then for an [[sSet]]-enriched adjunction

$$
  (L \dashv R) : C \stackrel{\leftarrow}{\to} D
$$

to be a Quillen adjunction it is already sufficient that $L$ preserves cofibrations and $R$ just fibrant objects.

=--

This appears as [[Higher Topos Theory|HTT, cor. A.3.7.2]].

+-- {: .un_remark}
###### Remark

This is in particular useful for finding simplicial Quillen adjunctions into [[Bousfield localization of model categories|left Bousfield localizations]] of left proper model categories: the left Bousfield localization keeps the cofibrations unchanged and preserves left properness, and the fibrant objects in the Bousfield localized structure have a good characterization: they are the fibrant objects in the original model structure that are also [[local object]]s with respect to the set of morphisms at which one localizes. 

Therefore for $D$ the left Bousfield localization of a simplicial left proper model category $E$ at a [[class]] $S$ of morphisms, for checking the Quillen adjunction property of $(L \dashv R)$ it is sufficient to check that $L$ preserves cofibrations, and that $R$ takes fibrant objects $c$ of $C$ to such fibrant objects of $E$ that have the property that for all $f \in S$ the [[derived hom-space]] map $\mathbb{R}Hom(f,R(c))$ is a weak equivalence.

=--


## Related concepts

* [[Quillen adjunction]]

* **simplicial Quillen adjunction**

* [[Quillen equivalence]]

* [[monoidal Quillen adjunction]]



[[!redirects simplicial Quillen adjunctions]]