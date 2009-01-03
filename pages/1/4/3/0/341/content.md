In higher category theory, there are several periodic tables, analogous to the the period table of chemical elements. Just as this table allowed Mendele'ev to predict the existence of undiscovered elements in the table\'s gaps, so these periodic tables sometimes inspire us to invent new varieties of $n$-categories.

# History; Examples

... appearances in TWF, filling gaps, the first extension to small $n$, the established literature on $(n,r)$-categories, the stabilisation hypothesis, the tangle hypothesis, the table with Lie algebroids and the like, the appendix to John\'s and Mike\'s paper; most of these individual tables will have their own pages; much of the stuff below is new ...

# A big table

Two important tables are the periodic table of $k$-[[k-tuply monoidal n-category|k-tuply monoidal]] n-categories and the periodic table of $(n,r)$-[[(n,r)-category|categories]]. These can actually be combined into a single 3D table:

A __$k$-tuply monoidal $(n,r)$-category__ is an $\omega$-[[infinity-category|category]] (which you may interpret as weakly or strictly as you like) such that:
* any two parallel $j$-morphisms are equivalent, for $j &lt; k$;
* any $j$-morphism is an equivalence, for $j > r + k$;
* any two parallel $j$-morphisms are equivalent, for $j > n + k$.
Keep in mind that (at least for positive values of $k$) one usually relabels the $j$-morphisms as $(j-k)$-morphisms, which explains the usage of $r + k$ and $n + k$ instead of $r$ and $n$. As explained below, we may assume that $n \geq -1$, $-1 \leq r \leq n + 1$, $-1 \leq k \leq n + 2$, and $r + k \geq 0$.

To interpret this correctly for low values of $j$, we must assume that all objects ($0$-morphisms) in a given $\omega$-category are parallel, which leads us to speak of the two $-1$-morphisms that serve as their common source and target and to accept any object as an equivalence between these. In particular, any $j$-morphism is an equivalence for $j &lt; 1$, so if $r + k = 0$, then the condition is satisfied for any smaller value of $r + k$. Thus, we assume that $r + k \geq 0$.

One can continue to $-2$-morphisms and so on, but there is nothing to vary about these; every $(n,r)$-category is automatically $-1$-tuply monoidal. *However*, the naming shift is not applied at that level, so a simple $(n,r)$-category is actually a $-1$-tuply monoidal $(n+1,r+1)$-category. In constrast, a $0$-tuply monoidal $(n,r)$-categry is an *occupied* $(n,r)$-category.

The conditions that $j &lt; k$ and that $j > n + k$ will overlap if $n &lt; - 1$, so we don\'t use such values of $n$. In other words, any $k$-tuply monoidal $(-1,r)$-category is also a $k$-tuply monoidal $(n,r)$-category for any $n &lt; - 1$.

If any two parallel $j$-morphisms are equivalent, then any $j$-morphism between equivalent $(j-1)$-morphisms is an equivalence (being parallel to an identity for $j > 0$ and automatically for $j &lt; 1$). Accordingly, any $k$-tuply monoidal $(n,0)$-category is automatically also a $k$-tuply monoidal $(n,r)$-category for any $r &lt; 0$, and any $k$-tuply monoidal $(n,r)$-category for $r > n + 1$ is also a $k$-tuply monoidal $(n,n+1)$-category. Thus, we don\'t need $r &lt; -1$ or $r > n + 1$.

According to the [[stabilisation hypothesis]], every $k$-tuply monoidal $(n,r)$-category for $k > n + 2$ may be reinterpreted as an $(n+2)$-tuply monoidal $(n,r)$-category. Unlike the other restrictions on values of $n, r, k$, this one is not trivial.

## Special cases

As remarked before, a $-1$-tuply monoidal $(n,r)$-category is a simple $(n-1,r-1)$-category. The restriction that $r + k \geq 0$ becomes that $r - 1 \geq 0$. This, along with the shift by $1$ is why $(n,r)$-categories use $n \geq -2$ and $0 \leq r \leq n + 1$ rather than the restrictions on $n, r$ given before.

Similarly, a $0$-tuply monoidal $(n,r)$-category is an occupied $(n,r)$-category, that is an $(n,r)$-category with at least one object. Now the restriction that $r + k \geq 0$ becomes that $r \geq 0$. So for occupied $(n,r)$-categories, we use $n \geq -1$ and $0 \leq r \leq n + 1$. The possibility that $n = -2$ no longer appears, since it\'s nothing new in the occupied case. That is, every occupied $(-1)$-[[(-1)-category|category]] is automatically a $(-2)$-[[(-2)-category|category]].

A $k$-tuply monoidal $(n,0)$-category is a $k$-tuply monoidal $n$-[[n-groupoid|groupoid]]. A $k$-tuply monoidal $(n,-1)$-category is a $k$-[[k-tuply groupal n-groupoid|tuply groupal]] $n$-groupoid. This is why [[groupal category|groupal categories]] don\'t come up much; the progression from [[monoidal category|monoidal categories]] to [[monoidal groupoid|monoidal groupoids]] to [[groupal groupoid|groupal groupoids]] is a straight line up one column of the periodic table of monoidal $(n,r)$-categories. (But if we moved to a 4D table that required all $j$-morphisms to be equivalences for sufficiently low values of $j$, then groupal categories would appear there.)

A $k$-tuply monoidal $(n,n)$-category is simply a $k$-tuply monoidal $n$-category. A $k$-tuply monoidal $(n,n+1)$-category is a $k$-tuply monoidal $(n+1)$-[[n-poset|poset]]. Note that a $k$-tuply monoidal $\omega$-category and a $k$-tuply monoidal $\omega$-poset are the same thing.

A __stably monoidal $(n,r)$-category__ an $(n+2)$-tuply monoidal $(n,r)$-category. Although the general definition above won\'t give it, there is a notion of stably monoidal $(\omega,r)$-category, basically an $(\omega,r)$-category that can be made $k$-tuply monoidal for any value of $k$ in a consistent way.