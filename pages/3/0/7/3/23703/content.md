[[!redirects cartesian monoidal dagger categories]]

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
A **cartesian monoidal dagger category** is a [[monoidal dagger category]] $(C, \times, 1)$ with 

* a morphism $p_A \in Hom_C(A \times B,A)$ for $A \in Ob(C)$ and $B \in Ob(C)$. 
* a morphism $p_B \in Hom_C(A \times B,B)$ for $A \in Ob(C)$ and $B \in Ob(C)$. 
* a morphism $p_{A \times B} \in Hom_C(D,A \times B)$ for an object $D \in Ob(C)$ and morphisms $d_A \in Hom_C(D,A)$ and $d_B \in Hom_C(D,B)$
* a morphism $!_A \in Hom_C(A,1)$ for every object $A \in C$

such that 

* for every object $D \in Ob(C)$ and morphisms $d_A \in Hom_C(D,B)$ and $d_B \in Hom_C(D,B)$, $p_A \circ d_{A \times B} = d_A$ 
* for every object $D \in Ob(C)$ and morphisms $d_A \in Hom_C(D,B)$ and $d_B \in Hom_C(D,B)$, $p_B \circ d_{A \otimes B} = d_B$ 
* for every object $A \in Ob(C)$ and $B \in Ob(C)$ and morphism $f \in Hom_C(A,B)$, $!_B \circ f = !_A$. 

In a cartesian monoidal dagger category, the tensor product is called a **cartesian product** and the tensor unit is called a **terminal object**. 

## Examples ##

* [[semiadditive dagger category]]

## See also ##

* [[dagger category]]
* [[monoidal dagger category]]