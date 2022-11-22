
> should be merged with _[[Galois module]]_

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Representation theory
+-- {: .hide}
[[!include representation theory - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

A _Galois representation_ is a [[Galois module]] on a [[vector space]].

See at _[[Galois modules]]_ for more.

## Continuous Galois representations

When the Galois group is the [[absolute Galois group]] of a [[number field]] or a finite extension of the [[p-adic numbers]], and the field of scalars of the underlying vector space of the representation is a [[topological field]], one often considers continuous Galois representations (noting that the absolute Galois group is a [[topological group]]).

## Examples

An example of a continuous Galois representation can be obtained by taking the $\ell$-adic Tate module as discussed in the article on [[Galois modules]] and taking its tensor product with $\mathbb{Q}_{\ell}$.

## p-adic Galois representations

Continuous Galois representations of $\mathrm{Gal}(\overline{F}/F)$, where $F$ is a finite extension of $\mathbb{Q}_{p}$, over an underlying vector space over $E$, where $E$ is another extension of $\mathbb{Q}_{p}$ (often with some condition that $E$ is big enough) are called _p-adic Galois representations_ (in contrast to $\ell$-adic Galois representations, where the underlying vector space is over some extension of $\mathbb{Q}_{\ell}$, where $\ell$ is another prime not equal to $p$). p-adic Galois representations have a very rich theory (significantly richer and more complicated than $\ell$-adic Galois representations), and their study is part of [[p-adic Hodge theory]].

## Conjectures on Galois Representations

### Fontaine-Mazur Conjecture

The Fontaine-Mazur conjecture gives a criterion for when an $\ell$-adic Galois representation "comes from geometry", i.e. is obtained from the [[$\ell$-adic cohomology]] of a variety. Namely, a Galois representation comes from geometry if and only if it is unramified at almost all places, and de Rham (see [[p-adic Hodge theory]]) at the places over $\ell$ ([LiLFunctions](#LiLFunctions)).

### Langlands Correspondence

A restricted version of the global [[Langlands correspondence]] ([BuzzardMSRI](#BuzzardMSRI)) for $\GL_{n}$ states that algebraic automorphic representations of $\GL_{n}$ over $\mathbb{Q}$ are in bijection with compatible systems of $\ell$-adic Galois representations. A more general form is conjectured for number fields instead of $\mathbb{Q}$.

The [[local Langlands correspondence]] for $\GL_{n}$ states that irreducible admissible representations of $\GL_{n}(\mathbb{Q}_{p})$ are in correspondence with F-semisimple [[Weil-Deligne representations]] of $\Gal(\overline{\mathbb{Q}_{p}}/\mathbb{Q}_{p})$. This has been proved. A more general form is also true for more general local fields instead of $\mathbb{Q}_{p}$.

For reductive groups other than $\GL_{n}$, Galois representations need to be replaced by the more general concept of [[L-parameters]] (and the statement becomes a classification, in terms of a partition into L-packets, rather than a bijection).

## Related concepts

* [[class field theory]]

* [[p-adic Hodge theory]]

* [[Langlands correspondence]]

## References

* [[Richard Taylor]], _Galois representations_ ([pdf](http://www.math.ias.edu/~rtaylor/longicm02.pdf))

In the context of the Langlands program:

* {#BuzzardMSRI} Kevin Buzzard, _MSRI Summer School on automorphic forms_ ([web](http://wwwf.imperial.ac.uk/~buzzard/MSRI/))

The statement of the Fontaine-Mazur conjecture as stated in this article comes from

* {#LiLFunctions} Chao Li, _Arithmetic of L-Functions_ (notes taken by Pak-Hin Lee) ([pdf](http://www.math.columbia.edu/~phlee/CourseNotes/L-functions.pdf))

Review of the fact that Galois representations encode [[local systems]] are are hence analogs in [[arithmetic geometry]] of [[flat connections]] in [[differential geometry]] includes

* {#Lovering} Tom Lovering, _&#201;tale cohomology and Galois Representations_, 2012 ([pdf](http://tlovering.files.wordpress.com/2012/06/essay-body1.pdf))

See also at _[[function field analogy]]_.

[[!redirects Galois representations]]
