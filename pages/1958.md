
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Differential geometry
+-- {: .hide}
[[!include synthetic differential geometry - contents]]
=--
=--
=--

# Contents
* table of contents
{: toc}

## Idea

Given a [[differentiable manifold]] $X$, the __cotangent bundle__ $T^*(X)$ of $X$ is the [[dual vector bundle]] over $X$ dual to the [[tangent bundle]] $T x$ of $X$.


A __cotangent vector__ or __covector__ on $X$ is an element of $T^*(X)$.  The __cotangent space__ of $X$ at a point $a$ is the [[fiber]] $T^*_a(X)$ of $T^*(X)$ over $a$; it is a [[vector space]].  A __covector field__ on $X$ is a [[section]] of $T^*(X)$.  (More generally, a [[differential form]] on $X$ is a section of the [[exterior algebra]] of $T^*(X)$; a covector field is a __[[differential 1-form]]__.)

Given a covector $\omega$ at $a$ and a [[tangent vector]] $v$ at $a$, the pairing $\langle{\omega,v}\rangle$ is a [[scalar]] (a [[real number]], usually).  This (with some details about linearity and universality) is basically what it means for $T^*(X)$ to be the [[dual vector bundle]] to $T_*(X)$.  More globally, given a covector field $\omega$ and a [[tangent vector field]] $v$, the paring $\langle{\omega,v}\rangle$ is a scalar [[function]] on $X$.

Given a point $a$ in $X$ and a differentiable (real-valued) [[partial function]] $f$ defined near $a$, the __differential__ $\mathrm{d}_a f$ of $f$ at $a$ is a covector on $X$ at $a$; given a tangent vector $v$ at $a$, the pairing is given by
$$ \langle{\mathrm{d}_a f, v}\rangle = v[f] ,$$
thinking of $v$ as a [[derivation]] on [[differentiable functions]] defined near $a$.  (It is really the [[germ]] at $a$ of $f$ that matters here.)  More globally, given a differentiable function $f$, the __[[de Rham differential]]__ $\mathrm{d}f$ of $f$ is a covector field on $X$; given a vector field $v$, the pairing is given by
$$ \langle{\mathrm{d}f, v}\rangle = v[f] ,$$
thinking of $v$ as a derivation on differentiable functions.

One can also *define* covectors at $a$ to be germs of differentiable functions at $a$, modulo the [[equivalence relation]] that $\mathrm{d}_a f = \mathrm{d}_a g$ if $f - g$ is constant on some neighbourhood of $a$.  In general, a covector field won\'t be of the form $\mathrm{d}f$, but it will be a sum of terms of the form $h \mathrm{d}f$.  More specifically, a covector field $\omega$ on a coordinate patch can be written
$$ \omega = \sum_i \omega_i\, \mathrm{d}x^i $$
in local coordinates $(x^1,\ldots,x^n)$.
This fact can also be used as the basis of a definition of the cotangent bundle.

## Properties

### Symplectic structure
 {#SymplecticStructure}

Every cotangent bundle $T^\ast X$ carries itself a canonical [[differential 1-form]]

$$
  \theta
   \in
  \Omega^1(T^* X)
$$

with the property that under the [[isomorphism]]

$$
  j \;\colon\; \Gamma(T^* X) \stackrel{\simeq}{\to} \Omega^1(X)
$$

between [[differential 1-forms]] and smooth [[sections]] of the [[cotangent bundle]] we have for every smooth section $\sigma \in \Gamma(T^* X)$ the identification

$$
  \sigma^* \theta = j(\sigma)
$$

between the [[pullback of a differential form|pullback]] of $\theta$ along $\sigma$ and the 1-form corresponding to $\sigma$ under $j$.

This unique differential 1-form $\theta \in \Omega^1(T^* X)$ is called the **[[Liouville-Poincaré 1-form]]** or **canonical form** or **tautological form** on the cotangent bundle.


The [[de Rham differential]] $\omega \coloneqq d \theta$ is a [[symplectic form]]. Hence every cotangent bundle is canonically a [[symplectic manifold]].

On a [[coordinate chart]] $\mathbb{R}^n$ of $X$ with canonical [[coordinate functions]] denoted $(x^i)$, the cotangent bundle over the chart is $T^\ast \mathbb{R}^n \simeq \mathbb{R}^n \times \mathbb{R}^n$ with canonical coordinates $((x^i), (p_j))$. In these coordinates the canonical 1-form is (using [[Einstein summation convention]])

$$
  \theta = p_i d x^i
$$

and hence the [[symplectic form]] is 

$$
  \omega = d p_i \wedge d q^i
  \,.
$$

## Related concepts

* [[tangent bundle]]

* [[differential form]]

* [[exterior bundle]]

* [[Liouville-Poincaré 1-form]]

* [[principal symbol]], [[bicharacteristic flow]]

* [[wavefront set]], [[microlocal analysis]]

* [[microsupport]], [[microlocal sheaf theory]]

[[!redirects cotangent vector]]
[[!redirects cotangent vectors]]
[[!redirects covector]]
[[!redirects covectors]]

[[!redirects cotangent space]]
[[!redirects cotangent spaces]]
[[!redirects cotangent vector space]]
[[!redirects cotangent vector spaces]]

[[!redirects covector field]]
[[!redirects covector fields]]
[[!redirects cotangent vector field]]
[[!redirects cotangent vector fields]]
[[!redirects differential 1-form]]
[[!redirects differential 1-forms]]
[[!redirects smooth differential 1-form]]
[[!redirects smooth differential 1-forms]]
[[!redirects 1-form]]
[[!redirects 1-forms]]

[[!redirects cotangent bundle]]
[[!redirects cotangent bundles]]
[[!redirects Cotangent bundle]]
[[!redirects Cotangent bundles]]
