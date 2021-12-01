
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

The _generic interval_ is the standard [[1-simplex]] $\Delta_1$ in [[sSet]].

## Properties

What makes this interval 'generic' is the following result:

\begin{theorem}

_The [[topos]] [[sSet]] of [[simplicial sets]] is the [[classifying topos]] for [[linear orders]] with distinct [[top]] and [[bottom]] elements, i.e. intervals (aka nontrivial totally [[distributive lattices]]) with generic interval $\Delta_1=Hom_{\Delta}(\quad,[1])$.

If $I$ is an interval in a topos $\mathcal{E}$, then it corresponds to a [[geometric morphism]] $S_I \,\colon\, \mathcal{E}\rightarrow sSet$ with [[direct image]] part $S_I_* \,\colon\, \mathcal{E}\rightarrow sSet$ the [[singular simplicial set|singular functor]] and [[inverse image]] part the [[geometric realization]] functor $|\quad|_I \,\colon\, sSet\rightarrow \mathcal{E}$.

\end{theorem}

This result was announced by [[André Joyal]] in 1974 at the [[Isle of Thorns]], the first published proof appears in [Johnstone 1979](#Johnstone79) and in book form in [MacLane-Moerdijk 1994](#MacLaneMoerdijk94), sec. VIII.8).


\begin{remark} 

The classifying topos point of view is helpful, because it is the choice of an algebraic structure, of the kind classified, in a [[topological topos]] that gives rise to an exact singular/realization pair.  ([Lawvere 2013](#GrandisLawvere13))

\end{remark}


\begin{remark}

The generic interval and the results of [Wraith 1993](#Wraith93) play a role in Lawvere's attempt to view classical combinatorial topology as part of greater landscape situated in the [[presheaf topos]] on the category of nonempty finite sets, which is the classifying topos for nontrivial [[Boolean algebras]] and contains [[simplicial complexes]] and the category of [[groupoids]] [[Grpd]] as [[reflective subcategories]]  (cf. [Lawvere 1989](#Lawvere89), pp.273-275).

\end{remark}



## Related Concepts

* [[topological topos]]

* [[Aufhebung]]

* [[interval object]]

* [[sSet]]


## References ##

* {#Johnstone79} [[Peter Johnstone]], _On a topological topos_ , Proc. London Math. Soc. **3** 38 (1979) pp.237-271. (cf. this n-caf&#233; blog ([link](http://golem.ph.utexas.edu/category/2014/04/on_a_topological_topos.html)))

* {#Lawvere89} [[F. William Lawvere]], _Qualitative Distinctions between some Toposes of Generalized Graphs_, Contemporary Mathematics **92** (1989) pp.261-299 ([doi:10.1090/conm/092](http://dx.doi.org/10.1090/conm/092)).

* [[F. William Lawvere]], _Categories of Spaces may not be Generalized Spaces as Exemplified by Directed Graphs_, Revista Colombiana de Matem&#225;ticas **XX** (1986) pp.179-186. Reprinted with commentary in TAC **9** (2005) pp.1-7. ([pdf](ftp://ftp.tac.mta.ca/tac/html/tac/reprints/articles/9/tr9.pdf))

* {#Wraith93} [[Gavin C. Wraith]], _Using the Generic Interval_, Cah. Top. G&#233;om. Diff. Cat. **XXXIV** 4 (1993) pp.259-266. ([pdf](http://archive.numdam.org/ARCHIVE/CTGDC/CTGDC_1993__34_4/CTGDC_1993__34_4_259_0/CTGDC_1993__34_4_259_0.pdf))

* {#MacLaneMoerdijk94} [[Saunders Mac Lane]], [[Ieke Moerdijk]], _[[Sheaves in Geometry and Logic]]_ , Springer Heidelberg 1994.


* [[F. William Lawvere]], _Core Varieties, Extensivity, and Rig Geometry_, TAC  **20** no.14 (2008) pp.497-503. ([pdf](ftp://ftp.tac.mta.ca/pub/tac/html/volumes/20/14/20-14.pdf))


* [[F. William Lawvere]], [[Ross Street]], [[Todd Trimble]], _catlist exchange October 2011_ , ([link](http://comments.gmane.org/gmane.science.mathematics.categories/6980)) .

* {#GrandisLawvere13} [[Marco Grandis]], [[F. William Lawvere]], _catlist exchange November 2013_ , ([link](http://comments.gmane.org/gmane.science.mathematics.categories/7920)).




