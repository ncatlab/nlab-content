[[!redirects dagger functors]]

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Category theory
+--{: .hide}
[[!include category theory - contents]]
=--
=--
=--

# $\dagger$ functors
* tic
{: toc}

## Idea ##

A map between two [[dagger categories]] that preserves the dagger category structure. 

## Definition ##

+-- {: .un_defn}
###### Definition
Given two $\dagger$-categories $A$ and $B$, a **$\dagger$-functor** $F : A \to B$ consists of a function $F_0 : Ob(A) \to Ob(B)$ with a function $F_{a,b}:Hom_A(a,b) \to Hom_B(F a,F b)$ for every object $a,b:Ob(A)$, where $F_{a,b}$ is generally also denoted as $F$, such that

* for every object $a \in Ob(A)$, $F(1_a)=1_{F a}$, 
* for every object $a,b,c \in Ob(A)$ and morphisms $f \in Hom_A(a,b)$ and $g \in Hom_A(b,c)$, $F(g \circ_A f) = F g \circ_B F f$
* for every object $a,b \in Ob(A)$ and morphism $f \in Hom_A(a,b)$, $F(f^{\dagger_A}) = (F f)^{\dagger_B}$. 
=--

There is another definition which violates the [[principle of equivalence]], since the definition of the dagger in a dagger category in this case is a functor that imposes equations on objects: A $\dagger$-functor $F : (C, \dagger) \to (D, \ddagger)$ between two $\dagger$-categories $(C, \dagger)$ and $(D, \ddagger)$ is a [[functor]] $F : C \to D$ of the underlying categories, which commutes with the $\dagger$-structures in that $F \circ \dagger = \ddagger \circ F^{op}$. 

## See also ##

* [[dagger category]]
* [[monoidal dagger category]]