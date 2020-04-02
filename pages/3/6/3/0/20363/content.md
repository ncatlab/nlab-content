
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Topology
+--{: .hide}
[[!include topology - contents]]
=--
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

Condensed sets aim to provide a convenient setting
in the framework of [[homotopical algebra]] for working with [[algebra|algebraic]] objects that are equipped with sort of a [[topological space|topology]]. A related alternative is provided by [[pyknotic sets]].

## Definition


\begin{definition}

A _condensed set_ is a [[sheaf]] of [[sets]] on the [[pro-étale site]] of a point — in other words, on the [[category]] of [[profinite spaces]] with finite jointly [[surjective]] families of maps as [[covers]] — which is the [[colimit]] of a [[small diagram]] of [[representables]] (a [[small sheaf]]).

That is, a condensed set is a [[functor]]

$$
  ProfiniteSet^op 
  \longrightarrow
  Set
$$

such that the natural maps

$$
  T(\emptyset)
  \longrightarrow
  *
$$

and

$$
  T(S\sqcup S')
  \longrightarrow
  T(S) \times T(S')
$$

are [[bijections]] for any [[profinite sets]] $S$ and $S'$,
whereas the natural [[fork]]

$$
  T(S)\to T(S')
  \rightrightarrows 
  T(S'\times_S S')
$$

is an [[equalizer]] for any [[surjection]] of [[profinite sets]] $S'\to S$.

\end{definition}


[Scholze, p.7](#Scholze) modifies this definition to deal with size issues: 

For any uncountable [[strong limit cardinal]] $\kappa$, the category of _$\kappa$-condensed sets_ is the [[category of sheaves]] on the [[site]] of profinite sets of [[cardinality]] less than $\kappa$, with finite jointly surjective families of maps as covers. 

The category of condensed sets is then the (large) [[colimit]] of the category of $\kappa$-condensed sets along the [[filtered category|filtered]] [[poset]] of all uncountable [[strong limit cardinals]] $\kappa$, hence is the category of [[small sheaves]].

## Related concepts

* [[pyknotic set]]

* [[pro-étale site]]

* [[profinite set]]

## References

* {#Scholze} [[Peter Scholze]], _Lectures on condensed mathematics_, [PDF](https://www.math.uni-bonn.de/people/scholze/Condensed.pdf)

[[!redirects condensed sets]]
[[!redirects condensed object]]
[[!redirects condensed objects]]
[[!redirects condensed mathematics]]
