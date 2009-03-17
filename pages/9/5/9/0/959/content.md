# Idea

A $k$-tuply groupal $n$-groupoid is an $n$-[[n-groupoid|groupoid]] in which objects can be multiplied in $k$ invertible ways, all of which interchange with each other up to isomorphism.  By the [[Eckmann-Hilton argument]], this implies that these $k$ ways all end up being equivalent, but that the single resulting operation is more and more commutative as $k$ increases.  The [[stabilization hypothesis]] states that by the time we reach $k = n + 2$, the multiplication has become "maximally commutative."

There is as yet no general definition of $k$-tuply groupal $n$-groupoid, but the [[delooping hypothesis]] says that a $k$-tuply groupal $n$-groupoid can be interpreted as a special kind of $(n+k)$-groupoid, and if we wish we can take this hypothesis as a definition.  The hypothesis has been verified in many low-dimensional cases; see below.

+--{.query}
I copied this 'as yet no general definition' stuff from [[k-tuply monoidal n-category]], but I wouldn\'t be surprised if there were such a general definition for groupal groupoids.  If anybody knows or has a reference, please say!  ---Toby
=--

A $k$-tuply groupal $n$-groupoid is the same as a $k$-tuply monoidal $(n,-1)$-category; see [[k-tuply monoidal (n,r)-category]].

# Definition

For purposes of this page, a __$k$-tuply groupal $n$-groupoid__ is a [[pointed object|pointed]] $(n+k)$-groupoid such that any two parallel $j$-morphisms are [[equivalence|equivalent]], for $j \lt k$.  One usually relabels the $j$-morphisms as $(j-k)$-morphisms.  You may interpret this definition as weakly or strictly as you like, by starting with weak or strict notions of $(n+k)$-groupoid.

The given point serves as an equivalence between $(-1)$-morphisms (for now, see $(n,r)$-[[(n,r)-category|category]] for these), so there is nothing to say if $k \leq 0$ except that the category is pointed.  Thus we may as well assume that $k \geq 0$.  Also, according to the [[stabilization hypothesis|stabilisation hypothesis]], every $k$-tuply groupal $n$-groupoid for $k \gt n + 2$ may be reinterpreted as an $(n+2)$-tuply groupal $n$-groupoid.  Unlike the restriction $k \geq 0$, this one is not trivial.

## Special cases

A $0$-tuply groupal $n$-groupoid is simply a pointed $n$-groupoid, that is an $n$-groupoid equipped with a chosen object.  A $1$-tuply groupal $n$-groupal may be called simply a __groupal $n$-groupoid__, or an $(n+1)$-[[n-group|group]]__.

A __stably groupal $n$-groupoid__, or __symmetric groupal $n$-groupoid__, is an $(n+2)$-tuply groupal $n$-groupoid.  This is also called a __symmetric $(n+1)$-group__, with the numbering off as before.  Although the general definition above won\'t give it, there is a notion of stably groupal $\infty$-groupoid, basically an $\infty$-groupoid that can be made $k$-tuply groupal for any value of $k$ in a consistent way.

+--{.query}
I think that these are known, as variations on the them of $E_\infty$-[[E-infinity-space|space]] or something like that.  ---Toby
=--

# The periodic table

There is a [[periodic table]] of $k$-tuply groupal $n$-groupoids:
<table markdown="1"><tr><th>$k$&#8595;\$n$&#8594;</th><th>$-1$</th><th>$0$</th><th>$1$</th><th>$2$</th><th>...</th></tr>
<tr><th>$0$</th><td>trivial</td><td>[[pointed set]]</td><td>[[pointed object in Grpd|pointed groupoid]]</td><td>[[pointed object in 2Grpd|pointed 2-groupoid]]</td><td>...</td></tr>
<tr><th>$1$</th><td>trivial</td><td>[[group]]</td><td>[[2-group]]</td><td>[[3-group]]</td><td>...</td></tr>
<tr><th>$2$</th><td>\"</td><td>[[abelian group]]</td><td>[[braided 2-group]]</td><td>[[braided 3-group]]</td><td>...</td></tr>
<tr><th>$3$</th><td>\"</td><td>\"</td><td>[[symmetric 2-group]]</td><td>[[sylleptic 3-group]]</td><td>...</td></tr>
<tr><th>$4$</th><td>\"</td><td>\"</td><td>\"</td><td>[[symmetric 3-group]]</td><td>...</td></tr>
<tr><th>&#8942;</th><td>\"</td><td>\"</td><td>\"</td><td>\"</td><td>&#8945;</td></tr></table>