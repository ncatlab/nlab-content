+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Group Theory
+-- {: .hide}
[[!include group theory - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

Given an [[inner product space]] $V = (V,\langle-,-\rangle)$, the *[[orthogonal group]]* of $V$ is the subgroup of the [[general linear group]] $GL(V)$ which leaves the inner product invariant.

## Definition

Given an element $A$ of $GL(V)$, we say it _preserves the inner product_ $\langle-,-\rangle$ if $\langle A v ,A w \rangle = \langle v,w \rangle$ for all $v,w\in V$.

+-- {: .num_prop #inner_product_preserving_elements_closed}
###### Proposition

 If $A$ and $B$ preserve the inner product on $V$, then so do $AB$ and $A^{-1}$.
=--

We thus see that we have a group.

+-- {: .num_defn #def_of_O_n}
###### Definition
The **orthogonal group** $O(V,\langle-,-\rangle)$ is the subgroup of $GL(V)$ consisting of those elements that preserve the inner product.
=--


(... more detail ...)

## As a Lie group

When the base field is $\mathbb{R}$, $\mathbb{C}$ or $\mathbb{H}$ (the last being a [[skewfield]], but this is okay), and the vector space is finite-dimensional then we can put the structure of a finite-dimensional  [[manifold]] on $O(V,\langle-,-\rangle)$. We shall denote the group in this case by $O(n,\mathbb{K})$ where $V = \mathbb{K}^n$, $\mathbb{K} \in \{ \mathbb{R},\mathbb{C},\mathbb{H}\}$ and we take the 'standard' inner products on these spaces.

A relatively easy way to see that $O(n,\mathbb{K})$ is a manifold is that it is a smooth [[affine variety]] in [[Euclidean space]], but this requires some machinery. We can however construct explicit [[charts]] for $O(n,\mathbb{K})$ as a real manifold.

### Charts on the underlying manifold

One can use the algebra structure on matrices over the base [[field]] (or base [[division ring]]) of $V$ to define [[charts]] which are different to the charts one gets via the [exponential map](/nlab/show/exponential+map#exp_of_Lie_groups).

For $A \in O(n,\mathbb{K})$ Define the sets 
$$
  \Omega(A) := \{ X\in O(n,\mathbb{K}) | A + X \in GL(V) \}
$$
and
$$
  T_{A^\dagger} := \{ Y\in M_n(\mathbb{K}) | AY + (AY)^\dagger = 0 \}.
$$
Here $T_{A^\dagger}$ is a vector space, and will turn out to be the tangent space to $O(n,\mathbb{K})$ at $A^\dagger$.



+-- {: .num_prop #isomorphism_of_opens_with_tangent_spaces}
###### Proposition 
There is an isomorphism $c_A\colon \Omega(A) \stackrel{\sim}{\to} T_{A^\dagger}$.
=--
+-- {: .proof}
###### Proof
The map $c_A$ is defined as 
$$
  X \mapsto (I - A^\dagger X)(A + X)^{-1} = (I - A^\dagger X)(I + A^\dagger X)^{-1}A^\dagger
$$
the latter equality using that $A^{-1} = A^\dagger$. We need to check that this is indeed a map to $T_{A^\dagger}$ and that it is an isomorphism. 

Since
$$
   (A c_A(X))^\dagger = A c_I(A^\dagger X)^\dagger A^\dagger,
$$
if we show that $c_I(A^\dagger X)^\dagger = - c_I(A^\dagger X)$ we are done. Let $Z = X^\dagger A$, which is again in $O(n,\mathbb{K})$. Then
$$
\begin{aligned}
    c_I(Z)^\dagger & = \left( (I - Z)(I + Z)^{-1} \right)^\dagger\\
    & = \left( (I - Z)Z^\dagger Z^{\dagger -1}(I + Z)^{-1} \right)^\dagger\\
    & = \left( -(I - Z^\dagger)(I + Z^\dagger)^{-1} \right)^\dagger \\
    & = -(I + Z)^{-1}(I - Z)
\end{aligned}
$$
(tbc...)


=--



## Examples

* [[Euclidean space]] $\mathbb{R}^n$ with the standard inner product $\langle\mathbf{x},\mathbf{y}\rangle = \mathbf{x}\cdot\mathbf{y}$ has as orthogonal group the standard [[orthogonal group]] $O(n)$.

* The finite-dimensional [[Hilbert space]] $\mathbb{C}^n$ with the standard inner product has as orthogonal group $U(n)$, the [[unitary group]]

* The space $\mathbb{H}^n$, for $\mathbb{H}$ the [[quaternions]], has an inner product ... such that the corresponding orthogonal group is the [[compact symplectic group]] $Sp(n)$.

* (...Examples of indefinite signature go here...)