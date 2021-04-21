[[!redirects Bubble of nothing]]
[[!redirects Bubble of nothing]]
[[!redirects Bubble of nothing]]
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Gravity
+--{: .hide}
[[!include gravity contents]]
=--
#### Physics
+--{: .hide}
[[!include physicscontents]]
=--
#### Quantum field theory
+--{: .hide}
[[!include functorial quantum field theory - contents]]
=--
#### String theory
+-- {: .hide}
[[!include string theory - contents]]
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

A *bubble of nothing* in the sense of [Witten 82](#Witten82) is an instability of the [[Kaluza-Klein]] [[vacuum]] where a [[gravitational instanton]] mediates the decay of a $5$-dimensional [[Euclidean]] [[Schwarzschild spacetime]] into nothing:
the hole in space grows at the [[speed of light]] until it hits [[null infinity]], leading to the "annihilation" of spacetime.

## Construction of the solution

Let us start from the spacetime $(\mathbb{R}^{4}-B_R^3)\times S^1$, where $B_R^3$ is a [[ball]] of radius $R$ and $S^1$ is a circle of radius $R_5$, equipped with the following [[Euclidean]] [[Schwarzschild metric]]:
$$ g \;=\; r^2\mathrm{vol}_{S^3} + \frac{\mathrm{d}r^2}{1-\frac{R^2}{r^2}} + R_5^2 \left(1-\frac{R^2}{r^2}\right)\mathrm{d}\theta^2,$$
where $\theta$ is the coordinate on the circle and $r$ is the radius of $\mathbb{R}^{4}$.

Let the volume of the $3$-sphere be $\mathrm{vol}_{S^3} = \mathrm{d}\chi^2 + \sin(\chi)\mathrm{vol}_{S^2}$. We can now go back to the Minkowski signature by the [[Wick rotation]] $\psi := -i\chi + i\frac{\pi}{2}$. Thus, we have
$$ g \;=\; -r^2\mathrm{d}\psi^2 + \frac{\mathrm{d}r^2}{1-\frac{R^2}{r^2}} + r^2\cosh^2(\psi)\mathrm{vol}_{S^2} + R_5^2 \left(1-\frac{R^2}{r^2}\right)\mathrm{d}\theta^2.$$


## Properties

By change of coordinates $\rho := r\cosh(\psi)$ and $t:=r\sinh(\psi)$, we see that at large radius the metric goes to the [[Minkowski metric]]
$$\lim_{r\rightarrow \infty}g \;=\; -\mathrm{d}t^2 +\mathrm{d}\rho^2 + \rho^2\mathrm{vol}_{S^2}+R_5^2\mathrm{d}\theta^2.$$

However, the coordinates $(t,\rho)$ parametrize all the $4$-dimensional base manifold but the region $\{ \rho^2 - t^2 \leq R \}$ of the bubble.
The boundary of the bubble in the $4$-dimensional base space has a radius which grows with time as
$$ \rho_{\mathrm{BON}}(t) \;=\;\sqrt{R^2+t^2}.$$
Moreover, the effective size of the circle compactification will be depend on $r$ by
$$ R_{5}(r) \;=\; R_5\sqrt{1-\frac{R^2}{r^2}},$$
so that it goes to $0$ for $r\rightarrow R$ and it goes to $R_5$ for for $r\rightarrow \infty$.


## Related concepts

  * [[Coleman-De Luccia instanton]]

  * [[Kaluza-Klein theory]]

  * [[swampland]]

  * [[instanton]]

    * [[gravitational instanton]]

  * [[double dimensional reduction]]

  * [[moduli stabilization]]

  * [[landscape of string theory vacua]]

    * [[flux compactification]]

    * [[supersymmetry and Calabi-Yau manifolds]]

    * [string theory FAQ -- What does it mean to say that string theory has a "landscape" of solutions?](string%20theory%20FAQ#WhatDoesItMeanToSayStringTheoryHasALandscapeOfSolutions)


## References

* {#Witten82} [[Edward Witten]], _Instability of the Kaluza-Klein Vacuum_, Nucl. Phys. B195 (1982) 481-492 (<a href="https://doi.org/10.1016/0550-3213(82)90007-4">doi:10.1016/0550-3213(82)90007-4</a>).


[[!redirects Bubble of nothing]]
[[!redirects Bubble of nothing]]
[[!redirects Bubble of nothing]]