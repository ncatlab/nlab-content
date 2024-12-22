
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

\tableofcontents

## Idea

Proposed by [[Peter Scholze]] in the *Analytic Stacks* lectures in 2023 ([Clausen-Scholze 2023](#ClausenScholze23)) as a more well-behaved replacement for [[condensed sets]] and [[pyknotic sets]] in [[condensed mathematics]] that eliminate the size issues in the other two approaches. More specifically, 

* unlike [[condensed sets]], light condensed sets form a [[Grothendieck topos]], rather than merely a [[pretopos]]

* unlike [[pyknotic sets]], light condensed sets do not require [[universes]]

## Definition

Recall that a [[light profinite set]] is a [[countable set|countable]] [[limit]] of [[finite sets]]. A **light condensed set** or **$\aleph_1$-condensed set** is a [[sheaf]] on the [[site]] of [[light profinite sets]] with finite jointly surjective families of maps as covers. 

## Category of light condensed sets

The category of light condensed sets $\mathrm{LightCondSet}$ is a [[Grothendieck topos]]. 

The category of [[sequential topological spaces]] embed fully faithfully into the category of light condensed sets, and there is a functor that reflects the category of light condensed sets back onto the category of [[sequential topological spaces]]. 

### Internal logic

In the [[internal logic]] of the topos of light condensed sets, the [[weak limited principle of omniscience]] (WLPO) for the natural numbers is false (and thus [[excluded middle]] also fails). 

On the other hand, the [[lesser limited principle of omniscience]] (LLPO) does hold in the topos of light condensed sets. [[Markov's principle]] also holds in the topos of light condensed sets, as does the [[fan theorem]]. 

The full [[intermediate value theorem]] and the [[Brouwer's fixed point theorem]] can be proven in the topos of light condensed sets. 

## Related concepts

* [[Stone duality]]

* [[condensed mathematics]]

* [[condensed set]], [[pyknotic set]]

* [[sequential topological space]]

* [[Johnstone's topological topos]]

## References

* {#ClausenScholze23}[[Dustin Clausen]], [[Peter Scholze]], _Analytic Stacks,_ [YouTube playlist](https://www.youtube.com/playlist?list=PLx5f8IelFRgGmu6gmL-Kf_Rl_6Mm7juZO), [website](https://indico.math.cnrs.fr/event/10345/)

* {#Wärn24} [[David Wärn]], *On internally projective sheaves of groups* ([arXiv:2409.12835](https://arxiv.org/pdf/2409.12835))

* {#CCGM24} [[Felix Cherubini]], [[Thierry Coquand]], [[Freek Geerligs]], [[Hugo Moeneclaey]], *A Foundation for Synthetic Stone Duality* ([arXiv:2412.03203](https://arxiv.org/abs/2412.03203))

* *What does the topos of (light) condensed sets classify?* ([MathOverflow](https://mathoverflow.net/questions/470338/what-does-the-topos-of-light-condensed-sets-classify))

* *Clausen–Scholze's Theorem 9.1 of Analytic.pdf, in view of light condensed sets, AKA is the Liquid Tensor Experiment easier now?* ([MathOverflow](https://mathoverflow.net/questions/467433/clausen-scholzes-theorem-9-1-of-analytic-pdf-in-view-of-light-condensed-sets))

* *Condensed vs pyknotic vs consequential* ([MathOverflow](https://mathoverflow.net/questions/441838/condensed-vs-pyknotic-vs-consequential))

* [[David Roberts]], answer to *Notions of convergence not corresponding to topologies* ([MathOverflow](https://mathoverflow.net/a/464564))

[[!redirects light condensed set]]
[[!redirects light condensed sets]]

[[!redirects aleph1-condensed set]]
[[!redirects aleph1-condensed sets]]

[[!redirects LightCondSet]]
[[!redirects category of light condensed sets]]
[[!redirects categories of light condensed sets]]
[[!redirects topos of light condensed sets]]
[[!redirects toposes of light condensed sets]]
[[!redirects topoi of light condensed sets]]