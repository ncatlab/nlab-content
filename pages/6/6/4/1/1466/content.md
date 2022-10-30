
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Topology
+--{: .hide}
[[!include topology - contents]]
=--
=--
=--


# Uniform spaces
* table of contents
{: toc}

## Idea

Uniform spaces were invented by [[André Weil]], to capture a general notion of [[space]] for which it makes sense to speak of [[uniformly continuous map]]s. Such spaces include (pseudo)[[metric spaces]] and [[topological groups]].

A uniform structure or uniformity on a set $X$ consists of a collection of global binary relations $\varepsilon$ which allow us to say when one point $x$ is "$\varepsilon$-close" to another $y$. For a metric space, we have for instance relations expressed by the formula $d(x, y) \lt \varepsilon$, where $\varepsilon$ is a [[positive number]]. For a topological group, we have relations $x y^{-1} \in \varepsilon$, where $\varepsilon$ is a [[neighborhood]] of the identity.


## Definitions

The definition described above is based on [[entourages]]; it was the original one published in [[Bourbaki]] and is still most commonly seen today.  There is an equivalent (but less directly generalisable) definition based on [[uniform covers]].  The relationship with [[gauge spaces]] (defined below) also allows for another definition.


### Entourage uniformities
{#ent}

A **uniform structure**, or **uniformity**, on a set $X$ consists of a collection of [[binary relations]] $U \subseteq X \times X$ (called __entourages__ or __vicinities__) satisfying some conditions. Write $x \approx_U y$ if $x$ is related to $y$ through $U$; then the conditions are the following:

1. The [[equality relation]] $\Delta = \{(x, x): x \in X\}$ is contained in every entourage. That is,
   $$ \forall U,\; \forall x,\; x \approx_U x .$$
2. For every entourage $U$, there exists an entourage $V$ such that $V^op \subseteq U$, where $V^\op$ is the [[opposite relation]] to $V$. That is,
   $$ \forall U,\; \exists V,\; \forall x, y,\; y \approx_V x \;\Rightarrow\; x \approx_U y .$$
   In light of axiom (6), it follows that $U^op$ itself is an entourage.
3. For every entourage $U$, there exists an entourage $V$ such that $V \circ V \subseteq U$, where $\circ$ is the ordinary operation of [[relation|relational composition]]. That is,
   $$ \forall U,\; \exists V,\; \forall x, y, z,\; x \approx_V y \approx_V z \;\Rightarrow x \approx_U z .$$
4. There exists an entourage; in light of axiom (6), it follows that the universal relation $X \times X$ is an entourage.
5. If $U, V$ are entourages, so is some subset of $U \cap V$. In light of axiom (6), it follows that $U \cap V$ is an entourage.
6. If $U$ is an entourage and $U \subseteq V \subseteq X \times X$, then $V$ is an entourage.

In [[constructive mathematics]], we also need this condition:

* For every entourage $U$, there exists an entourage $V$ such that $\neg{V} \cup U = X \times X$, where $\neg{V}$ is the [[complement]] of $V$. That is,
  $$ \forall U,\; \exists V,\; \forall x, y,\; x \approx_U y \;\vee\; x &#8777;_V y .$$

We will call this axiom (0) when convenient.  (With [[excluded middle]], we can take $V$ to be $U$ itself, so this is classically trivial.)

A set equipped with a uniform structure is called a **uniform space**.


A collection of entourages satisfying (0--5) is a **[[base]]** for a uniformity; a base is precisely what generates a uniformity by taking the upward closure.  A collection satisfying (0--3) is a **preuniformity**; slightly more generally, we can replace each $V$ in the statement of these axioms with a finite [[intersection]] $V_1 \cap \cdots \cap V_n$ of entourages to get the concept of a **[[subbase]]** for a uniformity.  A subbase is precisely what generates a base by closing up under finite intersections and precisely what generates a uniformity by closing up under finite intersections and taking the upward closure.


### Covering uniformities
{#ucov}

An equivalent way to characterize a uniform space is by its collection of *[[uniform covers]]*.  Here a **cover** of a set $X$ is a collection $C \subseteq P(X)$ with [[union]] $X$.  For covers $C_i$, we define:

* $C_1$ **refines** $C_2$, written $C_1 \prec C_2$, if every element of $C_1$ is a subset of some element of $C_2$.

* $C_1 \wedge C_2 \coloneqq \{ A \cap B \;|\; A \in C_1, B \in C_2 \}$; this is also a cover.

* For $A \subseteq X$, $C[A] \coloneqq \bigcup \{ B \in C \;|\; A \cap B$ is [[inhabited set|inhabited]] $}$.

* $C^* \coloneqq \{ C[A] \;|\; A \in C\}$.

We now define a **covering uniformity** on $X$ to be a collection of covers, called **uniform covers**, such that

1. If $C$ is a uniform cover, there exists a uniform cover $C'$ such that $(C')^* \prec C$.

2. There exists a uniform cover; in light of axiom (4), it follows that the cover $\{X\}$ is a uniform cover.

3. If $C_1, C_2$ are uniform covers, so is some cover that refines $C_1 \wedge C_2$. In light of axiom (4), it follows that $C_1 \wedge C_2$ is a uniform cover.

4. If $C$ is a uniform cover and $C \prec C'$, then $C'$ is a uniform cover.

The axioms (2--4) here roughly correspond (respectively) to the axioms (4--6) in the entourage definition.  Axiom (1) takes on all of the real work; any collection of covers that satisfies it may be called a __[[subbase]]__ (but not corresponding directly to a subbase in the previous definition).

In [[constructive mathematics]], we also want to add an axiom (0):

*  If $C$ is a uniform cover, there exists a uniform cover $C'$ such that, for any two points $x, y$, either $x, y \in A$ for some $A \in C$ or $x, y \in B$ for no $B \in C'$.

(With [[excluded middle]], we can take $C'$ to be $C$, so this is classically trivial.)

+-- {: .query}
Is there a more natural way to state this in this context?
=--

If $X$ is a uniform space defined in terms of entourages, we give it a covering uniformity by declaring a cover to be uniform if it is refined by $\{ U[x] \;|\; x \in X\}$ for some entourage $U$, where $U[x] \coloneqq \{ y \;|\; x \approx_U y \}$.  Note that this does not mean that a uniform cover "consists of $U$-sized sets" but only that it contains a subcover consisting of sets "no smaller than $U$".

Conversely, given a covering uniformity, we define a base of entourages to consist of sets of the form $\bigcup \{ A \times A \;|\; A \in C\}$ for $C$ a uniform cover.  That is, for each cover $C$, we have a basic entourage $\approx_C$ such that $x \approx_C y$ iff $x, y \in A$ for some $A \in C$.  This defines a bijection between entourage uniformities and covering uniformities.


### Further definitions

We give these in terms of entourages, but they could also be given directly in terms of uniform covers if desired.

The **uniform topology** induced by a uniformity is defined by taking the [[neighborhoods]] of a point $x$ to be sets of the form
$$ U[x] \coloneqq \{ y \;|\; x \approx_U y \} $$
where $U$ is an entourage. (Recall that a subset is [[open subset|open]] iff it is a neighborhood of every point that it contains.) We point out that different uniformities may give rise to the same topology (just as different metrics, even uniformly inequivalent ones, may give rise to the same topology).


Given uniform spaces $X$ and $Y$, a [[function]] $f\colon X \to Y$ is said to be **[[uniformly continuous map|uniformly continuous]]** if for every entourage $V$ of $Y$, $(f \times f)^{-1}(V)$ is an entourage of $X$. Clearly, uniformly continuous functions are [[continuous map|continuous]] with respect to the corresponding uniform topologies, but the converse is false (although see below the discussion in the case where $X$ is [[compact space|compact]]). There is an obvious [[concrete category]] $Unif$ of uniform spaces and uniformly continuous maps.


One feature of uniform space theory which is not available for general topological spaces is the possibility of taking (Cauchy) completions. The relevant definitions are straightforward:

* A **[[Cauchy net]]** in a uniform space $X$ consists of a [[directed set]] $D$ and a function $f\colon D \to X$ such that for every entourage $U$, there exists $N \in D$ such that $f(m) \approx_U f(n)$ whenever $m, n \geq N$. (One can similarly define a **Cauchy filter**.  This definition makes a uniform space into a [[Cauchy space]].)

* A Cauchy net $f\colon D \to X$ **[[convergence|converges]]** to $x\colon X$ if for every entourage $U$, there exists $N \in D$ such that $n \geq N \;\Rightarrow\; x \approx_U f(n)$.  (This makes sense for arbitrary [[nets]] or [[filters]], but it can be proved that any convergent net is Cauchy.  This definition makes a uniform space into a [[convergence space]].)

* A uniform space $X$ is **[[complete space|complete]]** if every Cauchy net/filter in $X$ converges (not necessarily to a unique point).

* A uniform space $X$ is **[[Hausdorff space|Hausdorff]]** or **separated** if every convergent net/filter converges to a unique point.  (This is a purely topological concept.)

With these definitions, every uniform space becomes a [[Cauchy space]].


Every uniform space $X$ admits a Hausdorff completion $\overline{X}$, i.e., there is a uniformly continuous map $X \to \overline{X}$ (an [[embedding]] if $X$ is Hausdorff, [[dense map|dense]] in any case), characterized by the following universal property:

* Every uniformly continuous map $f\colon X \to Y$ to a complete Hausdorff uniform space $Y$ extends uniquely to a uniformly continuous map $\overline{f}\colon \overline{X} \to Y$.

In short, the category of complete Hausdorff uniform spaces is a [[reflective subcategory]] of $Unif$.

One can also define a (not necessarily Hausdorff) completion of $X$ by replacing the image of $X$ in $\overline{X}$ by $X$ itself, but this does not have as nice properties; in particular, complete uniform spaces do not form a reflective subcategory of $Unif$.

Every uniform space also has an underlying [[proximity]] (defined there), and the resulting functor $Unif \to Prox$ has a fully faithful right adjoint which identifies proximity spaces with uniform spaces that are [[totally bounded space|totally bounded]].

Uniform spaces can also be identified with [[syntopogenous spaces]] that are both *perfect* and *symmetric*; see [[syntopogenous space]].


## Examples

Every [[metric space]] (or more generally any pseudometric space) is a uniform space, with a base of uniformities indexed by positive numbers $\epsilon$.  (You can even get a countable base, for example by using only those $\epsilon$ equal to $1/n$ for some integer $n$.)  Define $x \approx_\epsilon y$ to mean that $d(x,y) \lt \epsilon$ (or $d(x,y) \leq \epsilon$ if you prefer).  Then axiom (3) may be proved by using $\epsilon/2$; axiom (0) may be proved constructively by using any positive number less than $\epsilon$ and applying the [[comparison]] law.  (The other axioms are easy.)  Every quasi(pseudo)metric space is a quasiuniform space in the same way.  We can also generalise from metric spaces to [[gauge spaces]]; see under Variations below.

Every [[topological group]] is a uniform space, with a base of uniformities indexed by neighbourhoods $U$ of the identity element, in two ways: left and right.  (These two ways agree for [[abelian groups]], of course; they also agree for [[compact group]]s, by the general theorem below for uniformities on [[compact spaces]].  I wonder if that has anything to do with [[Haar measure]]?)  In particular, any [[Banach space]] or [[Lie group]] is a uniform space.  Define $x \approx _U y$ to mean that $x \in y U$ (or $y \in x U$ for the other way).  Then axiom (3) may be proved by invoking the continuity of multiplication; axiom (0) cannot be proved constructively in general, although it can be proved for the classical examples of Lie groups and [[topological vector spaces]] (TVSs).

These are in a way the motivating examples.  The theory of uniformly continuous maps was developed first for metric spaces, but it was noticed that, for a metrisable TVS, it could be described entirely in terms of the topology and the addition, which immediately generalised to non-metrisable TVSs.  The theory of uniform spaces covers both of these (and their generalisations to pseudometric spaces and topological groups) at once.


## Basic Results

A first wave of results concerns [[separation axioms]]:

* Considered as topological spaces, uniform spaces are [[regular space|regular]] and (more profoundly) [[completely regular space|completely regular]].

As a matter of fact, a significant theorem is that a topology (on a given set) is the uniform topology for some uniformity if and only if it is completely regular.  See also the discussion below on the relation with metric and pseudometric spaces.

* For a uniform space, the following separation conditions are equivalent: $T_0$ (the topology distinguishes points), $T_1$ (points are closed), $T_2$ ([[Hausdorff space|Hausdorff]]), $T_3$ (regular Hausdorff), $T_{3\frac1{2}}$ (completely regular Hausdorff). Of course, this follows from the fact that it is completely regular.

* The category $Unif$ of uniform spaces admits arbitrary small [[products]] (which are preserved by the forgetful functors to [[Top]] and to [[Set]]). Hence it is not generally true that uniform spaces are [[normal space|normal]] (so that separated ones would be $T_4$), because for instance an uncountable power of the [[real line]] (with its usual topology) is not a normal space.

A second wave of results relates uniform spaces to [[pseudometric spaces]] (like metric spaces, but dropping the separation axiom that $d(x, y) = 0$ implies $x = y$):

* Every uniform space embeds uniformly in a product of pseudometric spaces. A uniform space whose uniformity admits a countable subbase is uniformly isomorphic to a pseudometric space (and hence to a metric space if the uniform space is separated, in which case the uniform space is called __metrisable__).

By this result, the results mentioned above on completions of uniform spaces may be proved by appeal to similar results for (pseudo)metric spaces.

Finally, we mention the special case of compact spaces:

* A [[compact Hausdorff space]] $X$ admits a unique uniformity whose corresponding topology is the topology of $X$. The entourages of this uniformity are precisely the neighborhoods of the diagonal in $X \times X$.

It follows then that if $X, Y$ are uniform spaces with $X$ compact Hausdorff and if $f\colon X \to Y$ is continuous, then $f$ is uniformly continuous.


## Variations

Some authors insist that a uniform space must be separated; this can be arranged directly in the definition (that is without reference to the uniform topology or to the concept of convergent net/filter) by adding the following axiom, a sort of converse axiom (1):

* If $x \approx_U y$ for every entourage $U$, then $x = y$.

This makes the discussion of completions slightly simpler.

If the symmetry axiom (2) is dropped, then the result is a __quasiuniform space__.  Quasiuniform spaces are related to quasi(pseudo)metrics in the same way as uniform spaces are related to (psuedo)metrics.  Perhaps surprisingly, *every* topological space is quasiuniformisable.  (There does not seem to be a way to define quasiuniform spaces in terms of (quasi)uniform covers.)

A __[[gauge space]]__ consists of a set $X$ and a collection $\mathcal{D}$ of pseudometrics on $X$; one usually requires $\mathcal{D}$ to be a [[filter]].  A gauge space defines a uniform space by taking one basic entourage for each pseudometric in $\mathcal{D}$ and each positive number $\epsilon$; conversely, every uniform space arises in this way, with the pseudometrics in the gauge being those that are uniformly continuous as maps on the product space.  However, gauge spaces form a category with a stricter notion of morphism, in which the categories $Met$ (of [[metric spaces]] and short maps) and $Unif$ (of uniform spaces and uniformly continuous maps) are both [[full subcategories]].  A __quasigauge space__ consists of a set and a collection of quasipseudometrics; every quasiuniform space arises from a quasigauge space.

In weak [[foundations]] of mathematics, the theorems above may not be provable.  In particular, the theorem that every uniform space arises from a gauge space is equivalent (internal to an arbitrary [[topos]] with a [[natural numbers object]]) to [[dependent choice]] (plus [[excluded middle]] if you leave out axiom 0).  If the concept is to be applied to analysis, then it may be best to define a uniform space as a gauge space satisfying a saturation condition.

There is also a "pointless" notion of uniform space, called a [[uniform locale]].


## Motivation for the axioms

The really critical axioms are (1--3): a collection of binary relations which satisfies those three axioms is a subbase, from we can generate a uniform structure straightforwardly. Indeed, (4--6) simply state that the entourages form a [[filter]], so generating a uniformity from a base or subbase is simply the usual generation of a filter from a base or subbase.

We draw particular attention to axiom (3), which may be called an "$\frac{\varepsilon}{2}$" principle. It generalizes a principle familiar from analysis in metric spaces, where one establishes $d(x, z) \lt \varepsilon$ by showing there exists $y$ such that $d(x, y) \lt \frac{\varepsilon}{2}$ and $d(y, z) \lt \frac{\varepsilon}{2}$, and applying the triangle inequality. The utility of this principle for metric spaces, extrapolated in this way, gives uniform spaces much of their power.

For full power in [[constructive mathematics]], we also need axiom (0), which may similarly be called a "something less than $\varepsilon$" principle.  (That is, for any $\varepsilon$ there is an $\varepsilon'$ such that any two points are either $\varepsilon$-close or $\varepsilon'$-far; classically we may take $\varepsilon'$ to be $\varepsilon$, but constructively it\'s better to think of $\varepsilon' \lt \varepsilon$.)  Axioms (0) and (3) can actually be combined into a single statement, as you might expect since $\frac{\varepsilon}{2} \lt \varepsilon$, but that makes the intuition less clear.

Axiom (1) is a nullary version of axiom (3); together they prove that, given any entourage $U$ and any integer $n \geq 0$, there exists an entourage $V$ whose $n$-fold composite is contained in $U$. The symmetry axiom then allows one to take the opposite of $V$ at any point in the composite as well.

Altogether, these may be seen as axiomatising the notion of *approximate* [[equivalence relation|equivalence]].  If $\approx$ is an approximate equivalence relation, then we might expect it to be
*  [[reflexive relation|reflexive]]: $x \approx x$ and
*  [[symmetric relation|symmetric]]: $x \approx y$ iff $y \approx x$, but
*  NOT [[transitive relation|transitive]]: $x \approx y \approx z$ does not necessarily mean that $x \approx z$.

One could stop there, but this is not a very useful notion of approximation.  Instead we generalise to a *family* of approximate equivalence relations and impose the $\frac{\varepsilon}{2}$ principle to allow them to be used.  This is nearly the definition of uniform space; in particular, the axiom (1) states precisely that each entourage is reflexive.  The symmetry axiom in the standard definition is weaker than requiring each individual entourage to be symmetric, but that is not an essential change; every uniformity has a base consisting of its symmetric entourages.  The final three axioms have already been explained as a closure condition; they force equivalent uniformities on a given set (in the sense that the [[identity function]] on the set is uniformaly continuous either way) to be equal.


## Categorical interpretation

The idea that a uniformity is an "approximate equivalence relation" can be made precise as follows.  A [[preorder]] is the same as a category [[enriched category|enriched]] over the poset $\mathbb{2}$ of [[truth values]], and it is an equivalence relation if and only if this category is symmetric.  In fancier language, a preorder is a [[monoid]] (or [[monad]]) in the [[bicategory]] $Rel = \mathbb{2} Mat$.  A quasi-uniform space can then be identified with a monoid in the bicategory $Pro Rel$, whose hom-categories are the categories of [[pro-objects]] in the hom-categories of $Rel$, aka [[filters]].  Of course, it is a uniform space just when it is also symmetric.  See also [[prometric space]].

In all these cases, in order to recover the correct notion of morphism abstractly, we must consider monoids in a [[double category]] or [[equipment]] rather than merely a bicategory.

## Related concepts

* [[proximity space]], [[syntopogenous space]]


## References

*  A. Weil, _Sur les espaces &#224; structure uniforme et sur la topologie g&#233;n&#233;rale_, Actualit&#233;s Sci. Ind. 551, Paris, (1937).

* John Kelley, _General Topology_, GTM 27, 1955.

* Eric Schechter, _[[Handbook of Analysis and its Foundations]]_.

* Warren Page, _Topological Uniform Structures_, Dover

* I.M. James, _Topologies and Uniformities_, Springer

* Norman Howes, _Modern Analysis and Topology_, Springer


[[!redirects uniform space]]
[[!redirects uniform spaces]]
[[!redirects uniform structure]]
[[!redirects uniform structures]]
[[!redirects uniformity]]
[[!redirects uniformities]]

[[!redirects quasiuniform space]]
[[!redirects quasiuniform spaces]]
[[!redirects quasi-uniform space]]
[[!redirects quasi-uniform spaces]]
[[!redirects quasiuniform structure]]
[[!redirects quasiuniform structures]]
[[!redirects quasi-uniform structure]]
[[!redirects quasi-uniform structures]]
[[!redirects quasiuniformity]]
[[!redirects quasiuniformities]]
[[!redirects quasi-uniformity]]
[[!redirects quasi-uniformities]]
