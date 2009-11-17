<div class="rightHandSide toc">
[[!include model category theory - contents]]
</div>


#Contents#
* automatic table of contents goes here
{:toc}

## Idea ##

To the extent that a [[model category]] is a [[presentable (infinity,1)-category|presentation]] of an [[(∞,1)-category]], the [[localization]] of a model category is a presentation for the [[localization of an (∞,1)-category]].

More specifically this means that 

* for a class of [[morphism]]s $S \subset Mor(C)$ of a [[model category]] $C$ 

* with an object $X \in C$ called an $S$-[[local object]] if for all $f \in S$ the [[(∞,1)-categorical hom-space]] $\mathbf{R}Hom_C(f,X) \in Mor(SSet)$ is a weak equivalence

the left Bousfield localization of $C$ at $S$ is the model category of $S$-local objects in $C$.

More generally this may be considered for any [[enriched model category]] $C$ or even [[enriched homotopical category]] with [[SSet]] replaced by the corresoponding enriched [[monoidal model category]]: one speaks of _enriched Bousfield localization_ ([Bar08](http://arxiv.org/abs/0708.2067)).

More in detail, the left Bousfield localization of $C$ is realized as a new [[model category]] structure on the same underlying category $C$ with 

* more weak equivalences thrown in, namely all $S$-[[local object|local weak equivalences]], that reduce the number of weak equivalence classes of objects to just the $S$-[[local object]]s

* the cofibrations being precisely the original cofibrations.

* this specifies the new fibrations, even though a precise characterization may be hard to come by (frequently, though, some of them are [[homotopy pullback]]s of of fibrations between $S$-[[local object]]s in $C$)

* except that the fibrant objects betwen the $S$-[[local object]]s that are fibrant in $C$.


See also [[localization of a simplicial model category]].



## Definition in model categories ##

Let $C$ be a category equipped with a [[model category]] structure and let $S$ be a class of morphisms in $C$. 

The **left Bousfield localization** of $C$ with respect to $S$ is, if it exists, a [[model category]] structure $L_S C$ on $C$ such that

* the class of weak equivalences of $L_S C$ equals the class of $S$-[[local equivalence]]s of $C$;

* the class of cofibrations of $L_S C$ equals that of $C$;

* the fibrations of $L_S C$ are precisely the morphisms with the right lifting property with respect to the $S$-[[local equivalence|local cofibration]]s of $C$.

Analogously the **right Bousfield localization** is defined as above, with the role of fibrations and cofibrations exchanged throughout.


+-- {: .un_prop }
###### Proposition

If the left Bousfield localization exists, i.e. of $L_S C$ is indeed a [[model category]] with the above definitions of cofibrations and weak equivalences, then it is indeed a [[localization of a model category]] in that

there is a _left Quillen functor_

$$
  j : C \to L_S C
$$

(i.e. $j$ preserves cofibrations and trivial cofibrations and has a [[right adjoint]])

such that the total left [[derived functor]]

$$
  L j : Ho C \to Ho L_S C
$$

takes the images of $S \subset Mor(C)$ in $Ho(C)$ to [[isomorphism]]s

and every other left Quillen functor with this property factors by a unique left Quillen functor through $j$.


=--

+-- {: .proof}
###### Proof

This is theorem 3.3.19 in _ModLoc_ .

=--


## Existence of Bousfield localizations ##

There are various results stating that under suitable conditions the left Bozusfield localization does exist.

+-- {: .un_theorem }
###### Theorem
**(Jeff Smith)**

If (with respect to a given [[Grothendieck universe]]) $C$ is a [[combinatorial model category]] and $S \subset Mor(C)$ is a small [[set]] of [[homotopy]]-classes of morphisms, then the left Bousfield localization $L_S C$ does exist.

Moreover, it satisfies the following conditions:

* it is a left [[proper model category]]

* it is a [[combinatorial model category]]

* the fibrant objectss are the fibrant $S$-[[local object]]s of $C$.

=--

+-- {: .proof}
###### Proof

This is theorem 2.11 in [Bar07](http://arxiv.org/abs/0708.2067))

=--



## Bousfield localization in triangulated categories ##

In the setup of [[triangulated category|triangulated categories]], the Bousfield localization is defined as follows. A *triangulated subcategory* $A$ of a triangulated category $B$ is a nonempty subcategory closed under suspension of objects and such that for all objects $X,Y$ in $A$ if $X\to Y\to Z\to X[1]$ is a distinguished triangle in $B$, then $Z$ is in $A$.  In that case one can define the [[Verdier quotient]] category $B/A$ which is a triangulated category equipped with a canonical functor $Q^*:B\to B/A$ which is also triangulated (additive and preserving distinguished triangles) and universal among all triangulated functors $B\to D$ which send objects of $A$ to objects isomorphic to $0$. A triangulated subcategory $A$ is *thick* if with any object in $A$ it contains all its direct summands in $B$.

In that case, the Verdier quotient $B/A$  has the property that the only objects whose images in $B/A$ are isomorphic to zero are the objects from $A$. Given a thick subcategory $A\subset B$, we say that the **Bousfield localization** exists if the Verdier quotient functor $Q^*$ has a right adjoint functor $Q_*$ which is then (automatically) triangulated and fully faithful. 

## References ##

Bousfield localization appears as definition 3.3.1 in

* **ModLoc** Hirschhorn, _Model categories and their localization_ 

and as proposition A.3.7.3 in

* [[Jacob Lurie]], [[Higher Topos Theory]] .

The relation to [[localization of an (infinity,1)-category]] is also in [[Higher Topos Theory|HTT]], for the time being see the discussion at [[models for ∞-stack (∞,1)-toposes]] for more on that.

A detailed discussion of Bousfield localization also in the context of [[enriched model category|enriched model categories]] is in

* Clark Barwick, _On (enriched) left Bousfield localization of model categories_ ([arXiv](http://arxiv.org/abs/0708.2067))


## Discussion ##

+-- {: .query}

  _Rafael Borowiecki_: How do this relate to Bousfield localization for spectra?

  _Rafael_: Could it be the Bousfield localization of a model category of spectra?

  [[Urs Schreiber]]: could you give me a concrete reference that spells out what you are thinking of when saying "Bousfield localization of spectra"? Then I can try to look at it and see if I can answer your question. I would guess, that, yes, it must refer to the Bousfield localization of a model category o spectra.

  _Rafael_: Here the Bousfield localization is with respect to a class of morphisms S. I found a case where the Bousfield localization is with respect to a spectrum of a generalized (co)homology theory instead. I think this is what i found before:

  [Elliptic cohomology: geometry, applications, and higher chromatic analogues](http://books.google.se/books?id=ofnD0loTwC0C&pg=PA255&lpg=PA255&dq=%22Bousfield+Localization%22+invented&source=bl&ots=0pPUhszwlL&sig=uxZ9U5N1BY1zB7dOBAc5eYB_e20&hl=sv&ei=ztmASvP8O4Wy-AaCkKCzCg&sa=X&oi=book_result&ct=result&resnum=1#v=onepage&q=%22Bousfield%20Localization%22%20invented&f=false)

  [On K(1)-local SU-bordism](http://arxiv.org/PS_cache/arxiv/pdf/0907/0907.4299v1.pdf)

  [Goodwillie towers and chromatic homotopy page8](http://arxiv.org/PS_cache/math/pdf/0410/0410342v2.pdf)

  Again there are different answers for what something is.
  I will stop complaining now. Good luck Urs.

[[Urs Schreiber]]: okay, thanks. So I looked at [def 10, page 10](http://arxiv.org/PS_cache/arxiv/pdf/0907/0907.4299v1.pdf#page=10) of   [On K(1)-local SU-bordism](http://arxiv.org/PS_cache/arxiv/pdf/0907/0907.4299v1.pdf)

This, yes, is a special case of what is decribed here. But just notice the two shades of the use of the word localization here:

let me recall: given a model category $C$ we may choose a set of morphisms $S = \{f : X \to Y\}$ and then say that an object $Z$ is an $S$-[[local object]] if homming $f$ into $Z$ produces isomorphisms.

Then:

* the Bousfield localization of the entire category $C$ is (if it exists) a new model category structure on $C$ where the weak equivalences now are the $S$-[[local equivalence]]

* in as far as the Bousfield localization is a model for a [[localization of an (infinity,1)-category]] every object $Z$ will be weakly equivalent to an $S$-local one $Z_E$, in that there is a morphism $Z \to Z_E$ which is a weak equivalence. Since $Z_E$ is $S$-local in the sense of the definition just recalled, this may be thought of as being the "localization" of the object $Z$.

So what they call localization there is what happens to the _objects_ as we apply Bousfield localization to the category that they live in, essentially. That the objects in their model category happen to be spectra is not important for this general kind of statement. They could be anything.

It may help to think of this in the example where $C$ is a category of [[simplicial presheaf|simplicial presheaves]] and the Bousfield localization is at those weak equivalences that induce the local [[model structure on simplicial presheaves]]. Then the Bousfield localization

$$
  SimpPSh_{glob} \to SimpPSh_{loc}
$$

is [[infinity-stackification]]. In this case the "localization morphism on objects" $Z \to Z_E$ the morphism that make a pre-stack $Z$ weakly equivalent to ist $\infty$-stackification $Z_E$. So here localization=stackification and in terms of that the general kind of situation here may be more familiar.

_Rafael_: Ok, i have thought about it with interest. Good answer. Thx for explaining.
=--


[[!redirects bousfield localization]]
[[!redirects Bousfield localisation]]