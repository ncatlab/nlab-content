
> This entry is about the family of binary relations indexed by the positive rational numbers defined by Auke Booij in [Analysis in univalent type theory](https://etheses.bham.ac.uk/id/eprint/10411/7/Booij2020PhD.pdf). For the family of binary relations indexed by the non-negative rational numbers defined by Fred Richman in [Real numbers and other completions](http://math.fau.edu/richman/docs/RealNums.pdf), see [[Richman premetric space]]. 

***

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Analysis
+-- {: .hide}
[[!include analysis - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea ##

A more general concept of [[metric space]] by Auke Booij. While Auke Booij simply called these structures "[[premetric spaces]]", there are multiple notions of premetric spaces in the mathematical literature, so we shall refer to these as Booij premetric spaces. 

## Definition ##

A __Booij premetric space__ is a [[set]] $S$ with a ternary [[relation]] $a \sim_\epsilon b$ for $a \in S$, $b \in S$, and $\epsilon \in \mathbb{Q}_+$, where $\mathbb{Q}_+$ represent the positive [[rational numbers]] in $\mathbb{Q}$. 

Booij premetric spaces are used as in the construction of the [[Cauchy real numbers]] and the [[HoTT book real numbers]]. 

### Uniform Booij premetric spaces

A Booij premetric space is [[uniform space|uniform]] if

1. for every positive rational number $\epsilon \in \mathbb{Q}_+$ and $a \in S$, $a \sim_\epsilon a$

2. for every positive rational number $\epsilon \in \mathbb{Q}_+$, there exists a positive rational number $\delta \in \mathbb{Q}_+$ such that for every $a \in S$, $b \in S$, and $c \in S$, if $a \sim_\epsilon b$ and $b \sim_\epsilon c$, then $a \sim_\delta c$. 

3. For every positive rational number $\epsilon \in \mathbb{Q}_+$, there exists a positive rational number $\delta \in \mathbb{Q}_+$ such that for every $a \in S$ and $b \in S$, if $a \sim_\epsilon b$, then $b \sim_\delta a$. 

4. There is a positive rational number $\epsilon \in \mathbb{Q}_+$ and elements $a \in S$ and $b \in S$ such that $a \sim_\epsilon b$. 

5. If there are positive rational numbers $\epsilon \in \mathbb{Q}_+$ and $\delta \in \mathbb{Q}_+$, then there is a positive rational number $\eta \in \mathbb{Q}_+$ such that for every element $a \in S$ and $b \in S$, if $a \sim_\eta b$, then $a \sim_\epsilon b$ and $a \sim_\delta b$. 

6. If there is a positive rational number $\epsilon \in \mathbb{Q}_+$, then there is a positive rational number $\delta \in \mathbb{Q}_+$ such that for all $a \in S$ and $b \in S$, if $a \sim_\epsilon b$, then $a \sim_\delta b$. 

## Generalizations

Booij premetric spaces could be generalized from the positive rational numbers $\mathbb{Q}_+$ to any set $T$. The binary relation $\sim_U$ for each element $U \in T$ is called an **[[entourage]]**. These are called **$T$-premetric spaces** and are sets $S$ with a ternary [[relation]] $a \sim_U b$ for $a \in S$, $b \in S$, and $U \in T$. These could also be used to construct the [[HoTT book real numbers]] if one only has an integral subdomain $R \subseteq \mathbb{Q}$ such as the [[dyadic rational numbers]] or the [[decimal rational numbers]], where the index set $T$ is $R_+$ rather than $\mathbb{Q}_+$. 

### Uniform spaces

Seven axioms are usually added to a $T$-premetric spaces, to get different variants of a [[uniform space]]. 

1. for every element $U \in T$ and $a \in S$, $a \sim_U a$

2. for every element $U \in T$, there exists an element $V \in T$ such that for every $a \in S$, $b \in S$, and $c \in S$, if $a \sim_V b$ and $b \sim_V c$, then $a \sim_U c$. 

3. For every element $U \in T$, there exists an element $V \in T$ such that for every $a \in S$ and $b \in S$, if $a \sim_V b$, then $b \sim_U a$. 

4. There is an element $U \in T$ and elements $a \in S$ and $b \in S$ such that $a \sim_U b$. 

5. If there are element $U \in T$ and $V \in T$, then there is an element $W \in T$ such that for every element $a \in S$ and $b \in S$, if $a \sim_W b$, then $a \sim_U b$ and $a \sim_V b$. 

6. If there is an element $U \in T$, then there is an element $V \in T$ such that for all $a \in S$ and $b \in S$, if $a \sim_U b$, then $a \sim_V b$. 

7. For every element $U \in T$, there exists an element $V \in T$ such that for all elements $a \in S$ and $b \in S$, $a \sim_U b$ or $\neg (a \sim_V b)$. 

Examples of these structures include

* [[uniformly locally decomposable spaces]] satisfy all 7 axioms. 

* [[uniform spaces]] satisfy axioms 1-6

* [[quasiuniformly locally decomposable spaces]] satisfy axioms 1, 2, and 4-7

* [[quasiuniform spaces]] satisfy axioms 1, 2, and 4-6

* [[preuniform spaces]] satisfy axioms 1-3

* [[quasipreuniform spaces]] satisfy axioms 1 and 2

### Euclidean spaces

Let $R$ be an [[ordered integral domain]], and let $V$ be a [[finite set|finite]] [[rank]] $R$-[[module]] with [[basis]] $X:\mathrm{Fin}(n) \to V$ and [[positive definite]] [[bilinear form|bilinear]] [[inner product space|inner product]] $\langle -, -\rangle:V \times V \to R$, where $\langle X_i, X_j \rangle = \delta_i^j$ and $\delta_{(-)}^{(-)}:\mathrm{Fin}(n) \times \mathrm{Fin}(n) \to R$ is the [[Kronecker delta]] indexed by $\mathrm{Fin}(n)$. 

We define the Euclidean premetric $a \sim_\epsilon b$ indexed by $a \in V$, $b \in V$, and $\epsilon \in R_+$ as

$$a \sim_\epsilon b \coloneqq \sum_{i = 0}^{n - 1} \langle a - b, X_i\rangle^2 \lt \epsilon^2$$

which makes $V$ an [[Euclidean space]]. 

## Convergence

Every $T$-premetric space is a [[sequential preconvergence space]] with the convergence relation $x \to b$ between sequences $x$ and elements $b$ true if and only if for all elements $U \in T$, there exists a natural number $N \in \mathbb{N}$ such that for all natural numbers $n \geq N$, $x_n \sim_U b$. 

Given a $T$-premetric space $(S, \sim)$ and a sequence $x:\mathbb{N} \to S$, a modulus of Cauchy convergence is a function $M:T \to \mathbb{N}$ such that for all elements $U \in T$ and for all natural numbers $m \geq M(\epsilon)$ and $n \geq M(\epsilon)$, $x_m \sim_U x_n$.  

A $T$-premetric space $S$ is **[[sequentially Cauchy complete]]** if every [[Cauchy sequence]] has a unique limit. A $T$-premetric space $S$ is **sequentially modulated Cauchy complete** if every sequence with a modulus of Cauchy convergence has a unique limit. 

All this could be generalised to [[nets]], since every $T$-premetric space is also a [[preconvergence space]] with the convergence relation $x \to b$ between nets $x$ and elements $b$ true if and only if for all elements $U \in T$ and [[directed sets]] $I$, there exists an element $N \in I$ such that for all natural numbers $n \geq N$, $x_n \sim_U b$. 

## See also ##

* [[premetric space]]

* [[Richman premetric space]]

* [[Cauchy structure]]

* [[metric space]]

## References ##

* Auke B. Booij, Analysis in univalent type theory ([pdf](https://etheses.bham.ac.uk/id/eprint/10411/7/Booij2020PhD.pdf))

[[!redirects Booij premetric]]
[[!redirects Booij premetrics]]
[[!redirects Booij premetric space]]
[[!redirects Booij premetric spaces]]

[[!redirects preentourage]]
[[!redirects preentourages]]
[[!redirects pre-entourage]]
[[!redirects pre-entourages]]