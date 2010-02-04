
#Contents#
* automatic table of contents goes here
{:toc}

## Definition

Let [[Top]] be a category of [[topological space]]s and $B$ an object in $Top$ (the 'base' space). The [[over category|slice category]] $Top/B$ is called the category of (topological) spaces over $B$ (or sometimes simply bundles).

An __&#233;tal&#233; space__ (or _&#233;tale map_) over $B$ is an object $p:E\to B$ in $Top/B$ such that $p$ is a [[local homeomorphism]]: that is, for every $e\in E$, there is an open set $U \ni e$ such that the [[image]] $p_*(U)$ is open in $B$ and the restriction of $p$ to $U$ is a [[homeomorphism]] $p|_U: U \to p(U)$. The set $E_x = p^{-1}(x)$ where $x\in U$ is called the __[[stalk]]__ of $p$ over $x$.  The underlying set of the _total space_ $E$ (from 'espace') is the union of its stalks (notice that we do not say fiber!).  $p$ is sometimes refered to as the _projection_.

Let $p:E\to B$ be in $Top/B$.  The (local) __[[section]]s__ of $p$ over an open set $U\subseteq B$ are the continuous maps $s:U\to E$ such that $p\circ s = \mathrm{id}_U$. It is an elementary but central fact that for an &#233;tale map $p$, _the images of local sections form a base for the topology_ of the total space $E$. The topology of $E$ is then typically non-Hausdorff.

The set of sections of $p$ over $U$ is denoted by $\Gamma_U p = (\Gamma p)(U) = \Gamma_U E = (\Gamma E)(U)$ and may be shown to extend to a functor $\Gamma : Top/B\to PShv_B$ where $PShv_B$ is the category of [[presheaf|presheaves]] over $B$.  The functor $\Gamma$ has a left adjoint $L : PShv_B\to Top/B$, whose [[essential image]] is the [[full subcategory]] $Et/B$ of &#233;tal&#233; spaces over $B$.  The essential image of the functor $\Gamma$ is the category $Shv_B$ of [[sheaf|sheaves]] over $B$, and this adjunction restricts to an [[equivalence of categories]] between $Et/B$ and $Shv_B$ (that is, it is an [[idempotent adjunction]]).

If $P:Open(X)^{op}\to Set$ is a sheaf, then one sometimes calls the total space $E(P)$ of the &#233;tal&#233; space $L(P) = (E(P)\to B)$ the 'space of the sheaf' $P$, having in mind the adjoint equivalence above.  (This is also called the __sheaf space__ or the __display space__; compare also a [[display morphism]] of [[contexts]].)  The associated sheaf functor $a:PShv_B\to Shv_B\hookrightarrow PShv_B$ decomposes as $a = \Gamma\circ L$, and $a$ may be considered as an endofunctor part of an [[idempotent monad]] in $PShv_B$ whose corresponding [[reflective subcategory]] is $Shv_B$.

### Relation to covering spaces

Every [[covering space]] (even in the more general sense not requiring any connectedness axiom) is &#233;tal&#233; but not vice versa: 

* for a covering space the inverse image of some open set in the base $B$ needs to be, by the definition, a disjoint union of homeomorphic open sets in $E$; however the 'size' of the neighborhoods over various $e$ in the same stalk required in the definition of &#233;tal&#233; space may differ, hence the intersection of their projections does not need to be an open set, if there are infinitely many points in the stalk.

* even if the the stalks of the etale space are finite, it need not be locally trivial. For instance the disjoint union $\coprod_i Ui$ of a collecton of open subsets of a space $X$ with the obvious projection $(\coprod_i U_i) \to X$ is etale, but does not have a typical fiber: the fiber over a given point has cardinality the number of open sets $U_i$ that contain this particular point.


## Grammar note

In French, the verb '&#233;taler' means, roughly, to spread out; '-er' becomes '-&#233;' to make a past participle.  So an 'espace &#233;tal&#233;' is a space that has been spread out over $B$.  On the other hand, '&#233;tale' is a (relatively obscure, distantly related) nautical adjective that can be translated as 'calm' or 'slack'.  So a 'fonction &#233;tale' is a slack function, one which is kind of a homeomorphism, but perhaps only locally. 


To quote from the [Wiktionnaire fran&#231;aise](http://fr.wiktionary.org/wiki/%C3%A9tale):
>'&#233;tale' _qualifie la mer qui ne monte ni ne descend &#224; la fin du flot ou du jusant_ 
('flot' = 'flow' and 'jusant' = 'ebb').


There is an interesting stanza from a song of L&#233;o Ferr&#233;:

* Et que les globules figurent
* Une math&#233;matique bleue,
* Sur cette mer jamais &#233;tale
* D'o&#249; me remonte peu &#224; peu
* Cette m&#233;moire des &#233;toiles. &#8212; (L&#233;o Ferr&#233;, La m&#233;moire et la mer)

He also mentions geometry and 'th&#233;or&#232;me' elsewhere in the song.


* [Further reference](http://secure.wikimedia.org/wikipedia/en/wiki/Wikipedia_talk:WikiProject_Mathematics/Archive11#french_spelling)


[[!redirects etale spaces]]
[[!redirects étalé space]]
[[!redirects étale space]]
[[!redirects espace étalé]]
[[!redirects sheaf space]]
[[!redirects display space]]