
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Topos Theory
+-- {: .hide}
[[!include topos theory - contents]]
=--
=--
=--

# Contents
* table of contens
{: toc}

## Idea

Most [[geometric morphisms]] between [[toposes]] are [[bounded geometric morphism|bounded]], and so most toposes can be considered as either a [[base topos]] - the universe of discourse - such as [[Set]], or as a topos of [[internal sheaves]] over another topos (for example any [[Grothendieck topos]]).

While there are lots of examples of toposes which aren't Grothendieck toposes, that is, bounded toposes over $Set$, for example the topos [[FinSet]] of finite sets, or [[realisability toposes]], this is due to the fact they _do not admit_ a geometric morphism to $Set$. Toposes of this form usually can be considered as a base topos/universe of discourse for non-standard versions of reasoning, for example [[finitism]] can be seen as taking the topos $FinSet$ as base topos.

An **unbounded topos** is a non-Grothendieck topos which _does_ admit a geometric morphism to $Set$ (or some other specified base topos), but which isn't equivalent to the category of sheaves on some small [[site]].


## Definition

A topos $\mathcal{E}$ equipped with a geometric morphism $p\colon \mathcal{E} \to Set$ is **unbounded** if $p$ is not bounded. Equivalently, $\mathcal{E}$ (equipped with $p$) is not equivalent to the category of [[sheaves]] on some small site (equipped with the usual geometric morphism to $Set$). 

This means that for any set $\{A_i\}_{i\in I}$ of objects of $\mathcal{E}$, which would aspire to be a [[separator|separating family]] for $\mathcal{E}$, there is a pair of morphisms $f,g\colon X \to Y$ of $\mathcal{E}$ such that for all $i\in I$, and all $t\colon A_i \to X$, we have $f\circ t = g\circ t$, but $f\neq g$.

More generally, we could work over a given base topos $\mathcal{S}$, and then an $\mathcal{S}$-topos $p\colon \mathcal{E} \to \mathcal{S}$ is unbounded if $p$ is not a bounded geometric morphism or equivalently it is not equivalent to the category of sheaves on an [[internal site]] in $\mathcal{S}$.


## Examples

There are relatively few examples of unbounded toposes.

* Given a non-[[locally small category|locally small]] [[groupoid]] $G$ with only a [[set]] of isomorphism classes of objects, the functor category $Cat(G,Set) =: GSet$ is a topos. It has a geometric morphism to $Set$, namely the global sections functor $\Gamma(X) = GSet(1,X)$, which is unbounded. $GSet$ is moreover [[cocomplete category|cocomplete]], [[Boolean topos|Boolean]] and even locally small.

* If $K$ is a topological group, the category $Unif(K)$ of sets with a [[uniformly continuous]] $K$-[[action]] is a $Set$-topos. In the case that $K$ has no smallest open subgroup, then $Unif(K)$ is still Boolean and locally small, but is not cocomplete (it fails to have infinite coproducts), and so not a Grothendieck topos.

* The [[topos of algebras over a monad|topos of coalgebras]] of a pullback-preserving [[comonad]] $M$ on a Grothendieck topos whose functor part is not [[accessible functor|accessible]] is a cocomplete topos $MCoalg$ over $Set$ which is not [[locally presentable category|locally presentable]] hence not a Grothendieck topos.

  * As a particular example, one can take a [[exact functor|left exact]] [[endofunctor]] $F$ on $Set$ and form the corresponding comonad $(X,Y) \mapsto (X,Y\times F(X))$ on $Set\times Set$ and the topos of coalgebras for this (which is equivalent to the [[Artin gluing]] $Gl(F)$ of $F$). In this case however it is not clear that there exist such endofunctors without assuming the existence of [[large cardinals]] (for instance the existence of a [[proper class]] of [[measurable cardinals]] is sufficient to give such an endofunctor).

    ([[David Roberts|DR]]: I think this result has since been improved, see the paper J. Adamek, V. Koubek and V. Trnkova, "How large are left exact functors?" in [TAC](http://www.tac.mta.ca/tac/volumes/8/n13/8-13abs.html). I will have to sort out whether what they are saying applies)

* Any topos that is not locally small, relative to some fixed topos $set$ of sets, when such a setting is properly defined, is not bounded over $set$.

* More coming soon!


## Related topics

* [[internal sheaves]]
* [[internal site]]
* [[bounded geometric morphism]]


## References

The unbounded toposes $GSet$, $Unif(K)$ and $MCoalg$ are mentioned in B3.1.4 of

* [[Peter Johnstone]], [[Sketches of an Elephant]]

as being (at the time) essentially the only examples of unbounded toposes.


[[!redirects unbounded topos]]
[[!redirects unbounded toposes]]
[[!redirects unbounded topoi]]
