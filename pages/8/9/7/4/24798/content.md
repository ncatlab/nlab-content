
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Foundations
+-- {: .hide}
[[!include foundations - contents]]
=--
=--
=--

# Two-sorted set theory
* table of contents
{: toc}

## Overview

There are a number of ways to present a [[set theory]]; one of the most basic decisions when it comes to presenting a set theory is whether the probable [[sets]] and probable [[elements]] should be regarded as the same kind of objects, as in [[unsorted set theory]], or as fundamentally different objects, as in [[two-sorted set theory]]. In the former, there is a global membership relation $\in$ which is defined on the entire [[domain of discourse]]. In the latter, there are two domains of discourse, one representing the probable sets and the other representing the probable elements or atoms, and for the membership relation $a \in b$, $a$ is required to be a probable element and $b$ is required to be a probable set. 

In contrast to [[unsorted set theory]], there is no global equality predicate in a two-sorted set theory. Instead, there are separate equality predicates for sets and elements, whereby it is meaningful to ask, given any two elements, whether those two elements are equal, and likewise, given any two set, whether those two sets are equal. Additionally, a set's identity here is determined by its elements, in other words the [[axiom of weak extensionality]] holds for the membership relation with respect to the equality relation of sets. 

Two-sorted set theories come in both [[material set theory]] and [[structural set theory]] flavors. For example, [[ZFC]], [[ZFA]], and [[New Foundations]] are could all be presented as two-sorted [[material set theories]], while [[ETCS]] can be presented as a two-sorted [[structural set theory]]. 

## Notions of sets and elements

We work in a two-sorted first order theory, where $S$ represents the type of probable sets, and $E$ represents the type of probable elements. Then, 

\begin{definition}
A notion of set and element in a two-sorted first-order theory with sorts $S$ and $E$ consists of:

* A binary predicate in $S$, $(-)=_S(-)$, called *equality of sets*

* A binary predicate in $E$, $(-)=_E(-)$, called *equality of elements*

* A unary predicate in $S$, $\mathrm{set}(-)$, called *being a set*

* A unary predicate in $E$, $\mathrm{element}(-)$, called *being an element*

* A binary predicate in $E$ on the left and $S$ on the right, $(-)\in(-)$, called *membership*

such that 

* $(-)=_E(-)$ is an [[equivalence relation]]

* if $a \in b$, then $a$ is an element and $b$ is a set

$$\forall a:E.\forall b:S.(a \in b) \to \mathrm{element}(a) \wedge \mathrm{set}(b)$$

* weak extensionality for sets and elements: for all $a:S$ and for all $b:S$, if a and b are sets, then $a =_S b$ if and only if, for all $c:E$, if $c$ is an element, then $c \in a$ if and only if $c \in b$

$$\forall a:S.\forall b:S.(\mathrm{set}(a) \wedge \mathrm{set}(b)) \implies ((a =_S b) \iff \forall c:E.(\mathrm{element}(c) \implies ((c \in a) \iff (c \in b))))$$
\end{definition}

## Element reflection and set reflection

In two-sorted set theories, sets are not literally elements. Instead, to represent that sets are elements and vice versa, one could add reflection rules and axioms to the set theory, which say that for every set, there is a corresponding element, and vice versa. 

In two-sorted set theory, **element reflection** is the statement that for all sets $A$, there is an element $\mathrm{asElem}(A)$, or equivalently, that there is a function $\mathrm{asElem}:S \to E$ in the set theory. Similarly, **set reflection** is the statement that for all elements $a$, there is a set $\mathrm{asSet}(A)$, or equivalently, that there is a function $\mathrm{asSet}:E \to S$ in the set theory. 

For any two-sorted set theory with element reflection, it is possible to define a membership relation on the elements alone which behaves like a global membership relation in [[unsorted set theory]], as follows 
$$a \in_E A \coloneqq \exists A':S.A =_E \mathrm{asElem}(A') \wedge a \in A'$$ 
Similarly, for any two-sorted set theory with set reflection, it is possible to define a membership relation on the sets alone which behaves like a global membership relation in [[unsorted set theory]], as follows 
$$a \in_S A \coloneqq \exists a':E.a =_S \mathrm{asSet}(a') \wedge a' \in A$$ 

## Examples

### Pure set theories

A two-sorted set theory with element reflection and set reflection is a [[pure set]] theory if $\mathrm{set}(A)$ and $\mathrm{element}(a)$ are both $\top$ for all $A:S$ and $a:E$, and set and element reflection are inverses of each other: $\mathrm{asElem}(\mathrm{asSet}(A)) =_S A$ and $\mathrm{asElem}(\mathrm{asSet}(a)) =_E a$. The induced membership relations $\in_E$ and $\in_S$ both behave as the global membership relation in an [[unsorted set theory]], so one could work entirely in $E$ or in $S$. 

### Set theories with urelements

A two-sorted set theory with element reflection is a [[material set theory]] with [[urelements]] if $\mathrm{set}(A)$ and $\mathrm{element}(a)$ are both $\top$ for all $A:S$ and $a:E$, and element reflection is an injection, $A =_S B$ only if $\mathrm{asElem}(A) =_E \mathrm{asElem}(B)$. The [[atoms]] or [[urelements]] are the elements which are not contained in the [[image]] of $\mathrm{asElem}$. The induced membership relation $\in_E$ behaves as the global membership relation in an [[unsorted set theory]], so one could work entirely in $E$.

### Categorical set theories

There are also two-sorted categorical set theories, such as the presentation of ETCS. In ETCS, there are two types, a set $Set$ and a set $Func$ representing sets and functions respectively, with functions $\mathrm{dom}:Func \to Set$ and $\mathrm{codom}:Func \to Set$ representing the domain and codomain of the function. (there might be a fiberwise set-truncation necessary in this definition) There is a set $1:Set$ representing the [[singleton]], the [[terminal object]] in $Set$. $\mathrm{set}(A)$ is true for all $A:Set$, but $\mathrm{element}(a)$ is only true for those functions whose source is the singleton terminal object $\mathrm{dom}(a) =_{Set} 1$. We define the membership relation $a \in A$ to be 
$$a \in A \coloneqq \mathrm{element}(a) \wedge \mathrm{set}(A) \wedge \mathrm{codom}(a) = A$$

Furthermore, there are multiple possible functions which could act as element reflections in categorical set theories, three of which are

* the [[identity functions]] of sets $A$, $\mathrm{asElem}(A) \coloneqq \mathrm{id}(A)$

* the unique [[function]] into the [[singleton]] and out of $A$, due to the [[universal property]] of the singleton, $\mathrm{asElem}(A) \coloneqq u(A)$, where $\mathrm{codom}(u(A)) = 1$ and $\mathrm{dom}(u(A)) = A$ 

* the unique [[function]] out of the [[empty set]] into $A$, due to the [[universal property]] of the empty set, $\mathrm{asElem}(A) \coloneqq v(A)$, where $\mathrm{dom}(v(A)) = \emptyset$ and $\mathrm{codom}(v(A)) = A$

This in turn induces the following definitions of sets in $Func$ itself:

* sets as [[identity functions]] $\mathrm{set}'(a) \coloneqq \mathrm{dom}(a) = a$ or $\mathrm{set}'(a) \coloneqq \mathrm{codom}(a) = a$ 

* sets as [[functions]] into the [[singleton]] $\mathrm{set}'(a) \coloneqq (\mathrm{codom}(a) = 1)$ 

* sets as functions out of the [[empty set]] ($\mathrm{set}'(a) \coloneqq (\mathrm{dom}(a) = 0)$). 

and the following definitions of membership relations on $Func$ itself:

* for sets as identity functions, the membership relation is defined as 
$$a \in_{Func} b \coloneqq \mathrm{element}(a) \wedge \mathrm{set}'(b) \wedge \mathrm{codom}(a) = b$$

* for sets as functions into the singleton, the membership relation is defined as 
$$a \in_{Func} b \coloneqq \mathrm{element}(a) \wedge \mathrm{set}'(b) \wedge \mathrm{codom}(a) = \mathrm{dom}(b)$$

* for sets as functions out of the empty set, the membership relation is defined as 
$$a \in_{Func} b \coloneqq \mathrm{element}(a) \wedge \mathrm{set}'(b) \wedge \mathrm{codom}(a) = \mathrm{codom}(b)$$

For the first two membership relations $\in_{Func}$, the identity morphism of the singleton $1$ is a [[Quine atom]], and any identity morphism of any set in bijection with $1$ is a [[Quine atom]]. For the third membership relation, there are no [[Quine atoms]]. While all the membership relations defined above are [[weakly extensional relations]], all three membership relations defined above could be proven not to be [[strongly extensional relations]], which means that the [[axiom of foundation]] fails in any of the three unsorted presentations of categorical set theory. 

### Allegorical set theories

## See also

* [[unsorted set theory]]
* [[two-sorted set theory]]
* [[dependently sorted set theory]]

* [[structural set theory]]
* [[material set theory]]
* [[structurally presented set theory]]

[[!redirects two-sorted set theory]]
[[!redirects two-sorted set theories]]

[[!redirects element reflection]]
[[!redirects set reflection]]