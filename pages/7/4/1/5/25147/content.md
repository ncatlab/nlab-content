
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Type theory
+-- {: .hide}
[[!include type theory - contents]]
=--
=--
=--

\tableofcontents

## Idea

In [[dependent type theory]], given types $A$ and $B$ and a family of elements $x:A \vdash f(x):B$, the [[function application to identifications]] for $f(x)$ is the family of elements
$$a:A, b:A, p:a =_A b \vdash \mathrm{ap}_f(a, b, p):f(a) =_B f(b)$$ 

A dependent function application to identifications is like an function application to identifications, but hwere we allow $B$ to depend on $x:A$ and similarly the [[identity type]] $f(a) =_B f(b)$ to be a [[heterogeneous identity type]] and depend on the identification $p:a =_A b$. 

## Definition

In [[dependent type theory]], given a type $A$ and a type family $x:A \vdash B(x)$ and a family of elements $x:A \vdash f(x):B(x)$, the **dependent function application to identifications** or **dependent action on identifications** for $f(x)$ is the family of elements
$$a:A, b:A, p:a =_A b \vdash \mathrm{apd}_f(a, b, p):f(a) =_B^p f(b)$$ 
inductively defined by 
$$a:A \vdash \mathrm{apd}_f(a, a, \mathrm{refl}_A(a)) =_{f(a) =_{B(a)} f(a)} \mathrm{refl}_A(a)$$ 
where $f(a) =_B^p f(b)$ is a [[heterogeneous identity type]]. 

In addition, there are two other families of elements which could be considered dependent function applications to identifications, which use [[transport]] and the inverse of transport rather than heterogeneous identity types:

$$a:A, b:A, p:a =_A b \vdash \mathrm{apdl}_f(a, b, p):f(a) =_{B(a)} \mathrm{tr}_B(a, b, p)^{-1}(f(b))$$ 
$$a:A, b:A, p:a =_A b \vdash \mathrm{apdr}_f(a, b, p):\mathrm{tr}_B(a, b, p)(f(a)) =_{B(b)} f(b)$$ 

Having one of the three notions of dependent function application to identifications means that one could define all three of them, because the types $f(a) =_B^p f(b)$, $f(a) =_{B(a)} \mathrm{tr}_B(a, b, p)^{-1}(f(b))$, and $\mathrm{tr}_B(a, b, p)(f(a)) =_{B(b)} f(b)$ are all [[equivalence of types|equivalent]] to each other. 

## See also

* [[equivalence type]]
* [[transport]]
* [[dependent function]]

[[!redirects dependent function application to identities]]
[[!redirects dependent function application to identifications]]
[[!redirects dependent function application to paths]]
[[!redirects dependent function application to equalities]]

[[!redirects application of a dependent function to identities]]
[[!redirects application of a dependent function to identifications]]
[[!redirects application of a dependent function to paths]]
[[!redirects application of a dependent function to equalities]]

[[!redirects dependent action on identities]]
[[!redirects dependent action on identifications]]
[[!redirects dependent action on paths]]
[[!redirects dependent action on equalities]]