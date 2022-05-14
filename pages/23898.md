[[!redirects extensional categories]]

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

An [[evaluational category]] where [[morphisms]] satisfy the [[function extensionality|axiom of extensionality]]. 

## Definition ##

An extensional category $C$ is a [[evaluational category]] such that for morphisms $f \colon Hom(A,B)$ and $g \colon Hom(A,B)$, if $f(x) = g(x)$ for all [[elements]] $x \colon El(A)$, then $f = g$. 

### From scratch ###

An **extensional category** is a class or type $\mathcal{C}$ with

* a set $El(A)$ for every object $A \in \mathcal{C}$, whose elements are called **elements** of $A$.

* a set $Hom(A, B)$ for every object $A \in \mathcal{C}$ and $B \in \mathcal{C}$, whose elements are called **morphisms from $A$ to $B$**

* a function called **evaluation** for every object $A \in \mathcal{C}$ and $B \in \mathcal{C}$
$$(-)((-)):Hom(A, B) \times \El(A) \to El(B)$$

* for every object $A \in \mathcal{C}$, a morphism $id_A \colon Hom(A, A)$ called the **identity morphism of $A$**;

* a function called **composition** for every object $A \in \mathcal{C}$, $B \in \mathcal{C}$, and $C \in \mathcal{C}$
$$(-)((-)):Hom(B, C) \times \Hom(A, B) \to Hom(A, C)$$

such that

* For every object $A \in \mathcal{C}$ and for every element $a \in El(A)$, $id_A(a) = a$.

* For every object $A \in \mathcal{C}$, $B \in \mathcal{C}$, and $C \in \mathcal{C}$, for every morphism $f \colon Hom(A,B)$ and $g \colon Hom(A,B)$, and for every element $a \in El(A)$, $(g \circ f)(a) = g(f(a))$.

* For every object $A \in \mathcal{C}$ and $B \in \mathcal{C}$ and for every morphism $f \colon Hom(A,B)$ and $g \colon Hom(A,B)$, if $f(x) = g(x)$ for all elements $x \colon El(A)$, then $f = g$. 

The associativity and unit laws of function composition follow from the axioms:

* For every object $A \in \mathcal{C}$ and $B \in \mathcal{C}$, morphism $f \colon Hom(A, B)$, and element $a \in El(A)$, 
$$(g \circ id_A)(a) = g(id_A(a)) = g(a)$$ 
and extensionality implies that $g \circ id_A = g$. 

* For every object $A \in \mathcal{C}$ and $B \in \mathcal{C}$, morphism $f \colon Hom(A, B)$, and element $a \in El(A)$, 
$$(id_B \circ g)(a) = id_B(g(a)) = g(a)$$ 
and extensionality implies that $id_B \circ g = g$. 

* For every object $A \in \mathcal{C}$, $B \in \mathcal{C}$, $C \in \mathcal{C}$, and $D \in \mathcal{C}$, morphism $f \colon Hom(A, B)$, $g \colon Hom(B, C)$, and $h \colon Hom(C, D)$, and element $a \in El(A)$, 
$$(h \circ (g \circ f))(a) = h((g \circ f)(a))$$ 
$$(h \circ (g \circ f))(a) = h(g(f(a))$$ 
$$(h \circ (g \circ f))(a) = (h \circ g)(f(a))$$ 
$$(h \circ (g \circ f))(a) = ((h \circ g) \circ f)(a)$$
and extensionality implies that $h \circ (g \circ f) = (h \circ g) \circ f$.

Thus, these axioms form a [[category]]. 

## Extensionality and well-pointedness ###

The category [[Set]] of sets and functions is both extensional and well-pointed. However, not every [[well-pointed category]] is an extensional category, as well-pointed categories are not required to be [[concrete categories]]. Moreover, not every extensional category is a [[well-pointed category]]: the category $Field$ of [[fields]] and field [[homomorphisms]] is extensional, but is not well-pointed because it doesn't have a [[terminal object]]. 

The distinction between extensionality and well-pointedness is the distinction between [[elements]] and [[global elements]] in a concrete evaluational category with a [[terminal object]], as it is not true that elements and global elements (if they exist) coincide in general. 


## Examples ##

* The category $Set$ of sets and functions is an extensional category. 

* The category $Mon$ of [[monoids]] and monoid [[homomorphisms]] is an extensional category. 

* The category $Ab$ of [[abelian groups]] and abelian group homomorphisms is an extensional category. 

* Given a commutative ring $R$, the category $R Mod$ of $R$-[[modules]] and $R$-[[linear maps]] is an extensional category. 

* Given a commutative ring $R$, the category $R Alg$ of $R$-[[algebras]] and $R$-algebra homomorphisms is an extensional category. 

* The category $CRing$ of [[commutative rings]] and commutative ring homomorphisms is an extensional category. 

* The category $Field$ of [[fields]] and field homomorphisms is an extensional category. 

* The category $HeytAlg$ of [[Heyting algebras]] and Heyting algebra homomorphisms is an extensional category. 

* The category $Frm$ of [[frames]] and frame homomorphisms is an extensional category. 

* The category $Conv$ of [[convergence spaces]] and [[continuous functions]] is an extensional category. 

* The category $Top$ of [[topological spaces]] and continuous functions is an extensional category. 

* The category $Met$ of [[metric spaces]] and [[isometries]] is an extensional category. 

* The category $StrictCat$ of [[strict categories]] and [[strict functors]] is an extensional category. 

* The category of empty sets and functions is an extensional category. 

## Non-examples ##

* The category $Prefunc$ of [[sets]] and [[prefunctions]] is not an extensional category. 

## See also ##

* [[function extensionality]]
* [[concrete category]]
* [[evaluational category]]
* [[well-pointed category]]
* [[Set]]

