

+-- {: .un_defn}
###### Theorem
**(Dold-Thom)**

The standard $n$-th [[homology group]] of a [[CW-complex]] $X$ is [[issomorphism|isomorphic]] to the $n$-th [[homotopy group]] of the [[free construction|free]] topological commutative [[monoid]] on $X$, which is an infinite [[symmetric product]] that is the [[colimit]] $\mathrm{Sym}^\infty X$ (denoted also $SP^\infty$) of the symmetric powers $\mathrm{Sym}^N X = X*X*...*X = (X\times X\times ...\times X)/\Sigma_N$ of $X$:

$$
  H_i(X) = \pi_i (\mathrm{colim}_N\, \mathrm{Sym}^N X)
  \,.
$$

=--


The [[Meyer-Vietoris sequence]] for homology is a consequence of applying $\pi_*(-)$ to the [[homotopy pullback]] square resulting from the application of $\mathrm{Sym}^\infty$ to the [[homotopy pushout]] square formed by the inclusions of the intersection, $A \cap B$, of two subspaces $A$ and $B$ of a space $X$ into $A$ and $B$.

## References

The original article is

* A. Dold, R. Thom, _Quasifaserungen und unendliche symmetrische Produkte_ , Ann. Math. (2) 69 (1959), 239--281.

