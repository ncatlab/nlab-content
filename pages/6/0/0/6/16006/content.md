
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Topos Theory
+--{: .hide}
[[!include topos theory - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea
 {#Idea}

For $\mathbf{H}$ a [[topos]], then an [[essential subtopos]]  $\mathbf{H}_l \hookrightarrow \mathbf{H}$ is called a _level_ of $\mathbf{H}$. This is equivalently the inclusion of the [[right adjoint]] of an [[adjoint cylinder]]/[[adjoint modality]].

The terminology is due to the fact ([Kelly-Lawvere 89](#KL89)) that the [[essential geometric morphism|essential]] [[subtoposes]] of a topos, or more generally the essential localizations of a suitably complete category, form a [[complete lattice]]. 

If for two levels $\mathbf{H}_{1} \hookrightarrow \mathbf{H}_2$ the second one includes the [[modal types]] of the [[idempotent comonad]] of the first one, and if it is minimal with this property, then [[Lawvere]] speaks of "[[Aufhebung]]" (see there for details) of the [[unity of opposites]] exhibited by the first one.

## Examples

* Every [[open subtopos]] is a level.

* For $\mathbf{H} = $ [[sSet]] the topos of [[simplicial sets]], then the tower of [[simplicial coskeleton|n-coskeleton]]-inclusions for all $n$ is a sequence of levels (the extra left adjoint exhibiting the essentialness being the [[simplicial skeleton]]). The [[Aufhebung]] in this example is discussed in detail in ([KRRZ 11](#KRRZ11)).

* The lowest level is the inclusion of the trivial subtopos as the [[terminal object]]. See also at _[[unity of opposites]]_ the section _[Werden](http://ncatlab.org/nlab/show/adjoint+modality#Werden)_.

* Often the level above this will be [[cohesion]] and the level above that, if it exists, [[differential cohesion]].

  Here differential cohesion itself typically comes in a countable tower of levels, given by the $n$th order [[infinitesimal objects]], for each $n$.

* The [[Hegelian taco]] abstracts a certain stacking of three levels viewed as a diagram in a [[2-category]] into a [[graphic monoid]].

* An essential localization $i_!\dashv i^\ast \dashv i_\ast :\mathcal{A}\to\mathcal{B}$ where $i_!\simeq i_\ast$ is called a **quintessential localization** (cf. [Johnstone 1996](#JS96) and the discussion at [[quality type]]).

## Properties

The lattice of essential localizations of a category is contained in the lattice of all localizations. While the suprema of localizations coincide in both lattices, the infinimum in the lattice of all localizations of even a pair of essential localizations need _not_ be an essential localization  ([Kelly-Lawvere 89](#KL89)).

Recall (e.g. from [Borceux 1994](#Borceux1), p.106) that [[adjunction|adjunctions]] compose: if $G\dashv F:\mathcal{A}\to\mathcal{B}$ and $K\dashv H:\mathcal{B}\to\mathcal{C}$ then $G\circ K \dashv H\circ F:\mathcal{A}\to\mathcal{C}$. Applying this twice to a pair of essential localizations yields:

+-- {: .num_prop #levelscompose} 
###### Proposition

Given two essential localizations $i_!\dashv i^\ast \dashv i_\ast :\mathcal{A}\to\mathcal{B}$ and $q_!\dashv q^\ast \dashv q_\ast :\mathcal{B}\to\mathcal{C}$ , hence in the situation:

 $$
\mathcal{A}\overset{\hookrightarrow}{\underset{\hookrightarrow}{\to}} \mathcal{B}\overset{\hookrightarrow}{\underset{\hookrightarrow}{\to}}\mathcal{C}
$$

there results a composed essential localization $q_!\cdot i_!\dashv i^\ast \cdot q^\ast \dashv q_\ast\cdot i_\ast :\mathcal{A}\to\mathcal{C}$. $\qed$
=--

Here , of course, $i^\ast \cdot q^\ast \dashv q_\ast\cdot i_\ast$ is just the adjunction involved in the composition $q\cdot i$ of the two geometric morphisms $q$ and $i$ (provided the categories involved are toposes), the important thing is that the essentialities $q_!$ and $i_!$ compose as well.

Since this just states that inclusions as well as essential geometric morphism are closed under composition and therefore so are essential inclusions, our primary interest here is to extract an explicit formula for the modalities corresponding to the composition:

The corresponding [[adjoint modalities]] are $(q_!\cdot i_!)\cdot (i^\ast \cdot q^\ast) \dashv  (q_\ast\cdot i_\ast)\cdot  (i^\ast \cdot q^\ast) :\mathcal{C}\to\mathcal{C}$.

## Related concepts

* [[quality type]]

* [[subtopos]]

* [[open subtopos]]

* [[essential sublocale]]

* [[essential subtopos]]

* [[essential geometric morphism]]

* [[Aufhebung]]

* [[Hegelian taco]]

## References

* {#SGA4} [[Michael Artin|M.Artin]], [[Alexander Grothendieck|A.Grothendieck]], [[J. L. Verdier]] (eds.), _Th&#233;orie des Topos et Cohomologie Etale des Sch&#233;mas - SGA 4_ , Springer LNM **269** Heidelberg 1972. (sec. IV 7.6., pp.414-416)

* {#Borceux1}[[Francis Borceux|F. Borceux]], _Handbook of Categorical Algebra vol. 1_ , Cambridge UP 1994.

* {#JS96}[[Peter Johnstone|P. Johnstone]], _Remarks on Quintessential and Persistent Localizations_ , TAC **2** no.8 (1996) pp.90-99. ([pdf](http://www.tac.mta.ca/tac/volumes/1996/n8/n8.pdf))

* {#KL89}[[G. M. Kelly]], [[F. W. Lawvere]], _On the Complete Lattice of Essential Localizations_ , Bull.Soc.Math. de Belgique **XLI** (1989) pp.289-319.

* {#KRRZ11} C. Kennett, [[Emily Riehl|E. Riehl]], M. Roy, M. Zaks, _Levels in the toposes of simplicial sets and cubical sets_ , JPAA **215** no.5 (2011) pp.949-961. ([arXiv:1003.5944](http://arxiv.org/abs/1003.5944))

* {#LW11}[[Rory Lucyshyn-Wright|R. Lucyshyn-Wright]], _Totally Distributive Toposes_ , arXiv.1108.4032 (2011). ([pdf](http://arxiv.org/pdf/1108.4032v3))

* {#MM19}[[Francisco Marmolejo|F. Marmolejo]], [[Matías Menni|M. Menni]], *Level $\epsilon$* , arXiv:1909.12757 (2019). ([abstract](https://arxiv.org/abs/1909.12757))

* {#VT01}[[Enrico Vitale|E. M. Vitale]], _Essential Localizations and Infinitary Exact Completions_ , TAC **8** no.17 (2001) pp.465-480. ([pdf](http://www.tac.mta.ca/tac/volumes/8/n17/n17.pdf))

