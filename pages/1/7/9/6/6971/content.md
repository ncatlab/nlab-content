
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

_Extensional type theory_ denotes the flavor of [[type theory]] in which [[identity types]] satisfy the *reflection rule*, saying that if two terms are [[typal equality|typally equal]] then they are also [[judgmental equality|judgmentally equal]].

In particular, this implies that all [[identity types]] are [[propositions]] / of [[h-level 1]], and thus equivalently that all types are required to be [[h-sets]].  Therefore, extensional type theory is a [[set-level type theory]], and hence a form of [[set-level foundations]].  However, there are other set-level type theories, such as those obtained by adding [[UIP]] as an axiom.

__Note:__ *For a while, the nLab incorrectly used "extensional type theory" to refer to what we now call [[set-level type theory]].  If you encounter uses of this sort, please correct them.*

Extensional type theory is poorly behaved metatheoretically, and very difficult to implement in a proof assistant.  However, it is sometimes more convenient to work with informally, and there are conservativity theorems relating it to other set-level type theories that are better-behaved.

Type theory which is not extensional is called _[[intensional type theory]]_.

+-- {: .num_remark}
###### Remark
The word "extensional" in type theory (even when applied to identity types) sometimes refers instead to the axiom of  [[function extensionality]].  In general this property is orthogonal to the one considered here: function extensionality can hold or fail in both extensional and intensional type theory.

In particular, [[homotopy type theory]] is [[intensional type theory|intensional]] in that [[identity types]] are crucially _not_ demanded to be [[propositions]], but [[function extensionality]] is often assumed (in terms of these intensional identity types, of course) --- in particular, it follows from the [[univalence axiom]].  Indeed, univalence itself is arguably an [[extensionality principle]] for the universe (Hofmann and Streicher originally introduced it under the name "universe extensionality"), but it is inconsistent with "extensional type theory" in the sense considered here.
=--

+-- {: .num_remark}
###### Remark
The origin of the names "extensional" and "intensional" is somewhat confusing.  In fact they refer to the behavior of the [[definitional equality]].  The idea is that the [[identity type]] is always an "extensional" notion of equality (although it can be more or less extensional, depending on whether further extensionality principles like [[function extensionality]] and [[univalence]] hold).  Thus, if the definitional equality *coincides* with the identity type, as it does under the reflection rule, the former is also extensional, and so we call the type theory "extensional" --- while if the two equalities do *not* coincide, then the definitional equality has room to be more intensional than the identity type, and so we call the type theory "intensional".
=--


## Definition

The Martin-Lof definition of [[identity types]] as an [[inductive type]] family makes them intensional.  To make the type theory extensional, we add a rule that any [[inhabitant]] of an identity type $p:Id_A(x,y)$ induces a [[definitional equality]] between $x$ and $y$.  In other words, we have an "equality reflection rule" of the form

$$ \frac{p:Id_A(x,y)}{x\equiv y} $$

At first, this may appear to be only a "[[skeleton|skeletality]]" assumption, since it does not assert explicitly that $p$ is [[reflexive relation|reflexivity]] rather than a nontrivial [[automorphism|loop]].  However, we can derive this with the induction rule for identity types.  Consider the [[dependent type]]

$$ (x:A),(y:A),(p:Id_A(x,y)) \;\vdash\; Id_{Id_A(x,y)}(p,refl(x)). $$

This is well-typed because the reflection rule applied to $p$ yields a judgmental equality $x\equiv y$, so that we have $refl(x):Id_A(x,y)$.  Moreover, [[substitution|substituting]] $x$ for $y$ and $refl(x)$ for $p$ yields the type $Id_{Id_A(x,x)}(refl(x),refl(x))$, which is inhabited by $refl(refl(x))$.

Thus, by induction on identity, we have a term in the above type, witnessing a [[typal equality]] between $p$ and $refl(x)$.  Finally, applying the equality reflection rule again, we get a judgmental equality $p\equiv refl(x)$.

+-- {: .num_remark}
###### Remark
On the other hand, if in addition to the equality reflection rule we postulate that all equality proofs are definitionally equal to reflexivity, then we can derive the induction rule for identity types.  Extensional type theory is often presented in this form.
=--

A different, also equivalent, way of presenting extensional type theory is with a definitional [[eta-conversion]] rule for the identity types; see _[here](identity+type#EtaConversion)_.

## Properties

### Decidability

Extensional [[Martin-Löf type theory]] does not have [[decidability|decidable]] type checking.  See _[[intensional type theory]]_ for more on this.

## Related concepts

* [[axiom K]], [[axiom UIP]]

* [[intensional type theory]], [[homotopy type theory]]

* [[observational type theory]], [[higher observational type theory]]

## Examples

* [[NuPRL]]

* [[Andromeda]]

## References

* {#Hofmann95} [[Martin Hofmann]], _Extensional concepts in intensional type theory_, Ph.D. thesis, University of Edinburgh, (1995) ([ECS-LFCS-95-327](http://www.lfcs.inf.ed.ac.uk/reports/95/ECS-LFCS-95-327/), [[HofmannExtensionalIntensionalTypeTheory.pdf:file]])
  

* [[Ieke Moerdijk]], E. Palmgren, _Wellfounded trees in categories_. Ann. Pure Appl. Logic, 104:189-218 (2000)

* [[Ieke Moerdijk]], E. Palmgren, _Type theories, toposes and constructive set theory: predicative aspects of AST_,  Ann. Pure Appl. Logic, 114:155-201, (2002)

* [[Jonathan Sterling]], [[Carlo Angiuli]], [[Daniel Gratzer]], _Cubical syntax for reflection-free extensional equality_. In Herman Geuvers, editor, _4th International Conference on Formal Structures for Computation and Deduction (FSCD 2019)_, volume 131 of _Leibniz International Proceedings in Informatics (LIPIcs)_, pages 31:1-31:25. ([arXiv:1904.08562](https://arxiv.org/abs/1904.08562), [doi:10.4230/LIPIcs.FSCD.2019.31](https://doi.org/10.4230/LIPIcs.FSCD.2019.31))

* [[Jonathan Sterling]], [[Carlo Angiuli]], [[Daniel Gratzer]], _A Cubical Language for Bishop Sets_, Logical Methods in Computer Science, 18 (1), 2022. ([arXiv:2003.01491](https://arxiv.org/abs/2003.01491)). 

Extensional type theory is discussed in chapter 2 of:

* {#AngiuliGratzer} [[Carlo Angiuli]], [[Daniel Gratzer]], *Principles of Dependent Type Theory* ([pdf](https://www.danielgratzer.com/papers/type-theory-book.pdf))

[[!redirects extensional type theories]]
[[!redirects equality reflection]]
[[!redirects equality reflection rule]]
