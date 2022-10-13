

In [[algebraic topology]], the **slant product in homology** is the following pairing between [[singular homology]] and [[singular cohomology]]:
$$
H_q(X,A)\otimes H^n(X\times Y,A')\to H^{n-q}(Y,A\otimes A').
$$

It is induced at the chains/cochains level by the [[cochain on a simplicial set|Eilenberg-Zilber chain map]] 
$$
  Chains(X)\otimes Chains(Y)\to Chains(X\times Y).
$$

When the [[abelian group]] $A$ has a commutative ring structure, one can take $A'=A$ and postcompose with $A\otimes A\to A$ to obtain the pairing
$$
H_q(X,A)\otimes H^n(X\times Y,A)\to H^{n-q}(Y,A).
$$

In particular, for $Y=*$ one obtains the contraction
$$
H_q(X,A)\otimes H^n(X,A)\to H^{n-q}(*,A)
$$
taking values in the coefficient ring of the given cohomology theory.

Likewise, the **slant product in cohomology**
is a map of the form
$$H^i(Y,A)\otimes H_n(X\times Y,A')\to H_{n-i}(X,A\otimes A').$$
It is induced by the [[Alexander-Whitney map]].

There are also versions for [[relative homology]] and [[relative cohomology]].
See [Dold](#Dold), VII.11 and VII.13.

* {#Dold} Albrecht Dold, _Lectures on Algebraic Topology_, Springer, 1980.