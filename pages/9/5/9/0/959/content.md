
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Group Theory
+-- {: .hide}
[[!include group theory - contents]]
=--
=--
=--

# Contents
* table of contents
{: toc}

## Idea

A $k$-tuply groupal $n$-groupoid is an $n$-[[n-groupoid|groupoid]] in which objects can be multiplied in $k$ invertible ways, all of which interchange with each other up to isomorphism.  By the [[Eckmann-Hilton argument]], this implies that these $k$ ways all end up being equivalent, but that the single resulting operation is more and more commutative as $k$ increases.  The [[stabilization hypothesis]] states that by the time we reach $k = n + 2$, the multiplication has become "maximally commutative."

There is as yet no general category-theoretic definition of $k$-tuply groupal $n$-groupoid, but the [[delooping hypothesis]] says that a $k$-tuply groupal $n$-groupoid can be interpreted as a special kind of $(n+k)$-groupoid, and if we wish we can take this hypothesis as a definition.  A $k$-tuply groupal $n$-groupoid can also be thought of as a $k$-tuply monoidal $(n,-1)$-[[k-tuply monoidal (n,r)-category|category]].  An alternate approach is to invoke instead the [[homotopy hypothesis]] to identify $n$-groupoids with [[homotopy n-type|homotopy n-types]], in which case we can apply classical homotopy theory.


## Definitions

### Category-theoretic

Invoking the delooping hypothesis, we define a __$k$-tuply groupal $n$-groupoid__ to be a [[pointed object|pointed]] $(n+k)$-groupoid such that any two parallel $j$-morphisms are [[equivalence|equivalent]], for $j \lt k$.  One usually relabels the $j$-morphisms as $(j-k)$-morphisms.  You may interpret this definition as weakly or strictly as you like, by starting with weak or strict notions of $(n+k)$-groupoid.

The given point serves as an equivalence between $(-1)$-morphisms (for now, see $(n,r)$-[[(n,r)-category|category]] for these), so there is nothing to say if $k \leq 0$ except that the category is pointed.  Thus we may as well assume that $k \geq 0$.  Also, according to the [[stabilization hypothesis|stabilisation hypothesis]], every $k$-tuply groupal $n$-groupoid for $k \gt n + 2$ may be reinterpreted as an $(n+2)$-tuply groupal $n$-groupoid.  Unlike the restriction $k \geq 0$, this one is not trivial.


### Homotopy-theoretic

Invoking the homotopy hypothesis, we define a __$k$-tuply monoidal $n$-groupoid__ to be an _$E_k$-$n$-type_: a [[topological space]] which is a [[homotopy n-type]] and which is equipped with an action by the [[little n-cubes operad|little k-cubes]] [[operad]] (or some operad equivalent to it).  The $k$-tuply groupal $n$-groupoids can then be identified with the [[grouplike topological monoid|grouplike]] $E_k$-[[E-k-space|spaces]].

It is a classical theorem of homotopy theory that grouplike $E_k$-spaces are the same as $k$-fold [[loop space]]s (see J.P. May, _The Geometry of Iterated Loop Spaces_).  This is the topological version of the delooping hypothesis (from which, of course, it takes its name).


### Special cases

A $0$-tuply groupal $n$-groupoid is simply a pointed $n$-groupoid, that is an $n$-groupoid equipped with a chosen object (or a space equipped with a chosen basepoint).  A $1$-tuply groupal $n$-groupoid may be called simply a __groupal $n$-groupoid__, or an __$(n+1)$-[[n-group|group]]__; topologically these can be identified with grouplike monoids that are $n$-types.

A __stably groupal $n$-groupoid__, or __symmetric groupal $n$-groupoid__, is an $(n+2)$-tuply groupal $n$-groupoid.  This is also called a __symmetric $(n+1)$-group__, with the numbering off as before.  Although the general definition above won\'t give it, there is a notion of stably groupal $\infty$-groupoid, basically an $\infty$-groupoid that can be made $k$-tuply groupal for any value of $k$ in a consistent way.  Topologically, these are called _grouplike $E_\infty$-[[E-infinity-space|spaces]]_ and can be identified with infinite [[loop space]]s.


## The periodic table
 {#PeriodicTable}

There is a [[periodic table]] of $k$-tuply groupal $n$-groupoids:
<table markdown="1"><tr><th>$k$&#8595;\$n$&#8594;</th><th>$-1$</th><th>$0$</th><th>$1$</th><th>$2$</th><th>...</th><th>$\infty$</th></tr>
<tr><th>$0$</th><td>trivial</td><td>[[pointed set]]</td><td>[[pointed object|pointed]] [[groupoid]]</td><td>[[pointed object|pointed]] [[2-groupoid]] </td><td>...</td><td>[[pointed object|pointed]] [[∞-groupoid]]</td></tr>
<tr><th>$1$</th><td>trivial</td><td>[[group]]</td><td>[[2-group]]</td><td>[[3-group]]</td><td>...</td><td>[[∞-group]]</td></tr>
<tr><th>$2$</th><td>\"</td><td>[[abelian group]]</td><td>[[braided 2-group]]</td><td>[[braided 3-group]]</td><td>...</td><td>[[braided ∞-group]]</td></tr>
<tr><th>$3$</th><td>\"</td><td>\"</td><td>[[symmetric 2-group]]</td><td>[[sylleptic 3-group]]</td><td>...</td><td>groupal [[E3-algebra]]</td></tr>
<tr><th>$4$</th><td>\"</td><td>\"</td><td>\"</td><td>[[symmetric 3-group]]</td><td>...</td><td>groupal [[E4-algebra]]</td></tr>
<tr><th>&#8942;</th><td>\"</td><td>\"</td><td>\"</td><td>\"</td><td>&#8945;</td><td>&#8942;</td></tr></table>


## References

The [[homotopy theory]] of $k$-tuply groupal $n$-groupoids is discussed in 


* [[A.R. Garzón]], J.G. Miranda, _Serre homotopy theory in subcategories of simplicial groups_, Journal of Pure and Applied Algebra Volume 147, Issue 2, 24 March 2000, Pages 107-123 (<a href="https://doi.org/10.1016/S0022-4049(98)00143-1">doi:10.1016/S0022-4049(98)00143-1</a>) 


[[!redirects k-tuply groupal n-groupoid]]
[[!redirects k-tuply groupal n-groupoids]]
