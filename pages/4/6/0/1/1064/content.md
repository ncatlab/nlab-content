There is a sequence of extra [[stuff, structure, property|structure and property]] on a [[category]] that makes this category behave like a general context for [[homological algebra]]. In order of increasing structure and property this is:

1. **[[Ab-enriched category]]**:
  a [[category]] that is [[Ab]]-[[enriched category|enriched]];

1. **[[pre-additive category]]**:
  an $Ab$-enriched category that has a [[terminal object]] or [[initial object]] and therefore a [[zero object]];

1. **[[additive category]]**: a pre-additive category that admits binary [[product]]s or binary [[coproduct]]s and therefore binary [[biproduct]]s (equivalently, an $Ab$-enriched category with all finite products or coproducts);

1. **[[pre-abelian category]]**:
  an additive category that admits [[kernel]]s and  [[cokernel]]s (equivalently, an $Ab$-enriched category with all finite [[limit]]s and [[colimit]]s);

1. **[[abelian category]]**:
  a pre-abelian category such that every [[monomorphism]] is a kernel and every [[epimorphism]] is a cokernel (and many other equivalent definitions).

Pre-abelian and abelian categories are sometimes called (AB1) and (AB2) categories, after the sequence of additional axioms on top of additive categories introduced by Grothendieck in [[Tohoku]].  AB1 and AB2 are self-dual axioms (AB1 is existence of kernels and cokernels, and AB2 requires that, for any $f$, the canonical morphism $\mathrm{Coim}\,f\to \mathrm{Im}\,f$ is an isomorphism). These continue in non-selfdual manner:

* AB3: an abelian category with all coproducts and products (hence with all [[colimit]]s and [[limit]]s);

* AB4: an (AB3) category in which coproducts of monomorphisms are monic and products of epimorphisms are epic;

* AB5: an (AB3) category in which [[filtered category|filtered colimits and cofiltered limit]]s of [[exact sequence]]s are exact;

* AB6: an AB3 category such that

  * for every object $A$ in $C$ and any family $B^j$ with $j \in J$ of directed families $B^j = B^j_i$ with $i in I_j$ the interesections of [[subobject]]s  over $j$ commute with direct summes over j.

  * Notice that this implies that inf for any family of subobjects exists.

The concepts (AB3--6) can also be split into independent colimit-like and limit-like parts. One can also consider dual axioms AB3$^\star$, AB4$^\star$, AB5$^\star$ and AB6$^\star$.

There are further refinements along these lines. In particular

* [[Grothendieck category]]: an AB5 category with a [[generator]].

#Further refinements#

Various further axiom structures are considered and of relevance on additive and abelian categories.

* [[suspended category]]

* [[triangulated category]]

* [[Quillen exact category]]

* [[Grothendieck category]]:  an AB5-category with a [[generator]]

# Generalizations #

* Abelian groups are to general [[group]]s as [[abelian category|abelian categories]] are to [[semi-abelian category|semi-abelian categories]].


#Examples#

Various generic classes of examples of additive and abelian categories are of relevance:

* [[category of chain complexes]]

* [[derived category]]