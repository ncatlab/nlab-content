#Idea#

In the modern perspective _homotopy theory_ is the theory of $(\infty,1)$-categories: those $\infty$-categories in which all $k$-morphisms for $k \gt 1$ are invertible.

The archetypical example is the $(\infty,1)$ category $Top$ of (suitably well behaved...) topological spaces: objects are topological spaces, morphisms are continuous maps between these, 2-morphisms are homotopies of such maps, and $k$-morphisms are higher order homotopies of homotopies.

A convenient and powerful way to handle such a situation is to consider only the 1-morphisms, but remember certain special properties of these 1-morphisms with regard to the higher morphisms associated with them. The three special properties that one remembers of a 1-morphisms is that it may be a

 * [[fibration]] $\to \gt$;

 * [[cofibration]] $\hookrightarrow$;

 * [[weak equivalence]] $\stackrel{\simeq}{\to}$.

The idea is that these morphisms correspond to the 

 * [[epimorphism]]s;

 * [[monomorphism]]s;

 * [[isomorphism]]s

"up to homotopy", i.e. up to the higher morphisms in the $(\infty,1)$-categorical context.

Quillen had axiomatized the relations to be satisfied by a collection of cofibrations, fibrations and weak equivalences to qualify as the "1-dimensional shadow" of an $(\infty,1)$-category. Categories satisfying these axioms are called [[model category|model categories]]. 

The original idea of this terminology was that these are _models_ for the homotopy theory of topological spaces. In particular simpler models. There is a model category structure on the category of simplicial sets, for instance, which is equivalent ("Quillen equivalent") to that of topological spaces. This can hence be regarded as providing a "combinatorial model" for topological spaces, as far as only their properties up to homotopy are concerned.

#Terminology#

 * Morphisms which are both (co)fibrations and weak equivalences are called **acyclic (co)fibrations**.

* **Generalized morphisms** are sequences of zig-zags
$
  \stackrel{\simeq}{\leftarrow}
  \to
  \stackrel{\simeq}{\leftarrow}
  \to
  \cdots
$.

#Related concepts#

There are several concepts in the literature which are _secretly_ special cases of general homotopy theory:

* [[anafunctor]]s are the generalized morphisms of length 1 in the [[folk model structure]] on $1Categories$;

* [[Morita morphism]] in the theory of [[Lie groupoid]]s are generalized morphisms of length one where both maps are acyclic fibrations
$ \lt \stackrel{\simeq}{\leftarrow} \stackrel{\simeq}{\to} \gt$ with respect to the [[folk model structure]]. This are the _saturated_ [[anafunctor]]s.


#Literature#

long list goes here, but for the moment there is just:

Julia Bergner, _A survey of $(\infty,1)$-categories_ ([arXiv](http://arxiv.org/abs/math/0610239)).