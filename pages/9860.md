
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Symplectic geometry
+--{: .hide}
[[!include symplectic geometry - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

A kind of [[correspondence]] space between [[Poisson manifolds]].

## Definition

+-- {: .num_defn}
###### Definition

For $(X_1, \pi_1)$ and $(X_2, \pi_2)$ two [[Poisson manifolds]], a _symplectic dual pair_ between them is a [[correspondence]] [[symplectic manifold]] $(Z,\pi_Z = \omega^{-1})$

$$
  (X_1, \pi_1) \stackrel{i_1}{\leftarrow} (Z,\omega) \stackrel{i_2}{\to} (X_2, \pi_2)
$$

such that for all $f_1 \in C^\infty(X_1)$ and $f_2 \in C^\infty(X_2)$ the [[Poisson bracket]] on $Z$ vanishes:

$$
  \{i_1^\ast f_1, i_2^\ast f_2\}_{\omega} = 0
  \,.
$$

=--

## Examples

+-- {: .num_example}
###### Example

A [[Lagrangian correspondence]] between [[symplectic manifolds]], regarded as [[Poisson manifolds]], is a symplectic dual pair.

=--

## Morita Equivalence

One may also impose additional conditions on $i_1$ and $i_2$. Suppose $i_1$ and $i_2$ are Poisson and anti-Poisson maps that are complete, constant rank with connected, simply-connected fibers satisfying the symplectic orthogonality of $i_1^\ast C^\infty (X_1)$ and $i_2^\ast C^\infty (X_2)$. Then this gives the notion of Morita equivalence between $X_1$ and $X_2$ as Poisson manifolds.

## Related concepts

* [[symplectic category]]

## References

The notion was introduced in

* M.V. Karasev, (1989), _The Maslov quantization conditions in higher cohomology and analogs of notions developed in Lie theory for canonical fibre bundles of symplectic manifolds I, II_ Selecta Math. Soviet. 8, 213&#8211;234, 235&#8211;258.

and

* [[Alan Weinstein]], _The local structure of Poisson manifolds_, J. Diff. Geom. 18, 523&#8211;557 (1983)

A textbook accounts are in

* Ch. 4 _Dual pairs_, in: A. Cannas da Silva, [[Alan Weinstein]], _Geometric models for noncommutative algebras_, Berkeley Math. Lec. Notes Series, AMS 1999, [pdf](http://math.berkeley.edu/%7Ealanw/Models.pdf)
*  J.-P. Ortega, T.S. Ratiu, _Momentum maps and Hamiltonian reduction_, Progress in Math. 222, Birkhauser 2004

Other

* Paul Skerritt, Cornelia Vizman, _Dual pairs for matrix Lie groups_, [arxiv/1805.01519](https://arxiv.org/abs/1805.01519)

A review with an eye towards [[geometric quantization]] with codomain [[KK-theory]] ([[geometric quantization by push-forward]]) is in section 3 of 

* [[Klaas Landsman]], _Functorial quantization and the Guillemin-Sternberg conjecture_,  Proc. Bialowieza 2002 ([arXiv:math-ph/0307059](http://arxiv.org/abs/math-ph/0307059))



[[!redirects symplectic dual pairs]]
