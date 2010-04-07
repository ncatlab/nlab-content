<div class="rightHandSide toc">
[[!include model category theory - contents]]
***
[[!include quasi-category theory contents]]
</div>


#Contents#
* automatic table of contents goes here
{:toc}

## Idea

A [[quasi-category]] is a [[simplicial set]] satisfying [[weak Kan complex|weak Kan filler conditions]] that make it behave like the [[nerve]] of an [[(∞,1)-category]]. 

There is a [[model category]] structure on the category [[SSet]] --  the **[[Andre Joyal|Joyal]] model structure** or **model structure on quasi-categories** -- such that the fibrant objects are precisely the quasi-categories and the weak equivalences precisely the correct _categorical equivalences_ that generalize the notion of [[equivalence of categories]].

## Details

> for the moment, see the corresponding section at [[model structure on simplicial sets]]


## Relation to the model structure for $\infty$-groupoids {#RelToInfGrpds}

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

**Proposition.** There is a [[Quillen adjunction]]

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

**Proof** This is ([JoTi, prop 1.19](http://arxiv.org/PS_cache/math/pdf/0607/0607820v2.pdf#page=7))

The following proposition shows that $(k_! \dashv k^!)$ is indeed a model for $(i \dashv Core)$:

**Proposition** 

* For any $X \in sSet$ the canonical morphism $X \to k_!(X)$ is an acyclic cofibration in $sSet_{Quillen}$;

* for $X \in sSet$ a [[quasi-category]], the canonical morphism $k^!(X) \to Core(X)$ is an acyclic fibration in $sSet_{Quillen}$.

**Proof** This is ([JoTi, prop 1.20](http://arxiv.org/PS_cache/math/pdf/0607/0607820v2.pdf#page=7))





[[!redirects Joyal model structure]]
[[!redirects Joyal model structure on simplicial sets]]
[[!redirects model structure on quasicategories]]
[[!redirects model structure on quasi-categories]]
[[!redirects model structure for quasicategories]]
