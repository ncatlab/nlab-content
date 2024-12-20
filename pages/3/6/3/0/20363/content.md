
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

> Topological spaces formalize the idea of spaces with a notion of "nearness" of points. However, they fail to handle the idea of "points that are infinitely near, but distinct" in a useful way. Condensed sets handle this idea in a useful way. ([Scholze 21](#Scholze21))

For instance, $\mathbb{R}/\mathbb{Q}$ and $\ell^2(\mathbb{N})/\ell^1(\mathbb{N})$ are indiscrete as topological spaces but retain structure as condensed sets.

Condensed sets contain information about limits of images of any set, $A$, along the [[ultrafilters]] of $A$.


## Definition


\begin{definition}

A _condensed set_ is a [[sheaf]] of [[sets]] on the [[pro-étale site]] of a point — in other words, on the [[category]] of [[profinite spaces]] with finite jointly [[surjective]] families of maps as [[covers]] — that is the [[colimit]] of a [[small diagram]] of [[representables]] (a [[small sheaf]]).

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

For any uncountable [[strong limit cardinal]] $\kappa$, the category of _$\kappa$-condensed sets_ $CondSet_\kappa$ is the [[category of sheaves]] on the [[site]] of profinite sets of [[cardinality]] less than $\kappa$, with finite jointly surjective families of maps as covers. 

The category of condensed sets $CondSet$ is then the (large) [[colimit]] of the category of $\kappa$-condensed sets along the [[filtered category|filtered]] [[poset]] of all uncountable [[strong limit cardinals]] $\kappa$, hence is the category of [[small sheaves]].

Another possible way to deal with set theoretic issue is presented in [Analytic Stacks](#ClausenScholze23).

The category of **light profinite sets** is the full subcategory of $ProfiniteSet$ consisting of countable sequential limits of finite sets. 
The category of **light condensed sets** $LightCondSet$ is the [[category of sheaves]] on the [[site]] of light profinite sets with finite jointly surjective families of maps as covers. 

## Equivalence of sites

Several different [[sites]] can be used to define [[condensed sets]], and, more generally, condensed [[∞-groupoids]]:

* [[compact Hausdorff spaces]];

* [[Stone spaces]] (compact Hausdorff [[totally disconnected spaces]]);

* [[Stonean spaces]] (compact Hausdorff [[extremally disconnected spaces]]).

In all three cases, morphisms are given by continuous maps and covering families are given by finite families of jointly surjective continuous maps.

The equivalence of sites is established in [Yamazaki](#Yamazaki). See also [Proposition 2.3, 2.7](#ScholzeLCM).

The category of _light_ profinite sets is also equivalent to the opposite of the category of countable [[Boolean algebras]] ([Clausen-Scholze 2023](#ClausenScholze23), Lecture 2).

## Properties

Condensed sets form a [[locally small]], [[well-powered category|well-powered]], [[locally cartesian closed]] [infinitary-pretopos](pretopos#infinitary) $CondSet$, that is neither a [[Grothendieck topos]] nor an [[elementary topos]] -- since it lacks both a small [[separator]] (indeed, it is not even [[total category|total]]) and a [[subobject classifier]]. It has a large [[separator]] of finitely presentable [[projective object|projectives]], and hence is algebraically exact. ([Campbell 20](#Campbell20)) In [a talk](#Campbell21) by [[Alexander Campbell]], it is claimed that the category of condensed sets is the [infinitary-pretopos](pretopos#infinitary) completion of the [[pretopos]] of [[compact Hausdorff spaces]].

According to [[Peter Scholze]] in [this comment on the nCafé](https://golem.ph.utexas.edu/category/2020/03/pyknoticity_versus_cohesivenes.html#c057798) and [[Mike Shulman]] in [this comment on the nCafé](https://golem.ph.utexas.edu/category/2020/03/pyknoticity_versus_cohesivenes.html#c057792), condensed sets satisfy external [[CoSHEP]] and [[WISC]], but internal CoSHEP fails. 

See [Proposition 1.7](#ScholzeLCM) for the following proposition.

\begin{proposition}
The [[forgetful functor]]
from the category of [[topological spaces]]
to κ-condensed sets is a [[faithful functor]].
It becomes [[fully faithful]] when restricted
to κ-[[compactly generated spaces]].

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

For the category of _light_ condensed sets, there is a functor that reflects back onto the category of [[sequential topological spaces]]

## Related concepts

* [[pyknotic set]]

* [[light condensed set]]

* [[pro-étale site]]

* [[profinite set]]

* [[condensed infinity-groupoid]]

* [[condensed abelian group]]

* [[condensed mathematics]]


## References

* {#ScholzeLCM} [[Peter Scholze]], _Lectures on condensed mathematics_, [pdf](https://www.math.uni-bonn.de/people/scholze/Condensed.pdf)
* {#ScholzeLAG} [[Peter Scholze]], _Lectures on analytic geometry_, [pdf](https://www.math.uni-bonn.de/people/scholze/Analytic.pdf)
* {#DustinScholze20}[[Dustin Clausen]], [[Peter Scholze]], _Masterclass in condensed mathematics,_ [YouTube playlist](https://www.youtube.com/playlist?list=PLAMniZX5MiiLXPrD4mpZ-O9oiwhev-5Uq), [website](https://www.math.ku.dk/english/calendar/events/condensed-mathematics/) (including pdf notes)
* {#Scholze21} [[Peter Scholze]], Math Stack Exchange [answer](https://math.stackexchange.com/a/4199337/368788).
* {#Campbell20} [[Alexander Campbell]], _How nice is the category of condensed sets?_, [talk abstract](https://centre-of-australian-category-theory.github.io/seminar/talks/1632).
* {#Campbell21} [[Alexander Campbell]], _The universal property of the category of condensed sets_, [talk abstract](https://maths.anu.edu.au/news-events/events/universal-property-category-condensed-sets)
* {#ClausenScholze23}[[Dustin Clausen]], [[Peter Scholze]], _Analytic Stacks,_ [YouTube playlist](https://www.youtube.com/playlist?list=PLx5f8IelFRgGmu6gmL-Kf_Rl_6Mm7juZO), [website](https://indico.math.cnrs.fr/event/10345/)

The equivalence of various sites for condensed sets is established in

* {#Yamazaki} Koji Yamazaki, _Condensed Sets on Compact Hausdorff Spaces_, [arXiv:2211.13855](https://arxiv.org/abs/2211.13855).

[[!redirects condensed sets]]
[[!redirects CondSet]]
