
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Model theory
+-- {: .hide}
[[!include model theory - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

A _[[structure]]_ in [[mathematics]] (also "mathematical structure") is often taken to be a [[set]] equipped with some choice of elements, with some operations and some relations. Such as for instance the "structure of a [[group]]". In [[model theory]] this concept of mathematical structure is formalized by way of [[formal logic]]. 

Notice however that by far not every concept studied in [[mathematics]] fits as an example of a mathematical structure in the sense of classical [[first-order theory|first order]] model theory, described [below](#Definition). For instance a concept as basic as that of  [[topological spaces]] fails to be a structure in the sense of classical model theory (see [here](#MathSEDisc)). 

In [[category theory]] there is a more flexible concept of _[[structure]]_, see there.


## Definition
 {#Definition}

Given a [[first-order language]] $L$, which consists of symbols ([[variable|variable symbols]], constant symbols, [[function symbols]] and [[relation]] symbols including $\epsilon$) and [[quantifiers]]; a __structure__ for $L$, or "$L$-structure", is a [[set]] $M$ with an __interpretation__ for symbols: 

* if $R\in L$ is an $n$-ary [[relation]] symbol, then its interpretation $R^M\subset M^n$

* if $f\in L$ is an $n$-ary [[function]] symbol, then $f^M:M^n\to M$ is a function 

* if $c\in L$ is a constant symbol, then $c^M\in M$

The underlying set $M$ of the structure is referred to as (universal) __domain__ of the structure (or the universe of the structure).

Interpretation for an $L$-structure inductively defines an interpretation for well-formed formulas in $L$. We say that a sentence $\phi\in L$ is [[true]] in $M$ if $\phi^M$ is true. Given a [[theory]] $(L,T)$, which is a language $L$  together with a given set $T$ of sentences in $L$ ([[axioms]]), the interpretation in a structure $M$ makes those sentences true or false; if all the sentences in $T$ are true in $M$ we say that $M$ is a [[model]] of $(L,T)$. 

In [[model theory]], given a language $L$, a structure for $L$ is the same as a [[model]] of $L$ as a [[theory]] with an empty set of axioms. Conversely, a _model_ of a theory is a _structure_ of its underlying language that satisfies the axioms demanded by that theory.

There is a generalization of structure for languages/theories with multiple domains or sorts, called multi-sorted languages/theories. 

## Properties

### Elementary classes of structures

A class $K$ of structures of a given signature is an __elementary class__ if there is a [[first-order theory]] $T$ such that $K$ consists precisely of all models of $T$. 

There is a vast generalizations for higher-order theories (and more), see at  _[[abstract elementary class]]_ and _[[metric abstract elementary class]]_.

### Categories of structures

Every [[algebraic category]] whose [[forgetful functor]] preserves [[filtered colimits]] is the category of [[models]] for some [[first-order theory]]. The converse is false.

A detailed discussion of characterizations of [[categories]] of structures in the sense of  model theory is in ([Beke-Rosciky 11](#BekeRosciky11)).


### Interpretation in categorical logic 
 {#CategoricalInterpretation}

Every [[first-order language]] $L$ gives rise to a [[first-order hyperdoctrine]] with [[equality]] freely generated from $L$. Denoting this by $T(L)$, the base category $C_{T(L)}$ consists of sorts (which are products of basic sorts) and functional terms between sorts; the [[predicates]] are [[equivalence classes]] of [[relations]] definable in the language. The construction of $T(L)$ depends to some extent on the [[logic]] we wish to impose; for example, we could take the free [[Boolean hyperdoctrine]] generated from $L$ if we work in [[classical logic]]. 

There is also a "tautological" first order hyperdoctrine whose base category is $Set$, and whose predicates are given by the power set functor 

$$P \colon Set^{op} \to Bool$$ 

and then an interpretation of $L$, as described above, amounts to a morphism of hyperdoctrines $T(L) \to Taut(Set)$. 

This observation opens the door to a widened interpretation of "interpretation" in [[categorical logic]], where we might for instance generalize [[Set]] to any other [[topos]] $E$, and use instead $Sub \colon E^{op} \to Heyt$ (taking an object of $E$ to its [[Heyting algebra]] of [[subobjects]]) as the receiver of interpretations. This of course is just one of many possibilities. 


## References

Standard textbook accounts include

* [[Wilfrid Hodges]], section 1 of _A shorter model theory_, Cambridge University Press (1997)

* Chen Chung Chang, H. Jerome Keisler, _Model Theory. Studies in Logic and the Foundations of Mathematics_. 1973, 1990, Elsevier. 


Characterizations of [[categories]] of model-theoretic structures  and [[homomorphisms]] between them (certain accessible categories) is discussed in

* {#BekeRosciky11} [[Tibor Beke]], [[Jiří Rosický]], _Abstract elementary classes and accessible categories_, 2011   ([pdf](http://www.math.muni.cz/~rosicky/papers/elem7.pdf))

Online discussion includes

* {#MathSEDisc} Math.SE _[Topological spaces as model-theoretic structures &#8212; definitions?](http://math.stackexchange.com/questions/97856/topological-spaces-as-model-theoretic-structures-definitions)_
[[!redirects structures in model theory]]

[[!redirects mathematical structure]]
[[!redirects mathematical structures]]

[[!redirects structure (in model theory)]]
[[!redirects structures (in model theory)]]