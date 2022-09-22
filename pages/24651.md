
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Type theory
+-- {: .hide}
[[!include type theory - contents]]
=--
#### Category theory
+--{: .hide}
[[!include category theory - contents]]
=--
#### Algebra
+--{: .hide}
[[!include higher algebra - contents]]
=--
#### Monoid theory
+-- {: .hide}
[[!include monoid theory - contents]]
=--
=--
=--

# Contents
* table of contents
{:toc}

## Idea

In set theory, algebraic structures such as [[monoids]] are defined as a set with additional structure and equational axioms. However, in [[homotopy type theory]], there are two possible notions of what it means for a type to be a set, and what it means that a set has equational axioms. Traditionally in homotopy type theory, a set is defined using the [[identity type]], where every identity type between two elements $a:A$ and $b:A$ of a type $A$ is [[propositional truncation|propositionally truncated]]. However, equality in set theory is usually defined as an [[equivalence relation]], and one could directly translate the equivalence relation of equality into homotopy type theory, resulting in a [[symmetric proset]]. The equational axioms of algebraic structures could similarly be defined using the equivalence relation of the symmetric proset rather than the identity type. In the context of defining monoids, this results in the notion of a monoidal symmetric proset. 

## Definition

In [[homotopy type theory]], a *monoidal symmetric proset* is a [[symmetric proset]] $(M, \equiv_M)$ with a binary function $(-)\cdot(-):M \times M \to M$, an element $1:M$, and witnesses of associativity, left unitality, right unitality, and extensionality
$$a:M, b:M, c:M \vdash \mathrm{assoc}(a, b, c):(a \cdot b) \cdot c \equiv_M a \cdot (b \cdot c)$$
$$a:M \vdash \mathrm{lunit}(a):1 \cdot a \equiv_M a$$
$$a:M \vdash \mathrm{runit}(a):a \cdot 1 \equiv_M a$$
$$a:M, b:M, c:M, d:M \vdash \mathrm{ext}(a, b, c, d):(a \equiv_M b) \times (c \equiv_M d) \to (a \cdot c) \equiv_M (b \cdot d)$$

A monoidal symmetric proset is **univalent** or a **[[monoid]]** if the canonical function 
$$idtoequiv(a, b):(a =_M b) \to (a \equiv_M b)$$
is an equivalence of types for all elements $a:M$ and $b:M$. 

## Properties

Every monoidal symmetric proset is (the delooping of) a [[(2, 1)-preorder]] with only 1 object. 

## See also

* [[monoid]]
* [[symmetric proset]]
* [[(2, 1)-preorder]]
* [[monoidal groupoid]]
* [[monoidal category]]