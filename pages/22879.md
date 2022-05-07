
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Complex geometry
+--{: .hide}
[[!include complex geometry - contents]]
=--
#### Homotopy theory
+--{: .hide}
[[!include homotopy - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

On the [[homotopy type]] of [[mapping spaces]] of [[rational maps]], mostly from a [[Riemann surface]] to a [[complex projective space]]...

## Related concepts

* [[Yang-Mills monopole]]

* [[Cohomotopy]]

* [[Oka principle]]

## Properties

* For $n \in \mathbb{N}_+$, consider [[complex projective n-space]]
$\mathbb{C}P^n$. 

* Say that a [[continuous map]] $f \;\colon\; \Sigma_2 \to \mathbb{C}P^n$ out of a 2-[[dimension of a manifold|dimensional]] [[manifold]] has *degree* $d \in \mathbb{N}$ if the [[pullback in cohomology|pullback]] of the generator $1 \in \mathbb{Z} \simeq H^2\big( \mathbb{C}P^n;\, \mathbb{Z}\big)$ is $f^\ast(1) = d \in \mathbb{Z} \simeq H^2(\Sigma_2;\, \mathbb{Z})$.

* For $\Sigma$ a [[compact topological space|compact]] [[connected topological space|connected]] [[Riemann surface]] write $g_\Sigma \in \mathbb{N}$ for its [[genus of a Riemann surface|genus]]. 

\begin{proposition}\label{SegalOnHomotopyTypeOfRationalMapsIntoCPn}
  For $\Sigma$ a [[compact topological space|compact]] [[connected topological space|connected]] [[Riemann surface]], the inclusion
  \[
    Maps_{
      {rat}
    }^{deg = d}
    \big(
      \Sigma
      ,\,
      \mathbb{C}P^n
    \big)
    \xhookrightarrow{ \;\; i \;\; }
    Maps_{
      {top}
    }^{deg = d}
    \big(
      \Sigma
      ,\,
      \mathbb{C}P^n
    \big)
  \]
  of 

  1. the [[topological subspace]] of [[rational maps]] to [[complex projective n-space]] into 

  1. the [[connected component]] of maps of [[degree of a map|degree]] $d$ of the [[mapping space]] (with the [[compact open topology]]) of all [[continuous maps]] 

is

* for $g_\Sigma = 0$ (i.e. $\Sigma$ the [[Riemann sphere]]):

  an [[isomorphism]] on [[homotopy groups]] in degrees $\leq d (2 n -1)$;

* for $g_\Sigma \geq 1$:

  an [[isomorphism]] on [[ordinary homology|ordinary]] [[homology groups]] in degrees $\leq (d - 2g) (2 n -1)$.

\end{proposition}
([Segal 1979, Prop. 1.2, 1.3](#Segal79))

\begin{example}
  In the special case that $n = 1$ and $\Sigma = S^2$ is the [[2-sphere]] with its [[complex structure]], so that both [[domain]] and [[codomain]] are the [[Riemann sphere]] $\mathbb{C}P^1$, Prop. \ref{SegalOnHomotopyTypeOfRationalMapsIntoCPn} says that
$$
    Maps_{
      {rat}
    }^{deg = d}
    \big(
      \mathbb{C}P^1
      ,\,
      \mathbb{C}P^1
    \big)
    \xhookrightarrow{ \;\; i \;\; }
    Maps_{
      {top}
    }^{deg = d}
    \big(
      S^2
      ,\,
      S^2
    \big)
$$

is an isomorphism on [[homotopy groups]] up to degree $\leq d$.
\end{example}
([Segal 1979, Prop. 1.1'](#Segal79)) This statement controls the classification of [[Yang-Mills monopoles]].

\begin{remark}\label{ComaprisonToHomotopicalOkaPrinciple}
  Prop. \ref{SegalOnHomotopyTypeOfRationalMapsIntoCPn} may be compared to the [homotopical Oka principle](Oka+principle#HomotopicalOkaPrinciple), which applies (since $\mathbb{C}P^n$ is an [[Oka manifold]] by [this Prop.](Oka+manifold#ComplexProjectiveSpaceIsOkaManifold)) to the complementary case of connected *non-compact* ("open") Riemann surfaces $\Sigma$ (which are [[Stein manifolds]] by [this Example](Stein+manifold#SteinSurfacesAreOpenRiemannSurfaces)), in which case it says that the corresponding inclusion of the space of [[holomorphic maps]]

$$
    Maps_{
      {hol}
    }
    \big(
      \Sigma
      ,\,
      \mathbb{C}P^n
    \big)
    \xhookrightarrow{ \;\; i \;\; }
    Maps_{
      {top}
    }
    \big(
      \Sigma
      ,\,
      \mathbb{C}P^n
    \big)
$$

induces an isomorphism on all [[homotopy groups]], hence is a [[weak homotopy equivalence]] -- reflecting the fact that non-compactness of the Riemann surfaces and absence of any asymptotic boundary condition provides a large supply of holomorphic functions.
\end{remark}

## References

Original article:

* {#Segal79} [[Graeme Segal]], _The topology of spaces of rational functions_, Acta Math. Volume 143 (1979), 39-72 ([euclid:1485890033](https://projecteuclid.org/euclid.acta/1485890033))

Further discussion:

* [[Fred Cohen]], [[Ralph Cohen]], [[B. M. Mann]], [[R. J. Milgram]], _The topology of rational functions and divisors of surfaces_, Acta Math (1991) 166: 163 ([doi:10.1007/BF02398886](https://doi.org/10.1007/BF02398886))

* [[Ralph L. Cohen]], [[John D. S. Jones]], [[Graeme B. Segal]], *Stability for holomorphic spheres and Morse theory*, in: K. Grove, I. H. Madsen, E. K. Pedersen (eds.) *Geometry and Topology: Aarhus*, Contemporary Mathematics
Volume: 258 (2000)  ([arXiv:math/9904185](https://arxiv.org/abs/math/9904185), [ ISBN:978-0-8218-2158-9](https://bookstore.ams.org/conm-258))

* Jacob Mostovoy, *Spaces of rational maps and the Stone–Weierstrass theorem*, Topology Volume 45, Issue 2, March 2006, Pages 281-293 ([arXiv:10.1016/j.top.2005.08.003](https://doi.org/10.1016/j.top.2005.08.003))

* Yasuhiko Kamiyama, *Remarks on spaces of real rational functions*, The Rocky Mountain Journal of Mathematics Vol. 37, No. 1 (2007), pp. 247-257 ([jstor:44239357](https://www.jstor.org/stable/44239357))

Generalization to the case that the [[codomain]] is 

...a [[Grassmannian]]:

* [[Frances Kirwan]], *On spaces of maps from Riemann surfaces to Grassmannians and applications to the cohomology of moduli of vector bundles*, Ark. Mat. 24(1-2): 221-275 (1985) ([doi:10.1007/BF02384399](https://www.projecteuclid.org/journals/arkiv-for-matematik/volume-24/issue-1-2/On-spaces-of-maps-from-Riemann-surfaces-to-Grassmannians-and/10.1007/BF02384399.full))

...a [[flag manifold]]:

* [[C. P. Boyer]], [[B. M. Mann]], [[J. C. Hurtubise]], [[R. J. Milgram]], *The topology of the space of rational maps into generalized flag manifolds*, Acta Mathematica. 1994 Mar 1;173(1):61-101 ([doi:10.1007/BF02392569](https://projecteuclid.org/journals/acta-mathematica/volume-173/issue-1/The-topology-of-the-space-of-rational-maps-into-generalized/10.1007/BF02392569.full))

* [[J. C. Hurtubise]], *Holomorphic maps of a Riemann surface into a flag manifold*, J. Differential Geom. 43(1): 99-118 (1996) ([doi:10.4310/jdg/1214457899](https://projecteuclid.org/journals/journal-of-differential-geometry/volume-43/issue-1/Holomorphic-maps-of-a-Riemann-surface-into-a-flag-manifold/10.4310/jdg/1214457899.full))

Application to [[Skyrmions]]:

* Steffen Krusch, *Homotopy of rational maps and the quantization of Skyrmions*, Annals of Physics Volume 304, Issue 2, April 2003, Pages 103-127 (<a href="https://doi.org/10.1016/S0003-4916(03)00014-9">doi:10.1016/S0003-4916(03)00014-9</a>)

[[!redirects homotopies of rational maps]]

[[!redirects homotopy type of spaces of rational maps]]
[[!redirects homotopy types of spaces of rational maps]]

[[!redirects homotopy type of spaces of rational functions]]
[[!redirects homotopy types of spaces of rational functions]]

