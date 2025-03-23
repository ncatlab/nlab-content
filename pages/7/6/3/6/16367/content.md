+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Model category theory
+--{: .hide}
[[!include model category theory - contents]]
=--
#### Monoidal categories
+--{: .hide}
[[!include monoidal categories - contents]]
=--
#### Higher algebra
+--{: .hide}
[[!include higher algebra - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}


## Idea

Let $C$ be [[symmetric monoidal category]] and $C$ the category of [[commutative monoids]] in $C$.
When $C$ is further a [[model category]], there are certain conditions under which there is an induced [[model structure]] on $CMon(C)$, where the [[weak equivalences]] and [[fibrations]] are defined as in $C$.

## Distinction between E-infinity monoids

Recall that $CMon(C)$ can be described as the category of [[algebras over an operad]] over the [[operad]] [[Comm]].
If the operad [[Comm]] were [[cofibrant object|cofibrant]], then for the existence of the induced model structure on $CMon(C)$ it would be sufficient to require the [[monoid axiom in a monoidal model category|monoid axiom]], and to use the [[model structure on algebras over an operad]] as discussed there.
However [[Comm]] is in general not cofibrant, and this is the distinction between [[Comm]] and the [[E-infinity operad]]: the latter is a [[cofibrant replacement]] of the former.
This is why the [[model structure]] on [[commutative monoids]] may not always exist even when the model structure on [[E-infinity monoids in a symmetric monoidal model category]] does.

For example, take $C$ to be the category of [[chain complexes]] over a [[field]] of [[positive characteristic]].
Then the category of [[commutative monoids]] in $C$ is the category of [[commutative dg-algebras]].
This does not have an induced [[model structure]], as explained in [MO/23885/2503](http://mathoverflow.net/a/23885/2503).

See [Rectification](#Rectification) for some results on when the [[model structures]] on [[E-infinity monoids]] and [[commutative monoids]] are [[Quillen equivalent]], though.

## Model structure

Let $C$ be a [[symmetric monoidal model category]] and let $CMon(C)$ denote the category of [[commutative monoids]] in the underlying category of $C$.
Define a [[weak equivalence]] (resp. [[fibration]]) of [[commutative monoids]] to be a [[weak equivalence]] (resp. [[fibration]]) of the underlying objects of $C$.
Below we will give sufficient conditions for this to define a [[model structure]] on $CMon(C)$.

+-- {: .un_theorem}
###### Theorem
Suppose that

  * $C$ is [[combinatorial model category|combinatorial]],

  * $C$ is _freely powered_, i.e.

    * $C$ satisfies the [[monoid axiom in a monoidal model category]],

    * $C$ is [[left proper model category|left proper]] and ...

    * every cofibration in $C$ is a _power cofibration_, i.e. ...

Then the category $CMon(C)$ is a [[combinatorial model category]] with [[weak equivalences]] and [[fibrations]] as defined above.
=--

See ([Lurie](#LurieHA), Proposition 4.5.4.6).

Next we state a more general version of this result, for which we will require some set-theoretic assumptions.
Suppose that $C$ is [[cofibrantly generated model category|cofibrantly generated]] by a set of [[cofibrations]] $I$ and a set of [[trivial cofibrations]] $J$.
Let $I \otimes C$-cell denote the closure of $I \otimes C = \{ i \otimes \id_X : i \in I, X \in Ob(C) \}$ under [[cobase change]] and [[transfinite composition]], and similarly for $J \otimes C$-cell.

+-- {: .un_theorem}
###### Theorem
Suppose that

  * $C$ is [[cofibrantly generated model category|cofibrantly generated]] by a set of cofibrations $I$ and a set of fibrations $J$,

  * the [[domains]] of the morphisms in $I$ (resp. $J$) are [[small objects]] relative to $(I\otimes C)$-cell (resp. $(J\otimes C)$-cell),

  * $C$ satisfies the [[monoid axiom in a monoidal model category]]

  * $C$ satisfies the _commutative monoid axiom_, i.e. ...

Then the category $CMon(C)$ is a [[cofibrantly generated model category]] with [[weak equivalences]] and [[fibrations]] as defined above.

If $C$ is further [[simplicial model category|simplicial]] (resp. [[combinatorial model category|combinatorial]], [[tractable model category|tractable]]), then so is $CMon(C)$.
=--

See ([White 14](#White14), Theorem 3.2).

## Rectification {#Rectification}

Rectification of $E_\infty$-monoids is the question of whether the [[weak equivalence]] between the [[operads]] [[Comm]] and the [[E-infinity operad]] induces a [[Quillen equivalence]] on the [[model category of algebras over an operad|model categories of algebras]].
Since the [[model category of algebras over an operad]] over the [[E-infinity operad]] is a presentation of the [[(infinity,1)-category]] of [[commutative monoids in a symmetric monoidal (infinity,1)-category]], rectification for $C$ is equivalent to saying that the [[(infinity,1)-category]] presented by the model structure on [[commutative monoids]] is equivalent to the [[(infinity,1)-category]] of [[commutative monoids in a symmetric monoidal (infinity,1)-category]] in the [[symmetric monoidal (infinity,1)-category]] presented by $C$.

The following cases are particularly interesting.

* Rectification holds in the [[model category]] of [[symmetric spectra]].
* It does not hold in the [[model category]] of [[simplicial sets]] or in the [[model category]] of [[simplicial abelian groups]].

See ([Lurie](#LurieHA), Theorem 4.5.4.7) for sufficient conditions for rectification to hold.
See also ([White 14](#White14), Paragraph 4.2) for more discussion.

A general rectification criterion for [[symmetric monoidal model categories]] is formulated in [PS 14](#PS14), Proposition&#160;10.1.2 and Theorem&#160;9.3.6.
It says that given a [[tractable]] symmetric monoidal model category&#160;that satisfies a certain
compact generatedness assumption
with a morphism of [[admissible operads]] $A\to B$
(e.g., $A=E_\infty$, $B=Comm$),
the Quillen adjunction between $A$-monoids and $B$-monoids induced by the morphism
of operads $A\to B$ is a Quillen equivalence
if and only if for any cofibration&#160;$s$ and any $n\ge0$
the morphism $(A_n\to B_n)\wedge_{\Sigma_n}s^{\wedge n}$ is a weak equivalence, where $\wedge$ denotes the [[pushout product]] with respect to the monoidal structure.

## Related concepts

* [[model structure on E-infinity monoids in a symmetric monoidal model category]]

* [[model structure on monoids in a monoidal model category]]

* [[commutative monoid in a symmetric monoidal (infinity,1)-category]]

* [[model structure on algebras over an operad]]

* [[model structure on algebras over a monad]]

* [[model structure on simplicial T-algebras]]

## References

* {#White14} [[David White]], _Model Structures on Commutative Monoids in General Model Categories_, [arXiv:1403.6759](http://arxiv.org/abs/1403.6759).

* {#LurieHA} [[Jacob Lurie]], _[[Higher Algebra]]_.

* {#PS14} [[Dmitri Pavlov]] and [[Jakob Scholbach]], _Admissibility and rectification of colored symmetric operads_, [arXiv:1410.5675](http://arxiv.org/abs/1410.5675).

[[!redirects commutative monoids in a symmetric monoidal model category]]

[[!redirects model structure on commutative monoids]]
[[!redirects model structures on commutative monoids]]
[[!redirects model category of commutative monoids]]
[[!redirects model categories of commutative monoids]]
[[!redirects model category of commutative monoids in a symmetric monoidal model category]]
[[!redirects model categories of commutative monoids in a symmetric monoidal model category]]

[[!redirects model structure on commutative monoids in a symmetric monoidal model category]]