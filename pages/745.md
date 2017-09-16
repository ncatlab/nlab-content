# Definition #

If $f:C\to E$ and $g:D\to E$ are [[functor]]s, their **comma category** is the category $(f/g)$ (also written $(f\downarrow g)$) whose

* [[object]]s are triples $(c,d,\alpha)$ where $c\in C$, $d\in D$, and $\alpha:f(c)\to g(d)$ is a morphism in $E$, and whose
* [[morphism]]s from $(c_1,d_1,\alpha_1)$ to $(c_2,d_2,\alpha_2)$ are pairs $(\beta,\gamma)$, where $\beta:c_1\to c_2$ and $\gamma:d_1\to d_2$ are morphisms in $C$ and $D$, respectively, such that $\alpha_2 . f(\beta) = g(\gamma) . \alpha_1$.


# Examples #

* If $f$ and $g$ are both the identity functor of a category $C$, then $(f/g)$ is the category $C ^{\mathbf{2}} $ of arrows  in $C$.

* If $f$ is the identity functor of $C$ and $g$ is the inclusion $1\to C$ of an object $c\in C$, then $(f/g)$ is the [[slice category]] $C/c$.

* Likewise if $g$ is the identity and $f$ is the inclusion of $c$, then $(f/g)$ is the [[coslice category]] $c/C$.


# 2-categorical properties #

The comma category $(f/g)$ comes with a canonical 2-cell in the square
$$\array{(f/g) & \to & C\\
  \downarrow & \Downarrow & \downarrow f\\
  D & \overset{g}{\to} & E}$$
which is universal in the [[2-category]] [[Cat]]; that is, it is an example of a [[2-limit]].  Squares with the same universal property in an arbitrary 2-category are called [[comma square|comma squares]] and their top left vertex is called a [[comma object]].


# Remarks #

The terminology "comma category" is a holdover from an old notation $(f,g)$ for such a category, about which the less said the better.
