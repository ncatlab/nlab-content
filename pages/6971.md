
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Type theory
+-- {: .hide}
[[!include type theory - contents]]
=--
=--
=--

# Contents
* table of contents
{: toc}

## Idea

_Extensional type theory_ denotes the flavor of [[type theory]] in which [[identity types]] are demanded to be [[propositions]] / of [[h-level 1]].  In other words, they are determined by their [[extension (semantics)|extensions]] --- the collection of pairs of points which are equal.  Type theory which is not extensional is called _[[intensional type theory]]_.

+-- {: .num_remark}
###### Remark

The word "extensional" in type theory (even when applied to identity types) sometimes refers instead to the axiom of  [[function extensionality]].  In general this property is orthogonal to the one considered here: function extensionality can hold or fail in both extensional and intensional type theory.  In particular, [[homotopy type theory]] is [[intensional type theory|intensional]] in that [[identity types]] are crucially _not_ demanded to be [[propositions]], but [[function extensionality]] is often assumed (in terms of these intensional identity types, of course) --- in particular, it follows from the [[univalence axiom]].

=--


## Definition

The basic definition of [[identity types]] as an [[inductive type]] family makes them intensional.  There are two sorts of ways to make them extensional: [[definitional equality|definitionally]] or propositionally.


### Definitional extensionality

In a definitionally extensional type theory, any [[inhabitant]] of an identity type $p:Id_A(x,y)$ induces a [[definitional equality]] between $x$ and $y$.  In other words, we have an "equality reflection rule" of the form

$$ \frac{p:Id_A(x,y)}{x\equiv y} $$

At first, this may appear to be only a "[[skeleton|skeletality]]" assumption, since it does not assert explicitly that $p$ is [[reflexive relation|reflexivity]] rather than a nontrivial [[automorphism|loop]].  However, we can derive this with the induction rule for identity types.  Consider the [[dependent type]]

$$ (x:A),(y:A),(p:Id_A(x,y)) \;\vdash\; Id_{Id_A(x,y)}(p,refl(x)). $$

This is well-typed because the reflection rule applied to $p$ yields a definitional equality $x\equiv y$, so that we have $refl(x):Id_A(x,y)$.  Moreover, [[substitution|substituting]] $x$ for $y$ and $refl(x)$ for $p$ yields the type $Id_{Id_A(x,x)}(refl(x),refl(x))$, which is inhabited by $refl(refl(x))$.

Thus, by induction on identity, we have a term in the above type, witnessing a [[propositional equality]] between $p$ and $refl(x)$.  Finally, applying the equality reflection rule again, we get a definitional equality $p\equiv refl(x)$.

+-- {: .num_remark}
###### Remark
On the other hand, if in addition to the equality reflection rule we postulate that all equality proofs are definitionally equal to reflexivity, then we can derive the induction rule for identity types.  Definitionally extensional type theory is often presented in this form.
=--

A different, also equivalent, way of presenting definitionally extensional type theory is with a definitional [[eta-conversion]] rule for the identity types; see _[here](identity+type#EtaConversion)_.


### Propositional extensionality
 {#PropositionalExtensionality}
 
In a propositionally extensional type theory, we still distinguish [[definitional equality|definitional]] and [[propositional equality]], but no two terms can be propositionally equal in more than one way (up to propositional equality).  In the language of [[homotopy type theory]], this means that all types are [[h-sets]].  There are a number of equivalent ways to force this to be true by adding [[axioms]] to type theory.

1. We can add as an axiom the "uniqueness of identity proofs" ([[axiom UIP]]) property that any two inhabitants of the same identity type $Id_A(x,y)$ are themselves equal (in the corresponding higher identity type).

1. We can add Streicher's *[[axiom K]]* which says that any inhabitant of a self-equality type $Id_A(x,x)$ is (propositionally) equal to the identity/reflexivity equality $1_x$.  (Axiom K is so named because $K$ comes after $J$, and $J$ usually denotes the [[elimination rule|eliminator]] for [[identity types]].)

1. In the presence of [[dependent sum types]], we can add an axiom saying that if $(a,b_1)$ and $(a,b_2)$ are pairs in a dependent sum $\sum_{x\colon A} B(x)$ with the same first component, and the identity type $Id_{\sum_{x\colon A} B(x)}((a,b_1), (a,b_2))$ is inhabited, then so is $Id_{B(a)}(b_1,b_2)$.

1. We can allow definition of functions by a strong form of *pattern matching*, as in unmodified [[Agda]].  The relevant "extra strength" is to allow output *types* of a pattern match which are only well-defined *after* the pattern has been matched.

Propositionally extensional type theory has some of the attributes of intensional type theory, and many type theorists use "extensional type theory" to refer only to the definitional version.


## Properties

### Decidability

Only the intensional, but not the extensional, [[Martin-Löf type theory]] has [[decidability|decidable]] type checking.  See _[[intensional type theory]]_ for more on this.

## Related concepts

* [[axiom K]], [[axiom UIP]]

* [[intensional type theory]], [[homotopy type theory]]

* [[observational type theory]]

## Examples

* [[NuPRL]]

* [[Homotopy Type System]] is [[dependent type theory]] with a mix of extensional and intensional [[identity types]].

## References

* {#Hofmann95} [[Martin Hofmann]], _Extensional concepts in intensional type theory_, Ph.D. thesis, University of Edinburgh, (1995) ([ECS-LFCS-95-327](http://www.lfcs.inf.ed.ac.uk/reports/95/ECS-LFCS-95-327/), [[HofmannExtensionalIntensionalTypeTheory.pdf:file]])
  

* [[Ieke Moerdijk]], E. Palmgren, _Wellfounded trees in categories_. Ann. Pure Appl. Logic, 104:189-218 (2000)

* [[Ieke Moerdijk]], E. Palmgren, _Type theories, toposes and constructive set theory: predicative aspects of AST_,  Ann. Pure Appl. Logic, 114:155-201, (2002)



[[!redirects extensional type theories]]
