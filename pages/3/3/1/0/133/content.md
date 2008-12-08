In its modern form the axiom of choice in an [[internalization|ambient category]] $A$ says that

* _Every [[epimorphisms]] in $A$ splits._

This means: for every [[epimorphism]] $f : A \to\gt B$ there is a morphis $\sigma : B \to A$ (a [[section]]), such that
$$
  (B \stackrel{\sigma}{\to} A \stackrel{f}{\to} B) 
  =
  (B \stackrel{Id_B}{\to})
  \,.
$$

#Remarks#

* If $A = Sets$ then this reproduces the axiom choice in its traditional form: an epimorphism $A  \to B$ of sets can be regarded as a $B$-indexed family of sets. The existence of a section is equivalent to a choice of one element in each set of this family.

* Formulated in terms of sections the _axiom of choice_ may look much less mysterious. For instance, it is clear that it fails in contexts such as $A =$ [[Top]] and $A = $[[Diff]], due to the existence of nontrivial topological of smooth fiber bundles.

* See also [[anafunctor]].