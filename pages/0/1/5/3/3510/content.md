
<div class="rightHandSide toc">
[[!include model category theory - contents]]
</div>


#Contents#
* automatic table of contents goes here
{:toc}


## Idea

The notion of [[complete Segal space]] is a model for the notion of [[(∞,1)-category]]. The [[model category]] structure on the collection of all [[bisimplicial set]]s is a model for the [[(∞,1)-category]] of all Segal spaces, hence for the [[(∞,1)-category of (∞,1)-categories]].

## Definition

The following [[model category]] structure models the [[(∞,1)-category]] of [[complete Segal space]]s.

+-- {: .un_prop}
###### Proposition
**(Rezk model structure for complete Segal spaces)**

The category $[\Delta^{op}\times \Delta^{op}, Set]$ of [[bisimplicial set]]s carries the structure of an [[sSet]]-[[enriched category]] with [[hom-object]] for two bisimplicial sets $X$ and $Y$ given by

$$
  hom(X,Y) := i_2^*(Y^X)
  \,,
$$

where

* $Y^X$ is the [[internal hom]] in the standard [[closed monoidal structure on presheaves]];

* $i_2 : \Delta \to \Delta \times \Delta$ is the [[right adjoint]] to the projection $\Delta \times \Delta \to \Delta$ on the second factor, given by $i_2 : [n] \mapsto ([0],[n])$.

This refines to the structure of a

* [[left proper model category|left proper]]

* [[cartesian closed category|cartesian]] [[monoidal model category|closed]]

* [[simplicial model category]] 

by setting

* cofibrations are the [[monomorphism]]s

* weak equivalences are the **Rezk weak equivalences**:. those morphisms $u : A \to B$ such that for all [[complete Segal space]]s $X$ the morphism $hom(u,X) \to hom(B,X) \to hom(A,X)$ is a weak equivalence in the standard [[model structure on simplicial sets]].

The fibrant objects in the structure are precisely the [[complete Segal space]]s.

=--

+-- {: .proof}
###### Proof

This appears as [JT, theorem 4.1](http://arxiv.org/PS_cache/math/pdf/0607/0607820v2.pdf#page=21). 

=--

For handling this it can be useful to realize it as a [[Bousfield localization of model categories|left Bousfield localization]] of the following model structure

+-- {: .un_prop}
###### Proposition
**(vertical model structure on bisimplicial sets)**

The category $[\Delta^{op}\times \Delta^{op}, Set]$ of [[bisimplicial set]]carries the structure of a 

* [[proper model category|proper]]

* [[cartesian closed category|cartesian]] [[monoidal model category|closed]]

* [[simplicial model category]] 

by setting

* cofibrations are the [[monomorphism]]s

* weak equivalences $X_{\bullet,\bullet} \to Y_{\bullet,\bullet}$
  are the column-wise weak equivalences 
  $X_{n,\bullet} \to Y_{n,\bullet}$ in the standard 
  [[model structure on simplicial sets]].

=--

+-- {: .proof}
###### Proof

This is due to Reedy.
It appears as [JT, theorem 2.6](http://arxiv.org/PS_cache/math/pdf/0607/0607820v2.pdf#page=11). 

=--



## Relation to quasi-categories {#RelQCat}

We have the following pair of [[adjunction]]s between [[simplicial set]]s and [[bisimplicial set]]s.

The first is

$$
  (p_1^* \dashv i_1^*)
  :
  [\Delta^{op}, Set]
  \stackrel{\overset{i_1^*}{\leftarrow}}{\overset{p_1^*}{\to}}
  [\Delta^{op} \times \Delta^{op}, Set]
$$

where $i_1^*$ sends a bisimplicial set to the simplicial set of its first row

$$
  i_1^* : X_{\bullet,\bullet} \mapsto X_{\bullet, 0}
  \,.
$$

The other is

$$
  (t_! \dashv t^!)
  :
  [\Delta^{op} \times \Delta^{op}, Set]
  \stackrel{\overset{t^!}{\leftarrow}}{\overset{t_!}{\to}}
  [\Delta^{op}, Set]
$$

where 

* $t_!$ assigns the total simplicial set to a bisimplicial set: it is the left [[Kan extension]] of the functor $t : \Delta \times \Delta \to BiSSet$ given by $([k],[l]) \mapsto \Delta[k]\times Ex^{\infty}(\Delta[l])$ along the [[Yoneda embedding]]

  $$
    t_!(X_{\bullet,\bullet})
    =
    \int^{[k],[l]}
      X_{k,l} \cdot \Delta[k] \times Ex^\infty(\Delta[l])
      \,;
  $$

* and where $t^!$ forms in each degree the mapping space

  $$
    t^! : X_\bullet \mapsto ([m,n] \mapsto 
      Hom_{sSet}( \Delta[m] \times Ex^{\infty} \Delta[n], X)
    )
    \,,
  $$

where $Ex^\infty$ is the [[Kan fibrant replacement]] functor.

+-- {: .un_prop}
###### Proposition

The composite adjunction

$$
  sSet
    \stackrel{\overset{i_1^* t^!}{\leftarrow}}{\overset{t_! p_1^*}{\to}}
  sSet
$$

is the identity adjunction: both functors are [[isomorphic]] to the identity functor.

=--

+-- {: .proof}
###### Proof

This appears at the end of the proof of [JT, theorem 4.12](http://arxiv.org/PS_cache/math/pdf/0607/0607820v2.pdf#page=26). 

=--


+-- {: .un_prop}
###### Proposition

Both these adjunctions are [[Quillen equivalence]]s between the [[model structure for quasi-categories]] on simplicial sets and the Rezk model structure for complete Segal spaces on bisimplicial sets.

=--

+-- {: .proof}
###### Proof

This appears [JT, theorem 4.11, 4.12](http://arxiv.org/PS_cache/math/pdf/0607/0607820v2.pdf#page=25). 

=--



## References

Complete Segal spaces were originally defined in 

* [[Charles Rezk]], _A model for the homotopy theory of homotopy theory_ , Trans. Amer. Math. Soc., 353(3), 973-1007

The [[Quillen equivalence]] with the [[model structure for quasi-categories]] is discussed in 

* [[Andre Joyal]], [[Myles Tierney]], _Quasi-categories vs Segal spaces_ ([arXiv:0607820](http://arxiv.org/abs/math/0607820))

A survey of the model structures and their relations is in 

* [[Julia Bergner]], _A survey of $(\infty, 1)$-categories_ ([arXiv](http://arxiv.org/abs/math.AT/0610239)).
