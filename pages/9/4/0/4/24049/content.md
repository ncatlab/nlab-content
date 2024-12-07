+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Higher geometry
+--{: .hide}
[[!include higher geometry - contents]]
=--
#### Topology
+--{: .hide}
[[!include topology - contents]]
=--
#### $(\infty,1)$-Category theory
+--{: .hide}
[[!include quasi-category theory contents]]
=--
#### Higher category theory
+--{: .hide}
[[!include higher category theory - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

The original motivation behind condensed infinity-groupoids is to create well-behaved categories of mathematical structures such as condensed [[HZ]]-[[module spectra]] in which one could do derived analytic geometry using category-theoretic methods without resorting to not-so-well behaved categories of topological spaces. 

However, [[David Corfield]] offers another motivation for condensed infinity-groupoids in the blog post [Pyknoticity vs Cohesiveness](https://golem.ph.utexas.edu/category/2020/03/pyknoticity_versus_cohesivenes.html#c057721) on the nCafé, as a way to extend [[cohesion]] to the $p$-adic case (see at [[condensed cohesion]]): 

> Mathematics rather than physics is the subject of chapter 5 of my book, where I’m presenting [[cohesive homotopy type theory|cohesive HoTT]] as a means to gain some kind of conceptual traction over the vast terrain that is modern geometry. However I’m aware that there are some apparent limitations, problems with ‘$p$-adic’ forms of cohesion, cohesion in algebraic geometry, and so on. In the briefest note (p. 158) I mention the closely related pyknotic and condensed approaches of, respectively, (Barwick and Haine) and (Clausen and Scholze).

## Definition

A **condensed infinity-groupoid** or **condensed anima** is a [[hypercomplete (infinity,1)-topos | hypercomplete]] [[(infinity,1)-sheaf]] of [[infinity-groupoids]] on the [[pro-étale (infinity,1)-site]] of the point, small relative to a universe $\mathcal{U}$. 

Equivalently, it is an [[(infinity,1)-functor]] 

$$T:ProfiniteSpaces^\op \longrightarrow \infty Grpd_\mathcal{U}$$

from the [[opposite category|opposite]] [[(infinity,1)-category]] of [[profinite spaces]] to the [[(infinity,1)-category]] [[Infinity-Grpd]] of [[infinity-groupoids]] which are small relative to a [[universe]] $\mathcal{U}$, such that the natural maps

$$T(\mathbb{0}) \to \mathbb{1}$$

and 

$$T(S + S^{'}) \to T(S) \times T(S^{'})$$

are [[homotopy equivalences]] for any profinite space $S$ and $S^{'}$, and the natural map 

$$T(S) \to  \operatorname{lim}_{\Delta} T(S_\bullet)$$

is a [[homotopy equivalence]] for any [[hypercover]] of profinite spaces $S_\bullet \to S$. 

When restricted to the site of [[extremally disconnected topological space | extremally disconnected]] compact Hausdorff spaces, hyperdescent is automatic, so the simplest equivalent definition of a condensed infinity-groupoid is simply a finite-product-preserving [[(infinity,1)-functor]] $T:ExtrDisc^\op \longrightarrow \infty Grpd_\mathcal{U}$, see ([Barwick-Haine, corollary 2.4.4](#BarwickHaine19)).

## Properties

The [[(infinity,1)-category]] 
$\mathrm{Cond}\infty\mathrm{Grpd}$ of condensed infinity-groupoids is a locally small [[locally cartesian closed (infinity,1)-category|locally cartesian closed]] [[(infinity,1)-pretopos]]. 

[[Peter Scholze]] speculates in [this comment on the nCafé](https://golem.ph.utexas.edu/category/2020/03/pyknoticity_versus_cohesivenes.html#c057721) that $\mathrm{Cond}\infty\mathrm{Grpd}$ seem to form a [[predicative elementary (infinity,1)-topos]]. If true, then $\mathrm{Cond}\infty\mathrm{Grpd}$ is an example of an [[elementary (infinity,1)-topos]] which is not a [[Grothendieck (infinity,1)-topos]]. 

## Terminology

In the model of [[infinity-groupoids]] as [[simplicial sets]]/[[Kan complexes]], condensed infinity-groupoids are sometimes referred to as **condensed anima**. 

## Related concepts

* [[condensed mathematics]]
* [[condensed set]]
* [[condensed spectrum]]
* [[condensed E-infinity ring]]
* [[condensed module spectrum]]

## References

* {#Corfield20} [[David Corfield]], _Modal homotopy type theory_, Oxford University Press 2020 ([ISBN: 9780198853404](https://global.oup.com/academic/product/modal-homotopy-type-theory-9780198853404))

* {#BarwickHaine19} [[Clark Barwick]], [[Peter Haine]], _Pyknotic objects, I. Basic notions_, ([arXiv:1904.09966](https://arxiv.org/abs/1904.09966)

* {#Zhu23} [[Qi Zhu]], *Fractured Structure on Condensed Anima*, MSc thesis (2023) &lbrack;[pdf](https://1429cecd-24a0-4223-8b7c-1ebf47aa12e2.filesusr.com/ugd/8e912a_fe1c2f8e90094d0fa065fb8129687963.pdf), [[QiZhu-FracturedCondensed.pdf:file]]&rbrack;

See [[condensed mathematics]] and [[infinity-groupoid#Anima]]. 

[[!redirects condensed infinity-groupoid]]
[[!redirects condensed infinity-groupoids]]
[[!redirects condensed anima]]
[[!redirects condensed ∞-groupoids]]
[[!redirects condensed ∞-groupoid]]

[[!redirects pyknotic infinity-groupoid]]
[[!redirects pyknotic infinity-groupoids]]
[[!redirects pyknotic anima]]
[[!redirects pyknotic ∞-groupoids]]
[[!redirects pyknotic ∞-groupoid]]
