
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Foundations
+-- {: .hide}
[[!include foundations - contents]]
=--
=--
=--

# Unsorted set theory
* table of contents
{: toc}

## Overview
 {#Overview}

There are a number of ways to present a [[set theory]]; one of the most basic decisions when it comes to presenting a set theory is whether the probable [[sets]] and probable [[elements]] should be regarded as the same kind of objects, as in [[unsorted set theory]], or as fundamentally different objects, as in [[two-sorted set theory]]. In the former, there is a global membership relation $\in$ which is defined on the entire [[domain of discourse]]. In the latter, there are two domains of discourse, one representing the probable sets and the other representing the probable elements or atoms, and for the membership relation $a \in b$, $a$ is required to be a probable element and $b$ is required to be a probable set. 

Furthermore, in an unsorted set theory, there is also a global equality predicate, whereby it is meaningful to ask, given any two objects, whether those two objects are equal. Additionally, a set's identity here is determined by its elements, in other words the [[axiom of weak extensionality]] holds for the global membership relation with respect to the equality relation. 

Unsorted set theories come in both [[material set theory]] and [[structural set theory]] flavors. For example, [[ZFC]], [[ZFA]], and [[New Foundations]] are unsorted [[material set theories]], while [[fully formal ETCS]] is an unsorted [[structural set theory]]. 

## Notions of sets and elements

First of all, in order to give a definition pertaining to all unsorted set theories, we need to know: what is a set theory? Probably no theory can *intrinsically* be called a set theory; it is only given that distinction by our intent to regard some of its objects of study as “sets” and others as their “elements.” Thus we make the following definition.

\begin{definition}
A notion of set and element in a unsorted first-order theory consists of:

* A binary predicate $(-)=(-)$ called *equality*

* A unary predicate $\mathrm{set}(-)$ called *being a set*

* A unary predicate $\mathrm{element}(-)$ called *being an element*

* A binary predicate $(-)\in(-)$ called *membership*

such that 

* if $a \in b$, then $a$ is an element and $b$ is a set

$$\forall a.\forall b.(a \in b) \to \mathrm{element}(a) \wedge \mathrm{set}(b)$$

* weak extensionality for sets and elements: for all $a$ and for all $b$, if a and b are sets, then $a = b$ if and only if, for all $c$, if $c$ is an element, then $c \in a$ if and only if $c \in b$

$$\forall a.\forall b.(\mathrm{set}(a) \wedge \mathrm{set}(b)) \implies ((a = b) \iff \forall c.(\mathrm{element}(c) \implies ((c \in a) \iff (c \in b))))$$
\end{definition}

## Examples

### Pure set theories

In [[pure set]] theories, such as [[ZFC]] and [[New Foundations]], $\mathrm{set}(a)$ and $\mathrm{element}(a)$ is $\top$ for all objects $a$, $\in$ is the primitive membership relation and $=$ is defined through the axiom of extensionality. 

### Set theories with urelements

In set theories with [[urelements]], such as [[ZFA]], only $\mathrm{element}(a)$ is $\top$ for all objects $a$, $\in$ is the primitive membership relation, $\mathrm{set}$ is the primitive sethood predicate, and $=$ is defined through the axiom of extensionality. 

### Categorical set theories

In an unsorted categorical set theory, such as [[Todd Trimble]]'s [[fully formal ETCS]], $=$ is a primitive, and there is a specified symbol $1$ representing the [[identity morphism]] of the [[terminal object]] and a specified symbol $0$ representing the [[identity morphism]] of the [[initial object]], as well as $s$ and $t$ representing the [[identity morphisms]] of the [[source]] and [[target]]. The elements are functions with domain $1$, $\mathrm{element}(a) \coloneqq (\mathrm{dom}(a) = 1)$ There are many possible notions of sets, three of which include: 

* sets as [[identity functions]] $\mathrm{set}(a) \coloneqq \mathrm{dom}(a) = a$ or $\mathrm{set}(a) \coloneqq \mathrm{codom}(a) = a$ 

* sets as [[functions]] into the [[singleton]] $\mathrm{set}(a) \coloneqq (\mathrm{codom}(a) = 1)$ 

* sets as functions out of the [[empty set]] ($\mathrm{set}(a) \coloneqq (\mathrm{dom}(a) = 0)$). 

Thus, there are many different definitions of the membership relation $\in$, which for the above notions of set are:

* for sets as identity functions, the membership relation is defined as 
$$a \in b \coloneqq \mathrm{element}(a) \wedge \mathrm{set}(b) \wedge \mathrm{codom}(a) = b$$

* for sets as functions into the singleton, the membership relation is defined as 
$$a \in b \coloneqq \mathrm{element}(a) \wedge \mathrm{set}(b) \wedge \mathrm{codom}(a) = \mathrm{dom}(b)$$

* for sets as functions out of the empty set, the membership relation is defined as 
$$a \in b \coloneqq \mathrm{element}(a) \wedge \mathrm{set}(b) \wedge \mathrm{codom}(a) = \mathrm{codom}(b)$$

For the first two membership relations $\in$, the singleton $1$ is a [[Quine atom]], and any set in bijection with $1$ is a [[Quine atom]]. For the third membership relation, there are no [[Quine atoms]]. While all the membership relations defined above are [[weakly extensional relations]], all three membership relations defined above could be proven not to be [[strongly extensional relations]], which means that the [[axiom of foundation]] fails in any of the three unsorted presentations of categorical set theory. 

### Allegorical set theories

## See also

* [[unsorted set theory]]
* [[two-sorted set theory]]
* [[dependently sorted set theory]]

* [[structural set theory]]
* [[material set theory]]
* [[structurally presented set theory]]

[[!redirects unsorted set theory]]
[[!redirects unsorted set theories]]

[[!redirects single-sorted set theory]]
[[!redirects single-sorted set theories]]