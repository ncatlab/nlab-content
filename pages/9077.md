
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Group Theory
+-- {: .hide}
[[!include group theory - contents]]
=--
#### Differential geometry
+--{: .hide}
[[!include synthetic differential geometry - contents]]
=--
#### $\infty$-Lie theory
+--{: .hide}
[[!include infinity-Lie theory - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}


## Definition

Let $G$ be a [[compact topological group|compact]] [[Lie group]]. 

A **[[torus]]** in $G$ is an [[abelian group|abelian]] [[subgroup]] $T \hookrightarrow G$ which is [[connected topological space|connected]] (and [[compact topological group|compact]]). Note that any compact connected abelian Lie group must be a torus, hence the name.

A **maximal torus** is a subgroup which is maximal with these properties.

The [[Lie algebra]] of a maximal torus of $G$ is a [[Cartan subalgebra]] of the Lie algebra of $G$.

## Properties
 {#Properties}

Suppose throughout that the [[compact Lie group]] $G$ is [[connected topological space|connected]].

+-- {: .num_prop #CartanTheorem}
###### Proposition

Given a choice of maximal torus $T \hookrightarrow G$, then each element $g \in G$ is [[adjoint action|conjugate]] to an element of its maximal torus, i.e. there exists $h_g \in G$ such that $h_g g h_g^{-1} \in T \hookrightarrow G$.

=--

(e.g. [Johansen, theorem 2.7.3](#Johansen))

+-- {: .num_remark}
###### Remark

For the [[unitary group]] $U(n)$, by example \ref{InUnitaryGroup},  prop. \ref{CartanTheorem} is the [[spectral theorem]] that unitary matrices may be diagonalized.

=--

+-- {: .num_cor}
###### Corollary

Any two choices of maximal tori are conjugate.

=--

(e.g. [Johansen, corollary 2.7.5](#Johansen))

+-- {: .num_prop}
###### Proposition

Any two elements of a maximal torus $T\hookrightarrow G$ are conjugate in $G$ precisely if they are conjugate via the [[Weyl group]]. 

=--

(e.g. [Johansen, prop 2.7.13](#Johansen))

+-- {: .num_cor}
###### Corollary

The [[conjugacy classes]] of $G$ are in bijection to $T/W(G,T)$.

=-- 

+-- {: .num_prop} 
###### Proposition 
Under the assumptions on $G$, the [[exponential map]] $\exp: \mathfrak{g} \to G$ is [[surjection|surjective]]. 
=-- 

+-- {: .proof} 
###### Proof 
The [[exponential map]] $\mathbb{R} \to S^1$ is surjective; similarly, if $\mathfrak{h}$ is a [[Cartan subalgebra]] of $\mathfrak{g}$, then the exponential map $\mathfrak{g} \to G$ maps $\mathfrak{h}$ homomorphically onto a maximal torus. Also the exponential map $\mathfrak{g} \to G$ preserves conjugation by any element of $G$, i.e., $\exp(g x g^{-1}) = g\exp(x)g^{-1}$. Then surjectivity follows from Proposition \ref{CartanTheorem}. 
=-- 


## Examples

+-- {: .num_example #InUnitaryGroup}
###### Example

The maximal torus of a [[unitary group]] $U(n)$ is the subgroup $U(1)^n\hookrightarrow U(n)$ of diagonal matrices with unitary entries.

=--

+-- {: .num_example}
###### Example


The maximal torus of the [[special unitary group]] $SU(n+1)$ is again $U(1)^n$ (one dimension lower) included as the subgroup of diagonal matrices whose first $n$ diagonal entries are arbitrary elements of $U(1)$ and whose last diagonal entry is the inverse of their product.

=--

+-- {: .num_example}
###### Example

The maximal torus of the [[special orthogonal group]] $SO(2n)$ and $SO(2n+1)$ is $U(1)^n \simeq SO(2)^n$ included block-diagonal (with, in the odd-dimensional case, the remaining block entry being the unit).

=--



## Related concepts

* [[maximal subgroup]]

* [[maximal compact subgroup]]

* [[Cartan subalgebra]]

* [[weight (in representation theory)]], [[root (in representation theory)]]

* [[Weyl group]]

* [[orbit method]]

## References

e.g.

* {#Johansen} Troels Roussauc Johansen, section 2.6 of _Character Theory for Finite Groups and Compact Lie Groups_ [pdf](http://www.math.upb.de/~johansen/character-theory.pdf)


[[!redirects maximal tori]]