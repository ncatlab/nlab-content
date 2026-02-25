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

A _Reissner-Nordström wormhole_ is an [[Einstein-Rosen bridge]] constructed from the [[Reissner-Nordström spacetime]] of a [[black hole]].

## Formulation

Let $M$ be the mass and $Q$ be the charge, then the [[Reissner-Nordström spacetime]] is given by:
$$
\mathrm{d}^2s
=\left(
1
-\frac{2M}{r}
+\frac{Q^2}{r^2}
\right)\mathrm{d}^2t
+\left(
1
-\frac{2M}{r}
+\frac{Q^2}{r^2}
\right)^{-1}\mathrm{d}^2r
+r^2\mathrm{d}\Omega.
$$
The [[event horizons]] lie at the radii $r_\pm=M\pm\sqrt{M^2-Q^2}$. The idea of an [[Einstein-Rosen bridge]] is now to transform the parameter $r\in\mathbb{R}^+$ into a parameter $u\in\mathbb{R}$ with:
$$
u^2
=r-r_+.
$$
Since there is no $u$ for $r\lt r_+$, one $u$ for $r=r_+$ and two $u$ for $r\gt r_+$, the transformation topologically describes glueing the exterior part of the [[Reissner-Nordström spacetime]] to itself along the [[event horizon]]. One has the following transformation for the differential and the radial component:
$$
2u\mathrm{d}u
=\mathrm{d}r;
$$$$1-\frac{2M}{r}+\frac{Q^2}{r^2}
\rightarrow \frac{u^2}{(u^2+r_+)^2}\left(u^2+\sqrt{r_\mathrm{S}^2-4r_\mathrm{Q}^2}\right).$$
$$\mathrm{d}s^2
=-\frac{u^2}{(u^2+r_+)^2}\left(u^2+2\sqrt{M^2-Q^2}\right)c^2\mathrm{d}t^2+4(u^2+r_+)^2\left(u^2+2\sqrt{M^2-Q^2}\right)^{-1}\mathrm{d}u^2
+(u^2+r_+)\mathrm{d}\Omega^2
$$

## Related concepts

[[!include charged and rotating black holes -- table]]