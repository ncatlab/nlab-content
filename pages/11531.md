
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
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

The **Arf-Kervaire invariant problem** asks whether certain hypothetical elements $\theta_j \in \pi^s_{2^{j+1} - 2}$ of the stable [[homotopy groups of spheres]] exist. In fact the definition of these elements works in all dimensions but due to a theorem of Browder they do not exist in dimensions $d\neq 2^{j+1} - 2$.

Prior to ([Hill-Hopkins-Ravenel 09](#HillHopkinsRavenel09)), all that was known rested on the explicit construction of such elements for $j=1,...,5$ (so in dimensions 2,6,14,30 and 62). HHR established that these elements do not exist for $j \gt 6$, so the only dimension in which existence remains unknown in 126 (ie $j=6$). The proof is by construction of a 256-periodic [[spectrum]] $\Omega$ and a [[spectral sequence]] for it that can detect the elements $\theta_j$ as elements of $\pi_*(\Omega)$. HHR then show that $\pi_n(\Omega)=0$ for $-4\lt n\lt 0$, which by the periodicity, implies that the images of $\theta_j$ must be elements of the trivial group, and hence are themselves trivial.

## Key properties of the $C_8$ fixed point spectrum $\Xi$

We write $\Xi$ to mean the spectrum "$\Omega$" discussed in [Hill-Hopkins-Ravenel 09](#HillHopkinsRavenel09).

### Detection theorem
It has an [[Adams-Novikov spectral sequence]] in which the image of each $\theta_j$ is non-trivial. This means if $\theta_j\in \pi_*(\mathbb{S})$ exists then it can be seen in $\pi_*(\Xi)$.

### Periodicity Theorem
The spectrum is 256-periodic, as in $\Omega^{256}\Xi \simeq \Xi$.

### Gap Theorem
We have $\pi_k(\Xi) = 0$ for $-4 \lt k \lt 0$. Its proof uses the [[slice spectral sequence]].

### Result

Suppose $\theta_7 \in \pi_{254}(\mathbb{S})$ exists then the detection theorem implies that it has a non-trivial image in $\pi_{254}(\Xi)$. But by the periodicity and gap theorems we see that $\pi_{254}(\Xi)$ is trivial. The argument for $j \ge 7$ is similar since $|\theta_j| = 2^{j+1} \equiv -2 \mod 256$.

## Related concepts

* [[Kervaire invariant]]

* [[Hopf invariant one problem]]

## References

The solution of the problem in the negative, except for one outstanding dimension (namely 126), appears in

* {#HillHopkinsRavenel09} [[Michael Hill]], [[Michael Hopkins]], [[Douglas Ravenel]], _On the non-existence of elements of Kervaire invariant one_, Annals of Mathematics Volume 184 (2016), Issue 1 ([doi:10.4007/annals.2016.184.1.1](https://doi.org/10.4007/annals.2016.184.1.1), [arXiv:0908.3724](http://arxiv.org/abs/0908.3724), [talk slides](https://www.math.rochester.edu/people/faculty/doug/otherpapers/Skye_handout.pdf)) 

* {#HillHopkinsRavenel} [[Michael Hill]], [[Michael Hopkins]], [[Douglas Ravenel]], _The Arf-Kervaire problem in algebraic topology: Sketch of the proof_, Current Developments in Mathematics, 2010: 1-44 (2011) ([[HHRKervaire.pdf:file]], [doi:10.4310/CDM.2010.v2010.n1.a1](https://dx.doi.org/10.4310/CDM.2010.v2010.n1.a1))

On the [[equivariant stable homotopy theory]] involved:

* [Hill-Hopkins-Ravenel 09, Appendix](#HillHopkinsRavenel09)

* [HillHopkinsRavenel, section 4](#HillHopkinsRavenel)

More resources are collected at

* [[Douglas Ravenel]], _[A solution to the Arf-Kervaire invariant problem](http://www.math.rochester.edu/people/faculty/doug/kervaire.html)_, web resources 2009

* {#HillHopkinsRavenelIntroduction} [[Michael Hill]], [[Michael Hopkins]], [[Douglas Ravenel]], _The Arf-Kervaire invariant problem in algebraic topology: introduction_, 2016
([pdf](http://math.ucla.edu/~mikehill/Research/CDMHistory.pdf))

[[!redirects Kervaire invariant one problem]]
[[!redirects Kervaire invariant problem]]