[[!redirects cocartesian monoidal dagger categories]]

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
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
A **cocartesian monoidal dagger category** is a [[monoidal dagger category]] $(C, +, 0)$ with 

* a morphism $i_A \in Hom_C(A,A + B)$ for $A \in Ob(C)$ and $B \in Ob(C)$. 
* a morphism $i_B \in Hom_C(B,A + B)$ for $A \in Ob(C)$ and $B \in Ob(C)$. 
* a morphism $d_{A + B} \in Hom_C(A + B,D)$ for an object $D \in Ob(C)$ and morphisms $d_A \in Hom_C(A,D)$ and $d_B \in Hom_C(B,D)$
* a morphism $0_A \in Hom_C(0,A)$ for every object $A \in C$

such that 

* for every object $D \in Ob(C)$ and morphisms $d_A \in Hom_C(A,D)$ and $d_B \in Hom_C(B,D)$, $d_{A + B} \circ i_A = d_A$ 
* for every object $D \in Ob(C)$ and morphisms $d_A \in Hom_C(A,D)$ and $d_B \in Hom_C(B,D)$, $d_{A + B} \circ i_B = d_B$ 
* for every object $A \in Ob(C)$ and $B \in Ob(C)$ and morphism $f \in Hom_C(A,B)$, $f \circ 0_A = 0_B$. 

In a cocartesian monoidal dagger category, the tensor product is called a **coproduct** and the tensor unit is called an **initial object**. 

## Examples ##

* [[semiadditive dagger category]]

## See also ##

* [[dagger category]]
* [[monoidal dagger category]]