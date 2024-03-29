
#Contents#
* table of contents
{:toc}

## Idea

The _product law_ or _product rule_ or _[[Leibniz]] rule_ of [[differentiation]] says that for $f,g : X \to \mathbb{R}$ two [[differentiable functions]] and $f g$ their (pointwise) product the [[derivative]] of their product is

$$
  d (f g) = (d f) g + f (d g)
  \,.
$$

Generalized to [[differential forms]] the product law says that $d$ is a [[derivation]] of degree +1 on the [[graded commutative algebra]] of differential forms:

$$
  d (f \wedge g) = (d f) \wedge g + (-1)^{\deg f} f \wedge (d g)
  \,
$$

if $f$ is homogeneous. 

## Categorification 

One categorified form of the product rule occurs in the theory of [[species]]. Let $V$ be a [[symmetric monoidal category]] with finite [[coproducts]] over which the tensor product [[preserved limit|distributes]], and let $FB$ be the [[core]] [[groupoid]] consisting of [[finite sets]] and [[bijections]]. Recall the [[Day convolution|convolution product]] for species $F, G: FB \to V$ is given by the formula 

$$(F \otimes G)[S] = \sum_{S = T + U} F[T] \otimes G[U]$$ 

and the derivative of $F$ is given by the formula 

$$F'[S] = F[S \sqcup \{\ast\}].$$ 

Then it is easy to check that the canonical map 

$$F' \otimes G + F \otimes G' \to (F \otimes G)'$$ 

is an [[isomorphism]]. More generally, for any finite set $X$ one can define an $X^{th}$ derivative by the formula 

$$F^{(X)}[S] = F[S + X]$$ 

and then one has a canonical isomorphism 

$$(F \otimes G)^{(X)} \cong \sum_{X = Y + Z} F^{(Y)} \otimes G^{(Z)}$$ 

which is a [[categorification]] of the general product rule 

$$(f \cdot g)^{(n)} = \sum_{n = j + k} \frac{n!}{j! k!} f^{(j)} \cdot g^{(k)}.$$ 

## Related concepts

* [[derivation]]

* [[multiplicative spectral sequence]] 


[[!redirects product law]]
[[!redirects product rule]]
