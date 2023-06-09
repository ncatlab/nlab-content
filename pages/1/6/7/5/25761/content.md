
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Differential cohomology
+--{: .hide}
[[!include differential cohomology - contents]]
=--
#### Complex geometry
+--{: .hide}
[[!include complex geometry - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}


## Idea
 {#Idea}

What is called *Hodge-filtered cohomogy* &lbrack;[Hopkins & Quick (2014)](#HopkinsQuick14)&rbrack; is the variant of [[differential generalized cohomology]] obtained by passing from real [[differential geometry]] to [[complex geometry]]: 

Where [[differential cohomology]] by default  pairs a given   [[Whitehead-generalized cohomology theory]] $E$ of [[underlying]] [[topological spaces]] with the degree-filtered $E_\bullet \otimes \mathbb{R}$-valued [[de Rham complexes]] of [[differential forms]] on real [[smooth manifolds]], the Hodge-filtered variant pairs instead with the [[Hodge filtration|Hodge filtered]] $E_\bullet \otimes \mathbb{C}$-valued [[Dolbeault complexes]], namely really (see [there](Hodge+structure#HodgeFiltrationForComplexSpaceReproducesKaehlerHodgeStructure)) with the degree-filtered [[holomorphic de Rham complexes]].

Concretely, for $p \in \mathbb{Z}$, the *Hodge-filtered $E$-cohomology* $E^\bullet_{\mathcal{D}}(p)(\mathcal{X})$ of a [[complex manifold]] $\mathcal{X}$, or more generally of an [[infinity-stack|$\infty$-stack]] over the [[site]] $Mfd_{\mathbb{C}}$ of all [[complex manifolds]] (with [[open covers]]), is the [[cohomology]] in the [[(infinity,1)-category|$\infty$-category]] of [[(infinity,1)-sheaves of spectra|$(\infty,1)$-sheaves of spectra]] $Sp\big(Sh_\infty(Mfd_{\mathbb{C}})\big)$ which is represented by the [[homotopy fiber product]]-spectrum

\[
  \label{DefiningHomotopyPullback}
  E_{\mathcal{D}}(p)
  \;\;
    \coloneqq
  \;\;
  E
  \underset{
    \Omega^{\geq p}(\text{-};\pi_{\bullet}(E)\otimes \mathbb{C})
  }{\times}
    \Omega^{\bullet}(\text{-};\pi_{\bullet}(E)\otimes \mathbb{C})  
  \,,
\]
where

* $E$ denotes the [[spectrum]] [[Brown representability theorem|representing]] the given [[Whitehead-generalized cohomology theory]] $E$ and regarded as a [[locally constant infinity-stack|locally constant $\infty$-stack]];

* $\Omega^\bullet(\text{-};A_\bullet)$ denotes the [[abelian sheaf]] of [[chain complexes]] given by the [[holomorphic de Rham complex]] with [[coefficients]] in a [[graded abelian group]] $A_\bullet$ and understood as an [[(infinity,1)-sheaf of spectra|$(\infty,1)$-sheaf of]] [[Eilenberg-MacLane spectra]] via the [[stable Dold-Kan correspondence]];

* $\Omega^{\geq p}(A_\bullet)$ denotes the subcomplex of $\geq p$-forms, similarly regarded,

* $E$ is regarded as fibered over $\Omega^\bullet\big(\text{-};A_\bullet\big)$ via the "[[complexification]]" map on $E$ given by [[smash product]] $E \simeq E \wedge \mathbb{S}\longrightarrow E \wedge H \mathbb{C}$ with the [[unit]] of the [[ring spectrum]] $H \mathbb{C}$ (what we may recognize as the [[Chern-Dold character]]) or rather (to be compatible with [[Pierre Deligne]]'s original convention) that map followed by the [[automorphism]] which in degree $2n$ is given by multiplication with $(2 \pi \mathrm{i})^n \,\in\, \mathbb{C}$ .

This is [Hopkins & Quick (2014), Def. 4.2](#HopkinsQuick14), being the direct holomorphic analog of the respective definition of [[differential cohomology]] (cf. the *[[differential cohomology hexagon]]*) in [[Quadratic Functions in Geometry, Topology, and M-Theory|Hopkins & Singer (2005)]] (except for that conventional rescaling by $(2\pi \mathrm{i})^{\bullet/2}$.)

In the special case where $E \,\coloneqq\, H\mathbb{Z}$ is [[integral cohomology|integral]] [[ordinary cohomology]] the above homotopy pullback (eq:DefiningHomotopyPullback) reproduces the [[Deligne complex]] in its original form (see the details spelled out [there](Deligne+cohomology#TheDifferentialHexagonForDeligne); but the key observation may be recognized already in the classical review of [Esnault & Viehweg (1988), Def. 2.6](Deligne+cohomology#EsnaultViehweg88)), whence the subscript "$\mathcal{D}$" in the above definition may be read as being for "generalized Deligne cohomology".
 
## References

### General

The general concept of Hodge-filtered [[differential cohomology]] and introducing the special case of Hodge-filtered [[complex cobordism cohomology]]:

* {#HopkinsQuick14} [[Michael J. Hopkins]], [[Gereon Quick]], *Hodge filtered complex bordism*, Journal of Topology **8** 1 (2014) 147-183 &lbrack;[arXiv:1212.2173](https://arxiv.org/abs/1212.2173), [doi:10.1112/jtopol/jtu021](https://doi.org/10.1112/jtopol/jtu021)&rbrack;

### Hodge filtered ordinary cohomology

The case of Hodge-filtered [[integral cohomology|integral]]$\;$[[ordinary cohomology]] is the original definition of *[[Deligne cohomology]]*, see [there](Deligne+cohomology#References) for references.

### Hodge-filtered complex cobordism

The case of Hodge filtered [[differential cobordism cohomology theory|differential]] [[MU]]-[[cobordism cohomology theory]]

* [Hopkins & Quick (2014), §5](#HopkinsQuick14)

Introduction and survey:

* [[Gereon Quick]], *Geometric Hodge filtered complex cobordism*, [talk at](Center+for+Quantum+and+Topological+Systems#QuickMar2023) *[[CQTS]]* (March 2023) &lbrack;video:[YT](https://www.youtube.com/watch?v=pMu0gT5kIBo)&rbrack;

A geometric cocycle model:

* [[Knut B. Haus]], [[Gereon Quick]], *Geometric Hodge filtered complex cobordism* &lbrack;[arXiv:2210.13259](https://arxiv.org/abs/2210.13259)&rbrack;

Refinement of the [[Abel-Jacobi map]] to [[Hodge filtration|Hodge filtered]] [[differential cobordism cohomology theory|differential]] [[MU]]-[[cobordism cohomology theory]]:

* [[Gereon Quick]], *An Abel-Jacobi invariant for cobordant cycles*, Documenta Mathematica **21** (2016) 1645–1668 &lbrack;[arXiv:1503.08449](https://arxiv.org/abs/1503.08449)&rbrack;


On [[Umkehr maps]] in this context:

* [[Knut Bjarte Haus]], [[Gereon Quick]], *Geometric pushforward in Hodge filtered complex cobordism and secondary invariants* &lbrack;[arXiv:2303.15899](https://arxiv.org/abs/2303.15899)&rbrack;

[[!redirects Hodge-filtered differential cohomology theory]]


[[!redirects Hodge-filtered cohomology]]
[[!redirects Hodge-filtered cohomology theory]]




