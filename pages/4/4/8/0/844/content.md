
#Contents#
* automatic table of contents goes here
{:toc}

## Idea

The _join of two [[quasi-category|quasi-categories]]_ is the generalization of the [[join of categories]] from ordinary [[category|categories]] to [[quasi-category|quasi-categories]].

The  _join_ of quasi-categories $C$ and $C'$ is a [[quasi-category]] $C \star C'$ which looks roughly like the disjoint union of $C$ with $C'$ with one morphisms from every object of $C$ to every object of $C'$ thrown in.


## Definition

Two different definitions are used in the literature, which are equivalent with respect to the [[model structure on quasi-categories]].

1. The **join** $C \star_{s} C'$ of two [[quasi-category|quasi-categories]] $C$ and $C'$ is the [[join of simplicial sets]] of their underlying [[simplicial set]]s.

1. The join $C \star_J D$ of two quasi-categories is the [[homotopy colimit]] 

   $$
     \array{
       C \times D &\stackrel{p_2}{\to}& D
       \\
       {}^{\mathllap{p_1}} &\swArrow_\simeq& \downarrow
       \\
       C &\to& C \star_J D
     }
   $$

   modeled (since the [[model structure for quasi-categories]] is a [[category of fibrant objects|category of cofibrant objects]], see [[mapping cone]]) concretely as the ordinary [[colimit]]

   $$
     \array{
       && X \times Y \times {1} &\to&  Y
       \\
       &&\downarrow && \downarrow
       \\
       X \times Y \times {0}
       &\to& X \times Y \times \Delta^1
       \\
       \downarrow &&&& \downarrow
       \\
       X &\to& &\to& C \star_J D
     }
   $$   
 
   in [[SSet]].

Indeed, the join of two [[simplicial set]]s that happen to be [[quasi-category|quasi-categories]] is itself a quasi-category, due to

## Properties

For $C$ and $D$ [[simplicial set]]s, the canonical morphism

$$
  C \star_J D \to C \star_s D
$$

is a weak equivalence in the [[model structure on quasi-categories]].

## References

The operation $\star_s$
is discussed around [proposition 1.2.8.3, p. 43](http://arxiv.org/PS_cache/math/pdf/0608/0608040v4.pdf#page=43) of 

* [[Jacob Lurie]], _[[Higher Topos Theory]]_  .


The operation $\star_J$ is discussed in
[chapter 3](http://www.crm.cat/HigherCategories/hc2.pdf#page=95) of

* [[André Joyal]], _The theory of quasicategories and its applications_ lectures at [Simplicial Methods in Higher Categories](http://www.crm.es/HigherCategories/), ([pdf](http://www.crm.cat/HigherCategories/hc2.pdf))

and in [[Higher Topos Theory|section 4.2.1]] of

* [[Jacob Lurie]], _[[Higher Topos Theory]]_  ,

where also the relation between both constructions is established.

