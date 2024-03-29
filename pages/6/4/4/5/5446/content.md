
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Algebra
+--{: .hide}
[[!include higher algebra - contents]]
=--
=--
=--


# Anti-Homomorphisms
* table of contents
{: toc}

## Idea

While a [[homomorphism]] of [[magmas]] (including [[groups]], [[rings]], etc) must preserve multiplication, an _antihomomorphism_ must instead _reverse_ multiplication.


## Definitions

Let $A$ and $B$ be [[magmas]], or more generally [[magma objects]] [[internalisation|in]] any [[symmetric monoidal category]] $C$.  (Examples include [[groups]], which are magmas with extra properties; [[rings]], which are magma objects in [[Ab]] with extra proprties; etc.)

An __antihomomorphism__ from $A$ to $B$ is a [[homomorphism]] $f\colon A \to B^\op$ where $B^\op$ is the [[opposite magma]] of $B$, or equivalently, it is a [[function]] (or $C$-morphism) $f\colon A \to B$ such that:

*  for every two ([[generalised element|generalised]]) elements $x, y$ of $A$, $f(x y) = f(y) f(x)$.

Note that for magma objects in $C$, the left-hand side of this equation is a generalised element of $B$ whose source is ${|x|} \otimes {|y|}$ (where ${|x|}$ and ${|y|}$ are the sources of the generalised elements $x$ and $y$ and $\otimes$ is the [[tensor product]] in $C$), while the right-hand side is a generalised element of $B$ whose source is ${|y|} \otimes {|x|}$.  Therefore, this definition only makes unambiguous sense because $C$ is symmetric monoidal, using the unique [[natural isomorphism]] ${|x|} \otimes {|y|} \cong {|y|} \otimes {|x|}$.

An __antiautomorphism__ is an antihomomorphism whose underlying $C$-morphism is an [[automorphism]].


## Examples

* The [[inverse function]] of a [[group]] is a [[monoid]] anti-homomorphism, and in fact an anti-automorphism, hence an [[anti-involution]], since $(x y) (x y)^{-1} = 1 = x x^{-1} = x y y^{-1} x^{-1}$, which means that $(x y)^{-1} = y^{-1} x^{-1}$. 

* The [[antipode]] in a [[Hopf algebra]] is an anti-homomorphism (by [this Prop.](Hopf+algebra#AntipodeIsAnAntihomomorphism)). The same is separately required for antipodes on associative [[bialgebroid]]s.

* In a [[star-algebra]] the star-operation is an anti-homomorphism, in fact an anti-automorphism, hence an anti-[[involution]].

* Combining these two examples, in an [[involutive Hopf algebra]] the [[antipode]] is an anti-automorphism.

## Related concepts

* [[opposite magma]]

[[!redirects antihomomorphism]]
[[!redirects antihomomorphisms]]
[[!redirects anti-homomorphism]]
[[!redirects anti-homomorphisms]]

[[!redirects antiautomorphism]]
[[!redirects antiautomorphisms]]
[[!redirects anti-automorphism]]
[[!redirects anti-automorphisms]]

