[[!redirects étalé space]]

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Topology
+--{: .hide}
[[!include topology - contents]]
=--
#### étale morphisms
+--{: .hide}
[[!include etale morphisms - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Definition

Let [[Top]] be a category of [[topological space]]s and $B$ an object in $Top$ (the 'base' space). The [[over category|slice category]] $Top/B$ is called the category of (topological) spaces over $B$ (or sometimes simply bundles).

An __étale space__ (or _[[étale map]]_, sometimes *étalé space*) over $B$ is an object $p:E\to B$ in $Top/B$ such that $p$ is a [[local homeomorphism]]: that is, for every $e\in E$, there is an open set $U \ni e$ such that the [[image]] $p(U)$ is open in $B$ and the restriction of $p$ to $U$ is a [[homeomorphism]] $p|_U: U \to p(U)$. 

The set $E_x = p^{-1}(x)$ where $x\in B$ is called the __[[stalk]]__ of $p$ over $x$.  

The underlying set of the _total space_ $E$ is the union of its stalks (notice that we do not say fiber!).  $p$ is sometimes refered to as the _projection_.

## Definition for arbitrary toposes

The following is adapted from a [MathOverflow answer](https://mathoverflow.net/questions/78681/etal%c3%a9-space-construction-for-presheaves-on-a-grothendieck-site/111293#111293) by [[David Carchedi]]:

> As long as $C$ has a [[small set]] of topological generators (i.e., as long as $Sh(C,J)$ isn't too large to be a [[topos]]), there always exists a certain version of an étale space: If $F$ is a [[sheaf]] on $(C,J)$, the [[slice topos]] $Sh(C,J)/F$ has a canonical étale projection  $\pi_F:Sh(C,J)/F \to Sh(C,J)$. This map is a [[local homeomorphism of topoi]]. This topos with this local homeomorphism is the étale space of $F$. Indeed, we may make this construction for each object $c \in C$, call it $U(c) \coloneqq Sh(C,J)/y(c)$, where $y(c)$ is the (possibly sheafified) [[Yoneda embedding|Yoneda embedded]] object. Then, "[[sections]] of $\pi_F$ over $U(c) \to Sh(C,J)$" are in [[bijection]] with [[elements]] of $F(c)$. If the Grothendieck [[site]] $(C,J)$ happened to be the [[canonical site]] of a [[topological space]], then each [[slice]] $Sh(C,J)/F$ is equivalent to [[category of sheaves|sheaves]] on the étale space of that [[sheaf]], and the projection corresponds to the usual one. In particular, $U(c) \to Sh(C,J)$ corresponds to the inclusion of an [[open subset]]. So, this is reduces to the usual construction for spaces. Another example is, if $(C,J)$ were the [[small étale site]] of some [[scheme]] $S$, then each $Sh(C,J)/F$ is the small étale site of some algebraic space (with no separation conditions) étale over $S$, with $\pi_F$ corresponding to the étale map from this algebraic space to $S$.

## Properties

### Relation to sheaves
 {#RelationToSheaves}

Let $p:E\to B$ be in $Top/B$.  The (local) __[[sections]]__ of $p$ over an open set $U\subseteq B$ are the [[continuous maps]] $s:U\to E$ such that $p\circ s = \mathrm{id}_U$. It is an elementary but central fact that for an &#233;tale map $p$, _the images of local sections form a base for the topology_ of the total space $E$. The topology of $E$ is then typically non-[[Hausdorff space|Hausdorff]].

The set of sections of $p$ over $U$ is denoted by $\Gamma_U p = (\Gamma p)(U) = \Gamma_U E = (\Gamma E)(U)$ and may be shown to extend to a [[functor]] $\Gamma : Top/B\to PShv_B$ where $PShv_B$ is the [[category of presheaves]] over $B$.  The functor $\Gamma$ has a [[left adjoint]] $L : PShv_B\to Top/B$, whose [[essential image]] is the [[full subcategory]] $Et/B$ of étale spaces over $B$.  The [[essential image]] of the functor $\Gamma$ is the [[category of sheaves]] $Shv_B$  over $B$, and this [[adjunction]] restricts to an [[equivalence of categories]] between $Et/B$ and $Shv_B$ (that is, it is an [[idempotent adjunction]]).

If $P:Open(B)^{op}\to Set$ is a [[sheaf]], then one sometimes calls the total space $E(P)$ of the étale space $L(P) = (E(P)\to B)$ the __space of the sheaf__ $P$, having in mind the adjoint equivalence above.  (This is also called the __sheaf space__ or the __display space__ (alias __étale space__, or in French: __espace étalé__); compare also a [[display morphism]] of [[contexts]].)  The associated sheaf functor $a:PShv_B\to Shv_B\hookrightarrow PShv_B$ decomposes as $a = \Gamma\circ L$, and $a$ may be considered as an endofunctor part of an [[idempotent monad]] in $PShv_B$ whose corresponding [[reflective subcategory]] is $Shv_B$.

(e.g. [MacLane-Moerdijk, section II.5, II.6](#MacLaneMoerdijk))

### Relation to covering spaces

Every [[covering space]] (even in the more general sense not requiring any connectedness axiom) is étale but not vice versa: 

* for a covering space the [[inverse image]] of some [[open subset]] in the base $B$ needs to be, by the definition, a [[disjoint union]] of homeomorphic open sets in $E$; however the 'size' of the [[open neighborhoods]] over various $e$ in the same [[stalk]] required in the definition of étale space may differ, hence the intersection of their projections does not need to be an open set, if there are infinitely many points in the stalk.

* even if the the stalks of the étale space are finite, it need not be locally trivial. For instance the [[disjoint union]] $\coprod_i U_i$ of a collection of [[open subsets]] of a topological space $X$ with the obvious projection $(\coprod_i U_i) \to X$ is étale, but does not have a typical fiber: the fiber over a given point has [[cardinality]] the number of open sets $U_i$ that contain this particular point.


## Grammar note
{#grammar}

In French, the verb 'étaler' means, roughly, to spread out; '-er' becomes '-é' to make a past participle.  So an 'espace étalé' is a space that has been spread out over $B$.  On the other hand, 'étale' is a (relatively obscure, distantly related) nautical adjective that can be translated as 'calm' or 'slack'.  


To quote from the [Wiktionnaire français](https://fr.wiktionary.org/wiki/%C3%A9tale):

> 'étale' _qualifie la mer qui ne monte ni ne descend &#224; la fin du flot ou du jusant_ 
('flot' = 'flow' and 'jusant' = 'ebb').


There is an interesting stanza from a song of L&#233;o Ferr&#233;:

> Et que les globules figurent

> Une math&#233;matique bleue,

> Sur cette mer jamais &#233;tale

> D'o&#249; me remonte peu &#224; peu

> Cette m&#233;moire des &#233;toiles. 

> &#8212; (L&#233;o Ferr&#233;, La m&#233;moire et la mer)

He also mentions geometry and 'th&#233;or&#232;me' elsewhere in the song.


* [Further reference](https://en.wikipedia.org/wiki/Wikipedia_talk:WikiProject_Mathematics/Archive11#french_spelling)


## Related concepts

* [[étale groupoid]], [[étale infinity-groupoid]]


## References

* {#MacLaneMoerdijk} [[Saunders Mac Lane]], [[Ieke Moerdijk]], sections II.5 and II.6 of _[[Sheaves in Geometry and Logic]]_

For generalizations to étale spaces of stacks in groupoids see

* [[David Carchedi]], _An étalé space construction for stacks_,  Algebr. Geom. Topol. 13 (2013), no. 2, 831–903.

[[!redirects etale space]]
[[!redirects etale spaces]]
[[!redirects étalé space]]
[[!redirects étalé spaces]]
[[!redirects étale space]]
[[!redirects étale spaces]]
[[!redirects etalé space]]
[[!redirects etalé spaces]]
[[!redirects espace étalé]]
[[!redirects espaces étalés]]
[[!redirects espace etale]]
[[!redirects espaces etales]]

[[!redirects sheaf space]]
[[!redirects sheaf spaces]]

[[!redirects display space]]
[[!redirects display spaces]]
