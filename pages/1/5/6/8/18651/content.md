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

A **duploid** is a [[category]]-like structure where objects have a specific [[polarity in type theory|polarity]] and composition is not necessarily [[associative]].

Duploids are models of programming languages with explicitly polarized [[positive type|positive]] and [[negative type|negative]] types, accomodating both [[call-by-value]] and [[call-by-name]] programming paradigms.

A duploid can be constructed from an [[adjunction]] and the category of duploids is [[reflective subcategory|reflective]] in the category of adjunctions, equivalent to the subcategory of adjunctions satisfying an equalizing requirement.

## Definition

A **pre-duploid** $\mathcal{D}$ consists of

1. a set $|\mathcal{D}|$ of objects with a polarity map $\varpi : |\mathcal{D}| \to \{+,-\}$. If $\varpi(A) = +$, we say $A$ is positive and otherwise negative.
2. for every pair $A,B \in |\mathcal{D}|$ a set of morphisms $\mathcal{D}(A,B)$.
3. for every compatible pair of morphisms $f \in \mathcal{D}(A,B), g\in \mathcal{D}(B,C)$ a composite $g \odot f \in \mathcal{D}(A,C)$.
4. for every object $A$ an identity morphism $id_A \in \mathcal{D}(A,A)$.
5. For every $f \in \mathcal{D}(A,B), g \in \mathcal{D}(B,C), h \in \mathcal{D}(C,D)$, an associative law $f \odot (g \odot h) = (f \odot g) \odot h$ when $B$ is negative or $C$ is positive.

## Related Concepts

* [[polarity in type theory]]
* [[thunk-force category]]
* [[runnable monad]]

## References

Duploids were introduced in chapter II of

* {#Mthesis} Guillaume Munch-Maccagoni, Syntax and Models of a Non-Associative Composition of Programs and Proofs, PhD thesis University of Paris Diderot, 2013 [pdf link](http://guillaume.munch.name/files/SMAC-screen.pdf)