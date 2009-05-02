## Idea ##

A _lax 2-adjunction_ is an [[adjunction]] 'up to adjointness'.  A
1-categorical adjunction is given by a [[natural isomorphism]] of [[hom-set]]s

$$\phi_{A,B} : D(F A,B) \cong C(A,G B)$$

and a strict 2-adjunction is analogous, where $C,D$ are instead [[strict 2-category|strict 2-categories]], $F,G$ are [[strict 2-functor|strict 2-functors]], and $\phi$ is a strictly 2-natural isomorphism of hom-categories.  A __lax 2-adjunction__ is given by a (suitably natural) pair of functors

$$\hat\phi_{A,B} : D(F A,B) \overset{\to}{\leftarrow} C(A,G B) :
\check\phi_{A,B} $$

such that $\check\phi\dashv\hat\phi$.


## Definition ##

Just as the notion of [[adjunction]] makes sense not just in $Cat$ but
in any 2-category, lax 2-adjunctions can be defined in any [[3-category]] when the above is suitably reformulated by using the 2-categorical [[Yoneda lemma]].  So, given 0-cells $C,D$ and 1-cells $F:C\to D$, $G:D\to C$ in any 3-category, we say $F$ is __lax left adjoint__ to $G$ if we have

* 2-cells $\eta:C\Rightarrow G F$ and $\epsilon:F G \Rightarrow D$, and

* instead of strict triangle equalities, 3-cells (called _triangulators_)
  $s,t$

  <center markdown="1">[[lax-adj-mdfs.png:pic]]</center>

  satisfying the _swallowtail identities_:

  <center markdown="1">[[lax-adj-swlwtl-eta.png:pic]]</center>

  and

  <center markdown="1">[[lax-adj-swlwtl-eps.png:pic]]</center>

+--{: .query}
[[Mike Shulman|Mike]]: What 3-category are we intended to work in to obtain an equivalence with the original notion?  I guess this is the question of how strict we require $C,D,F,G$ to be and whether "suitably natural" means "strictly 2-natural" or "pseudo natural."

Since on the nLab, everything is weak by default, it seems that we should probably use the unadorned name for the version where $C$, $D$ are weak 2-categories, $F$ and $G$ are weak 2-functors, and $\hat\phi$ and $\check\phi$ are pseudo natural.

[[Finn Lawler|Finn]]:  For Gray, $C,D,F,G$ are all strict, and $\eta,\epsilon$ are lax.  I'm still trying to understand the connection between the two formulations, so I'm not sure how extra weakness on one side translates to the other.  I should have a better idea soon.

[[Mike Shulman|Mike]]: Unfortunately, there is no 3-category, not as usually understood, in which the 2-cells are lax transformations.  The interchange law for whiskering lax transformations holds only laxly, so at most you have some sort of 'lax 3-category.'  Actually, in the case of $2Cat$, what you have is that $2Cat$ with the lax [[Gray tensor product]] is biclosed and hence enriched over itself, and that sort of enrichment is the relevant 3-category-like structure.  (More grist for [[michaelshulman:n-topos for large n|my mill]] that lax things are important!)
=--

## Sources ##

This idea was introduced in Gray's [[Gray-adjointness-for-2-categories|book]] under the name of _transcendental quasi-adjunction_.

+--{: .query}
[[Mike Shulman|Mike]]: Is there a reference for the name "lax 2-adjunction?"  It looks very similar to the notion of "local adjunction"  in

* Renato Betti and John Power, _On Local Adjointness of Distributive Bicategories_

except that they allow $F$ to be an oplax functor, $G$ a lax functor, $\hat\phi$ an oplax transformation, and $\check\phi$ a lax transformation.

[[Finn Lawler|Finn]]:  I'm roughly following Seely, _Modelling computations: a 2-categorical framework_, from [here](http://www.math.mcgill.ca/~rags/WkAdj/LICS.pdf).  He cites Gray and Kelly--Street, _Review of the elements of 2-categories_ (which I haven't seen yet).

[[Mike Shulman|Mike]]: Kelly-Street don't say anything about lax adjunctions.  I want to make sure we think seriously about what this sort of thing should be called, rather than just following one or another author.  As far as I can tell, it doesn't fit into the general precise meaning of 'lax' (being a type of morphism of algebras for a 2-monad), and there are so many possible variations (as in Gray's book) that it might be nice to have a sensible system of nomenclature that would include them all.  Maybe.  On the other hand, I actually never really took Gray's stuff very seriously because I couldn't think of any examples; maybe I should look more closely at Seely's paper.
=--
