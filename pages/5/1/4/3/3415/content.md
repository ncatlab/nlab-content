
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Model category theory
+--{: .hide}
[[!include model category theory - contents]]
=--
#### $(\infty,1)$-Category theory
+--{: .hide}
[[!include quasi-category theory contents]]
=--
=--
=--


#Contents#
* table of contents 
{:toc}

## Idea

A [[quasi-category]] is a [[simplicial set]] satisfying [[weak Kan complex|weak Kan filler conditions]] that make it behave like the [[nerve]] of an [[(∞,1)-category]]. 

There is a [[model category]] structure on the category [[SSet]] --  the **[[Andre Joyal|Joyal]] model structure** or **model structure on quasi-categories** -- such that the fibrant objects are precisely the quasi-categories and the weak equivalences precisely the correct _categorical equivalences_ that generalize the notion of [[equivalence of categories]].

## Definition

+-- {: .num_defn}
###### Definition

The **model structure for quasi-categories** or **Joyal model structure** $sSet_{Joyal}$ on [[sSet]] has

* [[cofibrations]] are the [[monomorphisms]]

* [[weak equivalences]] are those maps that are taken by the [[left adjoint]] of the [[homotopy coherent nerve]] to a weak equivalence in the [[model structure on simplicial categories]].

=--


## Properties

### As a Cisinski model strucre

The model structure for quasi-categories is the [[Cisinski model structure]] on [[sSet]] induced by the localizer which consists of the [[spine]] inclusions $\{Sp^n \hookrightarrow \Delta^n\}$. See ([Ara](#Ara)).

### General properties 
 {#GeneralProperties}

+-- {: .num_prop}
###### Proposition

The model structure for quasi-categories is

* a [[left proper model category]],

* a [[combinatorial model category]].

=--

+-- {: .num_remark}
###### Remark


It is also a [[monoidal model category]] and is naturally an [[enriched model category]] over itself, hence is $sSet_{Joyal}$-enriched (reflecting the fact that it tends to present an [[(infinity,2)-category]]). It is however _not_ $sSet_{Quillen}$-enriched and thus not a "[[simplicial model category]]".

=--

+-- {: .num_prop}
###### Proposition

For $p \colon \mathcal{C} \to \mathcal{D}$ a morphism of [[simplicial sets]] such that $\mathcal{D}$ is a [[quasi-category]]. Then $p$ is a fibration in $sSet_{Joyal}$ precisely if

1. it is an [[inner fibration]];

1. it is an "[[isofibration]]": for every [[equivalence in an (∞,1)-category|equivalence]] in $\mathcal{D}$ and a lift of its [[domain]] through $p$, there is also a lift of the whole equivalence through $p$ to an equivalence in $\mathcal{C}$.

=--

This is due to [[Joyal]]. ([Lurie, cor. 2.4.6.5](#Lurie)).

So ever [[fibration]] in $sSet_{Joyal}$ is an [[inner fibration]], but the converse is in general false. A notably exception are the fibrations to the point:

+-- {: .num_prop}
###### Proposition

The [[fibrant objects]] in $sSet_{Joyal}$ are precisely those that are [[inner fibration|inner fibrant]] over the point, hence those simplicial sets which are [[quasi-categories]].

=--

([Lurie, theorem 2.4.6.1](#Lurie))

### Relation to the model structure for $\infty$-groupoids {#RelToInfGrpds}

The inclusion of [[(∞,1)-category|(∞,1)-catgeories]] [[? Grpd]] $\stackrel{i}{\hookrightarrow}$ [[(∞,1)Cat]] has a left and a right [[adjoint (∞,1)-functor]]

$$
  (grpdfy \dashv i \dashv Core)
  \;\;
   :
  \;\;
  (\infty,1)Cat
  \stackrel{\overset{grpdfy}{\to}}{\stackrel{\overset{i}{\leftarrow}}{\overset{Core}{\to}}}  
  \infty Grpd
  \,,
$$

where

* $Core$ is the operation of taking the [[core]], the maximal $\infty$-groupoid inside an $(\infty,1)$-category;

* $grpdfy$ is the operation of _groupoidification_ that freely generates an $\infty$-groupoid on a given $(\infty,1)$-category

(see [[Higher Topos Theory|HTT, around remark 1.2.5.4]])

The adjunction $(grpdfy \dashv i)$ is modeled by the [[Bousfield localization of model categories|left Bousfield localization]]

$$
  (Id \dashv Id) \; :\;  sSet_{Joyal} \stackrel{\leftarrow}{\to}
  sSet_{Quillen}
  \,.
$$

Notice that the left [[derived functor]] $\mathbb{L} Id : (sSet_{Joyal})^\circ \to (sSet_{Quillen})^\circ$ takes a fibrant object on the left -- a [[quasi-category]] -- then does nothing to it but regarding it now as an object in $sSet_{Quillen}$ and then producing its fibrant replacement there, which is [[Kan fibrant replacement]]. This is indeed the operation of _groupoidification_ .

The other adjunction is given by the following

+-- {: .num_prop}
###### Proposition

There is a [[Quillen adjunction]]

$$
  (k_! \dashv k^!) \;\; : sSet_{Quillen}
  \stackrel{\overset{k^!}{\leftarrow}}{\overset{k_!}{\to}}
   sSet_{Joyal}
$$

which arises as [[nerve and realization]] for the [[cosimplicial object]]

$$
  k : \Delta \to sSet : [n] \mapsto \Delta'[n]
  \,,
$$

where $\Delta^'[n] = N(\{0 \stackrel{\simeq}{\to} 1 \stackrel{\simeq}{\to} \cdots \stackrel{\simeq}{\to} n\})$ is the [[nerve]] of the [[groupoid]] freely generated from the linear [[quiver]] $[n]$.

This means that for $X \in SSet$ we have

* $k^!(X)_n  = Hom_{sSet}(\Delta'[n],X)$.

* and $k_!(X)_n = \int^{[k]} X_k \cdot \Delta'[k]$.

=--

This is ([JoTi, prop 1.19](#JoyalTierney))

The following proposition shows that $(k_! \dashv k^!)$ is indeed a model for $(i \dashv Core)$:

+-- {: .num_prop}
###### Proposition

* For any $X \in sSet$ the canonical morphism $X \to k_!(X)$ is an acyclic cofibration in $sSet_{Quillen}$;

* for $X \in sSet$ a [[quasi-category]], the canonical morphism $k^!(X) \to Core(X)$ is an acyclic fibration in $sSet_{Quillen}$.

=--

This is ([JoTi, prop 1.20](#JoyalTierney))


## Related concepts

A similar model for [[(∞,n)-categories]] is disucssed at

* [[model structure on cellular sets]]

## References

The original construction of the Joyal model structure is in

* [[Andre Joyal]], _Theory of quasi-categories I_ 

Unfortunately, this is still not publically available. 

A proof that proceeds via [[homotopy coherent nerve]] and [[simplicially enriched categories]] is given in detail following theorem 2.2.5.1 in

* [[Jacob Lurie]], _[[Higher Topos Theory]]_
 {#Lurie}

The relation to the model structure for [[complete Segal space]]s is in

* [[Andre Joyal]], [[Myles Tierney]], _Quasi-categories vs. Segal spaces_ ([arXiv](http://arxiv.org/abs/math/0607820))

Discussion with an eye towards [[Cisinski model structures]] and the [[model structure on cellular sets]] is in 

* [[Dimitri Ara]], _Higher quasi-categories vs higher Rezk spaces_ ([arXiv](http://arxiv.org/abs/1206.4354))
 {#Ara}

See also

* [[Denis-Charles Cisinski]], _Alg&#232;bre homotopique et cat&#233;gories sup&#233;rieures_, course notes, 2009, [pdf](http://www.math.univ-toulouse.fr/~dcisinsk/coursinftycat.pdf).

[[!redirects Joyal model structure]]
[[!redirects Joyal model structure on simplicial sets]]
[[!redirects model structure on quasicategories]]
[[!redirects model structure on quasi-categories]]
[[!redirects model structure for quasicategories]]