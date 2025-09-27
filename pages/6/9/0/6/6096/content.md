
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Quantum field theory
+--{: .hide}
[[!include functorial quantum field theory - contents]]
=--
=--
=--

\tableofcontents

## Idea

A _homological_ [[TQFT]] is a representation of (meaning: [[functor]] on, cf. *[[functorial QFT]])*) a [[cobordism category]] that depends only on the [[homology]] of the [[hom-spaces]].

In $d = 2$ this is also called a _homological [[conformal field theory]]*. The passage to homology forgets the conformal structure.
The refinement of this concept from [[homology groups]] to [[chain complexes]] is called *[[TCFT]]*.


## Definition

Write $Bord$ for any given [[cobordism category]], regarded as a [[Top]]-[[enriched category]]. A **homological TQFT** is a [[symmetric monoidal functor|symmetric monoidal]] [[Ab]]-[[enriched functor]]

$$
  Z \colon H_\bullet(Bord) \to Ab
  \,.
$$

## Examples

* The [[string topology]] operations of a manifold are part of an HTQFT. See [there](string+topology#InTermsOfTQFTs) for details.


## References

For 2-dimensional cobordisms without boundary:

* {#Godin} [[Veronique Godin]]: *Higher string topology operations* (2007) &lbrack;[arXiv:0711.4859](http://arxiv.org/abs/0711.4859)&rbrack;
 
and generalized to arbitrary sets of boundary labels/[[branes]]:

* {#Kupers11} [[Sander Kupers]]: *HCFTs with and without branes*, chapter 2 of: *String topology operations*, MS thesis, Utrecht (2011) &lbrack;[hdl:20.500.12932/7283](https://studenttheses.uu.nl/handle/20.500.12932/7283), [[Kupers-StringTopology.pdf:file]]&rbrack;

[[!redirects HCFT]]
[[!redirects HCFTs]]

[[!redirects HQFT]]
[[!redirects HQFTs]]
