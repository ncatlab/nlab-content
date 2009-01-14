A $k$-tuply monoidal $n$-category is an $n$-[[n-category|category]] in which objects can be multiplied in $k$ ways.  Actually, by the [[Eckmann-Hilton argument]], these $k$ ways all end up being equivalent, but the operation will be more and more commutative as $k$ increases.  When $k = n + 2$, according to the [[stabilization hypothesis]], the multiplication is maximally commutative.

There is as yet no general definition of $k$-tuply monoidal $n$-category, but the [[delooping hypothesis]] says that a $k$-tuply monoidal $n$-category can be interpreted as a special kind of $(n+k)$-category, as in the definition below.  This hypothesis has been verified in many low-dimensional cases as well as for $\infty$-[[infinity-groupoid|groupoids]] (spaces).

# Definition

A __$k$-tuply monoidal $n$-category__ is a [[pointed object|pointed]] $(n+k)$-category such that any two parallel $j$-morphisms are [[equivalence|equivalent]], for $j < k$.  One usually relabels the $j$-morphisms as $(j-k)$-morphisms.  As explained below, we may assume that $0 \leq k \leq n + 2$.  Note that you may interpret this definition as weakly or strictly as you like, by starting with weak or strict notions of $(n+k)$-category.

+--{.query}

_Mike_: Is there any reason to allow negative values of $k$?  Would we ever want to say that a $(-1)$-monoidal $n$-category is a (possibly nonempty) $(n-1)$-category?  I can't think of any.

Also, is there a reason to prefer the definition above over "a $k$-[[k-connected n-category|connected]] $(n+k)$-category equipped with a chosen object (0-morphism)"?  If nothing else, this avoids having to talk about $(-1)$-morphisms.  But I'm not even sure that the definition above is correct, if you don't ask for any compatibility between the chosen equivalences.

_Toby_: Well, I\'d like to know what it means, if anything. I don\'t have a good enough feel for the compatibility to say anything confident about that.

I briefly had a version here with compatibility, although it\'s not enough actually. I think explicit pointedness is the way to go; it answers all my questions about small $k$ too. But you can still think about $(-1)$-morphisms.

=--

The given point serves as an equivalence between $(-1)$-morphisms (for now, see $(n,r)$-[[(n,r)-category|category]] for these), so there is nothing to say if $k \leq 0$ except that the category is pointed.  Thus we may as well assume that $k \geq 0$.

According to the [[stabilization hypothesis|stabilisation hypothesis]], every $k$-tuply monoidal $n$-category for $k \gt n + 2$ may be reinterpreted as an $(n+2)$-tuply monoidal $n$-category.  Unlike the previous restriction on $k$, this is not trivial.

## Special cases

A $0$-tuply monoidal $n$-category is simply a pointed $n$-category, that is an $n$-category equipped with an object.  A $1$-tuply monoidal $n$-category may be called simply a __[[monoidal n-category]]__.

A __stably monoidal $n$-category__ is an $(n+2)$-tuply monoidal $n$-category. Although the general definition above won\'t give it, there is a notion of stably monoidal $\infty$-category, basically an $\infty$-category that can be made $k$-tuply monoidal for any value of $k$ in a consistent way. Stably monoidal $n$-categories are also called __symmetric monoidal__, since the monoidal operation is maximally commutative.

# The periodic table

There is a [[periodic table]] of $k$-tuply monoidal $n$-categories.

<table><tr><th><i>k</i>&darr;\<i>n</i>&rarr;</th><th>&minus;1</th><th>0</th><th>1</th><th>2</th><th>&hellip;</th></tr>
<tr><th>0</th><td>trivial</td><td>[[pointed set]]</td><td>[[pointed category]]</td><td>[[pointed 2-category]]</td><td>&hellip;</td></tr>
<tr><th>1</th><td>trivial</td><td>[[monoid]]</td><td>[[monoidal category]]</td><td>[[monoidal 2-category]]</td><td>&hellip;</td></tr>
<tr><th>2</th><td>"</td><td>[[abelian monoid]]</td><td>[[braided monoidal category]]</td><td>[[braided monoidal 2-category]]</td><td>&hellip;</td></tr>
<tr><th>3</th><td>"</td><td>"</td><td>[[symmetric monoidal category]]</td><td>[[sylleptic monoidal 2-category]]</td><td>&hellip;</td></tr>
<tr><th>4</th><td>"</td><td>"</td><td>"</td><td>[[symmetric monoidal 2-category]]</td><td>&hellip;</td></tr>
<tr><th>&vellip;</th><td>"</td><td>"</td><td>"</td><td>"</td><td>&dellip;</td></tr></table>

Historically, the pointedness structure was ignored for $k = 0$. This gave a table as follows:

<table><tr><th><i>k</i>&darr;\<i>n</i>&rarr;</th><th>&minus;2</th><th>&minus;1</th><th>0</th><th>1</th><th>2</th><th>&hellip;</th></tr>
<tr><th>0</th><td>trivial</td><td>[[truth value]]</td><td>[[set]]</td><td>[[category]]</td><td>[[2-category]]</td><td>&hellip;</td></tr>
<tr><th>1</th><td>"</td><td>trivial</td><td>[[monoid]]</td><td>[[monoidal category]]</td><td>[[monoidal 2-category]]</td><td>&hellip;</td></tr>
<tr><th>2</th><td>"</td><td>"</td><td>[[abelian monoid]]</td><td>[[braided monoidal category]]</td><td>[[braided monoidal 2-category]]</td><td>&hellip;</td></tr>
<tr><th>3</th><td>"</td><td>"</td><td>"</td><td>[[symmetric monoidal category]]</td><td>[[sylleptic monoidal 2-category]]</td><td>&hellip;</td></tr>
<tr><th>4</th><td>"</td><td>"</td><td>"</td><td>"</td><td>[[symmetric monoidal 2-category]]</td><td>&hellip;</td></tr>
<tr><th>&vellip;</th><td>"</td><td>"</td><td>"</td><td>"</td><td>"</td><td>&dellip;</td></tr></table>

Indeed, it was this table that inspired the definition of $(-1)$-[[(-1)-category|category]] and $(-2)$-[[(-2)-category|category]] in the first place. However, a closer look at the general definition of $(n,r)$-[[(n,r)-category|category]] shows that these are not well behaved concepts after all, and a closer look at low values of $k$ destroys the motivation for them. (In fact, I include the column where $n = -1$ in the first table just to illustrate that there is nothing interesting there.)

# Low dimensions #

(Include some discussion of particlar cases here, like monoids, abelian monoids, monoidal categories, etc.)

# Discussion #

_[[Mike Shulman|Mike]]_: I believe strongly that the definition given above should actually be called a **$k$-connected $(n+k)$-category**, while a $k$-monoidal $n$-category should be defined (at least, if we want to take the delooping hypothesis as a definition, as is done here) to be a $k$-connected $(n+k)$-category _equipped with_ a chosen $j$-morphism $I_j:I_{j-1}\to I_{j-1}$ for each $j\le k$.  See section 5.6 of [n-categories and cohomology](http://arxiv.org/abs/math.CT/0608420) for some reasons.  One important reason is that only in that way can you identify the correct transformations and higher cells between $k$-monoidal $n$-functors.

Another reason, which I mentioned briefly at the end of that but didn't emphasize, is that constructively (and therefore also for sheaves and stacks) not every inhabited set can be pointed.  A [[monoid]] in a topos is a well-known concept, and can be identified with an [[internal category]] whose object-of-objects is 1.  But an internal category such that "any two objects are isomorphic" and "there exists an object" is a good deal more general of an object and does not deserve the name "monoid" or "1-monoidal 0-category."  In particular, the above definition of "1-monoidal 0-groupoid" would reduce to a [[gerbe]] rather than a [[group]].

_Toby_: I disagree with the statement that, constructively, not every inhabited set can be made pointed. It\'s easy to prove (the obvious proof is valid) in constructive set theory that for every inhabited set $A$ there is a pointed set whose underlying set is $A$. Probably your point is really about non-well-pointed toposes. (The discussion at [[inhabited set]] may be relevant here, but probably not in an essential way.)

Otherwise, I see that you\'re entirely right. Although probably I should read Cheng and Gurski first to make sure. When I have, I\'ll fix this page (and [[periodic table]]).

_Mike_: You are right, I am thinking about toposes in which 1 is not projective.  But, of course, as you point out, even there it is still true in the internal logic that every inhabited object can be pointed.  (Although you have to be careful about interpreting that statement, since the usual internal language cannot quantify over objects.)

_Toby_: Mike, can you explain to me how a pointed $2$-connected bicategory is simply a commutative monoid, even though (and this part I understand) a $2$-connected bicategory is a commutative monoid equipped with an invertible element (the two-sided unitor). I know that, in principle, this is in the appendix, but I\'m not seeing it.

_Mike_: Let's take 3.1 of [Cheng-Gurski](http://arxiv.org/abs/0708.1178) as a starting point.  So

* a 2-connected bicategory is a commutative monoid $X$ equipped with a distinguished invertible element $d_X\in X$.  However, $d_X$ has no effect at all on the morphisms and higher morphisms, so up to equivalence in the tricategory of 2-connected bicategories, we may as well assume it is the identity.

* a (weak) functor between 2-connected bicategories is a monoid homomorphism $F:X\to Y$ equipped with a distinguished invertible element $m_F\in Y$.  However, once again $m_F$ plays no role in the higher morphisms, so it might as well be the identity.

* a (weak) natural transformation between two monoid homomorphisms is just the assertion that they are equal (and thus, every such transformation is invertible).

* a modification between two such transformations is a distinguished not-necessarily-invertible element $\Gamma\in Y$.

Now let's add the basepoints.  This gets tricky to talk about without pictures, but I'll try.

* a pointed 2-connected bicategory is one equipped with a functor from $1$, the terminal bicategory.  This is just a monoid homomorphism $1\to X$, which of course is unique, together with a distinguished invertible element in $X$ which we can ignore.  Thus every 2-connected bicategory can be pointed in an essentially unique way.

* a pointed functor between two pointed 2-connected bicategories is a functor $F:X\to Y$ together with a weak natural equivalence, say $t_F$, between $1\to X\to Y$ and $1\to Y$.  Since these are always equal as monoid homomorphisms, there is always a unique (invertible) transformation connecting them, so such a pointed functor is just a monoid homomorphism $F:X\to Y$.

* a pointed transformation from $F$ to $G$ is a transformation $a$ from $F:X\to Y$ to $G:X\to Y$ together with an invertible modification, say $c_a$, relating $a t_F$ to $t_G$.  In other words, it is an assertion that $F=G$ together with a distinguished invertible element $\Gamma_a$ of $Y$.

* a pointed modification from $a$ to $b$ is a modification $m$ such that $m c_a = c_b$.  In other words, it is a distinguished element $\Lambda\in Y$ such that $\Lambda \Gamma_a = \Gamma_b$, or $\Lambda = \Gamma_a^{-1} \Gamma_b$ since $\Gamma_a$ is invertible.  Thus, any two pointed transformations $F\to G$ are related by a unique invertible modification.

We conclude that the tricategory of pointed 2-connected bicategories is triequivalent to the category of commutative monoids and monoid homomorphisms.

You might complain that in addition of the single weak natural equivalence $t_F$, $F$ ought also to be equipped with an inverse _adjoint_ equivalence for it.  The modifications involved in this would introduce two distinguished invertible elements in $Y$, which (by the triangle identities) would have to be each other's inverses.  But these elements would again play no role in the higher morphisms, so they might as well be identities.

_Toby_: OK, I see; including higher morphisms make the various choices for extra structure equivalent. In the (merely) connected case, they add new structure at the top level, so you get an equivalence only if you stop at just the right place, while in the pointed case, you can (and must) go all the way. In either case, the dependence on the unitor that Tom pointed out will disappear as soon as you look at the functors.