For a category $C$ and endofunctor $F$, a **coalgebra of** $F$ is an object $X$ in $C$ and a map $\alpha: X \to F(X)$.

Given two coalgebras $(x, \eta: x \to F x)$, $(y, \theta: y \to F y)$, a coalgebra map is a morphism $f: x \to y$ which respects the coalgebra structures: 

$$\theta \circ f = F(f) \circ \eta$$

The dual concept is an [[algebra for an endofunctor]].

See also [[terminal coalgebra]].

#Blog resources#

David Corfield, [_Coalgebraically Thinking_](http://golem.ph.utexas.edu/category/2008/11/coalgebraically_thinking.html)

David Corfield, [_The Status of Coalgebra_](http://golem.ph.utexas.edu/category/2008/12/the_status_of_coalgebra.html)

#References#

Jiri Adamek, [Introduction to coalgebras](http://www.tac.mta.ca/tac/volumes/14/8/14-08abs.html),
_Theory and Applications of Categories_, Vol. 14 (2005), No. 8, 157-199.