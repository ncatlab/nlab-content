
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


* [[Yang-Mills instantons]] are the gradient flow trajectories of the [[Chern-Simons action functional]].

* [[Ricci flow]] is the gradient flow of the [[action functional]] of [[dilaton gravity]]. 

  (This is a key part of Perelman's proof of the [[Poincare conjecture]].)

* the learning algorithm of a [[neural network]] is a gradient descent for the loss function ([Thierry & Mieg 2018](neural+network#ThierryMieg18))

## References

* Luigi Ambrosio, Nicola Gigli, Giuseppe Savaré: *Gradient Flows -- In Metric Spaces and in the Space of Probability Measures*, Lectures in Mathematics ETH Zürich, Springer (2008) &lbrack;[doi10.1007/978-3-7643-8722-8](https://doi.org/10.1007/978-3-7643-8722-8)&rbrack;

* Philippe Cl&#233;ment, _Introduction to Gradient Flows in Metric Spaces (II)_ ([pdf](https://igk.math.uni-bielefeld.de/sites/default/files/study_materials/notes2.pdf))

See also:

* Wikipedia: *[Gradient descent](https://en.wikipedia.org/wiki/Gradient_descent)*

* Wikipedia: *[Method of steepest descent](https://en.wikipedia.org/wiki/Method_of_steepest_descent)*

[[!redirects gradient flows]]

[[!redirects gradient descent]]

[[!redirects steepest descent]]
