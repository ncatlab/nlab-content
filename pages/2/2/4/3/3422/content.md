<div class="rightHandSide toc">
[[!include higher category theory - contents]]
</div>

> under construction

#Contents#
* automatic table of contents
{:toc}

## Idea

The **$(\infty,1)$-Grothendieck construction** is the analog of the [[Grothendieck construction]] which establishes an equivalence

$$
  Fib(C) \simeq 2Func(C^{op}, Cat)
$$

between [[fibered category|fibered categories]] and [[pseudofunctor]]s from [[category theory]] to [[(∞,1)-category]]-[[higher category theory|theory]].

The Grothendieck construction for [[∞-groupoid]]s constitutes an equivalence of [[(∞,1)-categories]]

$$
  LFib(C) \simeq \infty Func(C^{op}, \infty Grpd)
$$

of [[left fibration]]s and [[(∞,1)-functor]]s to [[? Grpd]], while the full Grothendieck construction for [[(∞,1)-categories]] constitutes an equivalence 

$$
  coCartFib(C) \simeq \infty Func(C^{op}, (\infty,1)Cat)
$$

between [[coCartesian fibration]]s and [[(∞,1)-functor]]s to [[(∞,1)Cat]].


>  For the moment, the analog of the [[Grothendieck construction]] for [[(∞,1)-categories]] is described at [[Cartesian fibration]] and at [[universal fibration of (∞,1)-categories]]. 

The correspondence between $(\infty,1)$-categorical [[cartesian fibrations]] $E \to C$ and [[(infinity,1)-presheaf|(∞,1)-presheaves]] $C \to (\infty,1)Cat^{op}$ may be [[model category|modeled]] by the [[Quillen equivalence]] between the [[model structure on marked simplicial over-sets]] and the projective [[global model structure on simplicial presheaves]].


## For $\infty$-groupoids


### Model structures


* [[model structure for left fibrations]]


## For $(\infty,1)$-categories


### Model structures

* [[model structure for coCartesian fibrations]]


## Relation beween the model structures

+-- {: .un_theorem}
###### Theorem (HTT, section 3.1.5)

Let $S$ be a [[simplicial set]].

There is a sequence of [[Quillen adjunction]]s

$$
  (sSet/S)_{Joyal}
  \stackrel{\overset{}{\to}}{\overset{}{\leftarrow}}
  sSet^+/S
  \stackrel{\overset{}{\to}}{\overset{}{\leftarrow}}
  (sSet^+/S)^{loc}
  \stackrel{\overset{}{\to}}{\overset{}{\leftarrow}}
  (sSet/S)_{rfib}
  \stackrel{\overset{}{\to}}{\overset{}{\leftarrow}}
  (sSet/S)_{Quillen}
  \,.
$$

Where from left to right we have

1. the [[model structure on an overcategory]] for the Joyal [[model structure for quasi-categories]];

1. the [[model structure for Cartesian fibrations]];

1. some localizaton of the model structure for Cartesian fibrations;

1. the [[model structure for right fibrations]] 

1. the [[model structure on an overcategory]] for the Quillen [[model structure on simplicial sets]];

The first and third Quillen adjunction here is a [[Quillen equivalence]] if $S$ is a [[Kan complex]].

=--


[[!redirects (∞,1)-Grothendieck construction]]