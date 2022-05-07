

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Group Theory
+-- {: .hide}
[[!include group theory - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Definition

An [[action]]

$$
  (-)\cdot(-) 
  \;\colon\;
  G \times X \to X
$$

of a [[group]] $G$ on a [[set]] $X$ is called _transitive_ if it has a single [[orbit]], i.e. for any two elements, $x, y \in X$, there exists $g\in G$ such that $y = g \cdot x$. 

This is equivalent to saying that the [[shear map]]

$$
  \array{
    G \times X
    &
    \overset
      { (pr_2, \cdot) }
      {\longrightarrow}&
    X \times X
    \\
    (g, x) 
    &
    \mapsto
    & 
    \big( x, g \cdot x \big)
    \,.
  }
$$

is in [[epimorphism]]. In this form the definition makes sense for [[action objects]] [[internalization|internal]] to any ambient [[category]] with [[finite products]].

Beware that often it is assumed that the underlying [[object]] $X$ of a transitive action is [[inhabited]] (but not always, see at *[[pseudo-torsor]]).



For $k\ge 0$, an action $G \times X \to X$ is said to be **$k$-transitive** if the componentwise-action $G \times X^{\underline{k}} \to X^{\underline{k}}$ is transitive, where $X^{\underline{k}}$ denotes the set of tuples of $k$ distinct points (i.e., [[injective functions]] from $\{1,\dots,k\}$ to $X$).  For instance, an action of $G$ on $X$ is 3-transitive if any pair of triples $(a_1,a_2,a_3)$ and $(b_1,b_2,b_3)$ of points in $X$, where $a_i \ne a_j$ and $b_i \ne b_j$ for $i\ne j$, there exists $g \in G$ such that $(b_1,b_2,b_3) = (g a_1,g a_2,g a_3)$.

A transitive action that is also [[free action|free]] is called _[[regular action|regular]]_ action. See also at _[[torsor]]_.

## Properties

A set equipped with a transitive action of $G$ (and which is [[inhabited]]) is the same thing as a [[connected object]] in the category of [[G-sets]]. A $G$-set may be decomposed uniquely as a coproduct of transitive $G$-sets.

## Examples

* Any group $G$ acts transitively on itself by multiplication $\cdot : G \times G \to G$, which is called the (left) [[regular representation]] of $G$.

* The [[alternating group]] $A_n$ acts transitively on $\{1,\dots,n\}$ for $n \gt 2$, and in fact it acts $(n-2)$-transitively for all $n \ge 2$.

* The [[modular group]] $PSL(2,\mathbb{Z})$ acts transitively on the [[rational number|rational]] [[projective line]] $\mathbb{P}^1(\mathbb{Q}) = \mathbb{Q} \cup \{\infty\}$. The [[projective general linear group]] $PGL(2,\mathbb{C})$ acts 3-transitively on the [[Riemann sphere]] $\mathbb{P}^1(\mathbb{C})$.

* An action of $\mathbb{Z}$ (viewed as the [[free group]] on one generator) on a set $X$ corresponds to an arbitrary [[permutation]] $\pi : X \to X$, but the action is transitive just in case $\pi$ is a _cyclic_ permutation.

## As an action on cosets

Let $* : G \times X \to X$ be a transitive action and suppose that $X$ is [[inhabited]].  Then $*$ is equivalent to the action of $G$ by multiplication on a [[coset]] space $G/H$, where the subgroup $H$ is taken as the [[stabilizer subgroup]]
$$H = G_x = \{ g \in G \mid g * x = x \}$$
of some arbitrary element $x \in X$.  In particular, the transitivity of $*$ guarantees that the $G$-equivariant map $G/H \to X$ defined by $g H \mapsto g * x$ is a bijection.  (Note that although the subgroup $H = G_x$ depends on the choice of $x$, it is determined up to conjugacy, and so the coset space $G/H$ is independent of the choice of element.)

## Related concepts

* [[combinatorial map]]

* [[homogeneous space]]

* [[torsor]]

* [[transitive action]], [[free action]], [[semi-free action]], [[regular action]]

* [[proper action]], [[properly discontinuous action]]

## References

* Helmut Wielandt.  _Finite Permutation Groups_.  Academic Press, 1964.

* [Fundamental theorem of group actions](http://groupprops.subwiki.org/wiki/Fundamental_theorem_of_group_actions) on the Group Properties Wiki.

[[!redirects transitive actions]]

[[!redirects transitive]]