
#Contents#
* table of contents goes here
{:toc}

## The Birkhoff-von Neumann theorem

Given a [[permutation]] $\sigma \in S_n$, the [[permutation matrix]] that is associated with $\sigma$ is the $n \times n$ matrix $P_{\sigma}(j,k)$, where $1 \le j,k \le n$, whose entries are given by

$P_{\sigma}(j,k)=
\left \{
\begin{aligned}
1 & if \sigma (j)=k \\
0 & otherwise.
\end{aligned}
\right.$

An $n \times n$ doubly stochastic matrix $D$ is a square matrix whose elements are real and whose rows and columns sum to unity.  Given such a matrix, there exist nonnegative weights $\{w_{\sigma}:\sigma \in S_n\}$ such that

$\sum_{\sigma \in S_n} w_{\sigma}=1$ and $\sum_{\sigma \in S_n} w_{\sigma} P_{\sigma}=D$.

The set of such matrices of order $n$ is said to form the convex hull of permutation matrices of the same order where the latter are the vertices (extreme points) of the former.

## Quantum extensions

In the quantum context, doubly stochastic matrices become doubly stochastic channels, i.e. completely positive maps preserving both the trace and the identity.  Quantum mechanically we understand the permutations to be the unitarily implemented channels.  That is, we expect doubly stochastic quantum channels to be convex combinations of unitary channels (that is channels that can be represented by some combination of [[unitary]] transformations).  Unfortunately it is well-known that some quantum channels $cannot$ be written that way.

However, large tensor powers of a channel may be easier to represent in this way, because one need not use only product unitaries in the decomposition.  Thus one proposed solution to the problem is to denote, for any doubly stochastic channel $T$, by $d_{B}(T)$ the **Birkhoff defect**, defined as the cb-norm distance from $T$ to the convex hull of the unitarily implemented channels.  Then the key is to determine whether $d_{B}(T^{\otimes n})$ goes to zero as $n\to\infty$.

## References

* Liviu Paunescu, Florin Radulescu, _A generalisation to Birkhoff - von Neumann theorem_ ([arXiv:1506.01685](https://arxiv.org/abs/1506.01685))



[[!redirects Birkhoff-von Neumann theorem]]
[[!redirects Birkhoff–von Neumann theorem]]
[[!redirects Birkhoff--von Neumann theorem]]
[[!redirects Birkhoff--von-Neumann algorithm]]
