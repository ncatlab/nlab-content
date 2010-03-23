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

# References

Christian B. Mendl and Michael M. Wolf, _Unital Quantum Channels - Convex Structure and Revivals of Birkhoff's Theorem_ ([pdf](http://arxiv.org/abs/0806.2820)).

L. J. Landau and R. F. Streater, _On Birkhoff 's theorem for doubly stochastic completely positive maps of matrix algebras_, Lin. Alg. Appl., 193:107&#8211;127, 1993. 
