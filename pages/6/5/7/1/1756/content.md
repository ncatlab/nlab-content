#Contents#
* automatic table of contents goes here
{:toc}

#Idea#

Quillen adjunctions are one convenient notion of morphism between [[model category|model categories]].  They induce adjunctions between the [[(infinity,1)-category|(infinity,1)-categories]] [[presentable (infinity,1)-category|presented]] by the model categories.


# Definition #

For $C$ and $D$ two [[model category|model categories]], a pair $(F,G)$

$$
  D \stackrel{G}{\to} C
$$
$$
  D \stackrel{F}{\leftarrow} C
$$
of [[adjoint functor]]s (with $F$ [[left adjoint]]) is a **Quillen adjunction** if the following equivalent conditions are satisfied:

* $F$ preserves cofibrations and acyclic cofibrations;

* $G$ preserves fibrations and trivial fibrations;

* $F$ preserves cofibrations and $G$ preserves fibrations;

* $F$ preserves trivial cofibrations and $G$ preserves trivial fibrations.

#Properties#

+-- {: .un_prop}
###### Proposition


It follows from the definition that

* the [[left adjoint]] $F$ preserves weak equivalences between cofibrant objects;

* the [[right adjoint]] $G$ preserves weak equivalences between fibrant objects.

=--


+-- {: .proof}
###### Proof

To show this for instance for $G$, we may argue as in a 
[[category of fibrant objects]] and apply the _factorization lemma_
which shows that every weak equivalence between fibrant objects may be
factored, up to [[homotopy]], as a [[span]] of acyclic fibrations.

These weak equivalences are preserved by $F$ and hence 2-out-of-3 the claim follows. 

For $G$ we apply the formally dual argument.

=--

+-- {: .un_prop}
###### Proposition

Let $C$ and $D$ be [[simplicial model categories]] and let 

$$
  (L \dashv R) : C \stackrel{\leftarrow}{\to} D 
$$

be an [[sSet]]-[[enriched category theory|enriched]] [[adjunction]] whose underlying ordinary adjunction is a Quillen adjunction. Let $C^\circ$ and $D^\circ$ be the [[(∞,1)-categories]] presented by $C$ and $D$ (the [[Kan complex]]-enriched full [[sSet]]-subcategories on fibrant-cofibrant objects). Then the Quillen adjunction lifts to a pair of [[adjoint (∞,1)-functor]]s 

$$
  (\mathbb{L} \dashv \mathbb{R}) : C^\circ \stackrel{\leftarrow}{\to} D^{\circ}
  \,. 
$$

On the [[decategorification|decategorified]] level of the [[homotopy category|homotopoy categories]] these are the total left and right [[derived functor]]s, respectively, of $L$ and $R$.

=--

+-- {: .proof}
###### Proof

This is proposition 5.2.4.6 in [[Higher Topos Theory|HTT]].

=--


#Remarks#

* Quillen adjunctions that are analogous to an [[equivalence of categories]] are called [[Quillen equivalence]]s.

* In an [[enriched model category]] one speaks of [[enriched Quillen adjunction]].


