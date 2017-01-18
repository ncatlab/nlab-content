
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Topology
+-- {: .hide}
[[!include topology - contents]]
=--
=--
=--

# Contents
* table of contents goes here
{: toc}

## Idea

A [[topological space]] (or more generally, a [[convergence space]]) is _Hausdorff_ if [[convergence]] is unique.  The concept can also be defined for [[locales]] (see Definition \ref{proper} below) and [[categorification|categorified]] (see [Beyond topological spaces](#BeyondTopologicalSpaces) below).  A Hausdorff space is often called $T_2$, since this condition came second in the original list of four [[separation axioms]] (there are more now) satisfied by [[metric spaces]].

Hausdorff spaces are a kind of [[nice topological space]]; they do not form a particularly [[nice category of spaces]] themselves, but many such nice categories consist of only Hausdorff spaces.  In fact, [[Felix Hausdorff]]\'s original definition of 'topological space' actually required the space to be Hausdorff, hence the name.  Certainly [[homotopy theory]] (up to [[weak homotopy equivalence]]) needs only Hausdorff spaces.  It is also common in analysis to assume that all spaces encountered are Hausdorff; if necessary, this can be arranged since every space has a Hausdorff quotient (in fact, the Hausdorff spaces form a [[reflective subcategory]] of [[Top]]), although usually an easier method is available than this sledgehammer.


## Definitions
 {#Definitions}

There are many equivalent ways of characterizing a space $S$ as __Hausdorff__. The traditional definition is this:

+-- {: .num_defn #classical}
###### Definition

Given points $x$ and $y$ of $S$, if $x \neq y$, then there exist [[open neighbourhoods]] $U$ of $x$ and $V$ of $y$ in $S$ that are [[disjoint subsets|disjoint]]: such that their [[intersection]] $U \cap V$ is the [[empty set]] (or explicitly, such that $x' \ne y'$ whenever $x' \in U$ and $y' \in V$).
=--

That is, any two distinct points can be _separated_ by open neighbourhoods, and it is simply a mundane way of saying that $\ne$ is [[open subset|open]] in the [[product topology]] on $S \times S$.


Here is a classically equivalent definition that is more suitable for [[constructive mathematics]]:

+-- {: .num_defn #constructive}
###### Definition

Given points $x$ and $y$ of $S$, if every neighbourhood $U$ of $x$ in $S$ meets every neighbourhood $V$ of $y$ in $S$ (which means that $U \cap V$ is [[inhabited set|inhabited]]), then $x = y$.
=--

This is the mundane way of saying that $=$ is [[closed subset|closed]] in $S \times S$.

Another way of saying this, which makes sense also for [[locales]], is the following:

+-- {: .num_defn #proper}
###### Definition

The [[diagonal]] embedding $S \to S \times S$ is a [[proper map]] (or equivalently a [[closed map]], since any closed subspace inclusion is proper).
=--

This way of stating the definition generalizes to [[topos theory]] and thus to many other contexts; but it is not always a faithful generalization of the classical notion for topological spaces.  See _[Beyond topological spaces](#BeyondTopologicalSpaces)_ below for more.


Here is an equivalent definition (constructively equivalent to Definition \ref{constructive}) that makes sense for arbitrary [[convergence spaces]]:

+-- {: .num_defn #convergence}
###### Definition

Given a [[net]] (or equivalently, a proper [[filter]]) in $S$, if it converges to both $x$ and $y$, then $x = y$.
=--

That is, convergence in a Hausdorff space is unique.


## Properties

The topology on a [[compact space|compact]] Hausdorff space is given precisely by the (existent because compact, unique because Hausdorff) limit of each [[ultrafilter]] on the space.  Accordingly, compact Hausdorff topological spaces are (perhaps surprisingly) described by a (large) [[algebraic theory]].  In fact, the category of compact Hausdorff spaces is monadic (over [[Set]]); the [[monad]] in question maps each set to the set ultrafilters on it.  (The results of this paragraph require the [[ultrafilter theorem]], a weak form of the [[axiom of choice]]; see [[ultrafilter monad]].)

A compact Hausdorff locale (or space) is necessarily [[regular locale|regular]]; a regular locale (or $T_0$ space) is necessarily Hausdorff.  Accordingly, [[locale]] theory usually speaks of 'compact regular' locales instead of 'compact Hausdorff' locales, since the definition of regularity is easier and more natural.  Then a version of the previous paragraph works for compact regular locales *without* the ultrafilter theorem, and indeed [[constructive mathematics|constructively]] over any [[topos]].


+-- {: .num_prop }
###### Proposition

[[a CW-complex is a Hausdorff space]].

=--


+-- {: .num_prop }
###### Proposition

[[compact subspaces of Hausdorff spaces are closed]].

=--



## Related notions

Arguably, the desire to make spaces Hausdorff ($T_2$) in analysis is really a desire to make them $T_0$; nearly every space that arises in analysis is at least [[regular space|regular]], and a regular $T_0$ space must be Hausdorff.  Forcing a space to be $T_0$ is like forcing a [[category]] to be [[skeletal category|skeletal]]; indeed, forcing a [[preorder]] to be a [[partial order]] is a special case of both (see [[specialisation topology]] for how).  It may be nice to assume, when working with a particular space, that it is $T_0$ but not to assume, when working with a particular underlying set, that every topology on it is $T_0$.

Whatever one thinks of that, there is a non-$T_0$ version of Hausdorff space, an __$R_1$ space__.  (The symbol here comes from being a weak version of a **r**egular space; in general a $T_i$ space is precisely both $R_{i-1}$ and $T_0$).  This is also called a __preregular space__ (in _[[HAF]]_) and a __reciprocal space__ (in convergence theory).

+-- {: .un_defn}
###### Definition (of $R_1$)
Given points $a$ and $b$, if every neighbourhood of $a$ meets every neighbourhood of $b$, then every neighbourhood of $a$ is a neighbourhood of $b$.  Equivalently, if any net (or proper filter) converges to both $a$ and $b$, then every net (or filter) that converges to $a$ also converges to $b$.
=--

There is also a notion of __sequentially Hausdorff space__:
+-- {: .un_defn}
###### Definition (of sequentially Hausdorff)
Whenever a [[sequence]] converges to both $x$ and $y$, then $x = y$.
=--
Some forms of [[predicative mathematics]] find this concept more useful.  Hausdorffness implies sequential Hausdorffness, but the converse is false even for [[sequential space]]s (although it is true for [[first-countable space]]s).

The reader can now easily define a _sequentially $R_1$ space_.


## Beyond topological spaces
 {#BeyondTopologicalSpaces}

The only reasonable definition for a [[locale]] $X$ to be **Hausdorff** is that its diagonal $X\to X\times X$ is a closed (and hence proper) inclusion.  However, if $X$ is a [[sober space]] regarded as a locale, this might not coincide with the condition for $X$ to be Hausdorff as a space, since the product $X\times X$ in the category of locales might not coincide with the product in the category of spaces.  But it does coincide if $X$ is a [[locally compact locale]], so in that case the two notions of Hausdorff are the same.

This notion of a _Hausdorff locale_ is a special case of that of _[[Hausdorff topos]]_ in [[topos theory]]. This also includes notions such as a _[[separated scheme]]_ etc.  The corresponding relative notion (over an arbitrary [[base topos]]) is that of _[[separated geometric morphism]]_. For schemes see _[[separated morphism of schemes]]_.


## In constructive mathematics

In [[constructive mathematics]], the Hausdorff notion multifurcates further, due to the variety of possible meanings of [[closed subspace]].  As a simple example, consider a [[discrete space]] $X$ regarded as a locale.  Since it is locally compact, the locale product $X\times X$ coincides with the space product (a theorem that is valid constructively); but nevertheless we have:

1. The diagonal $X\to X\times X$ always has an open complement.
2. Definition \ref{constructive} above always holds, since $\{x\}$ and $\{y\}$ are neighborhoods of $x$ and $y$, and if they intersect then $x=y$.
3. The diagonal $X\to X\times X$ is the complement of an open subset if and only if equality in $X$ is stable under [[double negation]], in other words if $X$ admits a tight [[inequality relation]].
4. The locale diagonal $\Delta:X\to X\times X$ is a closed sublocale if and only if $X$ has [[decidable equality]].  For closedness of $\Delta$ means that $\Delta_\ast(U\cup \Delta^\ast(V)) \subseteq \Delta_\ast(U) \cup V$ for any $U\in O(X)$ and $V\in O(X\times X)$, where $x\in \Delta^\ast(V)$ means $(x,x)\in V$, while $(x,y)\in \Delta_\ast(U)$ means $(x=y)\to (x\in U)$.  Now let $U = \emptyset$ and $V = \{ (x,x) \mid x\in X \}$.  Then $(x,y) \in \Delta_\ast(U\cup \Delta^\ast(V))$ means $(x=y) \to (\bot \vee (x=x))$, which is a tautology; while $(x,y) \in \Delta_\ast(U) \cup V$ means $((x=y)\to \bot) \vee (x=y)$, i.e. $\neg(x=y) \vee (x=y)$.

In particular, the statement "all discrete locales are Hausdorff (as locales)" is equivalent to [[excluded middle]].

In terms of 'weakly closed' and 'strongly closed' subsets, as described at [[closed subset]], Definition \ref{constructive} says that $=$ is *weakly* closed in $X \times X$.  If we instead say that $=$ is *strongly* closed, then this means that there is a [[tight inequality]] $\ne$ (the [[symmetric relation|symmetrization]] of the [[exterior]] of $=$) relative to which Definition \ref{classical} holds.  (We use $\ne$ twice in that definition: in the hypothesis that $x \ne y$ and in the conclusion that $x' \ne y'$.)  This corresponds to (3) above for a discrete space.


## Related concepts

* [[locally Hausdorff topological space]]


## References

Comments on the relation to [[topos theory]] are for instance in

* S. Niefield, _A note on the locally Hausdorff property_, Cahiers TGDC (1983) ([numdam](http://www.numdam.org/item?id=CTGDC_1983__24_1_87_0))


[[!redirects Hausdorff]]
[[!redirects Hausdorff space]]
[[!redirects Hausdorff spaces]]
[[!redirects Hausdorff topological space]]
[[!redirects Hausdorff topological spaces]]
[[!redirects Hausdorff convergence space]]
[[!redirects Hausdorff convergence spaces]]
[[!redirects Hausdorff locale]]
[[!redirects Hausdorff locales]]

[[!redirects sequentially Hausdorff space]]
[[!redirects sequentially Hausdorff spaces]]

[[!redirects R1 space]]
[[!redirects R1 spaces]]
[[!redirects preregular space]]
[[!redirects preregular spaces]]
[[!redirects reciprocal space]]
[[!redirects reciprocal spaces]]
