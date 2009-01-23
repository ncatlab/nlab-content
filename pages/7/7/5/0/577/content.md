#Definition

A [[monad]]
$(T, \mu: T^2 \to T, \nu: 1 \to T)$
on a category $C$ is _cartesian_ if the category 
$C$, the functor $T$, and the natural 
transformations $\mu$ and $\nu$ are all cartesian.
Here,

* A category $C$ is cartesian if it has all 
  pullbacks.
* A functor $T: C \to D$ is
  cartesian if it preserves pullbacks.
* A natural transformation $\alpha: S \to T$
  between functors $C \to D$
  is cartesian if for each map $f: A \to B$
  in $C$, the naturality square
  \[\array{
    S A & \overset{S f}{\to} & S B \\
    \alpha_A \downarrow & & \downarrow \alpha_B \\
    T A & \underset{T f}{\to} & T B
  }\]
  is a pullback.

+--{.query}
I would call a category with all pullbacks 'locally cartesian'.  Shouldn\'t a cartesian category at least have a terminal object?  Would a terminal object make any difference here?  &#8212;[[Toby Bartels|Toby]]
=--

#References

* Tom Leinster, _Higher Operads, Higher Categories_ 
  ([arXiv](http://arxiv.org/abs/math.CT/0305049)),
  section 4.1