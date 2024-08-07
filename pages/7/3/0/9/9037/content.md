
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Differential geometry
+--{: .hide}
[[!include synthetic differential geometry - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

What are now called _Hitchin functionals_ are [[functions]]/[[functionals]] on spaces of [[differential n-forms]] on [[manifolds]] of [[dimension]] 6 or 7, for $n = 3$ and/or $n =4$. They are such that their [[critical points]] characterize holomorphic 3-forms of [[complex manifolds]] in dimension 6, as [[associative 3-forms]] of [[G₂-manifolds]] in dimension 7.

## Definition

### In 6 dimensions

Let $X$ be a [[closed manifold|closed]] [[orientation|oriented]] [[smooth manifold]] of [[dimension]] 6. 

For $\Omega \in \wedge^3 \Gamma(T^* X)$ a [[differential n-form|differential 3-form]] on $X$, write 

* ${\vert \lambda \Omega \vert} \in (\wedge^6 \Gamma(T^* X))^{\otimes 2}$

* $\sqrt{\vert \lambda \Omega \vert} \in \wedge^6 \Gamma(T^* X)$.

The _Hitchin function_ on 3-forms is the function

$$
  \wedge^3 \Gamma(T^* X) \to \mathbb{R}
$$

which sends 3-form to the [[integration of differential forms]] of this 6-form over $X$

$$
  \Omega \mapsto \int_X \sqrt{\vert \lambda (\Omega) \vert}
  \,.
$$

### In 7 dimensions

Let $X$ be 7-dimensional.

Let $\Omega \in \wedge^3 \Gamma(T^* X)$ be a [[stable differential form]]. This determines a [[Riemannian metric]] $\g_\Omega$ on $X$. Write $\star_\Omega$ for the corresponding [[Hodge star operator]]. The _Hitchin functional_ now is the function that takes stable forms to 

$$
  \int_X \Omega \wedge \star_\Omega \Omega
  \,.
$$

## Properties

### In 6 dimensions

A differential 3-form $\Omega$ such that $\lambda(\Omega) \lt 0$ is a [[critical point]] of the above functional precisely if there is the structure of a [[complex manifold]] on $X$ such that $\Omega$ is the real part of a non-vanishing holomorphic 3-form.

This is ([Hitchin, theorem 13](#Hitchin00)).

### In 7 dimensions

(...)

## Related concepts

* [[Calabi-Yau manifold]], [[G₂-manifold]]

* [[topological M-theory]]

## References

The original articles are

* [[Nigel Hitchin]], _The geometry of three-forms in six and seven dimensions_, ([arXiv:math/0010054](http://arxiv.org/abs/math/0010054))
 {#Hitchin00}

* [[Nigel Hitchin]], _Stable forms and special metrics_ ([arXiv:math/0107101](http://arxiv.org/abs/math/0107101))
 {#Hitchin01}

Reviews with a perspective on the role of the functionals in [[physics]]/[[gravity]]/[[string theory]]/[[topological M-theory]] include

* [[Robbert Dijkgraaf]], [[Sergei Gukov]], [[Andrew Neitzke]], [[Cumrun Vafa]], _Topological M-theory as Unification of Form Theories of Gravity_ ([arXiv:hep-th/0411073v2](http://arxiv.org/abs/hep-th/0411073v2))


[[!redirects Hitchin functionals]]

[[!redirects Hitchin's functional]]
[[!redirects Hitchin's functionals]]

