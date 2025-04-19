

> This page is for developing preliminary notes or making typographical experiments, etc. It may be edited by anybody, anytime. But you don't necessarily need to delete other people's ongoing notes here in order to add your own. In any case, overwritten edits may always be recovered from the [page history](https://ncatlab.org/nlab/history/Sandbox).

\linebreak


***


Irreps of $C_k \wr Sym_3$.

Irreps of $C_k$ are all 1-dimensional and labeled by $p \in C_k$, with $[1] \in C_k$ acting on $\mathbf{1}_p$ as multiplication by $e^{2\pi \mathrm{i} \tfrac{p}{k}}$.

Case one: the partition is concentrated on a single irrep $\mathbf{1}_p$, 

$$
  n_i 
    \;=\; 
  \left\{
  \begin{array}{ccl}
    3 &\vert& i = p
    \\
    0 &\vert& \text{otherwise}
  \end{array}
  \right.
$$

Thus $Sym_{(3)} \simeq Sym_3$ and the irreps of this kind are of the form

$$
  \mathbf{1}_p^{\boxtimes_3} \otimes \sigma
$$

for $\sigma$ an irrep of $Sym_3$.


Case two: the partition is equally distributed on three distinct irreps.

Thus $Sym_{(3)} \simeq 1$ and the irreps of this kind are of the form

$$
  Ind
    _{ (C_k)^3 }
    ^{ C_k \wr Sym_3 }
  \big(
    \mathbf{1}_{p_1}
    \boxtimes
    \mathbf{1}_{p_2}
    \boxtimes
    \mathbf{1}_{p_3}
  \big)
  \;\;
  \simeq
  \;\;
  \mathbb{C}\big[ C_k \wr Sym_3\big]
  \otimes_{\mathbb{C}\big[ (C_k)^3 \big]}
  \big(
    \mathbf{1}_{p_1}
    \boxtimes
    \mathbf{1}_{p_2}
    \boxtimes
    \mathbf{1}_{p_3} 
  \big)
$$

Case 3: The partition is on irrep $\mathbf{1}_p$ with weight one and on another one $\mathbf{1}_{p'}$ with weight 2.

Here $Sym_{(3)} \simeq \Sym_2$

and the irreps are of the form

$$
  \mathbb{C}\big[
    C_p \wr Sym_3
  \big]
  \otimes_{ \mathbb{C}\big[ C_p \times (C_{p'} \wr Sym_2) \big] }
  \big(
  \mathbf{1}_{p} 
    \boxtimes 
  \mathbf{1}_{p'} 
    \boxtimes 
  \mathbf{1}_{p'}
  \big)
$$




(...)