

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

Modern formulations of the weight part of Serre's conjecture are stated differently, inspired by the observation by Ash and Stevens ([AshStevens86](#AshStevens86)) that a Galois representation over a finite field is modular of prime-to-$p$ level $N$ and weight $k$ if and only if the corresponding system of Hecke eigenvalues appears in the [[group cohomology]] $H^1(\Gamma(N),\Sym^{k-2}\overline{\mathbb{F}}_{p}^{2})$. This is the same as requiring that the system of Hecke eigenvalues appears in $H^{1}(\Gamma(N),V)$, where $V$ is a Jordan-Holder factor of $\Sym^{k-2}\overline{\mathbb{F}}_{p}^{2}$.

Therefore, modern formulations of the weight part of Serre's conjecture consists of associating to a Galois representation over a finite field $\mathbb{F}_{p}$ a set of _Serre weights_, which are irreducible $\overline{\mathbb{F}}_{p}$ representations of $\GL_{2}(\mathbb{F}_{p})$ (there are also generalizations to other groups). See also [GHS18](#GHS18) for more discussion of this point of view.

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

The modern formulation of the weight part of Serre's conjecture is discussed in

* {#GHS18} [[Toby Gee]], [[Florian Herzig]], [[David Savitt]], _General Serre Weight Conjectures_, J. Eur. Math. Soc. 20 (2018), no. 12, 2859-2949 ([arXiv:1509.02527](https://arxiv.org/abs/1509.02527))

The historical inspiration for the previous entry can be found in 

* {#AshStevens86} Avner Ash and Glenn Stevens, _Modular forms in characteristic l and special values of their L-functions_, Duke Math. J. 53 (1986), no. 3, 849–868. 

Review of the fact that Galois representations encode [[local systems]] are are hence analogs in [[arithmetic geometry]] of [[flat connections]] in [[differential geometry]] includes

* {#Lovering} Tom Lovering, _&#201;tale cohomology and Galois Representations_, 2012 ([pdf](http://tlovering.files.wordpress.com/2012/06/essay-body1.pdf))

See also at _[[function field analogy]]_.

* [[Peter Scholze]], _Locally symmetric spaces, and Galois representations_, Harvard CMD conference 2015, [yt](https://www.youtube.com/watch?v=4NCk8ItLMR0)

[[!redirects Galois representations]]
