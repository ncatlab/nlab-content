# Idea

A **chord diagram** (of order $n$) is basically a [[circle]] marked with $2n$ distinct points and $n$ chords joining those points, considered up to rotation of the circle. An **arc diagram** is what you get when you cut the circle at any of the $2n$ segments between the marked points, breaking the rotational symmetry.  For example, here is a chord diagram of order 3:

<center>
[[!include chord diagram > chord diagram]]
</center>

And here is the arc diagram obtained by cutting the chord diagram at the segment between points 0 and 5:

<center>
[[!include chord diagram > arc diagram]]
</center>

An arc diagram of order $n$ is entirely determined by specifying a [[fixed point]] free [[involution]] $\alpha$ on the [[ordinal]] $\mathbf{2n} = \{0 \to 1 \to \dots \to 2n{-}1\}$.  (In the above example, $\alpha = (02)(13)(45)$.)  The [[cyclic group]] $\mathbb{Z}_{2n}$ acts naturally on arc diagrams of order $n$ by [[conjugation action|conjugation]], which to any $0 \le k \lt 2n$ associates the transformation $\alpha \mapsto \tau_k\circ\alpha\circ\tau_k^{-1}$, where $\tau_k$ is addition modulo $2n$.  Conversely, taking the [[quotient]] by this [[action]] recovers the set of chord diagrams of order $n$.

## Related concepts

* [[Vassiliev invariant]]
* [[combinatorial map]]

## References

For more on chord diagrams emphasizing their connection to [[Vassiliev invariants]] of [[singular knots]], see Chapter 6 of

* [[Sergei K. Lando]] and [[Alexander K. Zvonkin]], _Graphs on Surfaces and Their Applications_, Springer, 2004.

as well as

* [[Dror Bar-Natan]], On the Vassiliev knot invariants, _Topology_ 34 (1995), 423-472. ([html](http://www.math.toronto.edu/~drorbn/papers/OnVassiliev/))

* [[Simon Willerton]], Vassiliev invariants and the [[Hopf algebra]] of chord diagrams, Math. Proc. Camb. Phil. Soc. (1996), 119, 55.

For chord diagrams and arc diagrams from the perspective of [[combinatorics]], see

* Jacques Touchard. Sur un probl&#232;me de configurations et sur les fractions continues. Canadian Journal of Mathematics 4 (1952), 2-25. ([doi](http://dx.doi.org/10.4153/CJM-1952-001-8))

* Philippe Flajolet and Marc Noy. Analytic combinatorics of chord diagrams. INRIA technical report 3914, March 2000. ([pdf](http://algo.inria.fr/flajolet/Publications/FlNo00.pdf))

* A. Khruzin. Enumeration of chord diagrams. arXiv:math/0008209, August 2000. ([arxiv](http://arxiv.org/abs/math/0008209))

[[!redirects arch diagram]]
[[!redirects arc diagram]]