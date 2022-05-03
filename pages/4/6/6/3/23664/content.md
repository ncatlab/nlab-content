+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Category theory
+-- {: .hide}
[[!include category theory - contents]]
=--
#### Relations
+-- {: .hide}
[[!include relations - contents]]
#### Constructivism, Realizability, Computability
+-- {: .hide}
[[!include constructivism - contents]]
=--
#### Type theory
+-- {: .hide}
[[!include type theory - contents]]

=--
=--
=--
=--

# Contents
* table of contents
{: toc}

## Definition 

### In category theory

An **extensional function** is a [[functor]] between [[setoids]] ([[thin category|thin]] [[groupoids]]). 

### In type theory

There are multiple inequivalent notions of extensional function in type theory. 

#### As functions that preserve equivalence relations

An **extensional function** is a [[function]] $f:A \to B$ between [[setoids]] $A$ and $B$ such that for all terms $a:A$ and $b:A$, $p:(a \equiv_A b) \to (f(a) \equiv_B f(b))$. 

#### As functions that preserve identity types

An **extensional function** is a [[function]] $f:A \to B$ between [[types]] $A$ and $B$ such that for all terms $a:A$ and $b:A$, $p:(a =_A b) \to (f(a) =_B f(b))$. 

If there exists an [[interval type]], then every function is an extensional function. 

## See also 

* [[functor]]
* [[thin category]]
* [[setoid]]
* [[equivalence relation]]
* [[identity types]]
* [[interval type]]

[[!redirects extensional function]]
[[!redirects extensional functions]]
[[!redirects extensional operation]]
[[!redirects extensional operations]]
[[!redirects extensional prefunction]]
[[!redirects extensional prefunctions]]
[[!redirects extensional pre-function]]
[[!redirects extensional pre-functions]]