
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Category theory
+--{: .hide}
[[!include category theory - contents]]
=--
=--
=--

* **groupoid**

* [[2-groupoid]]

* [[3-groupoid]]

* [[∞-groupoid]]


***

#Contents#
* table of contents
{:toc}

## Definition

A **groupoid** $G$ is a [[category]] in which all morphisms are [[isomorphism|isomorphisms]].  Often the requirement is made that $G$ is [[small category|small]].

A groupoid is **tame** if its [[groupoid cardinality|cardinality]] is finite.

Groupoids form a $2$-[[2-category|category]] (in fact a $(2,1)$-category) [[Grpd]].

## Notation

If $x,y$ are objects (also called vertices) of the groupoid $G$ then the set of morphisms (also called arrows) from $x$ to $y$ is written $G(x,y)$.  The set $G(x,x)$ (which is a [[group]] under composition) is also written $G(x)$ and called the _vertex group_ of $G$ at $x$.  It is also written $Aut_G(x)$ and called the [[automorphism group]] of $x$ in $G$, or written $\pi_1(G,x)$ and called the [[fundamental group]] of $G$ at $x$ (especially if you think of a groupoid as giving a [[homotopy 1-type]]).

As in any category, there is a question of notation for the composition, and in particular of the order in which to write things. It can be more convenient to write the composition of $a:x \to y$ and $b: y \to z$ as $a b:x \to z$, although a more traditional notation would be $b a$.  The two conventions can be distinguished by writing $a; b$ or $b\circ a$ (which is the most traditional notation for categories).

A groupoid $G$ is _connected_, or _transitive_,  if $G(x,y)$ is nonempty for all $x,y \in Ob(G)$; it is called _inhabited_, or _nonempty_, if it has at least one object. A maximal inhabited connected subgroupoid of $G$ is called a _component_ of $G$, and $G$ is then the [[disjoint union]] (the [[coproduct]] in $\Grpd$), of its connected components. The set of components of $G$ is written $\Pi_0(G)$. 

## Examples

1. Any [[group]] $H$ gives rise to a groupoid, sometimes denoted $\mathbf{B}H$ but often conflated with $H$ itself, which has exactly one object $*$ and with $\mathbf{B}H(*,*) = H$.  Any inhabited connected groupoid is [[equivalence of categories|equivalent]] to one arising in this way.

1. A disjoint union of (the one-object groupoids corresponding to) groups is naturally a groupoid, also called a _bundle of groups_.  The [[axiom of choice]] is equivalent to the claim that any groupoid is equivalent to one of this form.

1. From any [[action]] of a [[group]] $H$ on a [[set]] $X$ we obtain an [[action groupoid]] or "[[weak quotient]]" $X//H$.  If $X=\{*\}$ this gives the groupoid $\mathbf{B}H$, above.

1. A setoid, that is a set $X$ equipped with an [[equivalence relation]] $E$, becomes a groupoid with the multiplication $(x,y);(y,z) = (x,z)$ for all $(x,y), (y,z) \in E$.  (This gives one reason for the forward notation for composition.)  Such a groupoid is equivalent to the [[discrete category]] on the [[quotient set]] $X/E$.

1. In particular, if $E$ is the universal relation $X \times X$, then we get the _square groupoid_ $X^2$, also called the _trivial groupoid_ on $X$. Despite the latter name, there is an important special case, namely the groupoid $I= \{0,1\}^2$. This groupoid has non-identity elements $\iota:0 \to 1, \iota^{-1}: 1 \to 0$, and can be regarded as a groupoid model of the unit [[interval]] $[0,1]$ in topology.

1. Any [[topological space]] $X$ has a [[fundamental groupoid]] $\Pi_1(X)$ whose objects are the points of $X$ and whose arrows are homotopy classes of paths, with composition by concatenation of paths.  Note that $\Pi_0(\Pi_1(X)) = \Pi_0(X)$ is the set of [[path component|path components]] of $X$, and for any $x\in X$, $\pi_1(\Pi_1(X),x) = \pi_1(X,x)$ is the [[fundamental group]] of $X$ with basepoint $x$.  In theory one can obtain the higher [[homotopy group]]s in this way as well by generalizing from the fundamental groupoid to the [[fundamental infinity-groupoid]].

1. More generally, if we choose some subset $S$, of the points of a space $X$, then we have a [[full subcategory|full subgroupoid]] of $\Pi_1(X)$ containing only those points in $S$, denoted $\Pi_1(X,S)$.  This can result in much more manageable groupoids; for instance $\Pi_1([0,1],\{0,1\}) $ is the groupoid $I$ considered above, while $\Pi_1([0,1])$ has uncountably many objects (but is equivalent to $I$).

1. If $\Gamma$ is a [[directed graph]], then the free groupoid $F(\Gamma)$ is well defined. It is the left [[adjoint functor]] to the [[forgetful functor]] from groupoids to directed graphs. This shows an advantage of groupoids: the notion of _free equivalence relation_ or _free action groupoid_ does not make sense. But we can still talk of a presentation of an equivalence relation or action groupoid by generators and relations, by considering presentations of groupoids instead. 

+--{: .query}
[[Mike Shulman|Mike]]: It's not clear to me that the notion of "free equivalence relation" doesn't make sense.  Can't I talk about a left adjoint to the forgetful functor from equivalence relations to, say, directed graphs?  Maybe sets-equipped-with-a-binary-relation would be more appropriate, but either one works fine.

[[Ronnie Brown|Ronnie]]: Are you sure this forgetful functor equivalence relations to directed graphs has a left adjoint? Suppose the directed graph $\Gamma$ has one vertex $x$ and one loop $u:x  \to x$. The free groupoid on $\Gamma$ is the group of integers, which as a groupoid is not an equivalence relation. 

_Toby_:  But there is still a free [[setoid]] (set equipped with an equivalence relation) on $\Gamma$; it is the [[point]].  As a groupoid, it is not the same as the free groupoid on $\Gamma$, although it *is* the same as the free setoid on the free groupoid on $\Gamma$.  If there\'s an advantage to working with groupoids, perhaps it\'s that the free groupoid functor preserves distinctions that the free setoid functor forgets?  (In this case, a distinction preserved or forgotten is that between $\Gamma$ and the point, which as a graph does not have $u$.)
=--


## References

* P.J. Higgins,  Presentations of Groupoids, with Applications to Groups, Proc. Camb. Phil. Soc., 60 (1964) 7--20.

* P.J. Higgins, 1971, _Categories and Groupoids_, van
Nostrand, New   York. Reprints in Theory and Applications of
Categories, 7 (2005) pp 1--195.

* P.J. Higgins, The fundamental groupoid of a graph of groups, J. London Math. Soc. (2) 13 (1976) 145--149. 

* R. Brown, _Topology and groupoids_, Booksurge, 2006. 


[[!redirects groupoids]]
[[!redirects tame groupoid]]
[[!redirects tame groupoids]]