
# (Semi)definiteness
* table of contents
{: toc}

## Idea

There are many contexts where terms such as 'positive definite', 'negative semidefinite', and 'indefinite' appear.  This is an attempt to describe a general framework in which these may be used.  Warning: this may be [[centipede mathematics]].


## Definitions

Let $A$ be a [[set]] equipped with both a [[partial order]] $\leq$ (whose [[opposite relation|opposite]] is denoted $\geq$), an [[inequality relation]] $#$ (that is an irreflexive, symmetric relation), and a [[basepoint]] $0$.  (Warning: $#$ is nontrivial even in [[classical mathematics]], and it is rarely [[tight relation|tight]].)  We write $\lt$ for the conjunction of $\leq$ and $#$ (and $\gt$ for its opposite, the conjunction of $\geq$ and $#$).

An element $x$ of $A$ is:

* __positive__ (or _positive semidefinite_) if $x \geq 0$,
* __negative__ (or _negative semidefinite_) if $x \leq 0$,
* __semidefinite__ if $x$ is positive or negatve,
* __indefinite__ if $x$ is not semidefinite,
* __nondegenerate__ if $x # 0$,
* __definite__ if $x$ is semidefinite and nondegenerate,
* __positive definite__ if $x \gt 0$ (that is if $x$ is both positive and nondegenerate),
* __negative definite__ if $x \lt 0$ (that is if $x$ is both negative and nondegenerate).

Note that a positive or negative element must be semidefinite, so 'positive semidefinite' and 'negative semidefinite' are redundant; in many contexts, however, this redundancy is useful, since 'positive' and 'negative' are so widely used in other contexts.  Also, since a semidefinite element is definite iff it\'s nondegenerate, 'positive definite' and 'negative definite' really mean what they say.

In [[constructive mathematics]], it is not the partial order $\leq$ that is most relevant but rather the relation $\nleq$, which classically is the [[negation]] of $\leq$ but which constructively is generally stronger.  This relation $\nleq$ is required to satisfy properties [[de Morgan duality|dual]] to those of a partial order ([[irreflexive relation|irreflexivity]], [[comparison]], and [[connected relation|connectedness]]), and $\leq$ is then defined as the negation of $\nleq$.  We say that $x$ is __indefinite__ if $x \nleq 0$ and $x \ngeq 0$, and that $x$ is __semidefinite__ if it is not indefinite; all of the other definitions read the same.  (So constructively, &#8249;semidefinite&#8250; is not &#8249;positive or negative&#8250; but rather the [[double negation]] of that.)

We will also say that $A$ is __nontrivial__ if there exists a nondegenerate element, that is an $x$ such that $x # 0$.

Suppose that $A$ has the structure of a [[group]], which we will write additively (but without assuming commutativity).  We will say that the group structure is _right-compatible_ with the partial order $\leq$ and the inequality $#$ if

* $x \leq y$ iff $y - x \geq 0$, and
* $x # y$ iff $y - x # 0$.

(Thus $\leq$ and $#$ are entirely recoverable from the positive and nondegenerate elements, respectively.  Constructively, we require that $x \nleq y$ iff $y - x \nleq 0$.)

We can similarly say when $A$ is _left-compatible_.  (By symmetry of $#$, this half of the compatibility condition is the same.)  Of course, if $A$ is [[abelian group|commutative]], then left- and right-compatibility are the same entirely.


## Examples

[to come]


[[!redirects semidefinite]]
[[!redirects semidefiniteness]]
[[!redirects semidefinite element]]
[[!redirects semidefinite elements]]

[[!redirects positive semidefinite]]
[[!redirects positive semidefiniteness]]
[[!redirects positive semidefinite element]]
[[!redirects positive semidefinite elements]]
[[!redirects positive-semidefinite]]
[[!redirects positive-semidefiniteness]]
[[!redirects positive-semidefinite element]]
[[!redirects positive-semidefinite elements]]

[[!redirects negative semidefinite]]
[[!redirects negative semidefiniteness]]
[[!redirects negative semidefinite element]]
[[!redirects negative semidefinite elements]]
[[!redirects negative-semidefinite]]
[[!redirects negative-semidefiniteness]]
[[!redirects negative-semidefinite element]]
[[!redirects negative-semidefinite elements]]

[[!redirects definite]]
[[!redirects definiteness]]
[[!redirects definite element]]
[[!redirects definite elements]]

[[!redirects positive definite]]
[[!redirects positive definiteness]]
[[!redirects positive definite element]]
[[!redirects positive definite elements]]
[[!redirects positive-definite]]
[[!redirects positive-definiteness]]
[[!redirects positive-definite element]]
[[!redirects positive-definite elements]]

[[!redirects negative definite]]
[[!redirects negative definiteness]]
[[!redirects negative definite element]]
[[!redirects negative definite elements]]
[[!redirects negative-definite]]
[[!redirects negative-definiteness]]
[[!redirects negative-definite element]]
[[!redirects negative-definite elements]]

[[!redirects indefinite]]
[[!redirects indefiniteness]]
[[!redirects indefinite element]]
[[!redirects indefinite elements]]
