+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Constructivism, Realizability, Computability
+-- {: .hide}
[[!include constructivism - contents]]
=--
#### Category theory
+-- {: .hide}
[[!include category theory - contents]]
=--
=--
=--


# Duploid
* table of contents
{:toc}

## Idea

A **duploid** is a [[category]]-like [[structure]] where [[objects]] have a specific [[polarity in type theory|polarity]] and [[composition]] is not necessarily [[associative]].

Duploids are models of [[programming languages]] with [[side effects]] and explicitly polarized [[positive type|positive]] and [[negative type|negative]] [[types]], accomodating both [[call-by-value]] and [[call-by-name]] programming paradigms. Duploids axiomatize the algebraic structure of effectful morphisms, and to a certain extent "pure" morphisms (those with no side effects) can be characterized by equational properties as thunkable and linear morphisms. Contrast with [[call-by-push-value]] which directly provides a syntax for the pure morphisms (as values and stacks).

A duploid can be constructed from an [[adjunction]] and the category of duploids is [[reflective subcategory|coreflective]] in the category of adjunctions, equivalent to the [[subcategory]] of adjunctions satisfying an equalizing requirement. The intuition is that a duploid is what is left of an adjunction if we only consider (co)Kleisli morphisms and duploids can be identified with adjunctions whose categories can be recovered from the Kleisli morphisms.

## Definition

A **pre-duploid** $\mathcal{D}$ consists of

1. a set $|\mathcal{D}|$ of objects with a polarity map $\varpi : |\mathcal{D}| \to \{+,-\}$. If $\varpi(A) = +$, we say $A$ is positive and otherwise negative.
2. for every pair $A,B \in |\mathcal{D}|$ a set of morphisms $\mathcal{D}(A,B)$.
3. for every compatible pair of morphisms $f \in \mathcal{D}(A,B), g\in \mathcal{D}(B,C)$ a composite $g \odot f \in \mathcal{D}(A,C)$.
4. for every object $A$ an morphism $id_A \in \mathcal{D}(A,A)$ that is the identity with respect to composition.
5. For every $f \in \mathcal{D}(A,B), g \in \mathcal{D}(B,C), h \in \mathcal{D}(C,D)$, an associative law $h \odot (g \odot f) = (h \odot g) \odot f$ when $B$ is negative or $C$ is positive.

Note that when restricted to positive objects or negative objects, composition and identities form a category, written $\mathcal{P}$ and $\mathcal{N}$. When the polarity is known we write positive objects as $P,Q,R$ and negative objects as $L,M,N$. We call composition where the middle object is positive "positive composition" or "by-value composition" and notate it as $g \bullet f$ and when the middle object is negative we call it "negative composition" or "by-name composition" and notate it as $g \circ f$.
Then the associativity laws can be restated as:

1. $\bullet\bullet$: $f \bullet (g \bullet h)  = (f \bullet g) \bullet h$
2. $\circ\circ$: $f \circ (g \circ h)  = (f \circ g) \circ h$
3. $\bullet\circ$: $f \bullet (g \circ h)  = (f \bullet g) \circ h$

and we can see that the only obstacle to associativity is that $f \circ (g \bullet h)$ is not necessarily equal to $(f \circ g) \bullet h$.

A **duploid** is a pre-duploid $\mathcal{D}$ plus two **polarity shifts** 
$\Downarrow : |\mathcal{N}| \to |\mathcal{P}| and \Uparrow : |\mathcal{P}| \to |\mathcal{N}|$, and for each $P \in |\mathcal{P}|, N \in |\mathcal{N}|$, morphisms:

1. $delay_P : P \to \Uparrow P$
2. $force_P : \Uparrow P \to P$
3. $wrap_N : N \to \Downarrow N$
4. $unwrap_N : \Downarrow N \to N$

such that

1. $\forall f : A \to P, force_P \circ (delay_P \bullet f) = f$
2. $\forall f : N \to A, (f \circ unwrap_N) \bullet wrap_N = f$
3. $delay_P \bullet force_P = id_{\Uparrow P}$
4. $wrap_N \circ unwrap_N = id_{\Downarrow N}$

In light of the definition of linear and thunkable morphisms, these identities are equivalent to saying

1. $wrap_N$ is thunkable.
2. $wrap_N, unwrap_N$ is an isomorphism.
3. $force_P$ is linear.
4. $force_P, thunk_P$ is an isomorphism.

## Linear and Thunkable Morphisms

Just as thunkable morphisms can be defined in a [[thunk-force category]] and linear morphisms can be defined in a category with a [[runnable monad]], they can be defined in a duploid in  a similar way using $delay_P$ in place of the thunk and $unwrap_N$ in place of the run morphism.
However, thunkable and linear morphisms can also be defined in a _pre-duploid_, giving a simple characterization just in terms of associativity of composition.

A morphism $f$ is **thunkable** if for all compatible $g,h$,
$$h \odot (g \odot f) = (h \odot g) \odot f.$$
and a morphism $f$ is **linear** if for all compatible $g,h$,
$$f \odot (g \odot h) = (f \odot g) \odot h.$$

Observe that all $f : P \to B$ are trivially linear and $g : A \to N$ are trivially thunkable. Further thunkable and linear morphisms form (non-full) subcategories $\mathcal{D}_t, \mathcal{D}_l$.

To understand these concepts, consider the non-trivial situation where $f : A \to P$ is thunkable:
$$h \circ (g \bullet f) = (h \circ g) \bullet f.$$
on the left side, since we have a by-name composition, $h$ is "evaluated first", whereas on the right side we have a by-value composition, so $f$ is evaluated first.
Thus these two morphisms being equal implies in many semantics $f$ cannot perform any [[side-effect]]. For instance if $f$ prints to the screen and so does $h$, then each composite will print in a different order. Furthermore, if $f$ can manipulate its [[continuation]] explicitly, it has to treat it linearly otherwise $h$ may be evaluated twice or not at all.

In the dual, if $f : N \to B$ and $f$ is linear:
$$f \circ (g \bullet h) = (f \circ g) \bullet h$$
holds and similarly $f$ is evaluated first in the left morphism and $h$ is evaluated first in the right. Then as above it cannot perform any effects and has to treat its *input* linearly, as duplicating or dropping $h$ would make the equation fail to hold.

## Relation to Adjunctions

Briefly, the category of duploids and duploid functors is a [[reflective subcategory]] of the category of adjunctions and morphisms of adjunctions.

### A Duploid from an Adjunction

First, we construct a duploid from an adjunction, which we think of as a [[forgetful functor]] that only remembers the Kleisli morphisms of the adjunction. To keep the proof unbiased, we start with a [[profunctor]] $O : C_- &#8696; C_+$ that the adjunction [[representable functor|represents]]. This gives us a notion of "oblique-" or [[heteromorphism|hetero-]]morphism from a positive object $P \in C_+$ to a negative object $N \in C_-$ as $O(P,N)$ and can be used to define the Kleisli and coKleisli categories. In programming applications these are the "possibly effectful" morphisms. Then let $F \dashv G$ be adjoint functors representing $O$, i.e. there is a natural equivalence:
$$ C_-(F P, N) \cong O(P,N) \cong C_+(P, G N).$$
The pre-duploid $\mathcal{D}$ has as objects $|\mathcal{D}| = |C_+| + |C_-|$ with $\varpi(P) = +, \varpi(N) = -$.
The morphisms are defined as:
$$\mathcal{D}(A,B) = O(A^+,B^-)$$

where
$$P^+ = P$$
$$N^+ = G N$$
$$P^- = F P$$
$$N^- = N$$

and identities are given by the identities/unit and counit of the adjunction:

$$\id_P : O(P, F P) \equiv C_-(F P,F P)$$
$$\id_N : O(G N, N) \equiv C_+(G N,G N)$$

To define composition of $f \in \mathcal{D}(A,B), g \in \mathcal{D}(B,C)$, we inspect $B$. If $B = P$ is positive, composition is interpreted as composition in $C_-$, or equivalently in the [[Kleisli category]] of $GF$, using 
$$f \in O(A^+,F P) \cong C_-(F A^+, F P)$$
$$g \in O(P, C^-) \cong C_-(F P, C^-)$$
and similarly if $B = N$ is negative, composition is interpreted as composition in $C_+$, or equivalently in the [[Kleisli category]] of $FG$, using
$$f \in O(A^+,N) \cong C_+(A^+, G N)$$
$$g \in O(G N, C^-) \cong C_+(G N, G C^-)$$

This definition makes it clear that the identities are identity and the $\bullet\bullet$ and $\circ\circ$ laws hold from identity and associativity of $C_+,C_-$. 

### Adjunction from a Duploid

From a duploid, we can construct the "cofree" adjunction: i.e., a right adjoint to the forgetful functor just defined. Intuitively, we want to recover the homomorphisms just from the heteromorphisms. The maximal choice is to consider all thunkable morphisms between positive types and linear morphisms between negative types to be homomorphisms.

Furthermore, this functor is fully faithful, making the category of duploids a [[reflective subcategory]] of adjunctions: they can be identified with exactly those adjunctions in which the unit and counit are mono and epi respectively and in which all thunkable heteromorphisms are the image under $F$ of some homomorphism and vice-versa all linear heteromorphisms are in the image of $G$.
This is equivalent to saying that the unit $\eta$ is the [[equalizer]] of $GF\eta$ and $\eta GF$ and dually that the counit $\epsilon$ is the [[coequalizer]] of $FG\epsilon$ and $\epsilon FG$

## Related Concepts

* [[polarity in type theory]]
* [[thunk-force category]]
* [[runnable monad]]

## References

Duploids were introduced in chapter II of

* {#Mthesis} Guillaume Munch-Maccagoni, _Syntax and Models of a Non-Associative Composition of Programs and Proofs_, PhD thesis University of Paris Diderot, 2013 [link](https://hal.inria.fr/tel-00918642)