
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Topology
+--{: .hide}
[[!include topology - contents]]
=--
=--
=--

\tableofcontents

## Definition

Let $\mathbb{N}^*$ denote the [[list]] of [[natural numbers]]. A **bar** is a subset $P \subseteq \mathbb{N}^*$ such that for all sequences $\alpha$ of natural numbers, there exists a natural number $n$ such that the finite list of all $\alpha(i)$ for all $i \lt n$ is in $P$. 

A bar $P$ is an **inductive bar** if for all lists $a \in \mathbb{N}^*$ and all natural numbers $n \in \mathbb{N}$, if the concatenation of $a$ with $n$ is in $P$, then $a$ is in $P$. 

A bar $P$ is a **monotone bar** if for all lists $a, b \in \mathbb{N}^*$, if $a$ is in $P$, then the concatenation of $a$ and $b$ is in $P$. 

## Related concepts

* [[fan theorem]]

* [[bar induction]]

## References

* [[Tatsuji Kawai]], *Principles of bar induction and continuity on Baire space* ([arXiv:1808.04082](https://arxiv.org/abs/1808.04082))

* [[Tatsuji Kawai]], [[Giovanni Sambin]], *The principle of pointfree continuity*, Logical Methods in Computer Science, Volume 15, Issue 1 (March 5, 2019). ([doi:10.23638/LMCS-15%281%3A22%292019](https://doi.org/10.23638/LMCS-15%281%3A22%292019), [arXiv:1802.04512](https://arxiv.org/abs/1802.04512))

[[!redirects bar]]
[[!redirects bars]]

[[!redirects inductive bar]]
[[!redirects inductive bars]]

[[!redirects monotone bar]]
[[!redirects monotone bars]]

[[!redirects monotonic bar]]
[[!redirects monotonic bars]]