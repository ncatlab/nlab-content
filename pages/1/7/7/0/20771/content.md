
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Topology
+-- {: .hide}
[[!include topology - contents]]
=--
#### $(0,1)$-Category theory
+-- {: .hide}
[[!include (0,1)-category theory - contents]]
=--
=--
=--


# Contents 
* table of contents
{: toc}

## Idea
 {#Idea}

Compact ordered spaces can be thought of as a refinement of the notion of [[compact Hausdorff space]] to [[order theory|ordered]] spaces. They share many properties of compact Hausdorff spaces, where equality is replaced by the order relation. 
These spaces are a convenient choice for notions of [[convergence]] in an [[order theory|ordered]] setting.

In particular, just as [[compact Hausdorff spaces]] can be seen as [[algebra over a monad|algebras]] of the [[ultrafilter|ultrafilter monad]] on [[Set]], compact ordered spaces can be seen as algebras of the [[prime filter monad]] on [[Pos]], (see [below](#as_algebras)).


The concept was introduced by Nachbin (see [Nachbin '65](#nachbin)).


## Definition

A **compact ordered space** or **compact pospace** is a [[compact topological space]] $X$ equipped with a [[partial order]] which is [[closed subset|closed]] as a [[subset]] of $X\times X$.


## Properties

* A compact ordered space is always [[Hausdorff]], i.e. it is a [[compactum]]. To see this, note that since the [[relation]] is a closed subset of $X\times X$, so is the [[opposite relation]], and hence their intersection too, which is the [[diagonal]] of $X\times X$. 

(...)

## As algebras

For now, see [Flagg '96](#flagg).

(...)

## Connection with stably compact spaces 

For now, see [Jung '04](#jung2).

(...)

## See also 

* [[compact Hausdorff space]]
* [[stably compact space]]

## References


* {#nachbin} Leopoldo Nachbin, _Topology and Order_, Van Nostrand, 1965.

* {#flagg} Bob Flagg, _Algebraic theories of compact pospaces_, Topology and its Applications, 1996 ([doi:10.1016/S0166-8641(96)00117-4](https://doi.org/10.1016/S0166-8641%2896%2900117-4)).

* {#jung2} Achim Jung, _Stably compact spaces and the probabilistic powerspace construction_, ENTCS 87, 2004 ([doi:10.1016/j.entcs.2004.10.001](https://doi.org/10.1016/j.entcs.2004.10.001)).


[[!redirects compact ordered spaces]]
[[!redirects ordered compact space]]
[[!redirects ordered compact spaces]]
[[!redirects compact ordered topological space]]
[[!redirects compact ordered topological spaces]]
[[!redirects ordered compact topological space]]
[[!redirects ordered compact topological spaces]]
[[!redirects compact pospace]]
[[!redirects compact pospaces]]