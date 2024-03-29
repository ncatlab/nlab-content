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

All quotient inductive types described below are given together with some pseudo-[[Coq]] code, which would implement that QIT if Coq supported QITs natively.

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

A definition of the dyadic rationals as a [[symmetric midpoint algebra]]

    Inductive dyadic : Type :=
    | zero : dyadic
    | succ : dyadic -> dyadic
    | neg : dyadic -> dyadic
    | mid : dyadic -> dyadic -> dyadic
    | inv : forall (x : dyadic) neg neg x == x
    | idem : forall (x : dyaduc) mid x x == x
    | comm : forall (x y : dyadic) mid x y == mid y x
    | medial : forall (w x y z : dyadic) mid (mid w x) (mid y z) = mid (mid w y) (mid x z)
    | neutr : forall (x : dyadic) mid (neg x) x == zero
    | distneg : forall (x y : dyadic) mid (neg x) (neg y) == neg mid x y
    | distsucc : forall forall (x y : dyadic) mid (succ x) (succ y) == succ mid x y
    | twicesucc : forall forall (x y : dyadic) mid (succ succ x) y == succ mid x y
    | contr1 : forall (x y : dyadic) (p q : x == y), p == q.

### Classically extended natural numbers

The [[set]] of [[extended natural numbers]] as it behaves in [[classical mathematics]] as a quotient inductive type

    Inductive extnat : Type :=
    | zero : extnat
    | succ : extnat -> extnat
    | inf : extnat
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

### Sierpinski space

A definition of [[Sierpinski space]]:

    Inductive sierpinski : Type :=
    | top : sierpinski
    | meet : sierpinski -> sierpinski -> sierpinski
    | meet-left-unital : forall (a : sierpinski) meet top a = a
    | meet-right-unital : forall (a : sierpinski) meet a top = a
    | meet-associative : forall (a b c : sierpinski) meet meet a b c = meet a meet b c
    | meet-commutative : forall (a b : sierpinski) meet a b = meet b a
    | meet-idempotent : forall (a : sierpinski) meet a a = a
    | bottom : sierpinski
    | join : sierpinski -> sierpinski -> sierpinski
    | join-left-unital : forall (a : sierpinski) join bottom a = a
    | join-right-unital : forall (a : sierpinski) join a bottom = a
    | join-associative : forall (a b c : sierpinski) join join a b c = join a join b c
    | join-commutative : forall (a b : sierpinski) join a b = join b a
    | join-idempotent : forall (a : sierpinski) join a a = a
    | meet-join-absorption : forall (a b : sierpinski) meet a join a b = a
    | join-meet-absorption : forall (a b : sierpinski) join a meet a b = a
    | sequence-join : (nat -> sierpinski) -> sierpinski
    | sequence-bounded-above : forall (n : nat) (s : nat -> sierpinski) meet s n sequence-join s = s n
    | sequence-least-upper-bound : forall (a : sierpinski) (s : nat -> sierpinski) (forall (n : nat) meet s n a = s n) -> (meet sequence-join s x = sequence-join s)
    | element-sequence-meet : (sierpinski) -> (nat -> sierpinski) -> (nat -> sierpinski)
    | p : forall (a : sierpinski) (s : nat -> sierpinski) element-sequence-meet a s n = meet a s n
    | distributive : forall (a : sierpinski) (s : nat -> sierpinski) meet a sequence-join s = sequence-join element-sequence-meet a s 
    | contr1 : forall (x y : int) (p q : x == y), p == q.

### Cumulative hierarchy

According to [[Homotopy Type Theory -- Univalent Foundations of Mathematics]] the [[cumulative hierarchy]] of material sets could be constructed from a type universe as a quotient inductive type. 

### Cauchy complete real numbers

According to [[Homotopy Type Theory -- Univalent Foundations of Mathematics]] the [[Cauchy complete]] [[real numbers]] could be constructed from a type universe as a quotient [[inductive-inductive type]]. 

### Permutable trees

Altenkirch et al. gives the following definition of a permutable tree: 

    Inductive tree (A : Type) :=
    | leaf : tree A
    | node : (A -> tree A) -> tree A
    | mix : (forall (e : A -> A) isequiv(e)) -> (forall (e : A -> A) forall (f: A -> tree A) node f = node(f \circ e)
    | contr1 : forall (x y : tree A) (p q : x == y), p == q.

### Free posets

A definition of a [[free object|free]] [[poset]] as a quotient inductive-inductive type:

    Inductive poset (A: Type) :=
    | inj: A -> poset A
    | antisym: (forall x y : poset A) (x \leq y) -> (y \leq x) -> (x == y)
    | setcontr: forall (x y: poset A) (p q : x == y), p == q.

    Inductive \leq {poset A}: poset A -> poset A -> Type :=
    | refl: (forall x: poset A) x \leq x
    | trans: (forall x y z: poset A) (x \leq y) -> (y \leq z) -> (x \leq z)
    | pordercontr: forall (x y : poset A) (p q : x \leq y), p == q.


### Free pointed omega-complete partial orders
 {#FreePointedOmegaCompletePartialOrders}

It is possible to define the [[free object|free]] [[pointed object|pointed]] [[countable ordinal|omega]]-complete [[partial order]] on a 0-truncated type $A$ as a quotient inductive type. They are usually abbreviated as free pointed $\omega$-cpos (see [Altenkirch, Danielsson, and Kraus 2017,  §3.2](#ADK2017))


    Inductive omegacpo (A: Type) :=
    | inj: A -> omegacpo A
    | bottom: omegacpo A
    | denumjoin: (exists a: nat -> omegacpo A) (forall n: nat) a n \leq a succ n
    | antisym: (forall x y : omegacpo A) (x \leq y) -> (y \leq x) -> (x == y)
    | setcontr: forall (x y: omegacpo A) (p q : x == y), p == q.

    Inductive \leq {omegacpo A}: omegacpo A -> omegacpo A -> Type :=
    | refl: (forall x: omegacpo A) x \leq x
    | trans: (forall x y z: omegacpo A) (x \leq y) -> (y \leq z) -> (x \leq z)
    | init: (forall x : omegacpo A) bottom \leq x
    | upperbound: (forall a: nat -> omegacpo A) ((forall n: nat) a n) \leq denumjoin a p
    | leastupper: (forall x : omegacpo A) ((forall a: nat -> omegacpo A) ((forall n: nat) a n) \leq x) -> (forall a: nat -> omegacpo A) denum a p \leq x)
    | pordercontr: forall (x y : poset A) (p q : x \leq y), p == q.

Examples include the [[Sierpinski space]] $1_\bot$. 

### Internal type theory

From Altenkirch and Kaposi 2017

## Related concepts

* [[higher inductive type]]

## References

* [[Univalent Foundations Project]], section 11 of _[[Homotopy Type Theory -- Univalent Foundations of Mathematics]]_ (2013)

* {#ADK2017} [[Thorsten Altenkirch]], [[Nils Anders Danielsson]], [[Nicolai Kraus]], *Partiality, Revisited: The Partiality Monad as a Quotient Inductive-Inductive Type*, FoSSaCS 2017, Lecture Notes in Computer Science **10203** Springer (2017) &lbrack;[arXiv:1610.09254](https://arxiv.org/abs/1610.09254)&rbrack; 

* [[Thorsten Altenkirch]], [[Paolo Capriotti]], [[Gabe Dijkstra]], [[Fredrik Nordvall Forsberg]], *Quotient inductive-inductive types*, [arXiv](https://arxiv.org/abs/1612.02346), 2016

* [[Thorsten Altenkirch]], [[Ambrus Kaposi]], *Type Theory in Type Theory using Quotient Inductive Types*, POPL17, 2017 [PDF](http://www.cs.nott.ac.uk/~psztxa/publ/tt-in-tt.pdf)

* [[Thorsten Altenkirch]], [[Luis Scoccola]], *The Integers as a Higher Inductive Type*, [arXiv](https://arxiv.org/abs/2007.00167)

[[!redirects quotient inductive types]]