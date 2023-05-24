
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Topology
+--{: .hide}
[[!include topology - contents]]
=--
=--
=--

\tableofcontents

## Definition

Given a [[set]] $X$, a **zero-set structure** on $X$ is a [[sigma-topology|$\sigma$-topology]] $\mathcal{Z}$ such that 

* For every pair of distinct points in $X$ there is an open set $Z \in \mathcal{Z}$ containing precisely one of these points.

* If $Z \in \mathcal{Z}$ then there are $Z_n \in \mathcal{Z}$ for all natural numbers $n$ such that $Z^c = \bigcup_{n \in \mathbb{N}} Z_n$.

* If $Z_1, Z_2 \in \mathcal{Z}$ and $Z_1 \cap Z_2 = \emptyset$, then there are $V_1, V_2 \in \mathcal{Z}$ with $Z_1 \subseteq V_1^c$, $Z_2 \subseteq V_2^c$, and $V_1^c \cap V_2^c = \emptyset$.

## See also

* [[zero set]]
* [[sigma-topology]]

## References

* Fedor Petrov, *"countable" topology*, MathOverflow ([web](https://mathoverflow.net/questions/173255/countable-topology))

* Hugh Gordon, *Rings of functions determined by zero-sets*. Hugh Gordon. Pacific J. Math. Volume 36, Number 1 (1971), 133-157. ([pdf](https://projecteuclid.org/journals/pacific-journal-of-mathematics/volume-36/issue-1/Rings-of-functions-determined-by-zero-sets/pjm/1102971274.pdf))

[[!redirects zero-set structure]]
[[!redirects zero-set structures]]