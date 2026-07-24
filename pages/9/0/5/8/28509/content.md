
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### $(0,1)$-Category theory
+--{: .hide}
[[!include (0,1)-category theory - contents]]
=--
#### Algebra
+--{: .hide}
[[!include algebra - contents]]
=--
=--
=--

\tableofcontents

## Idea

Presemilattices are [[semilattices]] which do not necessarily satisfy [[antisymmetry]]. 

## Definition

In the same way as semilattices, presemilattices can be defined in an [[algebra|algebraic]] or an [[order theory|order-theoretic]] fashion. In the algebraic definition, one uses an [[equivalence relation]] $\equiv$ instead of [[equality]] $=$ to define the equational axioms of the algebraic structure (commutativity, associativity, etc) as well as axioms that the algebraic operations are $\equiv$-[[extensional function|extensional]], similarly to the [[setoid]] approach to algebra. In the order-theoretic definition, one assumes a [[preorder]] instead of a [[partial order]], and defines a *join-presemilattice* as a preorder with binary [[joins]] and a *meet-presemilattice* as a preorder with binary [[meets]].
 
\begin{definition}
An algebraic **presemilattice** is a set $A$ with an [[equivalence relation]] $\equiv$ and a [[binary operation]] $\cdot$ on $A$ which is 

1. $\equiv$-[[extensional function|extensional]] in that for all elements $w \in A$, $x \in A$, $y \in A$, $z \in A$, if $w \equiv y$ and $x \equiv z$, then $w \cdot x \equiv y \cdot z$. 

1. associative in that for all elements $x \in A$, $y \in A$, $z \in A$, $(x \cdot y) \cdot z \equiv x \cdot (y \cdot z)$. 

1. commutative in that for all elements $x \in A$ and $y \in A$, $x \cdot y \equiv y \cdot x$. 

1. idempotent in that for all elements $x \in A$, $x \cdot x \equiv x$. 

\end{definition}

\begin{definition}
A **join-presemilattice** is a set $A$ with a [[preorder]] $\leq$ and a [[binary operation]] $\vee$ on $A$ such that for all $x \in A$ and $y \in A$, $x \leq x \vee y$ and $y \leq x \vee y$. 
\end{definition}

\begin{definition}
A **meet-presemilattice** is a set $A$ with a [[preorder]] $\leq$ and a [[binary operation]] $\wedge$ on $A$ such that for all $x \in A$ and $y \in A$, $x \wedge y \leq x$ and $x \wedge y \leq y$. 
\end{definition}

These definitions of a presemilattice are equivalent to each other. Given a join-presemilattice, the [[opposite preorder]] on the set is a meet-presemilattice, and given a meet-presemilattice, the opposite preorder on the set is a join-presemilattice. The [[equivalence relation]] on a join-presemilattice or a meet-presemilattice is defined as $x \equiv y \coloneqq x \leq y \wedge y \leq x$, and the binary relation on a join-presemilattice or a meet-presemilattice is an algebraic presemilattice with respect to the equivalence relation $\equiv$. Conversely, every algebraic presemilattice can be made into a join-presemilattice by defining $x \leq y \coloneqq x \cdot y \equiv y$ or a meet-presemilattice by defining $x \leq y \coloneqq x \cdot y \equiv x$. 

The [[quotient set]] of a presemilattice by its [[equivalence relation]] $x \equiv y$ is a [[semilattice]].

### Bounded and unbounded presemilattices

Similarly to [[semilattices]], there is also the question of whether presemilattices are bounded or not, in the sense of a [[bounded lattice]]. With the algebraic definition of a presemilattice, one could either assume that presemilattices have [[neutral elements]] or [[absorbing elements]] or both or neither. With the order-theoretic definition of a presemilattice, one could either assume that presemilattices have [[top elements]] or [[bottom elements]] or both or neither. This yields four different kinds of presemilattices: 

* those presemilattices without either neutral elements or absorbing elements are **unbounded presemilattices** 

* those presemilattices with only neutral elements are **bounded presemilattices**  

* those presemilattices with only absorbing elements do not seem to have a name in the literature, but are still bounded from the opposite direction

* those presemilattices with both neutral and absorbing elements are **[[01-bounded semilattices|01-bounded]] presemilattices**

In a join-presemilattice, the [[top element]], if it exists, is a [[neutral element]] and the [[bottom element]], if it exists, is an [[absorbing element]] for the [[join]] operation. Likewise, in a meet-presemilattice, the [[bottom element]], if it exists, is a [[neutral element]] and the [[top element]], if it exists, is an [[absorbing element]] for the [[meet]] operation. 

## As a category

* A bounded meet-presemilattice is equivalently a cartesian monoidal preorder, a [[thin]] [[cartesian monoidal category]].

* A bounded join-presemilattice is equivalently a cocartesian monoidal preorder, a [[thin]] [[cocartesian monoidal category]].

* An unbounded meet-presemilattice is equivalently a thin [[locally cartesian category]]. 

* An unbounded join-presemilattice is equivalently a thin category whose [[opposite category]] is a [[locally cartesian category]]. 

## Related concepts

* [[preorder]]

* [[prelattice]]

* [[semilattice]]

## References

* [[Norman R. Reilly]], *Enlarging the Munn representation of inverse semigroups*, Journal of the Australian Mathematical Society. 1977;23(1):28-41. &lbrack;[doi:10.1017/S1446788700017316](https://doi.org/10.1017/S1446788700017316)&rbrack;

* [[Uri Andrews]], [[Andrea Sorbi]], *Effective Inseparability, Lattices, and Preordering Relations*, The Review of Symbolic Logic. 2021;14(4):838-865. &lbrack;[doi:10.1017/S1755020319000273](https://doi.org/10.1017/S1755020319000273), [arXiv:1901.06136](https://arxiv.org/abs/1901.06136)&rbrack;

[[!redirects presemilattice]]
[[!redirects presemilattices]]

[[!redirects pre-semilattice]]
[[!redirects pre-semilattices]]

[[!redirects presemi-lattice]]
[[!redirects presemi-lattices]]

[[!redirects pre-semi-lattice]]
[[!redirects pre-semi-lattices]]

[[!redirects join-presemilattice]]
[[!redirects join-presemilattices]]

[[!redirects join-pre-semilattice]]
[[!redirects join-pre-semilattices]]

[[!redirects join-presemi-lattice]]
[[!redirects join-presemi-lattices]]

[[!redirects join-pre-semi-lattice]]
[[!redirects join-pre-semi-lattices]]

[[!redirects meet-presemilattice]]
[[!redirects meet-presemilattices]]

[[!redirects meet-pre-semilattice]]
[[!redirects meet-pre-semilattices]]

[[!redirects meet-presemi-lattice]]
[[!redirects meet-presemi-lattices]]

[[!redirects meet-pre-semi-lattice]]
[[!redirects meet-pre-semi-lattices]]

[[!redirects bounded presemilattice]]
[[!redirects bounded presemilattices]]

[[!redirects bounded pre-semilattice]]
[[!redirects bounded pre-semilattices]]

[[!redirects bounded presemi-lattice]]
[[!redirects bounded presemi-lattices]]

[[!redirects bounded pre-semi-lattice]]
[[!redirects bounded pre-semi-lattices]]

[[!redirects bounded join-presemilattice]]
[[!redirects bounded join-presemilattices]]

[[!redirects bounded join-pre-semilattice]]
[[!redirects bounded join-pre-semilattices]]

[[!redirects bounded join-presemi-lattice]]
[[!redirects bounded join-presemi-lattices]]

[[!redirects bounded join-pre-semi-lattice]]
[[!redirects bounded join-pre-semi-lattices]]

[[!redirects bounded meet-presemilattice]]
[[!redirects bounded meet-presemilattices]]

[[!redirects bounded meet-pre-semilattice]]
[[!redirects bounded meet-pre-semilattices]]

[[!redirects bounded meet-presemi-lattice]]
[[!redirects bounded meet-presemi-lattices]]

[[!redirects bounded meet-pre-semi-lattice]]
[[!redirects bounded meet-pre-semi-lattices]]

[[!redirects unbounded presemilattice]]
[[!redirects unbounded presemilattices]]

[[!redirects unbounded pre-semilattice]]
[[!redirects unbounded pre-semilattices]]

[[!redirects unbounded presemi-lattice]]
[[!redirects unbounded presemi-lattices]]

[[!redirects unbounded pre-semi-lattice]]
[[!redirects unbounded pre-semi-lattices]]

[[!redirects unbounded join-presemilattice]]
[[!redirects unbounded join-presemilattices]]

[[!redirects unbounded join-pre-semilattice]]
[[!redirects unbounded join-pre-semilattices]]

[[!redirects unbounded join-presemi-lattice]]
[[!redirects unbounded join-presemi-lattices]]

[[!redirects unbounded join-pre-semi-lattice]]
[[!redirects unbounded join-pre-semi-lattices]]

[[!redirects unbounded meet-presemilattice]]
[[!redirects unbounded meet-presemilattices]]

[[!redirects unbounded meet-pre-semilattice]]
[[!redirects unbounded meet-pre-semilattices]]

[[!redirects unbounded meet-presemi-lattice]]
[[!redirects unbounded meet-presemi-lattices]]

[[!redirects unbounded meet-pre-semi-lattice]]
[[!redirects unbounded meet-pre-semi-lattices]]

[[!redirects cartesian monoidal preorder]]
[[!redirects cartesian monoidal preorders]]

[[!redirects cocartesian monoidal preorder]]
[[!redirects cocartesian monoidal preorders]]

