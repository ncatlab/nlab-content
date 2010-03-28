<div class="rightHandSide toc">
[[!include physicscontents]]
</div>

+-- {.query}
Zoran: there are several things called "Birkhoff's theorem" in various field of mathematics and mathematical physics, and belong even to at least 2 different classical Birkhoff's. Even wikipedia has pages for more than one such theorem. To me the first which comes to mind is Birkhoff's factorization theorem, now also popular in Kreimer-Connes-Marcolli work and in connection to loop groups (cf. book by Segal nad Pressley). I would like that the $n$lab does not mislead by distinguishing one of the several famous Bikhoff labels without mentioning and directing to 2-3 others. 

[[Ian Durham]]: Good point.  I think this probably ought to be renamed the "Birkhoff-von Neumann theorem."  Is that a good enough label or should we get more specific with it?
=--

#Contents#
* automatic table of contents goes here
{:toc}

#The Birkhoff-von Neumann theorem

Given a permutation $\sigma \in S_n$, the permutation matrix that is associated with $\sigma$ is the $n \times n$ matrix $P_{\sigma}(j,k)$, where $1 \le j,k \le n$, whose entries are given by

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

#Quantum extensions

In the quantum context, doubly stochastic matrices become doubly stochastic channels, i.e. completely positive maps preserving both the trace and the identity.  Quantum mechanically we understand the permutations to be the unitarily implemented channels.  That is, we expect doubly stochastic quantum channels to be convex combinations of unitary channels (that is channels that can be represented by some combination of [[unitary]] transformations).  Unfortunately it is well-known that some quantum channels $cannot$ be written that way.

However, large tensor powers of a channel may be easier to represent in this way, because one need not use only product unitaries in the decomposition.  Thus one proposed solution to the problem is to denote, for any doubly stochastic channel $T$, by $d_{B}(T)$ the **Birkhoff defect**, defined as the cb-norm distance from $T$ to the convex hull of the unitarily implemented channels.  Then the key is to determine whether $d_{B}(T^{\otimes n})$ goes to zero as $n\to\infty$.

>David Roberts: I'm guessing you wanted $T^{\otimes n}$ instead of $T\otimes n$.

>Ian Durham: Yep.  My bad.

Categorically, one possible way to approach this problem is to determine the relationship between the category of quantum channels, $QChan$, and the category of unitary transformations.

#Discussion

[[Ian Durham]]: Any suggestions concerning the last point?

[[David Roberts]]: There may be a functor between the two which is \'nice\' in some sense (has an [[adjoint functor|adjoint]], say) which encapsulates the next best possible result.

[[Ian Durham]]: Hmmm.  What I think I'm going to do is to try to tally up all the category theoretic properties of each.  That should make it easier to see if there's a functor between them, I would think.

[[!redirects Birkhoff-von Neumann theorem]]