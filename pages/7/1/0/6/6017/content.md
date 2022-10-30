
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### $\infty$-Chern-Simons theory
+--{: .hide}
[[!include infinity-Chern-Simons theory - contents]]
=--
#### Quantum field theory
+--{: .hide}
[[!include functorial quantum field theory - contents]]
=--
#### Physics
+--{: .hide}
[[!include physicscontents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

A _Yetter model_ is a [[4d TQFT]] [[sigma-model]] [[quantum field theory]] whose target space is a [[discrete infinity-groupoid|discrete]] [[2-groupoid]] and whose [[background gauge field]] is a [[circle n-bundle|circle 4-bundle]].

Together with the [[Dijkgraaf-Witten theory|Dijkgraaf-Witten model]] these form the first two steps in filtering of target spaces by [[homotopy type]] [[truncated|truncation]] of [[schreiber:∞-Chern-Simons theory]] <a href="http://nlab.mathforge.org/schreiber/show/infinity-Chern-Simons+theory#DiscreteTargets">with discrete target spaces</a>. It is hence also an example of a [[4d Chern-Simons theory]].


## Definition

Fix

* $G$ a [[discrete infinity-groupoid|discrete]] [[2-group]]; write $\mathbf{B}G$ for its [[delooping]] [[2-groupoid]];

* $\alpha : \mathbf{B}G \to \mathbf{B}^4 U(1)$ a [[characteristic class]] with coefficients in the [[circle n-group|circle 4-group]]. This is equivalently a cocycle in degree $4$ [[group cohomology]]

  $$
    [\alpha] \in H_{Grpd}^4(G, U(1))
    \,.
  $$ 

The **Yetter-model** is the <a href="http://nlab.mathforge.org/schreiber/show/infinity-Chern-Simons+theory#DiscreteTargets">∞-Dijkgraaf-Witten theory</a> induced by this data.

## Related concepts

* [[schreiber:∞-Chern-Simons theory]]

* [[higher dimensional Chern-Simons theory]]

  * [[1d Chern-Simons theory]]

  * [[2d Chern-Simons theory]]

  * [[3d Chern-Simons theory]]

  * [[4d Chern-Simons theory]]

  * [[5d Chern-Simons theory]]

  * [[6d Chern-Simons theory]]

  * [[7d Chern-Simons theory]]

  * [[infinite-dimensional Chern-Simons theory]]

  * [[AKSZ sigma-model]]




## References

The model without a [[background gauge field]]/cocycle was considered in

* [[David Yetter]], _TQFTs from homotopy 2-types_ , Journal of Knot Theory and its Ramifications 2 (1993), 113-123. 

The effect of having a nontrivial [[group cohomology|group 4-cocycle]] was considered (but now only on a 1-group) in 

* D. Birmingham, M. Rakowski, _On Dijkgraaf-Witten Type Invariants_, Lett. Math. Phys. 37 (1996), 363.

* [[Marco Mackaay]], _Spherical 2-categories and 4-manifold invariants_, Adv. Math. 153 (2000), no. 2, 353&#8211;390. ([arXiv:math/9805030](http://arxiv.org/abs/math/9805030))
 {#Mackay} .


The reinterpretation of the "state sum" equation used in the above publications as giving [[homomorphisms]] of [[simplicial sets]]/[[topological spaces]] is given in

* [[Tim Porter]], _Interpretations of Yetter's notion of $G$-coloring : simplicial fibre bundles and non-abelian cohomology_,  Journal of Knot Theory and its Ramifications 5 (1996) 687-720, 

and then extended to colorings in [[homotopy n-types]] in 

* [[Tim Porter]], _Topological Quantum Field Theories from Homotopy n-types_, Journal of the London Math. Soc. (2) 58 (1998) 723-732.

See also

* [[João Faria Martins]] and  [[Tim Porter]], _On Yetter's invariants and an extension of the Dijkgraaf-Witten invariant to categorical groups_, Theory and Applications of Categories, Vol. 18, 2007, No. 4, pp 118-150.
([TAC](http://www.tac.mta.ca/tac/volumes/18/4/18-04abs.html))

which has some remarks about higher (2-)group cocycles towards the end.


[[!redirects Crane-Yetter model]]
