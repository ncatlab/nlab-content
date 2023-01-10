
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Category theory
+-- {: .hide}
[[!include category theory - contents]]
=--
=--
=--

\tableofcontents

## Idea

In the same way that [[internal homs]] in a [[cartesian monoidal category]] behave as an internal version of [[hom-sets]] between two objects, the *object of monomorphism* should behave as an internal version of the sub-hom-set of monomorphisms between two objects. 

These generalize [[injection sets]] in the [[category of sets]] [[Set]]. 

## Definition

Given a [[cartesian monoidal category]] $C$ and two objects $A \in C$ and $B \in C$, there is a functor 
$$X \mapsto \mathrm{Mono}_{C/X}(A \times X, B \times X)$$ 
which takes an object $X \in C$ to a [[monomorphism]] between objects $A \times X$ and $B \times X$ in the [[slice category]] $C/X$. A [[representing object]] of the above functor, if it exists, is the **object of monomorphisms** between $A$ and $B$ and is denoted as $[A, B]_\mathrm{mono}$. 

## Properties

If the category is a [[cartesian closed category]], then there is a [[monomorphism]] $i:\mathrm{Mono}_C([A, B]_\mathrm{mono}, [A, B])$ between the object of monomorphism between $A$ and $B$ and the [[internal hom]] from $A$ to $B$. 

## See also

* [[injection set]]
* [[embedding type]]
* [[exponential object]], [[internal hom]], [[object of isomorphisms]]

[[!redirects object of monomorphisms]]
[[!redirects objects of monomorphisms]]
