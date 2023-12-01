
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Category theory
+--{: .hide}
[[!include category theory - contents]]
=--
=--
=--



# Semifunctors
* table of contents
{: toc}

## Idea

A _semifunctor_ is a [[homomorphism]] between [[semicategories]], like a [[functor]] is a homomorphims between [[categories]].

## Definition

A **semifunctor** $F$ from a [[semicategory]] $C$ to a semicategory $D$ is a map sending each [[object]] $x \in C$ to an object $F(x) \in D$ and each [[morphism]] $f : x \to y$ in $C$ to morphism $F(f) : F(x) \to F(y)$ in $D$, such that

* $F$ preserves [[composition]]: $F(g\circ f) = F(g)\circ F(f)$ whenever the left-hand side is well-defined.

If $C$ is a [[category]], then $F$ need *not* preserve its [[identity morphisms]], but the composition axiom does require that it send them to [[idempotents]] in $D$.

## Relation to Profunctors

In [[Rel]], the bicategory of relations, adjoint pairs of relations are equivalent to functions (see [[principle of unique choice]]). Even with the axiom of choice, the analogous theorem for [[Prof]], the bicategory of profunctors, says that an adjoint pair of profunctors is equivalent, not necessarily to a functor, but instead a semifunctor. If the codomain of the semifunctor is [[Cauchy complete]] this is equivalent to a functor, which recovers the usual formulation of this theorem.

## Examples

A mapping $F$ of a category into another category that sends $id_X$ to a nontrivial idempotent endomorphism of $F(X)$ is a semifunctor but not a functor.

More generally, recall from [[semicategory]] that the forgetful functor $U \colon Cat \to Semicat$ has a [[right adjoint]] $G$, which sends a semicategory to its category of idempotents, or [[Karoubi envelope]].  Thus to give a semifunctor from a category $C$ to a (semi)category $D$ is the same as giving a functor from $C$ to the Karoubi envelope $\bar D$ of $D$ (but beware that this correspondence does not hold for [[natural transformations]]).

Semifunctors between categories arise in the study of non-extensional type theories such as [[lambda calculus]] with $\beta$ equivalence, but not $\eta$ equivalence for the function type (see [Hayashi 85](#H85)).
Whereas with both $\beta, \eta$, a function type $A \to B$ can be described as a right adjoint functor to $A \times -$, the non-extensional function type can be described by weakening the requirement to the right adjoint being merely a semifunctor.

## Related concepts

* [[semicategory]]

* [[semi-simplicial set]]

* [[Karoubi envelope]]

## References

An early reference for semifunctors (there called "weak functors") is:

- B. Elkins and J. A. Zilber. _Categories of actions and Morita equivalence_, The Rocky Mountain Journal of Mathematics **6** 2 (1976): 199-225.

The terminology *semifunctors* originates in 

* {#Hayashi1985} [[Susumu Hayashi]], Def. 1.1 in: *Adjunction of semifunctors: categorical structures in nonextensional lambda calculus*, Theoretical Computer Science **41** (1985) 95-104 &lbrack;<a href="https://doi.org/10.1016/0304-3975(85)90062-3">doi:10.1016/0304-3975(85)90062-3</a>&rbrack;

whose author proceeds to discuss their [[adjoint pairs]] in the context of [[categorical semantics]] for a version of the [[lambda calculus]].


[[!redirects semifunctor]]
[[!redirects semifunctors]]

[[!redirects semi-functor]]
[[!redirects semi-functors]]
