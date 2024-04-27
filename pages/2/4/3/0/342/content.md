
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Higher category theory
+-- {: .hide}
[[!include higher category theory - contents]]
=--
=--
=--

# Contents
* table of contents
{: toc}

## Idea

An $(n,r)$-category is a [[higher category theory|higher category]] such that, essentially:

* all [[k-morphisms]] for $k \gt n$ are trivial.

* all [[k-morphisms]] for $k \gt r$ are reversible.

Put another way: given a sequence of (higher) categories $C_0, C_1, ..., C_n$ in which each $C_{i+1}$ is of the form $Hom(A, B)$ for some $0$-cells $A$ and $B$ from $C_i$, let us say that $C_n$ is a depth-$n$ Hom-category of $C_0$. (We can also cleanly extend this notion to depth-$\infty$ Hom-categories, by taking the position that there are none). An $(n, r)$-category, then, is one in which every depth-$r$ Hom-category is an $\infty$-groupoid, and, furthermore, every depth-$(n+2)$ Hom-category is a [[point]]. (The appearance of $n+2$ here rather than $n$ allows us to make sense of this definition even when $n$ is as low as $-2$, and suggests that perhaps, had history gone differently, the conventions would be to number these differently.)

So $(n,r)$-categories are a generalisation of both $n$-[[n-category|categories]] and $n$-[[n-groupoid|groupoids]], covering some of the ground in between (and a bit beyond). As $n$ increases, there are many more possibilities, until there are infinitely many kinds of $(\infty,r)$-[[(infinity,n)-category|categories]].

Note that the choice to represent the subset of groupoidal dimensions as a single number $r$ relies on the assumption that this set is upward closed, i.e. it is of the form $\{r+1, r+2, r+3, \ldots\}$.
This need not be the case, however: ordered groupoids (and in particular the [[horizontal categorification|single object case]] of [[ordered group]]s such as $(\mathbb{Z}, +, \leq)$) are a thing. They have invertible 1-morphisms, but non-invertible 2-morphisms.
Thus, the concept of an $(n, r)$-category and the periodic table below seem to be missing out on many possible situations.

## Definition
{#Definition}

Given a notion of [[infinity-category|$\infty$-category]] (as weak or strict as you like), then an **$(n,r)$-category** can be defined to be an $\infty$-category such that

* any $j$-morphism is an [[equivalence]], for $j \gt r$;
* any two [[parallel morphisms|parallel]] $j$-morphisms are equivalent, for $j \gt n$.

As explained below, we may assume that $n \geq -2$ and $0 \leq r \leq \max(0, n + 1)$.

For finite $r$, we can also define this inductively in terms of [[(∞,r)-categories]] as follows:

+-- {: .num_defn}
###### Definition

For $-2 \leq n \leq \infty$, an **[[(n,0)-category]]** is an [[∞-groupoid]] that is [[n-truncated]]: an [[n-groupoid]]. 

For $0 \lt r \lt \infty$, an **(n,r)-category** is an [[(∞,r)-category]] $C$ such that for all [[object]]s $X,Y \in C$ the $(\infty,r-1)$-categorical [[hom-object]] $C(X,Y)$ is an $(n-1,r-1)$-category.
=--

(Even for $r = \infty$, this definition makes sense, taking $\infty - 1$ to be $\infty$, as long as we know that an $(-1,\infty)$-category is the same thing as a $(-1,0)$-category.  But this may be overkill.)

You can also start with a notion of $n$-[[n-poset|poset]], then define an $(n,r)$-category to be an $(n+1)$-poset such that any $j$-morphism is an [[equivalence]] for $j \gt r$. Or, for $r \leq n$, you can start with a notion of $n$-[[n-category|category]], then define an $(n,r)$-category to be an $n$-category such that any $j$-morphism in an [[equivalence]] for $j \gt r$.

To interpret the first definition above correctly for low values of $j$, we must assume that all objects ($0$-morphisms) in a given $\infty$-category are parallel, which leads us to speak of the two $(-1)$-morphisms that serve as their common source and target and to accept any object as an equivalence between these. In particular, any $j$-morphism is an equivalence for $j \lt 1$, so if $r = 0$, then the condition is satisfied for any smaller value of $r$. Thus, we assume that $r \geq 0$.

To say that parallel $(-1)$-morphisms must be equivalent is meaningful; it requires that there be an object. One can continue to $(-2)$-morphisms and so on, but there is nothing to vary about these; so we assume that $n \geq -2$. In other words, a $(-2)$-[[(-2)-category|category]] will automatically be an $n$-category for any smaller value of $n$.

If any two parallel $j$-morphisms are equivalent, then any $j$-morphism between equivalent $(j-1)$-morphisms is an equivalence (being parallel to an identity for $j \gt 0$ and automatically for $j \lt 1$). Accordingly, any $(n,r)$-category for $r \gt n + 1$ is also an $(n,n+1)$-category. Thus, we assume that $r \leq n + 1$ (except when $n = -2$, where it would conflict with the convention $r \geq 0$ and so we simply take $r = 0$.)


## Homotopy-theoretic relation {#HomtopyTheory}

From the point of view of [[homotopy theory]], the notion of $(n,r)$-categories may be understood as a combination of the notion of [[homotopy n-type]] and that of [[directed space]].

Recall that an [[(∞,0)-category]] is an [[∞-groupoid]]. In light of the [[homotopy hypothesis]] -- that identifies $\infty$-groupoids with (nice) [[topological spaces]] and [[n-groupoids]] with [[homotopy n-types]] -- and in view of the notion of [[directed space]], the following terminology is suggestive:

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

* an [[(∞,0)-category]] is an undirected space: an [[∞-groupoid]],

* an [[(∞,1)-category]] is a [[directed space]]: a [[quasi-category]],

* an [[(∞,n)-category]] is an $n$-directed space

* etc.

## Special cases

An [[(n,n)-category]] is simply an $n$-[[n-category|category]]. An $(n,n+1)$-category is an $(n+1)$-[[n-poset|poset]]. Note that an $\infty$-category and an $\infty$-poset are the same thing. An $(n,0)$-category is an $n$-[[n-groupoid|groupoid]].  Even though they have no special name, $(n,1)$-[[(n,1)-category|categories]] are widely studied.

For low values of $n$, many of these notions coincide.  For instance, a $0$-[[0-groupoid|groupoid]] is the same as a $0$-[[0-category|category]], namely a [[set]].  And $(-1)$-[[(-1)-groupoid|groupoid]], $(-1)$-[[(-1)-category|category]], and $0$-[[0-poset|poset]] all mean the same thing (namely, a [[truth value]]) while $(-2)$-[[(-2)-groupoid|groupoid]], $(-2)$-[[(-2)-category|category]], and $(-1)$-[[(-1)-poset|poset]] likewise all mean the same thing (namely, the [[point]]).

Of particular importance is the case where $n = \infty$. See 

* [[(∞,n)-category]] .

### Topos cases

An analogous systematics exists for $(n,r)$-categories that in additions have the property of being a [[topos]] or [[higher topos theory|higher topos]].

* a [[(0,1)-topos]] is a [[Heyting algebra]]

  * in particular, a $(0,1)$-[[Grothendieck topos]] is a [[locale]]

* a $(1,1)$-topos is a [[topos]]

* an [[(∞,1)-topos]] is what [[Higher Topos Theory]] calls an $\infty$-topos


## The periodic table 

There is a [[periodic table]] of $(n,r)$-categories:
<table>
<tr><th markdown="1" style="white-space: nowrap;">$n$&#8594;<br/>$r$&#8595;</th>
  <th markdown="1">$-2$</th>
  <th markdown="1">$-1$</th>
  <th markdown="1">$0$</th>
  <th markdown="1">$1$</th>
  <th markdown="1">$2$</th>
  <th markdown="1">...</th>
  <th markdown="1">$\infty$</th></tr>
<tr><th markdown="1">$0$</th>
  <td>[[point]]</td>
  <td>[[truth value]]</td>
  <td>[[set]]</td>
  <td>[[groupoid]]</td>
  <td>[[2-groupoid]]</td>
  <td>...</td>
  <td>[[∞-groupoid]]</td></tr>
<tr><th markdown="1">$1$</th>
  <td>"</td>
  <td>"</td>
  <td>[[partial order|poset]]</td>
  <td>[[category]]</td>
  <td>[[(2,1)-category]]</td>
  <td>...</td>
  <td>[[(∞,1)-category]]</td></tr>
<tr><th markdown="1">$2$</th>
  <td>"</td>
  <td>"</td>
  <td>"</td>
  <td>[[2-poset]]</td>
  <td>[[2-category]]</td>
  <td>...</td>
  <td>[[(∞,2)-category]]</td></tr>
<tr><th markdown="1">$3$</th>
  <td>"</td>
  <td>"</td>
  <td>"</td>
  <td>"</td>
  <td>[[3-poset]]</td>
  <td>...</td>
  <td>[[(∞,3)-category]]</td></tr>
<tr><th markdown="1">&#8942;</th>
  <td>&#8942;</td>
  <td>&#8942;</td>
  <td>&#8942;</td>
  <td>&#8942;</td>
  <td>&#8942;</td>
  <td>&#8945;</td>
  <td>&#8942;</td></tr>
<tr><th markdown="1">$\infty$</th>
  <td>point</td>
  <td>truth value</td>
  <td>poset</td>
  <td>2-poset</td>
  <td>3-poset</td>
  <td>...</td>
  <td>[[(∞,∞)-category]]/[[∞-poset]]</td></tr>
</table>

## Models for weak (n,r)-categories 

There are various [[model category]] models for collections of $(n,r)$-categories.

* The standard [[model structure on simplicial sets]] models [[∞-groupoid|(∞,0)-categories]].

* The Joyal-[[model structure on simplicial sets]] models [[(∞,1)-category|(∞,1)-categories]].

* The [[Charles Rezk]]-model structure for [[Theta space]]s models general $(n,r)$-categories.

## Related concepts

* [[directed (n,r)-graph]]

* [[(n,r)-site]]

* [[0-category]], [[(0,1)-category]]

* [[category]]

* [[2-category]]

* [[3-category]]

* [[n-category]]

* [[(∞,0)-category]]

* [[(n,1)-category]]

* [[(∞,1)-category]]

* [[(∞,2)-category]]

* [[(∞,n)-category]]

* **(n,r)-category** 

* [[(n × k)-category]], [[n-fold category]]

## References

* [[John Baez]], [[Michael Shulman]], _Lectures on n-Categories and Cohomology_, ([arXiv:math/0608420](https://arxiv.org/abs/math/0608420)), in particular pp. 34-36.


[[!redirects (n,r) categories]]
[[!redirects (n,r) category]]
[[!redirects (n,r)-categories]]
[[!redirects (n,r)-category]]
[[!redirects (n, r)-category]] 
[[!redirects (n, r)-categories]] 


