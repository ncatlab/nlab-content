

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Topology
+--{: .hide}
[[!include topology - contents]]
=--
#### Foundations
+-- {: .hide}
[[!include foundations - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}


## Idea 
 {#Idea}

**Condensed mathematics** aims to provide a more convenient framework in which to treat [[algebra|algebraic]] objects which are equipped with a [[topological space|topology]], such as [[topological abelian groups]] or [[topological vector spaces]]. Related aims are to turn [[functional analysis]] into a branch of [[commutative algebra]], and various types of [[analytic geometry]] into [[algebraic geometry]].

For instance, the [[category]] of [[topological abelian groups]] is not [[abelian category|abelian]], which means for instance that it lacks a good theory of [[exact sequences]]. 
But the category of [[condensed abelian groups]] is [[abelian category|abelian]] and it contains topological abelian groups as a [[full subcategory]] (under appropriate conditions, see [ScholzeLCM](#ScholzeLCM), Proposition 1.7).

According to [[Peter Scholze]] in [this comment on the nCafé](https://golem.ph.utexas.edu/category/2020/03/pyknoticity_versus_cohesivenes.html#c057780), current expositions of condensed mathematics rely heavily on the [[axiom of choice]] and choice-like axioms such as the [[presentation axiom]], so it is unknown how much they still hold in the context of more [[constructive mathematics]] without choice. 

## Concepts

### Condensed objects

* [[condensed set]]

* [[condensed abelian group]]

* [[condensed ring]]

* [[condensed module]]


#### Solid objects

* [[solid abelian group]]

* [[solid module]]

* [[solidification functor]]

* [[solid spectrum]]


#### Liquid objects

* [[liquid vector space]]

* [[liquid module]]


#### Other

* [[trace-class map]]

* [[nuclear module]]

* [[analytic ring]]


### Higher condensed objects

* [[condensed infinity-groupoid]]

* [[condensed object in an (infinity,1)-category]]

* [[condensed spectrum]]

* [[condensed E-infinity ring]]

* [[condensed module spectrum]]

## Applications

The theory of solid modules was used to formulate the correct theory of $\ell$-adic sheaves for the geometrization of the [[local Langlands correspondence]] by Fargues and Scholze ([FarguesScholze21](#FarguesScholze21)). It has also been used by Mann to formalize the [[six operations]] for [[rigid analytic geometry]] ([Mann22](#Mann22)).

Condensed mathematics has also been used in [ClausenScholze22](#ClausenScholze22) to provide new "analysis-free" proofs of the finiteness of [[coherent cohomology]], [[Serre duality]], [[GAGA]], and the [[Hirzebruch-Riemann-Roch theorem]] in [[complex analysis]].

## Related entries

* [[bornological topos]]

* [[pyknotic set]]

* [[analytic geometry]]

## References

* {#ScholzeLCM} [[Peter Scholze]], _Lectures on condensed mathematics_, [pdf](https://www.math.uni-bonn.de/people/scholze/Condensed.pdf)

* {#ScholzeLAG} [[Peter Scholze]], _Lectures on analytic geometry_, [pdf](https://www.math.uni-bonn.de/people/scholze/Analytic.pdf)

* {#ClausenScholze22}[[Dustin Clausen]], [[Peter Scholze]], _Condensed Mathematics and Complex Geometry_, [pdf](https://people.mpim-bonn.mpg.de/scholze/Complex.pdf)


* {#DustinScholze20}[[Dustin Clausen]], [[Peter Scholze]], _Masterclass in condensed mathematics,_ [YouTube playlist](https://www.youtube.com/playlist?list=PLAMniZX5MiiLXPrD4mpZ-O9oiwhev-5Uq), [website](https://www.math.ku.dk/english/calendar/events/condensed-mathematics/) (including pdf notes)


[[formal proof|Formalization]]/[[certified programming|verification]] in [[proof assistants]] ([[Lean]]):

* [[Peter Scholze]], *[Liquid tensor experiment](https://xenaproject.wordpress.com/2020/12/05/liquid-tensor-experiment/)*, December 2020

* [[Peter Scholze]], *[Half a year of Liquid Tensor Experiment: Amazing developments](https://xenaproject.wordpress.com/2021/06/05/half-a-year-of-the-liquid-tensor-experiment-amazing-developments/)*, June 2021

Applications of condensed mathematics include the following:

* {#FarguesScholze21} [[Laurent Fargues]], [[Peter Scholze]], _Geometrization of the local Langlands correspondence_ ([arXiv:2102.13459](https://arxiv.org/abs/2102.13459))

* {#Mann22} Lucas Mann, _A p-Adic 6-Functor Formalism in Rigid-Analytic Geometry_ ([arXiv:2206.02022](https://arxiv.org/abs/2206.02022))

On condensed [[fractured (infinity,1)-topos|fractured $\infty$-topos]]-[[structure]] (cf. [[condensed local contractibility]]):  

* [[Qi Zhu]], *Fractured Structure on Condensed Anima*, MSc thesis, Bonn (2023) &lbrack;[pdf](https://1429cecd-24a0-4223-8b7c-1ebf47aa12e2.filesusr.com/ugd/8e912a_fe1c2f8e90094d0fa065fb8129687963.pdf), [[QiZhu-FracturedCondensed.pdf:file]]&rbrack;

with exposition in

* [[Qi Zhu]], *Fractured structure on condensed spaces*, talk notes (2023) &lbrack;[pdf](https://1429cecd-24a0-4223-8b7c-1ebf47aa12e2.filesusr.com/ugd/8e912a_8d2a90176ed14969a877e77ec1b787da.pdf), [[QiZhuFracturedCondensed.pdf:file]]&rbrack;

* [[Nima Rasekh]], *What is a topological structure?*, talk notes (April 2023) &lbrack;[pdf](https://guests.mpim-bonn.mpg.de/rasekh/Condensed.pdf), [[Rasekh-TopologicalStructure.pdf:file]]&rbrack;



