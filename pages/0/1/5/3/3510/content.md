
<div class="rightHandSide toc">
[[!include model category theory - contents]]
</div>


#Contents#
* automatic table of contents goes here
{:toc}


## Idea

The notion of [[complete Segal space]] is a model for the notion of [[(∞,1)-category]]. The [[model category]] structure on the collection of all [[bisimplicial set]]s is a model for the [[(∞,1)-category]] of all Segal spaces, hence for the [[(∞,1)-category of (∞,1)-categories]].

## Definition

+-- {: .un_prop}
###### Proposition
**(Rezk model structure)**

The category $[\Delta^{op}\times \Delta^{op}, Set]$ of [[bisimplicial set]]s is equipped with the structure of a 

* [[left proper model category|left proper]]

* [[cartesian closed category|cartesian]] [[monoidal model category|closed]]

* [[simplicial model category]] 

by setting

* cofibrations are the [[monomorphism]]s

* weak equivalences are the **Segal weak equivalences.

The fibrant objects in the structure are precisely the [[complete Segal space]]s.

=--

## Relation to quasi-categories {#RelQCat}


There are the following two [[Quillen equivalence]]s between the model structure for complete Segal spaces and the [[model structure for quasi-categories]].

One is 

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

where $t_!$ assigns the total simplicial set to a bisimplicial set, and where $t^!$ forms in each degree the mapping space

$$
  t^! : X_\bullet \mapsto ([m,n] \mapsto 
    Hom_{sSet}( \Delta[m] \times Ex^{\infty} \Delta[n], X)
  )
  \,,
$$

where $Ex^\infty$ is the [[Kan fibrant replacement]] functor.


## References

Complete Segal spaces were originally defined in 

* [[Charles Rezk]], _A model for the homotopy theory of homotopy theory_ , Trans. Amer. Math. Soc., 353(3), 973-1007

The [[Quillen equivalence]] with the [[model structure for quasi-categories]] is discussed in 

* [[Andre Joyal]], [[Myles Tierney]], _Quasi-categories vs Segal spaces_ ([arXiv:0607820](http://arxiv.org/abs/math/0607820))

A survey of the model structures and their relations is in 

* [[Julia Bergner]], _A survey of $(\infty, 1)$-categories_ ([arXiv](http://arxiv.org/abs/math.AT/0610239)).
