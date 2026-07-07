
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### $(0,1)$-Category theory
+--{: .hide}
[[!include (0,1)-category theory - contents]]
=--
=--
=--

\tableofcontents

## Idea

Prelattices are [[lattices]] which do not necessarily satisfy [[antisymmetry]]. 

## Definition

In the same way as lattices, prelattices can be defined in an [[algebra|algebraic]] or an [[order theory|order-theoretic]] fashion. In the algebraic definition, one uses an [[equivalence relation]] $\equiv$ instead of [[equality]] $=$ to define the equational axioms of the algebraic structure (commutativity, associativity, etc) as well as axioms that the algebraic operations are $\equiv$-[[extensional function|extensional]], similarly to the [[setoid]] approach to algebra. In the order-theoretic definition, one assumes a [[preorder]] instead of a [[partial order]]. 

\begin{definition}
An algebraic **prelattice** is a set $A$ with an [[equivalence relation]] $\equiv$ and two [[binary operations]] $\vee$ and $\wedge$ on $A$ which are 

1. $\equiv$-[[extensional function|extensional]] in that for all elements $w \in A$, $x \in A$, $y \in A$, $z \in A$, if $w \equiv y$ and $x \equiv z$, then $w \vee x \equiv y \vee z$ and $w \wedge x \equiv y \wedge z$. 

1. associative in that for all elements $x \in A$, $y \in A$, $z \in A$, $(x \vee y) \vee z \equiv x \vee (y \vee z)$ and $(x \wedge y) \wedge z \equiv x \wedge (y \wedge z)$. 

1. commutative in that for all elements $x \in A$ and $y \in A$, $x \vee y \equiv y \vee x$ and $x \wedge y \equiv y \wedge x$. 

1. idempotent in that for all elements $x \in A$, $x \vee x \equiv x$ and $x \wedge x \equiv x$. 

and which satisfy the absorption laws in that for all elements $x \in A$ and $y \in A$, $x \vee (x \wedge y) \equiv x$ and $x \wedge (x \vee y) \equiv x$. 
\end{definition}

\begin{definition}
An order-theoretic **prelattice** is a set $A$ with a [[preorder]] $\leq$ and [[binary operations]] $\vee$ and $\wedge$ on $A$ such that for all $x \in A$ and $y \in A$, $x \leq x \vee y$, $y \leq x \vee y$, $x \wedge y \leq x$ and $x \wedge y \leq y$. 
\end{definition}

These definitions of a prelattice are equivalent to each other. The [[equivalence relation]] on an order-theoretic prelattice is defined as $x \equiv y \coloneqq x \leq y \wedge y \leq x$, and the binary relation on an order-theoretic prelattice is an algebraic prelattice with respect to the equivalence relation $\equiv$. Conversely, every algebraic prelattice can be made into an order-theoretic prelattice by defining $x \leq y \coloneqq x \vee y \equiv y$ or $x \leq y \coloneqq x \wedge y \equiv x$. 

The [[quotient set]] of a prelattice by the [[equivalence relation]] $x \equiv y$ is a [[lattice]].

Also in the same way as lattices, one could either assume that prelattices have top and bottom elements, in which those without top and bottom elements are **unboounded prelattices** or **pseudoprelattices**, or prelattices do not have top and bottom elements, in which those with top and bottom elements are **bounded prelattices**. 

## As a category

A bounded prelattice is equivalently a bicartesian monoidal preorder, a [[thin]] [[cartesian monoidal category]] which is also a [[cocartesian monoidal category]]. An unbounded prelattice is equivalently a thin [[locally cartesian category]] whose [[opposite category]] is also locally cartesian. 

## Examples

One example of bounded prelattices include [[Heyting prealgebras]]. Two other examples are the [[integers]] $\mathbb{Z}$ and the [[polynomial ring]] $K[x]$ of a [[discrete field]] $K$, with respect to the divisibility [[preorder]] $a \vert b$, the [[greatest common divisor]] $\gcd$, and the [[least common multiple]] $\lcm$; unlike the natural numbers, these only form a bounded prelattice because there are more than one element in the [[group of units]] of both $\mathbb{Z}$ and $K[x]$, where $\mathbb{Z}^\times \coloneqq \{1, -1\}$ and $K[x]^\times \coloneqq K^\times$. 

Unbounded prelattices are important because given any ordered field $K$ with unbounded [[lattice]] structure, every [[ordered Artinian local ring|ordered Artinian local $K$-algebra]] is a unbounded prelattice. Ordered Artinian local $K$-algebras are used in [[synthetic differential geometry]]. 

## Related concepts

* [[preorder]]

* [[presemilattice]]

* [[total preorder]]

* [[Heyting prealgebra]]

* [[prelattice-ordered ring]]

* [[prelattice object]]

* [[lattice]]

## References

* [[Franco Montagna]], [[Andrea Sorbi]], *Universal recursion theoretic properties of r.e. preordered structures*, Journal of Symbolic Logic. 1985;50(2):397-406. &lbrack;[doi:10.2307/2274228](https://doi.org/10.2307/2274228)&rbrack;

* [[Uri Andrews]], [[Andrea Sorbi]], *Effective Inseparability, Lattices, and Preordering Relations*, The Review of Symbolic Logic. 2021;14(4):838-865. &lbrack;[doi:10.1017/S1755020319000273](https://doi.org/10.1017/S1755020319000273), [arXiv:1901.06136](https://arxiv.org/abs/1901.06136)&rbrack;

[[!redirects prelattice]]
[[!redirects prelattices]]

[[!redirects bounded prelattice]]
[[!redirects bounded prelattices]]

[[!redirects unbounded prelattice]]
[[!redirects unbounded prelattices]]

[[!redirects pseudoprelattice]]
[[!redirects pseudoprelattices]]

[[!redirects bicartesian monoidal preorder]]
[[!redirects bicartesian monoidal preorders]]

