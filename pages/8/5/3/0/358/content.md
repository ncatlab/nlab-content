A $k$-tuply monoidal $n$-category is an $n$-[[n-category|category]] in which (depending on the value of $k$) objects can be multiplied under a more or less commutative operation. An important point &#8212;and the key to the general definition&#8212; is that a $k$-tuply monoidal $n$-category can be interpreted as a special kind of $(n+k)$-category.

# Definition

A __$k$-tuply monoidal $n$-category__ is an $(n+k)$-category (which you may interpret as weakly or strictly as you like) such that any two parallel $j$-morphisms are equivalent, for $j < k$. One usually (at least for positive values of $k$) relabels the $j$-morphisms as $(j-k)$-morphisms. As explained below, we may assume that $-1 \leq k \leq n + 2$.

To interpret this correctly for low values of $j$, we must assume that all objects ($0$-morphisms) in a given $(n+k)$-category are parallel, which leads us to speak of the two $(-1)$-morphisms that serve as their common source and target and to accept any object as an equivalence between these.

One can continue to $(-2)$-morphisms and so on, but there is nothing to vary about these; every $n$-category is automatically $(-1)$-tuply monoidal. *However*, the naming shift is not applied at that level, so a simple $n$-category is actually a $(-1)$-tuply monoidal $(n+1)$-category. In constrast, a $0$-tuply monoidal $n$-category is an *occupied* $n$-category.

According to the [[stabilisation hypothesis]], every $k$-tuply monoidal $n$-category for $k > n + 2$ may be reinterpreted as an $(n+2)$-tuply monoidal $n$-category. Unlike the previous restriction on the value of $k$, this is not trivial.

## Special cases

As remarked before, a $(-1)$-tuply monoidal $n$-category is a simple $(n-1)$-category. Similarly, a $0$-tuply monoidal $n$-category is an occupied $n$-category, that is an $n$-category with at least one object.

A __stably monoidal $n$-category__ is an $(n+2)$-tuply monoidal $n$-category. Although the general definition above won\'t give it, there is a notion of stably monoidal $\infty$-category, basically an $\infty$-category that can be made $k$-tuply monoidal for any value of $k$ in a consistent way.

# The periodic table

There is a [[periodic table]] of $k$-tuply monoidal $n$-categories.

<table><tr><th><i>k</i>&darr;\<i>n</i>&rarr;</th><th>&minus;1</th><th>0</th><th>1</th><th>2</th><th>&hellip;</th></tr>
<tr><th>&minus;1</th><td>trivial</td><td>[[truth value]]</td><td>[[set]]</td><td>[[category]]</td><td>&hellip;</td></tr>
<tr><th>0</th><td>trivial</td><td>[[occupied set]]</td><td>occupied category</td><td>occupied [[2-category]]</td><td>&hellip;</td></tr>
<tr><th>1</th><td>trivial</td><td>[[monoid]]</td><td>[[monoidal category]]</td><td>[[monoidal 2-category]]</td><td>&hellip;</td></tr>
<tr><th>2</th><td>"</td><td>[[abelian monoid]]</td><td>[[braided monoidal category]]</td><td>[[braided monoidal 2-category]]</td><td>&hellip;</td></tr>
<tr><th>3</th><td>"</td><td>"</td><td>[[symmetric monoidal category]]</td><td>[[sylleptic monoidal 2-category]]</td><td>&hellip;</td></tr>
<tr><th>4</th><td>"</td><td>"</td><td>"</td><td>[[symmetric monoidal 2-category]]</td><td>&hellip;</td></tr>
<tr><th>&vellip;</th><td>"</td><td>"</td><td>"</td><td>"</td><td>&dellip;</td></tr></table>

Historically, the row where $k = -1$ was ignored, as was the occupiedness restriction for $k = 0$. This gave a table as follows:

<table><tr><th><i>k</i>&darr;\<i>n</i>&rarr;</th><th>&minus;2</th><th>&minus;1</th><th>0</th><th>1</th><th>2</th><th>&hellip;</th></tr>
<tr><th>0</th><td>trivial</td><td>[[truth value]]</td><td>[[set]]</td><td>[[category]]</td><td>&hellip;</td></tr>
<tr><th>1</th><td>"</td><td>trivial</td><td>[[monoid]]</td><td>[[monoidal category]]</td><td>[[monoidal 2-category]]</td><td>&hellip;</td></tr>
<tr><th>2</th><td>"</td><td>"</td><td>[[abelian monoid]]</td><td>[[braided monoidal category]]</td><td>[[braided monoidal 2-category]]</td><td>&hellip;</td></tr>
<tr><th>3</th><td>"</td><td>"</td><td>"</td><td>[[symmetric monoidal category]]</td><td>[[sylleptic monoidal 2-category]]</td><td>&hellip;</td></tr>
<tr><th>4</th><td>"</td><td>"</td><td>"</td><td>"</td><td>[[symmetric monoidal 2-category]]</td><td>&hellip;</td></tr>
<tr><th>&vellip;</th><td>"</td><td>"</td><td>"</td><td>"</td><td>"</td><td>&dellip;</td></tr></table>

Indeed, it was this table that inspired the definition of $(-1)$-[[(-1)-category|category]] and $(-2)$-[[(-2)-category|category]] in the first place. However, a closer look at the general definition of $(n,r)$-[[(n,r)-category|category]] shows that these are not well behaved concepts after all, and a closer look at low values of $k$ destroys the motivation for them. (In fact, the first table includes the column where $n = -1$ only to illustrate that there is nothing interesting there.)