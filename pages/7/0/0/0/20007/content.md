
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
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

Given two [[monoidal categories]] $(V_1,\otimes_1, I_1)$ and $(V_2, \otimes_2, I_2)$ used for enrichement in [[enriched category theory]] (for instance two [[Bénabou cosmoi]]) a [[lax monoidal functor]] between them

$$
  F 
  \;\colon\;
  (V_1, \otimes_1, I_1)
    \longrightarrow
  (V_2, \otimes_2, I_2)  
$$

canonically induces a [[2-functor]]

$$
  F_\ast \;\colon\; V_1 Cat \longrightarrow V_2 Cat
$$

between [[categories of V-enriched categories]] sending a $V_1$-[[enriched category]] $\mathcal{C}$ to the $V_2$-[[enriched category]] $F_\ast(\mathcal{C})$ such that 

1. $F_\ast(\mathcal{C})$ has the same [[objects]] as $\mathcal{C}$;

1. the [[hom-objects]] of $F_\ast(\mathcal{C})$ are the [[images]] of the hom-objects of $\mathcal{C}$ under $F$:

   $$
     F_\ast(\mathcal{C})(x,y)
     \;\coloneqq\;
     F\big(\mathcal{C}(x,y)\big)
   $$

1. the [[composition]], [[unit]], [[associator]] and [[unitor]] [[morphisms]] in $F_\ast(\mathcal{C})$ are the [[images]] of those of $\mathcal{C}$ composed with the structure morphisms of the [[lax monoidal functor|lax monoidal]]-[[structure]] on $F$.

([Eilenberg-Kelly 65](#EilenbergKelly65))

This operation $F_\ast$ is sometimes called "change of enriching category" or "change of enriching base" or just "change of base" (e.g. [Crutwell 14, chapter 4](#Crutwell14), [Riehl 14, lemma 3.4.3](#Riehl14)). But notice that, despite some vague similarity, this is different from [[base change]] of [[slice categories]].

In the special case that $\mathcal{C}$ has a single object and is hence (if thought of as [[pointed object|pointed]] by that object) equivalently a [[monoid object]] in $V_1$, this statement reduces to the statement that lax monoidal functors preserve [[monoids]] ([this Prop.](monoidal+functor#MonoidsToMonoidsByLaxMonoidal))


## Properties

The operation of change of enriching category is functorial from [[MonCat]] to [[2Cat]].  In particular, any [[monoidal adjunction]] $V_1\rightleftarrows V_2$ gives rise to a [[2-adjunction]] $V_1 Cat\rightleftarrows V_2 Cat$ (and also for profunctors).  

The adjunction $Cat \rightleftarrows K Cat$ described above (...) is a special case of this arising from the adjunction $-\cdot I: Set \rightleftarrows K : K(I,-)$.



## References


* {#EilenbergKelly65} [[Samuel Eilenberg]], [[Max Kelly]], _Closed categories_.  Proc. Conf. Categorical Algebra (La Jolla, Calif., 1965).  

* {#Crutwell14} [[Geoff Cruttwell]], chapter 4 of _Normed spaces and the Change of Base for Enriched Categories_, 2014 ([pdf](http://pages.cpsc.ucalgary.ca/~gscruttw/publications/thesis4.pdf))


* {#Riehl14} [[Emily Riehl]], lemma 3.4.3 in _[[Categorical Homotopy Theory]]_, Cambridge University Press 2014

[[!redirects changes of enriching category]]
[[!redirects changes of enriching categories]]

[[!redirects change of enriching base]]
[[!redirects changes of enriching base]]
[[!redirects changes of enriching bases]]

[[!redirects change of base in enriched category theory]]
[[!redirects changes of base in enriched category theory]]
[[!redirects changes of bases in enriched category theory]]
