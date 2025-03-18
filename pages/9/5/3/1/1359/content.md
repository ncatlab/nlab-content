
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Homological algebra
+--{: .hide}
[[!include homological algebra - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Definition

Let $C$ be a [[differential graded category]].

A **twisted complex** $E$ in $C$ is

* a [[graded set]] $\{E_i\}_{i \in \mathbb{Z}}$ of [[object]]s of $C$, such that only finitely many $E_i$ are not the [[zero object]];

* a set of [[morphism]]s $\{q_{i j} : E_i \to E_j \}_{i,j \in \mathbb{Z}}$ such that

  * $deg(q_{i j}) = i-j+1$;

  * $\forall i,j : \; d q_{i j} + \sum_{k} q_{k j}\circ q_{i k} = 0$.

The [[differential graded category]] $PreTr(C)$ of twisted complexes in $C$ has as objects twisted complexes and

$$
  PreTr(C)((E_\bullet, q), (E'_\bullet, q'))^k
  =
  \coprod_{l + j - i = k} C(E_i, E'_j)^l
$$

with differential given on $f \in C(E_i, E'_j)^l$ given by

$$
  d f = d_C f + \sum_m (q_{j m}\circ  f + (-1)^{l(i-m+1)} f \circ q_{m i})
  \,.
$$

The construction of categories of twisted complexes is functorial in that for $F : C \to C'$ a dg-functor, there is a dg-functor

$$
  PreTr(F) : PreTr(C) \to PreTr(C')
  \,.
$$

etc.

## Properties

Passing from a [[dg-category]] to its category of twisted complexes is a step towards enhancing it to a [[pretriangulated dg-category]].

## Related concepts

* [[Landau-Ginzburg model]], [[pretriangulated dg-category]]
* {#BondalKapranov90} [[Alexei Bondal]], [[Mikhail Kapranov]], _Enhanced triangulated categories_, &#1052;&#1072;&#1090;&#1077;&#1084;. &#1057;&#1073;&#1086;&#1088;&#1085;&#1080;&#1082;, &#1058;&#1086;&#1084; 181 (1990), No.5, 669&#8211;683 (Russian); transl. in USSR Math. USSR Sbornik, vol. 70 (1991), No. 1, pp. 93&#8211;107, (MR91g:18010) ([[bondalKaprEnhTRiangCat.pdf:file]])
* [[Bernhard Keller]], _A brief introduction to $A_\infty$-algebras_ ([pdf](https://webusers.imj-prg.fr/~bernhard.keller/publ/IntroAinfEdinb.pdf))
* [[Mikhail Kapranov]], Svyatoslav Pimenov, _Derived varieties of complexes and Kostant's theorem for gl(m|n)_,
[arxiv/1504.00339](http://arxiv.org/abs/1504.00339)

[[!redirects twisted complexes]]