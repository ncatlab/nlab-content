
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

Condensed sets are basic objects in [[condensed mathematics]], whose aim is to provide a convenient setting
in the framework for working with [[algebra|algebraic]] objects that are equipped with sort of a [[topological space|topology]]. A related alternative is provided by [[pyknotic sets]].

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

[Scholze, p.7](#ScholzeLCM) modifies this definition to deal with size issues: 

For any uncountable [[strong limit cardinal]] $\kappa$, the category of _$\kappa$-condensed sets_ is the [[category of sheaves]] on the [[site]] of profinite sets of [[cardinality]] less than $\kappa$, with finite jointly surjective families of maps as covers. 

The category of condensed sets is then the (large) [[colimit]] of the category of $\kappa$-condensed sets along the [[filtered category|filtered]] [[poset]] of all uncountable [[strong limit cardinals]] $\kappa$, hence is the category of [[small sheaves]].

## Properties

Condensed sets form a [[pretopos]].

See \cite[Proposition 1.7]{ScholzeLCM} for the following proposition.

\begin{proposition}
The [[forgetful functor]]
from the category of [[topological spaces]]
to condensed sets is a [[faithful functor]].
It becomes [[fully faithful]] when restricted
to [[compactly generated spaces]].
(In the case of κ-condensed sets, one must take κ-compactly generated
spaces instead.)

This functor admits a left adjoint,
which sends a condensed set $T$
to the [[topological space]] given by the underlying set $T(*)$ of $T$
equipped with the [[quotient topology]] induced by the map
$$\coprod_{S\to T}S\to T(*),$$
where $S$ runs over all (κ-small) [[profinite sets]] mapping into $T$.
The [[counit]] of this adjunction coincides with the counit $X^{cg}\to X$
of the adjunction between (κ-small) [[compactly generated spaces]]
and [[topological spaces]].
\end{proposition}

The left adjoint exists also for topological groups and other algebraic
structures, but in this case, the underlying set is not $T(*)$.

## Related concepts

* [[pyknotic set]]

* [[pro-étale site]]

* [[profinite set]]

* [[condensed mathematics]]

## References

* {#ScholzeLCM} [[Peter Scholze]], _Lectures on condensed mathematics_, [pdf](https://www.math.uni-bonn.de/people/scholze/Condensed.pdf)
* {#ScholzeLAG} [[Peter Scholze]], _Lectures on analytic geometry_, [pdf](https://www.math.uni-bonn.de/people/scholze/Analytic.pdf)
* {#DustinScholze20}[[Dustin Clausen]], [[Peter Scholze]], _Masterclass in condensed mathematics,_ [YouTube playlist](https://www.youtube.com/playlist?list=PLAMniZX5MiiLXPrD4mpZ-O9oiwhev-5Uq), [website](https://www.math.ku.dk/english/calendar/events/condensed-mathematics/) (including pdf notes)


[[!redirects condensed sets]]

