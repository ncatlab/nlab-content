
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Group Theory
+-- {: .hide}
[[!include group theory - contents]]
=--
#### Duality
+--{: .hide}
[[!include duality - contents]]
=--
=--
=--
#Contents#
* table of contents
{:toc}

## Statement

[[Pontryagin duality]] restricts to an [[equivalence of categories]] between [[abelian group|abelian]] [[profinite groups]] and (the [[opposite category|opposite]] of) [[abelian group|abelian]] [[torsion groups]] 

Notice that for $G$ a [[profinite group]] then $hom(G,\mathbb{R}/\mathbb{Z})\simeq hom(G,\mathbb{Q}/\mathbb{Z})$ and so one usually writes this equivalence as

$$
  hom(-,\mathbb{Q}/\mathbb{Z})
  \;\colon\;
  ProFinAb
  \stackrel{\simeq}{\longrightarrow}
  TorsionAb^{op}
$$

## Examples

* $\mathbb{Q}/\mathbb{Z}$ is dual to the [[profinite completion of the integers]] $\hat \mathbb{Z}$. And so the canonical map $\mathbb{Z} \longrightarrow \hat \mathbb{Z}$ is dual to $\mathbb{Q}/\mathbb{Z} \longrightarrow \mathbb{R}/\mathbb{Z}$.

* The abelian group underlying the [[p-adic integers]] $\mathbb{Z}_p$ is Pontryagin dual to the [[Prüfer p-group]] $\mathbb{Z}[p^{-1}]/\mathbb{Z}$.

$$
  \array{
     &\mathbb{Z}[p^{-1}]/\mathbb{Z}
     &\hookrightarrow&
     \mathbb{Q}/\mathbb{Z}
     &\hookrightarrow&
     \mathbb{R}/\mathbb{Z}
     \\
     {}^{\mathllap{hom(-,\mathbb{R}/\mathbb{Z})}}\downarrow
     \\
     &\mathbb{Z}_p
     &\leftarrow&
     \hat \mathbb{Z}
     &\leftarrow&
     \mathbb{Z}
  }
$$

## References

* [[Jean-Pierre Serre]], section 1.1. of _Galois cohomology_

* Ramakrishnan, Valenza, _Fourier analysis on number fields_

* [[Clark Barwick]], _Exercises on locally compact abelian groups: An invitation to harmonic analysis_  ([pdf](isites.harvard.edu/fs/docs/icb.topic651578.files/suppprobsLCA.pdf))
