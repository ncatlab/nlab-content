
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Model category theory
+--{: .hide}
[[!include model category theory - contents]]
=--
=--
=--


#Contents#
* automatic table of contents goes here
{:toc}

## Idea

Quillen adjunctions are one convenient notion of morphism between [[model category|model categories]].  They present [[adjoint (∞,1)-functors]] between the [[(∞,1)-category|(∞,1)-categories]] [[presentable (infinity,1)-category|presented]] by the model categories.


## Definition 

For $C$ and $D$ two [[model category|model categories]], a pair $(L,R)$

$$
  (L \dashv R) : C \stackrel{\overset{L}{\leftarrow}}{\underset{R}{\to}}
  D
$$


of [[adjoint functors]] (with $L$ [[left adjoint]]) is a **Quillen adjunction** if the following equivalent conditions are satisfied:

* $L$ preserves cofibrations and acyclic cofibrations;

* $R$ preserves fibrations and trivial fibrations;

* $L$ preserves cofibrations and $G$ preserves fibrations;

* $R$ preserves trivial cofibrations and $G$ preserves trivial fibrations.

Quillen adjunctions that are analogous to an [[equivalence of categories]] are called [[Quillen equivalences]].

In an [[enriched model category]] one speaks of [[enriched Quillen adjunction]].



## Properties

### General

+-- {: .un_prop}
###### Proposition


It follows from the definition that

* the [[left adjoint]] $L$ preserves weak equivalences between cofibrant objects;

* the [[right adjoint]] $R$ preserves weak equivalences between fibrant objects.

=--


+-- {: .proof}
###### Proof

To show this for instance for $R$, we may argue as in a 
[[category of fibrant objects]] and apply the _factorization lemma_
which shows that every weak equivalence between fibrant objects may be
factored, up to [[homotopy]], as a [[span]] of acyclic fibrations.

These weak equivalences are preserved by $R$ and hence by [[category with weak equivalences|2-out-of-3]] the claim follows. 

For $L$ we apply the formally dual argument.

=--

### Of $sSet$-enriched adjunctions {#sSet}

Of particular interest are [[SSet]]-[[enriched category theory|enriched]] adjunctions between [[simplicial model categories]]: [[simplicial Quillen adjunctions]]. 

These present [[adjoint (∞,1)-functors]], as the first proposition below asserts.


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

If $C$ and $D$ are [[simplicial model categories]] and $D$ is a left [[proper model category]], then an [[sSet]]-enriched adjunction

$$
  (L \dashv R) : C \stackrel{\leftarrow}{\to} D
$$

is a Quillen adjunction already if $L$ preserves cofibrations and $R$ just fibrant objects.

=--

This appears as [[Higher Topos Theory|HTT, cor. A.3.7.2]].

See [[simplicial Quillen adjunction]] for more details.




[[!redirects Quillen adjunctions]]
