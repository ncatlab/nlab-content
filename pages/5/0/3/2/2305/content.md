
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Cohomology
+--{: .hide}
[[!include cohomology - contents]]
=--
#### Differential geometry
+--{: .hide}
[[!include synthetic differential geometry - contents]]
=--
=--
=--


#Contents#
* table of contents 
{:toc}

## Idea

The _de Rham complex_  (named after [[Georges de Rham]]) $\Omega^\bullet(X)$ of a [[space]] $X$ is the [[cochain complex]] that in degree $n$ has the [[differential form]]s (which may mean: [[Kähler differential form]]s) of degree $n$, and whose [[differential]] is the **de Rham differential** or **exterior derivative**.

As $X$ varies this constitutes an [[abelian sheaf]] of complexes.

## Definition

### For smooth manifolds

The **de Rham complex** of a [[smooth manifold]] is the [[cochain complex]] which in degree $n \in \mathbb{N}$ has the [[vector space]] $\Omega^n(X)$ of degree-$n$ [[differential forms]] on $X$. The coboundary map is the deRham _[[exterior derivative]]_. The [[chain cohomology|cohomology]] of the de Rham complex is __de Rham cohomology__. Under the [[wedge product]], the deRham complex becomes a [[differential graded algebra]]. This may be regarded as the [[Chevalley?Eilenberg algebra]] of the [[tangent Lie algebroid]] $T X$ of $X$.

The corresponding [[abelian sheaf]] in this case defines a [[smooth spectrum]] via the [[stable Dold-Kan correspondence]], see at _[smooth spectrum -- Examples -- De Rham spectra](smooth+spectrum#ExamplesDeRhamSpectra)_.


### For algebraic objects

For [[smooth varieties]] $X$, algebraic de Rham cohomology is defined to be the [[hypercohomology]] of the de Rham complex $\Omega_X^\bullet$.

De Rham cohomology has a rather subtle generalization for possibly singular algebraic varieties due to ([Grothendieck](#Grothendieck)). 

For [[analytic spaces]]

* T. Bloom, M. Herrera, _De Rham cohomology of an analytic space_, Inv. Math. __7__ (1969), 275-296, [doi](http://dx.doi.org/10.1007/BF01425536)

### For cohesive homotopy types
 {#ForCohesiveHomotopyTypes}

In the general context of [[cohesive homotopy theory]] in a [[cohesive (∞,1)-topos]] $\mathbf{H}$, for $A \in \mathbf{H}$ a [[cohesive homotopy type]], then the [[homotopy fiber]] of the [[counit of a comonad|counit]] of the [[flat modality]]

$$
  \flat_{dR} A \coloneqq fib(\flat A \to A)
$$

may be interpreted as the de Rham complex with [[coefficients]] in $A$.

This is the [[codomain]] for the [[Maurer-Cartan form]] $\theta_{\Omega A}$ on $\Omega A$ in this generality. The [[shape modality|shape]] of $\theta_{\Omega A}$ is the general [[Chern character]] on $\Pi(\Omega A)$.

For more on this see at

* _[structures in a cohesive infinit-topos -- de Rham cohomology](cohesive+%28infinity%2C1%29-topos+--+structures#deRhamCohomology)_

More precisely, $\flat_{dR} \Sigma A$ and $\Pi_{dR} \Omega A$ play the role of the non-negative degree and negative degree part, respectively of the de Rham complex with coefficients in $\Pi \flat_{dR} \Sigma A$. For more on this see at 

* _[differential cohomology diagram -- de Rham coefficients](differential%20cohomology%20diagram#DeRhamCoefficients)_.

## Properties

### Basic theorems

* [[Poincare lemma]] 

* [[de Rham theorem]]

### Relation to Deligne complex


See at _[[Deligne complex]]_

## Related concepts

* [[pullback of differential forms]]

* [[equivariant de Rham cohomology]]

* [[twisted de Rham cohomology]]

* [[Deligne cohomology]]

* [[de Rham space]]

* [[Lie algebra valued differential forms]]

* [[L-infinity algebra valued differential forms]]

* [[absolute de Rham cohomology]]

* [[Dolbeault complex]], [[Dolbeault cohomology]]

* [[Hodge-de Rham spectral sequence]]

* [[chiral de Rham complex]]

* [[crystalline cohomology]], [[comparison theorem (crystalline cohomology)]]

* [[Hodge cohomology]]

## References

### In differential geometry

(...)

### In algebraic geometry

A useful introduction is 

* Kiran Kedlaya, _$p$-adic cohomology, from theory to practice_ ([pdf](http://swc.math.arizona.edu/aws/2007/KedlayaNotes11Mar.pdf))

A classical reference on the algebraic version is

* [[Alexander Grothendieck]], _On the De Rham cohomology of algebraic varieties_, Publications Math&#233;matiques de l'IH&#201;S __29__, 351-359 (1966), [numdam](http://www.numdam.org/item?id=PMIHES_1966__29__95_0).
 {#Grothendieck}
* A. Grothendieck, _Crystals and the de Rham cohomology of schemes_, in Giraud, Jean; Grothendieck, Alexander; Kleiman, Steven L. et al., Dix Expos&#233;s sur la Cohomologie des Sch&#233;mas, Advanced studies in pure mathematics __3__, Amsterdam: North-Holland, pp. 306&#8211;358, [MR0269663](http://www.ams.org/mathscinet-getitem?mr=0269663), [pdf](http://www.math.jussieu.fr/~leila/grothendieckcircle/DixExp.pdf)
* [[Robin Hartshorne]], _On the de Rham cohomology of algebraic varieties_, Publ. Math&#233;matiques de l'IH&#201;S __45__ (1975), p. 5-99 [MR55#5633](http://www.ams.org/mathscinet-getitem?mr=55:5633)
* P. Monsky, _Finiteness of de Rham cohomology_, Amer. J. Math. __94__ (1972), 237&#8211;245, [MR301017](http://www.ams.org/mathscinet-getitem?mr=301017), [doi](http://dx.doi.org/10.2307/2373603)

See also

* Yves Andr&#233;, _Comparison theorems between algebraic and
analytic De Rham cohomology_ ([pdf](http://www.emis.de/journals/JTNB/2004-2/pages335-355.pdf))

* [[Mikhail Kapranov]], _DG-Modules and vanishing cycles_ ([[KapranovDGModuleVanishingCycle.pdf:file]])

[[!redirects deRham complex]]
[[!redirects deRham algebra]]
[[!redirects de Rham algebra]]
[[!redirects deRham dga]]
[[!redirects de Rham dga]]
[[!redirects deRham dg-algebra]]
[[!redirects de Rham dg-algebra]]
[[!redirects de Rham cohomology]]
[[!redirects deRham cohomology]]

[[!redirects de Rham complex]]

[[!redirects de Rham complexes]]