[[!redirects equivalence of quasi-categories]]

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### $(\infty,1)$-Category theory
+--{: .hide}
[[!include quasi-category theory contents]]
=--
#### Equality and Equivalence
+--{: .hide}
[[!include equality and equivalence - contents]]
=--
=--
=--




#Contents#
* table of contents
{:toc}


## Definition 

An [[(∞,1)-functor]] between [[(∞,1)-categories]] is an _[[equivalence in an (∞,1)-category|equivalence]]_ in [[(∞,1)Cat]] precisely if it is an [[essentially surjective (∞,1)-functor]] and a [[full and faithful (∞,1)-functor]].  

When [[(∞,1)-categories]] are presented by [[quasi-categories]], an equivalence between them is presented by a [[weak equivalence]] in the  [[model structure for quasi-categories]].

## Properties 

+-- {: .num_lemma }
###### Lemma

An [[(∞,1)-functor]] $f : C \to D$ is an **equivalence** in [[(∞,1)Cat]] if  the following equivalent conditions hold

* On the underlying [[simplicial set]]s it is a weak categorical equivalence in Joyal's [[model structure for quasi-categories]].

* For every [[simplicial set]] $K$ the induced morphism $f_* : SSet(K,C) \to SSet(K,D)$ is a [[model structure for quasi-categories|weak categorical equivalence]].

* For every [[simplicial set]] $K$ the induced morphism $f_* : Core(SSet(K,C)) \to Core(SSet(K,D))$ on the maximal [[Kan complex]]es is a [[model structure on simplicial sets|equivalence of Kan complexes]] (a [[homotopy equivalence]]).

* The induced morphism $f_* : Core(SSet(\Delta^1, C)) \to Core(SSet(\Delta^1, D))$ is an equivalence of Kan complexes.

=--

+-- {: .proof}
###### Proof

The equivalence of the first three points is [[Higher Topos Theory|HTT, lemma 3.1.3.2]].

[Cisinki](#Cisinki), theorem 3.9.2, shows the third point can be weakened to taking just $K = \Delta^0, \Delta^1$, so to show equivalence with the fourth point, it suffices to show the $K = \Delta^1$ case implies the $K = \Delta^0$ case.

Suppose that $f_* : Core(SSet(\Delta^1, C)) \to Core(SSet(\Delta^1, D))$ is an equivalence. For each object $d \in D_0$, there is an edge $\varphi : c \to c'$ in $C_1$ such that $f_*(\varphi) \simeq id_d$. This implies $f(c) \simeq d$ and thus $f_*(id_c) \simeq id_d$, and that $\varphi \simeq id_c$.

Thus, $f_*$ restricts to an equivalence between the subcomplexes consisting of the connected components of the identity morphisms. But for any quasi-category $X$, this subcomplex is $\Core(X)^{\Delta^1} \subseteq \Core(X^{\Delta^1})$, and the degeneracy $\Core(X) \to \Core(X)^{\Delta^1}$ is an equivalence. Thus, the induced map $Core(C) \to Core(D)$ is an equivalence.

=--

## Related concepts

* [[equality]]

* [[isomorphism]]

* [[equivalence]]

* [[weak equivalence]]

* [[homotopy equivalence]], [[weak homotopy equivalence]]

* [[homotopy equivalence of toposes]]

* [[equivalence in an (∞,1)-category]]

* [[equivalence of categories]], [[adjoint functor]]

* [[equivalence of 2-categories]], [[2-adjunction]]

* [[equivalence of (2,1)-categories]]

* **equivalence of (∞,1)-categories**, [[adjoint (∞,1)-functor]]


[[!include properties of functors -- contents]]



[[!redirects equivalence of (∞,1)-categories]]
[[!redirects equivalences of (∞,1)-categories]]


[[!redirects equivalence of (infinity,1)-categories]]
[[!redirects equivalences of (infinity,1)-categories]]


## References

* {#Cisinksi} [[Denis-Charles Cisinski]], "Higher Categories and Homotopical Algebra"