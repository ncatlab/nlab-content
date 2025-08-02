
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

In [[constructive mathematics]] (originally: [[intuitionistic logic]]), the *BHK interpretation* of [[logical connectives]] (due to [Kolmogorov (1932, p. 59)](#Kolmogorov32), [Troelstra (1969, §2)](#Troelstra69), see the comments on attribution [below](#Attribution)) is such that the resulting [[proposition]] is regarded as [[true]] only if it is possible to [[constructive mathematics|construct]] a [[proof]] of its [[assertion]].
 
For instance, to assert a [[logical conjunction]] ("and") or a [[universal quantification]] ("for all") is taken to mean to provide a proof for all the instances.
Dually, but more notably, to assert a [[logical disjunction]] ("or") or an [[existential quantification]] ("exists") is taken to mean to prove one of the instances, so that there is no intuitionistic existence statement without construction of an example (the "disjunction property", see [there](intuitionistic+logic#DisjunctionProperty)).

This constructive interpretation of logical truth is the crux of the rejection of the [[principle of excluded middle]] in [[intuitionism]]/[[constructive mathematics]], for it implies that to prove $P \vee (\not P)$ (which may superficially/classically seem tautologous) one must prove $P$ or one must prove $\not P$ --- but neither proof may be known (e.g. if $P$ = [[Riemann hypothesis]]). 
(Here the classical mathematician is regarded as "idealistic" in their assumption that either case must hold, even if it is impossible to tell which one.)

In short this means that a proposition is regarded a [[true]] if there is an [[algorithm]], hence a [[computable function]],  to realize its [[proof]] whence one also speaks of the *[[realizability]] interpretation*. 
Closely related to the point of being synonymous is the paradigm of *[[propositions as types]]* and *[[proofs as programs]]*, also known as the *[[Curry-Howard correspondence]]* in [[type theory]]. 

Indeed, the fully formal version of the BHK interpretation may be understood as being the [[inference rules]], specifically the [[term introduction rules]], of [[intuitionistic type theory]] (as amplified in [Girard (1989, §2)](#Girard89) and [Martin-Löf (1996, Lec 3)](#MartinLöf96)).

## In mathematical foundations

### Dependent type theory

In [[dependent type theory]], propositions are usually defined as [[subsingletons]], types $A$ in which given $x:A$ and $y:A$ one can construct an [[identification]] $p(x, y):\mathrm{Id}_A(x, y)$. Predicates on a type $A$ are families of subsingletons $P(x)$ indexed by $x:A$. 

The [[BHK interpretation]] of predicate logic is defined using basic type theoretic operations: Given two propositions $P$ and $Q$, purely $P$ or $Q$ is given by an element of the binary [[sum type]]

$$P + Q$$

and the pure existential quantifier of a [[predicate]] $P(x)$ on a type $A$ is given by an element of the [[dependent sum type]]

$$\sum_{x:A} P(x)$$

Also, 

* false is given by the [[empty type]]

* true is given by any [[contractible type]]

* implication is given by the [[function type]]
$$P \to Q$$

* conjunction is given by the binary [[product type]]
$$P \times Q$$

* and the universal quantification is given by the indexed [[Cartesian product]]
$$\prod_{x:A} P(x)$$

### Set theory

The BHK interpretation of logic is also possible to express in set theory; in particular, in the [[internal logic]] of the resulting [[category of sets]] that arises from the set theory. 

Propositions in the internal logic are given by the [[subsingletons]], which are the sets $A$ in which for all $x$ and $y$ in $A$, $x = y$. Given any [[singleton]] $\{*\}$, any external proposition $P$ can be turned into an subsingleton via the subset 

$$\{p \in \{*\} \vert (p = *) \wedge P\}$$

This means that one can use the set-theoretic operations to define the [[BHK interpretation]] of predicate logic: Given two propositions $P$ and $Q$, purely $P$ or $Q$ is given by an element of the binary [[disjoint union]]

$$\{p \in \{*\} \vert (p = *) \wedge P\} \uplus \{p \in \{*\} \vert (p = *) \wedge Q\}$$

and the pure existential quantifier of a [[predicate]] $P(x)$ on a set $A$ is given by an element of the indexed [[disjoint union]]

$$\biguplus_{x \in A} \{p \in \{*\} \vert (p = *) \wedge P(x)\}$$

Also, 

* false is given by the [[empty set]], which is isomorphic to 
$$\{p \in \{*\} \vert (p = *) \wedge \bot\}$$

* true is given by any [[singleton]], which is isomorphic to 
$$\{p \in \{*\} \vert (p = *) \wedge \top\}$$

* implication is given by the [[function set]]
$${\{p \in \{*\} \vert (p = *) \wedge Q\}}^{\{p \in \{*\} \vert (p = *) \wedge P\} }$$

* conjunction is given by the binary [[Cartesian product]]
$$\{p \in \{*\} \vert (p = *) \wedge P\} \times \{p \in \{*\} \vert (p = *) \wedge Q\}$$

* and the universal quantification is given by the indexed [[Cartesian product]]
$$\prod_{x \in A} \{p \in \{*\} \vert (p = *) \wedge P(x)\}$$

Using this one can translate any theorems and proofs of set-level mathematics done in dependent type theory using the BHK interpretation over to set theory. 

## Historical versions
 {#HistoricalVersions}

The BHK interpretation evolved from a rather informal statement in [Kolmogorov (1932, p. 59)](#Kolmogorov32), over a more pronounced but still informal statement due to [Troelstra (1969, p. 5)](#Troelstra69), to the modern [[inference rules]] in [[intuitionistic type theory]] due to [Martin-Löf 75](Martin-Löf+dependent+type+theory#MartinLof75) (gentle exposition in [Martin-Löf (1996, Lec 3)](#MartinLöf96)):

From [Kolmogorov (1932, p. 59)](#Kolmogorov32):

\begin{imagefromfile}
    "file_name": "KolmogorovIntroducingBHK.jpg",
    "width": 540,
    "unit": "px",
    "margin": {
        "top": -30,
        "bottom": 20,
        "right": 0, 
        "left": 10
    }
\end{imagefromfile}


From [Heyting (1956, p. 97)](#Heyting56):

\begin{imagefromfile}
    "file_name": "HeytingIntroducingBHK.jpg",
    "width": 500,
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


{#FromTroelstraVanDalen88} From [Troelstra & van Dalen (1988)](#TroelstraVanDalen88):

\begin{imagefromfile}
    "file_name": "Troelstra-VanDalen-BHKInterpretation.jpg",
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

The idea of the interpretation is clearly expressed in [Kolmogorov (1932, p. 59)](#Kolmogorov32), though rather briefly and in unusual terminology: Instead of *propositions*, Kolmogorov speaks of *Aufgaben* (Deutsch for "tasks", but here in the sense used in math classes where it means "exercises" or "mathematical problems") in order to amplify the [[constructive mathematics|constructive]] aspects (he expands it out to *Konstruktionsaufgabe*, meaning "construction task").

While [[Arend Heyting]] may have been speaking of the idea of the "proof interpretation" of propositions since the 1930s, the first recognizable statement of what later was called the BHK interpretation is given in [Heyting (1956, §7.1.1)](#Heyting56).

The statement of the interpretation close to its modern formulation (but clearly of the same conceptual content as previously expressed in [Kolmogorov (1932, p. 59)](#Kolmogorov32) and [Heyting (1956, §7.1.1)](#Heyting56)) was then made explicit in [Troelstra (1969, §2)](#Troelstra69), where it is not attributed to anyone but presented as if the author's invention. 

Later, [Troelstra (1977, §2)](#Troelstra77) credits the idea to "Brouwer-Heyting-*Kreisel* (BHK)", not mentioning Kolmogorov --- indeed [Kreisel (1965)](#Kreisel65) is the only reference that [Troelstra (1969, §2)](#Troelstra69) makes explicit use of. 
(While this is the origin of the term "BHK interpretation", the adjustment/correction of its expanded version by exchanging "*K*reisel" for "*K*olmogorov" seems to be due to [Troelstra (1990, §2.1)](#Troelstra90).)

Still later, [Girard (1989, §1.2.2)](#Girard89) presents the same idea as "Heyting's semantics" (not mentioning anyone else, nor actually citing Heyting).

More discussion of this history is in *[SEP: "The Development of Intuitionistic Logic"](https://plato.stanford.edu/entries/intuitionistic-logic-development/)*.

Notice that Brouwer never explicitly formulated any interpretation of the kind that [Troelstra (1977, §2)](#Troelstra77) attributes to him, and in fact remained against all formalism his entire life. (His role in this history is to provide motivation and inspiration for Heyting and Kolmogorov.) Moreover, [Escardo & Xu (2015)](#EscardoXu15) have shown that Brouwer's famous intuitionistic theorem "all functions $\mathbb{N}^{\mathbb{N}} \to \mathbb{N}$ are continuous" is actually inconsistent under a literal version of this interpretation (i.e. without including [[propositional truncation]]).  

Thus, perhaps it should be called the "Heyting-Kolmogorov" interpretation. 

## Related concepts

* [[realizability topos]]

* [[computational trinitarianism]]

## References 

Original articles on [[intuitionism]] and, eventually, on [[intuitionistic logic]]:

* [[Arend Heyting]], *Die intuitionistische Grundlegung der Mathematik*, Erkenntnis **2** (1931) 106-115 &lbrack;[jsotr:20011630](https://www.jstor.org/stable/20011630), [pdf](http://www.psiquadrat.de/downloads/heyting1931.pdf)&rbrack;

* {#Kolmogorov32} [[Andrey Kolmogorov]], *Zur Deutung der intuitionistischen Logik*, Math. Z. **35** (1932) 58-65 &lbrack;[doi:10.1007/BF01186549](https://link.springer.com/article/10.1007/BF01186549)&rbrack;

* [[Hans Freudenthal]], *Zur intuitionistischen Deutung logischer Formeln*, Comp. Math. **4** (1937) 112-116 &lbrack;[numdam:CM_1937__4__112_0](http://www.numdam.org/item/?id=CM_1937__4__112_0)&rbrack;

* [[Arend Heyting]], *Bemerkungen zu dem Aufsatz von Herrn Freudenthal "Zur intuitionistischen Deutung logischer Formeln"*, Comp. Math. **4** (1937) 117-118 &lbrack;[doi:CM_1937__4__117_0](http://www.numdam.org/item/?id=CM_1937__4__117_0)&rbrack;

* [[L. E. J. Brouwer]], *Points and Spaces*, Canadian Journal of Mathematics **6** (1954) 1-17 &lbrack;[doi:10.4153/CJM-1954-001-9](https://doi.org/10.4153/CJM-1954-001-9)&rbrack;

Early monographs:

* {#Heyting56} [[Arend Heyting]], *Intuitionism: An introduction*, Studies in Logic and the Foundations of Mathematics, North-Holland (1956, 1971) &lbrack;[ISBN:978-0720422399]()&rbrack;

* {#Kreisel65} [[Georg Kreisel]], Section 2 of: *Mathematical Logic*,  in T. Saaty et al. (ed.), *Lectures on Modern Mathematics III*, Wiley New York (1965) 95-195

* {#TroelstraVanDalen88} [[Anne Sjerp Troelstra]], [[Dirk van Dalen]], Section 3.1 of: *Constructivism in Mathematics -- An introduction*, Vol 1, Studies in Logic and the Foundations of Mathematics **121**, North Holland (1988) &lbrack;[ISBN:9780444702661](https://www.elsevier.com/books/constructivism-in-mathematics-vol-1/troelstra/978-0-444-70266-1)&rbrack;

Early historical review:

* {#Troelstra90} [[Anne Sjerp Troelstra]], *On the Early History of Intuitionistic Logic*, in *Mathematical Logic*, Springer, (1990) &lbrack;[doi:10.1007/978-1-4613-0609-2_1](https://doi.org/10.1007/978-1-4613-0609-2_1)&rbrack;

Recognizable formulation of the so-called "BHK interretation" first appears in:

* [Kolmogorov (1932, p. 59)](#Kolmogorov32)

(who however speaks not of propositions but of *Aufgaben*, i.e. "tasks", here in the sense of: "mathematical problems") 

* [Heyting (1956, §7.1.1)](#Heyting56)

(who is maybe the first to speak of the "meaning of logical connectives") and then 

* {#Troelstra69} [[Anne Sjerp Troelstra]], §2 of: *Principles of Intuitionism*, Lecture Notes in Mathematics **95** Springer Heidelberg (1969)  &lbrack;[doi:10.1007/BFb0080643](https://link.springer.com/book/10.1007/BFb0080643)&rbrack;

(where it is presented as if the author's invention) and then recalled in

* {#Troelstra77} [[Anne Sjerp Troelstra]], §2 of: *Aspects of Constructive Mathematics*, Studies in Logic and the Foundations of Mathematics **90** 973-1052 (1977) &lbrack;<a href="https://doi.org/10.1016/S0049-237X(08)71127-3">doi:10.1016/S0049-237X(08)71127-3</a>&rbrack;

(where the same is now called the "Brouwer-Heyting-*Kreisel (BHK)* explanation" --- not mentioning Kolmogorov).

and later recalled in the context of [[constructive analysis]]:

* [[Douglas Bridges]], p. 96 of: *Constructive mathematics: a foundation for computable analysis*, Theoretical Computer Science **219** 1–2 (1999) 95-109 &lbrack;<a href="https://doi.org/10.1016/S0304-3975(98)00285-0">doi:10.1016/S0304-3975(98)00285-0</a>&rbrack;


This lead to the formulation of [[intuitionistic type theory]] in

* {#MartinLof75} [[Per Martin-Löf]], _An intuitionistic theory of types: predicative part_, in: H. E. Rose, J. C. Shepherdson (eds.), *Logic Colloquium '73, Proceedings of the Logic Colloquium*, Studies in Logic and the Foundations of Mathematics **80**, Elsevier (1975) 73-118 &lbrack;<a href="https://doi.org/10.1016/S0049-237X(08)71945-1">doi:10.1016/S0049-237X(08)71945-1</a>, [CiteSeer](http://citeseerx.ist.psu.edu/viewdoc/summary?doi=10.1.1.131.926)&rbrack;

reviewed in

* {#Girard89} [[Jean-Yves Girard]] (translated and with appendices by [[Paul Taylor]] and [[Yves Lafont]]), §1.2.2 of: *Proofs and Types*, Cambridge University Press (1989) &lbrack;[ISBN:978-0-521-37181-0](), [webpage](http://www.paultaylor.eu/stable/Proofs+Types.html), [pdf](https://www.paultaylor.eu/stable/prot.pdf)&rbrack;

(where it is called *Heyting semantics*) and then in

* {#MartinLöf96} [[Per Martin-Löf]], Lecture 3 of: *On the Meanings of the Logical Constants and the Justifications of the Logical Laws*, Nordic Journal of Philosophical Logic, **1** 1 (1996) 11-60 &lbrack;[pdf](http://docenti.lett.unisi.it/files/4/1/1/6/martinlof4.pdf), [[MartinLofOnTheMeaning96.pdf:file]]&rbrack;
 


See also:

* Wikipedia, _[BHK interpretation](http://en.wikipedia.org/wiki/BHK_interpretation)_

* Stanford Encyclopedia of Philosophy, *[The Development of Intuitionistic Logic](https://plato.stanford.edu/entries/intuitionistic-logic-development/#ProoInte)*



* Wouter Pieter Stekelenburg, _Realizability Categories_, ([arXiv:1301.2134](http://arxiv.org/abs/1301.2134)).

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

category: logic, philosophy