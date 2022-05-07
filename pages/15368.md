
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Analysis
+-- {: .hide}
[[!include analysis - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

The key conditions on a [[distance]] function for _[[metric spaces]]_ and on _[[norms]]_ on [[normed vector spaces]] is that the distance $d(x,z)$ between any two points $x,z$ is no larger than the sum of the distances $d(x,y) + d(y,z)$ via any third point $y$

$$
  d(x,z) \leq d(x,y) + d(y,z)
  \,.
$$

For the usual metric/norm on [[Euclidean space]] and $f$ and $g$ two edges of a [[triangle]]

$$
  \array{
    && y
    \\
    & {}^{\mathllap{f}}\nearrow && \searrow^{\mathrlap{g}}
    \\
    x && \underset{f + g}{\longrightarrow} && z
  }
$$

then this [[inequality]] expresses that the straight path from $x$ to $z$ is always shorter or at worst as long as the path from $x$ to $z$ via $y$.

However, [[normed fields]] and hence [[normed vector spaces]] for which this example gives the correct intuition are rare among all normed fields and vector spaces (they are the _[[archimedean]]_ ones).  Most norms instead satisfy the stronger [[ultrametric]] triangle inequality which says that

$$
  {\vert f + g \vert} \leq max({\vert f\vert}, {\vert g\vert })
  \,.
$$

A norm with this property is called _[[non-archimedean]].

## Interpretation in enriched category theory
 {#InterpretationInEnrichedCategoryTheory}

One may equivalently regard the triangle equality in [[metric spaces]] as the [[composition]] operation in a certain incarnation of the metric space as an [[enriched category]] ([Lawvere 73](#Lawvere73)). From this perspective some concepts from [[analysis]] usefully generalize to other [[enriched categories]], notably the concept of _[[Cauchy complete categories]]_. For more on this see at _[Lawvere metric space](metric+space#LawvereMetricSpace)_.

Namely regard the [[half-open interval]] $[0,\infty) \subset \mathbb{R}$ as a [[poset]] under the [[relation]] $\geq$, and regard this poset as a [[category]] (see at [[(0,1)-category]]). The operation of addition of real numbers makes this a [[monoidal category]].

This means that a category [[enriched category|enriched over]] this monoidal category $([0,\infty){\geq}, +)$ is

1. ([[objects]]) a set $X$;

1. ([[hom objects]]) for every [[pair]] of points $(x,y) \in X \times X$ a real number $d(x,y) \in [0,\infty)$

1. ([[composition]]) for all $x,y,z \in X$ a morphism in $[0,\infty)_{\geq}$ of the form

   $$
     \circ_{x,y,z} \;\colon\; d(x,y) + d(y,z) \longrightarrow d(x,z)
   $$

such that

1. ([[unitality]]) $d(x,x) = 0$;

1. ([[associativity]]) ...

Now since the [[category]] $[0,\infty)_{\geq}$ is a [[poset]], there is at most one morphism between any given pair of objects, and hence the choice of [[composition]] morphism $\circ_{x,y,z}$ above is really a condition on $d(-,-)$. Moreover, since a morphism $x \to y$ in $[0,\infty)$ exists precisely if $x \geq y$, then this condition is exactly the triangle identity

$$
  d(x,y) + d(y,z) \geq d(x,z)
  \,.
$$ 

Moreover, the [[unitality]] condition is part of the non-degeneracy condition on a metric, $d(x, y) = 0$ iff $x = y$, and the [[associativity]] condition is automatically satisfied once [[composition]] is defined.

## References

* Wikipedia, _[Triangle inequality](https://en.wikipedia.org/wiki/Triangle_inequality)_

* {#Lawvere73}  [[Bill Lawvere]] (1973).  _Metric spaces, generalized logic and closed categories_.  Reprinted in [[TAC]], 1986.  [Web](http://www.tac.mta.ca/tac/reprints/articles/1/tr1abs.html).
 

[[!redirects triangle inequalities]]
