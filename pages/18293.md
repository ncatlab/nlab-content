
#Contents#
* table of contents
{:toc}


## Idea

[[arithmetic|Arithmetic]] with [[cardinals]]. A kind of [[transfinite arithmetic]].

### Definition

For $S$ a [[set]], write ${|S|}$ for its [[cardinality]]. Then the standard operations in the [[category]] [[Set]] induce [[arithmetic]] operations on [[cardinal numbers]]:

For $S_1$ and $S_2$ two sets, the **sum** of their cardinalities is the cardinality of their [[disjoint union]], the [[coproduct]] in $Set$:
$$
  {|S_1|} + {|S_2|} \coloneqq {|S_1 \amalg S_2|}
  \,.
$$

More generally, given any family $(S_i)_{i: I}$ of sets indexed by a set $I$, the **sum** of their cardinalities is the cardinality of their disjoint union:
$$
  \sum_{i: I} {|S_i|} \coloneqq {|\coprod_{i: I} S_i|}
  \,.
$$

Likewise, the **product** of their cardinalities is the cardinality of their [[cartesian product]], the [[product]] in $Set$:
$$
  {|S_1|} \, {|S_2|} \coloneqq {|S_1 \times S_2|}
  \,.
$$

More generally again, given any family $(S_i)_{i: I}$ of sets indexed by a set $I$, the **product** of their cardinalities is the cardinality of their cartesian product:
$$
  \prod_{i: I} {|S_i|} \coloneqq {|\prod_{i: I} S_i|}
  \,.
$$

Also, the **exponential** of one cardinality raised to the power of the other is the cardinality of their [[function set]], the [[exponential object]] in $Set$:
$$
  {|S_1|}^{|S_2|} \coloneqq {|Set(S_2,S_1)|}
  \,.
$$

In particular, we have $2^{|S|}$, which (assuming the law of [[excluded middle]]) is the cardinality of the [[power set]] $P(S)$.  In [[constructive mathematics|constructive]] (but not [[predicative mathematics|predicative]]) mathematics, the cardinality of the power set is $\Omega^{|S|}$, where $\Omega$ is the cardinality of the set of [[truth values]].

The usual way to define an ordering on cardinal numbers is that ${|S_1|} \leq {|S_2|}$ if there exists an [[injection]] from $S_1$ to $S_2$:
$$
  ({|S_1|} \leq {|S_2|})
  \;:\Leftrightarrow\;
  (\exists (S_1 \hookrightarrow S_2))
  \,.
$$
Classically, this is almost equivalent to the existence of a [[surjection]] $S_2 \to S_1$, except when $S_1$ is [[empty set|empty]].  Even restricting to [[inhabited sets]], these are not equivalent conditions in [[constructive mathematics]], so one may instead define that ${|S_1|} \leq {|S_2|}$ if there exists a [[subset]] $X$ of $S_2$ and a surjection $X \to S_1$.  Another alternative is to require that $S_1$ (or $X$) be a [[decidable subset]] of $S_2$.  All of these definitions are equivalent using [[excluded middle]].

This order relation is [[antisymmetric relation|antisymmetric]] (and therefore a [[partial order]]) by the [[Cantor–Schroeder–Bernstein theorem]] (proved by Cantor using the [[well-ordering theorem]], then proved by Schroeder and Bernstein without it).  That is, if $S_1 \hookrightarrow S_2$ and $S_2 \hookrightarrow S_1$ exist, then a bijection $S_1 \cong S_2$ exists.  This theorem is not constructively valid, however.

The well-ordered cardinals are [[well-order|well-ordered]] by the ordering $\lt$ on [[ordinal numbers]].  Assuming the [[axiom of choice]], this agrees with the previous order in the sense that $\kappa \leq \lambda$ iff $\kappa \lt \lambda$ or $\kappa = \lambda$.  Another definition is to define that $\kappa \lt \lambda$ if $\kappa^+ \leq \lambda$, using the successor operation below.

The __[[successor]]__ of a well-ordered cardinal $\kappa$ is the smallest well-ordered cardinal larger than $\kappa$.  Note that (except for finite cardinals), this is different from $\kappa$\'s successor as an [[ordinal number]].  We can also take successors of arbitrary cardinals using the operation of [[Hartog's number]], although this won\'t quite have the properties that we want of a successor without the axiom of choice.


## Properties 

* It is traditional to write [[ℵ]]${}_0$ for the first [[infinite cardinal]] (the cardinality of the [[natural numbers]]), $\aleph_1$ for the next (the first uncountable cardinality), and so on.  In this way every cardinal (assuming choice) is labeled $\aleph_\mu$ for a unique [[ordinal number]] $\mu$, with $(\aleph_\mu))^+ = \aleph_{\mu^+}$.

* For every cardinal $\pi$, we have $2^\pi \gt \pi$ (this is sometimes called [[Cantor's theorem]]).  The question of whether $2^{\aleph_0} = \aleph_{1}$ (or more generally whether $2^{\aleph_\mu} = \aleph_{\mu^+}$) is called Cantor's continuum problem; the assertion that this is the case is called the (generalized) [[continuum hypothesis]]. It is known that the continuum hypothesis is undecidable in [[ZFC]]. 

* For every transfinite cardinal $\pi$ we have (using the axiom of choice) $\pi + \pi = \pi$ and $\pi \cdot \pi = \pi$, so addition and multiplication are [[idempotent]].



## References

Lecture notes include

* _Cardinal arithmetic_ ([pdf](https://www.math.ksu.edu/~nagy/real-an/ap-b-card.pdf))