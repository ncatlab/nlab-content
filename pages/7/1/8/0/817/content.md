
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

In the context of $V$-[[enriched category theory]] (with $V$ any suitable [[cosmos for enrichment]]) for $\mathbf{C}$, $\mathbf{D}$ a [[pair]] of [[enriched categories|$V$-enriched categories]], there is, fist of all, an ordinary [[category]] whose 

* [[objects]] are the [[enriched functors]] $F \colon \mathbf{C} \longrightarrow \mathbf{D}$,

* [[morphisms]] $\eta \colon F \Rightarrow F'$ are the [[enriched natural transformations]].

This notion is a generalization of the plain notion of the *[[functor category]]* between [[locally small categories]], to which it reduces in the case that $V \equiv $ [[Set]] equipped with its [[cartesian monoidal category|cartesian monoidal]]-[[structure]]. 

As such one may and does call this ordinary category the "enriched functor category" between $\mathbf{C}$ and $\mathbf{D}$, in the sense of the "category of enriched functors".

However, this category of enriched functors canonically enhances further to a $V$-[[enriched category]] itself, hence to an "enriched-functor enriched-category", then traditionally often denoted $[\mathbf{C}, \mathbf{D}]$ or similar.

Namely, for
$
  F, G \,\colon\, \mathbf{C} \longrightarrow \mathbf{D}
$
a [[pair]] of $V$-[[enriched functors]] between $V$-[[enriched categories]], the collection of [[enriched natural transformations]] from $F$ to $G$ can also be given the [[structure]] of an [[object]] in $V$, in a compatible way:


## Definition

For $\mathbf{C}$ and $\mathbf{D}$ $V$-[[enriched categories]], there is a $V$-[[enriched category]], denoted $[\mathbf{C},\,\mathbf{D}]$, whose

* [[objects]] are the $V$-[[enriched functors]] $F \colon \mathbf{C} \longrightarrow \mathbf{D}$

* [[hom-objects]] $\;[C,D](F,G)$ between $V$-functors $F, G$ are given by the $V$-enriched [[end]]
$$
  [\mathbf{C},\mathbf{D}](F,G) 
  \;\coloneqq\; 
  \int_{c \in \mathbf{C}} 
  \mathbf{D}\big(F(c),\, G(c)\big)
$$
over the [[enriched hom-functor]]
$$
  mathbf{D}\big(
    F(-)
    ,\,
    G(-)
  \big) 
  \;\colon\; 
  \mathbf{C}^{op} 
    \otimes 
  \mathbf{C} 
    \longright 
  V
  \,,
$$

* the [[composition]] operation 

$$
  \circ_{K,F,G} 
    \,\colon\, 
  [\mathbf{C},\mathbf{D}](F,G)
    \otimes 
  [\mathbf{C},\mathbf{D}](K,F) 
   \longrightarrow 
  [\mathbf{C},\mathbf{D}](K,G)
$$
is the universal morphism into the [[end]] $[\mathbf{C},\mathbf{D}](K,F)$ obtained from observing that the composites
$$
  [\mathbf{C},\mathbf{D}](F,G)
    \otimes 
  [\mathbf{C},\mathbf{D}](K,F)
    \stackrel{E_c\otimes E_d}{\longrightarrow}
  \mathbf{D}\big(F(c),G(c)\big) 
    \otimes 
  \mathbf{D}\big(K(c),F(c)\big)
    \stackrel{\circ_{K(c), F(c), G(c)}}{\longrightarrow}
  \mathbf{D}\big(K(c), F(c)\big)
$$

  (where $E_c \colon [\mathbf{C},\mathbf{D}](F,G) \to \mathbf{D}\big(F(c),G(c)\big)$ denotes the canonical [[morphism]] out of the [[end]], i.e. the counit)

  form an [[extranatural transformation|extra $V$-natural]] family, equivalently that
$$
 [\mathbf{C},\mathbf{D}](F,G)
   \otimes 
 [\mathbf{C},\mathbf{D}](K,F)
   \stackrel
    {\prod_{c \in Obj(c)}E_c\otimes E_c}
    {\longrightarrow}
 \prod_{c \in Obj(c)}
 \mathbf{D}\big(F(c),G(c)\big) 
   \otimes 
 \mathbf{D}\big(K(c),\,F(c)\big)
 \stackrel{\prod_{c \in Obj(c)}
   \circ_{K(c), F(c), G(c)}}{\longrightarrow}
 \prod_{c \in Obj(c)}
   \mathbf{D}\big(K(c),\,G(c)\big)
$$
equalizes the two maps appearing in the [[equalizer]]-definition of the [[end]].


+-- {: .un_prop}
###### Proposition

For $V = $[[Set]], so that $V$-enriched categories are just ordinary [[locally small category|locally small categories]], the $V$-enriched functor category coincides with the ordinary [[functor category]]. (See the examples below.)

=--

## Examples

### Ordinary functor categories

To understand the role of the [[end]] here, it is useful to spell this out for the case where $V =$ [[Set]], where we are dealing with ordinary [[locally small category|locally small]] categories.

So let $V = Set$ where set is equipped with its [[cartesian monoidal category|cartesian monoidal structure]].

Recall the definition of the [[end]] over

$$
  \mathbf{D}\big(
    F(-),G(-)
  \big) 
  \,\colon\, 
  \mathbf{C}^{op} \otimes \mathbf{C} 
    \longrightarrow 
  Set
$$

as an [[equalizer]]: it is the [[universal property|universal]] [[subobject]] 

$$
  \int_{c \in C} \mathbf{D}\big(F(c),\, G(c)\big)
  \hookrightarrow
  \prod_{c \in Obj(C)} \mathbf{D}\big(F(c),\, G(c)\big)
$$

of the [[product]] of all [[hom-sets]] in $D$ between the [[images]] of [[objects]] in $C$ under the [[functors]] $F$ and $G$. So one element $ \eta \in \int_{c \in \mathbf{C}} \mathbf{D}\big(F(c), G(c)\big)$ is a collection of morphisms

$$
  \big( 
    F(c) 
      \stackrel{\eta_c}{\longrightarrow} 
    G(c)
  \big)_{c \in Obj(c)}
$$

such that the "left and right [[action]]" (in the sense of [[distributors]]) of $\mathbf{D}\big(F(-),G(-)\big)$ on these elements coincides. Unwrapping what this action is (see the details at [[end]]) one find that 

* the "right [[action]]" by a morphism $c \stackrel{f}{\to} d$ is the postcomposition $
  (F(c) \stackrel{\eta_c}{\to} G(c)) \mapsto
  (F(c) \stackrel{\eta_c}{\to} G(c) \stackrel{G(f)}{\to} G(d))
$

* the "left [[action]]" by a morphism $c \stackrel{f}{\to} d$ is the precomposition $
  (F(d) \stackrel{\eta_d}{\to} G(d)) \mapsto
  (F(c) \stackrel{F(f)}{\to} F(d) \stackrel{\eta_d}{\to} G(d) )
$.

So the [[invariants]] under the combined action are those $\eta$ for which for all $f \colon c \to d$ in $C$ the [[diagram]]
$$
  \array{
    F(c) &\stackrel{\eta_c}{\longrightarrow} & G(c)
    \\
    \Big\downarrow^{F(f)}
    &&
    \Big\downarrow\mathrlap{^{G(f)}}
    \\
    F(d) 
    &
      \stackrel{\eta_d}{\longrightarrow} 
    & 
    G(d)
  }
$$

[[commuting diagram|commutes]]. Evidently, this means that the elements $\eta$ of the [[end]] $\int_{c \in \mathbf{C}} \mathbf{D}\big(F(c), G(c)\big)$ are precisely the [[natural transformation]]s between $F$ and $G$.

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

[[!redirects enriched-functor category]]
[[!redirects enriched-functor categories]]

[[!redirects enriched functor-category]]
[[!redirects enriched functor-categories]]


[[!redirects enriched presheaf category]]
[[!redirects enriched presheaf categories]]

[[!redirects category of enriched presheaves]]
[[!redirects categories of enriched presheaves]]




