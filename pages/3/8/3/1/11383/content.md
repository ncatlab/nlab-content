
> under construction

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Higher algebra
+--{: .hide}
[[!include higher algebra - contents]]
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

In analogy to how in ordinary [[algebra]] the natural [[logarithm]] of [[positive number|positive]] [[rational numbers]] is a [[group]] [[homomorphism]] from the [[group of units]] to the completion of the rationals by the (additive) [[real numbers]]

$$
  log \;\colon\; \mathbb{Q}^\times_{\gt 0}\longrightarrow \mathbb{R}
$$

so in [[higher algebra]] for $E$ an [[E-∞ ring]] there is a natural homomorphism

$$
  \ell_{n,p} \;\colon\; gl_1(E) \longrightarrow L_{K(n)} E
$$

from the [[∞-group of units]] of $E$ to the [[K(n)-local spectrum]] obtained from $E$ (see [Rezk 06, section 1.7](#Rezk06)).

On the [[cohomology theory]] [[Brown representability theorem|represented]] by &#167;E&#167; this induces a [[cohomology operation]] called, therefore, the "logarithmic cohomology operation".

## Definition

By the [[Bousfield-Kuhn construction]] there is an [[equivalence]] of spectra

$$
  L_{K(n)} gl_1(E) \simeq L_{K(n)}E
$$

between the [[K(n)-local spectrum]] induced by the [[∞-group of units]] of $E$ with that induced by $E$ itself. The logarithm on $E$ is the [[composition|composite]] of that with the [[Bousfield localization of spectra|localization map]]

$$
 \ell_{n,p}
  \;\colon\; 
 gl_1(E) \stackrel{}{\longrightarrow} L_{K(n)}gl_1(E) \stackrel{\simeq}{\to}  L_{K(n)} E
  \,.
$$

(see [Rezk 06, section 3](#Rezk06)).

## Properties

### Explicit formual in terms of power operations

Under some conditions there is an explicit formula of the logarithmic cohomology operation by a [[series]] of [[power operations]].

([Rezk 06, theorem 1.9](#Rezk06))

...

### Relation to the string-orientation of $tmf$


The abobve expression in terms of power operations may be used to establish the [[string orientation of tmf]] ([Ando-Hopkins-Rezk 10](#AndoHopkinsRezk10)).

...

## References

The expression in terms of [[power operations]] is due to

* {#Rezk06} [[Charles Rezk]], _The units of a ring spectrum and a logarithmic cohomology operation_, J. Amer. Math. Soc. 19 (2006), 969-1014 ([arXiv:math/0407022](http://arxiv.org/abs/math/0407022))

The application of this to the [[string orientation of tmf]] is due to

* {#AndoHopkinsRezk10} [[Matthew Ando]], [[Mike Hopkins]], [[Charles Rezk]], _Multiplicative orientations of KO-theory and the spectrum of topological modular forms_, 2010 ([pdf](http://www.math.uiuc.edu/~mando/papers/koandtmf.pdf))



[[!redirects logarithmic cohomology operations]]