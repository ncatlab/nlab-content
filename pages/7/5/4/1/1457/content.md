#Contents#
* automatic table of contents
{:toc}

# Idea #

A **metric space** is a set which comes equipped with a function which measures distance between points, called a _metric_. The metric can be used to generate a topology on the set, and a topological space whose topology comes from some metric is said to be _metrizable_. 

# Definition #

Traditionally, a metric space is defined to be a [[set]] $X$ equipped with a function 
$$d: X \times X \to [0, \infty)$$ 
(valued in nonnegative [[real numbers]]) satisfying the following axioms: 
* Triangle inequality: $d(x, y) + d(y, z) \geq d(x, z)$;
* Point inequality: $0 \geq d(x, x)$ (so $0 = d(x,x)$);
* Separation: $x = y$ if $d(x, y) = 0$ (so $x = y$ iff $d(x,y) = 0$);
* Symmetry: $d(x, y) = d(y, x)$.

Given a metric space $(X, d)$ and a point $x \in X$, the _open ball_ centered at $x$ of radius $r$ is 
$$B_r(x) = \{y \in X: d(x, y) \lt r\}$$ 
and it may be shown that the open balls form a basis for a [[topological space|topology]] on $X$. In fact, metric spaces are examples of [[uniform spaces]], and much of the general theory of metric spaces, including for example the notion of completion of a metric space, can be extrapolated to uniform spaces and even [[Cauchy spaces]].

As topological spaces, metric spaces enjoy a number of separation properties: they are [[Hausdorff space|Hausdorff]], regular, and even normal. They are also paracompact. 

# Variations #

If we allow $d$ to take values in $[0,\infty]$ instead of just in $[0,\infty)$, then we get __extended metric spaces__.  If we drop separation, then we get __pseudometric spaces__.  If we drop the symmetry condition, then we get __quasimetric spaces__.  Thus the most general notion is that of an extended quasipseudometric space, which are also called __Lawvere metric spaces__ for the reasons below.

On the other hand, if we strengthen the triangle inequality to
$$ max(d(x,y), d(y,z)) \geq d(x,z) ,$$
then we get __ultrametric spaces__, a more restricted concept.  (This include for example $p$-adic completions of number fields.)  Extended quasipseudoultrametric spaces can also be called __Lawvere ultrametric spaces__.

# Lawvere metric spaces #

Lawvere has pointed out that Lawvere metric spaces are precisely [[enriched category|categories enriched]] in the [[monoidal category|monoidal]] [[partial order|poset]] $([0, \infty], \geq)$, where the monoidal product is taken to be addition.  Taking the monoidal product to be supremum instead, enriched categories amount to Lawvere ultrametric spaces.

Thus generalized, many constructions and results on metric spaces turn out to be special cases of yet more general constructions and results of enriched category theory.  This includes for example the notion of (Cauchy) completion, which in general enriched category theory is related to [[Karoubi envelope|Karoubi envelopes]] and [[Morita equivalence]]. 

One would like to say that imposing the symmetry axiom gives us [[enriched groupoid|enriched groupoids]], which is correct for ultrametric spaces.  It\'s not clear, however, what this means for more general metric spaces, since the enriching category is then not [[cartesian monoidal category|cartesian]].

+--{: .query}
[[Mike Shulman|Mike]]: Perhaps it would be more accurate to say that the symmetry axiom gives us enriched $\dagger$-[[dagger category|categories]]?

_Toby_:  Yeah, that could work.  I was thinking of arguing that it makes sense to enrich groupoids in any monoidal poset, cartesian or otherwise, since we can write down the operations and all equations are trivial in a poset.  But maybe it makes more sense to call those enriched $\dagger$-categories.
=--


# Motivation for the axioms #

The triangle axiom is the fundamental idea behind a metric space; it goes back (at least) to Euclid and captures the idea that we are discussing the *shortest* distance between two points.  Given the triangle inequality, we have the polygon inequality
$$ d(x_0,x_1) + \cdots + d(x_{n-1},x_n) \geq d(x_0,x_n) $$
for all $n \gt 0$; the point inequality extends this to $n = 0$.

Besides extended metric spaces (where distances may be infinite), one might consider spaces where distances may be negative.  But in fact this gives us nothing new, at least if we have symmetry.  First,
$$ d(x,x) + d(x,x) \geq d(x,x) $$
forces $d(x,x) \geq 0$, so $d(x,x) = 0$; then
$$ 2 d(x,y) = d(x,y) + d(y,x) \geq d(x,x) $$
forces $d(x,y) \geq 0$.  A generalisation to negative distances is possible for quasimetric spaces, however; the simplest example has $2$ elements, with $d(x,y) = -d(y,x)$.

We can define a [[partial order]] $\leq$ on the points of a Lawvere metric space:
$$ x \leq y \;\Leftrightarrow\; d(x,y) = 0 .$$
Then the symmetry axiom implies that this relation is [[symmetric relation|symmetric]] and hence an [[equivalence relation]].  The [[quotient set]] under this equivalence relation satisfies separation; in this way, every pseudometric space is [[equivalence of categories|equivalent]] (as an enriched category) to a metric space.  Even for quasimetric spaces, we can still define an equivalence relation:
$$ x \equiv y \;\Leftrightarrow\; d(x,y) = 0 \;\wedge\; d(y,x) = 0 .$$
In [[constructive mathematics]], it works better to use $\lt$:
$$ x \lt y \;\Leftrightarrow\; d(x,y) \gt 0 ;$$
then the symmetry axiom implies that this is an [[apartness relation]], which (for quasimetric spaces) we can also define directly:
$$ x \# y \;\Leftrightarrow\; d(x,y) \gt 0 \;\vee\; d(y,x) \gt 0 .$$

# Examples #

* Every [[set]] carries the **[[discrete space|discrete metric]]** given by
  $$
    d(x,y) = \left\{\array{
      0 & if x = y
      \\
      1 & otherwise
    }\right.
  $$

  For certain purposes, it makes more sense to make most the non-zero distance $\infty$ instead of $1$; then one has an extended metric space.

* Every [[normed vector space]] is a metric space by $d(x,y) := \Vert x-y \Vert$; a pseudonormed vector space is a pseudometric space.

* Every connected [[Riemannian manifold]] becomes a pseudometric space (or a metric space if, as is often assumed, the manifold is Hausdorff) by taking the distance between two points to be infimum of the Riemannian length of all continuously differentiable paths connecting them

  $$
    d(x,y) := inf_{x \stackrel{\gamma}{\to} y} len(\gamma)
  $$

  If the manifold might not be connected, then it still becomes an extended metric space.


[[!redirects metric spaces]]
[[!redirects metric]]
[[!redirects pseudometric]]
[[!redirects pseudometric space]]
[[!redirects quasimetric]]
[[!redirects quasimetric space]]
[[!redirects ultrametric]]
[[!redirects ultrametric space]]
[[!redirects metrics]]
[[!redirects pseudometrics]]
[[!redirects pseudometric spaces]]
[[!redirects quasimetrics]]
[[!redirects quasimetric spaces]]
[[!redirects ultrametrics]]
[[!redirects ultrametric spaces]]
[[!redirects Lawvere metric space]]
[[!redirects Lawvere metric spaces]]
[[!redirects metrizable space]]
[[!redirects metrizable spaces]]
[[!redirects metrisable space]]
[[!redirects metrisable spaces]]