
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Homotopy theory
+--{: .hide}
[[!include homotopy - contents]]
=--
#### Representation theory
+-- {: .hide}
[[!include representation theory - contents]]
=--
#### Cohomology
+--{: .hide}
[[!include cohomology - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Definition

+-- {: .num_defn #TheOrbitCategory}
###### Definition

Given a [[topological group]] $G$ the __orbit category__ $\mathrm{Or}\, G$ (denoted also $\mathcal{O}_G$) is the [[category]] whose 

* objects are the [[homogeneous space]]s ($G$-orbit types) $G/H$, where $H$ is a closed [[subgroup]] of $G$, 

* and whose morphisms are $G$-equivariant maps.  

=--

+-- {: .num_remark }
###### Remark

For suitable continuous [[actions]] of $G$ on a [[topological space]] $X$, every [[orbit]] of the action is [[isomorphism|isomomorphic]] to one of the [[homogeneous spaces]] $G/H$ ($H$ is the [[stabilizer group]] of any point in the orbit). This is the sense in which def. \ref{TheOrbitCategory} gives "the category of all $G$-orbits".

=--

+-- {: .num_remark }
###### Remark

Def. \ref{TheOrbitCategory}
yields a [[small category|small]] [[enriched category|topologically enriched]] category (though of course if $G$ is a [[discrete group]], the enrichment of $\mathrm{Or}\, G$ is likewise discrete).  

Of course, like any category, it has a [[skeleton]], but as usually defined it is not itself skeletal, since there can exist distinct subgroups $H$ and $K$ such that $G/H\cong G/K$.


=--

+-- {: .num_remark }
###### Remark

Warning: This should not be confused with the situation where a group $G$ acts on a groupoid $\Gamma$ so that one obtains the  [[orbit groupoid]].   

=--

More generally, given a family $F$ of subgroups of $G$ which is closed under conjugation and taking subgroups one looks at the full subcategory $\mathrm{Or}_F\,G \subset \mathrm{Or}\,G$ whose objects are those $G/H$ for which $H\in F$.


## Variants

Sometimes a family, $\mathcal{W}$, of subgroups is specified, and then a subcategory of $\mathrm{Or}\, G$ consisting of the $G/H$ where $H\in \mathcal{W}$ will be considered. If the trivial subgroup is in $\mathcal{W}$ then many of the considerations of results such as [[Elmendorf's theorem]] will go across to the restricted setting.

## Properties

### Relation to Mackey functors

Orbit categories are used often in the treatment of [[Mackey functor]]s from the theory of [[locally compact group]]s and in the definition of [[Bredon cohomology]]. 

### Relation to Bredon equivariant cohomology

It appears in [[equivariant stable homotopy theory]], where the $H$-fixed [[homotopy groups]] of a space form a [[presheaf]] on the [[homotopy category]] of the orbit category (e.g. [page 8, 9 here](http://www.math.uchicago.edu/~may/PAPERS/Newthird.pdf#page=8)).

### Relation to $G$-spaces and Elmendorf's theorem

[[Elmendorf's theorem]] (see there for details) states that the [[(∞,1)-category of (∞,1)-presheaves]] on the orbit category $Orb_G$ are [[equivalence of (∞,1)-categories|equivalent]] to the [[localization of an (∞,1)-category|localization]] of [[topological spaces]] with $G$-[[action]] at the "fixed point weak equivalences".

### Relation to the category of groups, homomorphisms and conjugations

See at _[[global equivariant homotopy theory]]_.

## Related concepts

* [[global equivariant stable homotopy theory]]

* [[Bredon cohomology]]

##References

A very general setting for the use of orbit categories is described in

* [[W. G. Dwyer]] and [[D. M. Kan]], _Singular functors and realization functors_ , Nederl. Akad. Wetensch. Indag. Math., 87, (1984), 147 &#8211; 153. 

[[!redirects orbit categories]]
