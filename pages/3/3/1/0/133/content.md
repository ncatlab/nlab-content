In its modern form the axiom of choice in an [[internalization|ambient category]] $A$ says that

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

* The axiom of choice in [[Set]] is equivalent to the statement that the pair ($L =$ [[monomorphism]]s, $R =$ [[epimorphism]]s) is a [[weak factorization system]] in [[Set]].

* In the context of [[constructive mathematics]], the full axiom of choice in $Set$ implies the principle of [[excluded middle]] and so is rejected.  However, weaker forms of choice, up to [[COSHEP]], are often (if not usually) accepted by constructivists.

* The axiom of choice in $Set$ implies (and is implied by, given excluded middle) the [[well-ordering theorem]].

* See also 
  * [[anafunctor]];
  * [[foundations]].