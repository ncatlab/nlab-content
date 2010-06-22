
#Contents#
* automatic table of contents goes here
{:toc}

## Defintion

For $f \in C^\infty(\mathbb{R})$ a [[smooth function]] with $n$th [[derivative]] $f^{(n)} \in C^\infty(\mathbb{R})$, its **Taylor series** (at 0) is the [[power series]]

$$
  \sum_{n = 0}^\infty \frac{1}{n!} f^{(n)}(0) x^n
$$


Similarly for functions on any [[Cartesian space]] or [[smooth manifold]].

## Properties

+-- {: .un_theorem}
###### Theorem
**(Borel's theorem)**

The morphism

$$
  C^\infty(\mathbb{R}^{k+l})
  \to
  C^\infty(\mathbb{R}^k) [ [ X_1, \cdots X_l] ]
$$

obtained by forming Taylor series in $l$ variables is surjective.

=--

In particular, every [[power series]] in $\mathbb{R}[ [ X] ]$ is the taylor series of some [[smooth function]] on the [[real line]].


+-- {: .proof}
###### Proof

The proof is reproduced for instance in [[Models for Smooth Infinitesimal Analysis|MSIA, I, 1.3]]

=--

[[!redirects Taylor series expansion]]