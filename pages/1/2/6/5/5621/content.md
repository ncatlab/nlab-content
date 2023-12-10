
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### 2-Category theory
+--{: .hide}
[[!include 2-category theory - contents]]
=--
#### Notions of subcategory
+-- {: .hide}
[[!include notions of subcategory]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Definition

A [[2-functor]] $F \,\colon\, C \to D$ exhibits the [[2-category]] $C$ as a **full sub-2-category** of $D$ if for all [[object]]s $c_1,c_2 \in C$ the component [[functor]] $F_{c_1, c_2}$ is an [[equivalence of categories]]

$$
  F_{c_1, c_2} 
  \;\colon\; 
  C(c_1,c_2) 
  \xrightarrow{\;\; \simeq \;\;} 
  D\big(
    F(c_1), F(c_2)
  \big)
  \,,
$$

hence if $F$ is a **2-fully-faithful 2-functor**.

## Properties

$C$ and $D$ can be considered as (1-)categories by forgetting their 2-morphisms, and $F$ can be considered as a (1-)functor via [[decategorification]]. As a result, every full sub-2-category is also a full subcategory.

If $D$ is a [[(2,1)-category]] a full sub-2-category is equivalently a [[full sub-(∞,1)-category]].

## References

* Math Overflow, "When is a full sub-2-category not a full subcategory?", [web](https://math.stackexchange.com/q/4821592/425071)


## Related concepts



[[!include properties of functors -- contents]]




[[!redirects full sub-2-categories]]

[[!redirects full and faithful 2-functor]]
[[!redirects full and faithful 2-functors]]

[[!redirects fully faithful 2-functor]]
[[!redirects fully faithful 2-functors]]


[[!redirects sub-2-category]]