# Functor categories
* table of contents
{: toc}

## Definition

Given [[category|categories]] $C$ and $D$, the **functor category** -- written $D^C$ or $[C,D]$ -- is the category whosse

* [[object]]s are [[functor|functors]] $F: C \to D$  

* [[morphism]]s are [[natural transformation|natural transformations]] between these functors.


## Usage
 
Functor categories serve as the [[hom-category|hom-categories]] in the [[strict 2-category]] [[Cat]].

In the context of [[enriched category theory]] the functor category is generalized to the [[enriched functor category]].

In the absence of the [[axiom of choice]] (including many [[internal category|internal]] situations), the appropriate notion to use is the [[anafunctor category]].


## Size issues

If $C$ and $D$ are [[small category|small]], then $[C,D]$ is also small.

If $C$ is small and $D$ is [[locally small category|locally small]], then $[C,D]$ is still locally small.

Even if $C$ and $D$ are locally small, if $C$ is not small, then $[C,D]$ will usually not be locally small.

As a partial converse to the above, if $C$ and $[C,Set]$ are locally small, then $C$ must be [[essentially small category|essentially small]]; see [Fryed & Street (1995)](http://tac.mta.ca/tac/volumes/1995/n9/1-09abs.html).


[[!redirects functor category]]
[[!redirects functor categories]]
