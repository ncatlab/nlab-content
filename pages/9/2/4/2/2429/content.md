
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Differential geometry
+--{: .hide}
[[!include synthetic differential geometry - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

An _isometry_ is a [[function]] that preserves a metric, either in the sense of a [[metric space]] or in the sense of a [[Riemannian manifold]].


## Metric spaces

An __isometry__ $f\colon (X,d) \to (X',d')$ between metric spaces is a function $f\colon X \to X'$ between the underyling sets that respects the metrics in that $d = f^* d'$.  More explicitly, $d'(f(a),f(b)) = d(a,b)$ for any points $a,b$ in $X$.

The same idea holds for extended quasi-pseudo-generalisations of metric spaces.


## Manifolds

An __isometry__ $f\colon (X,g) \to (X',g')$ between Riemannian manifolds is a morphism $f\colon X \to X'$ between the underlying [[manifolds]] that respects the metrics in that $g = f^* g'$.  More explicitly, $g'(f_*v,f_*w) = g(v,w)$ for any [[tangent vectors]] $v,w$ on $X$.


## Global isometries

Global isometries are the [[isomorphisms]] of metric spaces or Riemannian manifolds.  An isometry is __global__ if it is a [[bijection]] whose inverse is also an isometry.  Bewteen metric spaces, isometries are necessarily [[injections]] and bijective isometries necessarily have isometries as inverses, so global isometries between metric spaces are also called _[[surjection|surjective]] isometries_; this does not work for Riemannian manifolds (where the inverse of an isometry need not be a morphism of manifolds), nor does it work for [[pseudometric spaces]] (where an isometry need not be injective).

## Infinitesimal isometries

see [[Killing vector field]]

[[!redirects isometries]]