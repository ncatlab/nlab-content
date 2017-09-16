#Idea#

To the extent that a [[model category]] is a [[presentable (infinity,1)-category|presentation]] of an [[(infinity,1)-category]], the [[localization]] of a model category is a presentation for the [[localization of an (infinity,1)-category]].

See also [[localization of a simplicial model category]].


#Definition in model categories#

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

+-- {: .query}

  _Rafael Borowiecki_: How do this relate to Bousfield localization for spectra?

  _Rafael_: Could it be the Bousfield localization of a model category of spectra?

  [[Urs Schreiber]]: could you give me a concrete reference that spells out what you are thinking of when saying "Bousfield localization of spectra"? Then I can try to look at it and see if I can answer your question. I would guess, that, yes, it must refer to the Bousfield localization of a model category o spectra.

  _Rafael_: Here the Bousfield localization is with respect to a class of morphisms S. I found a case where the Bousfield localization is with respect to a spectrum of a generalized (co)homology theory instead. I think this is what i found before:

  [Elliptic cohomology: geometry, applications, and higher chromatic analogues](http://books.google.se/books?id=ofnD0loTwC0C&pg=PA255&lpg=PA255&dq=%22Bousfield+Localization%22+invented&source=bl&ots=0pPUhszwlL&sig=uxZ9U5N1BY1zB7dOBAc5eYB_e20&hl=sv&ei=ztmASvP8O4Wy-AaCkKCzCg&sa=X&oi=book_result&ct=result&resnum=1#v=onepage&q=%22Bousfield%20Localization%22%20invented&f=false)
  [On K(1)-local SU-bordism](http://arxiv.org/PS_cache/arxiv/pdf/0907/0907.4299v1.pdf)
  [Goodwillie towers and chromatic homotopy page8](http://arxiv.org/PS_cache/math/pdf/0410/0410342v2.pdf)

  Again there are different answers for what something is.
=--

#Bousfield localization in triangulated categories#

In the setup of [[triangulated category|triangulated categories]], the Bousfield localization is defined as follows. A *triangulated subcategory* $A$ of a triangulated category $B$ is a nonempty subcategory closed under suspension of objects and such that for all objects $X,Y$ in $A$ if $X\to Y\to Z\to X[1]$ is a distinguished triangle in $B$, then $Z$ is in $A$.  In that case one can define the [[Verdier quotient]] category $B/A$ which is a triangulated category equipped with a canonical functor $Q^*:B\to B/A$ which is also triangulated (additive and preserving distinguished triangles) and universal among all triangulated functors $B\to D$ which send objects of $A$ to objects isomorphic to $0$. A triangulated subcategory $A$ is *thick* if with any object in $A$ it contains all its direct summands in $B$.

In that case, the Verdier quotient $B/A$  has the property that the only objects whose images in $B/A$ are isomorphic to zero are the objects from $A$. Given a thick subcategory $A\subset B$, we say that the **Bousfield localization** exists if the Verdier quotient functor $Q^*$ has a right adjoint functor $Q_*$ which is then (automatically) triangulated and fully faithful. 

#References#

Bousfield localization appears as definition 3.3.1 in

* **ModLoc** Hirschhorn, _Model categories and their localization_ 

and as proposition A.3.7.3 in

* [[Jacob Lurie]], [[Higher Topos Theory]] .

The relation to [[localization of an (infinity,1)-category]] is also in [[Higher Topos Theory|HTT]], for the time being see the discussion at [[models for infinity-stack (infinity,1)-toposes]] for more on that.

A detailed discussion of Bousfield localization also in the context of [[enriched model category|enriched model categories]] is in

* Clark Barwick, _On (enriched) left Bousfield localization of model categories_ ([arXiv](http://arxiv.org/abs/0708.2067))


[[!redirects bousfield localization]]
[[!redirects Bousfield localisation]]