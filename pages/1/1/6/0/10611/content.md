
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Type theory
+-- {: .hide}
[[!include type theory - contents]]
=--
#### Modalities, Closure and Reflection
+-- {: .hide}
[[!include modalities - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

A _modality_ in [[philosophy]] and formally in [[formal logic]]/[[type theory]] expresses a certain _mode_ (or "moment" as in [Hegel 12](#Hegel12)) of [[being]].

### In philosophy
 {#IdeaInPhilosophy}

According to ([Kant 1900](#Kant1900)) (see [WP](http://de.wikipedia.org/wiki/Kategorie_%28Philosophie%29)) the four "[[category (philosophy)|categories]]" are 

1. Quantity

1. Quality

1. Relation

1. Modality

and the modalities contain the three [[unity of opposites|pairs of opposites]]

* [[possibility]] - impossibility

* [[being]]/[[Dasein]] - [[nothing]]

* [[necessity]] - Zuf&#228;lligkeit


### In formal logic
 {#InFormalLogic}

In [[formal logic]] and [[type theory]] modalities are formalized by
 _modal operator_ or _[[closure operator]]_ $\sharp$, that send [[propositions]]/[[types]] $X$ to new propositions/types $\sharp X$, satisfying some properties. 

Adding such modalities to [[propositional logic]] or similar produces what is called [[modal logic]]. Here operators that are meant to formalize [[necessity]] and [[possibility]] ([[S4 modal logic]]) are maybe most famous. Adding modalities more generally to [[type theory]] yields _[[modal type theory]]_. See there for more details

The [[categorical semantics]] of these modalities is that $\sharp$ is interpreted an [[idempotent monad]]/[[comonad]] on the [[category of contexts]]. 

This has  a refinement to [[homotopy type theory]], where the [[categorical semantics]] of a _higher modality_ or _homotopy modality_ as an idempotent [[(infinity,1)-monad]] ([Shulman 12](#Shulman), [HoTTBook, def. 7.7.5](#HoTTBook)).

## Examples

* [[local modality]], [[Lawvere-Tierney topology]]

* [[double negation modality]]

* [[n-truncation modality]]

* [[unit type]] modality, [[empty type]] co-modality

* [[!-modality]]

* [[shape modality]] $\dashv$ [[flat modality]] $\dashv$ [[sharp modality]]

* [[reduction modality]] $\dashv$ [[infinitesimal shape modality]] $\dashv$ [[infinitesimal flat modality]]

* [[affine modality]]

## Related concepts

* [[monad (in computer science)]]

* [[modal type]], [[anti-modal type]]

* [[adjoint modality]]

* [[Galois connection]]

## References
 {#References}

### In formal logic

Discussion in [[formal logic]] and [[homotopy type theory]] ([[modal type theory]]):

* [[Mike Shulman]], _Higher modalities_, talk at [[UF-IAS-2012]], October 2012  ([pdf](http://uf-ias-2012.wikispaces.com/file/view/modalitt.pdf))
 {#Shulman}

* [[Mike Shulman]], _[All modalities are Higher Inductive Types](http://homotopytypetheory.org/2012/11/19/all-modalities-are-hits/)_

* {#HoTTBook} [Univalent Foundations Project](http://ncatlab.org/nlab/show/UF-IAS-2012), section 7.7 of _[[Homotopy Type Theory -- Univalent Foundations of Mathematics]]_


### In philosopy

* [[Georg Hegel]], _[[Science of Logic]]_, 1812
 {#Hegel12}

* [[Kant]], AA III, 93&#8211; KrV B 106
 {#Kant1900}

* German Wikipedia, _[Modalit&#228;t (Philosophie)](http://de.wikipedia.org/wiki/Modalit&#228;t_(Philosophie))_


[[!redirects modality]]
[[!redirects modalities]]
[[!redirects modal operator]]
[[!redirects modal operators]]