# Idea

Two important [[periodic table]]s are the table of $k$-[[k-tuply monoidal n-category|tuply monoidal]] $n$-categories and the table of $(n,r)$-[[(n,r)-category|categories]]. These can actually be combined into a single 3D table, which surprisingly also includes $k$-[[k-tuply groupal n-groupoid|tuply groupal]] $n$-groupoids.

# Definition

A __$k$-tuply monoidal $(n,r)$-category__ is a [[pointed object|pointed]] $\infty$-[[infinity-category|category]] (which you may interpret as weakly or strictly as you like) such that:
* any two parallel $j$-morphisms are equivalent, for $j \lt k$;
* any $j$-morphism is an equivalence, for $j \gt r + k$;
* any two parallel $j$-morphisms are equivalent, for $j \gt n + k$.

Keep in mind that one usually relabels the $j$-morphisms as $(j-k)$-morphisms, which explains the usage of $r + k$ and $n + k$ instead of $r$ and $n$. As explained below, we may assume that $n \geq -1$, $-1 \leq r \leq n + 1$, $0 \leq k \leq n + 2$, and (if convenient) $r + k \geq 0$.

To interpret this correctly for low values of $j$, assume that all [[object]]s ($0$-morphisms) in a given $\infty$-category are parallel, which leads one to speak of the two $(-1)$-morphisms that serve as their common source and target and to accept any object as an equivalence between these. In particular, any $j$-morphism is an equivalence for $j \lt 1$, so if $r + k = 0$, then the condition is satisfied for any smaller value of $r + k$. Thus, we may assume that $r + k \geq 0$. Similarly, since there is a chosen object (the basepoint), any parallel $j$-morphisms are equivalent for $j \lt 1$, 

The conditions that $j \lt k$ and that $j \gt n + k$ will overlap if $n \lt - 1$, so we don\'t use such values of $n$. In other words, any $k$-tuply monoidal $(-1,r)$-category is also a $k$-tuply monoidal $(n,r)$-category for any $n \lt - 1$.

If any two parallel $j$-morphisms are equivalent, then any $j$-morphism between equivalent $(j-1)$-morphisms is an equivalence (being parallel to an equivalence for $j \gt 0$ and automatically for $j \lt 1$). Accordingly, any $k$-tuply monoidal $(n,0)$-category is automatically also a $k$-tuply monoidal $(n,r)$-category for any $r \lt 0$, and any $k$-tuply monoidal $(n,r)$-category for $r \gt n + 1$ is also a $k$-tuply monoidal $(n,n+1)$-category. Thus, we don\'t need $r \lt -1$ or $r \gt n + 1$.

According to the [[stabilization hypothesis|stabilisation hypothesis]], every $k$-tuply monoidal $(n,r)$-category for $k \gt n + 2$ may be reinterpreted as an $(n+2)$-tuply monoidal $(n,r)$-category. Unlike the other restrictions on values of $n, r, k$, this one is not trivial.

# Special cases

A $0$-tuply monoidal $(n,r)$-category is simply a pointed $(n,r)$-category. The restriction that $r + k \geq 0$ becomes that $r \geq 0$. This is why $(n,r)$-categories use $0 \leq r \leq n + 1$ rather than the restriction on $r$ given before.

A $k$-tuply monoidal $(n,0)$-category is a $k$-tuply monoidal $n$-[[n-groupoid|groupoid]]. A $k$-tuply monoidal $(n,-1)$-category is a $k$-[[k-tuply groupal n-groupoid|tuply groupal]] $n$-groupoid. This is why [[groupal category|groupal categories]] don\'t come up much; the progression from [[monoidal category|monoidal categories]] to [[monoidal groupoid|monoidal groupoids]] to [[groupal groupoid|groupal groupoids]] is a straight line up one column of the periodic table of [[monoidal (n,r)-category|monoidal]] $(n,r)$-categories. (But if we moved to a 4D table that required all $j$-morphisms to be equivalences for sufficiently low values of $j$, then groupal categories would appear there.)

A $k$-tuply monoidal $(n,n)$-category is simply a $k$-tuply monoidal $n$-category. A $k$-tuply monoidal $(n,n+1)$-category is a $k$-tuply monoidal $(n+1)$-[[n-poset|poset]]. Note that a $k$-tuply monoidal $\infty$-category and a $k$-tuply monoidal $\infty$-poset are the same thing.

A __stably monoidal $(n,r)$-category__, or __symmetric monoidal $(n,r)$-category__, is an $(n+2)$-tuply monoidal $(n,r)$-category. Although the general definition above won\'t give it, there is a notion of stably monoidal $(\infty,r)$-category, basically an $(\infty,r)$-category that can be made $k$-tuply monoidal for any value of $k$ in a consistent way.