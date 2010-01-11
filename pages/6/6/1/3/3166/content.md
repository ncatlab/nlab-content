<div class="rightHandSide toc">
[[!include cohomology - contents]]
</div>



## Idea

The _[[cohomology]] of a [[category]]_ $C$ is often defined to be the [[groupoid cohomology]] of the [[∞-groupoid]] that is presented by the [[nerve]] of the category.

Hence for $\mathbf{A}$ some coeffiecient [[∞-groupoid]]  -- typically, but not necessarily, an [[Eilenberg-MacLane object]] $\mathbf{A} = K(A,n) = \mathbf{B}^n A$ -- regarded as a [[Kan complex]], the cohomology of $C$ in this sense is

$$
  H^n(C,A) := \pi_0 \infty Grpd( F(N(C)), \mathbf{A} )
  \,,
$$

where 

* $N(C)$ is the [[nerve]] of $C$;

* $F(N(C))$ is the [[Kan fibrant replacement]] of $N(C)$;

* [[∞Grpd]] is the [[(∞,1)-category]] of [[∞-groupoid]]s.

Using the standard [[model structure on simplicial sets]] this is the same as the [[hom-set]] in the [[homotopy category]] of [[SSet]]

$$
  \cdots = Ho_{SSet}(N(C), \mathbf{A})
  \,.
$$

One can also use the [[Thomason model structure]] on [[Cat]] to say the same: due to the [[Quillen equivalence]] $Cat_{Thomason} \stackrel{Quillen}{\simeq} SSet_{Quillen}$ we have for $\alpha$ any category whose groupoidification is equivalent to $\mathbf{A}$, i.e. any cateory such that $F(N(\alpha)) \simeq \mathbf{A}$ in [[∞Grpd]], we have

$$
  \cdots = Ho_{Cat_{Thomason}}(C,\alpha)
  \,.
$$

