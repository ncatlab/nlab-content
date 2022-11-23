

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

A _Galois representation_ is a [[linear representation]] of a [[Galois group]] (often the [[absolute Galois group]] of some [[field]]). In other words, given a [[field extension]] $E$ of $F$, and a [[vector space]] $V$ over some field $k$, a Galois representation $\rho$ is a [[group homomorphism]]

$$\rho:\Gal(E/F)\to \GL(V)$$

where $\GL(V)$ is the group of [[linear transformations]] of $V$. If $V$ is an $n$-dimensional vector space, $\GL(V)$ is the same as the [[general linear group]] $\GL_{n}(k)$. A [[Galois module]] is a generalization of a Galois representation to [[modules]] instead of vector spaces.

## Continuous Galois representations

When the Galois group is the [[absolute Galois group]] of a [[number field]] or a finite extension of the [[p-adic numbers]], and the field of scalars of the underlying vector space of the representation is a [[topological field]], one often considers continuous Galois representations (noting that the absolute Galois group is a [[topological group]]).

## Examples

An example of a continuous Galois representation can be obtained by taking the $\ell$-adic Tate module as discussed in the article on [[Galois modules]] and taking its tensor product with $\mathbb{Q}_{\ell}$.

## p-adic Galois representations

Continuous Galois representations of $\mathrm{Gal}(\overline{F}/F)$, where $F$ is a finite extension of the [[p-adic numbers]] $\mathbb{Q}_{p}$, over an underlying vector space over $E$, where $E$ is another extension of $\mathbb{Q}_{p}$ (often with some condition that $E$ is big enough) are called _p-adic Galois representations_ (in contrast to $\ell$-adic Galois representations, where the underlying vector space is over some extension of $\mathbb{Q}_{\ell}$, where $\ell$ is another prime not equal to $p$). p-adic Galois representations have a very rich theory (significantly richer and more complicated than $\ell$-adic Galois representations), and their study is part of [[p-adic Hodge theory]].

## Conjectures on Galois Representations

### Fontaine-Mazur Conjecture

The Fontaine-Mazur conjecture gives a criterion for when an $\ell$-adic Galois representation "comes from geometry", i.e. is obtained from the $\ell$-adic [[etale cohomology]] of a variety. Namely, a Galois representation comes from geometry if and only if it is unramified at almost all places, and de Rham (see [[p-adic Hodge theory]]) at the places over $\ell$ ([LiLFunctions](#LiLFunctions)).

### Langlands Correspondence

A restricted version of the global [[Langlands correspondence]] ([BuzzardMSRI](#BuzzardMSRI)) for $\GL_{n}$ states that algebraic automorphic representations of $\GL_{n}$ over $\mathbb{Q}$ are in bijection with compatible systems of $\ell$-adic Galois representations. A more general form is conjectured for number fields instead of $\mathbb{Q}$.

The [[local Langlands correspondence]] for $\GL_{n}$ states that irreducible admissible representations of $\GL_{n}(\mathbb{Q}_{p})$ are in correspondence with F-semisimple [[Weil-Deligne representations]] of $\Gal(\overline{\mathbb{Q}_{p}}/\mathbb{Q}_{p})$. This has been proved. A more general form is also true for more general local fields instead of $\mathbb{Q}_{p}$.

For reductive groups other than $\GL_{n}$, Galois representations need to be replaced by the more general concept of [[L-parameters]] (and the statement becomes a classification, in terms of a partition into L-packets, rather than a bijection).

### Serre's Modularity Conjecture

_Serre's modularity conjecture_ states that an odd (this means the image of complex conjugation has determinant $-1$) irreducible two-dimensional Galois representation over a [[finite field]] comes from a [[modular form]], and furthermore (in its strong form) gives a recipe for the level and weight of the modular form as well. This conjecture was proved by Khare and Wintenberger in [KhareWintenberger09a](#KhareWintenberger09a) and [KhareWintenberger09b](#KhareWintenberger09b).

## Related concepts

* [[class field theory]]

* [[etale cohomology]]

* [[Galois cohomology]]

* [[p-adic Hodge theory]]

* [[Langlands correspondence]]

## References

* [[Richard Taylor]], _Galois representations_ ([pdf](http://www.math.ias.edu/~rtaylor/longicm02.pdf))

In the context of the Langlands program:

* {#BuzzardMSRI} Kevin Buzzard, _MSRI Summer School on automorphic forms_ ([web](http://wwwf.imperial.ac.uk/~buzzard/MSRI/))

The statement of the Fontaine-Mazur conjecture as stated in this article comes from

* {#LiLFunctions} Chao Li, _Arithmetic of L-Functions_ (notes taken by Pak-Hin Lee) ([pdf](http://www.math.columbia.edu/~phlee/CourseNotes/L-functions.pdf))

The proof of Serre's modularity conjecture is given in

* {#KhareWintenberger09a} Khare, Chandrashekhar; Wintenberger, Jean-Pierre (2009), _Serre's modularity conjecture (I)_, Inventiones Mathematicae, 178 (3): 485–504

* {#KhareWintenberger09b} Khare, Chandrashekhar; Wintenberger, Jean-Pierre (2009), "Serre's modularity conjecture (II)", Inventiones Mathematicae, 178 (3): 505–586

Review of the fact that Galois representations encode [[local systems]] are are hence analogs in [[arithmetic geometry]] of [[flat connections]] in [[differential geometry]] includes

* {#Lovering} Tom Lovering, _&#201;tale cohomology and Galois Representations_, 2012 ([pdf](http://tlovering.files.wordpress.com/2012/06/essay-body1.pdf))

See also at _[[function field analogy]]_.

[[!redirects Galois representations]]
