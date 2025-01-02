
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

A [[ring]] equipped with an [[apartness relation]] such that all ring operations are [[strongly extensional]] in that they reflect the apartness relation. 

In [[classical mathematics]], every [[apartness relation]] is logically equivalent to the [[negation]] of an [[equivalence relation]], so apartness rings are equivalent to [[rings]] with an equivalence relation which are [[ring setoids]] with respect to the equivalence relation. But in [[constructive mathematics]], not every [[apartness relation]] is logically equivalent to the [[negation]] of an [[equivalence relation]]; hence the concept of a *ring with apartness* or an *apartness ring*. 

## Definition

A [[ring]] $R$ is an **apartness ring** or a **ring with apartness** if it comes with an [[apartness relation]] $a \# b$ such that

* for all $a, b, c, d \in R$, $a + b \# c + d$ implies that $a \# c$ or $b \# d$

* for all $a, b \in R$, $-a \# -b$ implies that $a \# b$

* for all $a, b, c, d \in R$, $a \cdot b \# c \cdot d$ implies that $a \# c$ or $b \# d$

## Examples

* Every [[local ring]] is an apartness ring where the apartness relation $x \# y$ is given by invertibility of $y - x$. 

* Every [[approximate integral domain]] is an apartness ring where the apartness relation $x \# y$ is given by [[cancellative element|cancellativity]] of $y - x$. 

* Every [[seminorm|semi]][[normed ring]] is an apartness ring where the apartness relation $x \# y$ is given by $0 \lt \vert y - x \vert$. 

* Every [[strictly weakly ordered ring]] is an apartness ring where the apartness relation $x \# y$ is given by the relation $(x \lt y) \vee (y \lt x)$. In the presence of [[excluded middle]], strictly weakly ordered rings are [[totally preordered rings]] where $x \lt y$ is given by the [[negation]] of the [[total preorder]] $y \leq x$. 

## Tight apartness rings

An apartness ring is said to be a **tight apartness ring** or a **ring with tight apartness** if the apartness relation is a [[tight apartness relation]]. In [[classical mathematics]], every [[ring]] is a tight apartness ring where the tight apartness is given by [[denial inequality]]. However, in [[constructive mathematics]], this is not the case and one can distinguish between rings in the usual sense and tight apartness rings. 

In some parts of the constructive algebra literature, it is common for the unadorned term "ring" to refer to tight apartness rings, and for "algebra" to refer to tight apartness $R$-algebras. 

While [[rings]] are algebraic in the sense that they can be defined inside of a [[Lawvere theory]], tight apartness rings can only be defined in a [[Heyting category]] due to the negation used in the [[tight relation|tightness]] condition of the tight apartness relaiton of a tight apartness ring and the disjunction used in the strong extensionality of the binary ring operations, and thus are not algebraic in the above sense. 

In [[constructive mathematics]], a ring is said to be **discrete** if it is a tight apartness ring whose apartness relation is also [[decidable relation]]. Thus, [[discrete integral domains]] and [[discrete fields]] are discrete rings. In classical mathematics, every ring is discrete in this sense due to [[excluded middle]]. Note that the use of "discrete ring" in constructive algebra is not the same as the notion of [[discrete space|topologically discrete]] [[topological rings]] in [[topology|topological]] [[algebra]] and [[analysis]]. 

## Related concepts

* [[ring]]

* [[local ring]]

* [[strictly weakly ordered ring]], [[totally preordered ring]]

* [[ring setoids]]

* [[inequality ring]]

* [[antisubalgebra]]

* [[antithesis interpretation]]

## References

* {#TroelstraVanDalen88} [[Anne Sjerp Troelstra]], [[Dirk van Dalen]]: *Constructivism in Mathematics -- An introduction*, Volume II, Studies in Logic and the Foundations of Mathematics **123**: North Holland (1988) &lbrack;[ISBN:9780444703583](https://shop.elsevier.com/books/constructivism-in-mathematics-vol-2/troelstra/978-0-444-70358-3)&rbrack;

* {#Shulman2022} [[Michael Shulman]], *Affine logic for constructive mathematics*. Bulletin of Symbolic Logic, Volume 28, Issue 3, September 2022. pp. 327 - 386 ([doi:10.1017/bsl.2022.28](https://doi.org/10.1017/bsl.2022.28), [arXiv:1805.07518](https://arxiv.org/abs/1805.07518))

[[!redirects apartness ring]]
[[!redirects apartness rings]]

[[!redirects ring with apartness]]
[[!redirects rings with apartness]]

[[!redirects tight apartness ring]]
[[!redirects tight apartness rings]]

[[!redirects ring with tight apartness]]
[[!redirects rings with tight apartness]]

[[!redirects discrete ring]]
[[!redirects discrete rings]]

[[!redirects apartness algebra]]
[[!redirects apartness algebras]]

[[!redirects algebra with apartness]]
[[!redirects algebras with apartness]]

[[!redirects tight apartness algebra]]
[[!redirects tight apartness algebras]]

[[!redirects algebra with tight apartness]]
[[!redirects algebras with tight apartness]]

[[!redirects discrete algebra]]
[[!redirects discrete algebras]]