
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Category theory
+-- {: .hide}
[[!include category theory - contents]]
=--
=--
=--

# Contents
* table of contents
{: toc}

## Definition

An **inverse** of a [[morphism]] $f : X \to Y$ in a [[category]] or [[unital magmoid]] (or an element of a [[monoid]] or [[unital magma]]) is another morphism $f^{-1} : Y \to X$ which is both a left-inverse (a [[retraction]]) as well as a right-inverse (a [[section]]) of $f$, in that 
$$
  f \circ f^{-1} : Y \to Y 
$$
equals the [[identity morphism]] on $Y$ and
$$
  f^{-1} \circ f : X \to X 
$$
equals the [[identity morphism]] on $X$.


## Remarks

* A morphism which has an inverse is called an [[isomorphism]].

* The inverse $f^{-1}$ is unique if it exists.

* The inverse of an inverse morphism is the original morphism, $(f^{-1})^{-1} = f$.

* An [[identity morphism]], $i$, is a morphism which is its own inverse: $i^{-1} = i$.

* A category in which all morphisms have inverses is called a [[groupoid]].

* An amusing exercise is to show that if $f,g,h$ are morphisms such that $f\circ g,\; g\circ h$ are defined and are isomorphisms, then $f,g,h$ are all isomorphisms. 

  * This is a special case of the **[[two-out-of-six property]]** which is satisfied by the _weak equivalences_ in any [[homotopical category]].

  * When this is applied to a [[homotopy category]] such as that of [[Top]] for the standard [[model structure on topological spaces]] it implies the construction of and formulae for certain homotopies.

* In a [[balanced category]], such as a [[topos]] or more particularly [[Set]], every morphism that is both [[monomorphism|monic]] and [[epimorphism|epic]] is an [[isomorphism]] and thus has an inverse. A [[partial order]] is an unbalanced category where every morphism is both monic and epic. Only its [[identity morphisms]] have inverses. 

## In non-associative or non-unital contexts

These can be a little more complicated; see [[quasigroup]], [[nonassociative group, and [[possibly empty loop]] for some discussion of the one-object version, and [[quasigroupoid]] for the many-object version. 


## Related concepts

* [[inverse morphism]], [[inverse function]]

* [[weak inverse]]

* [[inversion involution]]


[[!redirects inverse]]
[[!redirects inverses]]
[[!redirects inverse element]]
[[!redirects inverse elements]]
[[!redirects inverse of an element]]
[[!redirects inverses of an element]]
[[!redirects inverses of elements]]
[[!redirects invertible element]]
[[!redirects invertible elements]]

[[!redirects inverse morphism]]
[[!redirects inverse morphisms]]
[[!redirects inverse of a morphism]]
[[!redirects inverses of a morphism]]
[[!redirects inverses of morphisms]]
[[!redirects invertible morphism]]
[[!redirects invertible morphisms]]
