
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Type theory
+-- {: .hide}
[[!include type theory - contents]]
=--
#### Foundations
+-- {: .hide}
[[!include foundations - contents]]
=--
=--
=--


# Judgments
* table of contents
{: toc}

## Idea

In [[formal logic]], a __judgment__, or __judgement__, is a "meta-[[proposition]]"; that is, a proposition belonging to the [[meta-language]] (the [[deductive system]] or [[logical framework]]) rather than to the [[object language]].

More specifically, any [[deductive system]] includes, as part of its specification, which strings of symbols are to be regarded as the _judgments_.  Some of these symbols may themselves express a [[proposition]] in the object language, but this is not necessarily the case.

The interest in judgements is typically in how they may arise as _theorems_, or as _consequences_ of other judgements, by way of the [[deduction]] rules in a deductive system.  One writes
$$\vdash J$$
to mean that $J$ is a judgment that is derivable, i.e. a [[theorem]] of the deductive system.


## Examples

### In first-order logic

In [[first-order logic]], a paradigmatic example of a judgement is the judgement that a certain string of symbols is a well-formed [[proposition]].  This is often written as "$P \;prop$", where $P$ is a [[metavariable]] standing for a string of symbols that denotes a proposition.

Another example of a judgement is the judgement that these symbols form a proposition [[proof|proved]] to be [[true]].  This judgment is often written as "$P\;true$".

Neither of these judgements is the same thing as the proposition $P$ itself.  In particular, the proposition is a statement *in* the logic, while the judgement that the proposition is a proposition, or is provably true, is a statement *about* the logic.  However, often people abuse notation and conflate a proposition with the judgment that it is true, writing $P$ instead of $P\;true$.


### In type theory

The distinction between judgements and [[propositions]] is particularly important in [[intensional type theory]].

The paradigmatic example of a judgment in [[type theory]] is a *typing judgment*.  The assertion that a [[term]] $t$ has [[type]] $A$ (written "$t:A$") is not a statement *in* the type theory (that is, not something which one could apply logical operators to in the type-theoretic system) but a statement *about* the type theory.

Often, type theories include only a particular small set of judgments, such as:

* typing judgments (written $t:A$, as above)

* judgments of typehood (usually written $A \;type$)

* judgments of [[equality]] between typed terms (written say $(t=t'):A$)

(In a type theory with a [[type of types]], judgments of typehood can sometimes be incorporated as a special case of typing judgments, writing $A:Type$ instead of $A\;type$.)

These limited sets of judgments are often defined [[inductive definition|inductively]] by giving [[type formation]]/[[term introduction]]/[[term elimination]]- and [[computation rules]] (see [[natural deduction]]) that specify under what hypotheses one is allowed to conclude the given judgment.

These inductive definitions can be formalized by choosing a particular [[type theory]] to be the meta-language; usually a very simple type theory suffices (such as a [[dependent type theory]] with only [[dependent product types]]).  Such a meta-type-theory is often called a [[logical framework]].


## Hypothetical and generic judgments

It may happen that a judgment $J$ is only derivable under the assumptions of certain other judgments $J_1,\dots, J_2$.  In this case one writes
$$ J_1,\dots,J_n \;\vdash J.$$
Often, however, it is convenient to incorporate hypotheticality into judgments themselves, so that $ J_1,\dots,J_n \;\vdash J $ becomes a single _[[hypothetical judgment]]_.  It can then be a consequence of other judgments, or (more importantly) a hypothesis used in concluding other judgments.  For instance, in order to conclude the truth of an [[implication]] $\phi\Rightarrow\psi$, we must conclude $\psi$ *assuming* $\phi$; thus the [[introduction rule]] for implication is
$$ \frac{\phi \;\vdash\; \psi}{\vdash\; \phi\Rightarrow\psi}$$
with a hypothetical judgment as its hypothesis.  See [[natural deduction]] for a more extensive discussion.

In a [[type theory]], we may also consider the case where the hypotheses $J_1$ are typing judgments of the form $x:A$, where $x$ is a [[variable]], and in which the conclusion judgment $J$ involves these variables as [[free variables]].  For instance, $J$ could be $\phi\;prop$, where $\phi$ is a valid (well-formed) proposition only when $x$ has a specific [[type]] $X$.  In this case we have a _[[generic judgement]]_, written
$$ (x \colon X) \;\vdash\; (\phi \; prop). $$
which expresses that _assuming the hypothesis or [[antecedent]] judgement_ that $x$ is of type $X$, as a consequence we have the [[succedent]] judgement that $\phi$ is a proposition. If on the right here we have a typing judgment 

$$
  (x \colon X) \;\vdash\; (t \colon A)
$$

we have a _[[term in context]]_.

For more about the precise relationship between the various meanings of $\vdash$ here, see [[natural deduction]] and [[logical framework]].

While this may seem to be a very basic form of (hypothetical/generic) judgement only, in systems such as [[dependent type theory]] or [[homotopy type theory]], all of [[logic]] and a good bit more is all based on just this.


## History of the notion and notation
 {#History}

\begin{imagefromfile}
    "file_name": "Frege-Urtheil.jpg",
    "float": "right",
    "width": 570,
    "unit": "px",
    "margin": {
        "top": -10,
        "bottom": 20,
        "right": 10, 
        "left": 20
    }
\end{imagefromfile}


The terminology of *judgement* in [[formal logic]], and the notation

$$
  \vdash A
$$

for the *judgement* of *content* $A$ is due to [Frege (1879, §2)](#Frege1879) (Frege's *das Urtheil* -- or *das Urteil* in modern German spelling -- directly translates to: *the judgement*).

{#RusselWhiteheadAssertion} This notion and notation (often "Frege's Urteilsstrich" -- "judgement stroke") was adopted by [Russell & Whitehead (1910, p. xviii)](#RussellWhitehead1910), who however speak of "assertion" instead of "judgement"  --- see [Martin-Löf (1996, p. 6)](#Martin-Löf96) for speculation that these authors may have wanted "to avoid any association with Kantian philosophy" (cf. [below](#KantTheoryOfJudgement)):

\begin{imagefromfile}
    "file_name": "RussellWhitehead-Assertion.jpg",
    "width": 650,
    "unit": "px",
    "margin": {
        "top": -30,
        "bottom": 20,
        "right": 10, 
        "left": 20
    }
\end{imagefromfile}

and then by [Church (1940, §5)](#Church40) (without any attribution) --- now allowing hypotheses/assumptions on the left of the *Urteilsstrich* --- to mean *provable* under these assumptions:

\begin{imagefromfile}
    "file_name": "Church-ProvableUnderAssumptions.jpg",
    "width": 700,
    "unit": "px",
    "margin": {
        "top": -40,
        "bottom": 20,
        "right": 10, 
        "left": 20
    }
\end{imagefromfile}

Similarly, [Kochen (1961, p.2)](#Kochen61) introduced (in a context of [[model theory]]) the notation "$\mathfrak{A} \;\vDash\; P$" (apparently not actively remembering its historical origin, cf. [Kochen (2017)](#Kochen17)) for a notion in [[model theory]] pronounced  "$\mathfrak{A}$ *validates* $P$" --- which is at least closely related to these hypothetical judgements (and often used synonymously, e.g. [here](https://open.conted.ox.ac.uk/sites/open.conted.ox.ac.uk/files/resources/Create%20Document/Turnstiles.pdf)):

\begin{imagefromfile}
    "file_name": "Kochen-Validation.jpg",
    "width": 700,
    "unit": "px",
    "margin": {
        "top": -40,
        "bottom": 20,
        "right": 10, 
        "left": 20
    }
\end{imagefromfile}


The need (which had been contested by some logicians such as [[Ludwig Wittgenstein|Wittgenstein]], cf. [jstor:43154266](https://www.jstor.org/stable/43154266)) for Frege's distinction between a proposition "$A$" as such and its judgement/assertion/proof/validation "$\vdash A$" was vocally argued for by [Martin-Löf (1984, pp. 2)](#Martin-Löf84), [(1987)](#Martin-Löf87) and in [(1996, lectures 1-2)](#Martin-Löf96), together with a re-promotion of Frege's *Urteilsstrich* notation "$\vdash$" ([ML84, p. 2](#Martin-Löf84),  [ML96, p. 2, 6](#Martin-Löf96)):

\begin{imagefromfile}
    "file_name": "Martin-Loef--Judgement.jpg",
    "width": 620,
    "unit": "px",
    "margin": {
        "top": -30,
        "bottom": 20,
        "right": 10, 
        "left": 20
    }
\end{imagefromfile}



The notation for *hypothetical* judgements

\[
  \label{GenericHypotheticalJudgement}
  context \;\vdash\; judgement
\]

was then (without attribution to Church or Martin-Löf) adopted for [[dependent type theory]] in [Hofmann (1995, p. 31)](#Hofmann95), later published as [Hofmann (1997, p. 82)](#Hofmann97):

\begin{imagefromfile}
    "file_name": "Hofmann-judgements.jpg",
    "width": 610,
    "unit": "px",
    "margin": {
        "top": -20,
        "bottom": 20,
        "right": 10, 
        "left": 20
    }
\end{imagefromfile}

This eventually became the trademark of the practice of [[dependent type theory]] (though mostly used without any attribution), e.g.: [Jacobs (1998, p. 2, 121, 586)](dependent+type+theory#Jacobs98); [Bauer, Haselwarter & Lumsdaine (2020)](#BauerHaselwarterLumsdaine20).

(Curiously, apparently [[Per Martin-Löf|Martin-Löf]] did not actually use the general notation (eq:GenericHypotheticalJudgement) in publications: When in [1996, p. 29](#Martin-Löf96) it comes to hypothetical judgements, he switched to using just a vertical "$\vert$" instead of "$\vdash$".)

{#HistorySummary} In summary:

| terminology | author | 
| ------------|--------|
| *judgement* | [Frege (1879)](#Frege1879) |
| *assertion* | [Russell & Whitehead (1910)](#RussellWhitehead1910) |
| *proof*     | [Church (1940)](#Church40) |
| *validation* | [Kochen (1961)](#Kochen61) |
| *judgement* | [Martin-Löf (1984](#Martin-Löf84), [1996)](#Martin-Löf96) <br/> [Hofmann (1995](#Hofmann95), [1997)](#Hofmann97) |


\linebreak

## Related concepts

* [[infinite judgment]]

* [[natural deduction]], [[sequent calculus]]

* [[context]], [[context extension]]

* [[type theory]], [[dependent type theory]]


## References
 {#References}

{#PreHistory} Pre-history of the notion of judgement (*Urteil*) in (informal) logic:

* {#KantTheoryOfJudgement} SEP: *[Kant’s Theory of Judgment](https://plato.stanford.edu/entries/kant-judgment/)*

* [[Georg Hegel]], first section, second chapter of *[[Science of Logic]]* (1813)

* [[Franz Brentano]], *Psychologie vom empirischen Standpunkte* (1874) &lbrack;[web](https://archive.org/details/psychologievome00kraugoog/page/n8/mode/2up)&rbrack;

  see: SEP: *[Brentano’s Theory of Judgement](https://plato.stanford.edu/entries/brentano-judgement/)*

The origin of the notion of "judgement" (and of the notation "$\vdash$" for it) in [[formal logic]]:

* {#Frege1879} [[Gottlob Frege]], *Begriffsschrift* (1879) &lbrack;[web scan](https://gdz.sub.uni-goettingen.de/id/PPN538957069?tify=%7B%22pages%22%3A%5B4%5D%2C%22view%22%3A%22info%22%7D), [Wikipedia entry](https://en.wikipedia.org/wiki/Begriffsschrift)&rbrack;

and under the name "assertion" in:

* {#RussellWhitehead1910} [[Bertrand Russell]], [[Alfred Whitehead]], p. xviii in: *[[Principia Mathematica]]* (1910)

Keeping the symbol "$\vdash$", now allowing hypothesis on the left, but pronouning it as "[[proof]] under assumptions":

* {#Church40} [[Alonzo Church]], §5 of: *A Formulation of the Simple Theory of Types*, The Journal of Symbolic Logic **5** 2 (1940) 56-68  &lbrack;[doi:10.2307/2266170](https://doi.org/10.2307/2266170)&rbrack;

  > (see also at *[[simple type theory]]*)

Discussion in the context of what became known as [[Martin-Löf dependent type theory]]:

* {#Martin-Löf84} [[Per Martin-Löf]] (notes by [[Giovanni Sambin]]), p. 2-4 in: _Intuitionistic type theory_, Lecture in Padua 1984, Bibliopolis (1984) &lbrack;[pdf](https://archive-pml.github.io/martin-lof/pdfs/Bibliopolis-Book-retypeset-1984.pdf), [[MartinLofIntuitionisticTypeTheory.pdf:file]]&rbrack;

* {#Martin-Löf87} [[Per Martin-Löf]], *Truth of a proposition, evidence of a judgement, validity of a proof*, Synthese **73** (1987) 407–420 &lbrack;[doi:10.1007/BF00484985](https://doi.org/10.1007/BF00484985), [pdf](https://archive-pml.github.io/martin-lof/pdfs/Truth-of-a-Proposition-Evidence-of-a-Judgment-1987.pdf)&rbrack; 

* {#MartinLoef90} [[Per Martin-Löf]], _A path from logic to metaphysics_, talk at _Nuovi problemi della logica e della filosofia della scienza_, Jan 1990 ([pdf](https://github.com/michaelt/martin-lof/raw/master/pdfs/A-path-from-logic-to-metaphysics-1991.pdf))

* {#Martin-Löf96} [[Per Martin-Löf]], *On the Meanings of the Logical Constants and the Justifications of the Logical Laws*, Nordic Journal of Philosophical Logic, **1** 1 (1996) 11-60 &lbrack;[pdf](http://docenti.lett.unisi.it/files/4/1/1/6/martinlof4.pdf), [[MartinLofOnTheMeaning96.pdf:file]]&rbrack;

* {#Hofmann95} [[Martin Hofmann]], §2.1.2 in: *Syntax and semantics of dependent types*, Chapter 2 in: _Extensional concepts in intensional type theory_, Ph.D. thesis, University of Edinburgh (1995), Distinguished Dissertations, Springer (1997) &lbrack;[ECS-LFCS-95-327](http://www.lfcs.inf.ed.ac.uk/reports/95/ECS-LFCS-95-327/), [[HofmannExtensionalIntensionalTypeTheory.pdf:file]], [doi:10.1007/978-1-4471-0963-1](https://doi.org/10.1007/978-1-4471-0963-1)&rbrack;

  also published as:
  
* {#Hofmann97} [[Martin Hofmann]], p. 82 of: *Syntax and semantics of dependent types*, in *Semantics and logics of computation*, Publ. Newton Inst. **14**, Cambridge Univ. Press (1997) 79-130 &lbrack;[doi:10.1017/CBO9780511526619.004](https://doi.org/10.1017/CBO9780511526619.004)&rbrack;

Reviewed in:

* {#PfenningDavies01} [[Frank Pfenning]], Rowan Davies, §2, §3 of: _A judgemental reconstruction of modal logic_, Mathematical Structures in Computer Science **11** 4 (2001) 511-540 &lbrack;[doi:10.1017/S0960129501003322](https://doi.org/10.1017/S0960129501003322), [pdf](http://www.cs.cmu.edu/~fp/papers/mscs00.pdf)&rbrack;
 
Further discussion in 

* Greta Coraglia, [[Ivan Di Liberti]], *Context, Judgement, Deduction* &lbrack;[arXiv:2111.09438](https://arxiv.org/abs/2111.09438)&rbrack;

Textbook acccount in a context of [[programming languages]]:

* [[Robert Harper]], section I.3 of  _[[Practical Foundations for Programming Languages]]_ (2015)

The alternative notation "$\vDash$" for *satisfaction* with closely related (if different) usage [seems](https://mathshistory.st-andrews.ac.uk/Miller/mathsym/set/) to originate in 

* {#Kochen61} [[Simon Kochen]], p. 223 in: *Ultraproducts in the Theory of Models*, Ann. Math.  **74** 2 (1961) 221-261 &lbrack;[doi:10.2307/1970235](https://doi.org/10.2307/1970235)&rbrack;

whose author

> cannot recollect whether &lbrack;he&rbrack; originated it or took it from some other paper.

according to:

* {#Kochen17} [[Simon Kochen]], *Origins of the double turnstile*, FOM mailing list posting (Feb 2017) &lbrack;[web](https://cs.nyu.edu/pipermail/fom/2017-February/020265.html), [screenshot](/nlab/files/Kochen-OriginOfDoubleTurnstile.jpg)&rbrack;

See also:

* Formal Logic Wikibook: *[Satisfaction](https://en.wikibooks.org/wiki/Formal_Logic/Predicate_Logic/Satisfaction)*



[[!redirects judgment]]
[[!redirects judgments]]
[[!redirects judgement]]
[[!redirects judgements]]
[[!redirects hypothetical judgment]]
[[!redirects hypothetical judgments]]
[[!redirects hypothetical judgement]]
[[!redirects hypothetical judgements]]
[[!redirects generic judgment]]
[[!redirects generic judgments]]
[[!redirects generic judgement]]
[[!redirects generic judgements]]

[[!redirects assertion]]
[[!redirects assertions]]

[[!redirects validation]]
[[!redirects validations]]


