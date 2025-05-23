
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Algebra
+--{: .hide}
[[!include algebra - contents]]
=--
=--
=--



#Contents#
* table of contents
{: toc}

## Idea
An element $x$ in a [[ring]] (or potentially even a [[nonassociative algebra|nonassociative]] [[rig]]) $A$ is __nilpotent__ if there exist a natural number $n$ such that $x^n = 0$. 

## Properties

\begin{theorem}
Every [[nilpotent element]] in a [[ring]] is a [[quasiregular element]]. 
\end{theorem}

\begin{proof}
Given a ring $R$ and an element $x \in R$, if $x$ is nilpotent, then one can construct a natural number $n \in \mathbb{N}$ such that $x^{n + 1} = 0$, and

$$(1 - x)(1 + x + x^2 + \ldots + x^n) = 1 \qquad (1 + x + x^2 + \ldots + x^n)(1 - x) = 1$$ 

which means that $x$ is quasiregular. 
\end{proof}

## Nilpotent algebras

An ring/rig/algebra is __nilpotent__ if there exists a uniform number $n$ such that any product of $n$ elements is $0$. An algebra over a [[field]] is __locally nilpotent__ if all of its finitely-generated subalgebras are nilpotent. A [[Lie algebra]] element is __[[ad-nilpotent Lie algebra|ad-nilpotent]]__ if the multiplication with any of its elements is a nilpotent linear operator. A Lie algebra $A$ is __nilpotent__ iff its [[lower central series]] $A, [A,A], [A,[A,A]], \ldots, [A,[A,[A,\ldots,[A,A]\cdots]]], \ldots$ terminates with $0$ after finitely many steps. By Engel's theorem ([English Wikipedia](http://en.wikipedia.org/wiki/Engel_theorem)) a finite-dimensional Lie algebra is nilpotent iff it is locally nilpotent. Thus sometimes locally nilpotent Lie algebras are called __Engel's Lie algebras__. 

The class of locally nilpotent [[associative algebras]] is closed under extensions (defined in the category of associative algebras).  Consequently associative algebras have a largest nilpotent ideal (namely the sum of all locally nilpotent ideals), which is called __Levitskii radical__. 

The structure rings of classical [[algebraic variety|algebraic varieties]] are finitely generated [[noetherian ring|noetherian]] commutative associative unital rings _without nilpotent elements_. One of the principal advantages of Grothendieck's theory of [[schemes]] is to allow for nilpotent elements in [[local rings]]. A scheme is [[reduced scheme|reduced]] if there are no nilpotent elements in stalks of the structure sheaf.

## Related pages

* [[nilpotent group]]

* [[nilpotent topological space]]

* [[nilradical]]

For [[Lie algebras]]:

* [[Jacobson-Morozov theorem]]

[[!redirects nilpotent]]
[[!redirects nilpotent element]]
[[!redirects nilpotent elements]]

[[!redirects nilpotent algebra]]
[[!redirects nilpotent algebras]]
[[!redirects locally nilpotent algebra]]
[[!redirects locally nilpotent algebras]]


[[!redirects Engel's Lie algebra]]
[[!redirects Engel's Lie algebras]]

[[!redirects Levitskii radical]]
[[!redirects Levitskii radicals]]
