
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Type theory
+-- {: .hide}
[[!include type theory - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

[[type|Types]] enable the restriction of the [[domain]] and [[codomain]] of [[computer programs]], but they may not always be precise enough. Refining the [[type system]] of a language involves introducing [[subtypes]] while retaining the [[syntax]] of its [[terms]]. For instance, predicate subtyping can be used to limit `head` to non-empty [[lists]] (`list{ l : len(l) > 0}`) and `div` to non-zero arguments (`int{ n : n <> 0 }`).

More precisely, in [Greenberg 2015](#Greenberg15), [[Frank Pfenning]] describes *type refinement* as a long-term research program with the following goals:

* capture more precise properties of [[programs]],

* retain the good theoretical and practical properties of the simpler disciplines,

* retain usability, modularity, elegance, etc.

Works in this program include:

* *datasort refinements* (types are named *refinement types*) of Freeman, Davies, and Pfenning, which refine the set of available constructors for a type;

* *predicate subtyping* (types are named *refined types* or *predicate subtypes*), where predicates are taken from a tractable domain (see for example *index refinements* of Xi and Pfenning);

but don't include general [[subset types]], as type checking becomes undecidable.

Predicate subtyping is found in languages like [[Liquid Haskell]] and [[F*]].

## Predicate subtyping

### Typing rules

Conditional expressions may be typed using the following rule:

$$ \frac{\Gamma \vdash e:\mathsf{Bool} \qquad \Gamma, \underline{e} \vdash e_1 : T_1 \qquad \Gamma, \underline{\neg e} \vdash e_2 : T_2}{\Gamma \vdash \operatorname{if-then-else}(e, e_1, e_2) : T_1 \sqcup_e T_2} $$

where $\Gamma, \underline{e}$ is the enrichment of $\Gamma$
with the fact that $e$ is true, usually using a dummy variable,
i.e., $\underline{e} = (\underline{} : \{ v : \mathsf{Unit} \mid e \})$,
and where $T_1 \sqcup_e T_2$ is the dependent join of $T_1$ and $T_2$.

$$ T_1 \sqcup_e T_2 = \{ v : T \mid (e \implies v \in T_1) \wedge (\neg e \implies v \in T_2) \} $$

### Example

In a language with (dependent) predicate subtyping, one may implement and type [[negation]] as follows (see [Jhala 2010](#Jhala2010)):

```
val not : x:bool => bool[ b | b ⇔ ¬x ]
let not = x => { if (x) { false } else { true } };
```

## Related concepts

* [[subset type]], [[subtype]]
* [[intrinsic and extrinsic views of typing]]

## References

* {#Greenberg15} Michael Greenberg, _A refinement type by any other name_, 2015, ([blog post](http://www.weaselhat.com/2015/03/16/a-refinement-type-by-any-other-name/)).
* [[Jana Dunfield]], _Combining Two Forms of Type Refinements_, 2002, ([report](https://research.cs.queensu.ca/home/jana/papers/combining/Dunfield02_combining.pdf)).
* [[Robert Atkey]], [[Patricia Johann]], [[Neil Ghani]], _When is a Type Refinement an Inductive Type?_, ([pdf](https://bentnib.org/inductive-refinement.pdf)).

On datasort refinements:

* Tim Freeman, [[Frank Pfenning]], _Refinement types for ML_, Proceedings of the ACM Conference on Programming Language Design and Implementation, 1991, pp. 268&#8211;277, ([pdf](https://www.cs.cmu.edu/~fp/papers/pldi91.pdf)).
* [[Frank Pfenning]], _Church and Curry: Combining Intrinsic and Extrinsic Typing_, ([pdf](https://www.cs.cmu.edu/~fp/papers/andrews08.pdf)).

On predicate subtyping:

* {#Jhala2010} Ranjit Jhala, Niki Vazou, _Refinement Types: A Tutorial_, ([arXiv:2010.07763](https://arxiv.org/abs/2010.07763)).
* Yitzhak Mandelbaum, David Walker, [[Robert Harper]], _An Effective Theory of Type Refinements_, ([pdf](http://www.cs.cmu.edu/~rwh/papers/effref/icfp03.pdf)).
* Susumu Hayashi, _Logic of refinement types_, Proceedings of the Workshop on Types for Proofs and Programs, 1993, pp. 157-172.

On index refinements in particular:

* Hongwei Xi, Frank Pfenning, _Dependent types in practical programming_, in A. Aiken, editor, Conference Record of the 26th Symposium on Principles of Programming Languages (POPL'99),pages 214&#8211;227. ACM Press, January 1999.

On refinement systems as [[functors]]:

* [[Paul-André Melliès]], [[Noam Zeilberger]], _Type refinement and monoidal closed bifibrations_, [arXiv:1310.0263](http://arxiv.org/abs/1310.0263).
* [[Paul-André Melliès]], [[Noam Zeilberger]], _Functors are Type Refinement Systems_, ([pdf](http://noamz.org/papers/funts.pdf) , [HAL](https://hal.inria.fr/hal-01096910)).
* [[Paul-André Melliès]], [[Noam Zeilberger]], _An Isbell Duality Theorem for Type Refinement Systems_, ([pdf](https://www.irif.fr/~mellies/papers/an-isbell-duality-theorem-for-type-refinement-systems.pdf)).

[[!redirects datasort refinement]]
[[!redirects datasort refinements]]
[[!redirects index refinement]]
[[!redirects index refinements]]
[[!redirects predicate subtype]]
[[!redirects predicate subtypes]]
[[!redirects predicate subtyping]]
[[!redirects refined type]]
[[!redirects refined types]]
[[!redirects refinement type]]
[[!redirects refinement types]]
