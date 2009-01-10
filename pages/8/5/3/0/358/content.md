A $k$-tuply monoidal $n$-category is an $n$-[[n-category|category]] in which (depending on the value of $k$) objects can be multiplied under a more or less commutative operation. An important point &#8212;and the key to the general definition&#8212; is that a $k$-tuply monoidal $n$-category can be interpreted as a special kind of $(n+k)$-category.

# Definition

A __$k$-tuply monoidal $n$-category__ is an $(n+k)$-category (which you may interpret as weakly or strictly as you like) such that any two parallel $j$-morphisms are [[equivalence|equivalent]], for $j < k$. One usually (at least for positive values of $k$) relabels the $j$-morphisms as $(j-k)$-morphisms. As explained below, we may assume that $-1 \leq k \leq n + 2$.

To interpret this correctly for low values of $j$, we must assume that all [[object]]s ($0$-morphisms) in a given $(n+k)$-category are parallel, which leads us to speak of the two $(-1)$-morphisms that serve as their common source and target and to accept any object as an equivalence between these.

One can continue to $(-2)$-morphisms and so on, but there is nothing to vary about these; every $n$-category is automatically $(-1)$-tuply monoidal. *However*, the naming shift is not applied at that level, so a simple $n$-category is actually a $(-1)$-tuply monoidal $(n+1)$-category. In constrast, a $0$-tuply monoidal $n$-category is an *inhabited* $n$-category.

According to the [[stabilization hypothesis|stabilisation hypothesis]], every $k$-tuply monoidal $n$-category for $k > n + 2$ may be reinterpreted as an $(n+2)$-tuply monoidal $n$-category. Unlike the previous restriction on the value of $k$, this is not trivial.

## Special cases

As remarked before, a $(-1)$-tuply monoidal $n$-category is a simple $(n-1)$-category. Similarly, a $0$-tuply monoidal $n$-category is an inhabited $n$-category, that is an $n$-category with at least one object.

A __stably monoidal $n$-category__ is an $(n+2)$-tuply monoidal $n$-category. Although the general definition above won\'t give it, there is a notion of stably monoidal $\infty$-category, basically an $\infty$-category that can be made $k$-tuply monoidal for any value of $k$ in a consistent way.

# The periodic table

There is a [[periodic table]] of $k$-tuply monoidal $n$-categories.

<table><tr><th><i>k</i>&darr;\<i>n</i>&rarr;</th><th>&minus;1</th><th>0</th><th>1</th><th>2</th><th>&hellip;</th></tr>
<tr><th>&minus;1</th><td>trivial</td><td>[[truth value]]</td><td>[[set]]</td><td>[[category]]</td><td>&hellip;</td></tr>
<tr><th>0</th><td>trivial</td><td>[[inhabited set]]</td><td>inhabited category</td><td>inhabited [[2-category]]</td><td>&hellip;</td></tr>
<tr><th>1</th><td>trivial</td><td>[[monoid]]</td><td>[[monoidal category]]</td><td>[[monoidal 2-category]]</td><td>&hellip;</td></tr>
<tr><th>2</th><td>"</td><td>[[abelian monoid]]</td><td>[[braided monoidal category]]</td><td>[[braided monoidal 2-category]]</td><td>&hellip;</td></tr>
<tr><th>3</th><td>"</td><td>"</td><td>[[symmetric monoidal category]]</td><td>[[sylleptic monoidal 2-category]]</td><td>&hellip;</td></tr>
<tr><th>4</th><td>"</td><td>"</td><td>"</td><td>[[symmetric monoidal 2-category]]</td><td>&hellip;</td></tr>
<tr><th>&vellip;</th><td>"</td><td>"</td><td>"</td><td>"</td><td>&dellip;</td></tr></table>

Historically, the row where $k = -1$ was ignored, as was the inhabitedness restriction for $k = 0$. This gave a table as follows:

<table><tr><th><i>k</i>&darr;\<i>n</i>&rarr;</th><th>&minus;2</th><th>&minus;1</th><th>0</th><th>1</th><th>2</th><th>&hellip;</th></tr>
<tr><th>0</th><td>trivial</td><td>[[truth value]]</td><td>[[set]]</td><td>[[category]]</td><td>&hellip;</td></tr>
<tr><th>1</th><td>"</td><td>trivial</td><td>[[monoid]]</td><td>[[monoidal category]]</td><td>[[monoidal 2-category]]</td><td>&hellip;</td></tr>
<tr><th>2</th><td>"</td><td>"</td><td>[[abelian monoid]]</td><td>[[braided monoidal category]]</td><td>[[braided monoidal 2-category]]</td><td>&hellip;</td></tr>
<tr><th>3</th><td>"</td><td>"</td><td>"</td><td>[[symmetric monoidal category]]</td><td>[[sylleptic monoidal 2-category]]</td><td>&hellip;</td></tr>
<tr><th>4</th><td>"</td><td>"</td><td>"</td><td>"</td><td>[[symmetric monoidal 2-category]]</td><td>&hellip;</td></tr>
<tr><th>&vellip;</th><td>"</td><td>"</td><td>"</td><td>"</td><td>"</td><td>&dellip;</td></tr></table>

Indeed, it was this table that inspired the definition of $(-1)$-[[(-1)-category|category]] and $(-2)$-[[(-2)-category|category]] in the first place. However, a closer look at the general definition of $(n,r)$-[[(n,r)-category|category]] shows that these are not well behaved concepts after all, and a closer look at low values of $k$ destroys the motivation for them. (In fact, I include the column where $n = -1$ in the first table just to illustrate that there is nothing interesting there.)

# Discussion #

_[[Mike Shulman|Mike]]_: I believe strongly that the definition given above should actually be called a **$k$-connected $(n+k)$-category**, while a $k$-monoidal $n$-category should be defined (at least, if we want to take the delooping hypothesis as a definition, as is done here) to be a $k$-connected $(n+k)$-category _equipped with_ a chosen $j$-morphism $I_j:I_{j-1}\to I_{j-1}$ for each $j\le k$.  See section 5.6 of [n-categories and cohomology](http://arxiv.org/abs/math.CT/0608420) for some reasons.  One important reason is that only in that way can you identify the correct transformations and higher cells between $k$-monoidal $n$-functors.

Another reason, which I mentioned briefly at the end of that but didn't emphasize, is that constructively (and therefore also for sheaves and stacks) not every inhabited set can be pointed.  A [[monoid]] in a topos is a well-known concept, and can be identified with an [[internal category]] whose object-of-objects is 1.  But an internal category such that "any two objects are isomorphic" and "there exists an object" is a good deal more general of an object and does not deserve the name "monoid" or "1-monoidal 0-category."  In particular, the above definition of "1-monoidal 0-groupoid" would reduce to a [[gerbe]] rather than a [[group]].

_Toby_: I disagree with the statement that, constructively, not every inhabited set can be made pointed. It\'s easy to prove (the obvious proof is valid) in constructive set theory that for every inhabited set $A$ there is a pointed set whose underlying set is $A$. Probably your point is really about non-well-pointed toposes. (The discussion at [[inhabited set]] may be relevant here, but probably not in an essential way.)

Otherwise, I see that you\'re entirely right. Although probably I should read Cheng and Gurski first to make sure. When I have, I\'ll fix this page (and [[periodic table]]).

_Mike_: You are right, I am thinking about toposes in which 1 is not projective.  But, of course, as you point out, even there it is still true in the internal logic that every inhabited object can be pointed.  (Although you have to be careful about interpreting that statement, since the usual internal language cannot quantify over objects.)
