+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Equivariant higher algebra
+--{: .hide}
[[!include equivariant higher algebra - contents]]
=--
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
Indexed coproducts are to [[tensor products]] as [[equivariant symmetric monoidal categories]] are to [[symmetric monoidal categories]].

## Definition

Let $H \subset G$ be a subgroup of a finite group and $S \in \mathbb{F}_H$ a finite $H$-set. 
The equivalence $\Ind_H^G:\mathbb{F}_H \xrightarrow \sim \mathbb{F}_{G,/[G/H]}$ identifies $S$ with a canonical map $\psi_S:\Ind_H^G S \rightarrow [G/H]$.

Postcomposition along $\psi_S$ yields a [[natural transformation]] between [[evaluation map|evaluation functors]] $\ev_S = (-)_S = \prod_{[H/K_i] \in \mathrm{Orb}(S)} (-)_{K_i} \implies (-)_H = \ev_H$, each sending $\mathrm{Fun}(\mathrm{Span}(\mathbb{F}_G), \mathrm{Cat})$.
If $\mathcal{C}^{\otimes} \in \mathrm{Fun}(\mathrm{Span}(\mathbb{F}_G), \mathrm{Cat}_\infty)$ is [[product-preserving functor|product-preserving]] (i.e. it is a [[G-symmetric monoidal ∞-category]]), then we refer to the value of this natural transformation on $\mathcal{C}^{\otimes}$ as the **indexed tensor functor**, and write it as
$$
  \bigotimes_{K_i}^S:\mathcal{C}_S = \prod_{H/K_i \in \mathrm{Orb}(S)} \mathcal{C}_{K_i} \rightarrow \mathcal{C}_H.
$$


## Related concepts

* [[Parametrized Higher Category Theory and Higher Algebra]], [[G-∞-category]], [[equivariant symmetric monoidal category]]

* [[equivariant homotopy theory]]

## References

Originally, 

* {#HillHopkinsRavenel09} [[Michael Hill]], [[Michael Hopkins]], [[Douglas Ravenel]], *On the non-existence of elements of Kervaire invariant one*, Annals of Mathematics **184** 1 (2016)&lbrack;[doi:10.4007/annals.2016.184.1.1](https://doi.org/10.4007/annals.2016.184.1.1), [arXiv:0908.3724](http://arxiv.org/abs/0908.3724), [talk slides](https://www.math.rochester.edu/people/faculty/doug/otherpapers/Skye_handout.pdf)&rbrack; 

Since then,

* [[Denis Nardin]], [[Jay Shah]], _Parametrized and equivariant higher algebra_, ([arxiv:2203.00072](https://arxiv.org/abs/2203.00072))

* {#Barkan22} [[Shaul Barkan]], [[Rune Haugseng]], [[Jan Steinebrunner]], _Envelopes for Algebraic Patterns_, (2022) ([arXiv:2208.07183](https://arxiv.org/abs/2208.07183))

[[!redirects indexed coproducs]]

[[!redirects indexed product]]
[[!redirects indexed products]]