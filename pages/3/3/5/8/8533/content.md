

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Higher algebra
+--{: .hide}
[[!include higher algebra - contents]]
=--
#### Higher linear algebra
+-- {: .hide}
[[!include homotopy - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

The notion of _$(\infty,1)$-module_ over an [[monoid object in an (∞,1)-category]] (for instance an [[A-∞ ring]] or [[E-∞ ring]]) is the generalization to ([[stable homotopy theory|stable]])[[homotopy theory]] of the notion of [[module]] over a [[ring]].

## Definition

See at _[[module over an algebra over an (∞,1)-operad]]_.

## Examples

* in the [[stable (∞,1)-category of spectra]]: [[module spectrum]] over an [[ring spectrum]]

## Properties

### Compact modules

+-- {: .num_prop}
###### Propositon

Let $R$ be an [[A-∞ ring]]. The (∞,1)-category of ∞-modules $R Mod$ is a [[compactly generated (∞,1)-category]] and the [[compact object in an (∞,1)-category|compact objects]] coincide with the [[perfect modules]]

=--

([[Higher Algebra|HA, prop. 8.2.5.2]])


### Relation to fiberwise stabilization

By the discussion an [[tangent (∞,1)-category]] we may realize $E_\infty$-modules over $R$ as objects in the [[stabilization]] of the [[over-(∞,1)-category]] over $R$:

+-- {: .num_prop}
###### Proposition

Let $E_\infty := Alg^{Comm}(\infty Grpd)$ be the [[(∞,1)-category]] of [[E-∞ ring]]s and let $R \in E_\infty$. Then the [[stabilization]] of the [[over-(∞,1)-category]] over $A$ 

$$
  Stab(E_\infty/R) \simeq A Mod(Spec)
$$

is equivalentl to the category of $R$-module spectra.

=--

This is ([Lurie, cor. 1.5.15](#Lurie)).


### Stable Dold-Kan correspondence
 {#StableDoldKanCorrespondence}

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



+-- {: .num_example}
###### Example

For $X$ a [[topological space]] and $R$ a ring, let $C_\bullet(X, R)$ be the standard [[chain complex]] for [[singular homology]] $H_\bullet(X, R)$ of $X$ with coefficients in $R$.

Under the stable Dold-Kan correspondence, prop. \ref{StableDoldKan}, this ought to be identified with the [[smash product]] $(\Sigma^\infty_+ X) \wedge H R$ of the [[suspension spectrum]] of $X$ with the [[Eilenberg-MacLane spectrum]]. Notice that by the general theory of [[generalized homology]] the [[homotopy groups]] of the latter are again singular homology

$$
  \pi_\bullet( (\Sigma^\infty_+ X) \wedge H R) \simeq H_\bullet(X, R)
  \,.
$$

While the correspondence $(\Sigma^\infty_+ X) \wedge H R \sim C_\bullet(X,R)$ under the above equivalence is suggestive, maybe nobody has really checked it in detail. It is sort of stated as true for instance on <a href="http://arxiv.org/PS_cache/arxiv/pdf/0906/0906.5198v1.pdf#page=15">p. 15 </a> of ([BCT](#BCT)).

=--



## Related concepts

* [[action]], [[∞-action]]

* [[module]], **$(\infty,1)$-module**

  * [[(∞,1)-category of (∞,1)-modules]]

  * [[tensor product of ∞-modules]]

  * [[(∞,1)-module bundle]]

  * [[perfect module]]

* [[2-module]]

* [[bimodule]]

  [[(∞,1)-bimodule]]

* [[(∞,n)-module]]

* [[representation]], [[∞-representation]]




## References

Discussion in terms of [[module objects]] in [[symmetric smash product of spectra|symmetric monoidal]] [[model categories of spectra]] includes

* [[Anthony Elmendorf]], [[Igor Kriz]], [[Peter May]], section 5 of _[[Modern foundations for stable homotopy theory]]_ ([pdf](http://hopf.math.purdue.edu/Elmendorf-Kriz-May/modern_foundations.pdf))


Modules over algebras over an arbitrary [[(∞,1)-operad]] are discussed in  section 3.3 of 

* [[Jacob Lurie]], _[[Higher Algebra]]_

Modules specifically over [[A-∞ algebras]] are discussed in section 4.2 there.

Further discussion of [[(infinity,n)-bimodules]] is in

* {#Haugseng14} [[Rune Haugseng]], _The higher Morita category of $E_n$-algebras_ ([arXiv:1412.8459](http://arxiv.org/abs/1412.8459))

The equivalence between the [[homotopy categories]] of  $H R$-module spectra and $Ch_\bullet(R Mod)$ is due to

*{#Robinson}  Alan Robinson, _The extraordinary derived category_ , Math. Z. 196 (2) (1987) 231&#8211;238.
 

The refinement of this statement to a [[Quillen equivalence]] is due to

* {#SchwedeShipley} [[Stefan Schwede]], [[Brooke Shipley]], _Stable model categories are categories of modules_ , Topology 42 (2003), 103-153 ([pdf](http://www.math.uic.edu/~bshipley/classTopFinal.pdf))
 

Applications to [[string topology]] are discussed in

* {#BCT} [[Andrew Blumberg]], [[Ralph Cohen]], [[Constantin Teleman]], _Open-closed field theories, string topology and Hochschild homology_ ([arXiv:0906.5198](http://arxiv.org/abs/0906.5198))
 

See the section on string topology at [[sigma model]] for more on this.

[[!redirects ∞-module]]
[[!redirects infinity-modules]]
[[!redirects ∞-modules]]

[[!redirects infinity-module]]

[[!redirects (∞,1)-module]]
[[!redirects (∞,1)-modules]]
[[!redirects (infinity,1)-modules]]

