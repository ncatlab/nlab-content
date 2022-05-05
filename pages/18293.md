

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Arithmetic
+--{: .hide}
[[!include arithmetic geometry - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}


## Idea

Cardinal arithmetic is an [[arithmetic]] with [[cardinals]], which generalizes the ordinary [[arithmetic]] of [[natural numbers]] to non-[[finite set|finite numbers]].

The idea is that on [[finite sets]], whose [[cardinalities]] are [[natural numbers]], the usual operations of [[arithmetic]] -- [[addition]], [[multiplication]] and [[exponentiation]] -- are represented on [[finite sets]] by basic operations of [[set theory]], namely forming [[disjoint union]] of sets, forming [[Cartesian product]] of sets and forming [[function sets]] of sets. 

| $\phantom{A}$[[natural numbers]]$\phantom{A}$ | $\phantom{A}$[[finite sets]]$\phantom{A}$ |
|---------------------|-----------------|
| $\phantom{A}$[[addition]]$\phantom{A}$ | $\phantom{A}$[[disjoint union]]$\phantom{A}$ | 
| $\phantom{A}$[[multiplication]]$\phantom{A}$ | $\phantom{A}$[[Cartesian product]]$\phantom{A}$ |
| $\phantom{A}$[[exponentiation]]$\phantom{A}$ | $\phantom{A}$[[function sets]]$\phantom{A}$ | 

(Here passing from the left to the right column is an example of _[[vertical categorification|categorification]]_, while passing from right to left is an example _[[decategorification]]_.)

But the operations on sets on the right directly generalize from [[finite sets]] to general sets, hence from sets whose [[cardinality]] is a [[natural number]] to [[infinite cardinals]]. Therefore cardinal arithmetic is also called a _[[transfinite arithmetic]]_.

## Definitions

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


### Remarks 

* It is traditional to write [[ℵ]]${}_0$ for the first [[infinite cardinal]] (the cardinality of the [[natural numbers]]), $\aleph_1$ for the next (the first uncountable cardinality), and so on.  In this way every cardinal (assuming choice) is labeled $\aleph_\mu$ for a unique [[ordinal number]] $\mu$, with $(\aleph_\mu))^+ = \aleph_{\mu^+}$.

* For every cardinal $\pi$, we have $2^\pi \gt \pi$ (this is sometimes called [[Cantor's theorem]]).  The question of whether $2^{\aleph_0} = \aleph_{1}$ (or more generally whether $2^{\aleph_\mu} = \aleph_{\mu^+}$) is called Cantor's continuum problem; the assertion that this is the case is called the (generalized) [[continuum hypothesis]]. It is known that the continuum hypothesis is undecidable in [[ZFC]]. 

## Properties 

+-- {: .num_theorem} 
###### Theorem 
For every [[infinite cardinal]] $\pi$ we have (using the axiom of choice) $\pi + \pi = \pi$ and $\pi \cdot \pi = \pi$, so addition and multiplication are [[idempotent]]. 
=-- 

+-- {: .proof} 
###### Proof 
Since $\pi \leq \pi + \pi = 2 \cdot \pi \leq \pi \cdot \pi$, it suffices to prove $\pi \cdot \pi \leq \pi$. Establishing this is closely analogous to establishing one of the standard bijections $\mathbb{N} \cong \mathbb{N} \times \mathbb{N}$ -- not the one that enumerates along successive diagonals  $x + y = k$ which are spheres in an $L^1$ [[p-norm|metric]] (and which involves additive structure), but one which enumerates along successive spheres in an $L^\infty$ metric (which involves only order structure). 

With this hint in mind, regard $\pi$ as the least [[ordinal]] in its cardinality class (using the [[well-ordering theorem]]), and suppose $\pi$ is a minimal counterexample to the statement. Thus ${|\alpha|}^2 = {|\alpha|}$ for all ordinals $\alpha \lt \pi$. Consider $\pi^3 = \pi \times \pi \times \pi$ in [[lexicographic order]]. This is a well-ordered set, as is the subset 

$$S = \{(x, y, z) \in \pi^3: x = \max(y, z)\}$$ 

under the order inherited from $\pi^3$. Clearly $S \cong \pi^2$ as sets. Under the supposition ${|\pi|} \lt {|\pi|}^2$, the ordinal $\pi$ is isomorphic to one of the [[lower set|initial segments]] 

$$S(a, b, c) \coloneqq \{(x, y, z) \in S: (x, y, z) \lt (a, b, c)\}$$ 

of $S$, say $S(\alpha, \beta, \gamma)$. But then (regarding $\alpha$ as an ordinal less than $\pi$) 

$${|\pi|} = {|S(\alpha, \beta, \gamma)|} \leq {|S(\alpha, \alpha, \alpha)|} = {|\alpha|}^2 = {|\alpha|} \lt {|\pi|}$$ 

which gives a contradiction. 
=-- 

+-- {: .num_remark} 
###### Remark 
Conversely, if (relative to ZF or any other standard set theory) we assume that any infinite set can be put in bijection with its cartesian square, then every set can be well-ordered, a result originally due to Tarski. Details may be found at [[Hartogs number]]. 
=-- 

+-- {: .num_cor} 
###### Corollary 
If one of two non-zero cardinals $\kappa, \lambda$ is infinite, then 

$$\kappa + \lambda = \kappa \cdot \lambda = \max \{\kappa, \lambda\}.$$ 
=-- 

+-- {: .proof} 
###### Proof 
Clearly, $\kappa \leq \kappa + \lambda$ and $\lambda \leq \kappa + \lambda$, so $\max \{\kappa, \lambda\} \leq \kappa + \lambda$, and similarly for multiplication instead of addition, assuming the cardinals are non-zero. 
Letting $\mu = \max \{\kappa, \lambda\}$, we also have 

$$\kappa \cdot \lambda \leq \mu \cdot \mu = \mu$$ 

and similarly for addition instead of multiplication. 
=-- 

## References

Traditional lecture notes include

* Alexandru Baltag, _Axiomatix set  theory lecture 8: Cardinal arithmetic_ ([pdf](http://www.vub.ac.be/CLWF/SS/Sets8.pdf))

* _Cardinal arithmetic_ ([pdf](https://www.math.ksu.edu/~nagy/real-an/ap-b-card.pdf))

See also 

* Planetmath, _[cardinal arithmetic](http://planetmath.org/cardinalarithmetic)_

The point of view of [[categorification]] is amplified in 

* [[Emily Riehl]], _Categorifying cardinal arithmetic_ ([pdf](http://www.math.jhu.edu/~eriehl/arithmetic.pdf))

