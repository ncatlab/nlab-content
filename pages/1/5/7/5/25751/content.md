
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Category theory
+-- {: .hide}
[[!include category theory - contents]]
=--
#### Enriched category theory
+--{: .hide}
[[!include enriched category theory contents]]
=--
=--
=--


#Contents#
* table of contents
{: toc}

## Idea

The notion of **locally graded category** is a joint generalisation of [[enriched categories]], [[actegories]], and [[powered and copowered categories|powered categories]]. The idea is that we grade the [[morphisms]] of a category by a [[monoidal category]] $V$ in such a way that [[identity morphisms]] have grade labeled by the [[unit object]] $I$ and the [[composition|composite]] of morphisms is graded by the [[tensor product]] of the separate grades.

## Definition

Let $(V, \otimes, I)$ be a [[monoidal category]]. For small $V$, a **locally $V$-graded category** is a [[enriched category|category enriched]] over the [[presheaf category]] $([V^{op}, Set], \widehat\otimes, y_V)$, regarded with its [[monoidal category|monoidal]] [[structure]] given by [[Day convolution]].

Explicitly, a locally $V$-graded category $C$ comprises:

- a [[class]] $|C|$ of [[objects]]
- for all $v \in V$ and $c, c' \in |C|$, a [[set]] $C_v(c, c')$ of $v$-graded morphisms
- for every $v$-graded morphism $f : c \to c'$ and $p : v' \to v$, a $v'$-graded morphism $p^* f : c \to c'$
- a $I$-graded [[identity morphism]] $1_c$ for each object $c \in |C|$
- a $v \otimes v'$-graded composite morphism $g f \colon c \to c''$ for each $v$-graded morphism $f \colon c \to c'$ and $v'$-graded morphism $g \colon c' \to c''$

satisfying evident laws.

## Locally indexed categories

The presheaf category $[V^{op}, Set]$ is also [[cartesian monoidal category|cartesian monoidal]]. A category enriched in $([V^{op}, Set], \times, 1)$ is called **locally $V$-indexed** by [Levy (2019)](#Levy19).

When $V$ is [[cartesian monoidal category|cartesian monoidal]], the two concepts coincide ([Levy 2019](#Levy19)). 

As we have stated the definitions, this is trivial, but both concepts have more elementary reformulations that avoid [[size issues]], for which this is a nontrivial theorem.

For example, with [Levy (2019), slide 21](#Levy19) this gives an abstract proof of the standard fact that [[simplicially enriched categories]] can be viewed as those [[simplicial objects]] in [[Cat]] which take value in [[identity-on-objects functors]] (e.g. [Riehl (2023), Prop. 1.2.3](#Riehl23)).

## References

Locally graded categories were introduced as **large $V$-categories** in:

* [[Richard Wood]], *Indicial methods for relative categories*, PhD thesis (1976) &lbrack;[hdl:10222/55465](http://hdl.handle.net/10222/55465)&rbrack;

* [[Richard Wood]],  *$V$-indexed categories*, in *Indexed Categories and Their Applications*, Lecture Notes in Mathematics **661** (1978) 126-140 &lbrack;[doi:10.1007/BFb0061362](https://link.springer.com/chapter/10.1007/BFb0061362)&rbrack;

See also 

* [[Richard Wood]], *re: module for a category*, message to [[categories mailing list]] (2003) &lbrack;[link](https://github.com/punkdit/categories/blob/26b751bbcbe6765fe447e805629ff6416f4c38b1/gmane/science/mathematics/categories/2425)&rbrack;

For the terminology we use see:

* {#Levy19} [[Paul Blain Levy]], *Locally graded categories*, talk (2019) &lbrack;slides:[pdf](https://www.cs.bham.ac.uk/~pbl/papers/locgrade.pdf), [[Levy-LocallyGradedCategories.pdf:file]]&rbrack;

* [[Dylan McDermott]], [[Tarmo Uustalu]], _Flexibly graded monads and graded algebras_, in: *Mathematics of Program Construction MPC 2022*, Lecture Notes in Computer Science **13544**, Springer (2022) &lbrack;[doi:10.1007/978-3-031-16912-0_4](https://dl.acm.org/doi/abs/10.1007/978-3-031-16912-0_4)&rbrack;

For the example of [[simplicially enriched category]] example see for instance:

* {#Riehl18} [[Emily Riehl]], Prop. 1.2.3 in: _Homotopy coherent structures_, Expositions in Theory and Applications of Categories, **1** (2023) 1-31 &lbrack;[arXiv:1801.07404](https://arxiv.org/abs/1801.07404), [tac:te1](http://www.tac.mta.ca/tac//expositions/articles/1/te1abs.html)&rbrack;

A generalisation of locally graded categories to skew-enrichment may be found in the following under the name **skew-proactegories**:

* [[Alexander Campbell]], _Skew-enriched categories_, Applied Categorical Structures 26.3 (2018): 597-615.


[[!redirects locally graded categories]]
[[!redirects locally indexed category]]
[[!redirects locally indexed categories]]