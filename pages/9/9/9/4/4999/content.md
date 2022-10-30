
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
#### Modalities, Closure and Reflection
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

The term _modal logic_ refers to an enrichment of standard formal [[logic]] where the standard operations ([[and]], [[or]], [[not]], implication and perhaps [[universal quantifier|forall]], etc.) are accompanied by certain extra operations -- called _modal operators_ and often denoted by "$\lozenge$" and "$\Box$" or similar -- such that for $p$ any [[proposition]] the expression $\Box p$ is a new proposition whose interpretation is roughly as "$p$ holds (only) in some _mode_" or "$p$ holds (only) _in a certain way_", such as: "$p$ is _possibly_ true", "$p$ will _eventually become_ true", "$p$ is _believed_ to be true", etc. 

There is no established axiom set that an operator on propositions has to satisfy to count as a _modal operator_. As a result, for instance in the preface of ([Blackburn-deRijke-Venema](#BlackburnDeRijkeVenema)) et al.) it says

>_'Ask three modal logicians what modal logic is, and you are likely to get at least three different answers'_.

Hence there is a good bit of flexibility in the notion _modal logic_.
The archetypical example of a modal logic, often taken to be the default example, is a system, called _[[S4 modal logic]]_ or some slight variants (S1, S2, ...) of it, that aims to model the idea of propositions being "possibly true" or "necessarily true".  We list and discuss further examples of modal logic in more detail below in _[Examples](#Examples)_. 

One way to view the axioms of [[S4 modal logic]] is as being those of [[propositional logic]] together with a [[monad (in computer science)|co-monad]] $\Box$ on the [[type of propositions|universe of propositions]].  Accordingly, many other flavours of modal operators that are being considered (but not all) are also (co)monads, see below at _[modal type theory -- Relation to monads](modal%20type%20theory#RelationToMonads)_. This has an evident generalization to _[[modal type theory]]_, which is concerned with [[type theory|type theories]] equipped with [[monad (in computer science)|(co)monads]] on their [[type of types|type universe]]. Hence when restricted to modalities that are required to be (co)monads, then modal logic is the counterpart in _[[computational trinitarianism]]_ to [[category theory]] making use of [[closure operator]] [[monads]] and to [[computer science]] with [[monads in computer science]].

For a good survey of and introduction to modal logic see _[SEP - Modern Origins of Modal Logic](#SEPModernOrigins)_ for (historical) motivation and introduction and then _[SEP - Modal logic](#SEPModalLogic)_ for more technical details.

Modal logics have [[semantics]] in terms of sets with [[relations]], called _[[Kripke frames]]_ in the context of modal logic. They also have algebraic semantics in terms of algebras with (co)-closure operators. For instance, [[temporal logic|temporal logics]] can have [[posets]] as [[models]].



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

## Examples
 {#Examples}

Here is a brief list of flavors of modal logic. More details are discussed below.


*  [[epistemic logics]]: it is known to $X$ that, it is common knowledge that (see [below](#EpistemicLogic) for more);

*  [[dynamic logic]]: after the program/computation/action finishes, the program enables, throughout the computation;

* tense logic: henceforth, eventually, hitherto, previously, now, tomorrow, yesterday, since, until, inevitably, finally, ultimately, endlessly, it will have been, it is being ...

* deontic logic: it is obligatory/forbidden/permitted/unlawful that 


* doxastic logic: it is believed that

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

## Links
  
* {#SEPModernOrigins} Stanford Encyclopedia of Philosophy: _[Modern Origins of Modal Logic](http://plato.stanford.edu/entries/logic-modal-origins/)_.
 
* {#SEPModalLogic} Stanford Encyclopedia of Philosophy: _[Modal Logic](http://plato.stanford.edu/entries/logic-modal/)_.
 
## References
 {#References}

A nice historical overview of modern modal logic that might serve as a general introduction as well can be found in

* [[R. Goldblatt]], _Mathematical Modal Logic: a View of its Evolution_ , in Gabbay, Woods (eds.), _Handbook of the History of Logic vol. 6_ , Elsevier Amsterdam 2005. ([draft](http://homepages.mcs.vuw.ac.nz/~rob/papers/modalhist.pdf))

One of the earliest texts that exhibits the [[intuitionism|intuitionist]] context is

* Oskar Becker, _Zur Logik der Modalit&#228;ten_ , Jahrbuch f&#252;r Philosophie und ph&#228;nomenologische Forschung **11** (1930)  pp.497-548. ([digizeit](http://www.digizeitschriften.de/dms/img/?PID=PPN827944462_0011%7CLOG_0010))

A standard textbook and reference is

* {#BlackburnDeRijkeVenema} [[Patrick Blackburn]], M. de Rijke and [[Yde Venema]], _Modal Logic_, Cambridge Tracts in Theoretical Computer Science, vol. 53, 2001.

Two standard references are

* P. Blackburn, J. van Benthem, F. Wolter (eds.), _The Handbook of Modal Logic_ , Elsevier Amsterdam 2007.

* [[Marcus Kracht]], _Tools and Techniques in Modal Logic_ , Studies in Logic and the Foundation of Mathematics **142** Elsevier Amsterdam 1999. ([draft](http://wwwhomes.uni-bielefeld.de/mkracht/html/tools/book.pdf))

Other texts on modal logic include

* {#Scott70} [[Dana Scott]], _Advice on Modal Logic_, in [[Karel Lambert]] (ed.) _Philosophical problems in Logic -- Some recent developments_, Reidel 1970

  > Here is what I consider one of the biggest mistakes in all of modal logic: concentration on a system with just _one_ modal operator. (p. 161)

* {#MakkaiReyes95} [[Michael Makkai]], [[Gonzalo Reyes]], _Completeness results for intuitionistic and modal logic in a categorical setting_, Annals of Pure and Applied Logic 72 (1995) 25-101

  (on [[de dicto and de re]] phenomena in [[hyperdoctrine|hyperdoctrinal]] modal logic)

A formulation of modal logic in terms of [[type|typing]] [[judgements]] and  [[type formation rules]] is in 

* {#Pfenning-Davies} [[Frank Pfenning]], Rowan Davies, _A judgemental reconstruction of modal logic_, Mathematical Structures in Comp. Sci., 11(4):511{540, August 2001. (2000) ([pdf](http://www.cs.cmu.edu/~fp/papers/mscs00.pdf))
 
A discussion of  coalgebraic modal logic and of general modal logic in terms of [[coalgebra]] and the [[terminal coalgebra of an endofunctor]] is in 

* [[Corina Cirstea]], [[Alexander Kurz]], Dirk Pattinson, Lutz Schr&#246;der and [[Yde Venema]], _Modal logics are coalgebraic_ ([pdf](http://eprints.soton.ac.uk/267144/1/ModalCoalgRev.pdf))

Formalization of modalities ([[higher modalities]]) in [[homotopy type theory]] appears around definition 1.11 of

* [[Egbert Rijke]], [[Bas Spitters]], _Sets in homotopy type theory_ ([arXiv:1305.3835](http://arxiv.org/abs/1305.3835))

An overview of applications of modal logic in [[linguistics]] can be found in

* Lawrence S. Moss, Hans-J&#246;rg Tiede, _Applications of Modal Logic in Linguistics_ , pp.299-341 in Blackburn, van Benthem, Wolter (eds.), _The Handbook of Modal Logic_ , Elsevier Amsterdam 2007. ([draft](http://www.indiana.edu/~iulg/moss/linguistics.pdf))



[[!redirects modal logic]]
[[!redirects modal logics]]