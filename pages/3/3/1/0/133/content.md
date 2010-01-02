# The axiom of choice
* tic
{: toc}


## Statement

In its modern form, the axiom of choice in an [[internalization|ambient category]] $A$ says that

* _Every [[epimorphism]] in $A$ splits._

This means: for every [[epimorphism]] $f : A \to B$ there is a morphism $\sigma : B \to A$ (a [[section]]), such that
$$
  (B \stackrel{\sigma}{\to} A \stackrel{f}{\to} B) 
  =
  (B \stackrel{Id_B}{\to} B)
  \,.
$$

If the ambient category is not [[balanced category|balanced]], such as a [[regular category|regular]] or [[coherent category]] which is not a [[pretopos]], it may be more appropriate to replace "epimorphism" by [[regular epimorphism]].

If $A$ is a [[extensive category|superextensive]] [[site]], then the axiom of choice for $A$ may be taken to say that, given any [[cover]]ing family $(p_i: U_i \to X)_i$, there is an appropriate section $X \to \coprod_i U_i$.


## Remarks

* If $A = Sets$ then this reproduces the axiom of choice in its traditional form: an epimorphism $A \to B$ of sets can be regarded as a $B$-indexed family of sets. The existence of a section is equivalent to a choice of one element in each set of this family.

* Formulated in terms of sections the _axiom of choice_ may look less mysterious than in its original formulation. For instance, it is clear that it fails in contexts such as $A =$ [[Top]] and $A = $[[Diff]], due to the existence of nontrivial topological and smooth fiber bundles.

* When the full axiom of choice it may still be valid for some restricted class of objects $A$ and/or $B$.  An object $B$ such that any epimorphism $A\to B$ splits is called [[projective object|projective]]; this means that one can make choices 'indexed by' $B$.  Dually, an object $A$ such that one can make choices 'with values in' $A$ is called a [[choice object]] (this is not quite equivalent to every epimorphism $A\to B$ splitting).

* In the context of [[constructive mathematics]], the full axiom of choice in $Set$ implies the principle of [[excluded middle]] and so is rejected.  However, weaker forms of choice, such as [[countable choice]], [[dependent choice]], and [[COSHEP]], are often (if not usually) accepted by constructivists.


## Equivalents 

The following statements are all equivalent to the axiom of choice in $Set$ (although sometimes the proof in one direction or the other requires [[excluded middle]]):

* The [[well-ordering theorem]] (that any set can be [[well-order|well-ordered]]),
* [[Zorn's lemma]],
* that ($L =$ [[monomorphism]]s, $R =$ [[epimorphism]]s) is a [[weak factorization system on Set]].

## Variants

There are a number of weaker axioms which are implied by the full axiom of choice.  Some of these are valid or accepted more generally than the full AC, and/or suffice for some of the usual applications of choice.

* The axiom of [[countable choice]] says that the set $\mathbb{N}$ of [[natural number]]s is projective.  This suffices for many of the usual applications of choice in analysis.

* The axiom of [[dependent choice]] strengthens countable choice by allowing the set of possible choices for $n+1$ to depend on the choice made for $n$.

* The axiom [[COSHEP]], also called the "presentation axiom," says that any set admits a surjection from a projective one (whereas full AC says that all sets are projective).  This is sufficient for the existence of projective resolutions and cofibrant replacements.  For example, see the [[folk model structure on Cat]].

The axiom of choice can also be strengthened in a few ways.

* While the ordinary axiom of choice says that any surjection of sets is split, the *axiom of global choice* says that this is also true for any surjection of [[proper classes]].  (Making this precise requires a bit of work.)  It is equivalent to the existence of a well-ordering of the class of all sets.

* One can also postulate a [[choice operator]], which gives a *specified* way to choose an element from any nonempty set.  This implies global choice, and conversely a choice operator can be defined from any well-ordering of the class of all sets.


## See also

* [[anafunctor]];
* [[foundations]].


category: foundational axiom