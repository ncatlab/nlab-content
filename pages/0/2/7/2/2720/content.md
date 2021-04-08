

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Riemannian geometry
+--{: .hide}
[[!include Riemannian geometry - contents]]
=--
#### Differential geometry
+--{: .hide}
[[!include synthetic differential geometry - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Definition

### In terms of a 2-tensor

A **Riemannian metric** on a [[smooth manifold]] $M$ is defined as a covariant symmetric 2-[[tensor]] $(., .)_p, p \in M$ -- a section of the symmetrized second tensor power of the [[tangent bundle]] -- such that $(v,v)_p \gt 0$ for all $v \in T_p(M)$.  For convenience, we will write $(v,w)$ for $(v,w)_p$.  In other words, a Riemannian metric is a collection of (positive) inner products on each of the [[tangent space]]s $T_p(M)$ such that if $X,Y$ are (smooth) [[vector field]]s, the function $(X,Y): M \to \mathbb{R}$ defined by taking the inner product at each point, is smooth.  A [[manifold]] together with a Riemannian metric is called a [[Riemannian manifold]].

### In terms of a Vielbein

> for the moment see [[Poincare Lie algebra]] and [[first-order formulation of gravity]]
 

## Examples

There are several ways to get Riemannian metrics:
 
1. On $\mathbb{R}^n$, there is a standard Riemannian metric coming from the usual inner product.  More generally, if $g_{i j}: \mathbb{R}^n \to \mathbb{R}$ are smooth functions such that the matrix $(g_{i j}(x))$ is symmetric and positive definite for all $x \in \mathbb{R}^n$, we get a Riemannian metric $\sum_{i,j} g_{i j} d x^i \otimes d x^j$ on $\mathbb{R}^n$, where the sum is to be interpreted as a covariant tensor.

2. Given an immersion $N \to M$, a Riemannian metric on $M$ induces one on $N$ in the natural way, simply by pulling back.  For instance, any surface in $\mathbb{R}^3$ has a Riemannian structure based upon the standard Riemannian structure on $\mathbb{R}^3$---based simply on the usual inner product---and induced on the surface.  

3. Given an open covering $U_i$ on $M$, Riemannian metrics $(\cdot, \cdot)_i$ on $U_i$, and a partition of unity $\phi_i$ subordinate to the covering $U_i$, we get a Riemannian metric on $M$ by 
\[ (v,w)_p := \sum_i \phi_i(p) (v,w)_{i,p}.\]
Thus, using 1) above, any smooth manifold---which necessarily admits partitions of unity---can be given a Riemannian metric.


## Lengths of Curves

A Riemannian metric allows us to take the length of a curve in a manner resembling the standard case.  Given $v \in T_p(M)$, use the notation $\left \Vert{v} \right \Vert := (v,v) = (v,v)_p$.
If $c: I \to M$ is a smooth curve for $I$ an interval in $\mathbb{R}$, we define
\[ l(c) := \int_I \left \Vert{c'(t)}\right \Vert d t;\]
this is easily checked to be independent of parametrization, just as in the usual case.
Using this, we can make a Riemannian manifold $M$ into a metric space: for $p,q \in M$, let
\[ d(p,q) := \inf_{c \mid c(a)=p,c(b)=q} l(c).\]
 
The metric on $M$ induces the standard [[topology]] on $M$.
To see this, first note that it is a local question, so we can reduce to the case of $M$ an open ball in euclidean space $\mathbb{R}^n$.  Each tangent vector $v \in T_p(M)$ can be viewed as an element of $\mathbb{R}^n$ in a natural way.  Now let $\left \Vert{\cdot}\right \Vert_{\mathbb{R}^n}$ be the standard norm on $\mathbb{R}^n$.  By continuity, we can find $\delta \gt 0$ by shrinking $M$ if necessary such that for all $v \in T_p(M), p \in K$,
\[  \delta \left \Vert{v}\right \Vert_{\mathbb{R}^n} \leq \left \Vert{v}\right \Vert_p \leq \delta^{-1}   \left \Vert{v}\right \Vert_{\mathbb{R}^n} ;\]
in particular, the lengths of curves in $M$ are necessarily comparable to the usual lengths in $\mathbb{R}^n$.  The result now follows.

## Related concepts

* [[signature of a metric]]

* [[invariant Riemannian metric]]

* [[orthogonal structure]]

* [[Riemannian manifold]], [[pseudo-Riemannian manifold]]

* [[Levi-Civita connection]]

* [[moduli space of Riemannian metrics]]

## References

An introduction in terms of [[synthetic differential geometry]] is in 

* [[Gonzalo Reyes]], _Metrics, connections and curvature_ ([pdf](http://po-start.com/reyes/wp-content/uploads/2007/01/metrics.pdf))


[[!redirects Riemannian metrics]]

[[!redirects metric tensor]]
[[!redirects metric tensors]]
