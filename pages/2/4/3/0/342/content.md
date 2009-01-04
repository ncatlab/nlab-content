$(n,r)$-categories are a generalisation of both $n$-[[n-category|categories]] and $n$-[[n-groupoid|groupoids]], covering all of the ground in between (and a bit beyond). As $n$ increases, there are many more possibilities, until there are infinitely many kinds of $(\infty,r)$-[[(omega,r)-category|categories]].

# Definition

An __$(n,r)$-category__ is an $\infty$-[[infinity-category|category]] (which you may interpret as weakly or strictly as you like) such that:
* any $j$-morphism is an [[equivalence]], for $j > r$;
* any two parallel $j$-morphisms are equivalent, for $j > n$.
As explained below, we may assume that $n \geq -2$ and $0 \leq r \leq n + 1$ (but still allowing $r = 0$ for $n = - 2$).

To interpret this correctly for low values of $j$, we must assume that all objects ($0$-morphisms) in a given $\infty$-category are parallel, which leads us to speak of the two $-1$-morphisms that serve as their common source and target and to accept any object as an equivalence between these. In particular, any $j$-morphism is an equivalence for $j < 1$, so if $r = 0$, then the condition is satisfied for any smaller value of $r$. Thus, we assume that $r \geq 0$.

To say that parallel $-1$-morphisms must be equivalent is meaningful; it requires that there be an object. One can continue to $-2$-morphisms and so on, but there is nothing to vary about these; so we assume that $n \geq -2$. In other words, a $(-2)$-[[(-2)-category|category]] will automatically be an $n$-category for any smaller value of $n$.

If any two parallel $j$-morphisms are equivalent, then any $j$-morphism between equivalent $(j-1)$-morphisms is an equivalence (being parallel to an identity for $j > 0$ and automatically for $j < 1$). Accordingly, any $(n,r)$-category for $r > n + 1$ is also an $(n,n+1)$-category. Thus, we assum that $r \leq n + 1$. However, when $n = -2$, this contradicts the assumption that $r \geq 0$, so we allow $r = 0$ in that case just to talk about $n = -2$.

# Special cases

An $(n,n)$-category is simply an $n$-[[n-category|category]]. An $(n,n+1)$-category is an $(n+1)$-[[n-poset|poset]]. Note that an $\omega$-category and an $\omega$-poset are the same thing. An $(n,0)$-category is an $n$-[[n-groupoid|groupoid]]. Even though they have no special name, $(n,1)$-[[(n,1)-category|categories]] are widely studied.

# The periodic table

There is a [[periodic table]] of $(n,r)$-categoires. This looks best if you leave out $n = -2$:

<table><tr><th><i>r</i>&darr;\<i>n</i>&rarr;</th><th>&minus;1</th><th>0</th><th>1</th><th>2</th><th>&hellip;</th></tr>
<tr><th>0</th><td>[[truth value]]</td><td>[[set]]</td><td>[[groupoid]]</td><td>[[2-groupoid]]</td><td>&hellip;</td></tr>
<tr><th>1</th><td>"</td><td>[[poset]]</td><td>[[category]]</td><td>[[(2,1)-category]]</td><td>&hellip;</td></tr>
<tr><th>2</th><td>"</td><td>"</td><td>[[2-poset]]</td><td>[[2-category]]</td><td>&hellip;</td></tr>
<tr><th>3</th><td>"</td><td>"</td><td>"</td><td>[[3-poset]]</td><td>&hellip;</td></tr>
<tr><th>&vellip;</th><td>"</td><td>"</td><td>"</td><td>"</td><td>&dellip;</td></tr></table>