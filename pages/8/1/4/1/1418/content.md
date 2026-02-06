
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Category theory
+-- {: .hide}
[[!include category theory - contents]]
=--
#### Compact objects
+-- {: .hide}
[[!include compact object - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Definition


+-- {: .num_defn}
###### Definition

A **locally finitely presentable category** is an [[ℵ]]${}_0$-[[locally presentable category]].

=--

We spell out what this means:


An [[object]] $X$ of a [[category]] $C$ is said to be [[finitely presentable object|finitely presentable]] (sometimes called [[compact object|compact]] or 'finite') if the [[representable functor]] $C(X,-)$ is finitary, i.e., preserves [[filtered colimits]]. Write $C_{fp}$ for the full subcategory of $C$ consisting of the finitely presentable objects.


A category $C$ satisfying (any of) the following equivalent conditions is said to be __locally finitely presentable__ (or **lfp**):

1. $C$ is the [[free cocompletion]] of a [[small category|small]] [[finitely cocomplete category]] under [[filtered colimits]]: see [[ind-object]].
1. $C$ has all small [[colimit|colimits]], the category $C_{fp}$ is [[essentially small category|essentially small]], and any object in $C$ is a [[filtered colimit]] of the canonical diagram of finitely presentable objects mapping into it.
1. $C$ is the category of models for an [[essentially algebraic theory]].  Here an 'essentially algebraic theory' is a small category $D$ with finite limits, and its category of 'models' is the category of finite-limit-preserving functors $D \to Set$. (See [[Gabriel--Ulmer duality]].)
1. $C$ is the category of models for a finite limit [[sketch]].
1. $C_{fp}$ has finite colimits, and the restricted [[Yoneda embedding]] $C\hookrightarrow [C_{fp}^{op},Set]$ identifies $C$ with the category of finite-limit-preserving functors $C_{fp}^{op} \to Set$.

Replacing "finite" by "of cardinality less than $\kappa$" everywhere, for some [[cardinal number]] $\kappa$, results in the notion of a [[locally presentable category]].

## Examples

* [[Set]], Graph, [[Pos]], [[Cat]], [[Ab]] are all lfp.

* [[Top]], [[FinSet]] are not lfp.

## Related pages

* [[locally strongly finitely presentable category]]
* [[accessible category]]

## References

* P. Gabriel, F. Ulmer, _Lokal präsentierbare Kategorien_, Springer Lect. Notes in Math. __221__ 1971 [Zbl0225.18004](https://zbmath.org/?q=an:0225.18004) [MR327863](https://mathscinet.ams.org/mathscinet-getitem?mr=327863)
* Jiří Adámek, Jiří Rosicky, _Locally presentable and accessible categories_, Cambridge University Press 1994.

Introductory account:

* [[Maru Sarazola]], *An introduction to locally finitely presentable categories* (2017) &lbrack;[pdf](https://pi.math.cornell.edu/~maru/documents/locally_finitely_presentable_cats.pdf), [[Sarazola_LocallyPresentableCategories.pdf:file]]&rbrack;


In additive context

* [[Henning Krause]], _Functors on locally finitely presented additive categories_, Colloq. Math. 75:1 (1998) [pdf](http://matwbn.icm.edu.pl/ksiazki/cm/cm75/cm75110.pdf)

If $V$ is a locally finitely presentable symmetric monoidal closed category then there is a bijection between exact $V$-localizations of the $V$-category of $V$-valued $V$-enriched presheaves on a $V$-category $C$
and $V$-enriched Grothendieck topologies on $C$: 

* [[Francis Borceux]], Carmen Quinteiro, _A theory of enriched sheaves_, Cahiers Topologie Géom. Différentielle Catég. 37 (1996), no. 2, 145–162 [numdam](https://eudml.org/doc/91577) [MR1394507](https://mathscinet.ams.org/mathscinet-getitem?mr=1394507)
[[!redirects locally finitely presentable categories]]
[[!redirects lfp category]]
[[!redirects lfp categories]]

[[!redirects finitely presentable category]]
[[!redirects finitely presentable categories]]
