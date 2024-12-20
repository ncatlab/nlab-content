
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Category theory
+--{: .hide}
[[!include category theory - contents]]
=--
#### 2-Category theory
+--{: .hide}
[[!include 2-category theory - contents]]
=--
#### Equality and Equivalence
+--{: .hide}
[[!include equality and equivalence - contents]]
=--
=--
=--



# Adjoint equivalences
* table of contents
{: toc}

## Idea

In [[category theory]], the notion of *adjoint equivalence* is a more "coherent" or "structured" notion of [[equivalence of categories]], in which the [[2-morphism|2-]][[isomorphisms]] relating composites to identities are required to satisfy [[coherence laws]] (namely the [[zigzag identities]] for an [[adjunction]]).

## Definition

An **adjoint equivalence** between [[categories]] is a pair of [[adjoint functors]] $f\dashv g$ in which the [[unit of an adjunction|unit]] $\eta$ and [[unit of an adjunction|counit]] $\varepsilon$ are [[natural isomorphisms]].  It follows in particular that each of $f,g$ constitute an [[equivalence of categories]].

There is an identical definition internal to any [[2-category]], which reproduces the above notion when applied in [[Cat]].

## Properties

We work in any 2-category.  First, we observe:

+-- {: .num_lemma}
###### Lemma
If $(f,g,\eta,\varepsilon)$ is an adjoint equivalence, then so is $(g,f,\varepsilon^{-1},\eta^{-1})$.
=--

Therefore, in an adjoint equivalence, each functor is both the [[left adjoint]]  and the [[right adjoint]] of the other (i.e. it is an [[ambidextrous adjunction]]).

The definition as given above is also redundant:

+-- {: .num_lemma}
###### Lemma
If $(f,g,\eta,\varepsilon)$ is any equivalence, then it satisfies one [[zigzag identity]] iff it satisfies the other.
=--


+-- {: .proof}
###### Proof


Using [[string diagram]] notation, with strings progressing up the page and 1-morphisms progressing from left to right, we can draw the data of an equivalence (omitting labels for the regions denoting objects) as follows:

[[!include equivalence data - SVG]]

If we now suppose that one zigzag identity holds:

[[!include zigzag identity 1 - SVG]]

then we can verify the other as follows.  (The first step uses the inverse of the first zigzag identity.)

[[!include zigzag identity 1 implies 2 - SVG]]

=--

Furthermore, although an adjoint equivalence is a "stronger" or "more structured" notion than a mere equivalence, the property of "being adjoint equivalent" is no stronger a condition than "being equivalent," since every equivalence may be refined to an adjoint equivalence by modifying one of the natural isomorphisms involved.  More specifically:

+--{: .num_theorem}
###### Theorem
If $f\colon X\to Y$ is a morphism which is an equivalence, then given any morphism $g\colon Y\to X$ and any isomorphism $\eta\colon 1 \cong g f$, there exists a unique 2-isomorphism $\varepsilon\colon f g \cong 1$ such that $(f,g,\eta,\varepsilon)$ is an adjoint equivalence.
=--

+--{: .proof}
###### Proof

Since $f$ is an equivalence, there exists a $g'$ and isomorphisms $f g' \cong 1$ and $1\cong g' f$.  However, we also have $g \cong g f g' \cong g'$, so the isomorphism $f g' \cong 1$ also induces an isomorphism $f g\cong 1$, which we denote $\xi$.  Now $\eta$ and $\xi$ may not satisfy the zigzag identities, but if we define $\varepsilon$ as follows:
$$
f g
\xrightarrow{f g \xi^{-1}} f g f g
\xrightarrow{f \eta^{-1} g} f g
\xrightarrow{\xi} 1
$$
then we can verify, using string diagram notation as above, that $\varepsilon$ satisfies one zigzag identity, and hence (by the previous lemma) also the other:

[[!include adjointification zigzag identity - SVG]]

Finally, if $\varepsilon'\colon f g \to 1$ is any other isomorphism satisfying the zigzag identities with $\eta$, then we have
$$\varepsilon' = \varepsilon' . (\varepsilon f g) . (f \eta g) = 
\varepsilon . (f g \varepsilon') . (f \eta g) = \varepsilon$$
using the [[interchange law]] and two zigzag identities.  This shows uniqueness.

=--

In [[Categories Work]], IV.4, there is a different proof of the weaker fact that if a [[functor]] $f$ is part of an equivalence, then it is part of an adjoint equivalence.  This proof is given in [[Cat]], but can be applied representably to any 2-category.

Since adjoints are unique up to unique isomorphism when they exist, it follows that any adjunction involving one functor which is an equivalence must be an adjoint equivalence.  Therefore, for a fixed morphism $f$, the "category of adjoint equivalence data $(f,g,\eta,\varepsilon)$" is either empty (if $f$ is not an equivalence) or equivalent to the [[terminal category]] (if $f$ is an equivalence).  In other words, it is a [[(-1)-category]].

Therefore, in any 2-category, the following data are all equivalent (i.e. form equivalent categories):

* A morphism $f\colon X\to Y$ with the [[property]] of being an equivalence.

* A morphism $f\colon X\to Y$ with the *structure* of a morphism $g\colon Y \to X$ and an isomorphism $\eta\colon 1 \cong g f$, together with the *property* that there exists an isomorphism $f g \cong 1$.

* A morphism $f$ together with the structure of adjoint equivalence data $(f,g,\eta,\varepsilon)$.

In other words, adjoint equivalences are the way to make the property of "being an equivalence" completely into "algebraic" structure.  However, they are *not* equivalent to the category of the following data:

* A morphism $f$ together with the structure of a morphism $g\colon Y \to X$ and arbitrary isomorphisms $\eta\colon 1 \cong g f$ and $\varepsilon\colon f g \cong 1$.

## Applications

### Intervals in homotopy theory

One instance of the usefulness of adjoint equivalences is that the "[[walking structure|walking]] adjoint equivalence" 2-category is equivalent to the [[point]].  Thus, it can be used as an [[interval object]] in $2Cat$, and in fact it is one of the generating cofibrations for the [[canonical model structure|canonical (Lack) model structure]] on $2Cat$.  This is not true of the "walking non-adjoint equivalence."

### Defining tricategories

The original definition of [[tricategory]] by Gordon-Power-Street involved coherence 2-morphisms with the property of being equivalences in the relevant hom-bicategories.  This is fine for most purposes, but for others it is insufficient, such as the following.

* Since "being an equivalence" is not algebraic structure, the GPS definition of tricategory, taken literally, is not an algebraic structure.  In particular, it is not [[monadic functor|monadic]] over 3-[[globular sets]], nor is it the algebras for a [[globular operad]].  Such monadicity is important if one wants to state [[coherence theorems]] as properties of [[free object|free]] structures.

* The definition of 3-functors and higher [[transfors]] between tricategories include data and axioms that involve composites incorporating not just the coherence equivalences, but their pseudo-inverses.  Therefore, strictly speaking these definitions are not well-defined unless the definition of tricategory comes with chosen pseudo-inverses for these coherence equivalences---in which case one should certainly also choose full adjoint equivalence data in order that the space of choices be contractible.

These problems are, of course, easy to remedy by simply requiring adjoint equivalence data rather than merely single equivalence morphisms.  This change was first written down by Gurski.

### Cartesian closed 2-categories

In a [[cartesian closed category]] with [[equalizers]], for any two objects $X$ and $Y$ one can construct the "object of isomorphisms from $X$ to $Y$" as the following equalizer:
$$ Iso(X,Y) \to X^Y \times Y^X \;\rightrightarrows\; X^X \times Y^Y $$
where the top arrow on the right side is (composition, reversed composition) and the bottom arrow factors through $(id,id)\colon 1 \to X^X \times Y^Y$.  One can then prove that the maps $Iso(X,Y)\to X^Y$ and $Iso(X,Y)\to Y^X$ are monic, so that $Iso(X,Y)$ can be regarded either as "the object of maps $X\to Y$ which are isomorphisms" or "the object of maps $Y\to X$ which are isomorphisms" (or, as is most evident from its construction, "the object of pairs of maps $X\to Y$ and $Y\to X$ which are inverse isomorphisms").

In a [[cartesian closed 2-category]], however, the analogous "2-equalizer" $Eqv(X,Y)$, does not have similar properties: the projections $Eqv(X,Y)\to X^Y$ and $Eqv(X,Y)\to Y^X$ will not in general be [[fully faithful morphism|fully faithful]].  Thus, we can only regard $Eqv(X,Y)$ as "the object of not-necessarily-adjoint equivalence data $(f,g,\eta,\varepsilon)$."  However, if we use a further [[equifier]] to construct its "subobject of adjoint equivalence data" $AdjEqv(X,Y)$, then the projections $AdjEqv(X,Y)\to X^Y$ and $AdjEqv(X,Y)\to Y^X$ will be fully faithful, so that $AdjEqv(X,Y)$ can also be regarded as "the object of maps $X\to Y$ which are equivalences" and dually.

## In higher category theory

In [[higher category theory]], one expects to have a similar "fully coherent" notion of "adjoint equivalence" in any [[n-category]] or [[infinity-category]], and one hopes to prove a similar theorem that any [[equivalence]] can be refined to an adjoint equivalence.  This is known to be true at least in the following cases:

* For [[Gray-categories]], the statement and proof is in [[Steve Lack]]'s paper [1001.2366](http://arxiv.org/abs/1001.2366) on the [[model structure for Gray-categories]].  See [[adjoint 2-equivalence]].

* For [[tricategories]], the corresponding statement can be deduced from the Gray-categorical version using the [[coherence theorem for tricategories]].  A direct proof can also be found in [[Nick Gurski]]'s paper [Biequivalences in tricategories](http://www.tac.mta.ca/tac/volumes/26/14/26-14abs.html).

* For [[strict omega-categories]], more or less this fact can be found in the study of "generic squares" in the paper [0712.0617](http://arxiv.org/abs/0712.0617) on the [[model structure for strict omega-categories]].

* For [[quasicategories]], the theorem is true, where an "adjoint equivalence" means simply a map out of the [[nerve]] of the [[interval groupoid]]; see [[equivalence in a quasicategory]].

## Related concepts

* [[enriched adjoint equivalence]]

[[!redirects adjoint equivalences]]

[[!redirects adjoint equivalence of categories]]
[[!redirects adjoint equivalences of categories]]



