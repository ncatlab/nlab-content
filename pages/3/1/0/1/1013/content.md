
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Category theory
+-- {: .hide}
[[!include category theory - contents]]
=--
=--
=--

# Stuff, structure, and properties
* table of contents
{: toc}

## Idea
 {#Idea}

It is common in [[mathematics]] to speak of 

1. objects enjoying "extra properties" (for instance a [[ring]] being [[commutative ring]]); 

1. objects carrying "extra structure" (for instance a [[set]] carrying a [[topological space|topology]]);

1. objects being equipped with "extra stuff" (for instance a [[ring]] being equipped with a [[module]]).

In [[model theory]] there is a formalization of what it means to equip a [[set]] with [[mathematical structure]], and one may say what it means for a function between these sets to have the property of preserving this extra structure. 
But this formalization captures only parts of the situations in which it is useful to speak of "extra property", "extra structure", and "extra stuff".

Now [[category theory]] is precisely the kind of mathematical meta-theory that allows a nice and general formalization of such matters. Here we discuss such a formalization, due to ([Baez-Bartels-Dolan 98](#BaezBartelsDolan98), see also [Baez-Shulman 06, section 2.4](#BaezShulman06)), phrased in terms of properties of [[functors]] that compare a [[category]] of [[objects]] with extra structure/property/stuff to the underlying category of objects without.

In fact this formalization involves the generalization of what in [[homotopy theory]] is called the [[Postnikov tower]] theory (or [[(n-connected, n-truncated) factorization system]]), generalizing this from [[groupoids]] to [[categories]] ([[directed homotopy type theory|directed homotopy types]]).

For related discussion see also at _[[structure type]]_ and _[[stuff type]]_.

Note that this account operates under the [[principle of equivalence]], where constructions are taken to be invariant under morphisms which are invertible in a maximally weak sense. When working with various amounts of [[strict n-category|strictness]], further requirements are appropriate, some of which are noted below.


## Definitions

To begin with, let $C$ and $D$ be [[groupoids]], and let $F: C \to D$ be a [[functor]].  By fiat, declare $F$ to be a [[forgetful functor]].  Then

* $F$ **forgets nothing** if it is an [[equivalence of categories]];
* $F$ **forgets only properties** if $F$ is [[full and faithful functor|fully faithful]];
* $F$ **forgets at most structure** if $F$ is [[faithful functor|faithful]];
* $F$ **forgets at most stuff** regardless.


Another way to break down the possibilities (used in a $3$-way [[factorization system|factorisation system]]) is as follows:

* $F$ **forgets only properties** if $F$ is [[full functor|full]] and faithful;
* $F$ **forgets purely structure** if $F$ is [[essentially surjective functor|essentially surjective]] (on objects) and faithful;
* $F$ **forgets purely stuff** if $F$ is essentially surjective and full.

{#Strengthening} Depending on author and the strictness of the situation, more properties are required of a functor to forget structure ([Ehresmann 57](#Ehresmann57), [Ehresmann 65](#Ehresmann65), [Adamek-Rosicky-Vitale 09, remark 13.18](#AdamekRosickyVitale)):

1. $F$ is an [[amnestic functor]] ($F$-vertical [[isomorphisms]] are [[identities]]),

1. $F$ is an [[isofibration]].

However, notice that these two conditions violate the [[principle of equivalence]] for [[categories]]. In the terminology of _[[strict categories]]_ one might hence refer to these conditions as expressing "strict extra structure".




### Interpretation in terms of k-surjectivity

The pattern here is best understood in terms of the notion of [[k-surjective functor|essentially k-surjective functor]]. 

Recall that for a functor between ordinary categories (1-categories)

* essentially surjective $\simeq$ essentially 0-surjective
* full $\simeq$ essentially 1-surjective
* faithful $\simeq$ essentially 2-surjective

and that every 1-functor is essentially $k$-surjective for all $k \geq 3$.

So the above says for a functor $F : C \to D$:

| If it is ...                        | then it ...               | but it ...                             |
| ----------------------------------- | ------------------------- | -------------------------------------- |
| essentially $(k \geq 0)$-surjective | forgets nothing           | remembers everything                   |
| essentially $(k \geq 1)$-surjective | forgets only properties   | remembers at least stuff and structure |
| essentially $(k \geq 2)$-surjective | forgets at most structure | remembers at least stuff               |
| essentially $(k \geq 3)$-surjective | may forget everything     | may remember nothing                   |


It is worth noting that this formalism captures the intuition of how "stuff", "structure", and "properties" are expected to be related:

* stuff may be equipped with structure;
* structure may have (be equipped with) properties.

The $3$-way breakdown looks like this:

| If it is ...                       | then it ...              | but it ...                                  |
| ---------------------------------- | ------------------------ | ------------------------------------------- |
| essentially $(k \ne 0)$-surjective | forgets only properties  | remembers at least stuff and structure      |
| essentially $(k \ne 1)$-surjective | forgets purely structure | remembers at least stuff and properties     |
| essentially $(k \ne 2)$-surjective | forgets purely stuff     | remembers at least structure and properties |

This formalism does *not* capture the intuition so well, and in fact the 'properties' (and 'structure') remembered by a functor that forgets purely structure (or purely stuff) may not match what one expects.

See also the examples below.


### Generalization to higher groupoids

The formulation in terms of $k$-surjectivity induces an immediate generalization of the notions of stuff, structure and properties to the context of [[infinity-category|infinity-groupoids]].  Baez's students speak of "2-stuff," "3-stuff," and so on.   Of course, structure and properties can then be called 0-stuff and $(-1)$-stuff, respectively.


### Generalization to categories and higher categories

The theory is easiest when restricted to groupoids as above; for [[category|categories]], there are several ways to go.  One is to keep the definition as phrased above (a functor between categories forgets only properties if it is fully faithful, forgets at most structure if it is faithful, etc.).  Another is to apply the above definition instead to the functor between the [[core|underlying groupoids]] of the categories in question.

To tell the difference, ask yourself whether the difference between a [[monoid]] and a [[semigroup]] is the *structure* of being equipped with an [[identity element]] or only the *property* that an identity element exists.  Note that an identity element, if it exists, must be unique and must be preserved by semigroup isomorphisms and by monoid homomorphisms but not by semigroup homomorphisms.

A third option is to define a new notion: a functor **forgets at most property-like structure** if it is [[pseudomonic functor|pseudomonic]].  This means that (1) the functor is faithful and (2) its induced functor between underlying groupoids is fully faithful.  Intuitively, property-like structure can be described as consisting of "properties which need not automatically be preserved by morphisms" or "structure which, if it exists, is uniquely determined." Examples include that a category has all limits of a specified sort.

Property-like structure becomes much more prevalent for higher categories.  For example, the forgetful functor from the 2-category of [[cartesian monoidal categories]] (and product-preserving functors) to [[Cat]] is essentially $(k\ge 2)$-surjective, and its induced functor between 2-groupoids is essentially $(k\ge 1)$-surjective; thus it forgets property-like structure.  See also [[lax-idempotent 2-monad]].

Note that property-like structure is known in traditional [[logic]] as __categorical__ structure.  Obviously, this term can be confusing in [[categorial logic]]!


## A factorisation system
 {#AFactorizationSystem}

Just as the category [[Set]] has the best known $2$-way [[factorization system|factorisation system]], in which every [[function]] is factored into a [[surjection]] followed by an [[injection]], so the [[2-category]] [[Cat]] has a [[ternary factorisation system]], in which every functor is factored into parts which forget 'purely' stuff, structure, and properties.

Specifically, given a functor $F: C \to D$, let the __[[1-image]]__ $1 im F$ of $F$ be the category whose objects are objects of $C$ and whose morphisms $x \to y$ are morphisms $F(x) \to F(y)$ in $D$; let the __[[2-image]]__ $2 im F$ of $F$ be the category whose objects are objects of $C$ and whose morphisms $x \to y$ are morphisms $b: F(x) \to F(y)$ in $D$ such that $b = F(a)$ for some $a: x \to y$ in $C$.  (So the only difference bewteen $2 im F$ and $C$ itself is equality of morphisms.)  If you want to be complete, call $C$ itself the __[[3-image]]__ of $F$ and $D$ the __[[0-image]]__.

The situation looks like this:

| This category ... | gets objects from ... | and morphisms from ... | and equality of morphisms from ... |
| ----------------- | --------------------- | ---------------------- | ---------------------------------- |
| $C$               | $C$                   | $C$                    | $C$                                |
| $2 im F$          | $C$                   | $C$                    | $D$                                |
| $1 im F$          | $C$                   | $D$                    | $D$                                |
| $D$               | $D$                   | $D$                    | $D$                                |

Then $F$ can be factored into functors
$$ C \stackrel{F_2}\to 2 im F \stackrel{F_1}\to 1 im F \stackrel{F_0}\to D ,$$
where $F_2$ forgets purely stuff, $F_1$ forgets purely structure, and $F_0$ forgets only properties.  Conversely, this ternary factorization suffices to determine the notions of faithful, full, and essentially surjective functors: see [[ternary factorization system]].


## Examples


### The classical categories of sets with extra structure

The classical examples are the forgetful functors to [[Set]]  that define the classical categories such as [[Top]], [[Grp]], [[Vect]], etc. All these categories are categories of <em>sets equipped with extra structure</em> (e.g. with a topology, with a group structure, etc). Accordingly the obvious functors to [[Set]] are 

* faithful
* not full.

Hence indeed, by the above yoga, they forget this extra structure but remember the stuff in question (the underlying set).


### More examples

The embedding of abelian groups into all groups, $F :$ [[Ab]] $\to$ [[Grp]] is faithful and full, but not essentially surjective. Hence it should remember stuff and structure but forget properties. Indeed, the property it forgets is the property "is abelian" which is a property of the group _structure_ sitting on the underlying set of a group. Hence the sequence of functors
$$
  Ab \to Grp \to Set \to pt
$$
(with [[point|pt]] the terminal category) successively forgets first a property (being abelian) then structure (the group structure on a set) then stuff (the underlying set).

Notice that the order here is backwards from the automatic factorisation given by the $3$-way factorisation system described above.  (And in fact, the structure forgotten here is not 'pure'; $Grp \to Set$ is not essentially surjective.)  Indeed, the above factorisation is arbitrary; it comes from seeing an abelian group as a group with an extra property and a group as a set with extra structure, but one may view things differently (for example, that an abelian group is a [[monoid]] with extra property, or a set with two group structures that are related as in the [[Eckmann-Hilton argument]]).

The automatic factorisation is in fact like this (up to [[equivalence of categories]]):
$$
  Ab \to \pt \to \pt \to \pt
$$
because the original functor $Ab \to \pt$ is already essentially surjective and full.  In other words, from the perspective of $\pt$, an abelian group is simply extra stuff.

More interestingly, we can factor the forgetful functor $Ab \to Set$:
$$
  Ab \to Ab \to Set \setminus \{\empty\} \to Set
$$
Here, the first part is trivial because $Ab \to Set$ is faithful.  The category $Set \setminus \{\empty\}$ is the category of [[inhabited set]]s, that is the category of sets that are capable of being equipped with the structure of an abelian group.  So from the point of view of its underlying set, an abelian group is a set with the *property* that it is inhabited and the *structure* of an abelian group but no additional *stuff*.

For something interesting at every level, take the functor $Ab \times Ab \to Set$ that takes the underlying set of the first abelian group.  This factors as follows:
$$
  Ab \times Ab \to Ab \to Set \setminus \{\empty\} \to Set
$$
So a pair of abelian groups (from the perspective of the underlying set of the first one) consists of the *property* that the set is inhabited, then the *structure* of an abelian group on that set, and finally extra *stuff* consisting of the entire second group.


## Logical interpretation

In [[logic]] a property $P$ is given by a [[predicate]], which we may think of as an operation that takes a thing $x$ to the [[truth value]] of the statement "$x$ has  property $P$".  Note that a truth value is a $(-1)$-[[(-1)-groupoid|groupoid]]; we get structure and stuff by replacing this with a [[set]] (a $0$-[[0-groupoid|groupoid]]) or a [[groupoid]] (a $1$-[[1-groupoid|groupoid]]) and we get $n$-stuff by replacing this with an $n$-[[n-groupoid|groupoid]].

Now, if a property of objects of a category $C$ that respects the [[principle of equivalence]] holds for some object $x$, then it must hold for any object [[isomorphism|isomorphic]] to $x$.  That is, the predicate defining that property is actually a [[functor]] from the [[core]] $C_iso$ of $C$ to the groupoid $TV_iso$ of truth values.  Given such a predicate functor $P$, it\'s immediate how to define a [[full subcategory]] $C_P$ of $C$ consisting of those objects with the property; the [[inclusion functor]] $C_P \hookrightarrow C$ is fully faithful, as it should be for extra property.  Conversely, given a fully faithful functor $F: D \to C$, define a property of objects of $C$ that respects the [[principle of equivalence]] as follows: an object $x$ of $C$ has the property if there is some object $a$ of $D$ such that $x \cong F(a)$.  If you apply this to $C_P \hookrightarrow C$, then you get the predicate $P$ back; if you start with an arbitrary fully faithful $F: D \to C$, define a predicate $P$, and then form $C_F$, you\'ll find that $C_F$ and $D$ are [[equivalence of categories|equivalent]], even as [[bundle]]s over $C$.

Diagrammatically this may be phrased as saying that every fully faithful functor $D \to C$ arises as a [[2-limit|weak pullback]] of the $1$-[[subobject classifier]]

$$
  \array{
    D_{iso} &\to& *
    \\
    \downarrow &\Downarrow& \downarrow^{true}
    \\
    C_{iso} &\stackrel{P}{\to}& \{\true, false \}
  }
$$


Similarly, any structure on objects of $C$ that respects the [[principle of equivalence]] is given by a functor from $C_iso$ to the groupoid $Set_iso$ of sets.  Given such a functor $P$, let $C_P$ be the [[category of elements]] of $P$, which comes with a faithful functor from $C_P$ to $C$.  Conversely, given any faithful functor $F: D \to C$ and an object $x$ of $C$, let $P(x)$ be the [[essential fiber]] of $F$ over $x$, which (because $F$ is faithful) is a [[discrete category]] and hence (equivalent to) a set.  These operations are also invertible, up to equivalence.

Diagrammatically this may be phrased as saying that every faithful functor $D \to C$ arises as a [[2-limit|weak pullback]] of the $2$-subobject classifier (as described at [[generalized universal bundle]] and at [[category of elements]])

$$
  \array{
    D_{iso} &\to& (Set_*)_{iso}
    \\
    \downarrow &\Downarrow& \downarrow
    \\
    C_{iso} &\stackrel{}{\to}& Set_{iso}
  }
  \,.
$$


Next, any stuff on objects of $C$ that respects the [[principle of equivalence]] is given by a functor from $C_iso$ to $Grpd_iso$.  Here $Grpd_iso$ should be taken to be the $2$-[[2-groupoid|groupoid]] whose objects are groupoids, whose morphisms are equivalences, and whose $2$-morphisms are [[natural isomorphism]]s; similarly, the functor $P: C_iso \to Grpd_iso$ should be taken in the weakest sense (often called a [[pseudofunctor]]).  Then the [[Grothendieck construction]] turns $P$ into a category $C_P$ equipped with a functor to $C$; again, the essential fiber converts any functor $F: D \to C$ into such a $P$ (although really you must take the core of the essential fiber to get a groupoid).

Diagrammatically this may be phrased as saying that every functor $D \to C$ arises as a [[2-limit|weak pullback]] of the $3$-subobject classifier (as described at [[generalized universal bundle]] )

$$
  \array{
    D_{iso} &\to& (Grpd_*)_{iso}
    \\
    \downarrow &\Downarrow& \downarrow
    \\
    C_{iso} &\stackrel{}{\to}& Grpd_{iso}
  }
  \,.
$$



If $C$ is a mere $1$-[[1-category|category]], then any $P: C_iso \to 2 Grpd_iso$ is equivalent to some $P: C_iso \to Grpd_iso$, but in general we need to consider $P: C_iso \to n Grpd_iso$ or $P: C_iso \to \infty Grpd_iso$ to study higher forms of $n$-stuff.

Lest we forget, to be even more simple than an extra property, the groupoid of $(-2)$-[[(-2)-groupoid|groupoid]]s is the [[point]] $pt$, and there is exactly one functor $P$ from any $C_iso$ to $pt$, corresponding to the unique (up to equivalence) category equivalent to $C$.

For the [[(∞,1)-topos]] [[∞-Grpd]] of [[∞-groupoid]]s the analog of the subobject classifier is the  [[universal fibration of (∞,1)-categories]] $Z|_{\infty Grpd} \to \infty Grpd$. See also section 6.1.6 _$\infty$-Topoi and Classifying objects_ of [[Higher Topos Theory|HTT]].

## Formulation in homotopy type theory

A map between [[homotopy type theory|homotopy types]] is equivalent to a [[dependent sum]] projection $f: \sum_{x: A} B(x) \to A$. If the types $B(x)$ are [[homotopy n-type|n-types]], $f$ forgets $n$-stuff.


## Related entries

*  [[predicate]]

*  [[structure]], [[structure type]]

*  [[stuff type]]

* [[topological property]], [[uniform property]]

## References

* {#BaezBartelsDolan98} [original UseNet discussion](http://math.ucr.edu/home/baez/qg-spring2004/discussion.html) on `sci.physics.research` in 1998;
* a pedagogical comparison to quadratic, linear, and constant polynomials ([PDF](http://math.ucr.edu/home/baez/qg-spring2004/polynomials.pdf)) by Toby Bartels in 2004;

* {#BaezShulman06} [section 2.4, p. 15](http://arxiv.org/PS_cache/math/pdf/0608/0608420v2.pdf#page=15) and [section 3.1, p. 17](http://arxiv.org/PS_cache/math/pdf/0608/0608420v2.pdf#page=17) of J. Baez and M. Shulman, _[[Lectures on n-Categories and Cohomology]]_ ([arXiv](http://arxiv.org/abs/math/0608420)).

* {#Ehresmann57} [[Charles Ehresmann]], _Gattungen in Lokalen Strukturen_, 1957

* {#Ehresmann65} [[Charles Ehresmann]], _Cat&#233;gories et Structures_, Dunod, 1965

* {#AdamekRosickyVitale09} Adamek, Rosicky, Vitale, _Algebraic theories_ [pdf](https://perso.uclouvain.be/enrico.vitale/gab_CUP2.pdf) (2009)


[[!redirects stuff, structure, property]]
[[!redirects stuff, structure, properties]]
[[!redirects stuff, structures, properties]]
[[!redirects stuff, structure and property]]
[[!redirects stuff, structure and properties]]
[[!redirects stuff, structures and properties]]
[[!redirects stuff, structure, and property]]
[[!redirects stuff, structure, and properties]]
[[!redirects stuff, structures, and properties]]
[[!redirects property, structure, stuff]]

[[!redirects property]]
[[!redirects properties]]
[[!redirects extra property]]
[[!redirects extra properties]]

[[!redirects extra structure]]
[[!redirects extra structures]]

[[!redirects property-like structure]]

[[!redirects stuff]]
[[!redirects extra stuff]]
[[!redirects n-stuff]]
[[!redirects extra n-stuff]]
