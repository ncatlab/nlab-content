

+-- {: .un_defn}
###### Definition
**(Symmetric Product)**

There is a natural forgetful functor from topological commutative monoids to [[pointed space|pointed topological spaces]], where the basepoint of a commutative monoid is taken to be its unit element. The induced monad is the _infinite symmetric product_ construction:

$$
  Sym(X,e) = \mathrm{colim}_N Sym^N(X) \qquad
  Sym^N(X) = (X \times \dots \times X)/\Sigma_N
$$

Here the colimit is taken over the maps $Sym^N(X) \to Sym^{N+1}(X)$, $(x_1,\dots, x_n) \mapsto (x_1,\dots, x_n, e)$ where $e$ is the basepoint.

Thus $Sym(X,e)$ is the free topological commutative monoid on $X$ with the basepoint $e$ acting as the unit.

###### Theorem
**(Dold-Thom)**

The [[ordinary homology]],  hence the standard $n$-th [[homology group]] of a [[pointed connected CW-complex]] $(X,e)$ is [[isomorphism|isomorphic]] to the $n$-th [[homotopy group]] of the infinite symmetric product of $(X,e)$

$$
  H_i(X) = \pi_i (\mathrm{colim}_N\, \mathrm{Sym}^N X)
  \,.
$$

=--


The [[Mayer-Vietoris sequence]] for homology is a consequence of applying $\pi_*(-)$ to the [[homotopy pullback]] square resulting from the application of $\mathrm{Sym}^\infty$ to the [[homotopy pushout]] square formed by the inclusions of the intersection, $A \cap B$, of two subspaces $A$ and $B$ of a space $X$ into $A$ and $B$.

## References

The original article is

* [[Albrecht Dold|A. Dold]], [[René Thom|R. Thom]], _Quasifaserungen und unendliche symmetrische Produkte_ , Ann. Math. (2) 69 (1959), 239--281. ([pdf](http://www.maths.ed.ac.uk/~aar/papers/doldthom.pdf))

For a textbook account, see [Hatcher](https://pi.math.cornell.edu/~hatcher/AT/AT.pdf#page=484), Sec. 4.K p. 475.
