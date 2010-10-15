
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
* automatic table of contents goes here
{:toc}

## Idea

A **concrete site** is a [[site]] whose objects can be thought of as [[set]]s with extra [[stuff, structure, property|structure]]: it is a [[category]] that is a [[concrete category]] and a [[site]] in a compatible way.

In a [[category of presheaves]] on a concrete site one can consider [[concrete presheaves]].


## Definition

+-- {: .un_def}
###### Definition

A **[[concrete site]]** is a [[site]] $C$ with a [[terminal object]] $*$ such that

1. the functor $Hom_C(*,-) : C \to Set$ is a [[faithful functor]];

1. for every [[coverage|covering family]] $\{f_i : U_i \to U\}$ in $C$ the morphism 

   $$
     \coprod_i Hom_C(*,f) : \coprod_i Hom_C(*, U_i) \to Hom_C(*, U) 
   $$

   is [[surjective]].

=--

## Examples

* every ([[small category|small]]) [[concrete category]] becomes a concrete site when equipped with the trivial [[coverage]] (every covering family consists of just an [[identity]] morphism);

  * for instance the [[simplex category]] $\Delta$, which is the site for [[simplicial set]]s.

* Any small subcategory of [[concrete categories]] such as [[Top]], [[Diff]], etc, with their standard [[coverage]]s (by [[open cover]])s;

  * for instance [[CartSp]] (covering families are open covers);

    which is the site for [[smooth space]]s, including [[diffeological space]]s.


[[!redirects concrete sites]]