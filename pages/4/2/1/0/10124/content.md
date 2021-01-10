
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Higher algebra
+--{: .hide}
[[!include higher algebra - contents]]
=--
=--
=--



#Contents#
* table of contents
{:toc}

## Idea


For $R \in CRing_\infty$ an [[E-∞ ring]], the [[(∞,1)-modules]] over $R$ with [[homomorphisms]] between them form an [[(∞,1)-category]], the _$(\infty,1)$-category of $(\infty,1)$-modules over $R$_.

## Properties

### Compact generation, dualizable and perfect objects
 {#CompactGeneration}

+-- {: .num_prop}
###### Propositon

Let $R$ be an [[A-∞ ring]]. The (∞,1)-category of ∞-modules $R Mod$ is a [[compactly generated (∞,1)-category]] and the [[compact object in an (∞,1)-category|compact objects]] coincide with the [[perfect modules]]

If $R$ is commutative ([[E-∞ ring|E-∞]]) then the perfect modules (and hence the compact objects) also coincide with the [[dualizable objects]].


=--

The first statement is ([[Higher Algebra|HA, prop. 7.2.4.2]]), the second ([[Higher Algebra|HA, prop. 7.2.4.4]]). For [[chain complexes]] this also appears as ([BFN 08, lemma 3.5](#BFN08)).

### Stable Dold-Kan correspondence
 {#StableDoldKan}

For $R$ an ordinary [[ring]], write $H R$ for the corresponding [[Eilenberg-MacLane spectrum]]. 

+-- {: .num_theorem #StableDoldKan}
###### Theorem

For $R$ any [[ring]] (or [[ringoid]], even) there is a [[Quillen equivalence]] 

$$
  H R Mod \simeq Ch_\bullet(R Mod)
$$

between model structure on  $H R$-module spectra and the [[model structure on chain complexes]] (unbounded) of ordinary $R$-[[module]]s.

This presents a corresponding [[equivalence of (∞,1)-categories]]. If $R$ is a commutative ring, then this is an equivalence of [[symmetric monoidal (∞,1)-categories]].

=--

This equivalence on the level of [[homotopy categories]] is due to ([Robinson](#Robinson)). The refinement to a Quillen equivalence is ([SchwedeShipley, theorem 5.1.6](#SchwedeShipley)). See also the discussion at _[[stable model categories]]_. A direct description as an equivalence of $(\infty,1)$-categories appears as ([Lurie, theorem 7.1.2.13](#Lurie)).



+-- {: .num_remark}
###### Remark

This is a stable version of the [[Dold-Kan correspondence]]. 

=--


See at __[[algebra spectrum]]_ for the corresponding statement for $H R$-algebra spectra and [[dg-algebras]].


### Periodicity

For $E$ a [[periodic ring spectrum]], then $E Mod$ ought to inherit a $\mathbb{Z}/2\mathbb{Z}$-[[∞-action]]. See at _[periodic ring spectrum -- Periodicity of modules](periodic+ring+spectrum#PeriodicityOnModules)_
## Related concepts

* [[Mod]]

* [[2Mod]]

* [[nMod]]


## References

Modules over algebras over an arbitrary [[(∞,1)-operad]] are discussed in  section 3.3 of 

* [[Jacob Lurie]], _[[Higher Algebra]]_

Modules specifically over [[A-∞ algebras]] are discussed in section 4.2 there.

The equivalence between the [[homotopy categories]] of  $H R$-module spectra and $Ch_\bullet(R Mod)$ is due to

* Alan Robinson, _The extraordinary derived category_ , Math. Z. 196 (2) (1987) 231&#8211;238.
 {#Robinson}

The refinement of this statement to a [[Quillen equivalence]] is due to

* [[Stefan Schwede]], [[Brooke Shipley]], _Stable model categories are categories of modules_ , Topology 42 (2003), 103-153 ([pdf](http://www.math.uic.edu/~bshipley/classTopFinal.pdf))
 {#SchwedeShipley}

Discussion in the context of [[derived algebraic geometry]] includes

* {#BFN08} [[David Ben-Zvi]], [[John Francis]], [[David Nadler]], section 3.1 of _Integral Transforms and Drinfeld Centers in Derived Algebraic Geometry_, J. Amer. Math. Soc. 23 (2010), no. 4, 909-966 ([arXiv:0805.0157](http://arxiv.org/abs/0805.0157))

[[!redirects (∞,1)-categories of (∞,1)-modules]]

[[!redirects (∞,1)-category of ∞-modules]]
[[!redirects (∞,1)-categories of ∞-modules]]
[[!redirects (infinity,1)-category of (infinity,1)-modules]]
[[!redirects (infinity,1)-categories of (infinity,1)-modules]]

[[!redirects (∞,1)-category of modules]]
[[!redirects (∞,1)-categories of modules]]
[[!redirects (infinity,1)-category of modules]]
[[!redirects (infinity,1)-categories of modules]]


[[!redirects (∞,1)Mod]]
