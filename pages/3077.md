
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Topology
+--{: .hide}
[[!include topology - contents]]
=--
=--
=--

# Contents 
* table of contents 
{: toc}

## Idea 

The ordinary "[[line]]" $\mathbb{R}$ (i.e. the [[real numbers]] equipped with their [[Euclidean space|Euclidean]] [[metric topology]]) may be thought of as the result of gluing a [[countable set]]  of copies of the [[half-open interval]] $[0, 1)$ end-to-end in both directions. A _long line_ is similarly obtained by gluing an _[[uncountable set]]_ of copies of $[0, 1)$ end-to-end in both directions, and is demonstrably "longer" than an ordinary line on account of a number of peculiar properties. 

The long line is a source of many counterexamples in [[topology]]. 


## Definition  

+-- {: .num_defn} 
###### Definition

Let $\omega_1$ be the [[first uncountable ordinal]], and consider the [[half-open interval]] $[0, 1)$ as an [[total order|totally ordered set]]. A **long ray** is the ordered set $\omega_1 \times [0, 1)$ taken in the [[lexicographic order]]; as a [[topological space|space]], it is given the [[order topology]]. The **long line** is the space obtained by gluing two long rays together at their initial points.

=-- 

The long line is a line in the sense of being a $1$-dimensional [[locally Euclidean space]] (without boundary) that is not closed (so not a [[circle]]).  However, it is not [[paracompact space|paracompact]], so it is not [[homeomorphic]] to the [[real line]] (even though it is [[Hausdorff space|Hausdorff]]).


## Properties 

All the assertions below apply to both the long line and the long ray. We write $L$ to cover both cases even if we only treat one. 

1. Every [[continuous function]] $f\colon L \to \mathbb{R}$ is eventually constant, i.e., there exists $x \in L$ and $c \in \mathbb{R}$ such that $f(y) = c$ whenever $y \geq x$ (and similarly $f$ is constant for all sufficiently small $x$). 

2. $L$ is a [[normal space|normal]] ($T_4$) space, but the [[Tychonoff product]] $L \times \bar{L}$ with its one-point [[compactification]] is not normal. (See for example [Munkres](#Munk).) 

3. Every continuous map $L \to L$ has a [[fixed point]]. 

4. $L$ is [[sequentially compact space|sequentially compact]] but not [[compact space|compact]]. (Being sequentially compact, they are also [[countably compact spaces]].) Thus, the image $f(L)$ under a continuous map $f: L \to \mathbb{R}$, being sequentially compact, is a compact subspace of $\mathbb{R}$. 

5. The long ray/line is not [[contractible space|contractible]]. Proof sketch for the long ray, with bottom lement denoted $\bot$: Suppose $H \colon I \times L \to L$ is a homotopy such that $H(0, -)$ is constant and $H(1, -)$ is the identity. For each $t \in [0, 1]$ the image $\im H(t, -)$ is an interval (either bounded or unbounded), since $L$ is [[connected space|connected]]. One may show the set 
$$S = \{t \in I: \im H(t, -)\;  \text{is bounded}\}$$ 
is both closed and open. It also contains $0$, hence is all of $I$. But $S$ can't contain $t = 1$, contradiction. 

Let us flesh out this sketched proof. First we show $S$ is closed. If $t_n$ is a sequence in $S$ with limit point $t \in I$, then $H(\{t_n\} \times L) \subseteq [\bot, b_n]$ for some sequence of bounds $b_n \in L$; this sequence has an upper bound $b \in L$. Then $H(\{t_n\} \times L) \subseteq [\bot, b]$ for all $n \in \mathbb{N}$, which is the same as saying $\bigcup_n \{t_n\} \times L \subseteq H^{-1}([\bot, b])$. Now $\{t\} \times L$ is included within the closure of the union, which is included within the closed set $H^{-1}([\bot, b])$. But $\{t\} \times L \subseteq H^{-1}([\bot, b])$ means $H(\{t\} \times L) \subseteq [\bot, b]$; hence $t \in S$. 

Now we show $S$ is open. This uses a [[countably compact space|countably compact]] version of the [[tube lemma]]. If $t \in S$, then we can find $b \in L$ such that $\{t\} \times L \subseteq H^{-1}([\bot, b))$, where the right side is open in $I \times L$. Let $B_r(t) \subseteq I$ denote the [[ball]] of radius $r$ about $t$, and for $c \lt d$ in $L$ let $(c, d)$ denote the open interval between $c$ and $d$. Consider the collection $T$ of all triples $(n, c, d) \in \mathbb{N} \times L \times L$ such that 

$$U_{n, c, d} \coloneqq B_{1/n}(t) \times (c, d) \subseteq H^{-1}([\bot, b)).$$ 

For each fixed $n \in \mathbb{N}$, put $U_n = \bigcup_{(n, c, d) \in T} (c, d)$. The $U_n$ form a countable [[open cover]] of $L$, since for every $x \in L$ there is a $U_{n, c, d}$ containing the pair $(t, x)$. Since $L$ is countably compact, there is a finite subcover $U_{n_1}, \ldots, U_{n_k}$. Putting $n = \max \{n_1, \ldots, n_k\}$, we see 

$$B_{1/n}(t) \times L = B_{1/n}(t) \times \bigcup_{i=1}^k U_{n_i} = \bigcup_{i=1}^k B_{1/n}(t) \times U_{n_i} \subseteq \bigcup_{i=1}^k B_{1/n_i}(t) \times U_{n_i} \subseteq H^{-1}([\bot, b))$$ 

from which it immediately follows that $B_{1/n}(t) \subseteq S$. 


## Related concepts

* [[line with two origins]]

## References 

* Steen and Seebach, _Counterexamples in Topology_. Springer-Verlag, New York, 1978. Reprinted by Dover Publications, New York, 1995. 

* [[James Munkres]], _Topology_ (2nd edition). Prentice-Hall, 2000. 

See also

* Wikipedia, _[Long line (topology)](https://en.wikipedia.org/wiki/Long_line_%28topology%29)_


[[!redirects long line]]
[[!redirects long lines]]
[[!redirects long ray]]
[[!redirects long rays]]