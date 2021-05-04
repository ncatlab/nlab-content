
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Topos Theory
+--{: .hide}
[[!include topos theory - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

In [[topology|point set topology]], an [[open map]] is a [[continuous map]] that sends [[open sets]] to open sets. The notion of an **open geometric morphism** is a generalization of this notion from topology to [[topos theory]].

From a logical perspective, a [[geometric morphism]] $f:\mathcal{F}\to\mathcal{E}$ is open iff it preserves the interpretation of [[first order logic]]. This contrasts with general geometric morphisms which are only bound to preserve [[geometric logic]].

## Definition

A [[geometric morphism]]

$$
  f := (f^* \dashv f_*) : \mathcal{F} \to \mathcal{E}
$$

is called _open_ if the following equivalent conditions hold

* the [[localic reflection]] of $f$ over $\mathcal{E}$ is an [[overt space | overt]] internal locale in $\mathcal{E}$;

* the [[inverse image]] $f^*$ is a [[Heyting functor]], hence preserves [[first order logic]].

## Examples

* [[locally connected geometric morphisms]] are open. (cf. [Johnstone (2002)](#J02), p.650)

## Properties

+-- {: .num_prop}
###### Proposition
A [[geometric morphism]] $f:\mathcal{F}\to\mathcal{E}$ is open iff the canonical map $\lambda:\Omega_\mathcal{E}\to f_\ast(\Omega_\mathcal{F})$ of poset objects in $\mathcal{E}$ has an internal left adjoint $\mu :f_\ast(\Omega_\mathcal{F})\to\Omega_\mathcal{E}$.
=--

(cf. [Mac Lane-Moerdijk (1994)](#MM94), p.502)

+-- {: .num_prop}
###### Proposition
A [[geometric morphism]] $f:\mathcal{F}\to\mathcal{E}$ is open iff the pullback of any [[bounded geometric morphism]] with codomain $\mathcal{E}$ is [[skeletal geometric morphism|skeletal]] iff the pullback of any [[localic geometric morphism]] with codomain $\mathcal{E}$ is [[skeletal geometric morphism|skeletal]].
=--

This result appears as corollary 4.9 in [Johnstone (2006)](#J06). 

## Related entries

* [[open morphism]]
* [[open subtopos]]
* [[proper geometric morphism]]

## References

* [[Peter Johnstone]], _Open maps of toposes_, Manuscripta Math. **31** no.1-3 (1980) pp.217-247. ([gdz](http://gdz.sub.uni-goettingen.de/dms/load/pdf/?PPN=GDZPPN002222744))

* {#J02}[[Peter Johnstone]], _[[Sketches of an Elephant]] vol.II_ , Oxford UP 2002. (section C3.1, pp.606-625)

* {#J06}[[Peter Johnstone]], _Complemented sublocales and open maps_ , Annals of Pure and Applied Logic **137** (2006) pp.240&#8211;255.

* [[André Joyal]], [[Myles Tierney]], _An extension of the Galois theory of Grothendieck_, Mem. Amer. Math. Soc. **309**
(1984).

* {#MM94}[[Saunders Mac Lane]], [[Ieke Moerdijk]], _[[Sheaves in Geometry and Logic]]_ , Springer Heidelberg 1994&#178;. (sections IX.6-8, pp.493ff; X.3, pp.535-538)

[[!redirects open geometric morphisms]]