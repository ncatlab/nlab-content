+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Foundations
+-- {: .hide}
[[!include foundations - contents]]
=--
#### Mathematics
+-- {: .hide}
[[!include mathematicscontents]]
=--
=--
=--


# Contents
* table of contents
{: toc}

## Idea

In "[[analytic versus synthetic|synthetic]]" approaches to the formulation of [[theories]] in [[mathematics]] the emphasis is on [[axioms]] that directly capture the core aspects of the intended [[structures]], in contrast to more traditional "analytic" approaches where axioms are used to encode some basic substrate out of which everything else is then built [[analytic versus synthetic|analytically]].

| analytic | synthetic |
|-----------|---------|
| [[structures]] built out of "point-[[set]]"-substrate |  [[axioms]] imposed on the available [[type theory|types]] |

Often the "synthetic approach" is just referred to as "axiomatic". For instance [[model categories]] were introduced as "axiomatic homotopy theory" and indeed they may be regarded as providing a synthetic axiomatization of [[homotopy theory]], which is not based on (but does subsume) the traditional "point-set model" provided by [[topological spaces]].



## Examples

* **[[synthetic geometry]]** axiomatizes the nature of objects in a [[plane]] or [[hyperplane]] without speaking of the [[plane]] or [[hyperplane]] itself as a collection of points and without speaking of these figures as being [[subsets]] of points.

* **[[synthetic differential geometry]]** is  refinement of this to contemporary research-level mathematics.

  Here instead of defining the concept of _[[smooth manifold]]_ analytically by "point-set methodology" as is traditional (a [[set]] of points equipped with a [[topology]] and a [[smooth structure]], etc.) one imposes one single [[axiom]] scheme in the ambient [[topos]] (the "[[Kock-Lawvere axiom]]" in this case) which essentially ensures that for all [[objects]]/[[types]] $X$ there exists also an object/type $T X$ which behaves as the [[tangent bundle]] of $X$ should. These axioms then turn out to have [[models]] in [[smooth spaces]] (which include [[smooth manifolds]]) but also in other, such as [[algebraic geometry]] and [[supergeometry]].

Alternatively one may set up synthetic differential geometry via axioms for [[differential cohesion]].

* **[[synthetic homotopy theory]]** -- With the advent of [[homotopy type theory]], which may be regarded to some extent as a further abstraction of axioms similar to those of model categories, it became more common to speak of this as "synthetic homotopy theory", as, for example, in the [[Homotopy Type Theory -- Univalent Foundations of Mathematics|HoTT book]]. For a list of work carried out in homotopy type theory, see at *[[mathematics presented in homotopy type theory]]*

* **[[synthetic topology]]** -- There are many different approaches for doing [[topology]] synthetically. Some of them include:

  * [[synthetic Stone duality]], which sets up the [[topos]] of [[light condensed sets]] via axioms

  * [[abstract Stone duality]], which sets up the [[category]] of [[locally compact locales]] via axioms

  * [[real-cohesive homotopy type theory]], which sets up the [[(infinity,1)-topos]] of [[Euclidean topological infinity-groupoids]] via axioms

* [[formal category theory]], a synthetic approach to [[category theory]]

* [[synthetic differential topology]]

* [[synthetic domain theory]]

  * [[synthetic guarded domain theory]]

* [[synthetic algebraic geometry]]

* [[synthetic probability theory]]

* [[synthetic computability theory]]

* {#SyntheticTaitComputatibility} [[synthetic Tait computability]]

* [[synthetic (infinity,1)-category theory|synthetic $(\infty,1)$-category theory]]


## Relation to constructivism 

Synthetic approaches are naturally compatible with [[constructive mathematics]]/[[intuitionistic mathematics]], but [[synthetic mathematics]] is about a different issue than [[constructivism]]. For instance even most constructive [[proof assistants]] in existence have in their libraries defined basic mathematics concepts, such as [[topological spaces]], in the traditional analytic way.


## Relation to computer science

There is at least some similarity between synthetic mathematics and [[domain specific embedded programming languages]], see for instance ([Hudak 98, section 3.2](http://ncatlab.org/nlab/show/domain+specific+embedded+programming+language#Hudak98)). In ([Hudak 98, figure 2](http://ncatlab.org/nlab/show/domain+specific+embedded+programming+language#Hudak98)) this shows aspects of a real-world DSL for "geometric region analysis" embedded in [[Haskell]] which under the [[relation between type theory and category theory]]/[[computational trinitarianism]] one immediately recognizes as a fragment of [[synthetic geometry]].

## Philosophical arguments

Proving an arithmetic result in [[Peano arithmetic]], or more generally a statement in an appropriate axiomatic theory, ensures axiomatic purity (a notion of *purity of methods*) , cf. [Lehet 2021](#Lehet21)).

Moreover, such proofs are certain to be valid because of the nature of the fundamental objects considered, as captured by the axioms of the theory, and not by accident because of their particular construction in such and such a system.



## Related concepts

* [[analytic versus synthetic]]



## References


### General

* [[Andrej Bauer]]: *Synthetic Mathematics with an Excursion Into Computability Theory*, talk at University of Wisconsin Logic Seminar (Feb 2021) &lbrack;[blog](http://math.andrej.com/2021/02/03/synthetic-mathematics-with-excursion-to-computability/), slides:[pdf](https://math.andrej.com/asset/data/madison-synthetic-computability-talk.pdf), [[Bauer-Synthetic.pdf:file]] video:[yt](https://youtu.be/323qWM6tK5g)&rbrack;

* Wikipedia: _[Analytic-synthetic distinction](https://en.wikipedia.org/wiki/Analytic%E2%80%93synthetic_distinction)_

On the axiomatic method:

* {#Lehet21} Ellen Lehet: *Impurity in Contemporary mathematics*,  Notre Dame J. Formal Logic **62** 1 (2021) 67-82 &lbrack;[doi:10.1215/00294527-2021-0003](https://doi.org/10.1215/00294527-2021-0003)&rbrack; 


### Synthetic homotopy theory
 {#ReferencesSyntheticHomotopyTheory}

Discussion of _synthetic [[homotopy theory]]_ (cf. *[[synthetic homotopy theory]]*, typically understood as [[homotopy type theory]]):

* [[Ulrik Buchholtz]], Sec. 3.1 of: _Higher Structures in Homotopy Type Theory_ &lbrack;[arXiv:1807.02177](https://arxiv.org/abs/1807.02177)&rbrack;

* [[Mike Shulman]], slides 37 onwards in: _Homotopical trinitarianism:A perspective on homotopy type theory_, 2018 ([pdf](https://home.sandiego.edu/~shulman/papers/trinity.pdf))

* {#Rijke19} [[Egbert Rijke]]: _Classifying Types_ &lbrack;[arXiv:1906.09435](https://arxiv.org/abs/1906.09435)&rbrack;

Via [[cubical type theory]]:

* [[Anders Mörtberg]], [[Loïc Pujet]], *Cubical synthetic homotopy theory*,  CPP 2020: Proceedings of the 9th ACM SIGPLAN International Conference on Certified Programs and Proofs (Jan 2020) 158–171 &lbrack;[doi:10.1145/3372885.3373825](https://doi.org/10.1145/3372885.3373825), [pdf](https://staff.math.su.se/anders.mortberg/papers/cubicalsynthetic.pdf)&rbrack;

Via [[simplicial type theory]]:

* [[Emily Riehl]]: _Synthetic perspectives on spaces and categories_ &lbrack;[arXiv:2510.15795](https://arxiv.org/abs/2510.15795)&rbrack;


