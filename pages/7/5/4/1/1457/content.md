## Idea

A **metric space** is a set which comes equipped with a function which measures distance between points, called a _metric_. The metric can be used to generate a topology on the set, and a topological space whose topology comes from some metric is said to be _metrizable_. 

## Definition 

Traditionally, a metric space is defined to be a [[set]] $X$ equipped with a function 
$$d: X \times X \to [0, \infty)$$ 
(valued in nonnegative [[real number]]s) satisfying the following axioms: 
* Triangle inequality: $d(x, y) + d(y, z) \geq d(x, z)$;
* Point inequality: $0 \geq d(x, x)$ (so $0 = d(x,x)$);
* Separation: $x = y$ if $d(x, y) = 0$ (so $x = y$ iff $d(x,y) = 0$);
* Symmetry: $d(x, y) = d(y, x)$.

Given a metric space $(X, d)$ and a point $x \in X$, the _open ball_ centered at $x$ of radius $r$ is 
$$B_r(x) = \{y \in X: d(x, y) \lt r\}$$ 
and it may be shown that the open balls form a basis for a [[topological space|topology]] on $X$. In fact, metric spaces are examples of [[uniform space]]s, and much of the general theory of metric spaces, including for example the notion of completion of a metric space, can be extrapolated to uniform spaces and even [[Cauchy space]]s.

As topological spaces, metric spaces enjoy a number of separation properties: they are Hausdorff, regular, and even normal. They are also paracompact. 

## Variations

If we allow $d$ to take values in $[0,\infty]$ instead of just in $[0,\infty)$, then we get __extended metric spaces__.  If we drop separation, then we get __pseudometric spaces__.  If we drop the symmetry condition, then we get __quasimetric spaces__.  Thus the most general notion is that of an extended quasipseudometric space, which are also called __Lawvere metric spaces__ for the reasons below.

On the other hand, if we strengthen the triangle inequality to
$$ max(d(x,y), d(y,z)) \geq d(x,z) ,$$
then we get __ultrametric spaces__, a more restricted concept.  (This include for example $p$-adic completions of number fields.)  Extended quasipseudoultrametric spaces can also be called __Lawvere ultrametric spaces__.

## Lawvere metric spaces

Lawvere has pointed out that Lawvere metric spaces are precisely [[enriched category|categories enriched]] in the monoidal poset $([0, \infty], \geq)$, where the monoidal product is taken to be addition.  Taking the monoidal product to be $(x, y) \mapsto max(x, y)$ instead, enriched categories amount to Lawvere ultrametric spaces.

Thus generalized, many constructions and results on metric spaces turn out to be special cases of yet more general constructions and results of enriched category theory.  This includes for example the notion of (Cauchy) completion, which in general enriched category theory is related to [[Karoubi envelope]]s and [[Morita equivalence]]. 

One would like to say that imposing the symmetry axiom gives us [[enriched groupoid]]s, but it\'s not clear that this makes sense.  (In particular, the enriching categories are not [[cartesian monoidal category|cartesian]].)