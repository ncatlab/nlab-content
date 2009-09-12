Given a [[manifold]] (or [[generalized smooth space]]) $X$, the _tangent bundle_ $T_*(X)$ of $X$ is a [[vector bundle]] over $X$.  A _tangent vector_ on $X$ is an element of $T_*(X)$.  The _tangent space_ of $X$ at a point $a$ is the [[fiber]] $T_a(X)$ of $T_*(X)$ over $a$; it is a [[vector space]].  A _tangent vector field_ on $X$ is a [[section]] of $T_*(X)$.

We have yet to define the tangent bundle; how to do this depends on what sort of space $X$ is.  Here we assume that $X$ is a [[manifold]]; see [[Frölicher space]] for the definition in that context.

There are 3 standard definitions of tangent vector known as algebraic (derivation), geometric (equivalence class of germs of curves) and physical definition (via components in local coordinate system with prescribed behaviour under change of coordinates). 

Algebraically, we may define a __tangent vector__ $v$ at $a$ on $X$ as a [[scalar]]-valued [[derivation]] on the space of [[germ]]s of differentiable [[functions]] defined on $X$ near $a$, augmented by evaluation at $a$.  That is, given [[partial functions]] $f$ and $g$, each defined on some [[neighbourhood]] of $a$, we have:

1.  $v[f] = v[g]$ if $f = g$ on some (perhaps smaller) neighbourhood of $a$,
2.  $v[f + g] = v[f] + v[g]$,
3.  $v[c f] = c\, v[f]$ for $c$ a scalar,
4.  $v[f g] = f(a)\, v[g] + v[f]\, g(a)$;

In light of (4), (3) is equivalent to:

*  $v[k] = 0$ for $k$ a [[constant function]] (or indeed, for any function constant on any neighbourhood of $a$).

Globally, we may define a __tangent vector field__ $v$ as an ordinary (unaugmented) derivation on the space of differentiable functions defined on all of $X$.  (This works for differentiable manifolds and smooth manifolds, but not for [[analytic manifold]]s and [[algebraic manifold]]s; we need to be able to change functions locally.)  That is, given [[functions]] $f$ and $g$, we have:

1.  $v[f] = v[g]$ if $f = g$ (so really, the only reason to list this is to keep the numbering the same),
2.  $v[f + g] = v[f] + v[g]$,
3.  $v[c f] = c\, v[f]$ for $c$ a scalar,
4.  $v[f g] = f\, v[g] + v[f]\, g$;

In light of (4), (3) is again equivalent to:

*  $v[k] = 0$ for $k$ a [[constant function]].


Given a differentiable [[curve]] $c: \mathbf{R} \to X$, the __derivative__ $\dot{c}$ of $c$ is a curve in the tangent bundle; given an argument $t$ and a function $f$ defined near $c(t)$, the action is given by
$$ \dot{c}[f](t) = (f \circ c)'(t) ,$$
where $'$ indicates the usual derivative on the real line, so that $\dot{c}(t)$ is a tangent vector at $c(t)$.  (We really only need $c$ to be defined on a neighbourhood of $t$, of course.)


One can also *define* vectors at $a$ to be curves $c$ such that $c(0) = a$, modulo the [[equivalence relation]] that $\dot{c}(0) = \dot{d}(0)$ if $c = d$ on some neighbourhood of $0$.  (Of course, $0$ could be replaced by any argument $t$ in this definition.)  A particularly important case is when $c$ is a level curve in some system of local coordinates $(x^1,\ldots,x^n)$ at $a$; that is, $c^i(t)$ is the point whose $i$th coordinate is $t$ and whose other coordinates are the same as at $a$.  The local tangent vector field given by these curves may be written $\partial/\partial{x^i}$ or $\partial_i$ (note the placement of the scripts).  This is because, if a function $f$ defined on that coordinate patch is identified with a function $f(x^1,\ldots,x^n)$ of $n$ real variables, then $\partial_i f$ becomes identified with the partial derivative $\partial{f(x^1,\ldots,x^n)}/\partial{x^i}$.  In general, a local vector field $v$ on such a coordinate patch can be written
$$ v = \sum_i v^i\, \partial_i .$$
This fact can also be turned into a definition of tanget vector.


(Yet another possible definition comes from the duality with the [[cotangent bundle]]; of course, then you have to pick a definition of *that* that doesn\'t use duality.)


Note that $\partial/\partial{f}$ doesn\'t make sense for an arbitrary function $f$; it only makes sense when $f$ is given as one component $x^i$ of a coordinate system.  That is, if $(f,g)$ and $(f,h)$ are both coordinate systems, then the two meanings of $\partial/\partial{f}$ need not be the same, because constant $g$ and constant $h$ aren\'t the same condition.  However, we can use the more complicated notation $(\partial/\partial{f})_g$ or $(\partial/\partial{f})_h$; this is common when $X$ is a [[phase space]] in [[thermodynamics]].  Of course, if a coordinate system is fixed by convention, then there is no ambiguity.


[[!redirects tangent vector]]
[[!redirects tangent space]]
[[!redirects tangent vector space]]
[[!redirects tangent vector field]]
[[!redirects tangent bundles]]
[[!redirects tangent vectors]]
[[!redirects tangent spaces]]
[[!redirects tangent vector spaces]]
[[!redirects tangent vector fields]]