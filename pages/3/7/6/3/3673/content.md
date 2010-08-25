
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Model category theory
+--{: .hide}
[[!include model category theory - contents]]
=--
=--
=--


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

an [[adjunction]] with [[right adjoint]] $U$. Say a morphism in $D$ is a fibration or weak equivalence precisely if its image under $U$ is, respectively, in $C$.

+-- {: .un_prop}
###### Proposition

Sufficient conditions for this to define a cofibrantly generated model category structure on $D$ are

1. the functor $F$ preserves [[small object]]s

   this is the case in particular when $U$ preserves [[filtered colimit]]s;

1. any [[sequential colimit]] of [[pushout]]s of images under $F$ of the generating trivial cofibrations in $C$ yields a weak equivalence in $D$;

   this is the case in particular if

   * $D$ has a fibrant replacement functor;

   * and $D$ has functorial [[path object]]s for fibrant objects.

=--

### Enrichment {#Enrichment}

Often the underlying model category $C$ is an [[enriched model category]] over some [[monoidal model category]] $S$ and one wishes to transfer also the model enrichment.

+-- {: .un_prop}
###### Observation

Assume the adjunction

$$
  (F \dashv U )\; : \; D \stackrel{\overset{F}{\leftarrow}}{\underset{U}{\to}} C
$$

satisfies the conditions of the above proposition so that the model structure on $C$ is transferred to $D$. Consider the case that $C$ is moreover an $S$-[[enriched model category]] and that $D$ can be equipped with the structure of a $S$-[[enriched category]] that is also  $S$-[[power]]ed and [[copower]]ed. 

Assume now that the $S$-powering of $D$ is taken by $U$ to the $S$-powering of $C$, in that $U(d^{(s_1 \to s_2)}) = U(d)^{(s_1 \to s_2)}$.

Then the transferred model structure and the $S$-enrichment on $D$ are compatible and make $D$ an $S$-enriched model category.

=--

+-- {: .proof}
###### Proof

By the axioms of [[enriched model category]] one sufficient condition to be checked is that for $s \to t$ any cofibration in $S$ and for $X \to Y$ any fibration in $D$, we have that the induced morphism

$$
  X^t \to X^s \times_{Y^s} Y^{t}
$$

is a fibration, which is a weak equivalence if at least one of the two input morphisms is. By the induced model structure, this is checked by applying $U$. But by assumption $U$ commutes with the powering, and since $U$ is a [[right adjoint]] it commutes with taking the pullback, so that under $U$ the morphism is

$$
  U(X)^t \to U(X)^s \times_{U(Y)^s} U(Y)^{t}
$$

which is the morphism induced from $U(X) \to U(Y)$. That this is indeed an (acyclic) fibration follows now from the fact that $C$ is an $S$-enriched model category.


=--


## Examples

* The [[model structure on algebraic fibrant objects]] is transferred from the underlying model category by forgetting the choice of fillers.

...

+--{: .query}
[[Mike Shulman]]: In addition to lots of examples, I think it would be also nice to include here a *non* example, of a case where the putative transferred model structure provably *doesn't* exist.
=--


## References

The study of transfer of model structures in this sense is apperently originally due to 

* [[Sjoerd Crans]], _Quillen closed model structure for sheaves_ ([web](http://citeseerx.ist.psu.edu/viewdoc/summary?doi=10.1.1.48.7459))

Summaries and further pointers to the literature happen to be on [p. 20](http://arxiv.org/PS_cache/math/pdf/0609/0609537v2.pdf#page=20) of

* [[Paul Goerss]], [[Kristen Schemmerhorn]], _Model Categories and Simplicial Methods_ ([arXiv](http://arxiv.org/abs/math.AT/0609537))

and on p. 6 of

* [[Clemens Berger]], [[Ieke Moerdijk]], _Axiomatic homotopy theory for operads_  ([pdf](http://www.math.uu.nl/publications/preprints/1242.pdf))

