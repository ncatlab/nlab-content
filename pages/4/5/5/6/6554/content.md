
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

For $(X,g)$ a [[Riemannian manifold]] and $f : X \to \mathbb{R}$ a [[smooth function]], let 

$$
  \nabla f := g^{-1}(d_{dR} f) \in \Gamma(T X)
$$

be the [[gradient]] [[vector field]] of $X$. The [[flow]] induced by this on $X$ is the **gradient flow** of $f$.

## Examples


* [[Yang-Mills instanton]]s are the gradient flow trajectories of the [[Chern-Simons action functional]].

* [[Ricci flow]] is the gradient flow of the [[action functional]] of [[dilaton gravity]]. 

  (This is a key part of Perelman's proof of the [[Poincare conjecture]].)

* the learning algorithm of a [[neural network]] is a gradient descent for the loss function ([Thierry-Mieg 18](neural+network#ThierryMieg18))

## References

* Philippe Cl&#233;ment, _Introduction to Gradient Flows in Metric Spaces (II)_ ([pdf](https://igk.math.uni-bielefeld.de/sites/default/files/study_materials/notes2.pdf))

[[!redirects gradient flows]]

[[!redirects gradient descent]]