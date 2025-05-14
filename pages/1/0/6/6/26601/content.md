
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Type theory
+-- {: .hide}
[[!include type theory - contents]]
=--
#### Homotopy theory
+--{: .hide}
[[!include homotopy - contents]]
=--
=--
=--

\tableofcontents

## Idea

In [[dependent type theory]], the binary pullback type of functions $f:A \to C$ and $g:B \to C$ is given by the type

$$\sum_{x:A} \sum_{y:B} f(x) = g(y)$$

However, by using large elimination of the [[type of booleans]] $\mathrm{bool}$ on the codomain of the functions and by using the induction principle for the type of booleans on the functions themselves, one has a family of functions

$$\mathrm{ind}_\mathrm{bool}(f, g):\prod_{b:\mathrm{bool}} \mathrm{rec}_\mathrm{bool}(A, B, b) \to C$$

and the resulting binary pullback is the type

$$\sum_{x:\mathrm{rec}_\mathrm{bool}(A, B, 0)} \sum_{y:\mathrm{rec}_\mathrm{bool}(A, B, 1)} \mathrm{ind}_\mathrm{bool}(f, g, 0, x) = \mathrm{ind}_\mathrm{bool}(f, g, 1, y)$$

Thus, it suffices to define the binary pushout of a boolean-indexed family of functions $f:\prod_{x:\mathrm{bool}} A(x) \to C$, which is the type

$$\sum_{x:A(0)} \sum_{y:A(1)} f(0, x) = f(1, y)$$

For any elements $x:A$ and $y:A$, the [[identity type]] $x = y$ is equivalent to the dependent sum type $\sum_{z:A} (x = z) \times (y = z)$, and so the pullback is equivalently the type

$$\sum_{x:A(0)} \sum_{y:A(1)} \sum_{z:C} (f(0, x) = z) \times (f(1, y) = z)$$

and since [[dependent sum types]] and [[product types]] commute, this is equivalently the type

$$\sum_{z:C} \left(\sum_{x:A(0)} (f(0, x) = z)\right) \times \left(\sum_{y:A(1)} (f(1, y) = z)\right)$$

By induction on the booleans, this is equivalently

$$\sum_{z:C} \prod_{b:\mathrm{bool}} \sum_{x:A(b)} f(b, x) = z$$

By generalizing this definition of binary pullbacks from the type of booleans to any arbitrary type, one gets general dependent pullbacks of an arbitrary family of functions with [[codomain]] $C$, which are also known as *[[wide pullbacks]]* in [[category theory]]. 

## Definition

Given a type $C$, an index type $I$, a family of [[domains]] $A(i)$ indexed by $i:I$, and a family of functions $f:\prod_{i:I} A(i) \to C$, the **dependent pullback type** or **wide pullback type** of $(C, I, A, f)$ is the [[dependent sum type]]

$$\sum_{y:C} \prod_{i:I} \sum_{x:A(i)} f(i, x) =_C y$$

The type $\sum_{x:A(i)} f(i, x) =_C y$ is the [[fiber type]] of the function $f(i):A(i) \to C$ at the element $y:C$, so this type is also the [[dependent product type|dependent product]] of [[fiber types]], or the **dependent fiber product type** or **dependent fibre product type**. 

In addition, there is a dependent function 
$$\lambda j.\lambda p.\pi_1(\pi_2(p)(j)):\prod_{j:I} \left(\sum_{y:C} \prod_{i:I} \sum_{x:A(i)} f(i, x) =_C y\right) \to A(j)$$

which shows that the dependent pullback type is a [[wide span]]. 

## Examples

* The [[dependent product type]] of a family of types $B(x)$ indexed by $x:A$ is the dependent pullback of the family of unique functions from each $B(x)$ to the [[unit type]]. 

* The [[intersection]] of a family of [[subtypes]] of a type $A$ is given by the dependent pullback of the [[embedding of types|embeddings]] into $A$. 

* Binary [[pullback types]] are boolean-indexed dependent pullbacks types. 

* When the family of domains $A(x)$ indexed by $x:I$ is a constant family of types, then the dependent pullback type are called **dependent equalizer types** or **wide equalizer types**. 

## Related concepts

* [[dependent product type]]
* [[dependent pushout type]]
* [[pullback type]], [[homotopy pullback]]
* [[wide pullback]]


[[!redirects dependent pullback]]
[[!redirects dependent pullbacks]]

[[!redirects dependent fiber product]]
[[!redirects dependent fiber products]]

[[!redirects dependent fibre product]]
[[!redirects dependent fibre products]]

[[!redirects dependent pullback type]]
[[!redirects dependent pullback types]]

[[!redirects dependent fiber product type]]
[[!redirects dependent fiber product types]]

[[!redirects dependent fibre product type]]
[[!redirects dependent fibre product types]]

[[!redirects wide pullback type]]
[[!redirects wide pullback types]]

[[!redirects wide fiber product type]]
[[!redirects wide fiber product types]]

[[!redirects wide fiber product type]]
[[!redirects wide fiber product types]]