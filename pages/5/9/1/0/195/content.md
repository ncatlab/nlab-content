
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Foundations
+-- {: .hide}
[[!include foundations - contents]]
=--
#### Category theory
+-- {: .hide}
[[!include category theory - contents]]
=--
#### Mathematics
+-- {: .hide}
[[!include mathematicscontents]]
=--
=--
=--

# Sets
* table of contents
{: toc}


## What should a set be?

The concept of _set_ appears in several different guises in [[mathematics]], and particularly in [[category theory]].


It is common to use [[foundations of mathematics]] in which 'set' is an undefined term; this is [[set theory]] as a foundation.  In a [[pure set|pure]] [[material set theory]] like [[ZFC]], every object is a set.  Even in a [[structural set theory|structural approach]] such as [[ETCS]], it is common for every object to be a [[structured set]] in some way or another.

Even if sets are not at the bottom of your foundations, still they are probably close.  For instance, in [[type theory]] sometimes sets are defined as [[predicates]] on [[types]], or as [[setoids]].  In [[homotopy type theory]], sets are defined as [[truncated object|0-truncated]] homotopy types; see below.

Material set theory conflates two notions of sets, which were elegantly (but not first) described by [[Mathieu Dupont]] in [a blog post](http://math.breckes.org/2009/03/the-two-meanings-of-the-word-%E2%80%9Cset%E2%80%9D-in-mathematics/) as 'set&#185;' and 'set&#178;', which we will here call 'abstract set' and 'concrete set'.  In the latter case (set&#178;), we have some fixed [[universe of discourse]] (say, consisting of all real numbers), and a __concrete set__ is a set of elements of this universe (so a set of real numbers, such as $\{5\}$, $\{ x | x \gt 2 \}$, or $\empty$).  In the former case (set&#185;), an __abstract set__ is a purely abstract concept, an unstructured (except perhaps for the [[equality relation]]) collection of unlabelled elements.  Arguably (this argument goes back at least to [[Bill Lawvere|Lawvere]]), [[Georg Cantor|Cantor]]\'s original concept of [[cardinal number]] (Kardinalzahl) was the abstraction from a concrete set to its underlying abstract set.

Here we adopt a structural approach, in which a __set__ is an abstract set, a (mostly) unstructured [[collection]].  For concrete sets, see [[subset]]; if the fixed universe of discourse is an abstract set $S$, then a concrete set will be a subset of $S$.  In material set theory (as usually conceived), the fixed universe of discourse is an abstract set (or [[proper class]]) $V$, an abstract set (internal to the theory) is an element of $V$, and a concrete set is a sufficiently [[small set|small]] subset of $V$; the concepts may be identified because $V$ comes with an [[bijection|isomorphism]] to its class of small subsets.


## What is a set?

We still need to clarify exactly what sort of collection a set is.  Although most foundations leave this unspecified, we may (perhaps circularly, and perhaps controversially) define it in various ways, as follows:

### In category theory

+-- {: .un_defn}
###### Definition

A __set__ is a [[category]] (or instead an $\infty$-[[infinity-groupoid|groupoid]] or even an $\infty$-[[infinity-category|category]]) that is [[small category|small]], [[discrete category|discrete]], and [[skeletal category|skeletal]]. (This definition needs explaination since it seems to be recursive, as "smallness" refers to what a set is.)
=--
Each of these three adjectives describes a different aspect of what makes something a 'set', and they serve different purposes, which should not be conflated.

That a set is (in the category-theoretic sense) [[discrete category|discrete]] is the most important point; nobody would call a category a 'set' merely because it is small and skeletal.  (This clause is also the reason why it makes no difference whether we start from categories, $\infty$-groupois, or $\infty$-categories; discreteness immediately limits us to $0$-[[0-groupoid|groupoids]].)  The discreteness of a set reflects its lack of internal structure; while a category may have much structure relating its objects, the only structure remaining in a discrete category is whether any two given objects are [[isomorphism|isomorphic]] (and the fact that isomorphism is an [[equivalence relation]]); if (and only if) they are, then they are considered __[[equality|equal]]__ as elements of the set.

That a set is [[small category|small]] allows there to be a collection of 'all' sets; this collection is not itself small, but we still have a [[large category]] of all sets, [[Set]].  A category that is merely discrete and skeletal may be called a __[[class]]__ instead.  But notice that the difference between a set and a class is a rather technical one; a class is just like a set, only (possibly) larger.  Indeed, not everyone would agree with the requirement that a set must be small; although that is probably the most common way of talking to deal with size issues, it is not the only way.  Another way, used by no less an authority than _[[Categories Work]]_, is to posit the existence of a strongly [[inaccessible cardinal]] $\kappa$ and define a __[[small set]]__ to be a set whose [[cardinality]] is less than $\kappa$.

That a set is [[skeletal category|skeletal]] is arguably the least important requirement; in fact, it is 'evil' in the technical sense of violating the [[principle of equivalence]].  A category that is merely small and discrete may be called a __[[setoid]]__ instead.  However, if you forbid yourself from referring to [[equality]] of elements of the setoid (which are the objects of the small discrete category) --- or, equivalently, interpret "equality" to mean "isomorphism" therein --- then you cannot distinguish the setoid from a set; each is merely a (small) collection of elements with an equivalence relation (called 'equivalence' in the setoid and 'equality' in the set, in both cases corresponding to isomorphism in a small discrete category).  While [[size issues]] are real and cannot be ignored completely, it is possible to adopt foundations in which the issue of skeletality simply does not appear.


### In homotopy type theory {#InHoTT}

As [[homotopy type theory]] may be viewed as a theory of $\infty$-[[infinity-groupoid|groupoids]], it falls under the preceding section; but since the language of HoTT is important to learn, let us look at it explicitly:
+-- {: .num_defn}
###### Definition

A **set** is a [[type]] in which there is an operation connecting any two parallel [[identity type|paths]] by a 2-path:

    Definition is_set A := forall (x y : A) (p q : x == y), p == q

(There are numerous other equivalent definitions; see [[h-set]].)
=--
Because this operation is defined internally, it acts on paths as well as points and implies that, for any two points of $A$, the [[identity type|type of paths]] between them is [[contractible space|contractible]] as soon as it is [[inhabited]].

Regarding types as [[∞-groupoids]], this definition takes care only of the discreteness requirement.  Regarding smallness, HoTT is usually formulated in [[Martin-Löf type theory]] with [[universes]] ([[type of types]]).  If we have chosen one particular universe as the universe of "small" things, then "setness" could be restricted to types belonging to that universe.

Finally, skeletality is mostly meaningless in HoTT because paths are the only notion of (propositional) [[equality]] which we have to reason with.  (There is also the notion of "definitional" equality, but as we cannot assert or prove statements of the form "$x$ and $y$ are definitionally equal" inside the theory, this is mostly not relevant for the purposes of setness.)


## Related concepts

* [[Set]]

* [[Bishop set]], [[setoid]]

* [[definable set]], [[constructible set]]

* [[recursive subset]]

* [[finite set]], [[hereditarily finite set]]

[[!include homotopy n-types - table]]


## References

### General

Formalization of sets in [[homotopy type theory]] (via [[h-sets]]) is discussed in 

* [[Egbert Rijke]], [[Bas Spitters]], _Sets in homotopy type theory_ ([arXiv:1305.3835](http://arxiv.org/abs/1305.3835))


### History

An early definition of "set" appears in

* Bernard Bolzano, _Paradoxien des Unendlichen_ (1847)

where in section 4 it says in translation 

> There are wholes which, although they contain the same parts A, B, C, D, ..., nevertheless present themselves as different when seen from our point of view or conception (this kind of difference we call 'essential'), e.g. a complete and a broken glass viewed as a drinking vessel.  [...]  A whole whose basic conception renders the arrangement of its parts a matter of indifference (and whose rearrangement therefore changes nothing essential from our point of view, if only that changes), I call a set.


[[!redirects set]]
[[!redirects sets]]

[[!redirects abstract set]]
[[!redirects abstract sets]]
