#Definition

A monad
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
    SA & \overset{Sf}{\to} & SB \\
    \alpha_A \downarrow & & \downarrow \alpha_B \\
    TA & \underset{Tf}{\to} & TB
  }\]
  is a pullback.

#References

* Tom Leinster, _Higher Operads, Higher Categories_ 
  ([arXiv](http://arxiv.org/abs/math.CT/0305049)),
  section 4.1