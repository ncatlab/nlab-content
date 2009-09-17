<div class="rightHandSide toc">
[[!include category theory - contents]]
***
[[!include higher category theory - contents]]
</div>


#Idea#

An $(n,r)$-category is a [[higher category theory|higher category]] such that, essentially:

* all [[k-morphism]]s for $k \gt n$ are trivial.

* all [[k-morphism]]s for $k \gt r$ are reversible.

So $(n,r)$-categories are a generalisation of both $n$-[[n-category|categories]] and $n$-[[n-groupoid|groupoids]], covering all of the ground in between (and a bit beyond). As $n$ increases, there are many more possibilities, until there are infinitely many kinds of $(\infty,r)$-[[(infinity,n)-category|categories]].


# Definition

Given a notion of $\infty$-[[infinity-category|category]] (as weak or strict as you like), then an **$(n,r)$-category** can be defined to be an $\infty$-category such that

* any $j$-morphism is an [[equivalence]], for $j \gt r$;
* any two parallel $j$-morphisms are equivalent, for $j \gt n$.

As explained below, we may assume that $n \geq -2$ and $0 \leq r \leq n + 1$ (but still allowing $r = 0$ for $n = - 2$).

You can also start with a notion of $n$-[[n-poset|poset]], then define an $(n,r)$-category to be an $(n+1)$-poset such that any $j$-morphism is an [[equivalence]] for $j \gt r$. Or, for $r \leq n$, you can start with a notion of $n$-[[n-category|category]], then define an $(n,r)$-category to be an $n$-category such that any $j$-morphism in an [[equivalence]] for $j \gt r$.

To interpret this correctly for low values of $j$, we must assume that all objects ($0$-morphisms) in a given $\infty$-category are parallel, which leads us to speak of the two $(-1)$-morphisms that serve as their common source and target and to accept any object as an equivalence between these. In particular, any $j$-morphism is an equivalence for $j \lt 1$, so if $r = 0$, then the condition is satisfied for any smaller value of $r$. Thus, we assume that $r \geq 0$.

To say that parallel $(-1)$-morphisms must be equivalent is meaningful; it requires that there be an object. One can continue to $(-2)$-morphisms and so on, but there is nothing to vary about these; so we assume that $n \geq -2$. In other words, a $(-2)$-[[(-2)-category|category]] will automatically be an $n$-category for any smaller value of $n$.

If any two parallel $j$-morphisms are equivalent, then any $j$-morphism between equivalent $(j-1)$-morphisms is an equivalence (being parallel to an identity for $j \gt 0$ and automatically for $j \lt 1$). Accordingly, any $(n,r)$-category for $r \gt n + 1$ is also an $(n,n+1)$-category. Thus, we assum that $r \leq n + 1$. However, when $n = -2$, this contradicts the assumption that $r \geq 0$, so we allow $r = 0$ in that case just to talk about $n = -2$.


# Homtopy-theoretic relation

From the point of view of [[homotopy theory]], the notion of $(n,r)$-categories may be understood as a combination of the notion of [[homotopy n-type]] and that of [[directed space]].

Recall that an [[(∞,0)-category]] is an [[∞-groupoid]]. In light of the [[homotopy hypothesis]] -- that identifies $\infty$-groupoids with (nice) [[topological space]]s and [[n-groupoid]]s with [[homotopy n-type]]s -- and in view of the notion of [[directed space]], the following terminology is suggestive:

+-- {: .standout}

An $(n,r)$-category is an $r$-directed homotopy $n$-type.

=--

Here we read 

* _$0$-directed_ as _undirected_

and

* _$1$-directed_ as _directed_ .

Then, indeed, we have for instance that

* a [[(1,0)-category]] is an undirected 1-type: a 1-[[groupoid]],

* a [[(n,r)-category|(2,0)-category]] is an undirected 2-type: a [[2-groupoid]],

* etc.

* a [[(n,n)-category|(1,1)-category]] is **directed 1-type** : a [[category]],

* an [[(n,n)-category]] is an $n$-directed $n$-type: an [[n-category]],

* etc.

* an [[(∞,0)-category]] is an undirected space: an [[infinity-groupoid]],

* an [[(∞,1)-category]] is a [[directed space]]: a [[quasi-category]],

* an [[(∞,n)-category]] is an $n$-directed space

* etc.


# Special cases

An [[(n,n)-category]] is simply an $n$-[[n-category|category]]. An $(n,n+1)$-category is an $(n+1)$-[[n-poset|poset]]. Note that an $\infty$-category and an $\infty$-poset are the same thing. An $(n,0)$-category is an $n$-[[n-groupoid|groupoid]].  Even though they have no special name, $(n,1)$-[[(n,1)-category|categories]] are widely studied.

For low values of $n$, many of these notions coincide.  For instance, a $0$-[[0-groupoid|groupoid]] is the same as a $0$-[[0-category|category]], namely a [[set]].  And $(-1)$-[[(-1)-groupoid|groupoid]], $(-1)$-[[(-1)-category|category]], and $0$-[[0-poset|poset]] all mean the same thing (namely, a [[truth value]]) while $(-2)$-[[(-2)-groupoid|groupoid]], $(-2)$-[[(-2)-category|category]], and $(-1)$-[[(-1)-poset|poset]] likewise all mean the same thing (namely, the [[point]]).

Of particular importance is the case where $n = \infty$. See 

* [[(infinity,n)-category]] .

## topos cases ##

An analogous systematics exists for $(n,r)$-categories that in additions have the property of being a [[topos]] or [[higher topos theory|higher topos]].

* a [[(0,1)-topos]] is a [[Heyting algebra]]

  * a $(0,1)$-[[Grothendieck topos]] is a [[locale]]

* a $(1,1)$-topos is a [[topos]]

* an [[(∞,1)-topos]] is an $(\infty,1)$-topos

# The periodic table

There is a [[periodic table]] of $(n,r)$-categories:
<table markdown="1"><tr><th>$r$&#8595;\$n$&#8594;</th><th>$-2$</th><th>$-1$</th><th>$0$</th><th>$1$</th><th>$2$</th><th>...</th></tr>
<tr><th>$0$</th><td>trivial</td><td>[[truth value]]</td><td>[[set]]</td><td>[[groupoid]]</td><td>[[2-groupoid]]</td><td>...</td></tr>
<tr><th>$1$</th><td>\"</td><td>\"</td><td>[[partial order|poset]]</td><td>[[category]]</td><td>[[(2,1)-category]]</td><td>...</td></tr>
<tr><th>$2$</th><td>\"</td><td>\"</td><td>\"</td><td>[[2-poset]]</td><td>[[2-category]]</td><td>...</td></tr>
<tr><th>$3$</th><td>\"</td><td>\"</td><td>\"</td><td>\"</td><td>[[3-poset]]</td><td>...</td></tr>
<tr><th>&#8942;</th><td>\"</td><td>\"</td><td>\"</td><td>\"</td><td>\"</td><td>&#8945;</td></tr></table>

[[!redirects (n,r)-categories]]
