
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### $(\infty,1)$-Category theory
+--{: .hide}
[[!include quasi-category theory contents]]
=--
=--
=--

\tableofcontents

## Idea

As a model for an [[(∞,1)-category]] a [[simplicially enriched category]] may be thought of as a [[semi-strict infinity-category|semi-strictification]] of a [[quasi-category]]: composition along 0-cells is strictly associative and unital.

## The Quillen equivalence between the Joyal model structure and the Dwyer–Kan–Bergner model structure

Our notation partly follows [Bergner (2018)](#Bergner18).

There is a [[Quillen equivalence]] (due to Joyal (unpublished) and [Lurie (2009), Thm. 2.2.5.1 & p. 91](#Lurie09)):

$$
 sSet\text{-}Cat
 \underoverset
   {\underset{\tilde N}{\longrightarrow}}
   {\overset{\mathfrak{C}}{\longleftarrow}}
   {\;\;\; \bot \;\;\;} 
 sSet.
$$

where:

* $SC$ denotes the category of [[sSet-enriched categories]]
equipped with the [[Dwyer–Kan–Bergner model structure]],

* $sSet$ denotes the [[Joyal model structure]] on [[simplicial sets]],

* $\tilde N$ denotes the [[homotopy coherent nerve]] functor,

* $\mathfrak{C}$ denotes its [[left adjoint functor]].

In particular, for $C$ a fibrant [[SSet]]-[[enriched category]], the canonical morphism

$$
  \mathfrak{C}\big(\tilde N(C)\big) 
  \longrightarrow 
  C
$$

given by the [[adjunction counit|counit]] of the above adjunction is derived, hence a [[Dwyer–Kan weak equivalence]] of [[simplicial categories]].

For $S$ any [[simplicial set]], the canonical morphism

$$
  S 
  \longrightarrow
  \tilde N\Big(
    R\big(
      \mathfrak{C}(S)
    \big)
  \Big)
$$

is a [[model structure for quasi-categories|categorical equivalence]] of simplicial sets,
where $R$ denotes a [[fibrant replacement]] functor in the [[Dwyer–Kan–Bergner model structure]].

For more details, see, for example, [Bergner (2018), §7.8](#Bergner)
or [Dugger & Spivak 2009a](#DuggerSpivak.Rigidification), or [Dugger & Spivak 2009b](#DuggerSpivak.Mapping).


## Relations

### Via $\bar W$-construction

We have an evident inclusion 
$$sSet Cat \hookrightarrow Cat^{\Delta}$$
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
$$\mathcal{N}(C) \to \bar W(C)$$
from the [[homotopy coherent nerve]]

=--

([Hinich](#Hinich))


## Related concepts

* [[straightening and unstraightening]]

* [[simplicial category]]

  * [[simplicially enriched category]]

  * [[simplicial object in Cat]]

* [[simplicial groupoid]]

There is an [[operad|operadic]] analog of the relation between quasi-categories and simplicial categories, involving, correspondingly, [[dendroidal sets]] and [[simplicial operads]].

## References

The idea of a [[homotopy coherent nerve]] has been around for some time.  It was first  made explicit by [[Cordier]] in 1980, and the link with quasi-categories was then used in his joint work  with [[Tim Porter|Porter]]. That work owed a lot to earlier ideas of  [[Michael Boardman|Boardman]] and [[Rainer Vogt|Vogt]] about seven years earlier who had used a more topologically based approach.  Precise references are given and the history discussed more fully at the entry, [[homotopy coherent nerve]]. 

The [[Quillen equivalence]] between the [[model structure for quasi-categories]] and the [[model structure on sSet-categories]] is described in

* [[Julie Bergner]], _A survey of $(\infty,1)$-categories_ ([arXiv](http://arxiv.org/abs/math/0610239))

A detailed discussion of the map from quasi-categories to $SSet$-categories is in 

* {#DuggerSpivak.Rigidification} [[Dan Dugger]], [[David Spivak]], _Rigidification of quasi-categories_ ([arXiv:0910.0814](http://arxiv.org/abs/0910.0814))


* {#DuggerSpivak.Mapping} [[Dan Dugger]], [[David Spivak]], _Mapping spaces in quasi-categories_ ([arXiv:0911.0469](http://arxiv.org/abs/0911.0469))


More along these lines is in 

* [[Emily Riehl]], _On the structure of simplicial categories associated to quasi-categories_ ([pdf](http://www.math.harvard.edu/~eriehl/necklace.pdf))

An expository account is in Section 7.8

* {#Bergner18} [[Julie Bergner]], _The homotopy theory of (∞,1)-categories_, London Mathematical Society Student Texts 90, 2018.


See also

* {#Hinich} [[Vladimir Hinich]], _Simplicial nerve in Deformation theory_ ([arXiv:0704.2503](http://arxiv.org/abs/0704.2503))
 

An introduction and overview of the relation between quasi-categories and simplicial categories is in section 1.1.5 of 

* {#Lurie09} [[Jacob Lurie]], _[[Higher Topos Theory]]_ (2009)

The details are in section 2.2
