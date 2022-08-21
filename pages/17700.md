#Contents#
* table of contents
{:toc}

##Idea 

In [[computer science]], a **side effect** refers simply to the modification of some kind of state, such as changing the value of a variable, writing some data to disk or raising an exception.


## Relation to Monads and Algebras and Multicategories

The presence of side effects in a programming language usually means the language cannot be given a [[denotational semantics]] in the category of [[sets]], or in any [[bicartesian closed category]]. Instead, they can be interpreted in the category of [[algebras]] of a [[monad]] on a [[bicartesian closed category]], often a monad presented by an [[algebraic theory]]. There is a direct relationship between properties of the monad or theory and the type theoretic syntax that can be interpreted in its [[Eilenberg-Moore category|category of algebras]]. 

| [[monads]]  | [[algebraic theories]] |  flavor of [[multicategory]] | typical model |
|---|---|---|---|
| [[strong monad]] | arbitrary theory | [[call-by-push-value]]/[[Freyd multicategory]]  | [[enriched category]] with [[powers]] and [[copowers]] |
| [[monoidal monad]] | [[commutative algebraic theory]] | [[linear logic]]/[[linear-non-linear logic]] | [[symmetric monoidal closed category]]/linear-non-linear adjunction
| [[affine monad]]  | [[affine algebraic theory]] | [[affine logic]] | [[semicartesian monoidal category]] |
| [[relevant monad]] | [[relevant algebraic theory]] | [[relevance logic]] | [[relevance monoidal category]] |
| preserves [[cartesian products]] | affine and relevant theory | [[cartesian multicategory]]/[[S4]] | monoidal adjunction between [[bicartesian closed]] categories

So in typical models, you have a category $V$ of "value types" and pure morphisms and a category $C$ of "comptuation types" or "linear types" and homomorphisms, where $C$ is the category of algebras of a monad on $V$. Then, how the types and terms of a language are interpreted in the model depends on the [[evaluation order]] of the language. In [[call-by-value]] languages, types are interpreted as objects of $V$, but terms $\Gamma \vdash M : A$ are interpreted as Kleisli morphisms $\Gamma \to T A$, or equivalently homomorphisms of free algebras in $C$: $F \Gamma \to F A$. In [[call-by-name]] languages, types are dually interpreted as objects of $C$, but terms $\Gamma \vdash M : A$ are interpreted as co-Kleisli morphisms $U\Gamma \to U A$.

A dual approach would be to start with a category of linear morphisms and construct a category of "value types" as the category of coalgebras of some well-behaved [[comonad]]. This approach is advocated by Girard in his original work on [[linear logic]].

## Related concepts

* [[algebraic effect]]

* [[monad (in computer science)]]

* [[effect handler]]

## References

The conditions on monads above and their relationship to structural rules are described in the following (though the notions themselves are originally due to [[Anders Kock]]).

* {#Jacobs94} [[Bart Jacobs]], _Semantics of Weakening and Contraction_, Annals of Pure and Applied Logic, volume 69, Issue 1, (1994) pp.73-106, doi:[10.1016/0168-0072(94)90020-5](https://doi.org/10.1016/0168-0072%2894%2990020-5)


On side effects in [[dependent type theory|dependent]] ([[dependent linear type theory|linear]]) [[type theory]]:


* [[Matthijs Vákár]], *In Search of Effectful Dependent Types* ([arXiv:1706.07997](https://arxiv.org/abs/1706.07997), [uuid:e91e19b3-7e10-4fda-9433-f23b469e4049](https://ora.ox.ac.uk/objects/uuid:e91e19b3-7e10-4fda-9433-f23b469e4049))



[[!redirects side effects]]

