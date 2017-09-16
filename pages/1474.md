[[!redirects Hausdorff spaces]]
[[!redirects sequentially Hausdorff space]]
[[!redirects sequentially Hausdorff spaces]]

A [[topological space]] (or more generally, a [[convergence space]]) is _Hausdorff_ if convergence is unique.  The concept can also be defined for [[locale]]s, but it is not as natural and a bit complicated.  A Hausdorff space is often called $T_2$, since this condition came second in the original list of four separation axioms (there are more now) satisfied by [[metric space]]s.

Hausdorff spaces are a kind of [[nice topological space]]; they do not form a particularly [[nice category of spaces]] themselves, but many such nice categories consist of only Hausdorff spaces.  In fact, Felix Hausdorff\'s original definition of 'topological space' actually required the space to be Hausdorff, hence the name.  Certainly [[homotopy theory]] needs only Hausdorff spaces.  It is also common in analysis to assume that all spaces encountered are Hausdorff; if necessary, this can be arranged since every space has a Hausdorff quotient (in fact, the Hausdorff spaces form a [[reflective subcategory]] of [[Top]]), although usually an easier method is available than this sledgehammer.

## Definitions

The traditional definition is this:  A topological space is __Hausdorff__ if any two distinct points can be separated by neighbourhoods.  That is, given points $x$ and $y$, if $x \neq y$, then there exist neighbourhoods $U$ of $x$ and $V$ of $y$ such that $U \cap V$ is the [[empty set]].

Here is a classically equivalent definition that is more suitable for [[constructive mathematics]]:  Given points $x$ and $y$, if every neighbourhood $U$ of $x$ meets every neighbourhood $V$ of $y$ (which means that $U \cap V$ is [[inhabited set|inhabited]]), then $x = y$.

Here is an equivalent definition that makes sense for arbitrary [[convergence space]]s:  Given a [[net]] (or equivalently, a proper [[filter]]), if it converges to both $x$ and $y$, then $x = y$.  That is, convergence in a Hausdorff space is unique.

Here is a definition for [[locale]]s, equivalent to the above for spatial locales:  ...  (Get this from Johnstone.)

There is also a notion of _sequential_ Hausdorffness:  A space is __sequentially Hausdorff__ if, whenever a [[sequence]] converges to both $x$ and $y$, then $x = y$.  Some forms of [[predicative mathematics]] find this concept more useful.  Hausdorffness implies sequential Hausdorffness, but the converse is false even for [[sequential space]]s (although it is true for [[first countable space]]s).

## Properties

The topology on a [[compact space|compact]] Hausdorff space is given precisely by the (existent because compact, unique because Hausdorff) limit of each [[ultrafilter]] on the space.  Accordingly, compact Hausdorff topological spaces are (perhaps surprisingly) described by a (large) [[algebraic theory]].  In fact, the category of compact Hausdorff spaces is monadic (over [[Set]]); the [[monad]] in question maps each set to the set ultrafilters on it.  (The results of this paragraph require the [[ultrafilter theorem]], a weak form of the [[axiom of choice]].)

A compact Hausdorff locale is necessarily regular; a regular locale is necessarily Hausdorff.  Accordingly, [[locale]] theory usually speaks of 'compact regular' locales instead of 'compact Hausdorff' locales, since the definition of regularity is easier and more natural.  Then a version of the previous paragraph works for compact regular locales *without* the ultrafilter theorem, and indeed [[constructive mathematics|constructively]] over any [[topos]].
