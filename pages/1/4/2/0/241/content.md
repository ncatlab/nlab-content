
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Topos Theory
+--{: .hide}
[[!include topos theory - contents]]
=--
=--
=--

#Contents#
* automatic table of contents goes here
{:toc}

##Definition##

Classically, we have:

+-- {: .un_defn}

A __Grothendieck topos__ $\mathcal{T}$ is a category that admits a [[geometric embedding]]

$$
  \mathcal{T} \stackrel{\stackrel{lex}{\leftarrow}}{\hookrightarrow}
  PSh(C)
$$

in a [[presheaf]] category, i.e., a full and faithful functor that has a left exact left adjoint. 

This is equivalently the [[category of sheaves]] ([[Set]]-valued [[presheaves]] satisfying the sheaf condition) over a [[small category|small]] [[site]].

=--

Since smallness can be relative, we also have:

+-- {: .un_defn}
For a given fixed [[ETCS|category of sets]] $S$, a __Grothendieck topos__ over $S$ is a [[category of sheaves]] ($S$-valued [[presheaves]] satisfying the sheaf condition) over a [[site]] which is [[small category|small]] relative to $S$, that is a site [[internal category|internal]] to $S$.
=--

Note that a Grothendieck topos is a [[topos]] because (or if) $S$ is.

The [[site]] is not considered part of the structure; different sites may give rise to [[equivalence of categories|equivalent]] category of sheaves.

By the general theory of [[geometric morphisms]], every Grothendieck topos sits inside a category of [[presheaf|presheaves]] by a [[geometric embedding]] $Sh(S) \hookrightarrow PSh(S)$. 

* This may be taken as an alternative definition of [[sheaf]]: since [[Lawvere-Tierney topology|Lawvere-Tierney topologies]] are bijectively given by [[geometric embeddings]],  instead of explicitly defining a sheaf as a presheaf satisfying [[descent]], one may define categories of sheaves as geometric embeddings into presheaf categories. 

* For details on the relation between the two perspectives see [[geometric embedding]].

* This perspective is useful for defining the [[vertical categorification]] of sheaves: [[stacks]] and [[∞-stacks]]: the higher categories of these may be defined as geometric embeddings into higher categories of presheaves. This has been worked out in detail for [[(∞,1)-categories]]. See [[(∞,1)-category of (∞,1)-sheaves]].

* Sometimes it is useful to distinguish between [[petit topos]] and [[gros topos]].


## Giraud\'s axioms

Giraud characterized Grothendieck toposes as categories satisfying certain exactness and small [[complete category|completeness]] properties (where "small" is again relative to the given category of sets $S$). The exactness properties are elementary (not depending on $S$), and are satisfied in any elementary [[topos]], or even a [[pretopos]].

Giraud\'s theorem characterises a Grothendieck topos as follows:

1. a [[locally small category]] with a small [[generating set]],
2. with all finite [[limits]],
3. with all small [[coproducts]], which are [[disjoint coproduct|disjoint]], and [[pullback stability|pullback-stable]],
4. where all [[congruences]] have effective [[quotient objects]], which are also pullback-stable.

These conditions are equivalent to

* a locally small [[infinitary pretopos]] with a small generating set.

See the [[Elephant]], theorem C.2.2.8.  See also [Wikipedia](https://secure.wikimedia.org/wikipedia/en/wiki/Topos#Giraud.27s_axioms).

Sometimes (3,4) are combined and strengthened to the statement that the category has all small [[colimits]], which are effective and pullback-stable.  However, this is a mistake for two reasons: it is a significantly stronger axiomatisation (since without the small generating set, not every infinitary pretopos has this property), and it is not valid in predicative mathematics (while the definition given above is).


## Generalizations

The notion of Grothendieck topos and its characterization from Giraud-type properties can be generalized from the context of categories to that of [[(∞,1)-categories]], where it yields the notion of [[(∞,1)-topos]].


## In weak foundations

We have two definitions of a Grothendieck topos:

*  the category of sheaves on some small site,
*  a category that satisfies Giraud\'s axioms.

The theorem that these are equivalent can be proved in quite weak foundations, whether [[finitist mathematics|finitist]], [[predicative mathematics|predicative]], or [[constructive mathematics|constructive]] (or all three at once).  Some hard-nosed predicativists (and even hard-nosed ZFC fundamentalists) may object to the language (on the ground that large things don\'t really exist), but they should accept the theorems when suitably phrased.

In predicative mathematics, however, we cannot prove that every Grothendieck topos is in fact a [[topos]]!  In fact, it is immediate that [[the category of sets]] is a Grothendieck topos, but $Set$ is an elementary topos if and only if [[power sets]] are small, which is precisely what predicativists doubt.  One can use the term __Grothendieck pretopos__ to avoid implying that we have an elementary topos.  On the other hand, since Grothendeick toposes came first, perhaps it is the definition of 'elementary topos' that is too strong.

Similarly, in finitist mathematics, we cannot prove that every Grothendieck topos has a [[natural numbers object]]; while in weakly predicative constructive mathematics, we cannot prove that every Grothendieck topos is [[cartesian closed category|cartesian closed]].  In each case, once a property is accepted of $Set$ (the [[axiom of infinity]] and small [[function sets]], in these examples), it can be proved for all Grothendieck toposes.

Constructivism as such is irrelevant; even in [[classical mathematics]], most Grothendieck toposes are not [[boolean topos|boolean]].  However, for an analogous result, try the theorem that the [[category of presheaves]] on a [[groupoid]] is boolean.

The theorem that every Grothendieck topos is [[cocomplete category|cocomplete]] is a subtle point; it fails only in finitist predicative mathematics.


## References

A quick introduction of the basic facts of sheaf-topos theory is chapter I, "Background in topos theory" in 

* [[Ieke Moerdijk]], _Classifying Spaces and Classifying Topoi_ Lecture Notes in Mathematics 1616, Springer (1995)


A standard textbook on this case is

* [[Saunders MacLane]], [[Ieke Moerdijk]], _[[Sheaves in Geometry and Logic]]_

Grothendieck topoi appear around section III,4 there.
A proof of Giraud's theorem is in appendix A.


The proof of Giraud's theorem for [[(∞,1)-topoi]] is section 6.1.5 of

* [[Jacob Lurie]], _[[Higher Topos Theory]]_


[[!redirects Grothendieck topos]]
[[!redirects Grothendieck toposes]]
[[!redirects Grothendieck topoi]]

[[!redirects Giraud axiom]]
[[!redirects Giraud axioms]]
[[!redirects Giraud's axiom]]
[[!redirects Giraud's axioms]]
[[!redirects Giraud's axiom]]
[[!redirects Giraud's axioms]]

[[!redirects Giraud theorem]]
[[!redirects Giraud's theorem]]
[[!redirects Giraud's theorem]]

[[!redirects sheaf topos]]
[[!redirects sheaf toposes]]
[[!redirects sheaf topoi]]
