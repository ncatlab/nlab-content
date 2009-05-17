## Idea

A **metric space** is a set which comes equipped with a function which measures distance between points, called a _metric_. The metric can be used to generate a topology on the set, and a topological space whose topology comes from some metric is said to be _metrizable_. 

## Definition 

Traditionally, a metric space is defined to be a set $X$ equipped with a function 

$$d: X \times X \to [0, \infty)$$ 

(valued in nonnegative real numbers) satisfying the following axioms: 

* [Triangle inequality] $d(x, y) + d(y, z) \geq d(x, z)$
* $0 \geq d(x, x)$, and if $d(x, y) = 0$, then $x = y$
* [Symmetry] $d(x, y) = d(y, x)$ 

Given a metric space $(X, d)$ and a point $x \in X$, the _open ball_ centered at $x$ of radius $r$ is 

$$B_r(x) = \{y \in X: d(x, y) \lt r\}$$ 

and it may be shown that the open balls form a basis for a topology on $X$. In fact, metric spaces are examples of uniform spaces, and much of the general theory of metric spaces can be extrapolated to uniform spaces, including for example the notion of completion of a metric space. 

As topological spaces, metric spaces enjoy a number of separation properties: they are Hausdorff, regular, and even normal. They are also paracompact. 

## Commentary

Lawvere has argued that a useful generalization of metric spaces arises by replacing the set of possible distances $[0, \infty)$ by $[0, \infty]$, and dropping the symmetry condition and the separation condition which says that 

$$d(x, y) = 0 \Rightarrow x = y$$ 

The remaining axioms (triangle inequality and $d(x, x) = 0$) may be interpreted as saying that Lawvere metric spaces are precisely categories enriched in the monoidal poset $([0, \infty], \geq)$, where the monoidal product is taken to be addition. (Taking the monoidal product to be $(x, y) \mapsto max(x, y)$ instead, enriched categories amount to ultrametric spaces, which include for example $p$-adic completions of number fields.) 

Thus generalized, many constructions and results on metric spaces turn out to be special cases of yet more general constructions and results of enriched category theory. This includes for example the notion of (Cauchy) completion, which in general enriched category theory is related to Karoubi envelopes and Morita equivalence. 
