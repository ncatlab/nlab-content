


+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### $(\infty,1)$-Category theory
+--{: .hide}
[[!include quasi-category theory contents]]
=--
=--
=--


#Contents#
* automatic table of contents goes here
{:toc}

## Idea

As a model for an [[(∞,1)-category]] a [[simplicially enriched category]] may be thought of as a [[semi-strict infinity-category|semi-strictification]] of a [[quasi-category]]: composition along 0-cells is strictly associative and unital.

The [[quasi-category]] corresponding to a simplicial category $C$ is its
[[derived functor|derived]] [[homotopy coherent nerve]] $N$

$$
  sSet Cat \stackrel{\overset{|-|}{\leftarrow}}{\underset{N}{\to}} sSet
  \,.
$$

## Relations

### Via homotopy coherent nerve

For $C$ an (fibrant, probably) [[SSet]]-[[enriched category]], the canonical morphism

  $$ 
    |N(C)| \to C
  $$

  (or possibly rather the [[derived adjunction counit]])

  is an equivalence in that it is essentially surjective on the underlying homotopy categories and a weak equivalence of simplicial sets hom-wise (...details/links...)

  For $S$ any [[simplicial set]], the canonical morphism

  $$
    S \to N(|S|)
  $$

  is a [[model structure for quasi-categories|categorical equivalence]] of simplicial sets.

### Via $\bar W$-construction

We have an evident inclusion 

$$
  sSet Cat \hookrightarrow Cat^{\Delta}
$$

of [[simplicially enriched categories]]
into [[simplicial objects in Cat]].

On the latter the $\bar W$-functor is defined as the composite

$$
  \bar W 
   \colon
  Cat^\Delta
   \stackrel{N^\Delta}{\to}
  sSet^\Delta
   \stackrel{}{\to}
  sSet
$$

where first we degreewise form the ordinary [[nerve]] of categories and then take the total simplicial set of [[bisimplicial sets]] (the [[right adjoint]] of pullback along the [[diagonal]] $\Delta^n \to \Delta^n \times \Delta^n$).

+-- {: .num_prop}
###### Proposition

For $C$ a [[simplicial groupoid]] there is a [[weak homotopy equivalence]]

$$
  \mathcal{N}(C) \to \bar W(C)
$$

from the [[homotopy coherent nerve]]

=--

([Hinich](#Hinich))


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

## Related concepts

* [[simplicial category]]

  * [[simplicially enriched category]]

  * [[simplicial object in Cat]]

* [[simplicial groupoid]]

There is an [[operad|operadic]] analog of the relation between quasi-categories and simplicial categories, involving, correspondingly [[dendroidal sets]] and [[simplicial operads]].

## References

The idea of a [[homotopy coherent nerve]] has been around for some time.  It was first  made explicit by [[Cordier]] in 1980, and the link with quasi-categories was then used in the joint work of him with [[Tim Porter|Porter]]. That work owed a lot to earlier ideas of  [[Michael Boardman|Boardman]] and [[Rainer Vogt|Vogt]] about seven years earlier who had used a more topologically based approach.  Precise references are given and the history discussed more fully at the entry, [[homotopy coherent nerve]]. 

The [[Quillen equivalence]] between the [[model structure for quasi-categories]] and the [[model structure on sSet-categories]] is described in

* [[Julie Bergner]], _A survey of $(\infty,1)$-categories_ ([arXiv](http://arxiv.org/abs/math/0610239))

A detailed discussion of the map from quasi-categories to $SSet$-categories is in 

* [[Dan Dugger]], [[David Spivak]], _Rigidification of quasi-categories_ ([arXiv:0910.0814](http://arxiv.org/abs/0910.0814))

* [[Dan Dugger]], [[David Spivak]], _Mapping spaces in quasi-categories_ ([arXiv:0911.0469](http://arxiv.org/abs/0911.0469))

More along these lines is in 

* [[Emily Riehl]], _On the structure of simplicial categories associated to quasi-categories_ ([pdf](http://www.math.harvard.edu/~eriehl/necklace.pdf))

See also

* [[Vladimir Hinich]], _Simplicial nerve in Deformation theory_ ([arXiv:0704.2503](http://arxiv.org/abs/0704.2503))
 {#Hinich}

An introduction and overview of the relation between quasi-categories and simplicial categories is in section 1.1.5 of 

* [[Jacob Lurie]], _[[Higher Topos Theory]]_ .

The details are in section 2.2
