
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Topology
+-- {: .hide}
[[!include topology - contents]]
=--
=--
=--


#Contents#
* table of contents
{: toc}

## Statement and proof

[[!include Urysohn metrization theorem - main theorem]]

The **proof** can be divided into three parts. Recall that "second-countable" means having a [[countable set|countable]] [[topological base|base]]. All topological spaces considered here are assumed to be [[T1|$T_1$]] (points are closed), so that "[[regular topological space|regular]]" means "regular [[Hausdorff space|Hausdorff]]". 

1. A [[regular space]] with a [[countable set|countable]] [[topological base|base]] is [[normal space|normal]]. 

1. A normal space $X$ is a [[completely regular space]], i.e., given a point $x \in X$ and an open set $U \subseteq X$ containing $x$, there exists a continuous function $f: X \to [0, 1]$ such that $f(x) = 1$ and $f(y) = 0$ for $y \notin U$. 

1. A completely regular space $X$ with a countable base can be embedded in the [[Hilbert cube]] $[0, 1]^\mathbb{N}$. Since $[0, 1]^\mathbb{N}$ is metrizable, so is $X$. 

The second assertion being proved at [[Urysohn lemma]], we prove the first and third assertions. 

+-- {: .num_prop} 
###### Proposition 
A regular space $X$ with a countable base is normal. 
=-- 

+-- {: .proof} 
###### Proof 
Let $A, B$ be disjoint [[closed sets]] of $X$. The collection of [[open sets]] $U$ such that $U \cap A$ is inhabited and $\widebar{U} \cap B = \emptyset$ is, by regularity, an open covering of $A$. By second-countability, we may index it as $U_1, U_2, \ldots$. Similarly, there is a countable open covering $V_1, V_2, \ldots$ of $B$ such that $\widebar{V_k} \cap A = \emptyset$. 

Now form open sets $Y_n \coloneqq U_n \cap \bigcap_{k=1}^n \neg \widebar{V_k}$ and $Z_n = V_n \cap \bigcap_{k=1}^n \neg \widebar{U_k}$. It is clear that the $Y_n$ cover $A$ and the $Z_n$ cover $B$. Moreover, $Y_m \cap Z_n = \emptyset$ for all $m, n$. For if $m \geq n$ say, then 

$$Y_m \cap Z_n \subseteq Y_m \cap V_n \subseteq Y_m \cap \widebar{V_n} \subseteq U_m \cap \neg \widebar{V_n} \cap \widebar{V_n} = \emptyset.$$ 

It follows that $\bigcup_m Y_m$ and $\bigcup_n Z_n$ are disjoint open sets containing $A$ and $B$, respectively. This completes the proof. 
=-- 

+-- {: .num_prop} 
###### Proposition 
A completely regular space $X$ with countable base can be embedded in $[0, 1]^\mathbb{N}$. 
=-- 

+-- {: .proof} 
###### Proof 
$X$ has a countable base $\mathcal{B}$. The set $S = \{(U, V) \in \mathcal{B} \times \mathcal{B}: \widebar{U} \subseteq V\}$ is countable. For each $s = (U, V) \in S$ there is by the Urysohn lemma a continuous map $g_s: X \to [0, 1]$ such that $g_s$ is identically $1$ on $\widebar{U}$ and identically $0$ on $\neg V$. The map 

$$g: X \to [0,1]^S: x \mapsto (s \mapsto g_s(x))$$ 

is a continuous injection, since if $x \neq y$, we can find a pair $s = (U, V) \in S$ with $x \in U$ and $y \notin V$, so that $g_s(x) = 1$ differs from $g_s(y) = 0$, whence $g(x) \neq g(y)$. The subspace topology on $X$ induced from the monomorphism $g$ is contained in the given topology of $X$, simply by continuity of $g$. On the other hand, if $W$ is an open neighborhood of $x$ in $X$, there exists a smaller open neighborhood $V \in \mathcal{B}$ and $s  = (U, V) \in S$ such that $g_s(x) = 1$ and $g_s$ is identically $0$ outside $V$. Provided that $g_s(x) - g_s(y) \lt 1$, we see $g_s(y) \neq 0$, so $y \in V$. In other words, letting $\pi_s: [0, 1]^S \to [0, 1]$ be the evident projection, we have $g_s = \pi_s \circ g$, so that the inverse image under $g$ of the subbase element $\pi_s^{-1}((0, 1])$ is $g_s^{-1}((0, 1]) \subseteq V \subseteq W$. This shows that the subspace topology induced by $g$ contains the topology of $X$. It follows that $g: X \to [0, 1]^S \cong [0, 1]^\mathbb{N}$ is an embedding into the [[Hilbert cube]]. 
=-- 

## Related theorems

* [[metrization theorem]]
* [[Nagata-Smirnov metrization theorem]]

## Related concepts

* [[topological space]]

* [[metrisable topological space]]

* [[second-countable space]]


## References

Named after [[Pavel Urysohn]].

Textbook accounts:

* {#Kelley55} [[John Kelley]], Ch. 4, Th. 16 in: *General topology*, D. van Nostrand, New York (1955), reprinted as: Graduate Texts in Mathematics, Springer (1975) &lbrack;[ISBN:978-0-387-90125-1](https://www.springer.com/gp/book/9780387901251)&rbrack;

* {#Munkres75} [[James Munkres]], Ch. 4, Thm 34.1 _Topology_, Prentice Hall (1975, 2000) &lbrack;ISBN:0-13-181629-2, [pdf](http://mathcenter.spb.ru/nikaan/2019/topology/4.pdf)&rbrack;

* [[Richard E. Hodel]], *The Alexandroff-Urysohn metrization theorem revisited*, in: *Set-Theoretic Topology*, Academic Press (1977) 239-253 &lbrack;[doi:10.1016/B978-0-12-584950-0.50021-3](https://doi.org/10.1016/B978-0-12-584950-0.50021-3)

See also:

* ProofWiki, *[Urysohn's_Metrization_Theorem](https://proofwiki.org/wiki/Urysohn%27s_Metrization_Theorem)*





