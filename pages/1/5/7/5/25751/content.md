* table of contents
{: toc}

## Idea

The notion of **locally graded category** is a joint generalisation of [[enriched categories]], [[actegories]], and [[powered and copowered categories|powered categories]]. The idea is that we grade the morphisms of a category by a monoidal category $V$ in such a way that identity morphisms have grade $I$ and the composite of morphisms corresponds to taking the tensor product of the grades.

## Definition

Let $(V, \otimes, I)$ be a [[monoidal category]]. A **locally $V$-graded category** is a category enriched in the [[presheaf category]] $([V^{op}, Set], \widehat\otimes, y_V)$, which is monoidal under [[Day convolution]].

## Locally indexed categories

The presheaf category $[V^{op}, Set]$ is also [[cartesian monoidal category|cartesian monoidal]]. A category enriched in $([V^{op}, Set], \times, 1)$ is called **locally $V$-indexed** by [Levy](#Levy).

When $V$ is [[cartesian monoidal category|cartesian monoidal]], the two concepts coincide ([Levy](#Levy)). (As we have stated the definitions, this is trivial, but both concepts have more elementary reformulations that avoid [[size issues]], for which this is a nontrivial theorem.)

This gives an abstract proof of the fact that [[simplicially enriched categories]] can be viewed as [[functors]] into the category of [[small categories]] and [[identity-on-objects functors]] (see Proposition 1.2.3 of [Riehl](#Riehl)).

## References

Locally graded categories were introduced as **large $V$-categories** by [[Richard Wood]] in his thesis:

* _Indical methods for relative categories_, [[Richard Wood]], 1976

* _V-indexed categories_, [[Richard Wood]], 1978, *Indexed Categories and Their Applications*, ([Springer](https://link.springer.com/chapter/10.1007/BFb0061362))

See also a post by [[Richard Wood]] on the [[categories mailing list]]: [link](https://github.com/punkdit/categories/blob/26b751bbcbe6765fe447e805629ff6416f4c38b1/gmane/science/mathematics/categories/2425).

For the terminology we use see:

{#Levy} * _Locally graded categories_, a 2019 talk by [[Paul Levy]], ([slides](https://www.cs.bham.ac.uk/~pbl/papers/locgrade.pdf))

* [[Dylan McDermott]], [[Tarmo Uustalu]]. _Flexibly graded monads and graded algebras_, in: *Mathematics of Program Construction MPC 2022*, Lecture Notes in Computer Science **13544**, Springer (2022) &lbrack;[doi:10.1007/978-3-031-16912-0_4](https://doi.org/10.1007/978-3-031-16912-0_4)&rbrack;

For the [[simplicially enriched category]] example, see:

* [[Emily Riehl]]. _Homotopy coherent structures_, [arXiv:1801.07404](https://arxiv.org/abs/1801.07404) (2018).

[[!redirects locally graded categories]]
[[!redirects locally indexed category]]
[[!redirects locally indexed categories]]