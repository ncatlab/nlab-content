
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
* table of contentshttps://ncatlab.org/nlab/edit/equivalence+of+categories
{: toc}

## Idea

The concept of _equivalence of categories_ is the correct [[category theory|category theoretic]] notion of "sameness" of [[categories]]. 

Concretely, an equivalence between two categories is a pair of [[functors]] between them which are [[inverse]] to each other _up to_ [[natural isomorphism]] of functors ([[inverse functors]]).

This is like an [[isomorphism]], but weakened such as to accomodate for the fact that the correct ambient context for categories is not iself a 1-category, but is the [[2-category]] [[Cat]] of all categories. Hence abstractly an equivalence of categories is just the special case of an [[equivalence in a 2-category]] specialized to [[Cat]].

If some foundational fine print is taken care of, then a functor exhibits an equivalence of categories precisely if it is both [[essentially surjective functor|essentially surjective]] and [[fully faithful functor|fully faithful]]. This is true in [[classical mathematics]] if the [[axiom of choice]] is assumed. It remains true non-classically, say for [[internal categories]], if the concept of functor is suitably adapted ("[[anafunctors]]"), or the concept of essentially surjective is suitably adapted ("[[split essentially surjective]]").

From the point of view of [[logic]] one may say that two [[categories]] are _equivalent_ if they have the same [[properties]] &#8212; although this only applies (by definition) to properties that obey the _[[principle of equivalence]]_.  

Just as equivalence of categories is the generalization of [[isomorphism]] of [[sets]] from sets to categories, so the concept generalizes further
to [[higher category theory|higher categories]] (see e.g. _[[equivalence of 2-categories]]_, _[[equivalence of (∞,1)-categories]]_) and ultimately to equivalence of $\infty$-[[infinity-category|categories]].


## Definitions

+-- {: .num_defn #EquivalenceViaInverseFunctor}
###### Definition

An **equivalence** between two [[categories]] $\mathcal{C}$ and $\mathcal{D}$ is an [[equivalence in a 2-category|equivalence in the 2-category]] [[Cat]] of all [[categories]], hence a pair of [[inverse functors]], hence it is

1. a pair of [[functors]] 

   $$
     \mathcal{C} 
       \underoverset
         {\underset{\phantom{AA}F \phantom{AA}}{\longrightarrow}}
         {\overset{\phantom{AA}G\phantom{AA}}{\longleftarrow}}
         {}
     \mathcal{D},
   $$

1. [[natural isomorphisms]]

   $$
     F \circ G \cong Id_{\mathcal{D}}
   $$

   and 

   $$
     G \circ F \cong Id_{\mathcal{C}}
     \,.
   $$

This is called an **[[adjoint equivalence]]** if the natural isomorphisms above satisfy the [[triangle identities]], thus exhibiting $F$ and $G$ as a pair of [[adjoint functors]].

Two categories are called **equivalent** if there exists an equivalence between them.

=--

+-- {: .num_prop #ViaSplitEssentiallySurjectiveAndFullyFaithful}
###### Proposition

Let $F \colon \mathcal{C} \to \mathcal{D}$ be a [[functor]]. Then the following are equivalent:

1. $F$ is part of an equivalence of categories in the sense of def. \ref{EquivalenceViaInverseFunctor}

2. $F$ is 

   1. a [[split essentially surjective functor]] and

   2. a [[fully faithful functor]].
=--

\begin{proof}
This proof is from the [[HoTT book]], and is set in the context of [[homotopy type theory]]. The categories here are what the HoTT book calls "precategories", i.e. not [[univalent categories]]:

Suppose $F$ is an equivalence of categories with $G,\eta,\epsilon$ specified. Then we have the function

$$
\begin{aligned}
  hom_B(F a, F b) &\to hom_A(a,b), \\
  g &\mapsto \eta_b^{-1}\circ G(g) \circ \eta_a.
\end{aligned}
$$

For $f:hom_A(a,b)$, we have

$$\eta_b^{-1} \circ G(F(f)) \circ \eta_a = \eta_b^{-1} \circ \eta_b \circ f = f$$
while for $g: hom_B(F a, F b)$ we have

$$
  \begin{aligned}
    F(\eta_b^{-1} \circ G(g) \circ \eta_a) &= F(\eta_b^{-1}) \circ F(G(g)) \circ F(\eta_a) \\
    &= \epsilon_{F b} \circ F(G(g)) \circ F(\eta_a) \\
    &= g \circ \epsilon_{F a} \circ F(\eta_a) \\
    &= g
  \end{aligned}
$$

using [[natural transformation|naturality]] of $\epsilon$, and the triangle identities twice. Thus, $F_{a,b}$ is an equivalence, so $F$ is [[fully faithful]]. Finally, for any $b:B$, we have $G b : A$ and $\epsilon_b : F G b \cong b$.

On the other hand, suppose $F$ is [[fully faithful]] and [[split essentially surjective]]. Define $G_0:B_0\to A_0$ by sending $b:B$ to the $a:A$ given by the specified essential splitting, and write $\epsilon_b$ for the likewise specified [[isomorphism]] $F G b \cong b$.

Now for any $g: hom_B(b,b')$, define $G(g): hom_A(G b, G b')$ to be the unique morphism such that $F(G(g))=(\epsilon_{b'})^{-1} \circ g \circ \epsilon_b$ which exists since $F$ is [[fully faithful]]. Finally for $a:A$ define $\eta_a : hom_A(a,G F a)$ to be the unique morphism such that $F \eta_a = \epsilon^{-1}_{F a}$. It is easy to verify that $G$ is a functor and that $(G,\eta \epsilon)$ exhibit $F$ as an equivalence of categories.

We clearly recover the same function $G_0 : B_0 \to A_0$. For the action of $F$ on hom-sets, we must show that for $g:hom_B (b,b')$, $G(g)$ is the necessarily unique morphism such taht $F(G(g))=(\epsilon_{b'})^{-1} \circ g \circ \epsilon_b$.

But this holds by [[natural transformation|naturality]] of $\epsilon$. Then we show $(2) \to (1) \to (2)$ gives the same data hence $(1)\simeq (2)$. 
\end{proof}

## Variants {#Variants}

We discuss some possible variants of the definition of equivalence of categories, each of which comes naturally from a different view of [[Cat]].

The first, _isomorphism_, comes from viewing $Cat$ as a mere [[1-category]]; it is too strong and is really only of interest for [[strict categories]].  The next, _strong equivalence_, comes from viewing $Cat$ as a [[strict 2-category]]; it is the most common definition given and is correct if and only if the [[axiom of choice]] holds.  The next definition, _weak equivalence_, comes from viewing $Cat$ as a [[model category]]; it is correct with or without choice and is about as simple to define as strong equivalence. The fourth, _anaequivalence_, comes from viewing $Cat$ as a [[bicategory]] that is not (without the axiom of choice) equivalent (as a bicategory!) to the strict $2$-category that defines strong equivalence; it is also always correct.

It is also possible to define 'category' in such a way that only a correct definition can be stated, but here we use the usual algebraic definitions of category, [[functor]], and [[natural isomorphism]].

### Isomorphism {#Isomorphism}

Two [[strict categories]] $C$ and $D$ are __isomorphic__ if there exist [[strict functors]] $F\colon C \to D$ and $G\colon D \to C$ such that $F G$ and $G F$ are each [[equality|equal]] to the appropriate [[identity functor]].  In this case, we say that $F$ is an __isomorphism__ from $C$ to $D$ (so $G$ is an isomorphism from $D$ to $C$) and call the pair $(F,G)$ an __isomorphism__ between $C$ and $D$.  The functor $G$ is called the __strict inverse__ of $F$ (so $F$ is the strict inverse of $G$).

If you think of $Cat$ as the category of (strict) categories and functors, then this is the usual notion of [[isomorphism]] in a category.  This is the most obvious notion of equivalence of categories and the first to be considered, but it is simply too strong for the purposes to which [[category theory]] is put.  For example, here are some basic and important equivalences of categories that are not isomorphisms:

* Let $C$ be the category of [[pointed sets]], and let $D$ be the category of sets and [[partial functions]].  The functor $F:C\to D$ takes a pointed set to its subset of non-basepoint elements, and a pointed function to the induced partial function on these (which is defined on those elements not sent to the basepoint).  See the section "The category of sets and partial functions" in [[partial function]] for this equivalence.

* Let $C$ be the category of finite-dimensional [[vector spaces]] over a [[field]] $k$, and let $D$ be the category whose objects are [[natural numbers]] and whose morphisms $n\to m$ are $m\times n$ matrices of elements of $k$ (which is equivalently the full subcategory of $C$ spanned by the specific vector spaces $k^n$).  Note in particular that here $D$ is a [[small category]], while $C$ is not (though it is [[essentially small category|essentially small]], being equivalent to $D$).


### Strong equivalence {#StrongEquivalence}

Two [[strict categories]] $C$ and $D$ are __strongly equivalent__ if there exist strict functors $F\colon C \to D$ and $G\colon D \to C$ such that $F G$ and $G F$ are each [[natural isomorphism|naturally isomorphic]] ([[isomorphism|isomorphic]] in the relevant [[functor category]]) to the appropriate [[identity functor]].  In this case, we say that $F$ is a __strong equivalence__ from $C$ to $D$ (so $G$ is a strong equivalence from $D$ to $C$).  The functor $G$ is called a __weak inverse__ of $F$ (so $F$ is a weak inverse of $G$).

Note that an isomorphism is precisely a strong equivalence in which the natural isomorphisms are [[identity natural transformation]]s.

If you think of $Cat$ as the [[strict 2-category]] of (strict) categories, functors, and [[natural transformation]]s, then this is the usual notion of [[equivalence]] in a $2$-[[2-category|category]].  This is the first 'correct' definition of equivalence to be considered and the one most often seen today; it is only correct using the axiom of choice.

+-- {: .query}
If possible, use or modify the counterexample to isomorphism to show how choice follows if strong equivalence is assumed correct.
=--


### Weak equivalence {#WeakEquivalence}

Two categories $C$ and $D$ are __weakly equivalent__ if there exist a category $X$ and functors $F\colon X \to D$ and $G\colon X \to C$ that are [[essentially surjective functor|essentially surjective]] and [[full and faithful functor|fully faithful]].  In this case, we say that $F$ is a __weak equivalence__ from $X$ to $D$ (so $G$ is a weak equivalence from $X$ to $C$) and call the [[span]] $(X,F,G)$ a __weak equivalence__ between $C$ and $D$.  (It is not entirely trivial to check that such spans can be composed, but they can be.)

A strict functor with a weak inverse is necessarily essentially surjective and fully faithful; the converse is equivalent to the axiom of choice.  Thus any strong equivalence becomes a weak equivalence in which $X$ is taken to be either $C$ or $D$ (or even built symmetrically out of $C$ and $D$ if you\'re so inclined); a weak equivalence becomes a strong equivalence using the axiom of choice to find weak inverses and composing across $X$.

If you think of $Cat$ as the model category of categories and functors with the [[canonical model structure]], then this is the usual notion of [[weak equivalence]] in a model category.


### Anaequivalence {#Anaequivalence}

Two categories $C$ and $D$ are __anaequivalent__ if there exist [[anafunctors]] $F\colon C \to D$ and $G\colon D \to C$ such that $F G$ and $G F$ are each ananaturally isomorphic (isomorphic in the relevant [[anafunctor category]]) to the appropriate [[identity anafunctor]].  In this case, we say that $F$ is an __anaequivalence__ from $C$ to $D$ (so $G$ is an anaequivalence from $D$ to $C$).  The functor $G$ is called an __anainverse__ of $F$ (so $F$ is an anainverse of $G$). See also _[[weak equivalence of internal categories]]_.

Any strict functor is an anafunctor, so any strong equivalence is an anaequivalence.  Using the axiom of choice, any anafunctor is [[ananatural isomorphism|ananaturally isomorphic]] to a strict functor, so any anaequivalence defines a strong equivalence.  Using the definition of an anafunctor as an appropriate span of strict functors, a weak equivalence defines two anafunctors which form an anaequivalence; conversely, either anafunctor in an anaequivalence is (as a span) a weak equivalence.

If you think of $Cat$ as the [[bicategory]] of categories, anafunctors, and [[ananatural transformation]]s, then this is the usual notion of [[equivalence]] in a $2$-category.  It\'s fairly straightforward to turn any discussion of functors and strong equivalences in a context where the axiom of choice is assumed into a discussion of anafunctors and anaequivalences in a more general context.

We can also regard the $2$-category $Cat$ above as obtained from the $2$-category $Str Cat$ of strict categories, strict functors, and natural transformations by formally inverting the weak equivalences as in [[homotopy theory]].

### Fully faithful essentially surjective functors

Finally, there are [[fully faithful]] and [[essentially surjective functors]]. However, while in general, these are not the same as equivalences in all mathematical foundations, they are the same under certain restrictions:

+-- {: .num_prop #ViaEssentiallySurjectiveAndFullyFaithful}
###### Proposition

Assume the ambient context is one of the following:

* [[classical mathematics]] with the [[axiom of choice]];

* [[constructive mathematics|constructive]] or [[internal category|internal]] category theory with "functor" meaning _[[anafunctor]]_;

* [[higher-level foundations]] with "category" meaning [[univalent category]].

Let $F \colon \mathcal{C} \to \mathcal{D}$ be a [[functor]]. Then the following are equivalent:

1. $F$ is part of an equivalence of categories in the sense of def. \ref{EquivalenceViaInverseFunctor}

2. $F$ is 

   1. an [[essentially surjective functor]] and

   2. a [[fully faithful functor]].

=--

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

### An example of a non-adjoint equivalence

Identify a group $H$ with its [[delooping]]. One can check the following:

* Any equivalence $F : H \leftrightarrows H : G$ of a group with itself comprises two automorphisms $F, G$, such that $F G$ and $G F$ are inner. The unit and counit are the group elements $g_{\rho}$ such that $GF(k) = g_{\rho} k g_{\rho}^{-1}$ and  $g_{\sigma}$ such that $FG(k) = g_{\sigma}^{-1} k g_{\sigma}$ for any $k \in H$.

* Any equivalence of $H$ with itself where $F$ and $G$ are themselves also inner is an adjoint equivalence.

* If $H$ has trivial center, then any equivalence of $H$ with itself is an adjoint equivalence.

* To obtain a non-adjoint equivalence, we therefore need a group $H$ with nontrivial center and nontrivial outer automorphisms, such that we can pick two whose products are inner.

* So take $H = K$ the Klein 4-group. This is a product of abelian groups, so abelian, so is its own center. In fact, it's $\mathbb{Z}/2 \mathbb{Z} \times \mathbb{Z} / 2 \mathbb{Z}$, so let $F = G$ the automorphism which interchanges coordinates. $FG = GF = \operatorname{id}_{K}$, which is given by conjugation by any element.

* If this were adjoint, the triangle equality for $F$ will stipulate that $F(g_{\rho}) = g_{\sigma}^{-1}$. We can pick $g_{\rho}$ and $g_{\sigma}$ to break this. For example, let $g_{\rho}$ be $(1,1)$ and let $g_{\sigma}$ be $(0,1)$.

This is a special case of the fact that, given a non-adjoint equivalence, you can always replace its unit with another unit (which determines the counit) to improve the equivalence to an [[adjoint equivalence]].

## In higher categories

All of the above types of equivalence make sense for $n$-[[n-category|categories]] and $\infty$-categories defined using an [[algebraic definition of higher category]]; again, it is the weak notion that is usually wanted.  When using a [[geometric definition of higher category]], often isomorphism cannot even be written down, so equivalence comes more naturally.

In particular, one expects (although a proof depends on the exact definition and hasn\'t always been done) that in any $(n+1)$-category of $n$-categories, every [[equivalence]] (in the sense of an $(n+1)$-category) will be essentially $k$-[[k-surjective functor|surjective]] for all $0\le k\le n+1$; this is the $n$-version of "full, faithful, and essentially surjective."  The converse should be true assuming that

*  we have an axiom of choice and use weak (pseudo) $n$-[[n-functor|functors]], or
*  we use $n$-[[n-anafunctor|anafunctors]] (which are automatically weak).

If we use too strict a notion of $n$-functor, then we will not get the correct notion of equivalence; if we use weak $n$-functors but not anafunctors, then we will get the correct notion of equivalence only if the axiom of choice holds, although again this can be corrected by moving to a span.  Note that even strict $n$-categories need weak $n$-functors to get the correct notion of equivalence between them!

For example, assuming choice, a [[strict 2-functor]] between strict $2$-categories is an equivalence in $Bicat$ if and only if it is essentially (up to equivalence) surjective on objects, locally essentially surjective, and [[locally fully faithful 2-functor|locally fully faithful]]. However, its weak inverse may not be a _strict_ $2$-functor, and even if it is, the equivalence transformations need not be strictly $2$-natural.  Thus, it need not be an equivalence in the [[strict 3-category]] $Str 2 Cat$ of $2$-categories, strict $2$-functors, and strict $2$-natural transformations, or even in the [[semi-strict 3-category]] $Gray$ of strict $2$-categories, strict $2$-functors, and pseudonatural transformations.

As with $Cat$, we can recover $Bicat$ as a [[full subcategory|full]] sub[[tricategory]] of $Gray$ by formally inverting all such weak equivalences.  Note that even with the axiom of choice, $Bicat$ is *not* equivalent (as a tricategory) to $Gray$, even though by the coherence theorem for tricategories it is equivalent to *some* $Gray$-category; see [here](http://arxiv.org/abs/math/0612299).


## Related concepts

[[!include properties of functors -- contents]]


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
