
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Category theory
+-- {: .hide}
[[!include category theory - contents]]
=--
#### Equality and Equivalence
+--{: .hide}
[[!include equality and equivalence - contents]]
=--
=--
=--

# Equivalence of categories
* table of contents
{: toc}

## Idea

Two [[categories]] are _equivalent_ if they have the same properties &#8212;although this only applies (by definition) to properties that obey the _[[principle of equivalence]]_.  An _equivalence_ between categories is a [[functor]] that realises this.

If one works with [[internal categories]] or doubts the [[axiom of choice]], some care must be taken in the definition.

Equivalence of categories generalises to [[higher category theory|higher categories]] and ultimately to equivalence of $\infty$-[[infinity-category|categories]].


## Definitions

+-- {: .num_defn}
###### Definition

An **equivalence** between two categories $C$ and $D$ is a pair of [[functor]]s 

$$
  C \stackrel{\overset{G}{\leftarrow}}{\underset{F}{\to}} D
$$

such that there are [[natural isomorphism]]s 

$$
  F \circ G \cong Id_D
$$

and 

$$
  G \circ F \cong Id_C
  \,.
$$
=--

This is called an **[[adjoint equivalence]]** if in addition $F$ and $G$ form a pair of [[adjoint functor]]s.

+-- {: .num_defn}
###### Definition

Two categories are called **equivalent** if there exists an equivalence between them.
=--

+-- {: .num_prop}
###### Proposition

A [[functor]] $F\colon C \to D$ is part of an equivalence precisely if 

* it is an [[essentially surjective functor]]

* and it is a [[full and faithful functor]].
=--

+-- {: .num_remark}
###### Remark

The definitions above work regardless of [[foundations]], if the term 'functor' is interpreted in an appropriate way.  For details, see the discussion of [Variants](#Variants) below.
=--

+-- {: .num_lemma}
###### Observation

Regarded as [[object]]s in the [[2-category]] [[Cat]], two categories are equivalent precisely if there is an [[equivalence in a 2-category]] between them.
=--


## Variants {#Variants}

We discuss some possible variants of the definition of equivalence of categories, each of which comes naturally from a different view of [[Cat]].

The first, _isomorphism_, comes from viewing $Cat$ as a mere category; it is too strong and is really only of historical interest.  The next, _strong equivalence_, comes from viewing $Cat$ as a [[strict 2-category]]; it is the most common definition given and is correct if and only if the [[axiom of choice]] holds.  The next definition, _weak equivalence_, comes from viewing $Cat$ as a [[model category]]; it is correct with or without choice and is about as simple to define as strong equivalence. The last, _anaequivalence_, comes from viewing $Cat$ as a [[bicategory]] that is not (without the axiom of choice) equivalent (as a bicategory!) to the strict $2$-category that defines strong equivalence; it is also always correct.

It\'s also possible to define 'category' in such a way that only a correct definition can be stated, but here we use the usual algebraic definitions of category, [[functor]], and [[natural isomorphism]].


### Isomorphism {#Isomorphism}

Two [[strict categories]] $C$ and $D$ are __isomorphic__ if there exist [[strict functors]] $F\colon C \to D$ and $G\colon D \to C$ such that $F G$ and $G F$ are each [[equality|equal]] to the appropriate [[identity functor]].  In this case, we say that $F$ is an __isomorphism__ from $C$ to $D$ (so $G$ is an isomorphism from $D$ to $C$) and call the pair $(F,G)$ an __isomorphism__ between $C$ and $D$.  The functor $G$ is called the __strict inverse__ of $F$ (so $F$ is the strict inverse of $G$).

If you think of $Cat$ as the category of (strict) categories and functors, then this is the usual notion of [[isomorphism]] in a category.  This is the most obvious notion of equivalence of categories and the first to be considered, but it is simply too strong for the purposes to which [[category theory]] is put.

+-- {: .query}
Give an intuitively clear counterexample here.
=--


### Strong equivalence {#StrongEquivalence}

Two strict categories $C$ and $D$ are __strongly equivalent__ if there exist strict functors $F\colon C \to D$ and $G\colon D \to C$ such that $F G$ and $G F$ are each naturally isomorphic (isomorphic in the relevant [[functor category]]) to the appropriate identity functor.  In this case, we say that $F$ is a __strong equivalence__ from $C$ to $D$ (so $G$ is a strong equivalence from $D$ to $C$).  The functor $G$ is called a __weak inverse__ of $F$ (so $F$ is a weak inverse of $G$).

Note that an isomorphism is precisely a strong equivalence in which the natural isomorphisms are [[identity natural transformation]]s.

If you think of $Cat$ as the [[strict 2-category]] of (strict) categories, functors, and [[natural transformation]]s, then this is the usual notion of [[equivalence]] in a $2$-[[2-category|category]].  This is the first 'correct' definition of equivalence to be considered and the one most often seen today; it is only correct using the axiom of choice.

+-- {: .query}
If possible, use or modify the counterexample to isomorphism to show how choice follows if strong equivalence is assumed correct.
=--


### Weak equivalence {#WeakEquivalence}

Two strict categories $C$ and $D$ are __weakly equivalent__ if there exist a category $X$ and strict functors $F\colon X \to D$ and $G\colon X \to C$ that are [[essentially surjective functor|essentially surjective]] and [[full and faithful functor|fully faithful]].  In this case, we say that $F$ is a __weak equivalence__ from $X$ to $D$ (so $G$ is an equivalence from $X$ to $C$) and call the [[span]] $(X,F,G)$ a __weak equivalence__ between $C$ and $D$.

A functor with a weak inverse is necessarily essentially surjective and fully faithful; the converse is equivalent to the axiom of choice.  Thus any strong equivalence becomes a weak equivalence in which $X$ is taken to be either $C$ or $D$ (or even built symmetrically out of $C$ and $D$ if you\'re so inclined); a weak equivalence becomes a strong equivalence using the axiom of choice to find weak inverses and composing across $X$.

If you think of $Cat$ as the model category of categories and functors with the [[canonical model structure]], then this is the usual notion of [[weak equivalence]] in a model category.


### Anaequivalence {#Anaequivalence}

Two categories $C$ and $D$ are __anaequivalent__ if there exist [[anafunctors]] $F\colon C \to D$ and $G\colon D \to C$ such that $F G$ and $G F$ are each ananaturally isomorphic (isomorphic in the relevant [[anafunctor category]]) to the appropriate [[identity anafunctor]].  In this case, we say that $F$ is an __anaequivalence__ from $C$ to $D$ (so $G$ is an anaequivalence from $D$ to $C$).  The functor $G$ is called an __anainverse__ of $F$ (so $F$ is an anainverse of $G$). See also _[[weak equivalence of internal categories]]_.

Any strict functor is an anafunctor, so any strong equivalence is an anaequivalence.  Using the axiom of choice, any anafunctor is [[ananatural isomorphism|ananaturally isomorphic]] to a strict functor, so any anaequivalence defines a strong equivalence.  Using the definition of an anafunctor as an appropriate span of strict functors, a weak equivalence defines two anafunctors which form an anaequivalence; conversely, either anafunctor in an anaequivalence is (as a span) a weak equivalence.

If you think of $Cat$ as the [[bicategory]] of categories, anafunctors, and [[ananatural transformation]]s, then this is the usual notion of [[equivalence]] in a $2$-category.  It\'s fairly straightforward to turn any discussion of functors and strong equivalences in a context where the axiom of choice is assumed into a discussion of anafunctors and anaequivalences in a more general context.

We can also regard the $2$-category $Cat$ above as obtained from the $2$-category $Str Cat$ of categories, functors, and natural transformations using [[homotopy theory]] by "formally inverting" the weak equivalences.


### Remarks

Note that *weak* inverses go with *strong* equivalences.  The terminology isn\'t entirely inconsistent (weak inverses contrast with *strict* ones, while weak equivalences contrast with *strong* ones) but developed at different times.  The prefix 'ana&#8209;' developed last and is perfectly consistent.

If you accept the axiom of choice, then you don\'t have to worry about the different kinds of equivalence (as long as you don\'t use isomorphism).  This is not just a question of [[foundations]], however, since the axiom of choice usually fails in [[internalization|internal contexts]].

It\'s also possible to use foundations (such as [[homotopy type theory]], some other forms of [[type theory]], or [[FOLDS]]) in which isomorphism and strong equivalence are impossible to state.  In such a case, one usually drops the prefixes 'weak' and 'ana&#8209;'.  In the $n$-Lab, we prefer to remain agnostic about foundations but usually drop these prefixes as well, leaving it up to the reader to insert them if necessary.


## Adjoint equivalence

Any equivalence can be improved to an __[[adjoint equivalence]]__: a strong equivalence or anaequivalence whose natural isomorphisms satisfy the [[adjoint functor|triangle identities]].  In that case, $G$ is called [[generalized the|the]] __adjoint inverse__ of $F$ (so $F$ is the adjoint inverse of $G$).  When working in the $2$-category $Cat$, a good rule of thumb is that it is okay to consider either

*  a functor with the _property_ of being a _general_ equivalence or
*  a functor with the _structure_ of being an _adjoint_ equivalence (that is, a functor $G$ and a pair of natural isomorphisms $F G \cong 1$ and $1 \cong G F$ satisfying the triangle identities),

whereas considering

* a functor with the _structure_ of being a _general_ equivalence (that is, merely a functor $G$ and a pair of natural isomorphisms $F G \cong 1$ and $1 \cong G F$)

is fraught with peril.  For instance, an adjoint inverse is unique up to unique isomorphism (much as a strict inverse is unique up to equality), while a weak inverse or anainverse is not.  Including adjoint equivalences is also the only way to make a higher-categorical structure completely _[[algebraic definition of higher category|algebraic]]_.


## In higher categories

All of the above types of equivalence make sense for $n$-[[n-category|categories]] and $\infty$-categories defined using an [[algebraic definition of higher category]]; again, it is the weak notion that is usually wanted.  When using a [[geometric definition of higher category]], often isomorphism cannot even be written down, so equivalence comes more naturally.

In particular, one expects (although a proof depends on the exact definition and hasn\'t always been done) that in any $(n+1)$-category of $n$-categories, every [[equivalence]] (in the sense of an $(n+1)$-category) will be essentially $k$-[[k-surjective functor|surjective]] for all $0\le k\le n+1$; this is the $n$-version of "full, faithful, and essentially surjective."  The converse should be true assuming that

*  we have an axiom of choice and use weak (pseudo) $n$-[[n-functor|functors]], or
*  we use $n$-[[n-anafunctor|anafunctors]] (which are automatically weak).

If we use too strict a notion of $n$-functor, then we will not get the correct notion of equivalence; if we use weak $n$-functors but not anafunctors, then we will get the correct notion of equivalence only if the axiom of choice holds, although again this can be corrected by moving to a span.  Note that even strict $n$-categories need weak $n$-functors to get the correct notion of equivalence between them!

For example, assuming choice, a [[strict 2-functor]] between strict $2$-categories is an equivalence in $Bicat$ if and only if it is essentially (up to equivalence) surjective on objects, locally essentially surjective, and [[locally fully faithful 2-functor|locally fully faithful]]. However, its weak inverse may not be a _strict_ $2$-functor and the equivalence transformations need not be strictly 2-natural.  Thus, it need not be an equivalence in the [[strict 3-category]] $Str 2 Cat$ of 2-categories, strict 2-functors, and strict 2-natural transformations, or even in the [[semi-strict 3-category]] $Gray$ of strict 2-categories, strict 2-functors, and pseudonatural transformations.

As with $Cat$, we can recover $Bicat$ as a [[full subcategory|full]] sub[[tricategory]] of $Gray$ by formally inverting all such weak equivalences.  Note that even with the axiom of choice, $Bicat$ is *not* equivalent (as a tricategory) to $Gray$, even though by the coherence theorem for tricategories it is equivalent to *some* Gray-category; see [here](http://arxiv.org/abs/math/0612299).


## Related concepts

* [[equality]], [[isomorphism]], [[equivalence]]

* [[weak equivalence]], [[homotopy equivalence]], [[weak homotopy equivalence]]

* [[homotopy equivalence of toposes]]

* [[equivalence in an (∞,1)-category]]

* **equivalence of categories**, [[weak equivalence of internal categories]]

* [[adjoint functor]]

* [[equivalence of 2-categories]], [[2-adjunction]]

* [[equivalence of (∞,1)-categories]], [[adjoint (∞,1)-functor]]


[[!redirects equivalence of categories]]
[[!redirects equivalences of categories]]
[[!redirects equivalent category]]
[[!redirects equivalent categories]]

[[!redirects isomorphism of categories]]
[[!redirects isomorphisms of categories]]
[[!redirects isomorphic category]]
[[!redirects isomorphic categories]]

[[!redirects adjoint equivalence of categories]]
[[!redirects adjoint equivalences of categories]]

[[!redirects equivalence of n-categories]]
[[!redirects equivalences of n-categories]]
[[!redirects equivalence of infinity-categories]]
[[!redirects equivalences of infinity-categories]]
[[!redirects equivalence of higher categories]]
[[!redirects equivalences of higher categories]]

[[!redirects equivalence of groupoids]]
[[!redirects equivalences of groupoids]]
[[!redirects equivalent groupoid]]
[[!redirects equivalent groupoids]]

[[!redirects isomorphism of groupoids]]
[[!redirects isomorphisms of groupoids]]
[[!redirects isomorphic groupoid]]
[[!redirects isomorphic groupoids]]

[[!redirects adjoint equivalence of groupoids]]
[[!redirects adjoint equivalences of groupoids]]

[[!redirects equivalence of n-groupoids]]
[[!redirects equivalences of n-groupoids]]
[[!redirects equivalence of infinity-groupoids]]
[[!redirects equivalences of infinity-groupoids]]
[[!redirects equivalence of higher groupoids]]
[[!redirects equivalences of higher groupoids]]
