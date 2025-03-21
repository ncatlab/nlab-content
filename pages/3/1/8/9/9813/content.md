
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Motivic cohomology
+--{: .hide}
[[!include motivic cohomology - contents]]
=--
=--
=--



#Contents#
* table of contents
{:toc}

## Definition

The [[category]] of _effective [[pure motives|pure]] Chow [[motive]]s_ , $Mot_{rat}^{eff}(k)$, is the [[idempotent completion]] of the [[category]] $Corr_{rat}(k)$ whose [[objects]] are [[smooth variety|smooth]] [[projective varieties]] over some [[field]] $k$, and whose [[hom-sets]] are [[Chow groups]] in the [[product]] of two varietes (see for instance [Vishik09, def. 2.1](#Vishik09)).

$$
  Hom_{Corr_{rat}(k)}(Y,X) \coloneqq CH^{dim X}(X \times Y)
  \,.
$$

Hence a [[morphism]] $X \to Y$ in $Mor_{rat}^{eff}(k)$ is an [[equivalence class]] of [[linear combinations]] of [[correspondences]]/[[spans]] of the form

$$
  X \leftarrow \Sigma \rightarrow Y
  \,.
$$

If one furthermore inverts the [[Lefschetz motive]] $\mathbf{L}$ then one obtains the category of _pure Chow motives_

$$
  Mot_{rat}(k) \coloneqq Mot_{rat}^{eff}(k)[\mathbf{L}^{-1}]
  \,.
$$

This was introduced by [[Grothendieck]]. See e.g. ([Vishik09, p. 6](#Vishik09)), ([Mazza-Voevodsky-Weibel, p. 181](#MazzaVoevodskyWeibel)).

This is a special case of the more general notion of _[[pure motives]]_. See there for more.

## Properties

### Relation to Voevodsky motives

There is a [[full and faithful functor]] from the category of Chow motives into that of [[Voevodsky motives]]:

$$
  Chow^{eff} \hookrightarrow DM^{eff}
  \,.
$$

(e.g [Mazza-Voevodsky-Weibel, prop. 20.1](#MazzaVoevodskyWeibel))

### Relation to noncommutative Chow motives

The relation between Chow motives and [[noncommutative Chow motives]] is recalled as theorem 4.6 in ([Tabuada 11](#Tabuada11)).

This relation is best understood via _[[K-motives]]_, see there.

### Relation to KK-theory

The definition of Chow motives in algebraic geometry is somewhat analogous to the construction of [[KK-theory]] in [[noncommutative topology]]. See at _[KK-theory -- Relation to motives](http://ncatlab.org/nlab/show/KK-theory#AsAnAnalogOfMotives)_.

## Related concepts

* [[pure motive]]

  * **Chow motive**

  * [[numerical motive]]

* [[motivic cohomology]]

* [[category of spans]]

## References

A quick and complete statement of the definition is in

* Alexander Vishik, _Chow groups and motives_, lecture notes 2009 ([pdf](http://alg-geo.epfl.ch/cours/geomthqf_vishik_09/docs/D2.pdf))
 {#Vishik09}

See also

* [[Carlo Mazza]], [[Vladimir Voevodsky]] and [[Charles Weibel]], _Lectures in motivic cohomology_ ([web](http://math.rutgers.edu/~weibel/motiviclectures.html) [pdf](http://www.math.rutgers.edu/~weibel/MVWnotes/prova-hyperlink.pdf))
 {#MazzaVoevodskyWeibel}

A review of [[noncommutative Chow motives]] is in section 4 of 

* [[Goncalo Tabuada]], _A guided tour through the garden of noncommutative motives_, ([arxiv1108.3787](http://arxiv.org/abs/1108.3787));
 {#Tabuada11} 

Discussion of how the [[triangulated categories of sheaves|derived category]] of a [[scheme]] determines its commutative and [[noncommutative motive|noncommutative]] Chow motive is in 

* [[Adeel Khan]], _On derived categories and noncommutative motives of varieties_, [arXiv](http://arxiv.org/abs/1401.7222).

[[!redirects Chow motives]]
[[!redirects category of Chow motives]]