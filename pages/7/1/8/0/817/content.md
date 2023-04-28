
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

In the context of $V$-[[enriched category theory]], for 
$
  F,G \colon C \to D
$
a [[pair]] of $V$-[[enriched functors]] between $V$-[[enriched category|enriched categories]], the collection of [[enriched natural transformations]] from $F$ to $G$ can also be given the [[structure]] of an [[object]] in $V$, so that the [[functor category]], $[C,D]$ becomes itself a $V$-[[enriched category]].


## Definition

For $C$ and $D$ $V$-[[enriched categories]], there is a $V$-[[enriched category]], denoted $[C,D]$, whose

* [[objects]] are the $V$-functors $F \colon C \to D$

* [[hom-objects]] $\;[C,D](F,G)$ between $V$-functors $F, G$ are given by the $V$-enriched [[end]]
$$
  [C,D](F,G) \coloneqq \int_{c \in C} D(F(c), G(c))
$$
over the [[enriched hom-functor]]
$$
  D\big(
    F(-)
    ,\,
    G(-)
  \big) 
  \;\colon\; 
  C^{op} \otimes C \to V
  \,,
$$


* the [[composition]] operation 
$$
  \circ_{K,F,G} \colon [C,D](F,G)\otimes [C,D](K,F) \to [C,D](K,G)
$$
is the universal morphism into the [[end]] $[C,D](K,F)$ obtained from observing that the composites
$$
 [C,D](F,G)\otimes [C,D](K,F)
 \stackrel{E_c\otimes E_d}{\to}
 D(F(c),G(c)) \otimes D(K(c),F(c))
 \stackrel{\circ_{K(c), F(c), G(c)}}{\to}
 D(K(c), F(c))
$$

  (where $E_c \colon [C,D](F,G) \to D(F(c),G(c))$ denotes the canonical [[morphism]] out of the [[end]], i.e. the counit)

  form an [[extranatural transformation|extra $V$-natural]] family, equivalently that
$$
 [C,D](F,G)\otimes [C,D](K,F)
 \stackrel{\prod_{c \in Obj(c)}E_c\otimes E_c}{\to}
 \prod_{c \in Obj(c)}
 D(F(c),G(c)) \otimes D(K(c),F(c))
 \stackrel{\prod_{c \in Obj(c)}\circ_{K(c), F(c), G(c)}}{\to}
 \prod_{c \in Obj(c)}D(K(c), G(c))
$$
equalizes the two maps appearing in the [[equalizer]]-definition of the [[end]].


+-- {: .un_prop}
######Proposition

For $V = $[[Set]], so that $V$-enriched categories are just ordinary [[locally small category|locally small categories]], the $V$-enriched functor category coincides with the ordinary [[functor category]]. (See the examples below.)
=--

## Examples

### Ordinary functor categories

To understand the role of the [[end]] here, it is useful to spell this out for the case where $V =$ [[Set]], where we are dealing with ordinary [[locally small category|locally small]] categories.

So let $V = Set$ where set is equipped with its [[cartesian monoidal category|cartesian monoidal structure]].

Recall the definition of the [[end]] over

$$
  D(F(-),G(-)) : C^{op} \otimes C \to Set
$$

as an [[equalizer]]: it is the [[universal property|universal]] [[subobject]] 

$$
  \int_{c \in C} D(F(c), G(c))
  \hookrightarrow
  \prod_{c \in Obj(C)} D(F(c), G(c))
$$

of the [[product]] of all [[hom-sets]] in $D$ between the [[images]] of [[objects]] in $C$ under the [[functors]] $F$ and $G$. So one element $ \eta \in \int_{c \in C} D(F(c), G(c))$ is a collection of morphisms

$$
  ( F(c) \stackrel{\eta_c}{\to} G(c))_{c \in Obj(c)}
$$

such that the "left and right [[action]]" (in the sense of [[distributors]]) of $D(F(-),G(-))$ on these elements coincides. Unwrapping what this action is (see the details at [[end]]) one find that 

* the "right [[action]]" by a morphism $c \stackrel{f}{\to} d$ is the postcomposition $
  (F(c) \stackrel{\eta_c}{\to} G(c)) \mapsto
  (F(c) \stackrel{\eta_c}{\to} G(c) \stackrel{G(f)}{\to} G(d))
$

* the "left [[action]]" by a morphism $c \stackrel{f}{\to} d$ is the precomposition $
  (F(d) \stackrel{\eta_d}{\to} G(d)) \mapsto
  (F(c) \stackrel{F(f)}{\to} F(d) \stackrel{\eta_d}{\to} G(d) )
$.

So the [[invariants]] under the combined action are those $\eta$ for which for all $f \colon c \to d$ in $C$ the diagram
$$
  \array{
    F(c) &\stackrel{\eta_c}{\to} & G(c)
    \\
    \downarrow^{F(f)}
    &&
    \downarrow^{G(f)}
    \\
    F(d) &\stackrel{\eta_d}{\to} & G(d)
  }
$$

commutes. Evidently, this means that the elements $\eta$ of the [[end]] $\int_{c \in C} D(F(c), G(c))$ are precisely the [[natural transformation]]s between $F$ and $G$.

### Pointwise order

For categories enriched in [[truth values]], the enriched functor category is given by the [[pointwise order]].

## Related concepts

* [[enriched Reedy category]]

* [[model structure on homotopical presheaves]]

* [[model structure on sSet-presheaves]]

## References

An original article:

* [[Brian Day]], [[Max Kelly]], *Enriched functor categories*, in: *Reports of the Midwest Category Seminar III*, Lecture Notes in Mathematics **106** (1969) 178-191 &lbrack;[doi:10.1007/BFb0059146](https://doi.org/10.1007/BFb0059146), [pdf](https://link.springer.com/content/pdf/10.1007/BFb0059146.pdf)&rbrack;

Review includes

* {#Day70} [[Brian Day]], _On closed categories of functors_, Reports of the Midwest Category Seminar IV, Lecture Notes in Mathematics Vol. 137. Springer-Verlag, 1970, pp 1-38 ([pdf](https://www.math.rochester.edu/people/faculty/doug/otherpapers/DayReport.pdf))

* [[Max Kelly]], [section 2.2 p. 29](http://www.tac.mta.ca/tac/reprints/articles/10/tr10.pdf#page=29) of _Basic concepts of enriched category theory_ ([pdf](http://www.tac.mta.ca/tac/reprints/articles/10/tr10.pdf))

[[!redirects enriched functor categories]]

[[!redirects enriched presheaf category]]
[[!redirects enriched presheaf categories]]

[[!redirects category of enriched presheaves]]
[[!redirects categories of enriched presheaves]]
