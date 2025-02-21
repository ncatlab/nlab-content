
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

An apartness ring $R$ where the apartness relation is a [[tight apartness relation]] is called a *[[tight apartness ring]]*. 

## Examples

* Every [[local ring]] equipped with the apartness relation $x \# y$ given by invertibility of $y - x$ is an apartness ring. 

* Every [[approximate integral domain]] is an apartness ring where the apartness relation $x \# y$ is given by [[cancellative element|cancellativity]] of $y - x$. 

* Every [[seminorm|semi]][[normed ring]] is an apartness ring where the apartness relation $x \# y$ is given by $0 \lt \vert y - x \vert$. 

* Every [[strictly weakly ordered ring]] is an apartness ring where the apartness relation $x \# y$ is given by the relation $(x \lt y) \vee (y \lt x)$. In the presence of [[excluded middle]], strictly weakly ordered rings are [[totally preordered rings]] where $x \lt y$ is given by the [[negation]] of the [[total preorder]] $y \leq x$. 

## Related concepts

* [[ring]]

* [[local ring]]

* [[strictly weakly ordered ring]], [[totally preordered ring]]

* [[ring setoids]]

* [[inequality ring]]

* [[tight apartness ring]]

* [[antisubalgebra]]

* [[antithesis interpretation]]

## References

* {#TroelstraVanDalen88} [[Anne Sjerp Troelstra]], [[Dirk van Dalen]]: *Constructivism in Mathematics -- An introduction*, Volume II, Studies in Logic and the Foundations of Mathematics **123**: North Holland (1988) &lbrack;[ISBN:9780444703583](https://shop.elsevier.com/books/constructivism-in-mathematics-vol-2/troelstra/978-0-444-70358-3)&rbrack;

* {#Shulman2022} [[Michael Shulman]], *Affine logic for constructive mathematics*. Bulletin of Symbolic Logic, Volume 28, Issue 3, September 2022. pp. 327 - 386 ([doi:10.1017/bsl.2022.28](https://doi.org/10.1017/bsl.2022.28), [arXiv:1805.07518](https://arxiv.org/abs/1805.07518))

[[!redirects apartness ring]]
[[!redirects apartness rings]]

[[!redirects ring with apartness]]
[[!redirects rings with apartness]]

[[!redirects apartness algebra]]
[[!redirects apartness algebras]]

[[!redirects algebra with apartness]]
[[!redirects algebras with apartness]]