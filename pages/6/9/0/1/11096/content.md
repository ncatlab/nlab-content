
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Homotopy theory
+--{: .hide}
[[!include homotopy - contents]]
=--
#### Type theory
+-- {: .hide}
[[!include type theory - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

The concept of a [[homotopy type]] ([[homotopy n-type]]) all of whose [[homotopy groups]] are [[finite groups]] does not have an established name. Sometimes it is called _$\pi$-finiteness_. In the context of [[groupoid cardinality]] "tameness" is used. In [[homological algebra]] "of [[finite type]]" is used, which in [[homotopy theory]] however badly clashes with the concept of [[finite homotopy type]] which is crucially different from _homotopy type with finite homotopy groups_. ([Anel 21](#Anel21)) uses "truncated coherent spaces".

## Properties

### (Co-)Limits indexed by homotopy types with finite homotopy groups

see at _[[K(n)-local stable homotopy theory]]_ (...)

### Relation to coherent objects
 {#RelationToCoherentObjects}

+-- {: .num_prop }
###### Proposition

[[∞Grpd]] is a [[coherent (∞,1)-topos]] and a [[locally coherent (∞,1)-topos]]. An [[object]] $X$, hence an [[∞-groupoid]], is an [[n-coherent object]] precisely if all its [[homotopy groups]] in degree $k \leq n$ are [[finite set|finite]]. Hence the fully coherent objects here are the homotopy types with finite homotopy groups.

=--

([[Spectral Schemes|Lurie SpecSchm, example 3.13]])

+-- {: .num_prop }
###### Proposition
The $(\infty, 1)$-category of homotopy types with finite homotopy groups is the initial [[(∞,1)-pretopos]].


=--

([Anel 21, Theorem 2.6.6](#Anel21)).


### Codensity monad of the inclusion into all homotopy types
 {#CodensityMonadOfInclusionIntoAllHomotopyTypes}

The inclusion of homotopy types with finite groups into all homotopy types generates a [[codensity monad]] whose algebras lie somewhere between [[totally disconnected]] compact Hausdorff [[condensed mathematics|condensed]] $\infty$-groupoids, and all compact Hausdorff condensed $\infty$-groupoids. (See [Scholze](#Scholze) for more details.)



## References

* G. J. Ellis, _Spaces with finitely many non-trivial homotopy groups all of which are finite_, Topology, 36, (1997), 501&#8211;504, ISSN 0040-9383.

* [[Jean-Louis Loday]], _Spaces with finitely many non-trivial homotopy groups_ (<a href="http://www-irma.u-strasbg.fr/~loday/PAPERS/82Loday(Spaces).pdf">pdf</a>)

* {#Scholze} [[Peter Scholze]], _Infinity-categorical analogue of compact Hausdorff_, [MO answer](https://mathoverflow.net/a/380399/447)

Discussion as an [[elementary (∞,1)-topos]]:

* {#Anel21} [[Mathieu Anel]], _The elementary infinity-topos of truncated coherent spaces_ ([arXiv:2107.02082](https://arxiv.org/abs/2107.02082))

[[!redirects homotopy types with finite homotopy groups]]

[[!redirects tame homotopy type]]
[[!redirects tame homotopy types]]