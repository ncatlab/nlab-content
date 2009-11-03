For a category $C$ and endofunctor $F$, a **coalgebra of** $F$ is an object $X$ in $C$ and a map $\alpha: X \to F(X)$.

Given two coalgebras $(x, \eta: x \to F x)$, $(y, \theta: y \to F y)$, a coalgebra map is a morphism $f: x \to y$ which respects the coalgebra structures: 

$$\theta \circ f = F(f) \circ \eta$$

The dual concept is an [[algebra for an endofunctor]].

See also [[terminal coalgebra]].

##Examples of coalgebras for functors on [[Set]]:

* $X \to F(X) = D(X)$, the set of probability distributions on $X$: Markov chain on $X$.
* $X \to F(X) = P(X)$, the powerset on $X$: Binary relation on $X$.
* $X \to F(X) = X^A \times B$: Deterministic automaton.
* $X \to F(X) = P(X^A \times B)$: Nondeterministic automaton.
* $X \to F(X) = A \times X \times X$, for a set of labels $A$: Labelled binary tree.

See [[coalgebra]] for examples on categories of modules.

#Blog resources#

David Corfield, [_Coalgebraically Thinking_](http://golem.ph.utexas.edu/category/2008/11/coalgebraically_thinking.html)

David Corfield, [_The Status of Coalgebra_](http://golem.ph.utexas.edu/category/2008/12/the_status_of_coalgebra.html)

#References#

Jiri Adamek, [Introduction to coalgebras](http://www.tac.mta.ca/tac/volumes/14/8/14-08abs.html),
_Theory and Applications of Categories_, Vol. 14 (2005), No. 8, 157-199.