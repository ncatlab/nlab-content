
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

A [[model category]] is a [[homotopical category]] equipped with especially nice control over the [[weak equivalences]]. In particular every [[object]] of the category is weakly equivalent to an object that is particularly well-behaved for forming [[derived hom-spaces]] _out of_ it.  These are the cofibrant objects.  Hence cofibrant objects are particularly good representatives of objects, which are the "same" as the given objects up to [[weak equivalence]].

One general intuition is that a cofibrant object is one that's uncoiled, unwound or puffed up. An object oftens fails to be cofibrant when it's "coiled up too tightly", with a bunch of strict equations that should be equivalences or paths.  This explains why cofibrant objects are good for mapping out of: if some equations in $X$ hold too strictly, then those equations would have to be preserved by a (strict) map out of $X$, which might not be possible if the intended codomain doesn't have such strict equations.

This concept also exists in [[homotopical categories]] with less [[extra structure]] than that of a full [[model category]]. For instance a [[cofibration category]] implements roughly half of the model category axioms, namely those for [[cofibrations]], and it has a concept of weakly equivalent replacement by a cofibrant object.

The adjective "cofibrant" is also used in contexts more general than these, but with a similar intuition.  For instance, there are [[cofibrant types]] in [[two-level type theory]].

The dual concept is a [[fibrant object]]: an object which is good for mapping *into*.  These also always exist in model categories, but not necessarily in cofibration categories (though they do in the [[formal dual|dual]] notion of [[fibration categories]]).

## Definition

### In a model category

In a [[model category]], an object $X$ is said to be **cofibrant** if the unique morphism $0\to X$ from the [[initial object]] is a [[cofibration]].

$$
  (X \;\; \text{cofibrant})
   \;\;\Leftrightarrow\;\;
  ( 0 \overset{\in Cof}{\longrightarrow} X)
$$

Hence the axiom that every morphism in a model category factors as a [[cofibration]] followed by an [[acyclic fibration]] implies the existence of [[cofibrant resolution]].

Namely, for $X$ any object, the factorization of the initial morphism as a cofibration followed by an acyclic fibration yields a cofibrant object $X_{cof}$ weakly equivalent to $X$

   $$
     0 
       \overset{\in Cof}{\longrightarrow}
     X_{cof}
       \overset{\in Fib \cap W}{\longrightarrow}
     X
   $$

## Examples

1. In the [[classical model structure on topological spaces]], the cofibrant objects are the [[retracts]] of [[cell complexes]], in particular the [[CW-complexes]].

1. In the [[classical model structure on simplicial sets]], every object is cofibrant.

1. In the [[canonical model structure]] on [[Cat]], every object is cofibrant.  However, this ceases to be the case in other canonical categorical model structures.  For instance, in the [[canonical model structure on 2-categories]], the cofibrant objects are those whose underlying 1-category is freely generated by a quiver.

1. In the projective [[model structure on dgc-algebras]] in non-negative degree, the cofibrant objects are the [[Sullivan algebras]] (see [there](model+structure+on+dg-algebras#SullivanAlgebras)). This plays a key role in [[rational homotopy theory]].

## Related concepts

* [[fibrant object]], [[bifibrant object]]

* [[fibration]], [[cofibration]]

* [[cofibrant replacement]]

* [[cofibrant type]]

* [[functorial factorization]]

[[!redirects cofibrant object]]
[[!redirects cofibrant objects]]
[[!redirects cofibrant]]
[[!redirects cofibrancy]]
