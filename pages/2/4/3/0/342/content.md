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

If any two parallel $j$-morphisms are equivalent, then any $j$-morphism between equivalent $(j-1)$-morphisms is an equivalence (being parallel to an identity for $j \gt 0$ and automatically for $j \lt 1$). Accordingly, any $(n,r)$-category for $r \gt n + 1$ is also an $(n,n+1)$-category. Thus, we assume that $r \leq n + 1$. However, when $n = -2$, this contradicts the assumption that $r \geq 0$, so we allow $r = 0$ in that case just to talk about $n = -2$.


# Homotopy-theoretic relation

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

+--{: .query}
[[Mike Shulman]]: I am not convinced that the homotopy hypothesis applies to anything directed.  I'll believe that maybe an $r$-directed $n$-type (whatever that means) should *have* a fundamental $(n,r)$-category, and that this operation has a left adjoint that geometrically realizes an $(n,r)$-category as an $r$-directed $n$-type.  But I don't see why to expect this adjunction to be an equivalence in the directed world, unless all of your $r$-directed $n$-types come equipped with a chosen CW-complex-like $n$-skeleton which you restrict your fundamental categories to.

More concretely: take the [[interval category]].  Realize it as a directed space; presumably you get a directed topological interval $[0,1]$.  Now take the fundamental category of this space: you get the ordered set $[0,1]$ considered as a category---quite different from the interval category!  In order to get back the interval category, you need to do something like remember the endpoints of the directed topological interval, and only use these chosen points as the objects of your fundamental category.  Perhaps everyone talking about identifying directed homotopy types with higher categories has some fix like this in mind, but if so I think it should be stressed.  (Alternately, maybe someone can tell me why I'm completely wrong.)

[[David Roberts]]: Perhaps one could take a leaf out of Ronnie Brown's book and consider filtered/stratified directed spaces. The relative fundamental category is, as you point out, the \'correct\' answer.

[[Urs Schreiber]]: right. I didn't mean to imply that there is an established theory of directed spaces that yields a directed homotopy hypothesis-theorem yet. Instead the idea was that "in view of the homotopy hypothesis" we should be entitled to think of an $(n,r)$-category as an $r$-directed $n$-type. Over at [[directed space]] I say more explicitly that one option is to _defined_ what a (nice) $r$-directed $n$-type is this way. I have very little online time today, otherwise I would now add a paragraph along these lines to the above. Maybe one of you feels like doing it. I still think that th slogan "An $(n,r)$-category is an $r$-directed $n$-type." is a very useful guiding principle, and be it for the right _definition_ of directed space. My impression is that the theory of directed spaces is at the time still tentative and not set in stonee. But if that's wrong, then I'd still keep the above slogan but put an explicit caveat that this uses the  notion "diected space" differently to that established in the literature.

[[David Corfield]]: During a discussion on fundamental categories with duals of statified spaces, we had this [description](http://golem.ph.utexas.edu/category/2006/11/this_weeks_finds_in_mathematic_2.html#c006316) of a project to provide a geometric picture of directed homtopy. Speaking of categories with duals, couldn't nLab do with some more pages on them?

[[Mike Shulman]]: Your definition at [[directed space]] ("a directed space is a topological space in which not every cell is traversable in all directions") doesn't say anything about a stratification, so I think it's misleading to then say that they could be defined as $(n,r)$-categories without making a point that this would change the notion.  My impression from the very little I've read about directed spaces is that they don't necessarily come with any sort of stratification.  Do we have any reason to want to define "$r$-directed $n$-type" to mean "$(n,r)$-category", other than that it would be cute if the homotopy hypothesis could be generalized?  We like $(n,r)$-categories for lots of reasons---but would calling them $r$-directed $n$-types really be useful to us or anyone else?

_Toby_:  I don\'t think that it helps our understanding of $(n,r)$-categories, at least not yet, which is why I moved this section down here.  But I think that it may help us to understand directed spaces, particularly to suggest the idea that spaces might be $r$-directed.
=--


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
