
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Relations
+-- {: .hide}
[[!include relations - contents]]
=--
=--
=--

# Apartness relations
* table of contents
{: toc}

## Idea

An _apartness relation_ is a [[binary relation]] that, instead of saying when two things are the same (as an [[equivalence relation]]), states when two things are different -- an [[inequality relation]].

Apartness relations are most used in [[constructive mathematics]]; in [[classical mathematics]], equivalence relations can take their place (mediated by [[negation]]).

The apartness relations that we discuss here are sometimes called __point--point apartness__, to distinguish this from the related concepts of _set--set_ or _point--set_ apartness relations; see [[proximity space]] and [[apartness space]] (respectively) for these.


## Definitions

### Abstract

A [[set]] $S$ equipped with an __apartness relation__ is a [[groupoid]] (with $S$ as the set of [[objects]]) [[enriched category|enriched]] over the [[cartesian monoidal category]] $TV^\op$, that is the [[opposite category|opposite]] of the [[partial order|poset]] of [[truth value|truth values]], made into a [[monoidal category]] using [[disjunction]]. By the law of [[excluded middle]] (which says that $TV$ is self-dual under [[negation]]), this is equivalent to equipping $S$ with an [[equivalence relation]] (which makes $S$ a groupoid [[enriched category|enriched]] over the cartesian category $TV$ *itself*). But in [[constructive mathematics]] (or interpreted [[internalization|internally]]), it is a richer concept with a topological flavour, as $TV^\op$ is a [[co-Heyting algebra]]. 

### Concrete

Of course, nobody but a category-theorist would use the above as a *definition* of an apartness relation. Normally, one defines an apartness relation on $S$ as a binary relation $\#$ satisfying these three properties:

* [[irreflexive relation|irreflexivity]]: for all $x: S$, $x \# x$ is false;
* [[symmetric relation|symmetry]]: for all $x, y: S$, if $y # x$, then $x # y$;
* [[comparison]]: for all $x, y, z: S$, if $x # z$, then $x # y$ or $y # z$.

(Notice that these are dual to the axioms for an [[equivalence relation]]; like those axioms, these correspond to [[identity morphisms]], [[inverses]], and [[composition]] in a groupoid.)


### Related notions

The [[negation]] of an apartness relation is an equivalence relation. (On the other hand, the statement that every equivalence relation is the negation of some apartness relation is equivalent to [[excluded middle]], and the statement that the negation of an equivalence relation is always an apartness relation is equivalent to the nonconstructive [[de Morgan law]].) An apartness relation is __tight__ (see [[connected relation]]) if this equivalence relation is [[equality]]; any apartness relation defines a tight apartness relation on the [[quotient set]]. A tight apartness relation, also called an __inequality__, is often written $\ne$ instead of $\#$, but keep in mind that $\ne$ is not the negation of $=$; rather, $=$ is the negation of $\ne$. (So inequality, when it exists, is more basic than equality.)

If $S$ and $T$ are both sets equipped with apartness relations, then a [[function]] $f\colon S \to T$ is __[[strongly extensional function|strongly extensional]]__ if $x \# y$ whenever $f(x) \# f(y)$; that is, $f$ reflects apartness. The strongly extensional functions are precisely the [[enriched functors]] between $TV^\op$-enriched groupoids, so they are the correct morphisms. (Note that there is no nontrivial notion of enriched [[natural isomorphism]], at least not when the apartness in $T$ is tight.)

In [[homotopy type theory]], a __pure tight apartness relation__ on a type $A$ is a [[type family]] $#_A:(A \times A) \rightarrow Type$ such that $\prod_{m:A} \prod_{n:A} ((m #_A n) \rightarrow 0) = (m =_A n)$, where $=_A$ is the [[equality type]] on $A$ and $=$ is equality between types. A __mere tight apartness relation__ on a type $A$ is a mere relation $#_A:(A \times A) \rightarrow Prop$ such that $\vert \prod_{m:A} \prod_{n:A} ((m #_A n) \rightarrow 0) \vert = \vert m =_A n\vert$, where $\vert A \vert$ is the [[propositional truncation]] of type $A$. 

## The category of inequality spaces

By an __inequality space__, I mean a set equipped with a tight apartness relation. By a __map__, I mean a strongly extensional function between inequality spaces.

In the category of inequality spaces, [[monomorphisms]] between inequality spaces are strongly extensional functions that preserve tight apartness, or strong [[injections]]. These monomorphisms are [[regular monomorphisms]]. The category of inequality spaces has all (small) [[limits]], [[created limit|created]] by the [[forgetful functor]] to [[Set]]. (For example, $(a,b) \ne (x,y)$ iff $a \ne x$ or $b \ne y$.) Similarly, it has all finite [[coproducts]], and it has [[quotient object|quotients]] of [[equivalence relations]]. In fact, this category is a [[complete category|complete]] [[pretopos]]. It is *not*, however, a [[Grothendieck topos]] (or even a [[topos]] at all), because it doesn\'t have all infinite coproducts. (To be precise, the statement that it has all small coproducts, or even that it has a subobject classifier, seems to be equivalent to excluded middle.)

We can say, however, that it has coproducts indexed by inequality spaces, although to make this precise is a triviality. More interestingly, it has products indexed by inequality spaces; that is, it is (even [[locally cartesian closed category|locally]]) a [[cartesian closed category]]. In particular, given inequality spaces $X$ and $Y$, the set $\StrExt(X,Y)$ of maps from $X$ to $Y$ becomes an inequality space under the rule that $f \ne g$ iff $f(x) \ne g(x)$ for some $x\colon X$.

If you generalise from inequality spaces to allow non-tight apartness relations, then you get (at first) a different category. However, now you also have $2$-[[2-morphism|morphisms]] which serve to identify unequal but equivalent (that is, not apart) elements of a space, so the resulting bicategory is [[equivalence of categories|equivalent]] to the category of inequality spaces.


## Topological aspects {#topology}

### The apartness topology

Let $S$ be a set equipped with an apartness relation $\ne$. Using $\ne$, many [[topology|topological]] notions may be defined on $S$. (Often one assumes that the apartness is tight; this corresponds to the $T_0$ [[separation axiom]] in topology.)

If $U$ is a [[subset]] of $S$ and $x$ is an element, then $U$ is a $\ne$-**[[neighbourhood]]** (or $\ne$-**neighborhood**) of $x$ if, given any $y\colon S$, $x \ne y$ or $y \in U$; note that $x \in U$ by irreflexivity. The neighbourhoods of $x$ form a [[filter]]: a superset of a neighbourhood is a neighbourhood, and the intersection of $0$ or $2$ (hence of any finite number) of neighbourhoods is a neighbourhood.

A subset $G$ is $\ne$-**[[open subset|open]]** if it\'s a neighbourhood of all of its members. The open subsets form a [[topological space|topology]] (in the sense of Bourbaki): any union of open subsets is open, and the intersection of $0$ or $2$ (hence of any finite number) of open subsets is open.

The $\ne$-**complement** of $x$ is the subset $\{y\colon S \;|\; x \ne y\}$; this is open by comparison. More generally, the $\ne$-**[[complement]]** of any subset $A$ is the set $\tilde{A}$, defined as:
$$ \tilde{A} \coloneqq \{y \;|\; \forall{x} \in A,\; x \ne y\} .$$
This is not in general open, but you would use it where you would classically use the set-theoretic complement. However, if $A$ is open to begin with, then $\tilde{A}$ equals the set-theoretic complement.

If $x \ne y$, then $x \in \tilde{y}$ and $y \in \tilde{x}$.  Thus, if $\ne$ is tight, then $(S, \ne)$ satisfies the $T_1$ [[separation axiom]]. Symmetry is important here; if we removed symmetry from the axioms of apartness (obtaining a [[quasi-apartness]]) but retained tightness, then we would still get a $T_0$ topology, but it would not be $T_1$. This is a version of the fact that failure of $T_1$ is given by a [[partial order]] (or a [[preorder]] if $T_0$ might also fail).

The $\ne$-**[[closure]]** $\bar{A}$ of a subset $A$ is the complement of its complement. This closure is a [[closure operator]]: $A \subset \bar{A}$, $\overline{\bar{A}} = \bar{A}$ (in fact, $\overline{\tilde{A}} = \tilde{A}$), $\bar{A} \subset \bar{B}$ whenever $A \subset B$, $\overline{S} = S$ (in fact, $\bar{\empty} = \empty$ too), and $\overline{A \cap B} = \bar{A} \cap \bar{B}$ (but *not* $\overline{A \cup B} = \bar{A} \cup \bar{B}$).

The __antigraph__ of a function $f\colon S \to T$ is
$$ \{(x,y) \;|\; x\colon S, y\colon T \;|\; f(x) \ne y\} .$$
Recall that in ordinary topology, a function between [[Hausdorff spaces]] is continuous iff its [[graph of a function|graph]] is closed. Similarly, a function $f\colon S \to T$ is strongly extensional iff its antigraph is open. (Then the [[graph of a function|graph]] of $f$ is the complement of the antigraph.)

One important topological concept that doesn\'t appear classically is locatedness; in an inequality space, a subset $A$ is __[[located subspace|located]]__ if, given any point $x$ and any neighbourhood $U$ of $x$, either $U \cap A$ is [[inhabited set|inhabited]] (that is, it has a point) or some neighbourhood of $x$ (not necessarily $U$) is contained in $\tilde A$. Note that every point is located. (For an example of a set that need not be located, consider $\{x\colon S \;|\; p\}$, where $p$ is an arbitrary [[truth value]]. In an inhabited space, this set is located iff $p$ is true or false.)


### Relation to metric spaces

Recall that, as [[Bill Lawvere]] taught us, a [[metric space]] is a groupoid (or $\dagger$-[[dagger-category|category]]) enriched over the category $([0,\infty[^\op,+)$ of nonnegative [[real numbers]], ordered in reverse, and made monoidal under addition. (Actually, you get a metric only if you impose a tightness condition, although again you can recover this up to equivalence from the $2$-morphisms. Furthermore, Lawvere advocated using $[0,\infty]$ instead of $[0,\infty[$, and also dropping the symmetry requirement to get enriched categories instead of groupoids. Thus, he dealt with extended quasipseudometric spaces. These details are not really important here.)

There is a [[monoidal functor]] from $([0,\infty[^\op,+)$ to $TV^\op$ that maps a nonnegative real number $x$ to the truth value of the statement that $x \gt 0$. Accordingly, any (symmetric) metric space becomes an inequality space, and any function satisfying $d(f(x),f(y)) \leq d(x,y)$) is strongly extensional.

The topological properties of metric spaces fit well with those of inequality spaces if you always work in this direction. For example, a set which is $d$-open will also be $\ne$-open, but not necessarily the other way around. Similarly, a (merely) [[continuous function]] between metric spaces is (still) strongly extensional.


### Relation to gauge spaces and uniform spaces

In analysis, many spaces are given as [[gauge spaces]], that is by families of pseudometrics; these also become inequality spaces by declaring that $x \ne y$ iff $d(x,y) \gt 0$ for some pseudometric $d$ in the family. (This will actually be a *tight* apartness iff the family of pseudometrics is separating.)

Classically, any [[uniform space]] may be given by a family of pseudometrics, but this doesn\'t hold constructively. In particular, a topological group may not be an inequality group (as in the next section).  However, we can generalize a bit beyond gauge spaces: any [[uniformly regular uniform space]] becomes an inequality space by declaring that $x \ne y$ iff there is an entourage $U$ with $(x,y)\notin U$.  (If the uniform space is not uniformly regular, the result is merely an [[inequality relation]], not an apartness.)


### Relation to proximity spaces

The constructive theory of [[proximity spaces]] is based on a generalisation of apartness relations (which here go between *points*) to an apartness relation between *sets*.  These are called _[[apartness space|apartness spaces]]_; just as apartness relations (between points) are classically equivalent to equivalence relations, so apartness spaces are classically equivalent to proximity spaces, with two sets being proximate if and only if they are not apart.

Of course, any apartness space has an apartness relation between points: $x$ and $y$ are apart iff $\{x\}$ and $\{y\}$ are apart.


### Relation to locales

Let $X$ be a set, regarded as a [[discrete locale]], whose [[frame]] of opens is $O(X) = P(X)$, the [[power set]] of $X$.  That is, the opens in the locale $X$ are precisely the subsets of the set $X$.  Since discrete locales are [[locally compact locale|locally compact]] (every set is the union of its [[K-finite set|K-finite]] subsets), the locale product $X\times X$ agrees with the spatial product, so that $X\times X$ is also discrete and every subset of $X\times X$ is open.  Thus, the opens in the locale $X\times X$ are precisely the subsets of $X\times X$.  In particular, an [[equivalence relation]] on the set $X$ can be identified with an *open* equivalence relation (in [[Loc]]) on the discrete locale $X$.

Thus, the following theorem gives a different precise sense in which apartness relations are dual to equivalence relations.

+--{: .num_theorem #ClosedLocalicEquivalenceRelation}
###### Theorem
An apartness relation on a set $X$ is the same as a (strongly) [[closed subspace|closed]] equivalence relation on the discrete locale $X$.  Moreover, the apartness topology defined above is, as a locale, the quotient of this equivalence relation.
=--
+--{: .proof}
###### Proof
By definition, a (strongly) closed sublocale of a locale $Y$ is one of the form $\mathsf{C}U$, for some open $U\in O(Y)$.  Thus, when $X$ is a discrete locale, a closed sublocale of $X\times X$ is of the form $\mathsf{C}U$ for some subset $U$ of $X\times X$.  This subset is the extension of the apartness relation, i.e. $U = \{ (x,y) \mid x\#y \}$.

For the first claim, therefore, it remains to show that the three axioms of an equivalence relation for $\mathsf{C}U$ correspond to the apartness axioms for $\#$.  Note that pullback along locale maps respects closed complements, i.e. $f^*(\mathsf{C}U) = \mathsf{C}(f^*U)$.  Thus, the pullback of $\mathsf{C}U$ along the twist map $X\times X \to X\times X$ is the closed sublocale corresponding to the twist of $U$, i.e. the set $\{ (x,y) \mid y\#x \}$.  Since $\mathsf{C}$ is a contravariant order-isomorphism between the posets of open and closed sublocales, symmetry for $\mathsf{C}U$ is equivalent to symmetry for $\#$.  Similarly, pulling $\mathsf{C}U$ back to $X\times X\times X$ along one of the three canonical projections gives the closed sublocale dual to the corresponding pullback of $U$ itself, and $\mathsf{C}$ transforms unions to intersections; thus transitivity for $\mathsf{C}U$ is equivalent to comparison for $\#$.  Finally, the pullback of $\mathsf{C}U$ along the diagonal is the closed sublocale dual to the similar pullback of $U$, so to say that the former is all of $X$ is equivalent to saying that the latter is $\emptyset$; thus reflexivity for $\mathsf{C}U$ is equivalent to irreflexivity for $\#$.

Now, the quotient in $Loc$ of such an an equivalence relation in particular comes equipped with a surjective locale map from $X$.  Thus, it is a spatial locale and can be regarded as a topology on the set $X$.  Moreover, quotients in $Loc$ are constructed as [[equalizers]] in $Frm$, so we have to compute the equalizer of the two maps $O(X) = P(X) \to O(\mathsf{C}U)$, where $O(\mathsf{C}U)$ is the frame of opens of $\mathsf{C}U$ regarded as a locale in its own right.  Equivalently, this means the equalizer of the two maps $P(X) \xrightarrow{\pi_i} P(X\times X) \xrightarrow{j_{\mathsf{C}U}} P(X\times X)$, where $j_{\mathsf{C}U}$ is the [[nucleus]] corresponding to $\mathsf{C}U$.

Now by definition, $j_{\mathsf{C}U}(V) = V\cup U$.  Thus, the elements of this equalizer --- which is to say, the opens in the locale quotient --- are subsets $V$ of $X$ such that $(V\times X) \cup U = (X\times V) \cup U$.  Reexpressed in terms of $\#$, that means that for any $x,y\in X$ we have $(x\in V \vee x\#y) \iff (y\in V \vee x\#y)$.  But since $\#$ is symmetric, this is equivalent to the unidirectional implication $(x\in V \vee x\#y) \to (y\in V \vee x\#y)$, and since $x\#y$ always implies itself, this is equivalent to $x\in V \to (y\in V \vee x\#y)$, which is precisely the condition defining the open sets in the apartness topology above.
=--

Recall that the negation of an apartness relation on $X$ is an equivalence relation on the *set* $X$.  This is the spatial part of the above closed localic equivalence relation, which in general (constructively) need not be itself spatial.  The apartness relation is tight just when this spatial part is the diagonal.  (By contrast, to say that the closed localic equivalence relation is *itself* the diagonal is to say that the discrete locale $X$ is [[Hausdorff space|Hausdorff]], which is only true if $X$ has [[decidable equality]].)

Another characterization of the $\#$-open sets is that $U$ is $\#$-open if $U\times X \subseteq (X\times U) \cup W_\#$, where $W_\#$ is $\#$ regarded as a subset of $X\times X$.  Rephrased in terms of complementary closed sublocales, this says that $\mathsf{C}U$ is "closed under the equivalence relation" dual to $\#$.  Thus, the closed sublocales of $X$ with its $\#$-topology (i.e. the formal complements of $\#$-open sets) correspond precisely to the closed sublocales of $X$ (the formal complements of arbitrary subsets of $X$) that respect this equivalence relation.

As a partial converse to the above theorem, if $X$ is a [[Hausdorff space|localically strongly Hausdorff]] topological space, meaning that its diagonal is a strongly closed sublocale, then the pullback of this diagonal to the discrete locale on the set of points of $X$ is a closed localic equivalence relation, hence an apartness, whose $\ne$-topology refines the given topology.  See [this theorem](/nlab/show/Hausdorff+space#Apartness).  If we are given an apartness relation $\ne$, it is unclear whether the $\ne$-topology is localically strongly Hausdorff; but if it is, then the apartness relation resulting from this topology is stronger than the given $\ne$.

## In algebra

Since inequality spaces have finite limits, the usual constructions of [[universal algebra]] apply; it\'s straightforward to define inequality [[groups]], inequality [[rings]], and so on.

The various subsets that appear in algebra (such as [[subgroups]], [[ideals]], and [[cosets]]) become less fundamental than certain subsets that are, classically, simply their complements. For example, a left ideal in a ring $R$ is a subset $I$ such that $0 \in I$, $x + y \in I$ whenever $x, y \in I$, and $x y \in I$ whenever $x \in I$. But a left _[[antiideal]]_ in an inequality ring $R$ is an $\ne$-open subset $A$ such that $0 \in A$ is false, $x \in A$ or $y \in A$ whenever $x + y \in A$, and $x \in A$ whenever $x y \in A$.  (The $\ne$-openness requirement is automatic if $\neg(0\in A)$ is strengthened to $p\ne 0$ for all $p\in A$, using that the ring operations are strongly extensional.)  Note that the complement of an antiideal is an ideal, but not every ideal can be constructively shown to be the complement of an antiideal; so antiideals are more fundamental than ideals, in an inequality ring.

[[prime ideal|Prime ideals]] are even more interesting. A two-sided antiideal $A$ (so also satisfying that $y \in A$ whenever $x y \in A$) is _antiprime_ (or simply _prime_ if no confusion is expected) if $1 \in A$ and $x y \in A$ whenever $x, y \in A$. Now the complement of an antiprime antiideal may *not* be a prime ideal (as normally defined). But in fact, it is antiprime antiideals that are more important in constructive algebra. In particular, an [[integral domain]] in constructive algebra is an inequality ring in which the antiideal of nonzero elements is antiprime.

The localic perspective on apartness relations extends naturally to anti-algebra: an antiideal is the same as a *closed* ideal in a discrete localic ring that respects the closed equivalence relation corresponding to $\ne$.  Equivalently, this is a closed ideal of the $\ne$-topology regarded as a (non-discrete) localic ring.  The spatial part of this closed localic ideal is then the ordinary ideal complementary to the antiideal, and so on.  Moreover, since unions of closed sublocales correspond to intersections of their open complements, an antiideal $A$ is antiprime exactly when its corresponding closed localic ideal $\mathsf{C}A$ is "prime" in an appropriate internal sense in [[Loc]], namely that $m^*(\mathsf{C}A) \subseteq (\mathsf{C}A \times R) \cup (R\times \mathsf{C}A)$, where $m:R\times R\to R$ is the multiplication.  The fact that the complement of an antiprime antiideal need not be prime in the usual sense corresponds to the fact that taking the spatial part of sublocales doesn't commute with unions.

For more about apartness algebra, see [[antisubalgebra]].

## Related concepts

* [[inequality relation]]

  * [[denial inequality]]

* [[antisubalgebra]]

[[!include logic symbols -- table]]

## References

According to [Troelstra and van Dalen](#TvD):

> Brouwer ([1919](#Brouwer1919)) introduced the notion of apartness (&#246;rtlich verschieden, Entfernung).... The axioms of the theory of apartness were formulated by Heyting ([1925](#Heyting1925)).

* {#Brouwer1919} [[L.E.J. Brouwer]], _Begr&#252;ndung der Mengenlehre unabh&#228;ngig vom logischen Satz vom ausgeschlossenen Dritten II: Theorie der Punktmengen.  1919

* {#Heyting1925} [[Arend Heyting]], _Intu&#239;tionistische Axiomatiek der Projectieve Meetkunde_ (Dutch), Ph.D. Thesis, 1925 

* [[Errett Bishop]]'s _Foundations of Constructive Analysis_ (1967) uses apartness for the real numbers and more general metric spaces.

* The 1985 edition with Douglas Bridges, _Constructive Analysis_, includes the general definition of apartness relation, there called an "inequality relation" (though in many other sources, as here, an [[inequality relation]] need not satisfy comparison).

* {#TvD} Anne Troelstra\'s and Dirk van Dalen\'s _Constructivism in Mathematics_ (1988) uses apartness for the reals (volume 1), and general apartness relations in algebra (volume 2, chapter 8).  They say "preapartness" and "apartness" instead of "apartness" and "tight apartness" respectively.

* Apartness plays a minimal role in _A Course in Constructive Algebra_ (also 1988), by Ray Mines, Fred Richman, and Wim Ruitenburg.

* A great reference for point-set topology in constructive mathematics is the Ph.D. thesis of Frank Waaldijk, _[Modern Intuitionist Topology](http://www.fwaaldijk.nl/modern%20intuitionistic%20topology.pdf)_ (1996).


[[!redirects apart]]
[[!redirects apartness]]
[[!redirects apartnesses]]

[[!redirects apartness structure]]
[[!redirects apartness structures]]
[[!redirects apartness relation]]
[[!redirects apartness relations]]

[[!redirects point-point apartness space]]
[[!redirects point-point apartness spaces]]
[[!redirects point–point apartness space]]
[[!redirects point–point apartness spaces]]
[[!redirects point--point apartness space]]
[[!redirects point--point apartness spaces]]
[[!redirects point-point apartness structure]]
[[!redirects point-point apartness structures]]
[[!redirects point–point apartness structure]]
[[!redirects point–point apartness structures]]
[[!redirects point--point apartness structure]]
[[!redirects point--point apartness structures]]
[[!redirects point-point apartness relation]]
[[!redirects point-point apartness relations]]
[[!redirects point–point apartness relation]]
[[!redirects point–point apartness relations]]
[[!redirects point--point apartness relation]]
[[!redirects point--point apartness relations]]

[[!redirects tight apartness]]
[[!redirects tight apartnesses]]
[[!redirects tight apartness structure]]
[[!redirects tight apartness structures]]
[[!redirects tight apartness relation]]
[[!redirects tight apartness relations]]

[[!redirects inequality space]]
[[!redirects inequality spaces]]
