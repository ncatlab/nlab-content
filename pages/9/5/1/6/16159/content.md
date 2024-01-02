
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Type theory
+-- {: .hide}
[[!include type theory - contents]]
=--
#### Equality and Equivalence
+--{: .hide}
[[!include equality and equivalence - contents]]
=--
#### Universes
+-- {: .hide}
[[!include universe - contents]]
=--
=--
=--


> Disambiguation: This should not be confused with propositional extensionality in [extensional type theory](extensional+type+theory#propositional_extensionality).


#Contents#
* table of contents
{:toc}

##Idea

In [[formal logic]] **propositional extensionality** holds when any two [[propositions]] $P$ and $Q$ are identified, $P = Q$, precisely if they [[implication|imply]] each other, $(P \leftrightarrow Q)$ (hence if they are _logically equivalent_ $(P \simeq Q)$), i.e.

$$
  (P=Q) \simeq (P\leftrightarrow Q)
  \,.
$$ 

## Properties

### In type theory and Relation to univalence

In [[type theory]] the expression $(P=Q)$ is the [[identity type]] $Id_{Prop}(P,Q)$ of the [[type of propositions|universe of propositions]] (or of the whole [[universe of types]], under [[propositions as types]]), with $P$ and $Q$ [[substitution|substituted]]. One might more precisely write $('P'='Q')$ here, with the quotation marks indicating that this is the _name_ of the proposition, namely a [[term]] of the universe type, rather than the proposition/type itself. 

On the other hand, the expression $(P \leftrightarrow Q)$ in [[homotopy type theory]] is the type of [[equivalence in homotopy type theory|equivalences]] $(P \simeq Q)$ between the two propositions, hence the [[subtype]] of the [[function type]] $(P \to Q)$ on those terms that, in particular, have a [[homotopy inverse]].

Hence propositional extensionality in type theory is the statement that 

$$
  ('P' = 'Q') \simeq (P \simeq Q)
  \,.
$$

(e.g. [Sozeau-Tabareau, section 3.2](#SozeauTabareau))

In [[homotopy type theory]], the assertion of this equivalence is a special case of the _[[univalence axiom]]_ which asserts this equivalence for all types $P$,$Q$, not necessarily propositions, with the [[identity type]] of the full [[universe of types]] on the left.

(e.g. [Sozeau-Tabareau, section 3.9](#SozeauTabareau))

## History

Specializing to the case where one of the propositions is 'true', [[George Boole]] can be taken (see [Voevodsky 14, slide 8](#Voevodsky14)) to be talking about propositional extensionality when he writes ([Boole 1853, p. 53](#Boole1853)):

> If instead of the proposition, "The sun shines," we say, "It is true that the sun shines," we then speak not directly of things, but of a proposition concerning things, viz., of the proposition "The sun shines." And, therefore, the proposition in which we thus speak is a secondary one.  Every primary proposition may thus give rise to a secondary proposition, viz., to that secondary proposition which asserts its truth, or declares its falsehood.

Later this became [[Alfred Tarski]]'s _material adequacy condition_, also known as _Convention T_:

> any viable theory of truth must entail, for every sentence $P$ of a language, a sentence of the form:

> $'P'$ is true if, and only if, $P$.

(see _[Wikipedia -- Semantic theory of truth -- Tarski's theory](https://en.wikipedia.org/wiki/Semantic_theory_of_truth#Tarski.27s_Theory)_)

This may be regarded as the above equivalence of propositional extensionality for the case that $Q \coloneqq$ [[true]]:

$$
  ('P' = 'true') \simeq (P \simeq true)
  \,.
$$

## See also

* [[extensionality]]

* [[set extensionality]]

## References

* {#Boole1853} [[George Boole]], _An Investigation of the Laws of Thought_, (1853) (retyped [pdf](http://www.gutenberg.org/files/15114/15114-pdf.pdf))

* {#SozeauTabareau} Matthieu Sozeau and Nicolas Tabareau, _Univalence For Free_ ([pdf](http://www.emn.fr/z-info/ntabareau/univalence_for_free/main.pdf))

* {#Voevodsky14} [[Vladimir Voevodsky]], _Foundations of Mathematics: their past, present and future, Part II_, ([slides](https://www.math.ias.edu/vladimir/sites/math.ias.edu.vladimir/files/2014_09_Bernays_2%20presentation.pdf))

[[!redirects material adequacy condition]]
[[!redirects material adequacy conditions]]

[[!redirects convention T]]
[[!redirects Convention T]]