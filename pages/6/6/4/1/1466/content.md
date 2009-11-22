# Uniform spaces
* tic
{: toc}


## Idea

Uniform spaces were invented by Andr&#233; Weil, to capture a general notion of space for which it makes sense to speak of uniformly continuous functions. Such spaces include (pseudo)[[metric spaces]] and [[topological groups]].

A uniform structure or uniformity on a set $X$ consists of a collection of global binary relations $\varepsilon$ which allow us to say when one point $x$ is "$\varepsilon$-close" to another $y$. For a metric space, we have for instance relations expressed by the formula $d(x, y) \lt \epsilon$. For a topological group, we have relations $x y^{-1} \in \varepsilon$, where $\varepsilon$ is a neighborhood of the identity.


## Definitions

A **uniform structure**, or **uniformity**, on a set $X$ consists of a collection of [[binary relations]] $U \subseteq X \times X$ (called __entourages__ or __vicinities__) satisfying some conditions. Write $x \approx_U y$ if $x$ is related to $y$ through $U$; then the conditions are the following:

1. The [[equality relation]] $\Delta = \{(x, x): x \in X\}$ is contained in every entourage. That is,
   $$ \forall U,\; \forall x,\; x \approx_U x .$$
1. For every entourage $U$, there exists an entourage $V$ such that $V^op \subseteq U$, where $V^\op$ is the [[opposite relation]] to $V$. That is,
   $$ \forall U,\; \exists V,\; \forall x, y,\; y \approx_V x \;\Rightarrow\; x \approx_U y .$$
   In light of axiom (6), it follows that $U^op$ itself is an entourage.
1. For every entourage $U$, there exists an entourage $V$ such that $V \circ V \subseteq U$, where $\circ$ is the ordinary operation of [[relation|relational composition]]. That is,
   $$ \forall U,\; \exists V,\; \forall x, y, z,\; x \approx_V y \approx_V z \;\Rightarrow x \approx_U z .$$
1. There exists an entourage; in light of axiom (6), it follows that the universal relation $X \times X$ is an entourage.
1. If $U, V$ are entourages, so is some subset of $U \cap V$. In light of axiom (6), it follows that $U \cap V$ is an entourage.
1. If $U$ is an entourage and $U \subseteq V \subseteq X \times X$, then $V$ is an entourage.

In [[constructive mathematics]], we also need this (classically trivial) condition:

* For every entourage $U$, there exists an entourage $V$ such that $\neg{V} \cup U = X \times X$, where $\neg{V}$ is the [[complement]] of $V$. That is,
  $$ \forall U,\; \exists V,\; \forall x, y,\; x \approx_U y \;\vee\; x &#8777;_V y .$$

We will call this axiom (0) when convenient.

A set equipped with a uniform structure is called a **uniform space**.


A collection of entourages satisfying (0--5) is a **base** for a uniformity; a base is precisely what generates a uniformity by taking the upward closure.  A collection satisfying (0--3) is a **preuniformity**; slightly more generally, we can replace each $V$ in the statement of these axioms with a finite [[intersection]] $V_1 \cap \cdots \cap V_n$ of entourages to get the concept of a **subbase** for a uniformity.  A subbase is precisely what generates a base by closing up under finite intersections and precisely what generates a uniformity by closing up under finite intersections and taking the upward closure.


The **uniform topology** induced by a uniformity is defined by taking the [[neighborhoods]] of a point $x$ to be sets of the form
$$ U[x] := \{ y \;:\; x \approx_U y \} $$
where $U$ is an entourage. (Recall that a set is open if it is a neighborhood of every point it contains.) We point out that different uniformities may give rise to the same topology (just as different metrics, even uniformly inequivalent ones, may give rise to the same topology).


Given uniform spaces $X$ and $Y$, a function $f: X \to Y$ is said to be **uniformly continuous** if for every entourage $V$ of $Y$, $(f \times f)^{-1}(V)$ is an entourage of $X$. Clearly, uniformly continuous functions are continuous with respect to the corresponding uniform topologies, but the converse is false (although see below the discussion in the case where $X$ is compact). There is an obvious [[concrete category]] $Unif$ of uniform spaces and uniformly continuous functions.


One feature of uniform space theory which is not available for general topological spaces is the possibility of taking (Cauchy) completions. The relevant definitions are straightforward:

* A **Cauchy net** in a uniform space $X$ consists of a [[directed set]] $D$ and a function $f: D \to X$ such that for every entourage $U$, there exists $N \in D$ such that $(f(m), f(n)) \in U$ whenever $m, n \geq N$. (One can similarly define a **Cauchy filter**.  This definition makes a uniform space into a [[Cauchy space]].)

* A Cauchy net $f: D \to X$ **converges** to $x \in X$ if for every entourage $U$, there exists $N \in D$ such that $n \geq N \Rightarrow (x, f(n)) \in U$.  (This definition makes sense for arbitrary [[nets]] or [[filters]], but it can be proved that any convergent net is Cauchy.  This definition makes a uniform space into a [[convergence space]].)

* A uniform space $X$ is **complete** if every Cauchy net/filter in $X$ converges (not necessarily to a unique point).

* A uniform space $X$ is **[[Hausdorff space|Hausdorff]]** or **separated** if every convergent net/filter converges to a unique point.  (This is a purely topological concept.)


Every uniform space $X$ admits a Hausdorff completion $\overline{X}$, i.e., there is a uniformly continuous map $X \to \overline{X}$ (an embedding if $X$ is Hausdorff, dense in any case), characterized by the following universal property:

* Every uniformly continuous function $f: X \to Y$ to a complete Hausdorff uniform space $Y$ extends uniquely to a uniformly continuous $\overline{f}: \overline{X} \to Y$.

In short, the category of complete Hausdorff uniform spaces is a [[reflective subcategory]] of $Unif$.

You can also define a (not necessarily Hausdorff) completion of $X$ by replacing the image of $X$ in $\overline{X}$ by $X$ itself, but this does not have as nice properties; in particular, complete uniform spaces do not form a reflective subcategory of $Unif$.


## Examples

Every [[metric space]] (or more generally any pseudometric space) is a uniform space, with a base of uniformities indexed by positive numbers $\epsilon$.  (You can even get a countable base, using only those $\epsilon$ equal to $1/n$ for some integer $n$.)  Define $x \approx_\epsilon y$ to mean that $d(x,y) \lt \epsilon$ (or $d(x,y) \leq \epsilon$ if you prefer).  Then axiom (3) may be proved by using $\epsilon/2$; axiom (0) may be proved constructively by using any positive number less than $\epsilon$ and applying the [[comparison]] law.  Every quasi(pseudo)metric space is a quasiuniform space in the same way.  We can also generalise from metric spaces to [[gauge spaces]]; see under Variations below.

Every [[topological group]] is a uniform space, with a base of uniformities indexed by neighbourhoods $U$ of the identity element, in two ways: left and right.  (These two ways agree for [[abelian groups]], of course; they also agree for [[compact group]]s, by the general theorem below for uniformities on [[compact spaces]].  I wonder if that has anything to do with Haar measure?)  In particular, any [[Banach space]] or [[Lie group]] is a uniform space.  Define $x \approx _U y$ to mean that $x \in y U$ (or $y \in x U$ for the other way).  Then axiom (3) may be proved by invoking the continuity of multiplication; axiom (0) cannot be proved constructively in general, although it can be proved for the classical examples of Lie groups and topological vector spaces (TVSs).

These are in a way the motivating examples.  The theory of uniformly continuous functions was developed first for metric spaces, but it was noticed that, for a metrisable TVS, it could be described entirely in terms of the topology and the addition, which immediately generalised to non-metrisable TVSs.  The theory of uniform spaces covers both of these (and their generalisations to pseudometric spaces and topological groups) at once.


## Basic Results

A first wave of results concerns [[separation axioms]]:

* Considered as topological spaces, uniform spaces are regular and (more profoundly) completely regular.

As a matter of fact, a significant theorem is that a topology is the uniform topology for some uniformity if and only if it is the topology of a completely regular space. See also the discussion below on the relation with metric and pseudometric spaces.

* For a uniform space, the following separation conditions are equivalent: $T_0$ (the topology distinguishes points), $T_1$ (points are closed), $T_2$ (Hausdorff), $T_3$ (regular Hausdorff), $T_{3\frac1{2}}$ (completely regular Hausdorff). Of course, this follows from the fact that it is completely regular.

* The category $Unif$ of uniform spaces admits arbitrary small [[products]] (which are preserved by the forgetful functors to [[Top]] and to [[Set]]). Hence it is not generally true that uniform spaces are [[normal space|normal]] (so that separated ones would be $T_4$), because for instance an uncountable power of the real line with its usual topology is not a normal space.

A second wave of results relates uniform spaces to [[pseudometric spaces]] (like metric spaces, but dropping the separation axiom that $d(x, y) = 0$ implies $x = y$):

* Every uniform space embeds uniformly in a product of pseudometric spaces. A uniform space whose uniformity admits a countable subbase is uniformly isomorphic to a pseudometric space (and hence to a metric space if the uniform space is separated, in which case the uniform space is called __metrisable__).

By this result, the results mentioned above on completions of uniform spaces may be proved by appeal to similar results for (pseudo)metric spaces.

Finally, we mention the special case of compact spaces:

* A [[compact Hausdorff space]] $X$ admits a unique uniformity whose corresponding topology is the topology of $X$. The entourages of this uniformity are precisely the neighborhoods of the diagonal in $X \times X$.

It follows then that if $X, Y$ are uniform spaces with $X$ compact Hausdorff and if $f: X \to Y$ is continuous, then $f$ is uniformly continuous.


## Variations

Some authors insist that a uniform space must be separated; this can be arranged directly in the definition (that is without reference to the uniform topology or to the concept of convergent net/filter) by adding the following axiom, a sort of converse axiom (1):

* If $x \approx_U y$ for every entourage $U$, then $x = y$.

This makes the discussion of completions slightly simpler.

If the symmetry axiom (2) is dropped, then the result is a __quasiuniform space__.  Quasiuniform spaces are related to quasi(pseudo)metrics in the same way as uniform spaces are related to (psuedo)metrics.  Perhaps surprisingly, *every* topological space is quasiuniformisable.

A __[[gauge space]]__ consists of a set $X$ and a collection $\mathcal{D}$ of pseudometrics on $X$; one usually requires $\mathcal{D}$ to be a [[filter]].  A gauge space defines a uniform space by taking one basic entourage for each pseudometric in $\mathcal{D}$ and each positive number $\epsilon$; conversely, every uniform space arises in this way, with the pseudometrics in the gauge being those that are uniformly continuous as maps on the product space.  However, gauge spaces form a category with a stricter notion of morphism, in which the categories $Met$ (of [[metric spaces]] and short maps) and $Unif$ (of uniform spaces and uniformly continuous maps) are both [[full subcategories]].  A __quasigauge space__ consists of a set and a collection of quasipseudometrics; every quasiuniform space arises from a quasigauge space.

In weak [[foundations]] of mathematics, the theorems above may not be provable.  In particular, the theorem that every uniform space arises from a gauge space is equivalent (internal to an arbitrary [[topos]] with a [[natural numbers object]]) to [[dependent choice]] (plus [[excluded middle]] if you leave out axiom 0).  If the concept is to be applied to analysis, then it may be best to define a uniform space as a gauge space satisfying a saturation condition.


## Motivation for the axioms

The really critical axioms are (1--3): a collection of binary relations which satisfies those three axioms is a subbase, from we can generate a uniform structure straightforwardly. Indeed, (4--6) simply state that the entourages form a [[filter]], so generating a uniformity from a base or subbase is simply the usual generation of a filter from a base or subbase.

We draw particular attention to axiom (3), which may be called an "$\frac{\varepsilon}{2}$" principle. It generalizes a principle familiar from analysis in metric spaces, where one establishes $d(x, z) \lt \varepsilon$ by showing there exists $y$ such that $d(x, y) \lt \frac{\varepsilon}{2}$ and $d(y, z) \lt \frac{\varepsilon}{2}$, and applying the triangle inequality. The utility of this principle for metric spaces, extrapolated in this way, gives uniform spaces much of their power.

For full power in [[constructive mathematics]], we also need axiom (0), which may similarly be called a "something less than $\varepsilon$" principle. (These two can actually be combined into a single statement, as you might expect since $\frac{\varepsilon}{2} \lt \epsilon$, but that makes the intuition less clear.)

Axiom (1) is a nullary version of the third axiom; together they prove that, given any entourage $U$ and any integer $n \geq 0$, there exists an entourage $V$ whose $n$-fold composite is contained in $U$. The symmetry axiom then allows one to take the opposite of $V$ at any point in the composite as well.

Altogether, these may be seen as axiomatising the notion of *approximate* [[equivalence relation|equivalence]].  If $\approx$ is an approximate equivalence relation, then we might expect it to be
*  [[reflexive relation|reflexive]]: $x \approx x$ and
*  [[symmetric relation|symmetric]]: $x \approx y$ iff $y \approx x$, but
*  NOT [[transitive relation|transitive]]: $x \approx y \approx z$ does not necessarily mean that $x \approx z$.

One could stop there, but this is not a very useful notion of approximation.  Instead we generalise to a *family* of approximate equivalence relations and impose the $\frac{\varepsilon}{2}$ principle to allow them to be used.  This is nearly the definition of uniform space; in particular, the axiom (1) states precisely that each entourage is reflexive.  The symmetry axiom in the standard definition is weaker than requiring each individual entourage to be symmetric, but that is not an essential change; every uniformity has a base consisting of its symmetric entourages.  The final three axioms have already been explained as a closure condition; they force equivalent uniformities on a given set (in the sense that the [[identity function]] on the set is uniformaly continuous either way) to be equal.


## Categorical interpretation

The idea that a uniformity is an "approximate equivalence relation" can be made precise as follows.  A [[preorder]] is the same as a category [[enriched category|enriched]] over the poset $\mathbb{2}$ of [[truth values]], and it is an equivalence relation if and only if this category is symmetric.  In fancier language, a preorder is a [[monoid]] (or [[monad]]) in the [[bicategory]] $Rel = \mathbb{2} Mat$.  A quasi-uniform space can then be identified with a monoid in the bicategory $Pro Rel$, whose hom-categories are the categories of [[pro-objects]] in the hom-categories of $Rel$, aka [[filters]].  Of course, it is a uniform space just when it is also symmetric.  See also [[prometric space]].

In all these cases, in order to recover the correct notion of morphism abstractly, we must consider monoids in a [[double category]] or [[equipment]] rather than merely a bicategory.


## References

*  A. Weil, _Sur les espaces &#224; structure uniforme et sur la topologie g&#233;n&#233;rale_, Actualit&#233;s Sci. Ind. 551, Paris, (1937).
* John Kelley, _General Topology_, GTM 27, 1955.
* Eric Schechter, _[[Handbook of Analysis and its Foundations]]_.
* Warren Page, _Topological Uniform Structures_, Dover
* I.M. James, _Topologies and Uniformities_, Springer
* Norman Howes, _Modern Analysis and Topology_, Springer


[[!redirects uniform spaces]]
[[!redirects uniformity]]
[[!redirects uniformities]]