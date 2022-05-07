+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Group Theory
+-- {: .hide}
[[!include group theory - contents]]
=--
#### Representation theory
+-- {: .hide}
[[!include representation theory - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Definition

A __left associative [[quasigroup]]__ is a [[semigroup]] $(G, \cdot)$ equipped with a __left division__ $(-)\backslash(-):G \times G \to G$  such that $x \cdot (x \backslash y) = y$ and $x \backslash (x \cdot y) = y$. A __right associative [[quasigroup]]__ is a [[semigroup]] $(G, (-)\cdot(-):G \times G \to G)$ equipped with a __right division__ $(-)/(-):G \times G \to G$ such that $(x / y) \cdot y = x$ and $(x \cdot y) / y = x$. A __two-sided associative [[quasigroup]]__ or just an __associative quasigroup__ is a semigroup that is both a left associative quasigroup and a right associative quasigroup. 

## Pseudo-torsors

Every left associative quasigroup $G$ has a [[pseudo-torsor]] $t_G:G^3 \to G$ defined as $t_G(x,y,z) = x \cdot (y \backslash z)$. Every right associative quasigroup $H$ has a [[pseudo-torsor]] $t_H:H^3 \to H$ defined as $t_H(x,y,z) = (x / y) \cdot z$. This means every associative quasigroup has two pseudo-torsors. If the (left or right) associative quasigroup is inhabited, then those pseudo-torsors are actually [[torsors]]. 

## Category of associative quasigroups

An __associative quasigroup homomorphism__ is a [[semigroup homomorphism]] between associative quasigroups that preserves left and right quotients. Associative quasigroup homomorphisms are the [[morphisms]] in the [[category]] of associative quasigroups $AssocQuasiGrp$. 

As the category of associative quasigroups is a concrete category, there is a [[forgetful functor]] $U:AssocQuasiGrp \to Set$. $U$ has a [[left adjoint]], the __free associative quasigroup__ [[free functor|functor]] $F:Set \to AssocQuasiGrp$. 

The __empty associative quasigroup__ $0$ whose underlying set is the [[empty set]] is the [[initial object|initial associative quasigroup]], and is [[strict initial object|strictly initial]]. The __trivial associative quasigroup__ $1$ whose underlying set is the [[singleton]] is the [[terminal object|terminal associative quasigroup]]. 

The __direct product__ $G \times H$ of associative quasigroups $G$ and $H$ is the [[cartesian product]] of sets $U(G) \times U(H)$ with an associative quasigroup structure defined componentwise by

$$
  (g_1, h_1) \cdot_{G \times H} (g_2, h_2) = (g_1 \cdot_G g_2, h_1 \cdot_H h_2)
$$

$$
  (g_1, h_1) /_{G \times H} (g_2, h_2) = (g_1 /_G g_2, h_1 /_H h_2)
$$

$$
  (g_1, h_1) \backslash_{G \times H} (g_2, h_2) = (g_1 \backslash_G g_2, h_1 \backslash_H h_2)
$$

for all $(g_1, h_1), (g_2, h_2) \in U(G) \times U(H)$, with [[product projections]] $p_G: G \times H \to G$ $p_H: G \times H \to H$ where $p_G(g, h) = g$ and $p_H(g,h) = h$ for all $(g,h)\in G \times H$ The direct product of associative quasigroups is thus the [[cartesian product]] in $AssocQuasiGrp$. The [[endofunctor]] $P(G) = G \times 1$ is the [[identity functor]] on $AssocQuasiGrp$ while the endofunctor $P(G) = G \times 0$ is a [[constant functor]] that sends every associative quasigroup to $0$. 

An __associative subquasigroup__ of an associative quasigroup $G$ is an associative quasigroup $H$ with an associative quasigroup [[monomorphism]] 
$$
  H \hookrightarrow G
  \,.
$$
The empty associative is the initial associative subquasigroup of $G$. 

Let $G$ and $H$ be associative quasigroups and let $f:G \to H$ be an associative quasigroup homomorphism. Then given an element $h \in H$, there is an associative subquasigroup 
$$
  i: I \hookrightarrow G
  \,.
$$
such that $g \in I$ if and only if $f(g) = h$. $I$ is called the __[[fiber]]__ of $f$ over $h$. 

Because $AssocQuasiGrp$ has a terminal object, cartesian products, and fibers, it is a [[finitely complete category]]. 

Every associative quasigroup $G$ and associative subquasigroup $H \hookrightarrow G$ has a __set of left [[ideal in a semigroup|ideals]]__ $G H$ in $G$ and a __set of right ideals__ $H G$ in $G$. 

## Examples

* Every [[group]] is an associative quasigroup. 

* The empty associative quasigroup is an associative quasigroup that is not a group. 

## Related concepts

* [[commutative quasigroup]]

* [[inverse semigroup]]