
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Universes
+-- {: .hide}
[[!include universe - contents]]
=--
#### Type theory
+-- {: .hide}
[[!include type theory - contents]]
=--
=--
=--



#Contents#
* table of contents
{:toc}

## Idea

In [[type theory]], a _type of (small) types_ -- usually written $Type$ -- is a [[type]] whose [[terms]] are themselves [[type|types]].  Thus, it is a [[universe]] of (small) [[type|types]], a _universe in type theory_.

In [[homotopy type theory]] a type of (small) types is what in [[(∞,1)-category theory|higher]] [[categorical semantics]] is interpreted as a (small) [[object classifier]].  Thus, the type of types is a refinement of the [[type of propositions]] which only contains the [[(-1)-truncated]]/[[h-level]]-1 types (and is semantically a [[subobject classifier]]).

In the presence of a type of types a [[judgement]] of the form

$$
  \vdash A : Type
$$

says that $A$ is a [[term]] of [[type]] $Type$, hence is a (small) [[type]] itself. More generally, a [[hypothetical judgement]] of the form

$$
  x : X \vdash A(x) : Type
$$

says that $A$ is an $X$-[[dependent type]].

In [[homotopy type theory]] the type of types $Type$ is often assumed to satisfy the [[univalence]] [[axiom]]. This is a reflection of the fact that in its [[categorical semantics]] as an [[object classifier]] is part of an [[internal (∞,1)-category]] in the ambient [[(∞,1)-topos]]: the one that as an [[indexed category]] is the small [[codomain fibration]].

[[Per Martin-Lof]]'s original type theory contained a type of *all* types, which therefore in particular contained itself, i.e. one had $Type : Type$.  But it was pointed out by [[Jean-Yves Girard]] that this was inconsistent; see [[Girard's paradox]].  Thus, modern type theories generally contain a hierarchy of types of types, with $Type_0 : Type_1$ and $Type_1 : Type_2$, etc.

## Formalizations 

### Type Universe &#224; la Russell
  {#RussellStyle}

A **universe &#224; la Russell** is a [[type]] whose terms *are* types. In the presence of a separate [[judgment]] "$A \;type$", this can be formulated as a [[natural deduction|deduction rule]] of the form

$$\frac{A:U}{A \;type}$$

Thus, the [type formers](natural+deduction#IntroductionAndElimination) have rules saying which universe they belong to, such as:

$$\frac{A:U\quad B:A\to U}{\Pi\, A\, B : U}$$

With universes &#224; la Russell, we can also omit the judgment "$A\; type$" and replace it everywhere by a judgment that A is a term of some universe. This is the approach taken by the [[Homotopy Type Theory -- Univalent Foundations of Mathematics|HoTT textbook]] and by [[Coq]].


### Type Universe &#224; la Tarski
 {#TarskiStyle}

A **universe &#224; la Tarski** ([Hofmann, section 2.1.6](#Hofmann), [Gallozzi 14, p. 40](#Gallozzi14)) is a type together with an "interpretation" operation allowing us to regard its [[terms]] as types (or "codes for types"). Thus we have a rule such as

$$\frac{A:U}{El(A)\;type}$$

We usually also have operations on the universe corresponding to (but not identical to) type formers, such as

$$\frac{A:U\quad B:A\to U}{pi(A, B) : U}$$

with an [[equality]] $El(pi(A,B))=\Pi \, El(A)\, El(B)$. Usually this latter equality (and those for other type formers) is a [[judgmental equality]]. If it is only an [[equivalence in homotopy type theory|equivalence]] (i.e. we have a rule which gives us a canonical term of the equivalence type), we may speak of a **weakly &#224; la Tarski universe** ([Gallozzi 14, p. 49-50](#Gallozzi14)).

We can give a slightly different definition of weakly &#224; la Tarski universe using [[propositional equality]] and a larger universe. More precisely, we can consider two (or many) universes $U$ and $U'$ with the usual rules for the relative reflection $el(a):U'$ for any $a:U$, a choice of weakly or strongly a la Tarski computational rules for the reflections $El$ and $El'$, and a computation rule for the relative reflection el of $U$ inside $U'$ based on propositional equality, which gives us canonical elements of the identity types $Id_{U'}(\pi'(el(a),el(b)),el(\pi(a,b)))$ and similarly for the other type formers.

If the containing universe is univalent the two definitions turn out to coincide.

Universes defined internally via [[induction-recursion]] are (strongly) &#224; la Tarski. Weakly &#224; la Tarski universes are easier to obtain in [[semantics]] (see [below](#CategoricalSemantics)): they are somewhat more annoying to use, but probably suffice for most purposes.


## Properties

### Universe enlargement
 {#UniverseEnlargement}

Both [[Coq]] and [[Agda]] have systems to manage universe sizes and [[universe enlargement]] automatically; Agda's is more advanced (universe polymorphism), whereas Coq's is good enough for many purposes but tends to produce "universe inconsistencies" when working with [[univalence]].  

### Categorical semantics
 {#CategoricalSemantics}

[[univalence|Univalent]] type universes [&#224; la Russell](#RussellStyle) have been shown to be interpreted in [[type-theoretic model categories]] presenting the base [[(∞,1)-topos]] [[∞Grpd]]
([Kapulkin-Lumsdaine-Voevodsky 12](#KapulkinLumsdaineVoevodsky12))
and more generally presenting [[(∞,1)-toposes]] of [[(∞,1)-presheaves]] over [[elegant Reedy categories]] ([Shulman 13](#Shulman13)).

Discussion for general [[(∞,1)-toposes]] (of [[(∞,1)-sheaves]]) that should have implementation [weakly &#224; la Tarski](#TarskiStyle) ([Gallozzi 14, p. 49-50](#Gallozzi14)) is in ([Gepner-Kock 12](#GepnerKock12)).

For more on this see the respective sections at _[[relation between type theory and category theory]]_.



## Related concepts

* [[resizing axiom]]

* [[universe polymorphism]]

* [[univalence]]

* [[Prop]], the [[type of propositions]], 

  * [[subobject classifier]]

* [[object classifier]]

* [[parametric polymorphism]]

* [[Girard's paradox]]

## References

Some of the text above is adapted from the entry _[[homotopytypetheory:universe]]_ at the [[homotopytypetheory:HomePage|homotopy type theory web]].

Basic discussion of the syntax of type universes is in 

* [[Erik Palmgren]], _On Universes in Type Theory_  ([pdf](http://www2.math.uu.se/~palmgren/universe.pdf))

Definition of type universes weakly &#224; la Tarski is in 

* {#Hofmann} [[Martin Hofmann]], section 2.1.6 of _Syntax and semantics of dependent types_ ([web](http://citeseerx.ist.psu.edu/viewdoc/summary?doi=10.1.1.36.8985))


Detailed discussion of the type of types in [[Coq]] is in

* [[Adam Chlipala]], _[Certified programming with dependent types](http://adam.chlipala.net/cpdt/)_ -- _[Library Universes](http://adam.chlipala.net/cpdt/html/Universes.html)_ 

See also around slide 8 of the survey

* Frade, _Calculus of inductive constructions_ (2008/2009) ([pdf](http://www3.di.uminho.pt/~mjf/pub/SFV-CIC-2up.pdf))

A formal proof in [[homotopy type theory]] that the type of [[homotopy n-types]] is not itself a homotopy $n$-type (it is an $(n+1)$-type) is in 

* Nicolai Kraus, C. Sattler, _The universe $\mathcal{U}_n$ is not an $n$-type_ May 2013 ([pdf](http://red.cs.nott.ac.uk/~ngk/universes.pdf))

[[(∞,1)-category theory|(∞,1)-Categorical]] semantics for [[univalence|univalent]] type universes is discussed in

* {#KapulkinLumsdaineVoevodsky12} [[Chris Kapulkin]], [[Peter LeFanu Lumsdaine]], [[Vladimir Voevodsky]], _The Simplicial Model of Univalent Foundations_ ([arXiv:1211.2851](http://arxiv.org/abs/1211.2851))

* {#Shulman13} [[Michael Shulman]], _The univalence axiom for elegant Reedy presheaves_ ([arXiv:1307.6248](http://arxiv.org/abs/1307.6248))

* {#GepnerKock12} [[David Gepner]], [[Joachim Kock]], _Univalence in locally cartesian closed ∞-categories_ ([arXiv:1208.1749](http://arxiv.org/abs/1208.1749))

[[!redirects types of types]]
[[!redirects universe of types]]
[[!redirects universes of types]]

Weak Tarski universes in homotopy type theory are discussed in 

* {#Gallozzi14} [[Cesare Gallozzi]], _Constructive Set Theory from a Weak Tarski Universe_, MSc thesis (2014) 


[[!redirects Type]]

[[!redirects type universe]]
[[!redirects type universes]]

[[!redirects universe in type theory]]
[[!redirects universes in type theory]]