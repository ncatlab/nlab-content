
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Riemannian geometry
+-- {: .hide}
[[!include Riemannian geometry - contents]]
=--
#### Differential geometry
+-- {: .hide}
[[!include synthetic differential geometry - contents]]
=--
=--
=--

# Contents
* table of contents
{: toc}

## Idea

An _isometry_ is a [[function]] that preserves a [[metric]], either in the sense of a [[metric space]] or in the sense of a [[Riemannian manifold]].


## Metric spaces

An __isometry__ $f\colon (X,d) \to (X',d')$ between metric spaces is a function $f\colon X \to X'$ between the underyling sets that respects the metrics in that $d = f^* d'$.  More explicitly, $d'(f(a),f(b)) = d(a,b)$ for any points $a,b$ in $X$.

The same idea holds for extended quasi-pseudo-generalisations of metric spaces.


## Manifolds

An __isometry__ $f\colon (X,g) \to (X',g')$ between Riemannian manifolds is a morphism $f\colon X \to X'$ between the underlying [[manifolds]] that respects the metrics in that $g = f^* g'$.  More explicitly, $g'(f_*v,f_*w) = g(v,w)$ for any [[tangent vectors]] $v,w$ on $X$.


## Global isometries

Global isometries are the [[isomorphisms]] of metric spaces or Riemannian manifolds.  An isometry is __global__ if it is a [[bijection]] whose inverse is also an isometry.  Between metric spaces, isometries are necessarily [[injections]] and bijective isometries necessarily have isometries as inverses, so global isometries between metric spaces are also called _[[surjection|surjective]] isometries_; this does not work for Riemannian manifolds (where the inverse of an isometry need not be a morphism of manifolds), nor does it work for [[pseudometric spaces]] (where an isometry need not be injective).


## Infinitesimal isometries

see [[Killing vector field]]


## Isometries on normed vector spaces 

In practice, isometries $E \to F$ between [[normed vector space|normed vector spaces]] tend to be affine maps. The following theorem gives a precise meaning to this. 

A norm on a vector space is **strictly convex** if, whenever ${\|u\|} = 1 = {\|v\|}$, we have ${\|t u + (1-t)v\|} \lt 1$ for some (hence all!) $t$ in the range $0 \lt t \lt 1$. In brief, no sphere contains a line segment. Examples of strictly convex spaces include spaces of type $L^p$ for $1 \lt p \lt \infty$. 

+-- {: .un_thm} 
###### Theorem 
Let $f \colon E \to F$ an isometry between normed vector spaces, and suppose $F$ is strictly convex. Then $f$ is affine. 
=-- 

+-- {: .proof} 
###### Proof 
To say that $f \colon E \to F$ is affine means that $f$ preserves linear combinations of the form $t x + (1-t)y$. It suffices to consider only the case where $0 \lt t \lt 1$ and, by continuity considerations, only the case of dyadic rationals between $0$ and $1$. Continuing this train of thought, it suffices to prove that $f(\frac1{2}(x + y)) = \frac1{2}(f(x) + f(y))$ for all $x, y$. 

In the case of strict convexity, midpoints $\frac1{2}(u+v)$ are determined in terms of the norm, as the unique point $w$ such that 

$${\|w - u\|} = \frac1{2}{\|u-v\|} = {\|w-v\|}.$$ 

The midpoint satisfies these equations for any normed vector space, but the uniqueness is a consequence of strict convexity. For if there were two such points $w, w'$, then for some point $w''$ on the line segment between them, we would have ${\|w'' - u\|} \lt \frac1{2}{\|u-v\|}$, and ${\|w''-v\|} \leq \frac1{2}{\|u-v\|}$ by ordinary convexity. But these two inequalities taken together would violate the triangle inequality. 

As a result, since $f$ is an isometry, $w = f(\frac1{2}(x+y))$ is forced to be the midpoint between $f(x)$ and $f(y)$ if $F$ is strictly convex. This completes the proof. 
=-- 

If $F$ is not strictly convex, then isometries need not be affine. For example, consider $E = \mathbb{R}$, and $F = \mathbb{R}^2$ equipped with the $l_\infty$ (max) norm. For any contractive map $\phi \colon \mathbb{R} \to \mathbb{R}$, e.g., any smooth function with ${|\phi'|} \leq 1$, the map $E \to F$ sending $x$ to $(x, \phi(x))$ is easily seen to be an isometry. 

If however $f$ is a _surjective_ isometry between normed vector spaces, then $f$ is affine, by the [[Mazur-Ulam theorem]]. 


## Related concepts

* [[isometry group]]

* [[superisometry]]


[[!redirects isometry]]
[[!redirects isometries]]
[[!redirects global isometry]]
[[!redirects global isometries]]

[[!redirects isometric isomorphism]]
[[!redirects isometric isomorphisms]]
