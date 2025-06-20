# Spaces stratified by a poset

* table of contents
{:toc}

## Idea

A **poset-stratified space** is a particular way to define a [[stratified space]] that is convenient for some purposes.

## Definition

A **poset-stratified space** is a continuous map $X\to P$, where $X$ is an arbitrary topological space and $P$ is a $T_0$ [[Alexandroff space]], i.e. a [[poset]] with the Alexandroff topology.

The category of stratified spaces is a full subcategory of the [[arrow category]] of [[Top]].  Note that Alexandroff topologies embed [[Pos]] fully-faithfully in [[Top]], so a map of stratified spaces consists of a continuous map $X\to Y$ and a poset map $P\to Q$ making a square commute.

## Examples

* The *cone* on a stratified space $X\to P$ is the quotient $X\times [0,1) / X\times \{0\}$, stratified by the poset $P^\lhd$ that adjoins a new bottom element to $P$.

* The standard stratification of the $n$-simplex $\Delta^n$ is obtained by regarding it as the $(n+1)$-fold cone of $\emptyset$.  It is stratified by the poset $[n] = \{0,\dots,n\}$.  Note that every stratified map $\Delta^n \to \Delta^m$ has an underlying poset map $[n]\to [m]$; it is a theorem the resulting map $Strat(\Delta^n,\Delta^m) \to Pos([n],[m])$ is a homotopy equivalence.  Thus, we have an embedding of the [[simplex category]] into $Strat$.

* Any manifold $M$ can be equipped with the trivial stratification over the terminal poset.  As a special case, the *extended simplices* $\Delta^n_e = \{ \vec{t} \in \mathbb{R}^{n+1} : \sum t_i = 1\}$ assemble into a cosimplicial object $\Delta^\bullet_e \in cStrat$.

## Conically smooth atlases and the $\infty$-category $Strat$

There is a notion of a *conically smooth atlas* on a stratified space.  (The definition is quite involved, inducting on a number of parameters simultaneously; see ([Ayala--Francis--Tanaka, section 3](#AFT)).)  The category of conically smooth stratified spaces (with conically smooth maps among them) is often again simply called $Strat$.

One can endow this new category $Strat$ with an enrichment in Kan complexes via the extended simplices, by defining $\mathrm{map}_{Strat}(X,Y)_\bullet = \mathrm{hom}_{Strat}(X \times \Delta^\bullet_e,Y)$.  This presents the $\infty$-categorical localization $\mathcal{S}trat$ of $Strat$ at the _stratified homotopy equivalences_ (see ([Ayala--Francis--Rozenblyum, Theorem 2.4.5](#AFRshh))).

## Exit path $\infty$-categories


For a stratified space $X$, its **exit path $\infty$-category** is a [[simplicial space]] (in the $\infty$-categorical sense) defined by 

$$Exit(X)_p = \hom_{\mathcal{S}trat}(\Delta^p,X)$$

using the above embedding of $\Delta$ into $Strat$.  It is proven in [Ayala-Francis-Rozenblyum](#AFRshh) that this is indeed a [[complete Segal space]].  The main result of that paper is the [[stratified homotopy hypothesis]], which is the assertion that this construction defines a fully-faithful embedding $Exit : \mathcal{S}trat \hookrightarrow Cat_\infty$, and that certain sheaves on  $\mathcal{S}$trat, known as **striation** sheaves, are equivalent to $(\infty, 1)$-categories.

## Related concepts

* [[stratified category]]

## References

* [[Jacob Lurie]], [[Higher Algebra]], Appendix A.5

* {#AFT} [[David Ayala]], [[John Francis]], [[Hiro Lee Tanaka]], *Local structures on stratified spaces*, [arXiv](http://arxiv.org/abs/1409.0501)

* [[David Ayala]], [[John Francis]], [[Nick Rozenblyum]], *Factorization homology from higher categories*, [arXiv](http://arxiv.org/abs/1504.04007)

* {#AFRshh} [[David Ayala]], [[John Francis]], [[Nick Rozenblyum]], *A stratified homotopy hypothesis*, [arXiv](http://arxiv.org/abs/1502.01713)

* [[Peter J. Haine]], _On the homotopy theory of stratified spaces_ ([arXiv:1811.01119](https://arxiv.org/abs/1811.01119))


whilst an earlier paper on exit paths is

* [[David Treumann]], *Exit paths and constructible stacks*, Compositio Math.145 (2009), 1504&#8211;1532. ([arXiv:0708.0659](https://arxiv.org/abs/0708.0659)). ([doi](https://doi.org/10.1112/S0010437X09004229)).

[[!redirects poset-stratified spaces]]