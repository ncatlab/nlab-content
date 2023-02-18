
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
 {#Idea}

In [[constructive mathematics]] (originally: [[intuitionistic logic]]), the *BHK interpretation* of [[logical connectives]] (due to [Kolmogorov (1932, p. 59)](#Kolmogorov32), [Troelstra (1969, §2)](#Troelstra69), see the comments on attribution [below](#Attribution)) is such that the resulting [[proposition]] is regarded as [[true]] if it is possible to [[constructive mathematics|construct]] a [[proof]] of its [[assertion]]. 

For instance, to assert a [[logical disjunction]] ("and") or a [[universal quantification]] ("for all") is taken to mean to provide a proof of all the instances.

Dually but more notably, to assert a [[logical disjunction]] ("or") or an [[existential quantification]] ("exists") is taken to mean to prove one of the instances, so that there is no intuitionistic existence statement without construction of an example (the "disjunction property", see [there](intuitionistic+logic#DisjunctionProperty)).

This constructive interpretation of logical truth is the crux of the rejection of the [[principle of excluded middle]] in [[intuitionism]]/[[constructive mathematics]], for it implies that to prove $P \vee (\not P)$ (which may superficially/classically seem tautologous) one must prove $P$ or one must prove $\not P$ --- but neither proof may be known (e.g. if $P$ = [[Riemann hypothesis]]). 

(Here the classical mathematician is regarded as "idealistic" in their assumption that either case must hold, even if it is impossible to tell which one.)

In short this means that a proposition is regarded a [[true]] if there is an [[algorithm]], hence a [[computable function]],  to realize its [[proof]] whence one also speaks of the *[[realizability]] interpretation*. 

Closely related to the point of being synonymous is the paradigm of *[[propositions as types]]* and *[[proofs as programs]]*, also known as the *[[Curry-Howard correspondence]]* in [[type theory]]. 

Indeed, the fully formal version of the BHK interpretation may be understood as being the [[inference rules]], specifically the [[term introduction rules]], of [[intuitionistic type theory]] (as amplified in [Girard (1989, §2)](#Girard89) and [Martin-Löf (1996, Lec 3)](#MartinLöf96)).



## Historical versions
 {#HistoricalVersions}

The BHK interpretation evolved from a rather informal statement in [Kolmogorov (1932, p. 59)](#Kolmogorov32), over a more pronounced but still informal statement due to [Troelstra (1969, p. 5)](#Troelstra69), to the modern [[inference rules]] in [[intuitionistic type theory]] due to [Martin-Löf 75](Martin-Löf+dependent+type+theory#MartinLof75) (gentle exposition in [Martin-Löf (1996, Lec 3)](#MartinLöf96)):

\linebreak

From [Kolmogorov (1932, p. 59)](#Kolmogorov32):

\begin{imagefromfile}
    "file_name": "KolmogorovIntroducingBHK.jpg",
    "width": 520,
    "unit": "px",
    "margin": {
        "top": -30,
        "bottom": 20,
        "right": 0, 
        "left": 10
    }
\end{imagefromfile}


From [Troelstra (1969, p. 5)](#Troelstra69):

\begin{imagefromfile}
    "file_name": "Troelstra-IntroducingBHKInterp.jpg",
    "width": 660,
    "unit": "px",
    "margin": {
        "top": -30,
        "bottom": 20,
        "right": 0, 
        "left": 10
    }
\end{imagefromfile}

From [Troelstra (1977, p. 977)](#Troelstra77):

\begin{imagefromfile}
    "file_name": "Troelstra-AttributingBHK.jpg",
    "width": 500,
    "unit": "px",
    "margin": {
        "top": -30,
        "bottom": 20,
        "right": 0, 
        "left": 10
    }
\end{imagefromfile}


{#FromBridges} From [Bridges (1999), p. 96](#Bridges99):

\begin{imagefromfile}
    "file_name": "Bridges-IntuitInterpOfConnectives.jpg",
    "width": 600,
    "unit": "px",
    "margin": {
        "top": -30,
        "bottom": 20,
        "right": 0, 
        "left": 10
    }
\end{imagefromfile}


The analogous discussion for [[inference rules]] in [[intuitionistic type theory]] is then given in [Martin-Löf (1975)](#MartinLof75),
reviewed in [Girard (1989, §2)](#Girard89) and with more emphasis in [Martin-Löf (1996, Lec 3)](#MartinLöf96).





## Attribution
 {#Attribution}

The idea of the interpretation is clearly expressed in [Kolmogorov (1932, p. 59)](#Kolmogorov32), though rather briefly and in unusual terminology: Instead of *propositions*, Kolmogorov speaks of *Aufgaben* (Deutsch for "task", but here in the sense used in math classes where it means "exercise" or "mathematical problem") in order to amplify the [[constructive mathematics|constructive]] aspects (he expands it out to *Konstruktionsaufgabe*, meaning "construction task").

The interpretation was then made quite explicit in [Troelstra (1969, §2)](#Troelstra69), where it is not attributed to anyone but the author's invention. 

Later, [Troelstra (1977, §2)](#Troelstra77) credits the idea to "Brouwer-Heyting-*Kreisel* (BHK)" (not mentioning Kolmogorov --- indeed [Kreisel (1965)](#Kreisel65) is the only reference that [Troelstra (1969, §2)](#Troelstra69) made explicit use of). 

Still later, [Girard (1989, §1.2.2)](#Girard89) presents the same idea as "Heyting's semantics" (not mentioning anyone else).

Certainly Brouwer never explicitly formulated any interpretation of this sort, and remained against all formalism his entire life.  Moreover, [Escardo & Xu (2015)](#EscardoXu15) have shown that Brouwer's famous intuitionistic theorem "all functions $\mathbb{N}^{\mathbb{N}} \to \mathbb{N}$ are continuous" is actually inconsistent under a literal version of this interpretation (i.e. without including [[propositional truncation]]).  Thus, perhaps it should only be called the "Heyting-Kolmogorov" interpretation. 

## Related concepts

* [[realizability topos]]

* [[computational trinitarianism]]

## References 

Original articles on [[intuitionistic logic]]:

* [[Arend Heyting]], *Die intuitionistische Grundlegung der Mathematik*, Erkenntnis **2** (1931) 106-115 &lbrack;[jsotr:20011630](https://www.jstor.org/stable/20011630), [pdf](http://www.psiquadrat.de/downloads/heyting1931.pdf)&rbrack;

* {#Kolmogorov32} [[Andrey Kolmogorov]], *Zur Deutung der intuitionistischen Logik*, Math. Z. **35** (1932) 58-65 &lbrack;[doi:10.1007/BF01186549](https://link.springer.com/article/10.1007/BF01186549)&rbrack;

* [[Hans Freudenthal]], *Zur intuitionistischen Deutung logischer Formeln*, Comp. Math. **4** (1937) 112-116 &lbrack;[numdam:CM_1937__4__112_0](http://www.numdam.org/item/?id=CM_1937__4__112_0)&rbrack;

* [[Arend Heyting]], *Bemerkungen zu dem Aufsatz von Herrn Freudenthal "Zur intuitionistischen Deutung logischer Formeln"*, Comp. Math. **4** (1937) 117-118 &lbrack;[doi:CM_1937__4__117_0](http://www.numdam.org/item/?id=CM_1937__4__117_0)&rbrack;

* [[L. E. J. Brouwer]], *Points and Spaces*, Canadian Journal of Mathematics **6** (1954) 1-17 &lbrack;[doi:10.4153/CJM-1954-001-9](https://doi.org/10.4153/CJM-1954-001-9)&rbrack;

* {#Kreisel65} [[Georg Kreisel]], Section 2 of: *Mathematical Logic*,  in T. Saaty et al. (ed.), *Lectures on Modern Mathematics III*, Wiley New York (1965) 95-195

Recognizable formulation of the so-called "BHK interretation" first appears in:

* {#Troelstra69} [[Anne Sjerp Troelstra]], §2 of: *Principles of Intuitionism*, Lecture Notes in Mathematics **95** Springer Heidelberg (1969)  &lbrack;[doi:10.1007/BFb0080643](https://link.springer.com/book/10.1007/BFb0080643)&rbrack;

(where it is presented as the author's invention) and then recalled in

* {#Troelstra77} [[Anne Sjerp Troelstra]], §2 of: *Aspects of Constructive Mathematics*, Studies in Logic and the Foundations of Mathematics **90** 973-1052 (1977) &lbrack;<a href="https://doi.org/10.1016/S0049-237X(08)71127-3">doi:10.1016/S0049-237X(08)71127-3</a>&rbrack;

(where the same is now called the "Brouwer-Heyting-*Kreisel* explanation").

and later recalled in the context of [[constructive analysis]]:

* [[Douglas Bridges]], p. 96 of: *Constructive mathematics: a foundation for computable analysis*, Theoretical Computer Science **219** 1–2 (1999) 95-109 &lbrack;<a href="https://doi.org/10.1016/S0304-3975(98)00285-0">doi:10.1016/S0304-3975(98)00285-0</a>&rbrack;


This lead to the formulation of [[intuitionistic type theory]] in

* {#MartinLof75} [[Per Martin-Löf]], _An intuitionistic theory of types: predicative part_, in: H. E. Rose, J. C. Shepherdson (eds.), *Logic Colloquium '73, Proceedings of the Logic Colloquium*, Studies in Logic and the Foundations of Mathematics **80**, Elsevier (1975) 73-118 &lbrack;<a href="https://doi.org/10.1016/S0049-237X(08)71945-1">doi:10.1016/S0049-237X(08)71945-1</a>, [CiteSeer](http://citeseerx.ist.psu.edu/viewdoc/summary?doi=10.1.1.131.926)&rbrack;

reviewed in

* {#Girard89} [[Jean-Yves Girard]] (translated and with appendiced by [[Paul Taylor]] and [[Yves Lafont]]), §1.2.2 of: *Proofs and Types*, Cambridge University Press (1989) &lbrack;[ISBN:978-0-521-37181-0](), [webpage](http://www.paultaylor.eu/stable/Proofs+Types.html), [pdf](https://www.paultaylor.eu/stable/prot.pdf)&rbrack;

(where it is called *Heyting semantics*) and then in

* {#MartinLöf96} [[Per Martin-Löf]], Lecture 3 of: *On the Meanings of the Logical Constants and the Justifications of the Logical Laws*, Nordic Journal of Philosophical Logic, **1** 1 (1996) 11-60 &lbrack;[pdf](http://docenti.lett.unisi.it/files/4/1/1/6/martinlof4.pdf), [[MartinLofOnTheMeaning96.pdf:file]]&rbrack;
 


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