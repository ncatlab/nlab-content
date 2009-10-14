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

It follows from the definition that

* $F$ preserves weak equivalences between cofibrant objects;

* $G$ preserves weak equivalences between fibrant objects.


#Remarks#

* Quillen adjunctions that are analogous to an [[equivalence of categories]] are called [[Quillen equivalence]]s.

* In an [[enriched model category]] one speaks of [[enriched Quillen adjunction]].


