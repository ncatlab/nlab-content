
<div class="rightHandSide toc">
[[!include model category theory - contents]]
</div>


#Contents#
* automatic table of contents goes here
{:toc}


## Idea

For $C$ a [[category]] with the structure of a [[model category]] and 

$$
 (F \dashv U )\; : \; D \stackrel{\overset{F}{\leftarrow}}{\underset{U}{\to}} C
$$

an [[adjunction]] with $U$ [[right adjoint]], under certain conditions it is possible  to _transfer_ the model structure from $C$ to a model structure on $D$ by declaring the fibrations and weak equivalences in $D$ to be precisely those morphisms whose image under $U$ are fibrations or weak equivalences, respectively, in $C$.

Typically this arises in situations where $D$ consist of the "same" objects as $C$ but equipped with extra [[stuff, structure, property]], and $U$ is the corresponding [[forgetful functor]] sending objects in $D$ to their underlying objects in $C$. Then $F$ is the corresponding [[free functor]].

## Properties

Let $C$ be a [[cofibrantly generated model category]] and

$$
  (F \dashv U )\; : \; D \stackrel{\overset{F}{\leftarrow}}{\underset{U}{\to}} C
$$

an [[adjunction]] with [[right adjoint]] $U$. Say a morphism in $D$ is a fibraton or weak equivalence precisely if its image under $U$ is, respectively, in $C$.

**Proposition** Sufficient conditions for this to define a cofibrantly generated model category structure on $D$ are

1. the functor $F$ preserves [[small object]]s

   this is the case in particular when $U$ preserves [[filtered colimit]]s;

1. any [[sequential colimit]] of [[pushout]]s of images under $F$ of the generating trivial cofibrations in $C$ yields a weak equivalence in $D$;

   this is the case in particular if

   * $D$ has a fibrant replacement functor;

   * and $D$ has functorial [[path object]]s for fibrant objects.


## Examples

...

+--{: .query}
[[Mike Shulman]]: In addition to lots of examples, I think it would be also nice to include here a *non* example, of a case where the putative transferred model structure provably *doesn't* exist.
=--


## References

The study of transfer of model structures in this sense is apperently originally due to 

* [[Sjoerd Crans]], _Quillen closed model structure for sheaves_ ([web](http://citeseerx.ist.psu.edu/viewdoc/summary?doi=10.1.1.48.7459))

A summary and further pointers to the literature happen to be on p. 6 of

* [[Clemens Berger]], [[Ieke Moerdijk]], _Axiomatic homotopy theory for operads_  ([pdf](http://www.math.uu.nl/publications/preprints/1242.pdf))