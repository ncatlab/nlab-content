## Idea ##

A _modular tensor category_ is roughly a [[category]] that encodes the _topological_ structure underlying a rational 2-dimensional [[conformal field theory]]. In other words, it is a basis-independent formulation of _Moore-Seiberg data_.

It is in particular a [[fusion category]] this is also a [[ribbon category]] and such that "modularity operation" is non-degenerate (this is what the name "modular tensor category" comes from):

this means that for $i,j \in I$ indices for representative of simple objects $U_i$, $U_j$, the matrix 
$$
  (s^{i j}) = (U_i-circle threading through the U_j-circle)
$$
is non-degenerate.

Here on the right what is means is the diagram in the modular tensor category made from the identityie morphisms, the duality morphisms and the braiding morphism on the objects $U_i$ and $U_j$ that looks lik a fuigure-8 with one circle threading through the other, and this diagram is interpreted as an element in the endormorphism space of the tensor unit object, which in turn is canonically identified with the ground field.

In the description of 2-dimensional [[conformal field theory]] in the [[FFRS-formalism]] it is manifestly this kind of modular diagram that encodes the torus partition function of the CFT. This explains the relevance of modular tensor categories in the description of [[conformal field theory]].

Since 2-dimensional conformal field theory is related by [[quantum holography]] to 3-dimensional [[TQFT]], modular tensor categories also play a role there, which was in fact understood before the full application in conformal field theory was: in the [[[Reshetikhin-Turaev model]].


## Definition ##

A **modular tensor category** is a [[category]] with the following long list of extra structure.

>needs to be put in more coherent form, just a stub

* it is an [[abelian category]], $\mathbb{C}$-linear (i.e. $Vect_{\mathbb{C}}$ [[enriched category]]), [[semisimple category]] [[monoidal catgeory|tensor category]]

* the tensor unit is a simple object, $I$ 
  a finite set of representatives of isomorphism classes of simple objects

* [[fusion category]]

* [[braided monoidal category]]

* [[ribbon category], in particular objects have duals

* **modularity** a non-degeneracy condition on the braiding given by an isomorphism of algebras
  $$
    K(C) \otimes_{\mathbb{Z}} \stackrel{\simeq}{\to} End(Id_C)
  $$
  where
  $$
    [U] \mapsto \alpha_U
  $$
  where the transformation $\alpha_U$ is given on the simple object $V$ by
  $$
    \alpha_U(V) = straight V-line encircled by U-loop
  $$
  (on the right we use string diagram notation)

#References#

section 2.1 of 

* J. Fuchs, I. Runkel, C. Schweigert, _TFT construction of RCFT correlators I: partition functions_ ([arXiv](http://arxiv.org/abs/hep-th/0204148))