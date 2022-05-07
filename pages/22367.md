## Definition

Given a finitely generated [[abelian group]] $A$ and $n\ge 3$,
the $n$th __Peterson space__ $P^n(A)$ of $A$
is the [[simply connected space]]
whose [[reduced cohomology groups]] vanish in dimension $k\ne n$
and the $n$th cohomology group is isomorphic to $A$.

## Existence and uniqueness

The Peterson space exists and is unique up to a [[weak homotopy equivalence]]
given the indicated conditions on $A$ and $n$.

There are counterexamples both to existence and uniqueness without these conditions.

For example, the Peterson space does not exist if $A$ is the abelian group of [[rationals]].

## Functoriality

If $n\ge 4$,
then $P_n$ is a functor from [[abelian groups]] without 2-[[torsion]]
to the [[homotopy category]] of [[pointed spaces]].

In fact, for all $n\ge 4$ the map
$$Hom(P^n(B),P^n(A))\to Hom(A,B)$$
is an isomorphism if $A$ has no 2-[[torsion]].


## Corepresentation of homotopy groups with coefficients

For all $n\ge2$, we have a canonical isomorphism
$$\pi_n(X,A)\cong [P^n(A),X],$$
where the left side denotes [[homotopy groups with coefficients]]
and the right side denotes morphisms in the pointed [[homotopy category]].

## Relation to Moore spaces

[[Moore spaces]] $M_n(A)$ are defined similarly to Peterson spaces,
using [[homology]] instead of [[cohomology]].

We have natural weak equivalences
$$P^n(A) \simeq M_n(Hom(A,\mathbf{Z}))$$
if $A$ is a finitely generated [[free abelian group]]
and
$$P^n(A) \simeq M_{n-1}(Hom(A,\mathbf{Q}/\mathbf{Z}))$$
if $A$ is a finite [[abelian group]].

## Examples

If $A=\mathbf{Z}$, then $P^n(A)=S^n$, so $\pi_n(X,\mathbf{Z})=\pi_n(X)$.

If $A=\mathbf{Z}/k\mathbf{Z}$,
then $P^n(A)$ is obtained by attaching an $n$-cell to an $(n-1)$-sphere
along a map of degree $k$.
Thus, $\pi_n(X,\mathbf{Z}/k\mathbf{Z})$ is defined for all $n\ge 2$.

## Related concepts

* [[Moore space]]

* [[Eilenberg–MacLane space]]

* [[homotopy groups with coefficients]]

## References

* [[Franklin P. Peterson]], _Generalized Cohomotopy Groups_.  American Journal of Mathematics 78:2 (1956), 259–281.  [doi:10.2307/2372515](http://dx.doi.org/10.2307/2372515)

* [[Joseph A. Neisendorfer]], _Homotopy groups with coefficients_, 
Journal of Fixed Point Theory and Applications 8:2 (2010), 247–338.  [doi:10.1007/s11784-010-0020-1](http://dx.doi.org/10.1007/s11784-010-0020-1).