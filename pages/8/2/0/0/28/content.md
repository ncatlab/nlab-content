#Definition#

A **groupoid** $G$ is a [[category]] in which all morphisms are [[isomorphism|isomorphisms]]. Usually the requirement is made that $G$ is small. 

A groupoid is **tame** if its [[groupoid cardinality|cardinality]] is finite.

##Notation##

If $x,y$ are objects (also called vertices) of the groupoid then the set of arrows from $x$ to $ y$ is written $G(x,y)$, and $G(x,x)$ is also written $G(x)$ and called the vertex group of $G$ at $x$. It is also written $Aut_G(x)$. 

There is a question of notation for the composition. The most convenient is that the composition of $a:x \to y$ and $b: y \to z$ is written $ab:x \to z$. 

A groupoid $G$ is _connected_, or _transitive_,  if $G(x,y)$ is nonempty for all $x,y \in Ob(G)$. A maximal connected subgroupoid of $G$ is called a component of $G$, and $G$ is then the disjoint union, or coproduct in the category of groupoids, of its connected components. The set of components of $G$ is written $\pi_0(G)$. 

##Examples## 
1. A disjoint union of groups is naturally a groupoid, also called a _bundle of groups_. 

1. An equivalence relation $E$ on a set $X$ becomes a groupoid with the multiplication $(x,y)(y,z)= (x,z)$ 
for all $(x,y), (y,z) \in E$. (This gives a reason for the above notation for composition.) 

1. In particular if $E=X \times X$ then we get the _square groupoid_ $X^2$. This apparently trivial example has an important special case, namely the groupoid $\bf{I}= \{0,1\}^2$. This groupoid has non identity elements $\iota:0 \to 1, \iota^{-1}: 1 \to 0$, and can be regarded as a groupoid model of the unit interval $[0,1]$ in topology. In particular, there is  an isomorphism  $\pi_1([0,1],\{0,1\}) \cong \bf{I}.$

1. If $\Gamma$ is a directed graph, then the free groupoid $F(\Gamma)$ is well defined. It is the left adjoint to the forgetful functor from groupoids to directed graphs. This shows an advantage of groupoids: the notion of _free equivalence relation_ or _free action groupoid_ does not make sense. But we can still talk of a presentation of an equivalence relation or action groupoid by generators and relations by considering presentations of groupoids. 


#See also#
***
* [[action groupoid|Action groupoid]]

##REFERENCES##

* P.J. Higgins,  Presentations of Groupoids, with Applications to Groups, Proc. Camb. Phil. Soc., 60 (1964) 7--20.

* P.J. Higgins, 1971, _Categories and Groupoids_, van
Nostrand, New   York. Reprints in Theory and Applications of
Categories, 7 (2005) pp 1-195.

* P.J. Higgins, The fundamental groupoid of a graph of groups, J. London Math. Soc. (2) 13 (1976) 145--149. 

