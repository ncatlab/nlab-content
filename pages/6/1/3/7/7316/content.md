
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Monoidal categories
+--{: .hide}
[[!include monoidal categories - contents]]
=--
#### Category theory
+--{: .hide}
[[!include category theory - contents]]
=--
=--
=--


\tableofcontents

## Idea

Opfibrations of multicategories are the generalization of _[[Grothendieck opfibrations]]_ from [[categories]] to [[multicategories]].


## Properties

### Relation to algebras over an operad

For a [[multicategory]] regarded as a ([[planar operad|non-symmetric]]) [[operad]], discrete opfibrations over it are equivalent to [[algebra over an operad|algebras over that operad]] ([Hermida, proposition 5.1](#Hermida)).

For [[symmetric multicategories]] we have the following. 
Let $P$ be a [[symmetric operad]] over [[Set]]


+-- {: .num_theorem}
###### Theorem

The [[operadic Grothendieck construction]] induces an [[equivalence of 2-categories]]

$$
  Alg_P(Cat)
  \simeq
  opFib_P
$$

between the [[∞-algebra over an (∞,1)-operad|weak]] [[algebra over an operad|algebras over]] $P$ and op-fibrations over $P$.

=--

This is ([Heuts, theorem 1.6](#Heuts)).

### Relation to representable multicategories

Opfibrations over the [[terminal object|terminal]] multicategory are equivalently [[representable multicategories]] ([Hermida, corollary 4.3](#Hermida)).

## Related concepts

- [[fibration of multicategories]]
- The generalization to the context of [[(∞,1)-operads]] is given by the notion of [[Cartesian fibration of dendroidal sets]].

## References

On opfibrations of planar [[multicategories]]:

* {#Hermida} [[Claudio Hermida]], _Fibrations for abstract multicategories_, Fields Institute Communications &lbrack;[[Hermida-FibsForMulticats.pdf:file]]&rbrack;
 
For [[symmetric multicategories]] a discussion of (op)fibrations and of the operadic [[Grothendieck construction]] is in:

* {#Heuts} [[Gijs Heuts]], section 1 of: _Algebras over infinity-operads_ &lbrack;[arXiv:1110.1776](http://arxiv.org/abs/1110.1776)&rbrack;
  

[[!redirects opfibrations of multicategories]]