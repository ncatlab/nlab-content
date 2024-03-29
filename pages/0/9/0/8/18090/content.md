

{:principle: .un_remark style="border:solid #0000cc;background: #add8e6;border-width:2px 1px;padding:0 1em;margin:0 1em;"}









***

This page contains a detailed introduction to basic [[topology]].
Starting from scratch (required background is just a basic concept of _[[sets]]_), and amplifying motivation from [[analysis]],
it first develops standard [[point-set topology]] ([[topological spaces]]).
In passing, some basics of [[category theory]] make an informal appearance,
used to transparently summarize some conceptually important aspects of the theory, such as
[[initial topology|initial]] and [[final topologies]] and the [[reflective subcategory|reflection]] into
[[Hausdorff topological space|Hausdorff]] and [[sober topological spaces]].
We close with discussion of the basics of [[topological manifolds]] and [[differentiable manifolds]],
laying the foundations for [[differential geometry]].
The second part introduces some basics of [[homotopy theory]], mostly the [[fundamental group]],
and ends with their first application to the classification of [[covering spaces]].



$\,$

{#AA} Lecture notes. $\;\;\;\;\;\;\;$ (web version requires Firefox browser -- [free download](https://www.mozilla.org/en-US/firefox/new/))

{#PartI}**part I**: _[[Introduction to Topology -- 1|Introduction to Topology 1 -- Point-set Topology]]_ $\;\;\;$([[IntroductionToTopologyI-170809.pdf:file]] 203p)


{#PartII}**part II**: _[[Introduction to Topology -- 2|Introduction to Topology 2 -- Basic Homotopy Theory]]_ $\;\;\,$ ([[IntroductionToTopologyII-170720.pdf:file]] 61p)

$\,$

For introduction to abstract _[[homotopy theory]]_ see instead at _[[Introduction to Homotopy Theory]]_.

***

$\,$

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Topology
+--{: .hide}
[[!include topology - contents]]
=--
=--
=--



#Contents#
* table of contents
{:toc}

$\,$

The idea of _[[topology]]_ is to study "[[spaces]]" with "[[continuous functions]]" between them.
Specifically one considers [[functions]] between [[sets]] (whence "[[point-set topology]]", see [below](#PointSetTopology))
such that there is a concept for what it means that these functions depend
continuously on their arguments, in that their values do not "jump".
Such a concept of [[continuous function|continuity]] is familiar from [[analysis]] on [[metric spaces]],
(recalled [below](#Continuity)) but the definition in topology generalizes this analytic concept
and renders it more foundational, generalizing the concept of [[metric spaces]] to that of _[[topological spaces]]_.

Hence, [[topology]] is the study of the [[category]] whose [[objects]] are [[topological spaces]], and whose
[[morphisms]] are [[continuous functions]].
This category is much more flexible than that of [[metric spaces]], for example it admits the construction of
arbitrary [[quotients]] and [[intersections]] of spaces.
Accordingly, topology underlies or informs many and diverse areas of mathematics, such as
[[functional analysis]], [[operator algebra]], [[manifold]]/[[scheme]] theory, hence [[algebraic geometry]] and [[differential geometry]],
and the study of [[topological groups]], [[topological vector spaces]], [[local  rings]], etc. Not the least, it gives rise to
the field of [[homotopy theory]], where one considers also continuous deformations of
continuous functions themselves ("[[homotopies]]").
Topology itself has many branches,
such as _[[low-dimensional topology]]_ or _[[topological domain theory]]_.

A popular imagery for the concept of a [[continuous function]] is provided by deformations of [[elasticity|elastic]]
physical bodies, which may be deformed by stretching them without tearing. The canonical illustration is
a continuous [[bijection|bijective]] function from the [[torus]] to the surface of a coffee mug, which maps half of the torus to the
handle of the coffee mug, and continuously deforms parts of the other half in order to form the actual cup.
Since the [[inverse function]] to this function is itself continuous,
the torus and the coffee mug, both regarded as [[topological spaces]], are "[[isomorphism|the same]]"
for the purposes of [[topology]]; one says they are _[[homeomorphic]]_.

<div style="float:right;margin:0 10px 10px 0;">
<img src="https://ncatlab.org/nlab/files/Surfaces.png" width="400">
</div>

On the other hand, there is _no_ [[homeomorphism]] from the [[torus]] to, for instance, the [[sphere]], signifying that these
represent two topologically distinct spaces. Part of topology is concerned with studying [[homeomorphism]]-[[invariants]]
of topological spaces ("[[topological properties]]") which allow to detect by means of [[algebra|algebraic]] manipulations
whether two topological spaces are homeomorphic
(or more generally [[homotopy equivalence|homotopy equivalent]]) or not. This is called _[[algebraic topology]]_.
A basic algebraic invariant is the [[fundamental group]] of a topological space (discussed [below](#FundamentalGroups)),
which measures how many ways there are to wind loops inside a topological space.

Beware the popular imagery of "[[rubber-sheet geometry]]", which only captures part of the full scope of topology,
in that it invokes spaces that _locally_ still look like [[metric spaces]] (called _[[topological manifolds]]_, see [below](#Manifolds)).
But the concept of topological spaces is a good bit more general.
Notably, [[finite topological spaces]] are either [[discrete topological space|discrete]] or very much unlike
[[metric spaces]]; the former play a role in [[categorical logic]]. Also, in [[geometry]], exotic topological spaces frequently arise when  forming non-free [[quotients]].
In order to gauge just how many of such "exotic" examples of topological  spaces beyond locally [[metric spaces]] one wishes
to admit in the theory,
extra "[[separation axioms]]" are imposed on topological spaces (see [below](#SeparationAxioms)), and the flavour of topology as a field
depends on this choice.

Among the separation axioms, the _[[Hausdorff topological space|Hausdorff space]]_ axiom is the most popular
(see [below](#TnTopologicalSpaces)). But the weaker axiom of [[sober topological space|sobriety]] (see [below](#SoberSpaces)) 
stands out, because on the one
hand it is the weakest axiom that is still naturally satisfied in applications to [[algebraic geometry]] ([[schemes are sober]])
and [[computer science]] ([Vickers 89](#Vickers89)), and on the other, it fully realizes the strong roots that
topology has in [[formal logic]]: [[sober topological spaces]] are entirely characterized by the
union-, intersection- and inclusion-relations
(logical [[conjunction]], [[disjunction]] and [[implication]]) among their [[open subsets]] ([[propositions]]).
This leads to a natural
and fruitful generalization of [[topology]] to more general "purely logic-determined spaces", called _[[locales]]_,
and in yet more generality, _[[toposes]]_ and _[[higher topos theory|higher toposes]]_. While the latter are beyond
the scope of this introduction, their rich theory and relation to the [[foundations]] of mathematics and geometry
provide an outlook on the relevance of the basic ideas of [[topology]].

$\,$

$\,$


## Point-set Topology

This chapter is at _[[Introduction to Topology -- 1|Introduction to Topology 1 -- Point-set Topology]]_

$\,$

$\,$


## Basic Homotopy Theory

This chapter is at _[[Introduction to Topology -- 2|Introduction to Topology 1 -- Basic Homotopy Theory]]_

$\,$

## References


### Point-Set Topology

#### General

A canonical compendium is

* {#Bourbaki71} [[Nicolas Bourbaki]], chapter 1 _Topological Structures_ in _Elements of Mathematics III: General topology_,  Springer (1971, 1990)

Introductory textbooks include

* {#Kelley55} [[John Kelley]], _General Topology_, Graduate Texts in Mathematics, Springer (1955)

* {#Munkres75} [[James Munkres]], _Topology_, Prentice Hall (1975, 2000)

Lecture notes include

* {#Waldhausen} [[Friedhelm Waldhausen]], _Topologie_ ([pdf](https://www.math.uni-bielefeld.de/~fw/ein.pdf))

See also the references at _[[algebraic topology]]_.




#### Special topics

The standard literature typically omits the following important topics:

Discussion of [[sober topological spaces]] is briefly in

* {#Johnstone82} [[Peter Johnstone]], section II 1. of _[[Stone Spaces]]_, Cambridge Studies in Advanced Mathematics __3__, Cambridge University Press 1982. xxi+370 pp. [MR85f:54002](http://www.ams.org/mathscinet-getitem?mr=698074), reprinted 1986.

An introductory textbook that takes sober spaces, and their relation to logic, as the starting point for topology is

* {#Vickers89} [[Steven Vickers]], _Topology via Logic_, Cambridge University Press (1989)


Detailed discussion of the [[Hausdorff reflection]] is in

* {#vanMunster14} Bart van Munster, _The Hausdorff quotient_, 2014 ([pdf](https://www.math.leidenuniv.nl/scripties/BachVanMunster.pdf))

### Basic homotopy theory

A textbook account is in 

* [[Tammo tom Dieck]], sections 2 an 3 of _Algebraic Topology_, EMS 2006 ([pdf](http://www.maths.ed.ac.uk/~aar/papers/diecktop.pdf))

Lecture notes include

* {#Moller11} [[Jesper Møller]], _The fundamental group and covering spaces_ (2011) ([pdf](http://www.math.ku.dk/~moller/f03/algtop/notes/covering.pdf))



