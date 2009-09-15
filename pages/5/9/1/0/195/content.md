<div class="rightHandSide toc">
[[!include category theory - contents]]
</div>


The concept of _set_ appears in several different guises in [[mathematics]], and particularly in [[category theory]].


## What should a set be?

It is common to use [[foundations of mathematics]] in which 'set' is an undefined term; this is [[set theory]] as a foundation.  In a pure material set theory like **[[ZFC]]**, every object is a set.  Even in a structural approach such as **[[ETCS]]**, it is common for every object to be a [[structured set]] in some way or another.  Even if sets are not at the bottom of your foundations, still they are probably close.

Material set theory conflates two notions of sets, which were elegantly (but not first) described by [[Mathieu Dupont]] in [a blog post](http://math.breckes.org/2009/03/the-two-meanings-of-the-word-%E2%80%9Cset%E2%80%9D-in-mathematics/) as 'set&#185;' and 'set&#178;'.  In the latter case (set&#178;), we have some fixed universe of discourse (perhaps consisting of all real numbers), and a 'set' is a set of elements of this universe (so a set of real numbers, such as $\{5\}$, $\{ x | x \gt 2 \}$, or $\empty$).  In the former case (set&#185;), a 'set' is a purely abstract concept, an unstructured (except perhaps for an [[equality relation]]) collection of unlabelled elements.  Arguably (this argument goes back at least to [[Lawvere]]), Cantor\'s original concept of [[cardinal number]] (Kardinalzahl) was the abstraction from a set&#178; to its underlying set&#185;.

Here we adopt a structural approach, in which a __set__ is a set&#185;, a (mostly) unstructured [[collection]].  For set&#178;, see [[subset]]; if the fixed universe of discourse is a set $S$, then a set&#178; will be a subset of $S$.


## What is a set?

We still need to clarify exactly what sort of collection a set is.  Although most foundations leave this unspecified, we may (probably circularly, and perhaps controversially) define it as follows:
+-- {: .un_defn}
###### Definition

A __set__ is a [[category]] that is [[small category|small]], [[discrete category|discrete]], and [[skeletal category|skeletal]].
=--
Each of these three adjectives describes a different aspect of what makes something a 'set', and they serve different purposes, which should not be conflated.

That a set is (in the category-theoretic sense) discrete is the most important point; nobody would call a category a 'set' merely because it is small and skeletal.  The discreteness of a set reflects its lack of internal structure; while a category may have much structure relating its objects, the only structure remaining in a discrete category is whether any two given objects are [[isomorphism|isomorphic]] (and the fact that isomorphism is an [[equivalence relation]]); if (and only if) they are, then they are considered _[[equality|equal]]_ as elements of the set.

That a set is small allows there to be a collection of 'all' sets; this collection is not itself small, but we still have a [[large category]] of all sets, [[Set]].  A category that is merely discrete and skeletal may be called a _[[class]]_ instead.  But notice that the difference between a set and a class is a rather technical one; a class is just like a set, only (possibly) larger.  Indeed, not everyone would agree with the requirement that a set must be small; although that is probably the most common way of talking to deal with size issues, it is not the only way.  Another way, used by no less an authority than _[[Categories Work]]_, it to posit the existence of a strongly [[inaccessible cardinal]] $\kappa$ and define a _small set_ to be a set whose cardinality is less than $\kappa$.

That a set is skeletal is arguably the least important requirement; in fact, it is [[evil]] in a technical sense.  A category that is merely small and discrete may be called a _[[setoid]]_ instead.  However, if you forbid yourself from referring to [[equality]] of elements of the setoid (which are the objects of the small discrete category), then you cannot distinguish the setoid from a set; each is merely a (small) collection of elements with an equivalence relation (called 'equivalence' in the setoid and 'equality' in the set, in both cases corresponding to isomorphism in a small discrete category).  While size issues are real and cannot be ignored completely, it is possible to adopt foundations (either [[type theory|type-theoretic]] or $\infty$-[[infinity-groupoid|groupoid-theoretic]]) in which this issue does not appear.


[[!redirects sets]]