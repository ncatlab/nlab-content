
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Homotopy theory
+--{: .hide}
[[!include homotopy - contents]]
=--
#### Model category theory
+--{: .hide}
[[!include model category theory - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

A [[model category]] is a [[homotopical category]] equipped with especially nice control over the [[weak equivalences]]. In particular every [[object]] of the category is weakly equivalent to an object that is particularly well-behaved for forming [[derived hom-spaces]] _into_ it.  These are the fibrant objects.  Hence fibrant objects are particularly good representatives of objects, which are the "same" as the given objects up to [[weak equivalence]].

One general intuition is that a fibrant object "has all the operations that it is supposed to".  From this perspective, a general object of a model category is a sort of generalized "presentation" of an algebraic gadget, on which some of the intended operations may be defined partially, but not necessarily all. A fibrant object is then one where all the operations are defined.  This explains why fibrant objects are good for mapping into: if the values of some operations are missing in an object $X$, then some morphisms into $X$ that "ought to exist" may fail because they ought to take image in the missing values of operations.

This concept also exists in [[homotopical categories]] with less [[extra structure]] than that of a full [[model category]]. For instance a [[fibration category]] implements roughly half of the model category axioms, namely those for [[fibrations]], and it has a concept of weakly equivalent replacement by a fibrant object.

The adjective "fibrant" is also used in contexts more general than these, but with a similar intuition.  For instance, there are [[fibrant types]] in [[two-level type theory]], and sometimes [[double categories]] with all [[companions]] and [[conjoints]] are called "fibrant" (or "bifibrant").

The dual concept is a [[cofibrant object]]: an object which is good for mapping *out* of.  These also always exist in model categories, but not necessarily in fibration categories (though they do in the [[formal dual|dual]] notion of [[cofibration categories]]).

## Definition

### In a model category

In a [[model category]], an [[object]] $X$ is said to be **fibrant** if the unique morphism $X\to 1$ to the [[terminal object]] is a [[fibration]].

$$
  (X \;\; \text{fibrant})
   \;\;\Leftrightarrow\;\;
  ( X \overset{\in Fib}{\longrightarrow} 1)
$$

Hence the axiom that every morphism in a model category factors as an [[acyclic cofibration]] followed by a [[fibration]] implies the existence of [[fibrant resolution]].

Namely, for $X$ any object, the factorization of the terminal morphism as an acyclic cofibration followed by a fibration yields a fibrant object $X_{fib}$ weakly equivalent to $X$

   $$
      X 
        \overset{\in Cof \cap W}{\longrightarrow} 
      X_{fib}
        \overset{\in Fib}{\longrightarrow}
      1
   $$



## Examples

1. In the [[classical model structure on topological spaces]], every object $X$ is fibrant (namely the [[continuous function]] $X \to \ast$ to the [[point space]] is a [[Serre fibration]]).

1. In the [[classical model structure on simplicial sets]], the fibrant objects are the [[Kan complexes]].

1. In the [[canonical model structure]] on [[Cat]], every object is fibrant, and similarly in other categorical examples.

## Related concepts

* [[cofibrant object]], [[bifibrant object]]

* [[fibration]], [[cofibration]]

* [[fibrant replacement]]

* [[fibrant type]]

* [[functorial factorization]]

[[!redirects fibrant object]]
[[!redirects fibrant objects]]
[[!redirects fibrancy]]
[[!redirects fibrant]]
