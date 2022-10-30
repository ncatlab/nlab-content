
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

## Idea

For $R \in CRing_\infty$ an [[E-∞ ring]], the [[(∞,1)-modules]] over $R$ with [[homomorphisms]] between them form an [[(∞,1)-category]], the _$(\infty,1)$-category of $(\infty,1)$-modules over $R$_.

## Properties

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


[[!redirects (∞,1)-categories of (∞,1)-modules]]

[[!redirects (∞,1)-category of ∞-modules]]
[[!redirects (∞,1)-categories of ∞-modules]]
[[!redirects (infinity,1)-category of (infinity,1)-modules]]
[[!redirects (infinity,1)-categories of (infinity,1)-modules]]


[[!redirects (∞,1)Mod]]

