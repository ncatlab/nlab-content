#Idea#

Enriched functors are used in place of [[functor]]s in [[enriched category theory]]: like functors they send objects to objects, but instead of mapping [[hom-set]]s to [[hom-set]]s they assign morphisms in the enriching category between [[hom-object]]s, while being compatible with composition and units in the obvious way.

#Definition#

Given two categories $C, D$ [[enriched category|enriched in]] a [[monoidal category]] $V$, an **enriched functor** $F: C \to D$ consists of 

* A function $F_0: C_0 \to D_0$ between the underlying collections of objects; 
* A $(C_0 \times C_0)$-indexed collection of morphisms of $V$, 
$$F_{x, y}: C(x, y) \to D(F_0x, F_0y)$$ 
[where $C(x, y)$ denotes the hom-object $\hom_C(x, y)$ in $V$], compatible with the enriched identities and compositions of $C$ and $D$;

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


#Remarks#

* Analogous to the [[functor category]] for ordinary [[functor]]s between ordinary [[category|categories]], enriched functors between two enriched categories form an [[enriched functor category]].


#References#

The standard reference on [[enriched category theory]] is

* Max Kelly, _Basic Concepts of Enriched Category Theory_ ([web](http://www.tac.mta.ca/tac/reprints/articles/10/tr10abs.html))