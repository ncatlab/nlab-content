A numerable open cover is an open cover that admits a subordinate partition of unity.

### Definition ###

Let $\{U_i\}$ be an open [[cover]] of the space $X$. It is said to be **numerable** if there is a collection of functions $\phi_i:X \to [0,1]$ such that 

* $\overline{supp(\phi_i)} \subset U_i$,
* at each point $x\in X$, only finitely many of the $\phi_i$ are non-zero,
* $\sum_i \phi_i(x) \equiv 1 \forall x\in X$.

Numerable open covers form a [[site]]. Many classical theorems concerning bundles are stated for the numerable site. For example, the classifying space $\mathcal{B}G$ actually classifies bundles which trivialise over a numerable cover. 

For paracompact spaces, numerable covers are cofinite in open covers, so that the numerable site is equivalent to the open cover site. (This needs some more and better saying -David R)