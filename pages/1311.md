A __$k$-tuply connected $n$-category__ is an $n$-[[n-category|category]] such that any two parallel $j$-morphisms are [[equivalence|equivalent]], for $j \lt k$.  You may interpret this definition as weakly or strictly as you like, by starting with weak or strict notions of $n$-category.  Note that we include the case $j = -1$ to mean that the $n$-category is [[inhabited set|inhabited]] when $k \geq 0$.

Thus, a $(-1)$-tuply connected $n$-category is simply an $n$-category, a $0$-tuply connected $n$-category is an inhabited $n$-category, a $1$-tuply connected $n$-category is an inhabited $n$-category in which all objects are equivalent, and so on.

The [[delooping hypothesis]] says that a $k$-[[k-tuply monoidal n-category|tuply monoidal]] $n$-category is the same thing as a [[pointed object|pointed]] $k$-tuply connected $(n+k)$-category.

One might want a stricter definition for $n$-categories, but this is certainly correct for $n$-[[n-groupoid|groupoid]]s.  Indeed, we can say that an $\infty$-[[infinity-groupoid|groupoid]] $X$ is $k$-tuply connected if and only if its [[fundamental n-groupoid]] $\Pi_n(X)$ is trivial for $n \lt k$.  In particular, an $\infty$-tuply connected $\infty$-groupoid is [[contractible space|contractible]].

+--{: .query}
[[Mike Shulman|Mike]]: I'm pretty sure that in algebraic topology, 1-connected means simply connected, and 0-connected means connected.  So your definitions make a space 0-connected when its fundamental $\infty$-groupoid is 1-tuply connected.  I would prefer that we retain the topologists' numbering and call this a 0-connected $\infty$-groupoid (the 'tuply' sounds weird to me for connectedness), with the off-by-one shift happening in the delooping: the $k$-fold delooping of a $k$-tuply monoidal $n$-category would be a $(k-1)$-connected $(n+k)$-category.
=--
