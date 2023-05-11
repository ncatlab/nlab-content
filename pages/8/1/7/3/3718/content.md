<div class="rightHandSide toc">
[[!include physicscontents]]
</div>

#Contents#
* automatic table of contents goes here
{:toc}

# Extremal quantum channels

The set of all quantum channels on $\mathcal{M}_{d}$ is convex and compact meaning it may be decomposed as

$$
T=\sum_{i}p_{i}T_{i}
$$

where the $p$'s are probabilities and the $T_{i}$'s are $extremal$ unital channels, that is channels that may not be further decomposed.

Channels with a single Kraus operator are pure channels and the extremal points in the convex set of channels are precisely the pure channels.  Here $T$ represents the set of $all$ channels on the particular space, not necessarily copies of the same one, i.e. the $T_{i}$ may not represent the same channel.  

## General extremality

$T$, with Kraus operators $\{A\}_i$, is extremal if and only if the set 

$$
\left \{A_{k}^{\dagger}A_{l} \right \}_{k,l\ldots N}
$$

is linearly independent.

## Unital extremality

In the case where $T$ is unital, it is extremal if and only if the set

$$
\left \{A_{k}^{\dagger}A_{l} \oplus A_{l}A_{k}^{\dagger} \right \}_{k,l \ldots N}
$$

is linearly independent.

# Discussion

[[Ian Durham]]: One major conundrum is to determine whether extremality is preserved over tensor products, i.e. given an extremal quantum channel, if you take $n$ copies of it (which amounts to tensoring it $n$ times with itself), as a whole are these $n$ copies still extremal?  It would be nice to see if category theory can shed some light on this problem since it is at the root of a particularly gnarly problem in [[quantum information]] theory..

# Tensor product of extreme channels

In the case of CPT or UCP maps the tensor product preserves extremality, but this is not always the case for UCPT maps.

A sketch of the proof for CPT maps is as follows. A finite sequence of vectors is linearly independent iff its Gram matrix is invertible. If $(A_k)_k$ and $(B_l)_l$ are Kraus operators for two CPT maps, then $(A_k \otimes B_l)_{k,l}$ are Kraus operators for the tensor product. Also, if both $(A_k)_k$ and $(B_l)_l$ are linearly independent, then $(A_k \otimes B_l)_{k,l}$ is also linearly independent. If we assume that $(A_k)_k$ and $(B_l)_l$ represent extreme CPT maps, then $(A_k^\dagger A_{k'})_{k,k'}$ and $(B_l^\dagger B_{l'})_{l,l'}$ are linearly independent. Let $G$ be the Gram matrix of $(A_k^\dagger A_{k'})_{k,k'}$ and $G'$ be the Gram matrix of $(B_l^\dagger B_{l'})_{l,l'}$, then $G$ and $G'$ are invertible. Let also $G''$ be the Gram matrix of $((A_k \otimes B_l)^\dagger (A_{k'} \otimes B_{l'}))_{(k,l),(k',l')}$. Extremality is preserved if $((A_k \otimes B_l)^\dagger (A_{k'} \otimes B_{l'}))_{(k,l),(k',l')}$ is linearly independent, which is equivalent to $G''$ being invertible. It follows that $G'' = G \otimes G'$ (Kronecker product). Using the properties of the Kronecker product and the invertibility of both $G$ and $G'$ we conclude that $G''$ is invertible.

A proof for the case of UCP maps may be obtained by the duality between CPT and UCP maps.

In the case of UCPT maps extremality is not always preserved. It is still preserved if one of the channels is over a space of dimension 2, since for dimension 2 the extreme UCPT maps are unitary channels. For higher dimensions one can construct counterexamples. A reason for this to happen is that if the UCPT maps are over a space of dimension $n$, then the Choi rank of an extreme UCPT map must be at most $\sqrt{2}n$. If we pick extreme UCPT maps over spaces of dimensions $n$ and $m$, one of them with rank greater than $\sqrt[4]{2}n$ and the other with rank greater than $\sqrt[4]{2}m$, then their tensor product have a rank greater than $\sqrt{2}nm$, so it can't be extreme.
 
# References

Christian B. Mendl and Michael M. Wolf, _Unital Quantum Channels - Convex Structure and Revivals of Birkhoff's Theorem_ ([pdf](http://arxiv.org/abs/0806.2820)).

L. J. Landau and R. F. Streater, _On Birkhoff 's theorem for doubly stochastic completely positive maps of matrix algebras_, Lin. Alg. Appl., 193:107&#8211;127, 1993. 

J. M. S. T. da Silva, On the Extremality of the Tensor Product of Quantum Channels ([pdf](https://arxiv.org/abs/2305.05795)).

[[!redirects extremal quantum channels]]