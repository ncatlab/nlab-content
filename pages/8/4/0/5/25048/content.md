
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

In the same way as lattices, prelattices can be defined in an [[algebra|algebraic]] or an [[order theory|order-theoretic]] fashion. In the algebraic definition, one uses an [[equivalence relation]] $\equiv$ instead of [[equality]] $=$ to define the equational axioms of the algebraic structure (commutativity, associativity, etc) as well as axioms that the algebraic operations are $\equiv$-[[extensional function|extensional]], similarly to the [[setoid]] approach to algebra. In the order-theoretic definition, one assumes a [[preorder]] instead of a [[partial order]]. 

The [[quotient set]] of a prelattice by the [[equivalence relation]] $x \equiv y \coloneqq x \leq y \wedge y \leq x$ is a [[lattice]].

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

