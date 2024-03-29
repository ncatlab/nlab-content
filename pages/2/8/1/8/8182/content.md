
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Symplectic geometry
+--{: .hide}
[[!include symplectic geometry - contents]]
=--
#### Geometric quantization
+--{: .hide}
[[!include geometric quantization - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

The notion of _Heisenberg Lie $n$-algebra_ is the generalization to [[n-plectic geometry]] of the notion of [[Heisenberg Lie algebra]] in [[symplectic geometry]].

The Heisenberg Lie $n$-algebra [[Lie integration|integrates]] to the _[[Heisenberg n-group]]_.


## Definition

We discuss a generalization of the notion of Heisenberg Lie algebra from ordinary [[symplectic geometry]] to a notion of _Heisenberg [[Lie n-algebra]]_  in [[higher geometric quantization]] of [[n-plectic geometry]]. 

The following definition is naturally motivated from the fact that:

1. The ordinary Heisenberg Lie algebra is the sub-Lie algebra of the 
[[Poisson bracket]] Lie algebra, the one underlying the corresponding [[Poisson algebra]] (see [below](#RelationToPoissonAlgebra)) on the constant and linear functions.

1. The generalization of [[Poisson bracket|Poisson brackets]] to [[Poisson Lie n-algebras]] in [[n-plectic geometry]] for all $n$ is established (see there).

In view of this, the following definition takes the Heisenberg Lie $n$-algebra to be the sub-Lie $n$-algebra of the [[Poisson Lie n-algebra]] on the linear and constant differential forms.

First we need the following definition, which is elementary, but nevertheless worth making explicit once.

+-- {: .num_defn}
###### Definition

Let $n \in \mathbb{N}$, let $(V, \omega)$ be an [[n-plectic vector space]]. 

The **corresponding $n$-plectic manifold** is the [[n-plectic manifold]] $(V, \mathbf{\omega})$, with $V$ now the canonical [[smooth manifold]] structure on the given vector space, and with 

$$
  \mathbf{\omega} \in \Omega^{n+1}(V)
$$

the [[differential form]] obtained by left (right) translating $\omega$ along $V$.

Explicitly, for all [[vector fields]] $\{v_i \in \Gamma(T V)\}_{i = 1}^n$ and all points $x \in V$ we set

$$
  \mathbf{\omega}_x(v_1, \cdots, v_n)
  :=
  \omega(v_1(x), \cdots, v_n(x))
  \,.
$$

Here on the right --  and in all of the following -- we are using that every [[tangent space]] $T_x V$ of $V$ is naturally identified with $V$ itself

$$
  T_x V \stackrel{\simeq}{\to} V
  \,.
$$

=--

+-- {: .num_defn}
###### Definition

Let $n \in \mathbb{N}$, 
let $(V, \omega)$ be an [[n-plectic vector space]]
and let $(V, \mathbf{\omega})$ be the corresponding
[[n-plectic manifold]].

The **Heisenberg Lie $n$-algebra** $Heis(V,\omega)$ is the sub-[[Lie n-algebra]] of the [[Poisson Lie n-algebra]] $\mathcal{P}(V, \omega)$ on those [[differential forms]] which are either linear or constant (with respect to left/right translation on $V$).

=--

All one has to observe is:

+-- {: .num_prop}
###### Proposition

This is indeed a sub-Lie $n$-algebra.

=--

+-- {: .proof}
###### Proof

We need to check that the linear and constant forms are closed under the [[L-infinity algebra]] brackets of $\mathcal{P}(V, \omega)$. 

The only non-trivial such brackets are the unary one, and the ones on elements all of degree 0. 

The unary bracket is given by the de Rham differential. Since this sends a linear form to a constant form and a constant form to 0, our sub-complex is closed under this.

Similarly, the brackets on elements all in degree 0 is given by contraction of $\mathbf{\omega}$ with the Hamiltonian vector fields of linear or constant forms. Since $\mathbf{\omega}$ is a constant form, and since the de Rham differential of a linear or constant form is constant (or even 0), these Hamiltonian vector fields are necessarily constant. Hence their contraction with $\mathbf{\omega}$ gives a constant form.

=--

## Related concepts

* the [[universal enveloping E-n algebra]] of a Heisenberg Lie n-algebra deserves to be called a _[[Weyl n-algebra]]_

[[!include slice automorphism groups in higher prequantum geometry - table]]


[[!include geometric quantization extensions - table]]


## References

The topological part of the Heisenberg Lie 2-algebra of the [[string]] [[sigma-model]] called the [[WZW model]] has been discussed (not under this name, though) in 

* [[John Baez]], [[Chris Rogers]], _Categorified Symplectic Geometry and the String Lie 2-Algebra_. [arXiv:0901.4721](http://arxiv.org/abs/0901.4721).

and shown to be the [[string Lie 2-algebra]].

General discussion in the broader context of [[higher differential geometry]] and [[higher prequantum geometry]] is in 

* {#FRS13a} [[Domenico Fiorenza]], [[Chris Rogers]], [[Urs Schreiber]], _[[schreiber:Higher geometric prequantum theory]]_ ([arXiv:1304.0236](http://arxiv.org/abs/1304.0236))

* {#FRS13b} [[Domenico Fiorenza]], [[Chris Rogers]], [[Urs Schreiber]], _[[schreiber:L-∞ algebras of local observables from higher prequantum bundles]]_, Homology, Homotopy and Applications, Volume 16 (2014) Number 2, p. 107 &#8211; 142 ([arXiv:1304.6292](http://arxiv.org/abs/1304.6292))


[[!redirects Heisenberg Lie n-algebras]]

[[!redirects Heisenberg Lie 2-algebra]]
[[!redirects Heisenberg Lie 2-algebras]]

[[!redirects Heisenberg L-∞ algebra]]
[[!redirects Heisenberg L-∞ algebras]]
[[!redirects Heisenberg L-infinity algebra]]
[[!redirects Heisenberg L-infinity algebras]]

