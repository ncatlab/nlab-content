#Idea#

Recall that the [[homotopy category]] $Ho_C$ of a [[category with weak equivalences]] $C$ or of a [[homotopical category]] is the best 1-categorical approximation to the [[(infinity,1)-category]] in which the weak equivalences of $C$ are literally [[equivalence]]s.

Analagously, for $F : C \to D$ a functor, a _derived functor_ of $F$ is a 1-categorical approximation to a functor which respects the weak equivalences in $C$.  If $F$ preserves weak equivalences, then by the universal property of $\Ho_C$ it factors uniquely through $C \to Ho_C$, but in general this is too much to ask.  Derived functors are "approximations" to $F$ defined on $\Ho_C$, but which are _not_ extensions of $F$ along $C\to \Ho_C$ (even up to isomorphism).

Often the term _derived functor_ refers to the particular case where $C = K(A)$ is a [[category of chain complexes]] in an [[abelian category]] $A$ and $Ho_C$ is the [[derived category]] of $A$. For this special case see also [[derived functor on a derived category]].


#Definition#

For $Core(C) \hookrightarrow W \hookrightarrow C$ a [[category with weak equivalences]], then for $F : C \to D$ any functor, the __left derived functor__ $L F$ of $F$ is the _right_ [[Kan extension]] of $F$ along the projection $p : C \to Ho_C$ to the [[homotopy category]]

$$
 \array{
   C &&\stackrel{F}{\to}&& D
   \\
   \downarrow^p &\Downarrow& \nearrow_{L F}
   \\
   Ho_C
 }
$$

(if it exists).  Dually, the __right derived functor__ $R F$ of $F$ is its _left_ Kan extension along $p$.  Note the reversal of handedness; this is unfortunate but unavoidable.

More generally, if $D$ is itself a category with weak equivalences, then by derived functors of $F$ we often mean derived functors of the composite

$$ C \stackrel{F}{\to} D \to Ho_D $$

+--{: .query}
[[Mike Shulman|Mike]]: I personally hold the opinion that it is better to _define_ a derived functor to be the result of applying $F$ to a fibrant and/or cofibrant replacement of some sort.  I have come to view the fact that sometimes (when a fibrant _or_ cofibrant replacement alone suffices) this happens to be a left or right Kan extension as merely an accident, which is of little practical or conceptual use.  I think this is borne out by the fact that these Kan extension are not "pointwise," that they are basically the _only_  non-pointwise Kan extensions that I have seen arise anywhere in mathematics, and that many of the nice properties of Kan extensions apply only to pointwise ones (in fact, Kelly _defines_ Kan extension to refer only to pointwise ones).  But I would be very interested to hear alternate points of view.

[[Zoran Skoda]]: This is very interesting; maybe it suggests that one needs to choose sort of factorization system or something, so that still thing has some universal property: among functors of special kind with respect to the factorization system of a sort. I would like to hear your examples and insight in more detail. Surely in homological 
algebra osmetimes one does not have sufficiently many projective or injectives so there is an appeal in something universal. Most interestingly, satelites make sense sometimes when derived functors don't but still satelites in very general (nonabelian) context are themselves still sort of Kan extensions. I do not understand why total derived functor would have kind of universality as one step in forming it has. 

[[Tim Porter|Tim]]: The 'homotopy Kan extensions' are weighted Kan extensions and can handle quite a few of the 'derived functor' cases.  As they are enriched versions they seem to generalise the pointwise case, yet manage to do more. Perhaps that neaeds airing as an idea.  I suspect it does not handle all the derived functors we might want.
=--


#Remarks#

* By the universal property of $Ho_C$, functors $Ho_C \to D$ are equivalent to functors $C\to D$ which take weak equivalences to isomorphisms.  If $F$ itself takes weak equivalences to isomorphisms, then its left and right derived functors are both (isomorphic to) its unique extension along $p$.  In general, however, $L F$ and $R F$ are not extensions of $F$ even up to isomorphism.


* The Kan extensions involved here are _not_ "pointwise" ones, meaning that they are not computed by limits and colimits objectwise.  This means that they lack many of the good properties of ordinary Kan extensions.  

* In practice, derived functors are usually computed using fibrant and cofibrant replacements (see the entries on [[homotopy theory]] and [[model category]]) or, more generally, [[deformation retract|deformation retracts]].

* The connection to the 
more elementary notion of [[derived functor on a derived category]] in [[homological algebra]] that is as follows. A functor $F:A \to B$ between [[abelian category|abelian categories]] induces a functor $Ch(F):Ch(A) \to Ch(B)$ between [[category of chain complexes|categories of chain complexes]], each of which can be equipped with the class of [[quasi-isomorphism|quasi-isomorphisms]] as weak equivalences.  We obtain the usual derived functors of $F$ by taking the derived functor of $Ch(F)$ in the above sense, evaluating it at an object of $A$ regarded as a chain complex concentrated in degree zero, and then taking the [[homology]] of the resulting chain complex in $B$.


#Examples#

* The (total) derived functor of the [[limit]] functor is the [[homotopy limit]].  The functors $lim^{(i)}$ often called the derived functors of Lim are then given by the (co)homology of that 'total' form.  