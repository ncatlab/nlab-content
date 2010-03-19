# Frobenius algebras
* table of contents
{: toc}


## Definition

+-- {: .num_defn}
###### Definition
A Frobenius algebra in a [[monoidal category]] is a quadruple $(A, \delta, \epsilon, \mu, \eta)$ such that

1. $(A, \mu, \eta)$ is a [[monoid]],
1. $(A, \delta, \epsilon)$ is a [[comonoid]], and
1. $(1 \otimes \mu) \circ (\delta \otimes 1) = \delta \circ \mu = (\mu \otimes 1) \circ (1 \otimes \delta)$.
=--

Frobenius algebras were originally formulated in vector spaces with the following equivalent definition.

+-- {: .num_defn}
###### Definition
For a vector space $V$ a Frobenius algebra over $V$ is a unital, associative algebra $(\mu, \eta)$ equipped with a linear form $\epsilon : V \rightarrow k$ such that $\epsilon\mu$ is a non-degenerate pairing. I.e. the induced map

\[ \widehat{\epsilon\mu} :: u \mapsto \epsilon\mu(1 \otimes u) \]

is an isomorphism of $V$ with its dual space $V^*$. In such a case, $\epsilon$ is called a Frobenius form.
=--

There are about a dozen equivalent definitions of a Frobenius algebra. Ross Street lists most of them in

* R. Street. Frobenius monads and pseudomonoids. J. Math. Phys. Vol 45 (10). 2004

## Types of Frobenius Algebras

If the associated monoid and comonoid are commutative (resp. cocommutative), then the Frobenius algebra is said to be commutative. If it lives in a [[†-category]], $(\delta)^\dagger = \mu$ and $(\epsilon)^\dagger = \eta$ then it is said to be a &#8224;-Frobenius algebra. These crop up when studying 2D [[TQFTs]]. If $\mu \circ \delta = 1$, a Frobenius algebra is said to be _special_.

Frobenius algebras also have nice [[PROPs]]. The PROP for a commutative Frobenius algebra is 2Cob and the PROP for a special commutative Frobenius algebra is Span(FinSet).

In some sense, special commutative Frobenius algebras are the dual structure of commutative [[bialgebra|bialgebras]], whose PROP is Cospan(FinSet).



