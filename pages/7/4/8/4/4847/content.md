
> This entry is about the _signature_ of a [[permutation]]. For other notions of [[signature]] see there.

#Contents#
* table of contents
{:toc}
 
## Definition


For $Aut(\{1, \cdots , n\}) \simeq S_n$ the [[symmetric group]] on $n \in \mathbb{N}$ elements, the _signature_ is the unique [[group]] [[homomorphism]]

$$
  sign : S_n \to \mathbb{Z}_2 = \{1, -1\}
$$

that sends each transposition $s_{i, i+1} : \{1, \cdots, n\} \to \{1, \cdots, n\}$, which interchanges the $i$th element with its neighbour and leaves the other elements fixed, to the nontrivial element $(-1) \in \mathbb{Z}_2$. 

Permutations in the kernel of $sign$ are called _even_ permutations, and the rest are called _odd_ permutations. 

+-- {: .un_lem}
###### Lemma 
The signature is well-defined. 
=-- 

+-- {: .proof}
###### Proof 
One way of seeing this is invoking a standard [[group presentation]] of $S_n$ where generators $\sigma_i$ for $i = 1$ to $n-1$ (representing $s_{i, i+1}$) are subject to relations 

$$\sigma_{i}^2 = 1, \qquad (\sigma_i \sigma_{i+1})^3 = 1, \qquad \sigma_i \sigma_j = \sigma_j \sigma_i \; ({|i-j|} \gt 1),$$ 

and checking that the sign applied to both sides of a relation equation gives the same result. 

Another is by invoking a tautological representation of $S_n$ on a [[polynomial algebra]] $\mathbb{Z}[x_1, \ldots, x_n]$, 

$$S_n \stackrel{\cong}{\to} Set_{core}(\{x_1, \ldots, x_n\}, \{x_1, \ldots, x_n\}) \to CRing_{core}(\mathbb{Z}[x_1, \ldots, x_n], \mathbb{Z}[x_1, \ldots, x_n])$$ 

(where [[core]] refers to the groupoid of invertible morphisms) and recognizing that for the special polynomial 

$$D \coloneqq \prod_{i \lt j} (x_i - x_j)$$ 

we have, for each permutation $\tau$, either $\tau \cdot D = D$ or $\tau \cdot D = -D$. (The polynomial $\Delta \coloneqq D^2$, which is invariant under the action, is called the [[discriminant]].) 
=-- 

## Computations 

There are various means for computing the signature (also called **sign**) of a permutation. 

The definition itself suggests one method: if we linearly [[total order|order]] the set $\{x_1, \ldots, x_n\}$ by $x_1 \lt \ldots \lt x_n$, then we can exhibit a permutation $\tau$ by a [[string diagram]] and simply count the number of crossings $I(\tau)$; then we have 

$$sign(\tau) = (-1)^{I(\tau)}.$$ 

Each crossing corresponds to a pair of elements $x_i \lt x_j$ such that $\tau(x_i) \gt \tau(x_j)$, called an **inversion**. 

Another method which does not depend on choosing a total order is to exhibit a permutation through its [cycle decomposition](http://ncatlab.org/nlab/show/permutation#via_cycle_decompositions_6). Each cycle of period $k$ contributes a sign $(-1)^{k-1}$, and the overall sign is the product of these contributions taken over all the cycles. Thus the signature is given by the parity of the number of cycles of even length. 

This cycle description can actually be used to give an independent definition of the signature. It is manifestly well-defined and invariant on conjugacy classes. To check that it defines a homomorphism to $\{1, -1\}$, it suffices to check that multiplication by a transposition changes the parity of the number of even-length cycles by one. This is easy if we note that transposing two elements belonging to different cycles merges two cycles into one, whereas transposing two elements belonging to the same cycle splits one cycle into two. 


## Related concepts

* [[Levi-Civita symbol]]

[[!redirects signatures of permutations]]
[[!redirects sign of a permutation]]
[[!redirects sign of the permutation]]


