In higher category theory, there are several periodic tables, analogous to the the period table of chemical elements. Just as this table allowed &#1052;&#1077;&#1085;&#1076;&#1077;&#1083;&#1077;&#1077;&#1074; to [predict the existence of undiscovered elements](https://secure.wikimedia.org/wikipedia/en/wiki/Mendeleev%27s_predicted_elements) in the table\'s gaps, so these periodic tables sometimes inspire us to invent new varieties of $n$-categories.

# History

The first periodic table of $n$-categories was a slightly distorted version of the periodic table of $k$-[[k-tuply monoidal n-category|tuply monoidal]] $n$-categories.

Fully filled out, the table looked like this:
<table><tr><th><i>k</i>&darr;\<i>n</i>&rarr;</th><th>&minus;2</th><th>&minus;1</th><th>0</th><th>1</th><th>2</th><th>&hellip;</th></tr>
<tr><th>0</th><td>trivial</td><td>[[truth value]]</td><td>[[set]]</td><td>[[category]]</td><td>[[2-category]]</td><td>&hellip;</td></tr>
<tr><th>1</th><td>"</td><td>trivial</td><td>[[monoid]]</td><td>[[monoidal category]]</td><td>[[monoidal 2-category]]</td><td>&hellip;</td></tr>
<tr><th>2</th><td>"</td><td>"</td><td>[[abelian monoid]]</td><td>[[braided monoidal category]]</td><td>[[braided monoidal 2-category]]</td><td>&hellip;</td></tr>
<tr><th>3</th><td>"</td><td>"</td><td>"</td><td>[[symmetric monoidal category]]</td><td>[[sylleptic monoidal 2-category]]</td><td>&hellip;</td></tr>
<tr><th>4</th><td>"</td><td>"</td><td>"</td><td>"</td><td>[[symmetric monoidal 2-category]]</td><td>&hellip;</td></tr>
<tr><th>&vellip;</th><td>"</td><td>"</td><td>"</td><td>"</td><td>"</td><td>&#8945;</td></tr></table>
Actually, the columns where $n = -1$ and $n = -2$ were not there, but they appeared to be required by the pattern of the table.

We now recognise that a $0$-tuply monoidal $n$-category should be *pointed*, leading to a slightly different table (see that page). Similarly, the definition given when $k \gt 0$ didn\'t mention pointedness, giving essentially the definition of $(k-1)$-[[k-connected n-category|connected]] $(n+k)$-category. This makes a difference to the notions of morphism and higher morphism between such structures.

Eugenia Cheng and Nick Gurski wrote a [paper](http://arxiv.org/abs/0708.1178) about how these don't end up quite right if you just look at $(k-1)$-connected $(n+k)$-categories, but in all cases we have analyzed they do come out correct if you look at the pointed versions.  More on this can be found in the appendix to  [n-categories and cohomology](http://arxiv.org/abs/math.CT/0608420).

# Examples

... appearances in TWF, filling gaps, the first extension to small $n$, the established literature on $(n,r)$-categories, the stabilisation hypothesis, the tangle hypothesis, the table with Lie algebroids and the like, the appendix to John\'s and Mike\'s paper; most of these individual tables will have their own pages; much of the stuff below is new ...

# A big table

Two important tables are the periodic table of $k$-[[k-tuply monoidal n-category|tuply monoidal]] $n$-categories and the periodic table of $(n,r)$-[[(n,r)-category|categories]]. These can actually be combined into a single 3D table:

A __$k$-tuply monoidal $(n,r)$-category__ is a [[pointed object|pointed]] $\infty$-[[infinity-category|category]] (which you may interpret as weakly or strictly as you like) such that:
* any two parallel $j$-morphisms are equivalent, for $j \lt k$;
* any $j$-morphism is an equivalence, for $j \gt r + k$;
* any two parallel $j$-morphisms are equivalent, for $j \gt n + k$.

Keep in mind that one usually relabels the $j$-morphisms as $(j-k)$-morphisms, which explains the usage of $r + k$ and $n + k$ instead of $r$ and $n$. As explained below, we may assume that $n \geq -1$, $-1 \leq r \leq n + 1$, $0 \leq k \leq n + 2$, and (if convenient) $r + k \geq 0$.

To interpret this correctly for low values of $j$, assume that all [[object]]s ($0$-morphisms) in a given $\infty$-category are parallel, which leads one to speak of the two $(-1)$-morphisms that serve as their common source and target and to accept any object as an equivalence between these. In particular, any $j$-morphism is an equivalence for $j \lt 1$, so if $r + k = 0$, then the condition is satisfied for any smaller value of $r + k$. Thus, we may assume that $r + k \geq 0$. Similarly, since there is a chosen object (the basepoint), any parallel $j$-morphisms are equivalent for $j \lt 1$, 

The conditions that $j \lt k$ and that $j \gt n + k$ will overlap if $n \lt - 1$, so we don\'t use such values of $n$. In other words, any $k$-tuply monoidal $(-1,r)$-category is also a $k$-tuply monoidal $(n,r)$-category for any $n \lt - 1$.

If any two parallel $j$-morphisms are equivalent, then any $j$-morphism between equivalent $(j-1)$-morphisms is an equivalence (being parallel to an equivalence for $j \gt 0$ and automatically for $j \lt 1$). Accordingly, any $k$-tuply monoidal $(n,0)$-category is automatically also a $k$-tuply monoidal $(n,r)$-category for any $r \lt 0$, and any $k$-tuply monoidal $(n,r)$-category for $r \gt n + 1$ is also a $k$-tuply monoidal $(n,n+1)$-category. Thus, we don\'t need $r \lt -1$ or $r \gt n + 1$.

According to the [[stabilization hypothesis|stabilisation hypothesis]], every $k$-tuply monoidal $(n,r)$-category for $k \gt n + 2$ may be reinterpreted as an $(n+2)$-tuply monoidal $(n,r)$-category. Unlike the other restrictions on values of $n, r, k$, this one is not trivial.

## Special cases

A $0$-tuply monoidal $(n,r)$-category is simply a pointed $(n,r)$-category. The restriction that $r + k \geq 0$ becomes that $r \geq 0$. This is why $(n,r)$-categories use $0 \leq r \leq n + 1$ rather than the restriction on $r$ given before.

A $k$-tuply monoidal $(n,0)$-category is a $k$-tuply monoidal $n$-[[n-groupoid|groupoid]]. A $k$-tuply monoidal $(n,-1)$-category is a $k$-[[k-tuply groupal n-groupoid|tuply groupal]] $n$-groupoid. This is why [[groupal category|groupal categories]] don\'t come up much; the progression from [[monoidal category|monoidal categories]] to [[monoidal groupoid|monoidal groupoids]] to [[groupal groupoid|groupal groupoids]] is a straight line up one column of the periodic table of monoidal $(n,r)$-categories. (But if we moved to a 4D table that required all $j$-morphisms to be equivalences for sufficiently low values of $j$, then groupal categories would appear there.)

A $k$-tuply monoidal $(n,n)$-category is simply a $k$-tuply monoidal $n$-category. A $k$-tuply monoidal $(n,n+1)$-category is a $k$-tuply monoidal $(n+1)$-[[n-poset|poset]]. Note that a $k$-tuply monoidal $\infty$-category and a $k$-tuply monoidal $\infty$-poset are the same thing.

A __stably monoidal $(n,r)$-category__, or __symmetric monoidal $(n,r)$-category__, is an $(n+2)$-tuply monoidal $(n,r)$-category. Although the general definition above won\'t give it, there is a notion of stably monoidal $(\infty,r)$-category, basically an $(\infty,r)$-category that can be made $k$-tuply monoidal for any value of $k$ in a consistent way.