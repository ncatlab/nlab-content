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

#Remarks#

* If $A = Sets$ then this reproduces the axiom of choice in its traditional form: an epimorphism $A \to B$ of sets can be regarded as a $B$-indexed family of sets. The existence of a section is equivalent to a choice of one element in each set of this family.

* Formulated in terms of sections the _axiom of choice_ may look less mysterious than in its original formulation. For instance, it is clear that it fails in contexts such as $A =$ [[Top]] and $A = $[[Diff]], due to the existence of nontrivial topological and smooth fiber bundles.

* When the full axiom of choice it may still be valid for some restricted class of objects $A$ and/or $B$.  An object $B$ such that any epimorphism $A\to B$ splits is called [[projective object|projective]]; this means that one can make choices 'indexed by' $B$.  Dually, an object $A$ such that one can make choices 'with values in' $A$ is called a [[choice object]] (this is not quite equivalent to every epimorphism $A\to B$ splitting).

* In the context of [[constructive mathematics]], the full axiom of choice in $Set$ implies the principle of [[excluded middle]] and so is rejected.  However, weaker forms of choice, up to [[COSHEP]], are often (if not usually) accepted by constructivists.  One good example is the axiom of _countable choice_, which says that the set $\mathbb{N}$ of [[natural number]]s is projective.  A stronger version is the [[axiom of dependent choice]].

* See also 
  * [[anafunctor]];
  * [[foundations]].


# Equivalents 

The following statements are all equivalent to the axiom of choice in $Set$ (although sometimes the proof in one direction or the other requires [[excluded middle]]):

* The [[well-ordering theorem]] (any set can be [[well-order|well-ordered]])

* [[Zorn's lemma]].

* ($L =$ [[monomorphism]]s, $R =$ [[epimorphism]]s) is a [[weak factorization system]] in [[Set]].
