+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Algebra
+-- {: .hide}
[[!include higher algebra - contents]]
=--
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

## Definitions

A __(left/right/two-sided) [[associative]] [[quasigroup]]__ is a (left/right/two-sided) [[quasigroup]] $(G, \cdot,\backslash,/)$ where $a \cdot (b \cdot c) = (a \cdot b) \cdot c$ for all $a$, $b$, and $c$ in $G$. 

In every associative quasigroup $G$, $a/a = b\backslash b$ for every $a$ and $b$ in $G$. This is because for every $a$ and $b$ in $G$, $b \cdot a = b \cdot (a/a) \cdot a = b \cdot (b\backslash b) \cdot a$. Left dividing both sides by $b$ and right dividing both sides by $a$ results in $a/a = b\backslash b$. This means in particular that $a/a = a\backslash a$, which means that every associative quasigroup is a [[possibly empty loop]]. Thus, an associative quasigroup is a associative possibly empty loop, or a __possibly empty group__. In particular, there is an additional definition of an associative quasigroup in terms of the left and right divisions alone, without any semigroup operation at all: 

A __left associative quasigroup__ is a [[set]] $G$ with a binary operation $(-)\backslash(-):G \times G \to G$ (a [[magma]]) such that:

  * For all $a$ and $b$ in $G$, $a\backslash a=b\backslash b$
  * For all $a$ in $G$, $(a\backslash (a\backslash a))\backslash (a\backslash a)=a$
  * For all $a$, $b$, and $c$ in $G$, $(a\backslash b)\backslash c= b\backslash ((a\backslash (a\backslash a))\backslash c)$. 

For any element $a$ in $G$, the element $a\backslash a$ is called a __right identity element__, and the element $a\backslash (a\backslash a)$ is called the __right inverse element__ of $a$. For all elements $a$ and $b$ in $G$, __left multiplication__ of $a$ and $b$ is defined as $(a\backslash (a\backslash a))\backslash b$. 

A __right associative quasigroup__ is a [[set]] $G$ with a binary operation $(-)/(-):G \times G \to G$ such that:

  * For all $a$ and $b$ in $G$, $a/a=b/b$
  * For all $a$ in $G$, $(a/a)/((a/a)/a)=a$
  * for all $a$, $b$, and $c$ in $G$, $a/(b/c)=(a/((c/c)/c)/b$

For any element $a$ in a $G$, the element $a/a$ is called a __left identity element__, and the element $(a/a)/a$ is called the __left inverse element__ of $a$. For all elements $a$ and $b$, __right multiplication__ of $a$ and $b$ is defined as $a/((b/b)/b)$. 

An __associative quasigroup__ is a possibly empty left and right group as defined above such that the following are true:

* left and right identity elements are equal (i.e. $a/a = a \backslash a$) for all $a$ in $G$

* left and right inverse elements are equal (i.e. $(a/a)/a = a\backslash (a\backslash a)$) for all $a$ in $G$

* left and right multiplications are equal (i.e. $a/((b/b)/b) = (a\backslash (a\backslash a))\backslash b$) for all $a$ and $b$ in $G$. 

This definition [first appeared on the heap article](https://ncatlab.org/nlab/revision/diff/heap/13) and is due to [[Toby Bartels]].

## Pseudo-torsors

Every left associative quasigroup $G$ has a [[pseudo-torsor]] $t_G:G^3 \to G$ defined as $t_G(x,y,z) = x \cdot (y \backslash z)$. Every right associative quasigroup $H$ has a [[pseudo-torsor]] $t_H:H^3 \to H$ defined as $t_H(x,y,z) = (x / y) \cdot z$. This means every associative quasigroup has two pseudo-torsors. If the (left or right) associative quasigroup is inhabited, then those pseudo-torsors are actually [[torsors]] or [[heaps]]. 

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

* [[quasigroup]]

* [[commutative quasigroup]]

* [[loop (algebra)|loop]]

* [[group]]

[[!include oidification - table]]

## References

* [The Group With No Elements](https://golem.ph.utexas.edu/category/2020/08/the_group_with_no_elements.html#c059798) at the [n-category café](https://golem.ph.utexas.edu/category/)

[[!redirects possibly empty group]]