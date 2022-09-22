+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Type theory
+-- {: .hide}
[[!include type theory - contents]]
=--
#### Category theory
+-- {: .hide}
[[!include category theory - contents]]
=--
=--
=--

# Contents
* table of contents
{:toc}

## Definition

In [[intensional type theory]] such as [[homotopy type theory]] a **pregroupoid** is a [[precategory]] $C$ with a family of functions $(-)^{{-1}_{a, b}}:Mor_C(a, b) \to Mor_C(b, a)$ for [[objects]] $a:Ob(C)$ and $b:Ob(C)$ and [[identifications]] $\lambda(a, b, 
 f):f^{{-1}_{a, b}} \circ_{a, b, a} f = id_a$ and $\rho(a, b, f):f \circ_{b, a, b} f^{{-1}_{a, b}} = id_b$ for [[objects]] $a:Ob(C)$ and $b:Ob(C)$ and [[morphisms]]  $f:Mor_C(a, b)$. 

Equivalently, it is a [[dagger precategory]] with identifications $\lambda(a, b, 
 f):f^{\dagger_{a, b}} \circ_{a, b, a} f = id_a$ and $\rho(a, b, f):f \circ_{b, a, b} f^{\dagger_{a, b}} = id_b$ for [[objects]] $a:Ob(C)$ and $b:Ob(C)$ and [[morphisms]] $f:Mor_C(a, b)$.

## Examples

* A pregroupoid whose sets of morphisms are all subsingletons is a [[symmetric proset]]. 

* A pregroupoid whose object type is a set is a [[strict groupoid]]. 

* A pregroupoid whose canonical functions 
$$idtotruncmor(a, b):a =_C b \to \vert Mor_C(a, b) \vert$$ 
are equivalences of types for all objects $a:Ob(C)$ and $b:Ob(C)$ is a [[skeleton|skeletal groupoid]]. 

* A pregroupoid whose canonical functions 
$$idtomor(a, b):a =_C b \to Mor_C(a, b)$$ 
are equivalences of types for all objects $a:Ob(C)$ and $b:Ob(C)$ is a [[univalent groupoid]]. Every 1-truncated type is equivalent to a univalent groupoid. 

* Every [[gaunt category|gaunt pregroupoid]] is a [[set]]. 

## See also

* [[precategory]]

* [[dagger precategory]]

* [[univalent groupoid]]

## References

* {#UFP13} Univalent Foundations Project, [[HoTT book|Homotopy Type Theory – Univalent Foundations of Mathematics]] (2013)

[[!redirects pregroupoids]]