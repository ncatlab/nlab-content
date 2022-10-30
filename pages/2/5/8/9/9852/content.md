
# Partial differentiation
* table of contents
{: toc}

## Idea

When a [[multifunction]] is differentiated with respect to any one of its [[variable|arguments]] alone, holding the others fixed, then we are engaged in _partial_ [[differentiation]].


## Definition

Very generally, let $(X_i)_i$ be a [[family]] of [[differentiable space]]s, let $Y$ be another such space, and let $f$ be a [[differentiable map]] to $Y$ from a [[subspace]] $U$ of the [[cartesian product]] $\prod_i X_i$.  Let $d$ be a relevant [[differential]] or [[derivative]] operator, and let $x_i$ be the composite
$$ U \hookrightarrow \prod_i X_i \twoheadrightarrow X_i $$
of the [[inclusion map]] of $U$ and the $i$th [[product projection]] (the $i$th [[coordinate]]).  Then under good conditions, we have
$$ d{f} = \sum_i \partial_i{f} \,d{x_i} $$
for a unique family $(\partial_i{f})_i$ of [[linear operators]], the __partial derivatives__ of $f$ with respect to this decomposition of $U$.  The term $\partial_i{f} \,d{x_i}$, which may be denoted $d_i{f}$, is similarly a __partial differential__ of $f$.

More precisely, we have a [[category]] of differentiable spaces and differentiable maps, on which is an [[endofunctor]] that takes each space $U$ to a notion of [[tangent bundle]] $T{U}$, which is a [[vector bundle]] over $U$, and takes a map $f\colon U \to Y$ to $d{f}\colon T{U} \to T{Y}$.  Then $d{x_i}\colon T{U} \to T{X_i}$, $\partial_i{f}_p\colon T_{x_i(p)}{X_i} \to T_{f(p)}{Y}$ is a linear operator between [[stalks]] (for $p$ a [[point]] in $U$), and the sum takes place in the [[vector space]] $T_{f(p)}{Y}$.

When the coordinates $x_i$ are given individual names $u, v, w, \ldots$, one usually writes $\partial{f}/\partial{u}$ for $\partial_i{f}$ (where $u$ replaces $x_i$); but $(\partial{f}/\partial{u})_{v,w,\ldots}$ is less ambiguous.  Similarly, one can write $(d{f})_{v,w,\ldots}$ for the partial differential $(\partial{f}/\partial{u})_{v,w,\ldots} \,d{u}$, which is $d_i{f}$ when $u$ replaces $x_i$.  (If $d{f}$ is thought of as an [[infinitesimal]] change in $f$, then $(d{f})_{v,w,\ldots}$ is an infinitesimal change subject to the condition that $v,w,\ldots$ are fixed.)  Then
$$ \left(\frac{\partial{f}}{\partial{u}}\right)_{v,w,\ldots} = \frac{(d{f})_{v,w,\ldots}}{d{u}} = \frac{(d{f})_{v,w,\ldots}}{(d{u})_{v,w,\ldots}} ,$$
which explains the notation and why '$\partial$' looks like '$d$'.  (The reason for the latter equality is that $\partial_i{x_j}$ is the [[Kronecker delta]] $\delta_{i,j}$.)

## Related concepts

* [[partial differential equation]]


[[!redirects partial differentiation]]

[[!redirects partial derivative]]
[[!redirects partial derivatives]]

[[!redirects partial differential]]
[[!redirects partial differentials]]
