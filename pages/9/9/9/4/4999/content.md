
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### $(0,1)$-Category theory
+--{: .hide}
[[!include (0,1)-category theory - contents]]
=--
#### Type theory
+-- {: .hide}
[[!include type theory - contents]]
=--
#### Modality
+-- {: .hide}
[[!include modalities - contents]]
=--
=--
=--

# Modal Logics
* table of contents
{:toc}

## Idea
 {#Idea}

The term _modal logic_ refers to an enrichment of standard [[formal logic]], where the standard [[logical conjunctions]] (*[[and]]*, *[[or]]*, *[[not]]*, *[[implication]]* and, [[first-order logic|perhaps]], *[[universal quantifier|for all]]*, *[[existential quantifier|exists]]* etc.) are accompanied by certain extra operations -- called _[[modal operators]]_ and traditionally denoted by symbols like "$\Box$", "$\lozenge$", , "$\bigcirc$" -- such that for $p$ any [[proposition]] an expression like $\Box p$ is a(nother) proposition whose interpretation is intended to be:

* "$p$ holds (only) _in a certain way_",

where the "certain way" is (implicitly) specified by whatever [[axioms]] are satisfied by the given [[modal operator]].

{#ModesOfBeing} In other words, [[modal operators]] in modal logic are meant to express a certain **mode of being true** --- and in generalization to [[modal type theory]] they express more generally a **mode of being**, whence the reference to  [[modalities]] as in [[Kant]]'s writings.

\begin{imagefromfile}
    "file_name": "LemmonScott-page1.jpg",
    "float": "right",
    "width": 370,
    "unit": "px",
    "margin": {
        "top": -50,
        "bottom": 20,
        "right": 0, 
        "left": 20
    },
    "caption": "p. 1 from [Lemmon and Scott 1977](#LemmonScott77)"
\end{imagefromfile}


For example (see also pointers [below](#Examples)):

* in *[[alethic modal logic]]* ([Wright 1951, Sec. III](#Wright51)) one considers modal operators meant to express that

  "$p$ is _[[necessity|necessarily]]_ true", or that "$p$ is _[[possibility|possibly]]_ true"

  This is the original sense of modal logic, going all the way back to [[Aristotle]] (whose account on the matter is reviewed in much detail by [Lemmon & Scott (1977) pp 1-12](#LemmonScott77)).

* in *[[epistemic modal logic]]* ([Wright 1951, Sec. IV](#Wright51)) one consider modal operators meant to express that something is "known to be true" etc. (whence the  reference to [[epistemology]]).

* in *[[temporal logic]]* one considers modal operators meant to express that

  "$p$ will _eventually become_ true", etc.;

* in *[[doxastic logic]]* one is concerned with statements such as:

  "$p$ is _believed_ to be true", etc.


Beware however that there is no broad agreement on which further [[axioms]] exactly make a general [[modal operator]] --- which in itself is any ([[comonad|co]]-)[[monad]] on the underlying [[universe of propositions]] ([[universe of types|of types]]), see [below](modal%20type%20theory#RelationToMonads) --- encode/reflect any such intended "mode of being (true)". As a result: 

>_'Ask three modal logicians what modal logic is, and you are likely to get at least three different answers'_. &lbrack;[Blackburn, deRijke & Venema (2001), Introduction](#BlackburnDeRijkeVenema01)&rbrack;

Historically, the default example of a modal logic is known as *[[S4 modal logic]]*, originally motivated as a model for [[epistemic logic]] (with a modality for being "[[necessity|necessarily true]]"), but really just axiomatizing ([[propositional logic]] equipped with) any [[monad (in computer science)|co-monad]] $\Box$ on the [[type of propositions|universe of propositions]], without further specification. There are variants known as *[[T modal logic]]* and *[[K modal logic]]* which drop some of the [[axioms]] even on this [[comonad|co]][[monad]], but it seems good practice to agree that a [[modal operator]] is *at least* a ([[comonad|co]]-)[[monad]] on the [[universe of propositions]] ([[universe of types|of types]]).


In this sense, modal logic is the counterpart in the *[[computational trilogy]]* to:

* [[category theory]] with ([[comonads|co]]-)[[monads]] ([[categorical algebra]]),

* [[computer science]] with (co-)[[monads in computer science]] ([[computational effects]]).

{#ModelsInIntroduction} Among [[semantics]]/[[models]] of modal logics are the [[geometric model for modal logics|geometric models]] based on *[[Kripke frames]]* which are [[sets]] (of *[[possible worlds]]*) on which the [[propositions]] in the logic may [[dependent type|dependend]] and equipped with [[relations]] which prescribe over which such worlds to [[quantifier|quantify]] in interpreting the [[modal operators]] (eg. which worlds to inspect to conclude that a proposition holds *possibly*).

Specifically for [[epistemic logic]] this *[[Kripke semantics]]* is hence also known as *[[possible worlds semantics]]*. (As least for [[S5 modal logic]] this is closely related to [[categorical models of dependent types]], as explained at *[[necessity and possibility]] -- [possible worlds via dependent types](necessity+and+possibility#InFirstOrderLogicAndTypeTheory)*.)

Some accounts of modal logic essentially regard the theory as being the logical study of such [[Kripke frames]] -- in the sense of sets equipped with [[relations]], hence "relational structures" (for instance [Blackburn, De Rijke & Venema (2001) p xi](#BlackburnDeRijkeVenema01) who start out saying that they do not know what modal logic is if not the study of relational structures).

There are also [[algebraic model for modal logics|algebraic models for modal logic]] in terms of algebras with (co)-[[closure operators]]. For instance, [[temporal logic|temporal logics]] can have [[posets]] as [[models]].



## Definition
 {#Definition}

### Modal Languages
{#modal+language}

Modal logics are built on **modal languages**, that is the usual propositional language plus those extra modalities. (Note that modalities may also be added to predicate logic, see [[first-order modal logic]].) The way the modalities work has to be laid down in an axiom system for the logic in question, for instance, for the temporal logic we might require an axiom saying
'If $F F\phi$ is true, then $F\phi$ is true', which will read a 'if it is going be true in the future that $\phi$ is going to be true in the future, then ...', see [[temporal logic]].  (Is this going to be something what we might want in '[[provability logic]]'; is it the case that we should expect that if it is provable that something is provable then that something must be itself provable. This concentrates the modelling process on exactly how we wish to have our 'context' to behave.) In this way the relational nature of a context that we are looking at can get encoded into the logic.


Modal languages add one or more modal operator, often denoted $\square$ or $\lozenge$ into the usual [[propositional logics]]. (For the moment, we will keep things fairly simple so assume these to  be unary operators and we will not be considering operators that have more than one input, for the moment at least. The general case will be considered later on, but in any case is discussed in detail in some of the books on modal logic listed below.)

We will give a modal language with $n$ modal operators, $\lozenge_i$, $i = 1,\ldots, n$, which can  be applied to propositions of the language to form new propositions.  If $n=1$, we will refer to the language, defined below,  as the _basic modal language_.

+-- {: .num_defn}
###### Definition

We suppose given a set of variables, the _$n$-operator basic modal language_, $\mathcal{L}_\omega(n)$, given by  

$$\phi ::= p_\lambda \mid \bot \mid \neg \phi \mid \phi_1 \vee \phi_2 \mid \lozenge_i\phi,$$  

where the $p_\lambda$ are the propositional variables ordered by finite ordinals, $\lambda$, and, as usual, $\lozenge_i$ is a modality for each  $i=1, \ldots , n$.  

=--

+-- {: .num_remark}
###### Remark

This form of definition needs a bit of interpreting if you have not met it before.  It gives a way of deciding if a formula is 'well-formed'.  The well formed formulae of  $\mathcal{L}_\omega(n)$ are defined as follows: A formula is either

   * a proposition variable, 

   * the propositional constant $\bot$, that is _falsum_, 

   * a negated formula,

   * a disjunction of two formulae, or

   * a formula prefixed by one of the diamonds / modal operators.

=--

+-- {: .num_remark}
###### Remark

The basic modal language will be $\mathcal{L}_\omega(1)$.  We will sometimes write $Prop$ for the set of propositional variables / atomic formulae or whatever other reasonable term is used in a context.

=--

+-- {: .num_remark}
###### Remark

The interpretation of $\lozenge \phi$ depends on the context (to some extent), but in the initial form here it is usually said to mean 'possibly $\phi$'.

=--

+-- {: .num_remark}
###### Remark

Some authors use an equivalent generation rule using $\square \phi$, which is $\neg \lozenge \neg \phi$. Of course, this interprets as 'necessarily $\phi$' in this initial form.  In [[epistemic logic]] the basic modal language interprets $\square \phi$ as saying 'the agent knows that $\phi$'.

=--

+-- {: .num_remark}
###### Remark

Other formulations replace $\vee$ and $\neg$ by implication $\phi_1\to \phi_2$, or by $\wedge$ and $\neg$.

=--

### Modal logics

+-- {: .num_defn}
###### Definition

A **modal logic** in $\mathcal{L}_\omega(n)$ is any set $\Lambda$ of $\mathcal{L}_\omega(n)$-formulae such that   

* $\Lambda$ includes all $\mathcal{L}_\omega(n)$-formulae that are instances of tautologies, 
 
and

* $\Lambda$ is closed under the inference rule 
_if $\phi$, $\phi\to \psi \in \Lambda$ then $\psi \in \Lambda$_ , i.e. detachment or __modus ponens__.

=--

One of the basic axiom systems leads to _[[normal modal logics]]_. 

+-- {: .num_defn}
###### Definition
**(deducibility)**

Suppose given a [[normal modal logic]], $\Lambda$ in $\mathcal{L}_\omega(n)$.  A formula $\phi$ is **$\Lambda$-deducible** from a set, $\Gamma$ of formulae, if there are finitely many formulae $\psi_0,\ldots,\psi_m\in \Gamma$ such that 

$$\vdash_\Lambda (\psi_0\to (\psi_1\to (\ldots \to (\psi_m\to \phi)\ldots)$$

that is the formula $(\psi_0\to (\psi_1\to (\ldots \to (\psi_m\to \phi)\ldots)$ is in $\Lambda$.

=--


+-- {: .num_remark}
###### Remark

As the set of all formulae in $\mathcal{L}_\omega(n)$ satisfies the conditions for a logic and any intersection of logics is itself also a logic, we have that given a set of formulae decreed to be 'axioms' for a logic, there is a smallest modal logic containing them.
 
=--

### Common modal axioms

* ([[axiom K (modal logic)|K]]) $\Box(A \to B) \to \Box A \to \Box B$
* (M) $\Box A \to A$
* (4) $\Box A \to \Box \Box A$
* (5) $\lozenge A \to \Box \lozenge A$
* (B) $A \to \Box \lozenge A$

## Examples
 {#Examples}

Here is a brief list of flavors of modal logic. More details are discussed below.

*  [[epistemic logics]]: it is known to $X$ that, it is common knowledge that;

* [[temporal logic]]: henceforth, eventually, hitherto, previously, now, tomorrow, yesterday, since, until, inevitably, finally, ultimately, endlessly, it will have been, it is being ...

*  [[dynamic logic]]: after the program/computation/action finishes, the program enables, throughout the computation;

* [[doxastic logic]]: it is believed that

* deontic logic: it is obligatory/forbidden/permitted/unlawful that 

* [[Lawvere-Tierney topology|geometric logic]]: it is locally the case that

* metalogic: it is valid/satisfiable/provable/consistent that ([Goldblatt](#Goldblatt)).

  The metalogical version was important in the [history of modern modal logic](http://plato.stanford.edu/entries/logic-modal-origins/). G&#246;del played an important role there. 



*  [[temporal logic|temporal logics]];


*  [[arrow structures|arrow logics]];

*  [[provability logics]]

   * [[Löb's axiom]] ([[incompleteness theorem]])



## Semantics 

We discuss the [[semantics]] of modal logics, its [[models]].

### In Kripke frames / relational structures

The usual [[semantics]] of modal languages is in terms of [[frame (modal logic)|frames]], and this is where the link with relational structures comes in. (These are quite often called 'Kripke frames' as Kripke was one of the first to use relational semantics in this context. 

A discussion of the history can be found in  ([BlackburnDeRijkeVenema, page 42](#BlackburnDeRijkeVenema)). 

(As there is another sense to [[frame]] as the dual of a [[locale]], we need to consider the terminology here and where necessary will use [[frame (modal logic)]] as the entry name.) A more detailed discussion of [[frame (modal logic)|frames]], models and the whole question of the semantics of modal logics is to be found at that entry. 

Modal logics are thus also the logics of [[relational structures]], in fact,   Blackburn et al (see references) have as their first slogan: **Modal languages are simple but expressive languages for talking about relational structures.**
The temporal logic that satisfies the axiom $(4)$ has models that are [[posets]], for instance, whilst many of the [[epistemic logics]] have models which are sets with equivalence relations on them. In each case, the idea is that the relational structure gives all the possible states of some system and the modal logic describes that system. This explains the great interest in computer science and artificial intelligence of applications of modal logics.



###Algebraic semantics
{#AlgebraicSemantics}

The usual algebraic semantics of modal logic is in terms of Boolean algebras with operators and is described in the entry [[algebraic models for modal logic]].

###Coalgebraic semantics

The geometric / relational /Kripke semantics of modal logics are instances of [[coalgebraic model for modal logic|coalgebraic semantics]].  This type of semantics also provides an excellent motivation and intuition for various types of modal logic that arise naturally in computer science.


### Categorical semantics
 {#CategoricalSemantics}

Every [[category]] comes with its [[internal logic]]. Modal operators in this internal logic can at least sometimes be identified with (co)reflectors into specified [[reflective subcategory|(co)reflective subcategories]]. See at _[[modal type theory]]_ for more on this.

Examples for this are [[local toposes]] and [[cohesive toposes]]. See there for more details.

## Theorems

* [[Goldblatt-Thomason theorem]]

## Related concepts

* [[modal hyperdoctrine]]

* [[modal operator]]

* [[adjoint modality]]

* [[adjoint logic]]

* [[modal type theory]]

* [[algebraic model for modal logic]]

* [[geometric model for modal logic]]

* [[coalgebraic model for modal logic]]

* [[coalgebra for an endofunctor]]

* The discussion of "[[possible worlds semantics]]" in modal logic is reminiscent of some discussion in the context of the "[[multiverse]]".
 

## References
 {#References}

One of the earliest texts that exhibits the [[intuitionism|intuitionist]] context is

* [[Oskar Becker]], *Zur Logik der Modalitäten*, Jahrbuch für Philosophie und phänomenologische Forschung **11** (1930)  497-548 &lbrack;[digizeit](http://www.digizeitschriften.de/dms/img/?PID=PPN827944462_0011%7CLOG_0010), [ophen:101138](https://ophen.org/pub-101138), [[Becker-LogikModalitaeten.pdf:file]]&rbrack;

translated in:

*  Stefania Centrone, Pierluigi Minari, *Oskar Becker, On the Logic of Modalities (1930): Translation, Commentary and Analysis*,  Synthese Library **444**, Springer (2022) &lbrack;[doi:10.1007/978-3-030-87548-0](https://doi.org/10.1007/978-3-030-87548-0)&rbrack;

The modern formalization of modal logic (and their enumeration by S1, ..., [[S4]], [[S5]]) originates with

* [[Clarence I. Lewis]], [[Cooper H. Langford]], pp 153 & App II of: *Symbolic Logic* (1932), Dover (2000) &lbrack;App. II [pdf](https://www.hist-analytic.com/Lewisstrict.pdf)&rbrack;

(who say "modal functions" for [[modal operators]]).

Early discussion making explicit [[epistemic modal logic]] and variants:

* {#Wright51} [[Georg H. von Wright]], *An Essay in Modal Logic*, North-Holland Publishing (1951)

* [[K. Jaakko J. Hintikka]], *Knowledge and belief: An introduction to the logic of the two notions*, Cornell University Press (1962) &lbrack;[ark:/13960/t9k437s65](https://archive.org/details/knowledgebeliefi00hint_0)&rbrack;

  > (introducing the formalism of [[K modal logic]])


Historical overview and introduction:

* {#Goldblatt03} [[Robert Goldblatt]], *Mathematical modal logic: A view of its evolution*, Journal of Applied Logic **1** 5–6 (2003) 309-392 &lbrack;<a href="https://doi.org/10.1016/S1570-8683(03)00008-9">doi:10.1016/S1570-8683(03)00008-9</a>&rbrack;

* {#Goldblatt05} [[Robert Goldblatt]], *Mathematical Modal Logic: a View of its Evolution*, in *Handbook of the History of Logic vol. 7*, Elsevier (2005) &lbrack;<a href="https://doi.org/10.1016/S1874-5857(06)80027-0">doi:10.1016/S1874-5857(06)80027-0</a>,[draft](http://homepages.mcs.vuw.ac.nz/~rob/papers/modalhist.pdf)&rbrack;

* {#SEPModernOrigins} Stanford Encyclopedia of Philosophy: _[Modern Origins of Modal Logic](http://plato.stanford.edu/entries/logic-modal-origins/)_.
 
* {#SEPModalLogic} Stanford Encyclopedia of Philosophy: _[Modal Logic](http://plato.stanford.edu/entries/logic-modal/)_.


Textbook accounts:
 {#TextbookAccounts}

* {#LemmonScott77} [[E. John Lemmon]] with [[Dana Scott]], *An Introduction to Modal Logic -- The "Lemmon Notes"*, B. Blackwell (1977) &lbrack;[ark:/13960/t3gz25k3h](https://archive.org/details/introductiontomo0000lemm/)&rbrack;

* {#BradleySwartz79} [[Raymond D. Bradley]], [[Norman Swartz]], *Possible Worlds -- An Introduction to Logic and its Philosophy*, Hackett Publishing (1979) &lbrack;[webpage](http://www.sfu.ca/~swartz/pw/), [pdf](https://www.sfu.ca/~swartz/pw/text/pw_all.pdf)&rbrack;

* {#BlackburnDeRijkeVenema01} [[Patrick Blackburn]], [[Maarten de Rijke]], [[Yde Venema]], *Modal Logic*, Cambridge Tracts in Theoretical Computer Science **53**, Cambridge University Press  (2001) &lbrack;[doi:10.1017/CBO9781107050884](https://doi.org/10.1017/CBO9781107050884)&rbrack;

* {#BlackburnvanBenthemWolter07} [[Patrick Blackburn]], [[Johan van Benthem]], [[Frank Wolter]] (eds.), *The Handbook of Modal Logic*, Studies in Logic and Practical Reasoning **3** (2007) &lbrack;[book webpage](https://cgi.csc.liv.ac.uk/~frank/MLHandbook/), [publisher page](https://www.sciencedirect.com/bookseries/studies-in-logic-and-practical-reasoning/vol/3/suppl/C)&rbrack;

* {#Benthem10} [[Johan van Benthem]], *Modal Logic for Open Minds* (2010) &lbrack;[ISBN:9781575865980](http://web.stanford.edu/group/cslipublications/cslipublications/site/9781575865980.shtml), [pdf](http://fenrong.net/teaching/mljvb.pdf), [webpage](https://archive.illc.uva.nl/lgc/MLoM/)&rbrack;


Other texts:

* {#Scott70} [[Dana Scott]], _Advice on Modal Logic_, in [[Karel Lambert]] (ed.) _Philosophical problems in Logic -- Some recent developments_, Reidel 1970

  > Here is what I consider one of the biggest mistakes in all of modal logic: concentration on a system with just _one_ modal operator. (p. 161)

* {#MakkaiReyes95} [[Michael Makkai]], [[Gonzalo Reyes]], _Completeness results for intuitionistic and modal logic in a categorical setting_, Annals of Pure and Applied Logic 72 (1995) 25-101

  > (on [[de dicto and de re]] phenomena in [[hyperdoctrine|hyperdoctrinal]] modal logic)

A formulation of modal logic in terms of [[type|typing]] [[judgements]] and  [[type formation rules]] is in 

* {#Pfenning-Davies} [[Frank Pfenning]], Rowan Davies, *A judgemental reconstruction of modal logic*, Mathematical Structures in Comp. Sci. **11** 4 (2001) 511-540 &lbrack;[pdf](http://www.cs.cmu.edu/~fp/papers/mscs00.pdf)&rbrack;

See also:

* [[Marcus Kracht]], _Tools and Techniques in Modal Logic_ , Studies in Logic and the Foundation of Mathematics **142** Elsevier Amsterdam (1999) &lbrack;[pdf](http://wwwhomes.uni-bielefeld.de/mkracht/html/tools/book.pdf), [doi:10.2307/2687780](https://doi.org/10.2307/2687780)&rbrack;

 
A discussion of  coalgebraic modal logic and of general modal logic in terms of [[coalgebra]] and the [[terminal coalgebra of an endofunctor]] is in 

* [[Corina Cirstea]], [[Alexander Kurz]], Dirk Pattinson, Lutz Schr&#246;der and [[Yde Venema]], _Modal logics are coalgebraic_ ([pdf](http://eprints.soton.ac.uk/267144/1/ModalCoalgRev.pdf))

Formalization of modalities ([[higher modalities]]) in [[homotopy type theory]] appears around definition 1.11 of

* [[Egbert Rijke]], [[Bas Spitters]], _Sets in homotopy type theory_ ([arXiv:1305.3835](http://arxiv.org/abs/1305.3835))

On applications of modal logic to [[linguistics]]:

* [[Lawrence S. Moss]], Hans-Jörg Tiede: _Applications of Modal Logic in Linguistics_, in: *Studies in Logic and Practical Reasoning **3** (2007) 1031-1076 &lbrack;<a href="https://doi.org/10.1016/S1570-2464(07)80022-X">doi:10.1016/S1570-2464(07)80022-X</a>, [pdf](https://www.csc.liv.ac.uk/~frank/MLHandbook/19.pdf)&rbrack;



[[!redirects modal logic]]
[[!redirects modal logics]]