A numerable open cover is an [[open cover]] of a topological space that admits a subordinate [[partition of unity]]. 

### Definition ###

Let $\{U_i\}$ be an open [[cover]] of the space $X$ (actually Dold doesn't always require open, see discussion below). It is said to be **numerable** if there is a collection of functions $\phi_i:X \to [0,1]$ such that 

* $\overline{supp(\phi_i)} \subset U_i$,
* at each point $x\in X$, only finitely many of the $\phi_i$ are non-zero,
* $\sum_i \phi_i(x) \equiv 1 \forall x\in X$.

The open cover $\phi_i^{-1}(0,1]$ is then a locally finite cover that refines $\{U_i\}$. The functions $\{\phi_i\}$ are a [[partition of unity]].

Numerable open covers form a [[site]] called the **numerable site**. Many classical theorems concerning bundles are stated for the numerable site. For example, the [[classifying space]] $\mathcal{B}G$ actually classifies [[bundles]] which trivialise over a numerable cover. (References? Dold for Milnor's classifying space, and tom Dieck I think for Segal's) These are called [[numerable bundles]].

For paracompact spaces, numerable covers are cofinal in open covers, so that the numerable site is equivalent to the open cover site. (This needs some more and better saying -David R)

There is also some result by Bourbaki that I have to look up that numerable covers are cofinal in [[locally finite open cover|locally finite covers]] of [[normal spaces]].

### References ###

A. Dold, _Partitions of unity in the theory of fibrations_

Another one by Dold, will look it up - it talks about stacked covers in the appendix: these are useful for 'decomposing' numerable covers of products to a sort of parameterised version depending on a numerable cover of the first factor. This is important in looking at concordance of numerable bundles.