
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

A _simplicial Quillen adjunction_ is an [[adjunction]] 

$$
  (L \dashv R) : C \stackrel{\leftarrow}{\to} D
$$

of [[sSet]]-[[enriched functor]]s between [[simplicial model categories]] $C$ and $D$, such that the underlying adjunction of ordinary functors is a [[Quillen adjunction]] between the [[model category]] structures underlying the simplicial model categories.

## Properties

Simplicial Quillen adjunctions model pairs of [[adjoint (∞,1)-functor]]s in a fairly immediate manner: their restriction to fibrant-cofibrant objects is the [[sSet]]-[[enriched functor]] that presents the $(\infty,1)$-[[derived functor]] under the model of [[(∞,1)-categories]] by [[simplicially enriched categories]]. 

+-- {: .un_prop}
###### Proposition

Let $C$ and $D$ be [[simplicial model categories]] and let 

$$
  (L \dashv R) : C \stackrel{\overset{L}{\leftarrow}}{\underset{R}{\to}} D 
$$

be an [[sSet]]-[[enriched category theory|enriched]] [[adjunction]] whose underlying ordinary adjunction is a Quillen adjunction. Let $C^\circ$ and $D^\circ$ be the [[(∞,1)-categories]] presented by $C$ and $D$ (the [[Kan complex]]-enriched full [[sSet]]-subcategories on fibrant-cofibrant objects). Then the Quillen adjunction lifts to a pair of [[adjoint (∞,1)-functors]] 

$$
  (\mathbb{L} \dashv \mathbb{R}) : C^\circ \stackrel{\leftarrow}{\to} D^{\circ}
  \,. 
$$

On the [[decategorification|decategorified]] level of the [[homotopy category|homotopoy categories]] these are the total left and right [[derived functors]], respectively, of $L$ and $R$.

=--

+-- {: .proof}
###### Proof

This is proposition 5.2.4.6 in [[Higher Topos Theory|HTT]].

=--


The following proposition states conditions undeer which a Quillen adjunction may be detected already from knowing of the right adjoint only that it preserves fibrant objects (instead of all fibrations).

+-- {: .un_prop}
###### Proposition

The underlying [[adjunction]] of an [[SSet]]-[[enriched category theory|enriched]]-[[adjunction]] 

$$
  (L \dashv R) : C \stackrel{\overset{L}{\leftarrow}}{\underset{R}{\to}}
  D
$$

between [[simplicial model categories]] $C$ and $D$, where $D$ is a [[left proper model category]] is a Quillen adjunction precisely if

* $R$ preserves fibrant objects

* $L$ preserves cofibrations.


=--

+-- {: .proof}
###### Proof

This is proposition A.3.7.2 in [[Higher Topos Theory|HTT]].

=--

+-- {: .un_prop}
###### Proposition

If $C$ and $D$ are [[simplicial model categories]] and $D$ is a left [[proper model category]], then an [[sSet]]-enriched adjunction

$$
  (L \dashv R) : C \stackrel{\leftarrow}{\to} D
$$

is a Quillen adjunction already if $L$ preserves cofibrations and $R$ just fibrant objects.

=--

This appears as [[Higher Topos Theory|HTT, cor. A.3.7.2]].


[[!redirects simplicial Quillen adjunctions]]