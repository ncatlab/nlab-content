
# Material set theory
* table of contents
{: toc}

## Overview

__Material set theory__ (also called _membership-based set
theory_) is a style of [[set theory]] that contrasts with [[structural set theory]].  In a material set theory, the [[elements]] of a set exist independently of that set.  (The terminology 'material', or at least 'materialistic', goes back at least to [Friedman 1997](#Friedman1997).) The standard example is [[ZFC]].

Some distinguishing features of a material set theory are 

* being an unsorted or single-sorted first-order theory

* a global membership predicate, whereby it is meaningful to ask, given any object and a set, whether the object is an element of the set. 

* a global equality predicate, whereby it is meaningful to ask, given any two objects, whether those two objects are equal 

* such that a set's identity here is determined by its elements, in other words the [[axiom of extensionality]] holds for the global membership relation with respect to the equality relation. 

Frequently in material set theory one takes everything to be a [[pure set]], including the elements of sets themselves. Therefore, any two sets may be meaningfully compared to ask if they are [[equal]] or if one is a member of the other.  As a slight variation (still material set theory), one may also accept ur-elements (or atoms) as elements. 

### Notions of sets and elements

First of all, in order to give a definition pertaining to all untyped set theories, we need to know: what is a set theory? Probably no theory can *intrinsically* be called a set theory; it is only given that distinction by our intent to regard some of its objects of study as “sets” and others as their “elements.” Thus we make the following definition.

\begin{definition}
A notion of set and element in a untyped first-order theory consists of:

* A binary predicate $(-)=(-)$ called *equality*

* A unary predicate $\mathrm{set}(-)$ called *being a set*

* A unary predicate $\mathrm{element}(-)$ called *being an element*

* A binary predicate $(-)\in(-)$ called *membership*

such that 

* if $a \in b$, then $a$ is an element and $b$ is a set

$$\forall a.\forall b.(a \in b) \to \mathrm{element}(a) \wedge \mathrm{set}(b)$$

* extensionality for sets and elements: for all $a$ and for all $b$, if a and b are sets, then $a = b$ if and only if, for all $c$, if $c$ is an element, then $c \in a$ if and only if $c \in b$

$$\forall a.\forall b.(\mathrm{set}(a) \wedge \mathrm{set}(b)) \implies ((a = b) \iff \forall c.(\mathrm{element}(c) \implies ((c \in a) \iff (c \in b))))$$
\end{definition}

Examples include

* [[ZFC]], where $\mathrm{set}(a)$ and $\mathrm{element}(a)$ is $\top$ for all objects $a$, $\in$ is the primitive membership relation and $=$ is defined through the axiom of extensionality. 

* [[ZFA]], where sets are defined as precisely those objects which are not elements $\mathrm{set}(a) \equiv \neg \mathrm{element}(a)$, $\in$ is the primitive membership relation and $=$ is defined through the axiom of extensionality. 

* [[fully formal ETCS]], which has $=$ as a primitive, and a specified symbol $1$ representing the [[identity morphism]] of the [[terminal object]], as well as $s$ and $t$ representing source and target morphisms. Sets are morphisms with target $1$, $\mathrm{set}(A) \equiv t(A) = 1$, and elements are morphisms with source $1$, $\mathrm{element}(a) \equiv s(a) = 1$. The membership relaiton $\in$ is defined by $a$ being an element, $A$ being a set, and the target of $a$ being equal to the source of $A$, $a \in A \equiv \mathrm{element}(a) \wedge \mathrm{set}(A) \wedge t(a) = s(A)$.

## Examples

### Fully formal ETCS

The untyped first-order theory of [[fully formal ETCS]] is a [[material set theory]] whose basic primitives are 

* [[morphisms]], 
* a binary predicate $=$ representing [[equality]] of morphisms,
* a function $s$ representing the [[identity morphism]] of the [[source]] of a morphism, 
* a function $t$ representing the identity morphism of the [[target]] of a morphism, 
* a ternary predicate $c$ which represents whether the first two morphisms are composable and the [[composite]] is the third morphism,
* a constant $1$ representing the identity morphism of the [[terminal object]]
* a quaternary predicate $p$ which represents whether four morphisms form a pullback square. 
* a function $P$ representing the identity morphism of the [[power object]] of the target of the morphism
* functions $\lambda$ and $\rho$ representing the [[jointly monic]] [[span]] for the local membership relation between [[elements]] and [[subobjects]] of a [[object]]. 
* constants $N$, $0$, $s$, representing the identity morphism of the [[natural numbers object]], the [[zero]] [[global element]], and the successor endomorphism of the natural numbers object

and axioms making the theory into a theory of a [[strict category|strict]] [[well-pointed topos]] with [[natural numbers object]] and the [[axiom of choice]]. 

Elements are represented by morphisms with source $1$, and sets are represented by morphisms with target $1$. An element is said to be in a set if the target of the element morphism is equal to the source of the set morphism. Thus, we can define the **global membership predicate** $\in$ on the morphisms as follows:

$$a \in A \coloneqq (t(A) = 1) \wedge (s(a) = 1) \wedge (s(A) = t(a))$$

This implies that $1$ is a [[reflexive set]], because by definition of a [[terminal object]] in the single-sorted definition of a finitely complete category, $t(1) = 1$, $s(1) = 1$, and $s(1) = t(1)$, which means that $1 \in 1$. This means that the [[axiom of foundation]] fails for $\in$. 

The well-pointedness condition for toposes implies that the membership relation $\in$ is an [[extensional relation]]: since $1$ is a [[separator]] and sets are morphisms into $1$, well-pointedness implies that sets $A$ and $B$ are equal if their elements are all equal to each other. 

Since [[fully formal ETCS]] has a global membership predicate which is an [[extensional relation]], and a morphism $1$ which is a [[reflexive set]] with regards to the global membership predicate, it is a [[material set theory]] where the [[axiom of foundation]] does not hold. 

## Related concepts

* [[cumulative hierarchy]]

* [[set-theoretic multiverse]]

## References

Relation to [[structural set theory]] is discussed in

* {#Shulman18} [[Michael Shulman]], _Comparing material and structural set theories_ ([arXiv:1808.05204](https://arxiv.org/abs/1808.05204))

See also

* {#Friedman1997} [[Harvey Friedman]] (1997). [Foundational Completeness](https://cs.nyu.edu/pipermail/fom/1997-November/000143.html). FOM, 1997 November.

[[!redirects material set theory]]
[[!redirects material set theories]]
