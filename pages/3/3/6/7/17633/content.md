
# (Semi)definiteness
* table of contents
{: toc}

## Idea

There are many contexts where terms such as 'positive definite', 'negative semidefinite', and 'indefinite' appear.  This is an attempt to describe a general framework in which these may be used.  Warning: this may be [[centipede mathematics]].


## Definitions

Let $A$ be a [[set]] equipped with both a [[partial order]] $\leq$ (whose [[opposite relation|opposite]] is denoted $\geq$), an [[inequality relation]] $#$, and a [[basepoint]] $0$.  (Warning: even in [[classical mathematics]], $#$ is often weaker than the [[denial inequality]], and it is rarely a [[comparison relation]].)  We write $\lt$ for the conjunction of $\leq$ and $#$ (and $\gt$ for its opposite, the conjunction of $\geq$ and $#$).

An element $x$ of $A$ is:

* __positive__ (or _positive semidefinite_) if $x \geq 0$,
* __negative__ (or _negative semidefinite_) if $x \leq 0$,
* __indefinite__ if $x$ is neither positive nor negative,
* __semidefinite__ if $x$ is not indefinite,
* __nondegenerate__ if $x # 0$,
* __definite__ if $x$ is semidefinite and nondegenerate,
* __positive definite__ if $x \gt 0$ (that is if $x$ is both positive and nondegenerate),
* __negative definite__ if $x \lt 0$ (that is if $x$ is both negative and nondegenerate).

Note that a positive or negative element must be semidefinite, so 'positive semidefinite' and 'negative semidefinite' are redundant; in many contexts, however, this redundancy is useful, since 'positive' and 'negative' are so widely used in other contexts.  Also, since a semidefinite element is definite iff it\'s nondegenerate, 'positive definite' and 'negative definite' really mean what they say.

Assuming [[classical logic]], of course &#8249;semidefinite&#8250; simply means &#8249;positive or negative&#8250;, but we need the more convoluted definition in [[constructive mathematics]].  That said, it\'s fairly common for &#8249;definite&#8250; to mean &#8249;positive-definite or negative-definite&#8250; even constructively.  (It would be nice to find some simple compatibility relationship between $\leq$ and $#$ that would ensure this.)

We will also say that $A$ is __nontrivial__ if there exists a nondegenerate element, that is an $x$ such that $x # 0$.


## Group structure

Suppose that $A$ has the structure of a [[group]], which we will write additively (but without assuming commutativity).  We will say that the group structure is _compatible_ with the partial order $\leq$ and the inequality $#$ if

* $x \leq y$ iff $y - x \geq 0$, and
* $x # y$ iff $y - x # 0$.

[more to come]


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
