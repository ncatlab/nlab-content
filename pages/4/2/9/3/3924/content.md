+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Algebra
+--{: .hide}
[[!include higher algebra - contents]]
=--
#### Monoidal categories
+--{: .hide}
[[!include monoidal categories - contents]]
=--
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

* **associator**, [[unitor]], [[Jacobiator]]

* [[pentagonator]], [[hexagonator]]

***

#Contents#
* table of contents
{:toc}

## Idea

In [[algebra]], given any [[non-associative algebra]] $A$, then the trilinear map

$$
  [-,-,-] \;-\; A \otimes A \otimes A \longrightarrow A
$$

given on any elements $a,b,c \in A$ by

$$
  [a,b,c] \coloneqq (a b) c - a (b c)
$$

is called the _[[associator]]_ (in analogy with the [[commutator]] $[a,b] \coloneqq a b - b a$ ).

An algebra for which the associator vanishes is hence an _[[associative algebra]]_. If the associator is possibly non-vanishing but completely anti-symmetric (in that for any [[permutation]] $\sigma$ of three elements then $[a_{\sigma_1}, a_{\sigma_2}, a_{\sigma_3}] = (-1)^{\vert \sigma\vert} [a_1, a_2, a_3]$ for $\vert \sigma \vert$ the [[signature of a permutation|signature of the permutation]]) then $A$ is called an _[[alternative algebra]]_.


In [[category theory]] and [[higher category theory]] (for [[monoidal categories]], [[bicategories]] and their higher versions) one considers relaxing the [[equation]] that exhibits the vanishing of the associator

$$
  (a b) c = a (b c)
$$

to a [[natural equivalence]]

$$
  \alpha_{a,b,c} \;\colon\; (a b) c \overset{\simeq}{\longrightarrow}  a (b c)
  \,.
$$

By slight mismatch with the terminology in [[algebra]], it is then this equivalence which is called _the associator_.



### In Bicategories

In a [[bicategory]] the [[composition]] of [[1-morphism]]s does not satisfy [[associativity]] as an equation, but there are natural _associator_ 2-morphisms 

$$
  h \circ (g \circ f) \stackrel{\simeq}{\Rightarrow} (h \circ g) \circ f
$$

that satisfy a [[coherence law]] among themselves.

If one thinks of the bicategory as obtained from a [[geometric definition of higher categories|geometrically defined 2-category]] $C$, then the composition operation of 1-morphisms is a _choice_ of  2-[[horn]]-fillers and the associator is a _choice_ of filler of the spheres $\partial \Delta[3] \to C$ formed by these. 


### In monoidal categories

By the [[periodic table of higher categories]] a [[monoidal category]] is a pointed [[bicategory]] with a single object, its [[object]]s are the 1-morphisms of the bicategory. Accordingly, here the  associator is a [[natural isomorphism]] 

$$ a_{x,y,z} : (x \otimes y) \otimes z \to x \otimes (y \otimes z) $$

relating the triple [[tensor products]] of these objects.

## Examples

* In a [[tensor category]] of [[representations]] the associator is called the _[[Wigner 6-j symbol]]_.

## Related concepts

* [[commutator]]

* [[coherence]]

[[!redirects associators]]