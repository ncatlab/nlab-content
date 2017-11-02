

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Differential geometry
+--{: .hide}
[[!include synthetic differential geometry - contents]]
=--
=--
=--


# Partial differentiation
* table of contents
{: toc}

## Idea

When a [[multifunction]] is differentiated with respect to any one of its [[variable|arguments]] alone, holding the others fixed, then we are engaged in _partial_ [[differentiation]].


## Definition

Very generally, let $(X_i)_i$ be a [[family]] of [[differentiable spaces]] (in some sense), let $Y$ be another such space, and let $f$ be a [[differentiable map]] to $Y$ from a [[subspace]] $U$ of the [[cartesian product]] $\prod_i X_i$.  Let $d$ be a relevant [[differential]] or [[derivative]] operator, and let $x_i$ be the composite
$$ U \hookrightarrow \prod_i X_i \twoheadrightarrow X_i $$
of the [[inclusion map]] of $U$ and the $i$th [[product projection]] (the $i$th [[coordinate]]).  Then under good conditions, we have
$$ d{f} = \sum_i \partial_i{f} \,d{x_i} $$
for a unique family $(\partial_i{f})_i$ of [[linear operators]], the __partial derivatives__ of $f$ with respect to this decomposition of $U$.  The term $\partial_i{f} \,d{x_i}$, which may be denoted $d_i{f}$, is similarly a __partial differential__ of $f$.

More precisely, we choose a [[category]] of [[differentiable spaces]] and differentiable maps between them, on which there is an [[endofunctor]] that takes each space $U$ to a notion of [[tangent bundle]] $T{U}$, which is assumed to be a [[vector bundle]] over $U$, and takes a map $f\colon U \to Y$ to $d{f}\colon T{U} \to T{Y}$.  (Note that this isn't the case for [[generalised smooth spaces]], but we could take [[microlinear spaces]], as well as more familiar examples such as [[differentiable manifolds]].)  Then $d{x_i}\colon T{U} \to T{X_i}$, $\partial_i{f}_p\colon T_{x_i(p)}{X_i} \to T_{f(p)}{Y}$ is a linear operator between [[stalks]] (for $p$ a [[point]] in $U$), and the sum takes place in the [[vector space]] $T_{f(p)}{Y}$.

We can extend this if we work in a [[cartesian closed category]] of [[generalised smooth spaces]].  As in the above, let $(X_i)_{i \in I}$ be a [[family]] of [[smooth spaces]] and $Y$ another smooth space.  For simplicity, let $f \colon \prod_i X_i \to Y$ be a smooth map (aka [[morphism]] in the category) defined on the whole product (so we take $U = \prod_i X_i$ in the above).  For $i_0 \in I$ we can use the cartesian closed structure to define a morphism 

$$
C^\infty(\prod_i X_i, Y) \xrightarrow{\cong} C^\infty(\prod_{i \ne i_0} X_i, C^\infty(X_{i_0},Y)).
$$

Thus given a morphism $f \colon \prod_i X_i \to Y$ we get a parametrised family of morphisms $X_{i_0} \to Y$ which we could write (using parameters) as $f(x_{\widehat{i_0}})(x_{i_0})$.  As taking the derivative is a smooth functor, we can *partially* differentiate the morphisms by applying differentiation to the morphisms $X_{i_0} \to Y$, thus yielding $d f_{i_0}(x_{\widehat{i_0}})(x_{i_0},v)$ as a morphism $\prod_{i \ne i_0} X_i \to C^\infty(T X_{i_0}, T Y)$.  In full, $d f_{i_0}$ is the image of $f$ under the chain of morphisms:

$$
C^\infty(\prod_i X_i, Y) \xrightarrow{\cong} C^\infty(\prod_{i \ne i_0} X_i, C^\infty(X_{i_0},Y)) \xrightarrow{C^\infty(\prod_{i \ne i_0} X_i, -)} C^\infty(\prod_{i \ne i_0} X_i, C^\infty(T X_{i_0}, T Y)).
$$

This is the **partial derivative** of $f$ along $X_{i_0}$.


## Notation

When the coordinates $x_i$ are given individual names $u, v, w, \ldots$, one usually writes $\partial{f}/\partial{u}$ for $\partial_i{f}$ (where $u$ replaces $x_i$); but $(\partial{f}/\partial{u})_{v,w,\ldots}$ is less ambiguous.  Similarly, one can write $(d{f})_{v,w,\ldots}$ for the partial differential $(\partial{f}/\partial{u})_{v,w,\ldots} \,d{u}$, which is $d_i{f}$ when $u$ replaces $x_i$.  (If $d{f}$ is thought of as an [[infinitesimal]] change in $f$, then $(d{f})_{v,w,\ldots}$ is an infinitesimal change subject to the condition that $v,w,\ldots$ are _fixed_.)  Then
$$ \left(\frac{\partial{f}}{\partial{u}}\right)_{v,w,\ldots} = \frac{(d{f})_{v,w,\ldots}}{d{u}} = \frac{(d{f})_{v,w,\ldots}}{(d{u})_{v,w,\ldots}} ,$$
which explains the notation and why '$\partial$' looks like '$d$'.  (The reason for the latter equality is that $\partial_i{x_j}$ is the [[Kronecker delta]] $\delta_{i,j}$.)


## Related concepts

* [[partial differential equation]]

* [[jet bundle]]

* [[differentiable function]], [[smooth function]]

* [[function with rapidly decreasing partial derivatives]]

[[!redirects partial differentiation]]

[[!redirects partial derivative]]
[[!redirects partial derivatives]]

[[!redirects partial differential]]
[[!redirects partial differentials]]
