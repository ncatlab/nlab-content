
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Diagram chasing lemmas
+-- {: .hide}
[[!include diagram chasing lemmas - contents]]
=--
#### Homological algebra
+-- {: .hide}
[[!include homological algebra - contents]]
=--
=--
=--
#Contents#
* table of contents
{:toc}

## Idea

A basic [[lemma]] in [[homological algebra]]: it constructs [[connecting homomorphisms]].

## Statement

+-- {: .num_lemma}
###### Lemma

Let 

$$
  \array{
    && A' &\to & B' &\stackrel{p}{\to}& C' &\to & 0
    \\
    && \downarrow^{\mathrlap{f}} && \downarrow^{\mathrlap{g}} && \downarrow^{\mathrlap{h}}
    \\
    0 &\to& A &\stackrel{i}{\to} & B &\to& C
  }
$$

be a [[commuting diagram]] in an [[abelian category]] $\mathcal{A}$ such that the two rows are [[exact sequences]]. 

Then there is a [[long exact sequence]] of [[kernels]] and [[cokernels]] of the form

$$
  ker(f)  \to ker(g) \to ker(h) \stackrel{\partial}{\to}
  coker(f) \to coker(g) \to coker(h)
  \,.
$$

Moreover

* if $A' \to B'$ is a [[monomorphism]] then so is $ker(f) \to ker(g)$

* if $B \to C$ is an [[epimorphism]], then so is $coker(g) \to coker(h)$.

If $\mathcal{A}$ is [[Freyd-Mitchell embedding theorem|realized]] as a ([[full subcategory]] of) a category of $R$-[[modules]], then the _[[connecting homomorphism]]_ $\partial$ here can be defined on elements $c' \in ker(h) \subset C'$ by

$$
  \partial (c') := i^{-1} \,g\, p^{-1}(c')
  \,,
$$

where $i^{-1}(-)$ and $p^{-1}(-)$ denote any choice of [[pre-image]] (the total formula is independent of that choice).


=--

+-- {: .num_remark}
###### Remark

The snake lemma derives its name from the fact that one may draw the connecting homomorphism $\partial$ that it constructs diagrammatically as follows:

[[SnakeLemma.png:pic]]

=--


## Related concepts

* [[connecting homomorphism]]

* [[salamander lemma]]

* [[3x3 lemma]], [[5-lemma]],

* [[horseshoe lemma]]

## References

An early occurence of the snake lemma is as lemma (5.8) of

* D. A. Buchsbaum, _Exact categories and duality_, Transactions of the American Mathematical Society Vol. 80, No. 1 (1955), pp. 1-34 ([JSTOR](http://www.jstor.org/stable/1993003))

In 

* [[Charles Weibel]], _[[An introduction to homological algebra]]_

it appears as lemma 1.3.2.


A purely [[category theory|category-theoretic]] proof is given in 

* Temple Fay, [[Keith Hardie]], [[Peter Hilton]], _The two-square lemma_, Publicacions Matem&#224;tiques, Vol 33 (1989) ([pdf](http://dmle.cindoc.csic.es/pdf/PUBLICACIONSMATEMATIQUES_1989_33_01_10.pdf))

and in 

* {#Wise} [[Jonathan Wise]], *A non-elementary proof of the snake lemma* (2011, 2023) &lbrack;[pdf](https://math.colorado.edu/%7Ejonathan.wise/papers/snake.pdf), [[Wise-SnakeLemma.pdf:file]], [MO:a/7531](https://mathoverflow.net/a/7531/381)&rbrack;

See also

* Wikipedia, _[Snake lemma](http://secure.wikimedia.org/wikipedia/en/wiki/Snake_lemma)_

