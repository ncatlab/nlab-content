
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

{#TypeUniverseAsReflection} One also speaks of $Type$ as being a _reflection_ of the type system in itself (e.g. [MartinL&#246;f 74, p. 6](#MartinLoef74), [Palmgren, pp. 2-3](#Palmgren), [Rathjen, p. 1](#Rathjen), [Luo 11, section 2.5](#Luo11), [Luo 12, p. 2](#Luo12), [Stanf. Enc. Phil.](#SEP)), following the _[[reflection principle]]_ in [[set theory]].

In [[homotopy type theory]] a type of (small) types is what in [[(∞,1)-category theory|higher]] [[categorical semantics]] is interpreted as a (small) _[[object classifier]]_.  Thus, the type of types is a refinement of the [[type of propositions]] which only contains the [[(-1)-truncated]]/[[h-level]]-1 types (and is semantically a [[subobject classifier]]).

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

A **universe &#224; la Tarski** ([Hofmann, section 2.1.6](#Hofmann), [Luo 12](#Luo12), [Gallozzi 14, p. 40](#Gallozzi14)) is a type $U$ together with an "interpretation" operation allowing us to regard its [[terms]] as _codes_ or _names_ for actual types. Thus we have a rule such as

$$\frac{A:U}{El(A)\;type}$$

saying that for each term $A$ of the type universe $U$ there is an actual type $El(A)$. (Conversely, with notation as used at _[[object classifier in an (infinity,1)-topos]]_, one might write $A = 'El(A)'$ to indicate that $A$ is the _name_ of the type $El(A)$ in the type universe.)

We usually also have operations on the universe corresponding to (but not identical to) type formers, such as

$$\frac{A:U\quad B:A\to U}{\pi(A, B) : U}$$

with an [[equality]] $El(\pi(A,B))=\Pi \, El(A)\, El(B)$. Usually this latter equality (and those for other type formers) is a [[judgmental equality]]. If it is only an [[equivalence in homotopy type theory|equivalence]] (i.e. we have a rule which gives us a canonical term of the equivalence type), we may speak of a **weakly &#224; la Tarski universe** ([Gallozzi 14, p. 49-50](#Gallozzi14)).

We can give a slightly different definition of weakly &#224; la Tarski universe using [[propositional equality]] and a larger universe. More precisely, we can consider two (or many) universes $U$ and $U'$ with the usual rules for the relative reflection $el(a):U'$ for any $a:U$, a choice of weakly or strongly a la Tarski computational rules for the reflections $El$ and $El'$, and a computation rule for the relative reflection el of $U$ inside $U'$ based on propositional equality, which gives us canonical elements of the identity types $Id_{U'}(\pi'(el(a),el(b)),el(\pi(a,b)))$ and similarly for the other type formers.

If the containing universe is univalent the two definitions turn out to coincide.

Universes defined internally via [[induction-recursion]] are (strongly) &#224; la Tarski. Weakly &#224; la Tarski universes are easier to obtain in [[semantics]] (see [below](#CategoricalSemantics)): they are somewhat more annoying to use, but probably suffice for most purposes.


## Properties

### Universe enlargement
 {#UniverseEnlargement}

Both [[Coq]] and [[Agda]] support [[universe polymorphism]] to deal with the issue of universe enlargement. Moreover, Coq supports [[typical ambiguity]].

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

Type universes in [[Martin-Löf type theory]] originate around

* {#MartinLoef74} [[Per Martin-Löf]], _An intuitionistic theory of types: predicative part_, In Logic Colloquium (1973), ed. H. E. Rose and J. C. Shepherdson (North-Holland, 1974), 73-118. ([web](http://citeseerx.ist.psu.edu/viewdoc/summary?doi=10.1.1.131.926))


Basic discussion of the syntax of type universes is in 

* {#Palmgren} [[Erik Palmgren]], _On Universes in Type Theory_  ([pdf](http://www2.math.uu.se/~palmgren/universe.pdf))

Definition of type universes weakly &#224; la Tarski is in 

* {#Hofmann} [[Martin Hofmann]], section 2.1.6 of _Syntax and semantics of dependent types_ ([web](http://citeseerx.ist.psu.edu/viewdoc/summary?doi=10.1.1.36.8985))

* {#Luo12} [[Zhaohui Luo]], _Notes on Universes in Type Theory_, 2012 ([pdf](http://www.cs.rhul.ac.uk/home/zhaohui/universes.pdf))

* {#Gallozzi14} [[Cesare Gallozzi]], _Constructive Set Theory from a Weak Tarski Universe_, MSc thesis (2014) ([arXiv:1411.5591](http://xxx.tau.ac.il/abs/1411.5591))


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


See also

* {#Rathjen} [[Michael Rathjen]], _The strength of Martin-L&#246;f type theory with superuniverse. Part I_ [pdf](https://www1.maths.leeds.ac.uk/~rathjen/Super.pdf)

* {#SEP} Stanford Encyclopedia of Philosophy,  _[Type theory -- Extensions of type systems, Polymorphism, Paradoxes](http://plato.stanford.edu/entries/type-theory/#6)_

* {#Luo11} [[Zhaohui Luo]], _Contextual analysis of word meanings in type-theoretical semantics_, in Pogodalla, Prost (eds.) _Logical Aspects of Computational Linguistics_, 2011 ([pdf](http://www.cs.rhul.ac.uk/home/zhaohui/LACL11.pdf))


[[!redirects Type]]

[[!redirects type universe]]
[[!redirects type universes]]

[[!redirects universe in type theory]]
[[!redirects universes in type theory]]