
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Type theory
+-- {: .hide}
[[!include type theory - contents]]
=--
#### Category theory
+--{: .hide}
[[!include category theory - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Definition ##

In [[homotopy type theory]], a **univalent groupoid** or **saturated groupoid** is a [[univalent dagger category]] $A$ where for all objects $a \colon A$ and $b \colon A$ and morphisms $f \colon \mathrm{Hom}_A(a, b)$, $f \circ f^\dagger = \mathrm{id}_B$ and $f^\dagger \circ f = \mathrm{id}_A$. Equivalently, it is a univalent dagger category where every morphism is a [[unitary morphism]]. 

Equivalently, a univalent or saturated groupoid is a [[precategory]] $A$ where for all objects $a:A$ and $b:A$ there is an equivalence between the [[identity type]] $a =_A b$ and the type $\mathrm{Hom}_A(a, b)$:

$$a:A, b:A \vdash \mathrm{disc}(a, b):\mathrm{isEquiv}(\mathrm{idToHom}(a, b))$$

where 

$$
  \mathrm{idToHom}(a, b)
  \;\colon\;
  (a =_A b) 
  \;
  \to 
  \;
  \mathrm{Hom}_A(a, b)
$$

$$
  \mathrm{idToHom}(x, y)
  \big(
    \mathrm{refl}_A(x)
  \big) 
    \;\coloneqq\;
  \mathrm{id}_A(x)
$$

The second definition implies that the only morphisms in $A$ are [[isomorphisms]], making $A$ a [[groupoid]], and thus the Rezk completeness condition holds in $A$, making $A$ [[univalent category|univalent]].

## See also ##

* [[univalence]]

* [[groupoid]]

* [[univalent dagger category]]

* [[discrete Segal type]]

[[!redirects univalent groupoids]]
[[!redirects saturated groupoid]]
[[!redirects saturated groupoids]]

