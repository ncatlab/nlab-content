
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### $\infty$-Chern-Weil theory
+--{: .hide}
[[!include infinity-Chern-Weil theory - contents]]
=--
#### Differential cohomology
+--{: .hide}
[[!include differential cohomology - contents]]
=--
#### Index theory
+-- {: .hide}
[[!include index theory - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

The _Chern-Gauss-Bonnet theorem_ gives a formula that computes the [[Euler characteristic]] of an even-[[dimension]]al [[smooth manifold]] as the [[integration]] of a [[curvature characteristic form]] of the [[Levi-Civita connection]] on its [[tangent bundle]].

For [[surface]]s the theorem simplifies and in this simpler version is the older _Gauss-Bonnet theorem_ .

## Statement

### For surfaces

(...)

### For smooth manifolds

+-- {: .num_theorem}
###### Theorem

Let $X$ be a [[compact space|compact]] [[smooth manifold]] of even [[dimension]] $dim X = 2k$. Write $\chi(X)$ for its [[Euler characteristic]].

For $\nabla$ any [[Levi-Civita connection]] on its [[tangent bundle]], write $F_\nabla$ for its [[curvature]] [[differential form|2-form]], valued in the [[orthogonal Lie algebra]] $\mathfrak{so}(2k)$ and $Pf(F_\nabla)$ for its [[Pfaffian]] $2k$-form.

Then 

$$
  \chi(X) = 
  \left(
    \frac{-1}{2 \pi}
  \right)^{k}
  \int_X Pf(F_\nabla)
  \,.
$$

=--

### For orbifolds

There is a generalization for $X$ an [[orbifold]] due to ([Satake](#Satake)).


## Related concepts

* [[Euler characteristic]]

* [[Euler form]]

* [[Poincaré–Hopf theorem]]

## References

Named after [[Carl Friedrich Gauss]].

The Chern-Gauss-Bonnet theorem goes back to 

* [[ Shiing-shen Chern]], _A Simple Intrinsic Proof of the Gauss-Bonnet Formula for Closed Riemannian Manifolds_ , Annals, 45 (1944), 747-752.

A classical textbook reference is chapter X of volume II of

* [[Werner Greub]], [[Stephen Halperin]], [[Ray Vanstone]], _[[Connections, Curvature, and Cohomology]]_ Academic Press (1973)


Discussion is for instance in 

* Denis Bell, _The Gauss-Bonnet theorem for vector bundles_ ([pdf](http://www.unf.edu/~dbell/GBT.pdf))

Expositions include

* [[Liviu Nicolaescu]], _The many faces of the Gauss-Bonnet theorem_ ([pdf](http://www.nd.edu/~lnicolae/GradStudSemFall2003.pdf))

* Denis Bell, _The Gauss-Bonnet theorem_ ([pdf](http://www.unf.edu/~dbell/GBVB.pdf))

* [[Chenchang Zhu]], _The Gauss-Bonnet theorem and its applications_ ([pdf](http://math.berkeley.edu/~alanw/240papers00/zhu.pdf))

* [[Johannes Ebert]], _[MO comment](http://mathoverflow.net/questions/53302/is-there-a-chern-gauss-bonnet-theorem-for-orbifolds/53351#53351)_


The generalization to [[orbifold]]s is considered in

* {#Satake} [[Ichiro Satake]], _The Gauss-Bonnet Theorem for V-manifolds_ J. Math. Soc. Japan Volume 9, Number 4 (1957), 464-492.  ([ProjectEclid](http://projecteuclid.org/euclid.jmsj/1261153826))
 

Generalization to [[orbifolds]]:

* Christopher Seaton, _Two Gauss–Bonnet and Poincaré–Hopf theorems for orbifolds with boundary_, Differential Geometry and its Applications
Volume 26, Issue 1, February 2008, Pages 42-51 ([doi:10.1016/j.difgeo.2007.11.002](https://doi.org/10.1016/j.difgeo.2007.11.002))


For an approach via 0|2-dimensional [[supersymmetric Euclidean field theory]], see

* [[Daniel Berwick-Evans]], _The Chern-Gauss-Bonnet Theorem via supersymmetric Euclidean field theories_, Communications in Mathematical Physics, Volume 335 (2015), ([arXiv:1310.5383](https://arxiv.org/abs/1310.5383)).

[[!redirects Chern-Gauss-Bonnet theorem]]
[[!redirects Gauss-Bonnet density]]
