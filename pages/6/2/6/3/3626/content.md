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

Frobenius algebras were originally formulated in the category of vector spaces with the following equivalent definition:

+-- {: .num_defn}
###### Definition
A **Frobenius algebra** is a unital, associative algebra $(A, \mu, \eta)$ equipped with a linear form $\epsilon : A \rightarrow k$ such that $\epsilon\mu$ is a non-degenerate pairing. I.e. the induced map

\[  u \mapsto \epsilon\mu(1 \otimes u) \]

is an isomorphism of $V$ with its dual space $V^*$. In such a case, $\epsilon$ is called a **Frobenius form**.
=--

From this definition it is easy to see that every Frobenius algebra in [[Vect]] is necessarily finite-dimensional.

There are about a dozen equivalent definitions of a Frobenius algebra. Ross Street lists most of them here:

* R. Street, Frobenius monads and pseudomonoids, _J. Math. Phys._ **45** (2004).  ([web](http://citeseerx.ist.psu.edu/viewdoc/summary?doi=10.1.1.91.2686))

## Types of Frobenius Algebras

We can define 'commutative' or 'symmetric' Frobenius algebras in any [[symmetric monoidal category]].  Namely, a Frobenius algebra is **commutative** if its associated monoid is commutative --- or equivalently, if its associated comonoid is cocommutative.  A Frobenius algebra $A$ is **symmetric** if 
$$\epsilon S_{A,A} = \epsilon \, $$
where $S_{A,A} : A \otimes A \to A \otimes A$ is the symmetry.  Any commutative Frobenius algebra is symmetric, but not conversely: for example the algebra of $n \times n$ matrices with entries in a field, with its usual trace as $\epsilon$, is symmetric but not commutative when $n \gt 1$.  A theorem of Eilenberg and Nakayama says that in the category of vector spaces over a field $k$, an algebra can be equipped with the structure of a symmetric Frobenius algebra if and only if it is **separable**, meaning that for any field $K$ extending $k$, $A \otimes_k K$ is a [[semisimple algebra|semisimple]] algebra over $K$.  

If a Frobenius algebra lives in a monoidal [[†-category]], $(\delta)^\dagger = \mu$ and $(\epsilon)^\dagger = \eta$, then it is said to be a **&#8224;-Frobenius algebra**. These crop up in the theory of 2d [[TQFTs]], and also in the foundations of [[quantum mechanics in terms of dagger-compact categories|quantum theory]].

If $\mu \circ \delta = 1$, a Frobenius algebra is said to be **special**.  

Frobenius algebras also have nice [[PROPs]]. The PROP for a commutative Frobenius algebra is 2Cob and the PROP for a special commutative Frobenius algebra is Span(FinSet).

In some sense, special commutative Frobenius algebras are dual to commutative [[bialgebra|bialgebras]], whose PROP is Cospan(FinSet).

[[!redirects Frobenius algebras]]