
#Contents#
* table of contents
{:toc}

## Idea

The perturbation of the [[differential]] in the passage from a [[classical BV-complex]] to a [[quantum BV-complex]] is called a _BV-Laplacian_. As discussed at _[[BV-complex]]_ the BV Laplacian is a [[homological algebra|homological]] incarnation of a [[measure]].

## Examples

In the archetypical example of the BV-complex of a [[smooth manifold]] of finite [[dimension]] $n$ and equipped with a [[volume form]] $vol$, the BV-Laplacian is the operation on [[multivector fields]] which is the image of the [[de Rham differential]] under the [[isomorphism]] between [[multivector fields]] and [[differential forms]] induced by contraction with the [[volume form]].

Specifically over a [[Cartesian space]] $\mathbb{R}^n$ with its canonical volume form and with $\{x^i, \xi_i\}$ the canonical [[basis]] elements of the algebra of multivectorfields, the BV-Laplacian has the expression

$$
  \Delta = \sum_{i = 1}^n \frac{\partial}{ \partial x^i} \frac{\partial}{\partial \xi_i}
$$

(it [[differentiation|differentiates]] the function and "removes a vector field" for each derivative, being the dual operation to "wedging with $d x^i$").

## Related concepts

[[BV-BRST formalism]]

* [[antifield]]

* [[ghost]]

[[!include action (physics) - table]]


## References

See at _[[BV-BRST formalism]]_ for general references.

Discussion of the BV-operation in [[renormalization]] and [[effective field theory]] is in section 10.1 of

* [[Kevin Costello]], _Renormalisation and the Batalin-Vilkovisky formalism_ ([arXiv:0706.1533](http://arxiv.org/abs/0706.1533))

[[!redirects BV Laplacian]]

[[!redirects BV operator]]
[[!redirects BV-operator]]
