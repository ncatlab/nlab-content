+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Type theory
+-- {: .hide}
[[!include type theory - contents]]
=--
#### Induction
+-- {: .hide}
[[!include induction - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

Quotient inductive types are [[higher inductive types]] with a [[0-truncation]] constructor. 

## Examples

All higher inductive types described below are given together with some pseudo-[[Coq]] code, which would implement that HIT if Coq supported HITs natively.

### Integers

A definition of the set of [[integers]] as a quotient inductive type. 

    Inductive int : Type :=
    | zero : int
    | succ : int -> int
    | pred : int -> int
    | sec : forall (x : int) pred succ x == x
    | ret : forall (x : int) succ pred x == x
    | contr1 : forall (x y : int) (p q : x == y), p == q.

Another definition of the integers as a quotient inductive type: 

    Inductive int : Type :=
    | zero : int
    | succ : int -> int
    | neg : int -> int
    | axiom1 : neg zero  == zero
    | axiom2 : forall (x : int) succ neg succ x == neg x
    | contr1 : forall (x y : int) (p q : x == y), p == q.

### Dyadic rational numbers

A minimal inductive definition of the [[dyadic rational numbers]] as a quotient inductive type: 

    Inductive dyadic : Type :=
    | zero : dyadic
    | succ : dyadic -> dyadic
    | pred : dyadic -> dyadic
    | act : nat -> dyadic -> dyadic
    | sec : forall (x : int) pred succ x == x
    | ret : forall (x : int) succ pred x == x
    | initfunc : forall (x : dyadic) act 0 x == succ x
    | funcsqrt : forall (n : nat) forall (x : dyadic) act (succ n) (act (succ n) x) == act n x
    | contr1 : forall (x y : dyadic) (p q : x == y), p == q.

### Classically extended natural numbers

The [[set]] of [[extended natural numbers]] as it behaves in [[classical mathematics]] as a quotient inductive type

    Inductive extnat : Type :=
    | zero : extnat
    | succ : extnat -> extnat
    | inf : extnat -> extnat
    | fixpoint : succ inf == inf
    | contr1 : forall (x y : int) (p q : x == y), p == q.

### Polynomial rings over integers

A definition of the [[polynomial ring]] over the integers with a set of indeterminants $A$. 

    Inductive intpoly (A: Type)  :=
    | indet : A -> (intpoly A)
    | zero : intpoly A
    | one : intpoly A
    | neg : (intpoly A) -> (intpoly A)
    | add : (intpoly A) -> (intpoly A) -> (intpoly A)
    | mult : (intpoly A) -> (intpoly A) -> (intpoly A)
    | alunital : forall (x : intpoly A) add zero x == x
    | arunital : forall (x : intpoly A) add x zero == x
    | aassoc : forall (x y z : intpoly A) add x (add y z) == add (add x y) z
    | acomm : forall (x y : intpoly A) add x y = add y x
    | alinv : forall (x : intpoly A) add (neg x) x == zero
    | arinv : forall (x : intpoly A) add x (neg x) == zero
    | ldist : forall (x y z : intpoly A) mult x (add y z) == add (mult x y) (mult x z)
    | rdist : forall (x y z : intpoly A) mult (add x y) z == add (mult x z) (mult y z)
    | mlunital : forall (x : intpoly A) mult one x == x
    | mrunital : forall (x : intpoly A) mult x one == x
    | massoc : forall (x y z : intpoly A) mult x (mult y z) == mult (mult x y) z
    | mcomm : forall (x y : intpoly A) mult x y = mult y x
    | contr1 : forall (x y : intpoly A) (p q : x == y), p == q.

### Quotients of sets

The [[quotient]] of an [[hProp]]-valued or (-1)-truncated [[equivalence relation]], yielding an [[hSet]] or [[0-truncated]] type:

    Inductive quotient (A : Type) (R : A -> A -> hProp) : Type :=
    | proj : A -> quotient A R
    | relate : forall (x y : A), R x y -> proj x == proj y
    | contr1 : forall (x y : quotient A R) (p q : x == y), p == q.

### Cumulative hierarchy

According to [[Homotopy Type Theory -- Univalent Foundations of Mathematics]] the [[cumulative hierarchy]] of material sets could be constructed from a type universe as a quotient inductive type. 

### Cauchy complete real numbers

According to [[Homotopy Type Theory -- Univalent Foundations of Mathematics]] the [[Cauchy complete]] [[real numbers]] could be constructed from a type universe as a quotient [[inductive-inductive type]]. 

### Partial map classifiers

From Altenkirch et al. 2018

### Internal type theory

From Altenkirch and Kaprosi 2017

## Related concepts

* [[higher inductive type]]

## References

* {#AltenkirchKaprosi} [[Thorsten Altenkirch]], Ambrus Kaposi, _Type Theory in Type Theory using Quotient Inductive Types_, POPL17, 2017 [PDF](http://www.cs.nott.ac.uk/~psztxa/publ/tt-in-tt.pdf)