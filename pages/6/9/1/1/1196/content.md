
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Foundations
+-- {: .hide}
[[!include foundations - contents]]
=--
=--
=--

# Contents
* table of contents
{:toc}

## Idea

__Intuitionistic logic__ was introduced by [[Arend Heyting]] as a [[logic]] for [[Brouwer]]\'s [[intuitionistic mathematics]].  It applies more generally to [[constructive mathematics]] and so may also be called __constructive logic__.

Beware the terminological ambiguity: Some people insist that "intuitionistic logic" refers to Brouwerian intuitionism, which includes axioms that contradict classical logic; but other people use "intuitionistic" to mean the same as what in other contexts is called "constructive", i.e. mathematics without the [[principle of excluded middle]] or the [[axiom of choice]] but nothing added that contradicts them.  Some people (particularly material set theorists) use "constructive" to mean *predicative* constructive and "intuitionistic" to mean impredicative constructive.


## Idea

### General

Intuitionistic logic is most easily described as [[classical logic]] without the [[principle of excluded middle]] ($\vdash A \vee \neg{A}$) or the [[double-negation]] rule ($\neg\neg{A} \vdash A$).  It may also be defined by starting with Gentzen\'s [[sequent calculus]] for [[classical logic]] (with $\neg$ but not $\bot$) and restricting to sequents $\Gamma \vdash \Delta$ where $\Delta$ may contain *at most one* formula, or by starting with [[sequent calculus]] with $\bot$ and restricting to such sequents where $\Delta$ must contain *exactly one* formula.

### Constructive interpretation of connectives
 {#ConstructiveInterpretationOfConnectives}

The *intuitionistic interpretation* of the [[logical connectives]] (known as the [[BHK interpretation]], due to [Kolmogorov (1932, p. 59)](#Kolmogorov32), [Heyting (1956, §7.1.1)](#Heyting56), [Troelstra (1969, §2)](#Troelstra69)) is such that the resulting [[proposition]] is regarded as [[true]] only if it is possible to [[constructive mathematics|construct]] a [[proof]] of its [[assertion]]. 

For instance, to assert a [[logical conjunction]] ("and") or a [[universal quantification]] ("for all") is taken to mean to provide a proof of all the instances.

Dually but more notably, to assert a [[logical disjunction]] ("or") or an [[existential quantification]] ("exists") is taken to mean to prove one of the instances, so that there is no intuitionistic existence statement without construction of an example (the "disjunction property", see [below](#DisjunctionProperty)).

This constructive interpretation of logical truth is the crux of the rejection of the [[principle of excluded middle]], for it implies that to prove $P \vee (\not P)$ (which may superficially/classically seem tautologous) one must prove $P$ or one must prove $\not P$ --- but neither proof may be known (e.g. if $P$ = [[Riemann hypothesis]]). 

(Here the classical mathematician is regarded as "idealistic" in their assumption that either case must hold, even if it is impossible to tell which one.)

{#FromKolmogorov} From [Kolmogorov (1932, p. 59)](#Kolmogorov32):

\begin{imagefromfile}
    "file_name": "KolmogorovIntroducingBHK.jpg",
    "width": 550,
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


The analogous discussion for [[inference rules]] in [[intuitionistic type theory]] is then given spring in [Girard (1989, §2)](#Girard89) and with more emphasis in [Martin-Löf (1996, Lec 3)](#MartinLöf96).


## Properties

### Double negation
 {#DoubleNegation}

The [[double negation translation]] says that a [[proposition]] $P$ is provable in [[classical logic]] precisely if its [[double negation]] $\not \not P$ is provable in constructive logic.

### Disjunction property
 {#DisjunctionProperty}

Unlike classical logic, intuitionistic logic has the
_disjunction-_ and _existence_ properties (cf. [above](#ConstructiveInterpretationOfConnectives)): any [[proof]] of
$\vdash A \vee B$ must contain a proof of either $\vdash A$ or $\vdash B$, and similarly any proof of $\vdash \exists x.\,F(x)$ must
construct a term $t$ and a proof of $\vdash F(t)$.  These
properties are what justify our calling intuitionistic
logic 'constructive'.

On the other hand, (classical) [[Peano arithmetic]] is
conservative over (intuitionistic) [[Heyting arithmetic]] when
restricted to $\Pi^0_1$ formulas; that is, formulas of the
form $\forall x\colon N.\, \exists y\colon N.\, F(x,y)$.  Roughly speaking,
classical logic can be just as 'constructive' as
intuitionistic logic as far as proving the totality of
functions $\mathbb{N} \to \mathbb{N}$ is concerned.

## Classicality principles

The principle of [[excluded middle]] is not provable in intuitionistic logic, and if we assume it then the logic becomes [[classical logic]].  But there are other principles that are provable classically but not intuitionistically, but which are weaker than full PEM, such as

* various [[omniscience principles]] such as LPO and LLPO
* the [[double-negation shift]]
* [[de Morgan's law]], i.e. [[weak excluded middle]]
* the [[world's simplest axiom of choice]]

## Related concepts

* [[BHK interpretation]]

[[!include categories and logic - table]]

## References

Original articles on [[intuitionism]]:

* {#Heyting1930} [[Arend Heyting]], *Die formalen Regeln der intuitionistischen Logik. I, II, III.* Sitzungsberichte der Preußischen Akademie der Wissenschaften, Physikalisch-Mathematische Klasse (1930) 42-56, 57-71, 158-169

  abridged reprint in:

  Karel Berka, Lothar Kreiser (eds.), *Logik-Texte*, De Gruyter (1986) 188-192 &lbrack;[doi:10.1515/9783112645826](https://doi.org/10.1515/9783112645826)&rbrack;

* [[Arend Heyting]], *Die intuitionistische Grundlegung der Mathematik*, Erkenntnis **2** (1931) 106-115 &lbrack;[jsotr:20011630](https://www.jstor.org/stable/20011630), [pdf](http://www.psiquadrat.de/downloads/heyting1931.pdf)&rbrack;

* {#Kolmogorov32} [[Andrey Kolmogorov]], *Zur Deutung der intuitionistischen Logik*, Math. Z. **35** (1932) 58-65 &lbrack;[doi:10.1007/BF01186549](https://link.springer.com/article/10.1007/BF01186549)&rbrack;

* [[Hans Freudenthal]], *Zur intuitionistischen Deutung logischer Formeln*, Comp. Math. **4** (1937) 112-116 &lbrack;[numdam:CM_1937__4__112_0](http://www.numdam.org/item/?id=CM_1937__4__112_0)&rbrack;

* [[Arend Heyting]], *Bemerkungen zu dem Aufsatz von Herrn Freudenthal "Zur intuitionistischen Deutung logischer Formeln"*, Comp. Math. **4** (1937) 117-118 &lbrack;[doi:CM_1937__4__117_0](http://www.numdam.org/item/?id=CM_1937__4__117_0)&rbrack;

* [[L. E. J. Brouwer]], *Points and Spaces*, Canadian Journal of Mathematics **6** (1954) 1-17 &lbrack;[doi:10.4153/CJM-1954-001-9](https://doi.org/10.4153/CJM-1954-001-9)&rbrack;

Early monographs:

* {#Heyting56} [[Arend Heyting]], *Intuitionism: An introduction*, Studies in Logic and the Foundations of Mathematics, North-Holland (1956, 1971) &lbrack;[ISBN:978-0720422399]()&rbrack;

* {#Kreisel65} [[Georg Kreisel]], Section 2 of: *Mathematical Logic*,  in T. Saaty et al. (ed.), *Lectures on Modern Mathematics III*, Wiley New York (1965) 95-195

Early historical account:

* {#Troelstra90} [[Anne Sjerp Troelstra]], *On the Early History of Intuitionistic Logic*, in *Mathematical Logic*, Springer, (1990) &lbrack;[doi:10.1007/978-1-4613-0609-2_1](https://doi.org/10.1007/978-1-4613-0609-2_1)&rbrack;



Recognizable statemens of the [[BHK interpretation]] of [[intuitionistic logic]] appear in 

* [Kolmogorov (1932, p. 59)](#Kolmogorov32)

(who however speaks not of propositions but of *Aufgaben*, i.e. "tasks", here in the sense of: "mathematical problems") 

* [Heyting (1956, §7.1.1)](#Heyting56)

(who is maybe the first to speak of the "meaning of logical connectives")

and then in

* {#Troelstra69} [[Anne Sjerp Troelstra]], §2 of: *Principles of Intuitionism*, Lecture Notes in Mathematics **95** Springer Heidelberg (1969)  &lbrack;[doi:10.1007/BFb0080643](https://link.springer.com/book/10.1007/BFb0080643)&rbrack;

(where it is presented as the author's invention) and then in

* {#Troelstra77} [[Anne Sjerp Troelstra]], §2 of: *Aspects of Constructive Mathematics*, Studies in Logic and the Foundations of Mathematics **90** 973-1052 (1977) &lbrack;<a href="https://doi.org/10.1016/S0049-237X(08)71127-3">doi:10.1016/S0049-237X(08)71127-3</a>&rbrack;

(where the same is now called the "Brouwer-Heyting-*Kreisel* explanation", not mentioning Kolmogorov)

and then in the context of [[intuitionistic type theory]]:

* {#Girard89} [[Jean-Yves Girard]] (translated and with appendiced by [[Paul Taylor]] and [[Yves Lafont]]), §1.2.2 of: *Proofs and Types*, Cambridge University Press (1989) &lbrack;[ISBN:978-0-521-37181-0](), [webpage](http://www.paultaylor.eu/stable/Proofs+Types.html), [pdf](https://www.paultaylor.eu/stable/prot.pdf)&rbrack;

(where it is called *Heyting semantics*), further expanded on on:

* {#MartinLöf96} [[Per Martin-Löf]], Lecture 3 of: *On the Meanings of the Logical Constants and the Justifications of the Logical Laws*, Nordic Journal of Philosophical Logic, **1** 1 (1996) 11-60 &lbrack;[pdf](http://docenti.lett.unisi.it/files/4/1/1/6/martinlof4.pdf), [[MartinLofOnTheMeaning96.pdf:file]]&rbrack;
 
and recalled in the context of [[constructive analysis]]:

* {#Bridges99}  [[Douglas Bridges]], p. 96 of: *Constructive mathematics: a foundation for computable analysis*, Theoretical Computer Science **219** 1–2 (1999) 95-109 &lbrack;<a href="https://doi.org/10.1016/S0304-3975(98)00285-0">doi:10.1016/S0304-3975(98)00285-0</a>&rbrack;


See also:

* Wikipedia, *[Intuitionistic logic](https://en.wikipedia.org/wiki/Intuitionistic_logic)*

* Stanford Encyclopedia, *[The Development of Intuitionistic Logic](https://plato.stanford.edu/entries/intuitionistic-logic-development/#ProoInte)*

* Internet Encyclopedia of Philosophy, _[Intuitionism in Mathematics](https://iep.utm.edu/intuitionism-in-mathematics/) (especially the appendix)
 

The observation that the [[poset]] of [[open subsets]] of a [[topological space]] (the [[internal logic]] of the [[sheaf topos]]) serves as a model for [[intuitionistic logic]] is apparently originally due to

* {#Tarski} [[Alfred Tarski]], _Der Aussagenkalk&#252;l und die Topologie_, Fundamenta Mathematicae 31 (1938), pp. 103-134.
 

A textbook account in the context of [[programming languages]] is in section 30 of

* [[Robert Harper]], _[[Practical Foundations for Programming Languages]]_


[[!redirects intuitionistic logic]]
[[!redirects Intuitionistic logic]]
