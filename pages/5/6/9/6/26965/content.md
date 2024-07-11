+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Homotopy theory
+--{: .hide}
[[!include homotopy - contents]]
=--
#### Stable Homotopy theory
+--{: .hide}
[[!include stable homotopy theory - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea
Indexed coproducts are to [[coproducts]] as [[equivariant symmetric monoidal categories]] are to [[symmetric monoidal categories]].

## Definition

\begin{definition}
If $\mathcal{C}$ is a [[G-∞-category]], $H \subset G$ a [[subgroup]], and $S$ a [[finite set|finite]] [[G-set|H-set]], by composing the [[diagonal functor]]  with [[restriction]], we have a [[functor]]
$$
  \Delta^S:\mathcal{C}_H \xrightarrow{\Delta} \prod_{H/K_i \in \mathrm{Orb}(S)} \mathcal{C}_{H} \xrightarrow{\Res} \prod_{H/K_i \in \mathrm{Orb}(S)} \mathcal{C}_{K_i}.
$$
If a pointwise [[left adjoint]] to $\Delta^S$ exists at a [[tuple]] $(X_{K_i})$, then the resulting object is denoted $\coprod_{K_i}^H X_{K_i}$ and called the **$S$-indexed coproduct of $(X_{K_i})$.**

Dually, if a pointwise [[right adjoint]] to $\Delta^S$ exists at a tuple $(X_{K_i})$, then the resulting object is denoted $\prod_{K_i}^H X_{K_i}$ and called the **$S$-indexed product of $(X_{K_i})$**.

\end{definition}

## Related concepts

* [[Parametrized Higher Category Theory and Higher Algebra]], [[G-∞-category]], [[equivariant symmetric monoidal category]]

* [[equivariant homotopy theory]]

## References

Originally, 

* {#HillHopkinsRavenel09} [[Michael Hill]], [[Michael Hopkins]], [[Douglas Ravenel]], *On the non-existence of elements of Kervaire invariant one*, Annals of Mathematics **184** 1 (2016)&lbrack;[doi:10.4007/annals.2016.184.1.1](https://doi.org/10.4007/annals.2016.184.1.1), [arXiv:0908.3724](http://arxiv.org/abs/0908.3724), [talk slides](https://www.math.rochester.edu/people/faculty/doug/otherpapers/Skye_handout.pdf)&rbrack; 

In higher category theory,

* {#PHCTI} [[Clark Barwick]], Emanuele Dotto, [[Saul Glasman]], [[Denis Nardin]], [[Jay Shah]], _Parametrized higher category theory and higher algebra: Expos&#233; I &#8211; Elements of parametrized higher category theory_, ([arXiv:1608.03657](https://arxiv.org/abs/1608.03657))

* {#Shah18} [[Jay Shah]], _Parametrized higher category theory_, ([arXiv:1809.05892](https://arxiv.org/abs/1809.05892))

* [[Jay Shah]], _Parametrized higher category theory II: Universal constructions_, ([arXiv:2109.11954](https://arxiv.org/abs/2109.11954))

[[!redirects indexed coproducs]]

[[!redirects indexed product]]
[[!redirects indexed products]]