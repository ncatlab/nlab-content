
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Symplectic geometry
+--{: .hide}
[[!include symplectic geometry - contents]]
=--
#### Higher geometry
+--{: .hide}
[[!include higher geometry - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

_Higher symplectic geometry_ is the generalization of [[symplectic geometry]] to the context of [[higher geometry]].

It involves two kinds of generalizations:

1. the [[symplectic form]] generalizes from a 2-form to a form of arbitrary arity. This aspect is called [[multisymplectic geometry]].

1. the base [[manifold]] is generalized to a [[smooth ∞-groupoid]] or [[∞-Lie algebroid]]. For binary symplectic forms this is called a [[symplectic Lie n-algebroid]].

In the full higher symplectic geometry both of these aspects are unified: a _multisymplectic $\infty$-groupoid_ is a [[smooth ∞-groupoid]] equipped with a [[smooth infinity-groupoid -- structures|differential n-form on smooth ∞-groupoids]] satisfying some condition.

Examples of higher symplectic geometries arise naturally as the [[covariant phase space]]s "over the point" or "in top codimension" (in the sense of [[extended topological quantum field theory]]) in systems of [[schreiber:∞-Chern-Simons theory]]: their $\infty$-multisymplectic form is the [[invariant polynomial]] that defines the theory.

## Definition

+-- {: .num_defn}
###### Definition

Let $\mathfrak{a}$ be an [[L-∞ algebroid]]. For $n \in \mathbb{N}$, an **[[n-plectic form]]** or **[[multisymplectic form]]** of $n$ arguments on $\mathfrak{a}$ is 

* an [[invariant polynomial]] $\omega$ on $\mathfrak{a}$ which is $n$-linear (takes $n$ arguments): 

  $$
    \omega \in  W^n(\mathfrak{a}) = \Omega^n(\mathfrak{a})
    \,;
  $$

* such that the contraction morphism

  $$
    \iota_{(-)}\omega : T \mathfrak{a} \to W^{n-1}(\mathfrak{a}) = \Omega^{n-1}(\mathfrak{a})
  $$

in injective.

=--

+-- {: .num_example}
###### Example

If $\mathfrak{a}$ is a Lie 0-algebroid (over a smooth manifold) then it is simply that [[smooth manifold]], $\mathfrak{a} = X$. In this case $W(\mathfrak{a}) = \Omega^{\bullet}(X)$ is the ordinary [[de Rham complex]] and an [[invariant polynomial]] is a closed [[differential form]] of positive degree.

In this case an $n$-plectic form on $\mathfrak{a}$ is a closed $n$-form $\omega(-,-,.\dots, -)$ on $X$ such that for every [[vector field]] $v \in \Gamma(T X)$ we have

$$
  (\omega(v,-,\cdots,-) = 0) \;\; \Rightarrow \;\;
  (v = 0).
$$

=--

## Applications

### Higher Chern-Simons theory

Every [[invariant polynomial]] $\omega$ induces an [[schreiber:∞-Chern-Simons theory]] [[action functional]]

$$
  S_{CS} : \Omega(\Sigma,\mathfrak{a}) \to \mathbb{R}
  \,.
$$

The [[variational calculus|variation]] of that functional is

$$
  \delta S_{CS} : A \mapsto \int_\Sigma \omega(\delta A, F_A, \cdots, F_A)
  \,.
$$

Therefore the condition that the invariant polynomial is $n$-plectic amounts to saying that $S_{CS}$ has no spurious global symmetries.

(...)

## Related concepts

* [[symplectic Lie n-algebroid]]

* [[symplectic ∞-groupoid]]

[[!include Isbell duality - table]]


## References

Discussion of what here we call "higher symplectic geometry over Lie 0-algebroids" ([[multisymplectic geometry]]) is in 

* [[Chris Rogers]], _Higher symplectic geometry_ PhD thesis ([arXiv](http://arxiv.org/abs/1106.4068)).

For more references see [[multisymplectic geometry]].