
#Contents#
* table of contents
{:toc}

## Definition

Let $\rho_r: S^1 \to S^1/C_r$ be the homeomorphism $z \mapsto \sqrt[r] z$, $C_r \coloneqq \mathbb{Z}/r\mathbb{Z}$. 

Given an $S^1$-space $X$, denote by $\rho^{\ast}_r X^{C_r}$ the $S^1$&#8211;space obtained by pulling back the $S^1/C_r$ action on $X^{C_r}$ via $\rho_r$, where $X^{C_r}$ is the [[homotopy fixed point]] space of the induced [[cyclic group]] action. Then $\rho^{\ast}_r(\rho^{\ast}_s X^{C_s})^{C_r} =\rho^{\ast}_{r s} X^{C_{r s}}$.

+-- {: .num_example}
###### Definition

A _cyclotomic space_ is 

1. a [[topological space]] $X$

1. equipped with a [[continuous function|continuous]] [[circle group]] [[action]] 

   (hence a [[topological G-space]] for $G = S^1$)

1. and equipped with a family of $S^1$-equivariant [[weak homotopy equivalences]] $R_r: \rho^{\ast}_r X^{C_r} \to X$, for $r \geq 1$, such that $R_1 = id$, and $R_{r s} = R_r \circ \rho^{\ast}_r R_s^{C_r}$.


=--

([Schl 09, def. 4.3](#Schl09), [AGHL 12, def. 3.6](#AGHL12))

## Properties

A [[free loop space]], $\mathcal{L} X$, is a cyclotomic space, where $S^1$ acts by rotation of loops.

Let $R X = \underset{R_r}{holim} \rho^{\ast}_r X^{C_r}$. Then $R$ is a [[comonad]] on the category of cyclotomic spaces.

The $S^1$-equivariant suspension spectrum of a cyclotomic space is a [[cyclotomic spectrum]].

## Related concepts

* [[cyclotomic spectrum]]

* [[cyclic space]]

## References

* {#Schl09} [[Christian Schlichtkrull]], _The cyclotomic trace for symmetric ring spectra_, Geometry & Topology Monographs 16 (2009), 545&#8211;592, ([pdf](/http://msp.org/gtm/2009/16/gtm-2009-16-014s.pdf)), ([arXiv:0903.3495](https://arxiv.org/abs/0903.3495))

* {#AGHL12} [[Vigleik Angeltveit]], [[Teena Gerhardt]], [[Michael Hill]], Ayelet Lindenstrauss, _On the algebraic K-theory of truncated polynomial algebras in several variables_ ([arXiv:1206.0247](https://arxiv.org/abs/1206.0247))

[[!redirects cyclotomic spaces]]


