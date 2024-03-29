
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Elliptic cohomology
+-- {: .hide}
[[!include elliptic cohomology -- contents]]
=--
#### Geometry
+--{: .hide}
[[!include higher geometry - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

A _nodal_  [[singular point of an algebraic variety|singularity]] of an [[algebraic curve]] is one of the form parameterized by the [[equation]] $x y = 0$. A _nodal curve_ is a curve with a nodal singularity.

(e.g. [Hain 08, p. 45](#Hain08))


## The nodal cubic

The nodal [[cubic curve]] (over some base) is (see at _[elliptic curve -- Nodal curves and cuspidal curves](elliptic+curve#EllipticCurvesNodalCurvesCuspidalCurves)_ for notation and background) the solution to the [[Weierstrass equation]] for which the [[discriminant]] vanishes, but the modular invariant $c_4$ does not.

This is equivalently the limit in which the [[j-invariant]] $j = \frac{c_4^3}{\Delta}$ goes to $\infty$.

## Properties of the nodal cubic


### Compactified moduli stack of elliptic curves and the Tate curve

The nodal [[cubic curve]] is not an [[elliptic curve]], as it is singular, but adding it to the [[moduli stack of elliptic curves]] $\mathcal{M}_{ell}$ produces the [[Deligne-Mumford compactification|compactification]] $\mathcal{M}_{\overline{ell}}$ which is often relevant.

The [[formal neighbourhood]] of the nodal curve in $\mathcal{M}_{\overline{ell}}$ is the [[Tate curve]].

### Over the complex numbers
 {#OverTheComplexNumbers}

Over the [[complex numbers]], the nodal cubic $E_0$ is the [[Riemann sphere]]/complex [[projective space]] $\mathbb{P}^1$ with the pole points 0 and $\infty$ identified (hence is a "[[complex manifold|complex]] [[torus]] with one cycle shrunk away"). Precisely: there is a [[holomorphic function]]

$$
  \mathcal{P}^1 \to \mathcal{P}^2
$$

which is onto $E_0 \subset \mathcal{P}_2$, sends the unit of the [[multiplicative group]] $1 \in \mathbb{C}^\times \hookrightarrow \mathbb{P}^1$ to the unit of $E_0$, maps $0,\infty \in \mathbb{P}^1$ both to the nodal singular double point of $E_0$ and is [[injective]] away from these points (e.g. [Hain 08, exercise 47, p. 45](#Hain08))

$$
  \array{
     \mathbb{C}^\times &\hookrightarrow& E_0
     \\
     \downarrow^\mathrlap{=} && \downarrow
     \\
     \mathbb{P}^1-\{0,\infty\} &\longrightarrow& \mathbb{P}^2
  }
  \,.
$$

<img src="http://ncatlab.org/nlab/files/ADE2Cycle.jpeg" width="220" alt="ADE 2Cycle" />

### Formal group and height

The [[formal group]] associated with a nodal cubic curve is of [[height of a formal group|height]] 1.  Indeed, passing to the point of the nodal curve in $\mathcal{M}_{\overline{ell}}$ connects [[elliptic cohomology]] (of [[chromatic level]] 2) to [[topological K-theory]] (of chromatic level 1). For more on this see at _[[moduli stack of tori]]_ and at _[tmf -- Properties -- Maps to K-theory and to Tate K-theory](tmf#MapToTateKTheory)_.

### Relation to gauge enhancement in F-theory

In [[F-theory]] the nodal singularity locus of the given [[elliptic fibration]] is interpreted as the locus of [[D7-branes]], see at _[F-brane scan](F-theory#Fbranescan)_.


## Related concepts

* [[cusp]]

* [[augmented Teichmüller space]]

* in [[F-theory]] the points where the fibers of the [[elliptic fibration]] degenerate to the nodal curve are where the [[D7-branes]] are located

## References

Discussion over the [[complex numbers]] is in 

* {#Hain08} [[Richard Hain]], section 5.2 of _Lectures on Moduli Spaces of Elliptic Curves_ ([arXiv:0812.1803](http://arxiv.org/abs/0812.1803))


[[!redirects nodal curves]]

[[!redirects nodal cubic curve]]
[[!redirects nodal cubic curves]]

[[!redirects nodal cubic]]
[[!redirects nodal cubics]]

[[!redirects nodal singularity]]
[[!redirects nodal singularities]]

