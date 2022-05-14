[[!redirects evaluational categories]]

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Category theory
+-- {: .hide}
[[!include category theory - contents]]
=--
#### Discrete and concrete objects
+-- {: .hide}
[[!include discrete and concrete objects - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea ##

A [[concrete category]] whose morphisms behave as [[functions]] do in [[Set]] with respect to [[elements]] and [[evaluation]]. 

## Definition ##

An **evaluational category** $C$ is a [[concrete category]] with a function $(-)((-)) \colon Hom(A,B) \times El(A) \to El(B)$ for objects $A:Ob(C)$ and $B \colon Ob(C)$ such that for every morphism $f \colon Hom(A,B)$ and $g \colon Hom(B,C)$ and every elements $x:El(A)$, $(g \circ f)(x) = g(f(x))$.

## Examples ##

* The category $Set$ of sets and functions is an evaluational category. 

* The category $Preset$ of [[sets]] and [[prefunctions]] is an evaluational category. 

* The category $Mon$ of [[monoids]] and monoid [[homomorphisms]] is an evaluational category. 

* The category $Ab$ of [[abelian groups]] and abelian group homomorphisms is an evaluational category. 

* Given a commutative ring $R$, the category $R Mod$ of $R$-[[modules]] and $R$-[[linear maps]] is an evaluational category. 

* Given a commutative ring $R$, the category $R Alg$ of $R$-[[algebras]] and $R$-algebra homomorphisms is an evaluational category. 

* The category $CRing$ of [[commutative rings]] and commutative ring homomorphisms is an evaluational category. 

* The category $Field$ of [[fields]] and field homomorphisms is an evaluational category. 

* The category $HeytAlg$ of [[Heyting algebras]] and Heyting algebra homomorphisms is an evaluational category. 

* The category $Frm$ of [[frames]] and frame homomorphisms is an evaluational category. 

* The category $Conv$ of [[convergence spaces]] and [[continuous functions]] is an evaluational category. 

* The category $Top$ of [[topological spaces]] and continuous functions is an evaluational category. 

* The category $Met$ of [[metric spaces]] and [[isometries]] is an evaluational category. 

* The category $StrictCat$ of [[strict categories]] and [[strict functors]] is an evaluational category. 

* The category of empty sets and functions is an evaluatioinal category. 

## Non-examples ##

* The category $Rel$ of sets and [[relations]] is not an evaluational category. 

* In general, given a concrete [[regular category]] $C$, the category $Rel(C)$ of objects of $C$ and [[congruences]] between objects of $C$ is not an evaluational category. 

* The category $Set_\bot$ of sets and [[partial functions]] is not an evaluational category. 

## See also ##

* [[concrete category]]

* [[evaluation map]] (for the [[internalization|internal]] non-concrete version)

* [[extensional category]]
