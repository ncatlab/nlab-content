

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Algebra
+-- {: .hide}
[[!include algebra - contents]]
=--
#### Constructivism, Realizability, Computability
+-- {: .hide}
[[!include constructivism - contents]]
=--
=--
=--

\tableofcontents

## Idea

A [[ring]] equipped with an [[tight apartness relation]] such that all ring operations are [[strongly extensional]] in that they reflect the tight apartness relation. 

In [[classical mathematics]], every [[tight apartness relation]] is logically equivalent to the [[denial inequality]], so tight apartness rings are equivalent to [[rings]]. But in [[constructive mathematics]], not every [[tight apartness relation]] is logically equivalent to [[denial inequality]]; hence the concept of a *ring with tight apartness* or a *tight apartness ring*. 

In some parts of the constructive algebra literature, it is common for the unadorned term "ring" to refer to tight apartness rings, and for "algebra" to refer to tight apartness $R$-algebras. 

## Definition

A [[ring]] $R$ is an **tight apartness ring** or a **ring with tight apartness** if it comes with an [[tight apartness relation]] $a \# b$ such that

* for all $a, b, c, d \in R$, $a + b \# c + d$ implies that $a \# c$ or $b \# d$

* for all $a, b \in R$, $-a \# -b$ implies that $a \# b$

* for all $a, b, c, d \in R$, $a \cdot b \# c \cdot d$ implies that $a \# c$ or $b \# d$

## Properties

While [[rings]] are algebraic in the sense that they can be defined inside of a [[Lawvere theory]], tight apartness rings can only be defined in a [[Heyting category]] due to the negation used in the [[tight relation|tightness]] condition of the tight apartness relation of a tight apartness ring and the disjunction used in the strong extensionality of the binary ring operations, and thus are not algebraic in the above sense. 

### Category of tight apartness rings

The category of tight apartness rings is the [[category]] whose [[objects]] are tight apartness rings and whose morphisms are [[strongly extensional]] [[ring homomorphisms]]. The [[initial object]] is the ring of [[integers]] $\mathbb{Z}$, and the [[terminal object]] is the [[trivial ring]] $0$. 

## Examples

* Every [[Heyting field]] is an apartness ring where the tight apartness relation $x \# y$ is given by invertibility of $y - x$. 

* Every [[Heyting integral domain]] is an apartness ring where the tight apartness relation $x \# y$ is given by [[cancellative element|cancellativity]] of $y - x$. 

* Every [[normed ring]] is an apartness ring where the tight apartness relation $x \# y$ is given by $0 \lt \vert y - x \vert$. 

* Every [[pseudo-ordered ring]] is an apartness ring where the apartness relation $x \# y$ is given by the relation $(x \lt y) \vee (y \lt x)$. In the presence of [[excluded middle]], pseudo-ordered rings are [[totally ordered rings]] where $x \lt y$ is given by the [[negation]] of the [[total order]] $y \leq x$. 

## Discrete rings

In [[constructive mathematics]], a ring is said to be **discrete** if it is a tight apartness ring whose apartness relation is also [[decidable relation]]. Thus, [[discrete integral domains]] and [[discrete fields]] are discrete rings. In classical mathematics, every ring is discrete in this sense due to [[excluded middle]]. Note that the use of "discrete ring" in constructive algebra is not the same as the notion of [[discrete space|topologically discrete]] [[topological rings]] in [[topology|topological]] [[algebra]] and [[analysis]]. 

## Related concepts

* [[ring]]

* [[field]]

* [[integral domain]]

* [[pseudo-ordered ring]], [[totally ordered ring]]

* [[normed ring]]

* [[inequality ring]]

* [[apartness ring]]

* [[antisubalgebra]]

## References

* {#TroelstraVanDalen88} [[Anne Sjerp Troelstra]], [[Dirk van Dalen]]: *Constructivism in Mathematics -- An introduction*, Volume II, Studies in Logic and the Foundations of Mathematics **123**: North Holland (1988) &lbrack;[ISBN:9780444703583](https://shop.elsevier.com/books/constructivism-in-mathematics-vol-2/troelstra/978-0-444-70358-3)&rbrack;

* {#Shulman2022} [[Michael Shulman]], *Affine logic for constructive mathematics*. Bulletin of Symbolic Logic, Volume 28, Issue 3, September 2022. pp. 327 - 386 ([doi:10.1017/bsl.2022.28](https://doi.org/10.1017/bsl.2022.28), [arXiv:1805.07518](https://arxiv.org/abs/1805.07518))

[[!redirects tight apartness ring]]
[[!redirects tight apartness rings]]

[[!redirects ring with tight apartness]]
[[!redirects rings with tight apartness]]

[[!redirects discrete ring]]
[[!redirects discrete rings]]

[[!redirects tight apartness algebra]]
[[!redirects tight apartness algebras]]

[[!redirects algebra with tight apartness]]
[[!redirects algebras with tight apartness]]

[[!redirects discrete algebra]]
[[!redirects discrete algebras]]