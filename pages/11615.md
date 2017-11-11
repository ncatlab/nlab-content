
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

In "synthetic" approaches to the formulation of [[theories]] in [[mathematics]] the emphasis is on [[axioms]] that directly capture the core aspects of the intended [[structures]], in contrast to more traditional "analytic" approaches where axioms are used to encode some basic substrate out of which everything else is then built [[analytic and synthetic|analytically]].

| analytic | synthetic |
|-----------|---------|
| [[structures]] built out of "point-[[set]]"-substrate |  [[axioms]] imposed on the available [[type theory|types]] |


## Examples

* _[[synthetic geometry]]_ axiomatizes the nature of figures drawn in the [[plane]] without speaking of the [[plane]] itself as a collection of points and without speaking of these figures as being [[subsets]] of points.

* A refinement of this to contemporary research-level mathematics is _[[synthetic differential geometry]]_. 

  Here instead of defining the concept of _[[smooth manifold]]_ analytically by "point-set methodology" as is traditional (a [[set]] of points equipped with a [[topology]] and a [[smooth structure]], etc.) one imposes one single [[axiom]] scheme in the ambient [[topos]] (the "[[Kock-Lawvere axiom]]" in this case) which essentially ensures that for all [[objects]]/[[types]] $X$ there exists also an object/type $T X$ which behaves as the [[tangent bundle]] of $X$ should. These axioms then turn out to have [[models]] in [[smooth spaces]] (which include [[smooth manifolds]]) but also in other, such as [[algebraic geometry]] and [[supergeometry]].

Often the "synthetic approach" is just referred to as "axiomatic". For instance [[model categories]] were introduced as "axiomatic homotopy theory" and indeed they may be regarded as providing a synthetic axiomatization of [[homotopy theory]], which is not based on (but does subsume) the tradtional "point-set model" provided by [[topological spaces]].

* With the advent of [[homotopy type theory]], which may be regarded to some extent as a further abstraction of axioms similar to those of model categories, it became more common to speak of this as "synthetic homotopy theory" (e.g. in the [[Homotopy Type Theory -- Univalent Foundations of Mathematics|HoTT book]]).

* [[synthetic differential topology]]

* [[synthetic domain theory]]

* [[synthetic computability theory]]

* [[synthetic topology]]


## Relation to constructivism 

Synthetic approaches are naturally compatible with [[constructive mathematics]]/[[intuitionistic mathematics]], but synthetic mathematics is about a different issue than constructivism. For instance even most constructive [[proof assistants]] in existence have in their libraries defined basic mathematics concepts, such as topological spaces, in the traditional analytic way.


## Relation to computer science

There is at least some similarity between synthetic mathematics and [[domain specific embedded programming languages]], see for instance ([Hudak 98, section 3.2](http://ncatlab.org/nlab/show/domain+specific+embedded+programming+language#Hudak98)). In ([Hudak 98, figure 2](http://ncatlab.org/nlab/show/domain+specific+embedded+programming+language#Hudak98)) this shows aspects of a real-world DSL for "geometric region analysis" embedded in [[Haskell]] which under the [[relation between type theory and category theory]]/[[computational trinitarianism]] one immediately recognizes as a fragment of [[synthetic geometry]].


[[!redirects synthetic homotopy theory]]
