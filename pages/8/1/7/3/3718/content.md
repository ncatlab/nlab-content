

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Quantum systems
+--{: .hide}
[[!include quantum systems -- contents]]
=--
=--
=--

#Contents#
* table of contents 
{:toc}

## Idea

Since the space of [[quantum channels]] is a [[convex set|convex]] [[compact topological space]], every quantum channel may we written as a convex linear combination of the *extremal* points of this space. On [[finite-dimensional Hilbert spaces]] of [[dimension of a vector space|dimension]] 2 the extremal channels are exactly the [[unitary quantum channels]], but in higher dimensions there may be non-unitary extremal channels.

## Properties

### In terms of Kraus operators

> (old material which needs referencing)

A general quantum channel $T$, with Kraus operators $\{A\}_i$, is extremal if and only if the set 

$$
\left \{A_{k}^{\dagger}A_{l} \right \}_{k,l\ldots N}
$$

is linearly independent.

As a [[unital quantum channel]] $T$ is extremal if and only if the set

$$
  \left \{A_{k}^{\dagger}A_{l} \oplus A_{l}A_{k}^{\dagger} \right \}_{k,l \ldots N}
$$

is linearly independent.


### Under tensor product

In the case of CPT or UCP maps the tensor product preserves extremality, but this is not always the case for UCPT maps. &lbrack;[Miller & da Silva 2023](#MillerDaSilva23)&rbrack;

A sketch of the proof for CPT maps is as follows. A finite sequence of vectors is linearly independent iff its Gram matrix is invertible. If $(A_k)_k$ and $(B_l)_l$ are Kraus operators for two CPT maps, then $(A_k \otimes B_l)_{k,l}$ are Kraus operators for the tensor product. Also, if both $(A_k)_k$ and $(B_l)_l$ are linearly independent, then $(A_k \otimes B_l)_{k,l}$ is also linearly independent. If we assume that $(A_k)_k$ and $(B_l)_l$ represent extreme CPT maps, then $(A_k^\dagger A_{k'})_{k,k'}$ and $(B_l^\dagger B_{l'})_{l,l'}$ are linearly independent. Let $G$ be the Gram matrix of $(A_k^\dagger A_{k'})_{k,k'}$ and $G'$ be the Gram matrix of $(B_l^\dagger B_{l'})_{l,l'}$, then $G$ and $G'$ are invertible. Let also $G''$ be the Gram matrix of $((A_k \otimes B_l)^\dagger (A_{k'} \otimes B_{l'}))_{(k,l),(k',l')}$. Extremality is preserved if $((A_k \otimes B_l)^\dagger (A_{k'} \otimes B_{l'}))_{(k,l),(k',l')}$ is linearly independent, which is equivalent to $G''$ being invertible. It follows that $G'' = G \otimes G'$ (Kronecker product). Using the properties of the Kronecker product and the invertibility of both $G$ and $G'$ we conclude that $G''$ is invertible.

A proof for the case of UCP maps may be obtained by the duality between CPT and UCP maps.

In the case of UCPT maps extremality is not always preserved. It is still preserved if one of the channels is over a space of dimension 2, since for dimension 2 the extreme UCPT maps are unitary channels. For higher dimensions one can construct counterexamples. A reason for this to happen is that if the UCPT maps are over a space of dimension $n$, then the Choi rank of an extreme UCPT map must be at most $\sqrt{2}n$. If we pick extreme UCPT maps over spaces of dimensions $n$ and $m$, one of them with rank greater than $\sqrt[4]{2}n$ and the other with rank greater than $\sqrt[4]{2}m$, then their tensor product have a rank greater than $\sqrt{2}nm$, so it can't be extreme.
 
## References

* {#Choi75} [[Man-Duen Choi]], Thm. 2.11 in: *Completely positive linear maps on complex matrices*, Linear Algebra and its Applications **10** 3 (1975) 285-290 &lbrack;<a href="https://doi.org/10.1016/0024-3795(75)90075-0">doi:10.1016/0024-3795(75)90075-0</a>

* [[L. J. Landau]], [[Raymond F. Streater]],  *On Birkhoff's theorem for doubly stochastic completely positive maps of matrix algebras*, Linear Algebra and its Applications **193** (1993) 107-127 &lbrack;<a href="https://doi.org/10.1016/0024-3795(93)90274-R">doi:10.1016/0024-3795(93)90274-R</a>&rbrack;

* [[Christian B. Mendl]], [[Michael M. Wolf]], *Unital Quantum Channels -- Convex Structure and Revivals of Birkhoff's Theorem*, Commun. Math. Phys. **289**  (2009) 1057-1096 &lbrack;[arXiv:0806.2820](http://arxiv.org/abs/0806.2820)&rbrack;

* {#MillerDaSilva23} James Miller, S. T. da Silva, *On the Extremality of the Tensor Product of Quantum Channels* &lbrack;[arXiv;2305.05795](https://arxiv.org/abs/2305.05795)&rbrack;

[[!redirects extremal quantum channels]]
