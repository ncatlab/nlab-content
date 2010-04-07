
<div class="rightHandSide toc">
[[!include quasi-category theory contents]]
</div>


#Contents#
* automatic table of contents goes here
{:toc}

## Idea

As a model for an [[(∞,1)-category]] a [[simplicially enriched category]] may be thought of as a [[semi-strict infinity-category|semi-strictification]] of a [[quasi-category]]: composition along 0-cells is strictly associative and unital.

The [[quasi-category]] corresponding to a simplicial category $C$ is its
[[homotopy coherent nerve]] $N$

$$
  sSet Cat \stackrel{\overset{|-|}{\leftarrow}}{\underset{N}{\to}} sSet
  \,.
$$

## Relations

* For $C$ any [[SSet]]-[[enriched category]], the canonical morphism

  $$ 
    |N(C)| \to C
  $$

  is an equivalence in that it is essentially surjective on the underlying homotopyy categories and a weak eqivalence of simplicial sets hom-wise (...details/links...)

  For $S$ any [[simplicial set]], the canonical morphism

  $$
    S \to N(|S|)
  $$

  is a [[model structure for quasi-categories|categorical equivalence]] of simplicial sets.

## Model category structures

The above relations constitute arrange into a [[Quillen equivalence]] between [[model category]] structures on quasicategories and simplicially enriched categories.

There is the 

* [[model structure for quasi-categories]]

* [[model structure on sSet-categories]].

The [[homotopy coherent nerve]] 

$$
  sSet Cat \stackrel{N}{\to} sSet_{Joyal}
$$

is the [[right adjoint]] part of a [[Quillen equivalence]] between these model structures.

## References

The [[homotopy coherent nerve]] is an old idea. See there for references.

The [[Quillen equivalence]] between the [[model structure for quasi-categories]] and the [[model structure on sSet-categories]] is described in

* [[Julie Bergner]], _A survey of $(\infty,1)$-categories_ ([arXiv](http://arxiv.org/abs/math/0610239))

A detailed discussion of the map from quasi-categories to $SSet$-categories is in 

* [[Dan Dugger]], [[David Spivak]], _Rigidification of quasi-categories_ ([arXiv:0910.0814](http://arxiv.org/abs/0910.0814))

* [[Dan Dugger]], [[David Spivak]], _Mapping spaces in quasi-categories_ ([arXiv:0911.0469](http://arxiv.org/abs/0911.0469))

An introduction and overview of the relation between quasi-categories and simplicial categories is in section 1.1.5 of 

* [[Jacob Lurie]], _[[Higher Topos Theory]]_ .

The details are in section 2.2
