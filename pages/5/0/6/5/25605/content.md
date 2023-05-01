
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Model category theory
+--{: .hide}
[[!include model category theory - contents]]
=--
#### Enriched category theory
+--{: .hide}
[[!include enriched category theory contents]]
=--
#### Monoidal categories
+--{: .hide}
[[!include monoidal categories - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

A *simplicial monoidal model category* is a [[classical model structure on simplicial sets|$sSet_{Qu}$]]-[[enriched monoidal model category]], namely a [[model category]] equipped with 

1. the [[structure]] of a [[monoidal model category]],

1. the [[structure]] of a [[simplicial model category]],

1. the compatibility structure that makes the [[underlying]] [[monoidal category|monoidal]] and [[sSet-enriched category|sSet-enriched]] structure an 

   [[sSet]]-[[enriched monoidal category]].

## Examples

\begin{example}
  It ought to be true that the [[Bousfield localization of model categories|Bousfield localization]] at the "realization equivalences" (see [this Prop.](model+structure+on+chain+complexes#MonoidalSimplicialEnhancementOfUnboundedChainModelStructure)) of the [[Reedy model structure]] on [[simplicial objects]] in [[chain complexes]] is simplicial monoidal under the objectwise [[tensor product of chain complexes]].
\end{example}

## References

The notion may be implicit in many discussions of [[monoidal model category]] such as used, notably, to build [[symmetric monoidal smash products of spectra]]. One reference making more explicit the need to specify compatibility structure is:

* [[Jacob Lurie]], Def. 4.1.7.8 in *[[Higher Algebra]]* &lbrack;[pdf](https://www.math.ias.edu/~lurie/papers/HA.pdf)&rbrack;

with a precursor in

* [[Jacob Lurie]], Def. 1.6.4 in: *Derived Algebraic Geometry II: Noncommutative Algebra* &lbrack;[arXiv:math/0702299](https://arxiv.org/abs/math/0702299)&rbrack;

but the actual compatibility is maybe not made very explicit there either, for this see the references at *[[enriched monoidal category]]*.


[[!redirects simplicial monoidal model categories]]

[[!redirects monoidal simplicial model category]]


