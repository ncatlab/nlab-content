
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Topology
+--{: .hide}
[[!include topology - contents]]
=--
=--
=--


# Contents
* automatic table of contents goes here
{:toc}


## Idea

The term [[convenient category of topological spaces]] is used for a category of [[topological space]]s nice enough to address many of the needs of working topologists, notably including the condition of being a [[cartesian closed category]]. As such, they are examples of [[nice category of spaces|nice categories of spaces]].

A primary example is the category of [[compactly generated space]]s.


## Definition

While the authors of this article don't know whether there exists in the literature a widely accepted definition of "convenient category of topological spaces", we propose the following definition as reasonable and convenient (see also the discussion [below](#NvC) on the distinction between "nice" and "convenient"): 

+-- {: .un_def}
######Definition
A **convenient category of topological spaces** is a [[full subcategory|full]] [[replete subcategory]] $C$ of the category of all topological spaces [[Top]] such that the following conditions 1-3 hold: 

1. Every [[CW complex]] is an object of $C$; 

1. $C$ is [[cartesian closed]]; 

1. $C$ is [[complete category|complete]] and [[cocomplete category|cocomplete]]. 

=--

Frequently it is also felt desirable to add closure under certain types of subspace inclusions. For instance, in the well-known examples one has 

* $C$ is closed under closed subspace inclusions in [[Top]], i.e., if $X$ belongs to $C$ and $A \subseteq X$ is a closed subspace (in $Top$), then $A$ also belongs to $C$. 

At times one might hope that $C$ is closed under open subspace inclusions as well, but this does not hold for all objects in some of the well-known examples of convenient categories. 

It may be well to note that colimits and limits in $C$ need not agree with the corresponding colimits and limits in $Top$, except under certain conditions. For example, because $C$ is a full subcategory of $Top$, the usual sorts of colimits used to present CW complexes are the same whether interpreted in $Top$ or in $C$. Also, if $C$ is closed under closed subspaces, an equalizer of a pair of maps between Hausdorff spaces in $C$ is the same whether computed in $Top$ or in $C$. On the other hand, products of $C$-objects in $Top$ need not land in $C$, so in that situation the product in $Top$ and the product in $C$ do not agree. 


## Examples

To be written. 


## "Nice" versus "convenient" categories of spaces
{#NvC}

A related entry is [[nice category of spaces]]. Here we explain the difference between "convenient" and "nice" categories of spaces. 

"A convenient category of topological spaces" is the title of a well-known paper by Norman Steenrod, who emphasized particularly function space constructions (i.e., cartesian closure) as a great convenience for working algebraic topologists, on top of (generally less problematic) completeness and cocompleteness assumptions. A well-known observation is that $Top$ lacks suitable function spaces, but that one can cut down to a suitable full subcategory of spaces which do admit function spaces; this typically involves the subtle and delicate interplay between compactness conditions and openness conditions. This comes at a cost -- that limits and/or colimits in the subcategory might not be computed as they are in $Top$ -- but this is generally considered a very small price to pay in exchange for the great convenience of these assumptions. 

That a convenient category of topological spaces contains all the CW complexes was not explicitly declared by Steenrod, but we feel certain that algebraic topologists want these as part of their convenient category. In practice this is a mild assumption, because the usual examples certainly contain all finite topological products of the interval $I$, and are closed under those $Top$-colimits used to present CW complexes, as built inductively from the basic spaces $I^n \cong D^n$. 

"Nice categories of spaces" should be thought of as a wider and vaguer term; it really means the category of spaces has "nice" categorical properties for some mathematical purpose at hand. Certainly any convenient category of spaces should be considered a nice category of spaces for the general purposes of algebraic topology. On the other hand, there are categories of spaces which are not "convenient" in the technical sense described above, but which may be very nice for certain purposes. 

For example, the category of [[compact Hausdorff space]]s can be considered as being very nice for certain purposes, because it is monadic over $Set$ (!). It is, however, not "convenient", as it very far from being cartesian closed. Another example of a nice category of spaces, as explained by Johnstone (see the references below), is the category of [[sequential space]]s, but this too is not cartesian closed. In a different direction, there is the (complete, cocomplete) cartesian closed category of [[equilogical space]]s, but this is not a full subcategory of $Top$, and the core concerns of mathematicians working with equilogical spaces are somewhat different from those of algebraic topologists. 

It should also be noted that "[[space]]" itself has a wider meaning than the technical notion of "[[topological space]]", even if topological intuitions come into play. For example, in domain theory, one often considers certain types of posets (for example, [[directed-complete partial order|dcpos]]) as certain types of "spaces". In this direction, we have that the category of dcpos and _Scott-continuous_ maps between them forms a complete, cocomplete, cartesian closed category. However, these types of spaces are quite far removed from the traditional concerns of geometry, hence are not "convenient" in the sense given above (despite the manifold relations between Scott continuity and the point-set topology which underlies the classical results on compactly generated spaces). In another direction, the category of [[locales]] is in some respects "nice", but these are not topological spaces either. 

Along with the entry on [[nice category of spaces]], see also [[subsequential space]], [[Johnstone's topological topos]], and Spanier's [[quasitopological space]]s. None of these is convenient in the precise sense above. 


## References

* [[Ronnie Brown]],  Function spaces and product topologies,  Quart. J. Math. (2) 15  (1964), 238--250.
* [[Norman Steenrod]], A convenient category of topological spaces, Michigan Math. J. 14 (1967) 133--152, [project euclid](http://projecteuclid.org/euclid.mmj/1028999711)
* Booth, P.; Tillotson, J., Monoidal closed, Cartesian closed and convenient categories of topological spaces. Pacific J. Math. 88 (1980), no. 1, 35--53. 
* Peter T. Johnstone, On a topological topos, Proc. London Math. Soc. (3) 38 (1979) 237&#8211;271.
* Edwin Spanier, "Quasi-topologies", Duke Mathematical Journal 30 (1) (1963), 1&#8211;14.


[[!redirects convenient category of topological spaces]]
[[!redirects convenient categories of topological spaces]]
[[!redirects convenient category of spaces]]
[[!redirects convenient categories of spaces]]
