
#Contents#
* automatic table of contents goes here
{:toc}

## Definition

For a [[category]] $C$ and [[endofunctor]] $F$, a **[[coalgebra]] of** $F$ is an [[object]] $X$ in $C$ and a map $\alpha: X \to F(X)$. (The object $X$ may be called the __carrier__ of the coalgebra)

Given two coalgebras $(x, \eta: x \to F x)$, $(y, \theta: y \to F y)$, a coalgebra map is a [[morphism]] $f: x \to y$ which respects the coalgebra structures: 

$$\theta \circ f = F(f) \circ \eta$$

The dual concept is an [[algebra for an endofunctor]]. Both [[algebras]] and coalgebras for endofunctors on $C$ are special cases of [[algebra for a C-C bimodule|algebras for C-C bimodules]].

See also [[terminal coalgebra]].

## Examples 

### Coalgebras for functors on $Set$

* $X \to F(X) = D(X)$, the set of probability distributions on $X$: Markov chain on $X$.
* $X \to F(X) = P(X)$, the powerset on $X$: Binary relation on $X$.
* $X \to F(X) = X^A \times B$: [[deterministic automaton]].
* $X \to F(X) = P(X^A \times B)$: Nondeterministic automaton.
* $X \to F(X) = A \times X \times X$, for a set of labels $A$: Labelled binary tree.

See [[coalgebra]] for examples on categories of modules.


### The real line as a terminal coalgebra

Let $Pos$ be the category of [[poset]]s. Consider the endofunctor

$$
  F_1 : Pos \to Pos
$$

that acts by [[ordinal product]] with $\omega$

$$
  F_1 : X \mapsto X \cdot \omega
  \,,
$$

where the right side is given the dictionary order, not the usual product order. 

**Proposition**

The terminal coalgebra of $F_1$ is order isomorphic to the non-negative [[real line]] $\mathbb{R}^+$, with its standard order.

**Proof** This is theorem 5.1 in

* D. Pavlovic, [[Vaughan Pratt]], _On coalgebra of real numbers_ ([web](http://citeseerx.ist.psu.edu/viewdoc/summary?doi=10.1.1.47.5204))


**Proposition**

The real interval $[0, 1]$ may be characterized, as a [[topological space]], as the terminal coalgebra for the functor on bi[[pointed object|pointed]] topological spaces which takes a space $X$ to the space $X \vee X$. Here, $X \vee Y$, for $(X, x_-, x_+)$ and $(Y, y_-, y_+)$, is the disjoint union of $X$ and $Y$ with $x_+$ and $y_-$ identified, and $x_-$ and $y_+$ as the two base points.

**Proof**

This is discussed in 

* [[Peter Freyd]], [cat list](http://www.mta.ca/~cat-dist/catlist/1999/realcoalg)



## References

* [[Jiri Adamek]], _[Introduction to coalgebras](http://www.tac.mta.ca/tac/volumes/14/8/14-08abs.html)_ ,
_Theory and Applications of Categories_, Vol. 14 (2005), No. 8, 157-199.

Here are two blog discussions of coalgebra theory:

* [[David Corfield]], _[_Coalgebraically Thinking_](http://golem.ph.utexas.edu/category/2008/11/coalgebraically_thinking.html)_

* [[David Corfield]], _[_The Status of Coalgebra_](http://golem.ph.utexas.edu/category/2008/12/the_status_of_coalgebra.html)_
