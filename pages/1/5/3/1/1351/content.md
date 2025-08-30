
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Higher category theory
+-- {: .hide}
[[!include higher category theory - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

Complicial sets are precisely those [[stratified simplicial sets]] which arise as the [[oriental|omega nerve]] of a [[strict omega-category]].



## Definition

A $k$-**admissible** [[n-simplex|$n$-simplex]] in a [[stratified simplicial set]] $X$ is a [[stratified simplicial set|map of stratified simplicial sets]] $\Delta^a_k[n] \to X$. Explicitly, this consists of a (thin) $n$-simplex $x \in X$ such that $x\cdot\alpha$ is thin for every $\alpha \colon [m] \to [n]$ whose image contains $k-1$, $k$, and $k+1$.

A **complicial set** is a [[stratified simplicial set]] satisfying the following three axioms:

1. if $x \in X$ is a $k$-admissible simplex whose $k-1$th and $k+1$th faces are thin, then its $k$th face is also thin;

2. there is a unique thin filler for all $(n-1)$-dimensional inner $k$-horns whose faces $x_0,\ldots, x_{k-2}$ are $(k-1)$-admissible and whose faces $x_{k+2},\ldots, x_n$ are $k$-admissible (nb: there is no condition on $x_{k-1}, x_{k+1} \in X_{n-1}$);

3. all thin 1-simplices are degenerate.

Equivalently, a **complicial set** is a stratified simplicial set that is (right) orthogonal to each of the following classes of stratified maps:

1. the **primitive** $t$-**extensions** $\Delta^a_k[n]' \to \Delta^a_k[n]''$, where $\Delta^a_k[n]'$ has all $n-1$-simplices except $\delta^k \colon [n-1] \to [n]$ thin, $\Delta^a_k[n]''$ has all $n-1$-simplices thin, and both stratified sets have any simplex $\alpha \colon [m] \to [n]$ with $k-1,k,k+1 \in$ im$(\alpha)$ thin;

2. the inclusions $\Lambda^a_k[n] \to \Delta^a_k[n]$ for all $n \geq 2$, $0 \lt k \lt n$;

3. the unique surjection $\Delta[1]_t \to \Delta[0]$, where every 1-simplex in $\Delta[1]_t$ is thin.

## Generalizations

* Weakening the conditions on a [[stratified simplicial set]] to be a complicial set yields notions of [[simplicial weak omega-category]].

* [[n-complicial set]]

## References

The original text:

* [[Dominic Verity]], *Complicial Sets Characterising the Simplicial Nerves of Strict $\omega$-Categories*, Memoirs of the AMS, **193** 905 (2008) &lbrack;[arXiv:math/0410412](http://arxiv.org/abs/math/0410412), [ams:memo-193-905](https://bookstore.ams.org/memo-193-905/)&rbrack;

Introduction:

* [[Emily Riehl]]: _Complicial sets, an overture_, in *2016 MATRIX Annals*, MATRIX Book Series **1** Springer (2018) &lbrack;[doi:10.1007/978-3-319-72299-3_4](https://doi.org/10.1007/978-3-319-72299-3_4), [arXiv:1610.06801](https://arxiv.org/abs/1610.06801)&rbrack;

[[!redirects complicial sets]]