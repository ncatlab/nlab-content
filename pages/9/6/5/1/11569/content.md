
> Not to be confused with *[[completion of a group]]*.

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Algebra
+--{: .hide}
[[!include higher algebra - contents]]
=--
#### Group Theory
+-- {: .hide}
[[!include group theory - contents]]
=--
#### Monoid theory
+-- {: .hide}
[[!include monoid theory - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

The [[forgetful functor]] $U$ from [[abelian groups]] to [[commutative monoids]] has a [[left adjoint]] $G$. This is called _group completion_.
A standard presentation of the group completion is the *[[Grothendieck group of a commutative monoid]]*. As such group completion plays a central role in the definition of [[K-theory]].


More generally in [[(∞,1)-category theory]] and [[higher algebra]] there is 
the [[left adjoint|left]] [[adjoint (∞,1)-functor]] 

$$
  K \;\colon\;  CMon_\infty(\infty Grpd) \longrightarrow AbGrp_\infty(\infty Grpd)
$$

to the inclusion of [[abelian ∞-groups]] ([[connective spectra]]) into [[commutative ∞-monoids]] in [[∞Grpd]] ([[E-∞ spaces]]). This may be called _$\infty$-group completion_.

This serves to define [[algebraic K-theory of symmetric monoidal (∞,1)-categories]].

In [[algebraic topology]] a key role was played by models of this process at least on [[H-spaces]] ([Quillen 71](#Quillen71), [May, def. 1.3](#May)). If $N$ is a [[topological monoid]], let $B N$ denotes its [[bar construction]] ("[[classifying space]]") and $\Omega B N$ the [[loop space]] of that. Then this 
$$
  N \longrightarrow \Omega B N
$$
represents the group completion of $N$ ([Quillen 71, section 9](#Quillen71), [May, theorem  1.6](#May)). This crucially enters the construction of the [[K-theory of a permutative category]].

According to ([Dwyer-Kan 80, prop. 3.7, prop. 9.2, remark 9.7](#DwyerKan80)) this indeed gives a model for the total [[derived functor]] of 1-categorical group completion.

## Examples

* [[group-completed configuration space of points]]


## Related concepts

* [[Grothendieck group]]

* [[localization of a monoid]]

## References

Classical accounts:

* {#BarrattPriddy72} [[Michael Barratt]], [[Stewart Priddy]], *On the homology of non-connected monoids and their associated groups*, Commentarii Mathematici Helvetici, **47** 1 (1972) 1–14 &lbrack;[doi:10.1007/BF02566785](https://link.springer.com/article/10.1007/BF02566785), [eudml:139496](https://eudml.org/doc/139496)&rbrack;

  > (on the [[Pontrjagin ring]]-structure under group completion of [[topological monoids]])

* {#Quillen71} [[Daniel Quillen]]: *On the group completion of a simplicial monoid*, Appendix Q in: [[Eric M. Friedlander]], [[Barry Mazur]]: *Filtrations on the homology of algebraic varieties*, Memoirs of the AMS **529** 110 (1994) 89-105 &lbrack;[doi:10.1090/memo/0529](https://doi.org/10.1090/memo/0529), [pdf](http://www.maths.ed.ac.uk/~aar/papers/quillencomp.pdf)&rbrack;

* {#May} [[Peter May]], *$E_\infty$-Spaces, group completions, and permutative categories*, in: *New Developments in Topology*, Cambridge University Press (1974) 61-94  &lbrack;[doi:10.1017/CBO9780511662607.008](https://doi.org/10.1017/CBO9780511662607.008), [pdf](http://www.math.uchicago.edu/~may/PAPERS/13.pdf)&rbrack;

* [[Dusa McDuff]], [[Graeme Segal]]: *Homology fibrations and the “group-completion” theorem*, Inventiones mathematicae **31** (1976) 279-284 &lbrack;[doi:10.1007/BF01403148](https://doi.org/10.1007/BF01403148)&rbrack;

  > (on the [[Pontrjagin ring]]-structure under group completion of [[topological monoids]])

* {#DwyerKan80} [[William Dwyer]], [[Daniel Kan]], _Simplicial localization of categories_, Journal of pure and applied algebra **17** (1980) 267-284

and specifically concerning [[configuration spaces of points]]:

* {#Segal73} [[Graeme Segal]], *Configuration-spaces and iterated loop-spaces*, Invent. Math. **21** (1973) 213-221  &lbrack;[doi:10.1007/BF01390197](https://doi.org/10.1007/BF01390197), [pdf](http://dodo.pdmi.ras.ru/~topology/books/segal.pdf), MR 0331377&rbrack;

* {#Okuyama05} [[Shingo Okuyama]]: *The space of intervals in a Euclidean space*, Algebr. Geom. Topol. **5** (2005) 1555-1572 &lbrack;[arXiv:math/0511645](https://arxiv.org/abs/math/0511645), [doi:10.2140/agt.2005.5.1555](https://doi.org/10.2140/agt.2005.5.1555)&rbrack;

* [[Kazuhisa Shimakawa]]: *Labeled configuration spaces and group completions*, Forum Mathematicum (2007) 353-364 &lbrack;[doi:10.1515/FORUM.2007.014](https://doi.org/10.1515/FORUM.2007.014), [[Shimakawa-ConfigGroupCompletion.pdf:file]]&rbrack;

Discussion of $\infty$-group completion:

* {#BunkeTamme12} [[Ulrich Bunke]], [[Georg Tamme]], section 2.1 of _Regulators and cycle maps in higher-dimensional differential algebraic K-theory_ ([arXiv:1209.6451](http://arxiv.org/abs/1209.6451))

* {#Nikolaus13} [[Thomas Nikolaus]]: _Algebraic K-Theory of $\infty$-Operads_ ([arXiv:1303.2198](http://arxiv.org/abs/1303.2198))

* {#BunkeNikolausVoelkl13} [[Ulrich Bunke]], [[Thomas Nikolaus]], [[Michael Völkl]], def. 6.1 in  _Differential cohomology theories as sheaves of spectra_ ([arXiv:1311.3188](http://arxiv.org/abs/1311.3188))

and specifically its monoidal properties:

* {#GepnerGrothNikolaus13} [[David Gepner]], [[Moritz Groth]], [[Thomas Nikolaus]], _Universality of multiplicative infinite loop space machines_ &lbrack;[arXiv:1305.4550](http://arxiv.org/abs/1305.4550)&rbrack;


[[!redirects group completions]]

[[!redirects ∞-group completion]]
[[!redirects ∞-group completions]]