
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Type theory
+-- {: .hide}
[[!include type theory - contents]]
=--
#### Constructivism, Realizability, Computability
+-- {: .hide}
[[!include constructivism - contents]]
=--
=--
=--



# Contents
* table of contents
{: toc}

## Idea

What came to be called the *BHK interpretation* of [[intuitionistic logic]] (see the attribution [below](#Attribution)) is a description of [[proofs]] of [[propositions]] in [[intuitionistic logic]] as [[functions]], often [[computable functions]], where it is also called the _[[realizability]] interpretation_. 

See at [Intuitionistic logic -- Constructive interpretation of connectives](intuitionistic+logic#ConstructiveInterpretationOfConnectives).

This is otherwise known as the paradigm of _[[propositions as types]]_ and _[[proofs as programs]]_, and in a precise form as the [[Curry-Howard correspondence]]. See there for more.

## Attribution
 {#Attribution}

The interpretation was first made explicit in [Troelstra (1969, §2)](#Troelstra69), where it is not attributed to anyone but the author's invention. 

Later, [Troelstra (1977, §2)](#Troelstra77) credits the idea to "Brouwer-Heyting-*Kreisel* (BHK)" (not mentoning Kolmogorov --- indeed [Kreisel (1965)](#Kreisel65) is the only reference that [Troelstra (1969, §2)](#Troelstra69) made explicit use of). 

Still later, [Girard (1989, §1.2.2)](#Girard89) presents the same idea as "Heyting's semantics" (not mentioning anyone else)

Certainly Brouwer never explicitly formulated any interpretation of this sort, and remained against all formalism his entire life.  Moreover, [Escardo & Xu (2015)](#EscardoXu15) have shown that Brouwer's famous intuitionistic theorem "all functions $\mathbb{N}^{\mathbb{N}} \to \mathbb{N}$ are continuous" is actually inconsistent under a literal version of this interpretation (i.e. without including [[propositional truncation]]).  Thus, perhaps it should only be called the "Heyting-Kolmogorov" interpretation. 

## Related concepts

* [[realizability topos]]

* [[computational trinitarianism]]

## References 

Original articles on [[intuitionistic logic]]:

* [[Arend Heyting]], *Die intuitionistische Grundlegung der Mathematik*, Erkenntnis **2** (1931) 106-115 &lbrack;[jsotr:20011630](https://www.jstor.org/stable/20011630), [pdf](http://www.psiquadrat.de/downloads/heyting1931.pdf)&rbrack;

* [[Andrey Kolmogorov]], *Zur Deutung der intuitionistischen Logik*, Math. Z. **35** (1932) 58-65 &lbrack;[doi:10.1007/BF01186549](https://link.springer.com/article/10.1007/BF01186549)&rbrack;

* [[Hans Freudenthal]], *Zur intuitionistischen Deutung logischer Formeln*, Comp. Math. **4** (1937) 112-116 &lbrack;[numdam:CM_1937__4__112_0](http://www.numdam.org/item/?id=CM_1937__4__112_0)&rbrack;

* [[Arend Heyting]], *Bemerkungen zu dem Aufsatz von Herrn Freudenthal "Zur intuitionistischen Deutung logischer Formeln"*, Comp. Math. **4** (1937) 117-118 &lbrack;[doi:CM_1937__4__117_0](http://www.numdam.org/item/?id=CM_1937__4__117_0)&rbrack;

* [[L. E. J. Brouwer]], *Points and Spaces*, Canadian Journal of Mathematics **6** (1954) 1-17 &lbrack;[doi:10.4153/CJM-1954-001-9](https://doi.org/10.4153/CJM-1954-001-9)&rbrack;

* {#Kreisel65} [[Georg Kreisel]], Section 2 of: *Mathematical Logic*,  in T. Saaty et al. (ed.), *Lectures on Modern Mathematics III*, Wiley New York (1965) 95-195

Recognizable formulation of the so-called "BHK interretation" first appears in:

* {#Troelstra69} [[Anne Sjerp Troelstra]], §2 of: *Principles of Intuitionism*, Lecture Notes in Mathematics **95** Springer Heidelberg (1969)  &lbrack;[doi:10.1007/BFb0080643](https://link.springer.com/book/10.1007/BFb0080643)&rbrack;

(where it is presented as the author's invention) and then in

* {#Troelstra77} [[Anne Sjerp Troelstra]], §2 of: *Aspects of Constructive Mathematics*, Studies in Logic and the Foundations of Mathematics **90** 973-1052 (1977) &lbrack;<a href="https://doi.org/10.1016/S0049-237X(08)71127-3">doi:10.1016/S0049-237X(08)71127-3</a>&rbrack;

(where the same is now called the "Brouwer-Heyting-*Kreisel* explanation")

and then in the context of [[intuitionistic type theory]]:

* {#Girard89} [[Jean-Yves Girard]] (translated and with appendiced by [[Paul Taylor]] and [[Yves Lafont]]), §1.2.2 of: *Proofs and Types*, Cambridge University Press (1989) &lbrack;[ISBN:978-0-521-37181-0](), [webpage](http://www.paultaylor.eu/stable/Proofs+Types.html), [pdf](https://www.paultaylor.eu/stable/prot.pdf)&rbrack;

(where it is called *Heyting semantics*)

* {#MartinLöf96} [[Per Martin-Löf]], Lecture 3 of: *On the Meanings of the Logical Constants and the Justifications of the Logical Laws*, Nordic Journal of Philosophical Logic, **1** 1 (1996) 11-60 &lbrack;[pdf](http://docenti.lett.unisi.it/files/4/1/1/6/martinlof4.pdf), [[MartinLofOnTheMeaning96.pdf:file]]&rbrack;
 
and recalled in a context of [[constructive analysis]]:

* [[Douglas Bridges]], p. 96 of: *Constructive mathematics: a foundation for computable analysis*, Theoretical Computer Science **219** 1–2 (1999) 95-109 &lbrack;<a href="https://doi.org/10.1016/S0304-3975(98)00285-0">doi:10.1016/S0304-3975(98)00285-0</a>&rbrack;


See also:

* Wikipedia, _[BHK interpretation](http://en.wikipedia.org/wiki/BHK_interpretation)_

* Wouter Pieter Stekelenburg, _Realizability Categories_ , ([arXiv:1301.2134](http://arxiv.org/abs/1301.2134)).

* {#EscardoXu15} [[Martin Escardo]], Chuangjie Xu, _The inconsistency of a Brouwerian continuity principle with the Curry--Howard interpretation_, 13th International Conference on Typed Lambda Calculi and Applications (TLCA 2015), Leibniz International Proceedings in Informatics (LIPIcs) *38* (2015) &lbrack;[doi:10.4230/LIPIcs.TLCA.2015.153](https://doi.org/10.4230/LIPIcs.TLCA.2015.153), [pdf](http://www.cs.bham.ac.uk/%7Emhe/papers/escardo-xu-inconsistency-continuity.pdf)&rbrack;


* E. G. F. D&#237;ez, _Five observations concerning the intended meaning of the intuitionistic logical constants_ , J. Phil. Logic **29** no. 4 (2000) pp.409&#8211;424 . ([preprint](https://webs.um.es/picazo/miwiki/lib/exe/fetch.php?id=inicio&cache=cache&media=five_observations_2000_jour_of_phil_logic_29_4_pp409_424.pdf))



Links to many papers on realizability and related topics may be found [here](http://www.staff.science.uu.nl/~ooste110/realizability.html).

For a comment see also 

* [[Robert Harper]], _Extensionality, Intensionality, and Brouwer's Dictum_ ([web](http://existentialtype.wordpress.com/2012/08/11/extensionality-intensionality-and-brouwers-dictum/))

[[!redirects Brouwer-Heyting-Kolmogorov interpretation]]

[[!redirects Brouwer Heyting Kolmogorov interpretation]] 
[[!redirects Brouwer-Heyting-Kolmogorov interpretation]] 
[[!redirects Brouwer–Heyting–Kolmogorov interpretation]] 
[[!redirects BHK interpretation]] 

[[!redirects realizability interpretation]] 
[[!redirects realisability interpretation]] 

[[!redirects BHK correspondence]]