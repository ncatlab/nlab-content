+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Algebra
+--{: .hide}
[[!include higher algebra - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

The idea of cancellative midpoint algebras is due to [Freyd 2008](#Freyd08).

## Definition

A __cancellative midpoint algebra__ is a [[midpoint algebra]] $(M,\vert)$ that satisfies the following *cancellativity* property: 

* for all $a$, $b$, and $c$ in $M$, if $a \vert b = a \vert c$, then $b = c$

## Examples

The [[rational numbers]], [[real numbers]], and the [[complex numbers]] with $a \vert b \coloneqq \frac{a + b}{2}$ are examples of cancellative midpoint algebras. 

In general, if $(M,\vert)$ forms a [[quasigroup]] and not just a [[cancellative monoid|cancellative]] [[magma]], then a unique $Z[1/2]$-[[module]] characterizes it. ([proof](https://frank-9976.github.io/midpoint.html))

The [[trivial group]] with $a \vert b = a \cdot b$ is a cancellative midpoint algebra.

[Escardó & Simpson 2001](#EscardóSimpson01) describe examples of this algebraic structure over many other [[categories]] besides [[Set]].

## Related concepts

* [[midpoint algebra]]

* [[symmetric cancellative midpoint algebra]]

* [[closed midpoint algebra]]

## References

* {#Freyd08} [[Peter Freyd]], *Algebraic real analysis*, Theory and Applications of Categories **20** 10 (2008) 215-306 &lbrack;[tac:20-10](http://www.tac.mta.ca/tac/volumes/20/10/20-10abs.html)&rbrack;

* {#EscardóSimpson01} [[Martín Escardó]] and [[Alex Simpson]]; *A universal characterization of the closed Euclidean interval*, in *16th Annual IEEE Symposium on Logic in Computer Science, Boston, Massachusetts, USA, June 16-19*, IEEE Computer Society (2001) 115–125
&lbrack;[doi:10.1109/LICS.2001.932488](https://doi.org/10.1109/LICS.2001.932488), [pdf](http://www.cs.bham.ac.uk/~mhe/papers/interval.pdf)&rbrack;

[[!redirects cancellative midpoint algebras]]


