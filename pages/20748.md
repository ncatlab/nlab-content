+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Measure and probability theory
+-- {: .hide}
[[!include measure theory - contents]]
=--
#### $(0,1)$-Category theory
+--{: .hide}
[[!include (0,1)-category theory - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

The stochastic order is [[partial order]] or [[preorder]] between [[probability measures]] or [[continuous valuations|valuations]] over an ordered space, which compares them in terms of "how higher up in the order the mass is". 


## Definition

Let $X$ be a [[topological space]] equipped with a [[preorder]] relation, and let $p$ and $q$ be [[Borel measures]] or [[continuous valuations|valuations]] on $X$. We say that $p \le q$ in the **stochastic order** if and only if for every [[upper set|upper]] [[open set]] $U\subseteq X$, we have that $p(U)\le q(U)$. 

Note that, if one does not require the measures to be normalized, one has for example $p\le 2p$ whenever the measure $p$ is non-signed. 
However, usually one is interested in comparing [[probability measures]] (or normalized [[valuation (measure theory)|valuations]]). In this case, assigning a higher mass to upper sets can be indeed interpreted as "having the mass placed at higher places".

Often one does not start with both an order and a topology on $X$, but obtains one structure from the other. If one starts with a [[partial order]] or a [[preorder]], one can take either the [[Alexandrov topology]] or the [[Scott topology]]:

 * In the former case, we say that $p\le q$ if and only if $p(U)\le q(U)$ for every [[upper set]] $U$. 
 
 * In the latter case, we say that $p\le q$ if and only if $p(U)\le q(U)$ for every [[Scott-open]] set $U$, i.e. [[upper set|upper]] and inaccessible by [[directed suprema]]. This is how one construct the [[probabilistic powerdomain]].

If one starts with a [[topological space]], one can take as preorder the [[specialization preorder]] relative to the given topology. This way, we say that $p\le q$ if and only if $p(U)\le q(U)$ for every [[open set]] $U$.
Equivalently, this is the [[pointwise order]] of [[valuations]] as functions on the frame of open sets.
This is how one constructs the [[extended probabilistic powerdomain]].

### For random variables

The stochastic order can be extended from probability measures to [[random variables]] by comparing their [[image measures|laws]]. 

Let $X$ be an ordered topological space, and let $f,g:\Omega\to X$ be [[random elements]] with values in $X$ on the [[probability space]] $(\Omega,\mu)$.
We say that $f\le g$ in the **stochastic order** if and only if $f_*\mu\le g_*\mu$ in the stochastic order of measures defined above. 

In decision theory, economics and related fields, this order is also known as **first-order stochastic dominance**, especially on the real line.


## As a 2-functor

Categories of [[preorders]] (possibly with extra [[structure]]) and monotone maps (possibly preserving the extra structure) can be canonically equipped with the structure of a [[locally posetal 2-category]]. 
Explicitly this is given by the [[pointwise order]]: given preorders $X$ and $Y$ and [[monotone maps]] $f,g:X\to Y$, we say that $f\le g$, or we draw a 2-cell $f\Rightarrow g$, if and only if for every $x\in X$, $f(x)\le g(x)$. 

The stochastic order can be seen as a way to turn a [[probability monad]] on a category of preorders into a [[2-monad]] by equipping it with an action on the 2-cells. 
In particular, let $P$ be a [[probability monad]] on a category of preorders. In order to make it a [[2-functor]], and so a [[2-monad]], we want to say that if $f,g:X\to Y$ are such that $f\le g$, then also $P f\le P g$ as maps $P X\to P Y$. The latter condition means that for all $p\in P X$, $(P f)(p) \le (P g)(p)$ in $P Y$, so we need a preorder relation on $P Y$ that is suitably compatible with the order on $Y$, in such a way that $P$ preserves these 2-cells (inequalities). The stochastic order is the canonical choice of such a preorder.

One can actually _define_ the stochastic order directly in terms of 2-cells as follows: given $f,g:X\to Y$ as above, $P f\le P g$ _if and only if_ $f\le g$.

Similarly, the stochastic order can be seen as a way of making the functor $P$ [[enriched functor|enriched]] in [[truth values]].


## See also
 
* [[monads of probability, measures, and valuations]]
* [[probabilistic powerdomain]], [[extended probabilistic powerdomain]]
* [[valuation (measure theory)]]


## References

* {#orderedkantorovich} [[Tobias Fritz]] and [[Paolo Perrone]], _Stochastic order on metric spaces and the ordered Kantorovich monad_, Advances in Mathematics 366, 2020. ([arXiv:1808.09898](https://arxiv.org/abs/1808.09898))

(...)

[[!redirects stochastic ordering]]
[[!redirects usual stochastic ordering]]
[[!redirects usual stochastic order]]
[[!redirects stochastic preordering]]
[[!redirects stochastic preorder]]
[[!redirects usual stochastic preordering]]
[[!redirects usual stochastic preorder]]