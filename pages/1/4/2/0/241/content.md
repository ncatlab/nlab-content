
#Contents#
* automatic table of contents goes here
{:toc}

##Definition##

For a given fixed [[ETCS|category of sets]] $S$, a __Grothendieck [[topos]]__ over $S$ is a [[category of sheaves]] over a [[site]] which is [[small category|small]] relative to $S$, that is a site [[internal category|internal]] to $S$. 

### Remarks ###

* The [[site]] is not considered part of the structure; different sites may give rise to [[equivalence of categories|equivalent]] category of sheaves.

* By the general theory of [[geometric morphisms]], every Grothendieck topos sits inside a category of [[presheaf|presheaves]] by a [[geometric embedding]] $Sh(S) \hookrightarrow PSh(S)$. 

  * This may be taken as an alternative definition of [[sheaf]]: since [[Lawvere-Tierney topology|Lawvere-Tierney topologies]] are bijectively given by [[geometric embeddings]],  instead of explicitly defining a sheaf as a presheaf satisfying [[descent]], one may define categories of sheaves as geometric embeddings into presheaf categories. 

  * For details on the relation between the two perspectives see [[geometric embedding]].

  * This perspective is useful for defining the [[vertical categorification]] of sheaves: [[stacks]] and [[∞-stacks]]: the higher categories of these may be defined as geometric embeddings into higher categories of presheaves. This has been worked out in detail for [[(∞,1)-categories]]. See [[(∞,1)-category of (∞,1)-sheaves]].


  * Sometimes it is useful to distinguish between [[petit topos]] and [[gros topos]].

##Giraud\'s axioms##

Giraud characterized Grothendieck toposes as categories satisfying certain exactness and small [[complete category|completeness]] properties (where "small" is again relative to the given category of sets $S$). The exactness properties are elementary (not depending on $S$), and are satisfied in any elementary [[topos]], or even a [[pretopos]].

Giraud\'s theorem characterises Grothendieck toposes as follows:
* a [[locally small category]] with a small [[generating set]],
* with all finite [[limits]],
* with all small [[coproducts]], which are [[disjoint coproduct|disjoint]], and [[pullback stability|pullback-stable]],
* where all [[congruences]] have effective [[quotient objects]], which are also pullback-stable.

These conditions are equivalent to

* a locally small [[pretopos|infinitary pretopos]] with a small generating set.

(See [Wikipedia](https://secure.wikimedia.org/wikipedia/en/wiki/Topos#Giraud.27s_axioms).)

This characterisation may be suitable even when the base category $S$ is only a [[pretopos]], although in that case a Grothendieck 'topos' need not actually be a topos. More generally, a Grothendieck topos will inherit properites from $S$, not only having a [[subobject classifier]], but also (for example) having a [[natural numbers object]]. Thus the concept makes sense even with weak [[foundations]] of mathematics, although it may not have all of the usual properties.

## Generalizations ##

The notion of Grothendieck topos and its characterization from Giraud-type properties can be generalized from the context of categories to that of [[(∞,1)-categories]], where it yields the notion of [[(∞,1)-topos]].


##References##

Grothendieck topoi appear around section IIIm,4 of

* MacLane-Moerdijk, [[Sheaves in Geometry and Logic]]

A proof of Giraud's theorem is in appendix A.

The proof of Giraud's theorem for [[(∞,1)-topoi]] is section 6.1.5 of

* [[Jacob Lurie]], [[Higher Topos Theory]]


[[!redirects Grothendieck topoi]]
[[!redirects Grothendieck toposes]]
[[!redirects Giraud's axioms]]
[[!redirects Giraud axioms]]
[[!redirects Giraud axiom]]