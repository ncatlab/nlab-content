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
=--
=--

#Contents#
* table of contents
{:toc}
## Idea

A _Schwarzschild wormhole_ is an [[Einstein-Rosen bridge]] constructed from the [[Schwarzschild spacetime]] of a [[black hole]].

## Formulation

Let $M$ be the mass, then the [[Schwarzschild spacetime]]  is given by: 
$$
\mathrm{d}^2s
=\left(
1
-\frac{2M}{r}
-\frac{\Lambda}{3}r^2
\right)\mathrm{d}^2t
+\left(
1
-\frac{2M}{r}
-\frac{\Lambda}{3}r^2
\right)^{-1}\mathrm{d}^2r
+r^2\mathrm{d}\Omega.
$$
The [[event horizon]] lies at the Schwarzschild radius $r_S=2M$. The idea of an [[Einstein-Rosen bridge]] is now to transform the parameter $r\in\mathbb{R}^+$ into a parameter $u\in\mathbb{R}$ with:
$$
u^2
=r-r_S.
$$
Since there is no $u$ for $r\lt r_S$, one $u$ for $r=r_S$ and two $u$ for $r\gt r_S$, the transformation topologically describes glueing the exterior part of the [[Schwarzschild spacetime]] to itself along the [[event horizon]]. One has the transformation for the differential and the radial component:
$$
2u\mathrm{d}u
=\mathrm{d}r;
$$
$$1-\frac{2M}{r}
=\frac{r-2M}{r}
=\frac{u^2}{u^2+2M}
$$
This results in the wormhole metric:
$$
\mathrm{d}s^2
=-\frac{u^2}{u^2+2M}c^2\mathrm{d} t^2
+4(u^2+2M)\mathrm{d}u^2
+(u^2+2M)^2\mathrm{d}\Omega^2.
$$

## Related concepts

[[!include charged and rotating black holes -- table]]