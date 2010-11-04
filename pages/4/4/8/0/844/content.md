
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### $(\infty,1)$-Category theory
+--{: .hide}
[[!include quasi-category theory contents]]
=--
=--
=--

#Contents#
* automatic table of contents goes here
{:toc}

## Idea

The _join of two [[quasi-category|quasi-categories]]_ is the generalization of the [[join of categories]] from ordinary [[category|categories]] to [[quasi-category|quasi-categories]].

The  _join_ of quasi-categories $C$ and $C'$ is a [[quasi-category]] $C \star C'$ which looks roughly like the disjoint union of $C$ with $C'$ with one morphisms from every object of $C$ to every object of $C'$ thrown in.


## Definition

Two different definitions are used in the literature, which are not isomorphic, but are weakly equivalent with respect to the [[model structure on quasi-categories]].

1. The **join** $C \star C'$ of two [[quasi-category|quasi-categories]] $C$ and $C'$ is the [[join of simplicial sets]] of their underlying [[simplicial set]]s.

1. The alternate join $C \diamondsuit D$ of two quasi-categories should be thought of as something like the [[2-limit|pseudopushout]]

   $$
     \array{
       C \times D &\stackrel{p_2}{\to}& D
       \\
       {}^{\mathllap{p_1}} &\swArrow& \downarrow
       \\
       C &\to& C \diamondsuit D
     }
   $$

   Explicitly (compare [[mapping cone]]) it is the ordinary [[colimit]]

   $$
     \array{
       && C \times D \times {1} &\to&  D
       \\
       &&\downarrow && \downarrow
       \\
       C \times D \times {0}
       &\to& C \times D \times \Delta^1
       \\
       \downarrow &&&& \downarrow
       \\
       C &\to& &\to& C \diamondsuit D
     }
   $$   
 
   in [[sSet]].

The join of two [[simplicial set]]s that happen to be [[quasi-category|quasi-categories]] is itself a quasi-category.

## Properties

For $C$ and $D$ [[simplicial set]]s, the canonical morphism

$$
  C \diamondsuit D \to C \star D
$$

is a weak equivalence in the [[model structure on quasi-categories]].

## Examples {#Examples}

### Joins with the point

Let $* = \Delta[0]$ be the [[terminal object|terminal]] quasi-category. Then for $X$ any quasi-category, 

* the join $X^{\triangleleft} := (*)\star X$ is the quasi-category obtained from $X$ by freely adjoining a new [[terminal object in a quasi-category|initial object]];

* the join $X^{\triangleright} := X \star (*)$ is the quasi-category obtained from $X$ by freely adjoining a new [[terminal object in a quasi-category|terminal object]].

For instance for $X = \Delta[1] = \{ 0 \to 1 \}$ be have

$$
  X^{\triangleright} = 
  \left\{
    \array{
      0 &&\to&& 1
      \\
      & \searrow &\swArrow& \swarrow
      \\
      && \bottom
    }
  \right\}
  \,.
$$

## References

The operation $\star_s$
is discussed around [proposition 1.2.8.3, p. 43](http://arxiv.org/PS_cache/math/pdf/0608/0608040v4.pdf#page=43) of 

* [[Jacob Lurie]], _[[Higher Topos Theory]]_  .


The operation $\diamondsuit$ is discussed in
[chapter 3](http://www.crm.cat/HigherCategories/hc2.pdf#page=95) of

* [[André Joyal]], _The theory of quasicategories and its applications_ lectures at [Simplicial Methods in Higher Categories](http://www.crm.es/HigherCategories/), ([pdf](http://www.crm.cat/HigherCategories/hc2.pdf))

and in [[Higher Topos Theory|section 4.2.1]] of

* [[Jacob Lurie]], _[[Higher Topos Theory]]_  ,

where also the relation between both constructions is established.

