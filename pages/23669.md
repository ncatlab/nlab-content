[[!redirects semiadditive dagger 2-posets]]

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Higher category theory
+--{: .hide}
[[!include higher category theory - contents]]
=--
=--
=--

## Contents ##
* table of contents
{:toc}

## Definition ##

A **semiadditive dagger 2-poset** is a [[dagger 2-poset]] $C$ such that 

* There exists an object $0:Ob(C)$ called the [[zero object]] such that for each object $A:Ob(C)$, there exists a morphism $Z_A:Hom(0, A)$ such that for each object $B:Ob(C)$ and morphism $R: Hom(A, B)$, $R \circ Z_A = Z_B$.

* For each object $A:Ob(C)$ and $B:Ob(C)$, there exists a object $A \oplus B:Ob(C)$ called the [[biproduct]] of $A$ and $B$, with morphisms $I_A: Hom(A,A \oplus B)$ and $I_B: Hom(B,A \oplus B)$, such that 

  * For each object $A:Ob(C)$, $B:Ob(C)$, and $C:Ob(C)$ and morphism $R_A:Hom(A,C)$ and $R_B:Hom(B,C)$, there exist a morphism $R: Hom(A \oplus B ,C)$ such that $R \circ I_A = R_A$ and $R \circ I_B = R_B$

  * For each object $A:Ob(C)$, $B:Ob(C)$, $C:Ob(C)$, and $D:Ob(C)$, and morphism $R:Hom(A, B)$ and $S:Hom(C,D)$, there exists a morphism $R \oplus S:Hom(A \oplus B,C \oplus D)$ where $(R \oplus S)^\dagger = R^\dagger \oplus S^\dagger$.

## Examples ##

* The dagger 2-poset [[Rel]] of [[sets]] and [[relations]] is a semiadditive dagger 2-poset. 

## See also ##

* [[dagger 2-poset]]
* [[semiadditive category]]
* [[semiadditive dagger category]]