
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Enriched category theory
+--{: .hide}
[[!include enriched category theory contents]]
=--
#### Analysis
+-- {: .hide}
[[!include analysis - contents]]
=--
=--
=--




\tableofcontents

## Idea


[Lawvere 1973](#Lawvere1973) pointed out that [[metric spaces]] are precisely [[enriched category|categories enriched]] in the [[monoidal category|monoidal]] [[partial order|poset]] $([0, \infty], \geq)$, where the [[tensor product]] is taken to be [[addition]].  The [[composition]] operation in this enriched category identifies with the [[triangle identity]] in the metric space (see at _[triangle inequality -- Interpretation in enriched category theory](triangle+inequality#InterpretationInEnrichedCategoryTheory)_).

Alternatively, taking the monoidal product to be [[supremum]] instead, enriched categories amount to Lawvere ultrametric spaces.

Thus generalized, many constructions and results on [[metric spaces]] turn out to be special cases of yet more general constructions and results of [[enriched category theory]].  This includes for example the notion of [[Cauchy complete category|Cauchy completion]], which in general enriched category theory is related to [[Karoubi envelope|Karoubi envelopes]] and [[Morita equivalence]].

The symmetry axiom is naturally interpreted as giving an enriched [[dagger category|$\dagger$-category]] [[structure]], if we treat the [[poset]] $[0, \infty]$ as a $\dagger$-[[monoid]] where the involution $\dagger$ is the identity. Note that when one is enriching over a [[cartesian monoidal category|cartesian monoidal]] poset, there is no difference between a $\dagger$-category and a [[groupoid]], so in that sense, ultrametric spaces could be regarded as [[enriched groupoid|enriched groupoids]], a perhaps more familiar concept. However, note that the requisite axioms for enriched groupoids do not make sense when the base of enrichment is not cartesian, so we cannot regard an ordinary metric space as an enriched groupoid, just as an enriched $\dagger$-category.

In the presence of the symmetry axiom, the [[separation axiom|"separation" axiom]] "$x=y$ if $d(x,y)=0$" is equivalent to [[skeletal category|skeletality]] of an enriched category.  That is, a pseudo-metric space is a metric space precisely when it is skeletal.  But in the non-symmetric case, this separation axiom is stronger than skeletality; the latter would say only "$x=y$ if $d(x,y)=d(y,x)=0$".  That is, a quasi-pseudo-metric space can be skeletal without being a quasi-metric space, at least the way the latter term is usually used.

Note that like any kind of enriched category, Lawvere metric spaces are [[monads]] in a [[bicategory]] of "matrices", whose objects are sets and whose morphisms from $X$ to $Y$ are functions $d:X\times Y \to [0,\infty]$.  This sort of perspective can be generalized to many other kinds of topological structures; an exposition is given in [Hofmann, Seal & Tholen 2014](#HofmannSealTholen2014).

The category of metric spaces and categories of random maps as generalised metric spaces were studied by [Meng 1988](#Meng1988).


## References

The original observation:

*  {#Lawvere1973}  [[Bill Lawvere]]: *Metric spaces, generalized logic and closed categories* (1973),  reprinted in Reprints in [[TAC|Theories and Applications of Categories]] **1** (2002) 1-37  &lbrack;[tac:tr1](http://www.tac.mta.ca/tac/reprints/articles/1/tr1abs.html), [pdf](http://www.tac.mta.ca/tac/reprints/articles/1/tr1.pdf)&rbrack;

and further discussion:

* {#Meng1988} Xiao-qing Meng: _Categories of convex sets and of metric spaces with applications to stochastic programming and related areas_, PhD thesis (1988) &lbrack;[[Meng.djvu|djvu:file]]&rbrack;

* {#HofmannSealTholen2014} [[Dirk Hofmann]], [[Gavin J. Seal]], [[Walter Tholen]] (ed.), *Monoidal topology: A Categorical Approach to Order, Metric, and Topology*,  Cambridge University Press (2014) &lbrack;[doi:10.1017/CBO9781107517288](https://doi.org/10.1017/CBO9781107517288), [pdf](https://sweet.ua.pt/dirk/artigos/HST14_Monoidal_topology_A_categorical_approach_to_order_metric_and_topology.pdf)&rbrack;


Application to [[triangulated categories]] in relation to their [[enhanced triangulated category|enhancement]]:

* [[Amnon Neeman]]: *Metrics on triangulated categories*, J. Pure Appl. Algebra **224** 4 (2020) 106206 &lbrack;[arXiv:1901.01453](https://arxiv.org/abs/1901.01453), [doi:10.1016/j.jpaa.2019.106206](https://doi.org/10.1016/j.jpaa.2019.106206)&rbrack;

* [[Amnon Neeman]]: *Excellent metrics on triangulated categories, and the involutivity of the map taking $\mathcal{S} to \mathfrak{S}({\mathcal{S})^{\mathrm{op}}}$* &lbrack;[arXiv:2505.09120](https://arxiv.org/abs/2505.09120)&rbrack;



[[!redirects metrics on a category]]

[[!redirects metrics on categories]]

[[!redirects Lawvere metric space]]
[[!redirects Lawvere metric spaces]]

