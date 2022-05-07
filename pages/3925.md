
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### 2-Category theory
+--{: .hide}
[[!include 2-category theory - contents]]
=--
#### Higher category theory
+--{: .hide}
[[!include higher category theory - contents]]
=--
=--
=--

* [[associator]], **unitor**, [[Jacobiator]]

* [[pentagonator]], [[hexagonator]]

***

# Contents
* table of contents
{:toc}

## Idea

A _unitor_ in [[category theory]] and [[higher category theory]] is an [[isomorphism]] that relaxes the ordinary [[uniticity]] _equality_ of a binary operation.


### In bicategories

In a [[bicategory]] the [[composition]] of [[1-morphism]]s does not satisfy [[uniticity]] as an equation, but there are natural _unitor_ 2-morphisms 

$$
  Id \circ f \stackrel{\simeq}{\Rightarrow} f
$$

$$
  f \circ Id \stackrel{\simeq}{\Rightarrow} f
$$

that satisfy a [[coherence law]] among themselves.


### In monoidal categories

By the [[periodic table of higher categories]] a [[monoidal category]] is a pointed [[bicategory]] with a single object, its [[object]]s are the 1-morphisms of the bicategory. 

Accordingly, a [[monoidal category]] is equipped with a [[natural isomorphism]]

$$ \ell_x : 1 \otimes x \to x $$

called the **left unitor**, and a natural isomorphism

$$ r_x : x \otimes 1 \to x $$

called the **right unitor**.


[[!redirects unitor]]
[[!redirects unitors]]
[[!redirects left unitor]]
[[!redirects left unitors]]
[[!redirects right unitor]]
[[!redirects right unitors]]
