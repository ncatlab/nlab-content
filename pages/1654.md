## Idea

A weighted colimit is a concept of [[colimit]] suitable for [[enriched category theory]], dual (in the enriched sense) to the concept of [[weighted limit]]. 

## Motivation ## 

Recall that a colimit of a diagram in a category $C$, that is, of a functor $F: J \to C$, is given by a universal cocone for $F$. A **cocone** for $F$ is a natural transformation from $F$ to a constant diagram 

$$\Delta(c) = (J \to 1 \stackrel{c}{\to} C)$$ 

so that a cocone for $F$ is an object of a [[comma category]] 

$$F \downarrow \Delta$$ 

where $\Delta: C^1 \to C^J$ is the diagonal functor obtained by pulling back along the unique functor $J \to 1$. A **universal cocone** is simply an initial object of $F \downarrow \Delta$. 

In enriched category theory, where one considers categories $C$ enriched in a "nice" [[monoidal category]] $V$ (generally one where $V$ is [[complete category|complete]], [[cocomplete category|cocomplete]], [[closed monoidal category|closed]] [[symmetric monoidal category|symmetric monoidal]]) there is in general no $V$-enriched diagonal functor $\Delta: C \to C^J$ to speak of. For example, when $V$ is the category [[Ab]], we have $C \simeq C^I$ where $I$ is the unit $V$-category having one object $1$ for which $hom(1, 1) = \mathbb{Z}$, but then for a general [[Ab-enriched category]] $J$, there is no [[enriched functor]] $J \to I$ to pull back along (or, there may be many, but none stand out as canonical). This shows that the usual notion of colimit doesn't adapt particularly well to the general enriched setting. 

The more flexible notion of weighted colimit (also called an _indexed colimit_ in some of the older accounts) was introduced by Borceux (and Kelly?) as giving the _right_ notion of colimit for enriched category theory. 

## Weighted colimits in ordinary category theory ## 

First we reformulate ordinary colimits in the language of [[tensor product]]s, in a way that suggests more general weighted colimits. 

Assume for the moment that the receiving category $C$ has all [[coproduct]]s and [[coequalizer]]s. As is well known, it follows that $C$ has all colimits; the proof is we can write down a formula for the colimit of $F: J \to C$: as a coequalizer of a pair 

$$\sum_{j, k \in Ob(J)} hom(j, k) \times F(j) \overset{\to}{\to} \sum_{k \in Ob(J)} F(k) \to colim_J F$$

where the cartesian product on the left refers to a coproduct of copies of $F(j)$ indexed over the set $hom(j, k)$. One of the two parallel arrows is induced by a collection of actions of the category $J$ on $F$, viz. 

$$hom(j, k) \times F(j) \to F(k) = \langle F(f): F(j) \to F(k) \rangle_{f: j \to k}$$

and the other is induced by a collection of projections 

$$hom(j, k) \times F(j) \to F(j)$$ 

each of which is the application of the functor $- \times F(j): Set \to C$ to the unique map $!: hom(j, k) \to 1.$ 

We can think of the map $hom(j, k) \to 1$ also as a component of an [[action]]: where $J$ acts on the terminal functor $1: J \to Set$. Or rather, dual to the way in which $J$ acts covariantly on $F$ (so $F$ is a _left_ $J$-module), we will think of $J$ acting _contravariantly_ on the terminal functor $1: J \to Set$ (so that $1$ becomes a _right_ $J$-module). 

Then the colimit of $F$ above is precisely a [[tensor product]] of the left module $F$ with the right module $1$. More explicitly, the tensor product is the coequalizer of two arrows 

$$\sum_{j, k} 1(k) \times hom(j, k) \times F(j) \overset{\to}{\to} \sum_j 1(j) \times F(j)$$ 

where one arrow is induced from a right action of $J$ on the functor 1, having components 

$$\rho_{j, k} \times F(j): (1(k) \times hom(j, k)) \times F(j) \to 1(j) \times F(j)$$ 

and the other is induced from a left action of $J$ on $F$, having components 

$$1(k) \times \lambda_{j, k}: 1(k) \times (hom(j, k) \times F(j)) \to 1(k) \times F(k)$$

From this standpoint, the colimit of $F$ is a rather specialized tensor product of the form 

$$1 \otimes_J F$$

and the unsuitability of this notion for general enriched categories could be thought of as a case of putting all one's eggs in the $1$ basket. 

A general right $J$-module $W: J^{op} \to Set$ may be called a **weight** (with $W(j)$ the weight at $j$). Thus instead of giving all objects $j$ an equal weight $W(j) = 1$, we vary the weight and get a more general notion of colimit (just as weighted averages generalize ordinary averages). More importantly, this notion of weighted colimit makes perfect sense in the context of enriched categories. 

## Definition ## 

Let $J$ be a [[small category]]. Given a functor $W: J^{op} \to Set$ (the _weight_) and a functor $F: J \to C$ (the _diagram_), the **weighted colimit** or tensor product is an object $W \cdot F$ of $C$ together with an isomorphism 

$$C(W \cdot F, c) \cong Set^{J^{op}}(W, C(F-, c))$$ 

that is [[natural isomorphism|natural]] in objects $c$ of $C$. (By the [[Yoneda lemma]], such an isomorphism is induced by a uniquely determined transformation 

$$W(j) \to C(F(j), W \cdot F),$$ 

natural in $j$, which is a weighted analogue of the universal cocone.) 

The notion of weighted colimit carries over in straightforward fashion to categories enriched in a complete, cocomplete, closed symmetric monoidal category $V$. In that case, if $J$ is a small $V$-category (that is a $V$-enriched category whose object class is small), and if $F: J \to C$ and $W: J^{op} \to V$ are $V$-functors, then a colimit of $F$ with respect to the weight $W$ is an object $W \cdot F$ of $C$ together with an $V$-[[enriched natural transformation|natural]] isomorphism 

$$C(W \cdot F, c) \cong V^{J^{op}}(W, C(F-, c))$$ 

(between $V$-functors in the argument $c$). In fact, we can dispense with the conditions that $V$ be complete, cocomplete, and closed, at the cost of not being able to refer to functor categories $V^{J^{op}}$, without which the notion is conceptually harder to express. 

A leitmotif playing in the background is that the category of weights $Set^{J^{op}}$ on $J$ (or $V^{J^{op}}$ in the enriched case) is the free ($V$-enriched) cocompletion of $J$. In other words, if $C$ is a ($V$-)category which is cocomplete in the "right" sense of the word, then every ($V$-)functor $F: J \to C$ extends, uniquely up to unique ($V$-)isomorphism, to a ($V$-)cocontinuous functor 

$$\widetilde{F}: V^{J^{op}} \to C$$ 

which is given by the weighted colimit construction $W \mapsto W \cdot F$. 

## Examples

To be filled in. The [[tensor product of functors]] is a general example.

## Related entries

* [[homotopy weighted colimit]]

* [[weighted limit]]

## References

* Very nice descriptions on the n-Cafe by:
  * [John Baez](http://golem.ph.utexas.edu/category/2007/02/day_on_rcfts.html#c007688)
  * [Todd Trimble](http://golem.ph.utexas.edu/category/2007/02/day_on_rcfts.html#c007723)
* Notes by Emily Riehl based on a talk by Mike Shulman [Weighted Limits and Colimits](http://www.math.jhu.edu/~eriehl/weighted.pdf)

[[!redirects weighted colimits]]