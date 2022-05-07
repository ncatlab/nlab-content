
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


## Idea

Enriched functors are used in place of [[functors]] in [[enriched category theory]]: like functors they send objects to objects, but instead of mapping [[hom-sets]] to [[hom-sets]] they assign morphisms in the enriching category between [[hom-objects]], while being compatible with composition and units in the obvious way.

## Definition

Given two categories $C, D$ [[enriched category|enriched in]] a [[monoidal category]] $V$, an **enriched functor** $F: C \to D$ consists of 

* A function $F_0: C_0 \to D_0$ between the underlying collections of objects; 
* A $(C_0 \times C_0)$-indexed collection of morphisms of $V$, 
$$F_{x, y}: C(x, y) \to D(F_0x, F_0y)$$ 
where $C(x, y)$ denotes the hom-object in $V$,

* such that the following diagrams commute for all $a, b, c \in C_0$:

  * respect for composition:
    $$
      \array{
        C(b,c) \otimes C(a,b) 
        &\stackrel{\circ_{a,b,c}}{\to}&
        C(a,c)
        \\
        \downarrow^{F_{b,c} \otimes F_{a,b}} && \downarrow^{F_{a,c}}
        \\
        D(F_0(b), F_0(c)) \otimes D(F_0(a), F_0(b))
        &\stackrel{\circ_{F_0(a),F_0(b), F_0(c)}}{\to}&
        D(F_0(a), F_0(c))
      }
    $$

  * respect for units:
    $$
      \array{
        && I
        \\
        & {}^{j_a}\swarrow && \searrow^{j_{F_0(a)}}
        \\
        C(a,a)
        &&\stackrel{F_{a,a}}{\to}&&
        D(F_0(a), F_0(a))
      }
    $$

     $V$'s unit object $I$ and the family of identity [[generalized element |elements]] $J_i$ from it are defined in [[enriched category]].

## Properties

* Analogous to the [[functor category]] for ordinary [[functors]] between ordinary [[categories]], enriched functors between two enriched categories form an [[enriched functor category]].

## Examples

* [[linear functor]]

* [[smooth functor]]

* [[topologically enriched functor]]

* Consider the enriching category with $[0,\infty]$ the set of objects, maps given by $\geq$, and tensor by $+$. Then $V$-categories are [[Lawvere metric spaces]], and $V$-functors are distance-decreasing maps.

* Categories enriched in the [[poset]] of truth values with conjunction as monoidal product are posets, and the corresponding enriched functors are precisely order-preserving maps.

## Related concepts

* [[enriched natural transformation]]

* [[enriched functor category]]

* [[enriched (∞,1)-functor]]

## References

* [[Max Kelly]], _Basic Concepts of Enriched Category Theory_ ([web](http://www.tac.mta.ca/tac/reprints/articles/10/tr10abs.html))

*  {#Lawvere73}  [[Bill Lawvere]] (1973).  _Metric spaces, generalized logic and closed categories_.  Reprinted in [[TAC]], 1986.  [Web](http://www.tac.mta.ca/tac/reprints/articles/1/tr1abs.html).

* [[Emily Riehl]], chapter 3 _Basics of enriched category theory_ in _[[Categorical Homotopy Theory]]_

For more references see at _[[enriched category theory]]_.

[[!redirects enriched functors]]