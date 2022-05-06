[[!redirects Geometric nerve of a tricategory]]
[[!redirects Street nerve]]
[[!redirects Street nerves]]
[[!redirects tricategory nerve]]
[[!redirects nerve of tricategories]]
[[!redirects nerve of a tricategory]]

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
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

The _geometric nerve_ is a natural  [[nerve]] operation on [[tricategories]], associating to every [[tricategory]] $\mathcal{C}$ a [[simplicial set]] $\mathrm{N}^{\mathsf{S}}_{\bullet}(\mathcal{C})$.

Also called the _Street nerve_ of $\mathcal{C}$, this notion, like the [[Duskin nerve]] of a [[bicategory]], is implicit in  ([ [[Ross Street]]'s work on [[oriental]]s](#Street1987)). While this construction was announced in ([Duskin, 2002](#Duskin2002)) as to appear in a (then) forthcoming paper, the latter never appeared. Instead, the notion was developed by Cegarra–Heredia in ([Cegarra–Heredia, 2012](#CegarraHeredia2012)).

Roughly, the [[Street]] nerve of $\mathcal{C}$ may be thought of as the [[simplicial set]] $\mathrm{N}^{\mathsf{S}}_{\bullet}(\mathcal{C})$ whose $n$-simplices are [[lax functors]] from the locally discrete [[tricategory]] associated to $[n]$ to $\mathcal{C}$ satisfying a variety of unitality conditions. In detail, however, the definition is more involved, as one faces problems with the definition of [[lax functor]]s between [[tricategories]] found in ([Gordon–Powers–Street](#GPS1995)); see ([Definition 5.1.1 of Cegarra–Heredia](#CegarraHeredia2012)).

 
## Properties

* The Street nerve identifies precisely nerves of [[trigroupoid]]s with $3$-[[hypergroupoid]]s: those [[Kan complexes]] for which the horn fillers in dimension $\geq 4$ are _unique_; see ([Carrasco, 2014](#Carrasco2014)).

## Picturing the Street nerve

Let ($\mathcal{C}$,$\mathsf{Hom}_{\mathcal{C}}(-,-)$,$\otimes$,$1^\mathcal{C}$,$\alpha$,$\alpha^{\bullet}$,$\phi$,$\phi^{\bullet}$,$\lambda$,$\lambda^{\bullet}$,$\eta$,$\eta^{\bullet}$,$\rho$,$\rho^{\bullet}$,$\epsilon$,$\epsilon^{\bullet}$,$\mathbf{\pi}$,$\mathbf{\lambda}$,$\mathbf{\mu}$,$\mathbf{\rho}$) be a tricategory.


## Related concepts

* [[nerve]]

* [[geometric nerve of a bicategory]]

* **geometric nerve of a tricategory**

* [[∞-nerve]]

* [[homotopy coherent nerve]]


## References

* {#CegarraHeredia2012} Antonio M. Cegarra and Benjamín A. Heredia, Geometric Realizations of Tricategories. Algebraic & Geometric Topology 14, no. 4 (2014): 1997-2064. [ [arXiv:1203.3664] ](https://arxiv.org/abs/1203.3664) 

* {#Carrasco2014} Pilar Carrasco, _Nerves of Trigroupoids as Duskin-Glenn’s $3$-Hypergroupoids_, Applied Categorical Structures 23.5 (2015): 673-707.

* {#Street1987} [[Ross Street]], _The algebra of oriented simplexes_, Journal of Pure and Applied Algebra, Volume 49, Issue 3, December 1987, Pages 283&#8211;335.

* {#GPS1995} [[Robert Gordon]], [[John Power]], [[Ross Street]], _Coherence for tricategories_, Mem. Amer. Math Soc. 117 (1995) no 558.

* {#Duskin2002} [[John Duskin]], _Simplicial matrices and the nerves of weak n-categories I: nerves of bicategories_ ([tac](http://www.tac.mta.ca/tac/volumes/9/n10/9-10abs.html)), Theory and Applications of Categories, Vol. 9, No. 10, 2002, pp. 198&#8211;308.
{#Duskin}