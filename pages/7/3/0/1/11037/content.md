+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Deduction and Induction
+-- {: .hide}
[[!include deduction and induction - contents]]
=--
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

# Contents
* table of contents
{: toc}

## Idea

The _cut rule_ in [[sequent calculus]] ([[formal logic]]) is the [[structural rule|structural]] [[inference rule]] that from [[sequents]] of the form

$$
  \Gamma \vdash A , \Delta
$$

and

$$
  \Pi, A \vdash \Lambda
$$

the new sequent

$$
  \Pi, \Gamma \vdash \Lambda, \Delta
$$

may be [[deduction|deduced]]. This is often written in the form 

$$\frac{\Gamma \vdash A, \Delta \quad \Pi, A \vdash \Lambda}{\Pi, \Gamma \vdash \Lambda, \Delta} \; cut.$$ 

In the [[categorical semantics]] where each [[sequent]] here is interpreted as a [[morphism]] in a [[category]], the cut rule asserts the existence of [[composition]] of morphisms.

## Cut elimination

> "A sequent calculus without cut-elimination is like a car without an engine" -- Jean-Yves Girard (in [Linear logic](http://iml.univ-mrs.fr/~girard/Synsem.pdf.gz))

The _cut-elimination theorem_ ("[[Gerhard Gentzen]]'s [[Gentzen's Hauptsatz|Hauptsatz]]") asserts that every [[judgement]] which has a [[proof]] using the cut-rule also has a proof not using it (a "cut-free proof").  While Gentzen\'s original theorem was for a few particular sequent calculi that he was considering, it is true of many other sequent calculi and is generally seen as desirable.  (That said, there are some useful sequent calculi in which it fails.) 

Intuitively, the problem in deciding whether a formula $B$ follows from a formula $A$, i.e., deriving $A \vdash B$, is that there could be very complicated steps in the middle, i.e., in typical mathematical arguments one puts together steps $A \vdash C$ and $C \vdash B$ where $C$ is potentially a complicated or large formula. For an automated theorem prover, the search space for such $C$ is potentially infinite. By establishing a cut-elimination theorem for formal systems, one circumvents this problem, and it is quite typical that cut-free proofs build up complex sequents from less complex sequents (cf. [[subformula property]]), so that one can decide whether a sequent is provable or derivable by following an inductive procedure. 

Cut-elimination is also a key step in deciding whether two proofs of a sequent are the "same" in some suitable sense. In [[type theory]], for instance, the issue is not merely whether $A \vdash B$ is provable or whether the function type $A \multimap B$ is inhabited (has a proof or a term witnessing that fact), but also the nature of the space of such proofs. Since any proof has a trivial cut-free formulation in a system where all provable sequents in the original system are simply postulated as axioms, a cut-elimination result worthy of the name will not merely replace a proof with one which is cut-free, but with a cut-free proof which is _equivalent_ to the original. This idea is used for instance in proving [[coherence theorems]]. 

Cut-elimination may also be used to give independent proof-theoretic motivation of the definition of a category, and other basic category theoretic notions, eg. [[adjunction]] (see [Do&#353;en 99](#Dos99)).


## Connection to identities 

In the analogy between the composition and the cut rule, the analogue of [[identity morphisms]] (or nullary compositions) is the identity rule

$$
  A \vdash A
$$

Typically, a cut-elimination algorithm goes hand-in-hand with an algorithm which eliminates the identity rule, or rather which pushes back identities as far as possible, down to identities for basic propositional variables (so for example, $p \wedge q \vdash p \wedge q$ may be proved using $p \vdash p$ and $q \vdash q$, in addition to the rules for $\wedge$, but $p \vdash p$ itself must be adopted as an axiom). 

In fact, there is a sense in which elimination of cuts is seen as _dual_ to elimination of identities, analogous to the sense in which [[beta reduction]] is seen as dual to [[eta expansion]]. Very typically, a normalization scheme on terms first applies eta expansions are far as they will go, and then applies beta reductions as far as they will go, so as to at last reach a normal form. The same goes for rewrite systems on sequent deductions, which first eliminate identities, then eliminate cuts. 

## Examples of elimination steps 

The conversion

$$
\frac{\displaystyle \frac{\Gamma, A \vdash B, \Delta}{\Gamma \vdash A \multimap B,\Delta} \;\;\; \frac{\Pi_1 \vdash A,\Lambda_1 \;\;\; \Pi_2,B \vdash \Lambda_2}{\Pi_2,\Pi_1, A\multimap B \vdash \Lambda_2,\Lambda_1}}{\Pi_2,\Pi_1, \Gamma \vdash \Lambda_2,\Lambda_1, \Delta}
  \quad\to\quad
\frac{\displaystyle \frac{\Gamma, A \vdash B, \Delta \;\;\; \Pi_1 \vdash A,\Lambda_1}{\Pi_1,\Gamma \vdash \Lambda_1,B,\Delta} \;\;\; \Pi_2,B \vdash \Lambda_2}{\Pi_2,\Pi_1, \Gamma \vdash \Lambda_2, \Lambda_1,\Delta}
$$

replaces a single cut on the formula $A \multimap B$ with a pair of cuts on the formulas $A$ and $B$, in the process eliminating the use of the logical rules ${\multimap}R$ and ${\multimap}L$. 

Although this step replaces one cut by two, the cuts have been in effect pushed up the proof tree, to formulas of lower complexity. Cuts are finally eliminated when they have been pushed all the way up to identity axioms on propositional variables, by applying conversions of type 

$$\frac{\displaystyle \frac{}{x \vdash x}\; axiom \;\;\;\; \frac{}{x \vdash x}\; axiom}{x \vdash x} \; cut \quad\to\quad \frac{}{x \vdash x}\; axiom.$$ 

Likewise, the conversion

$$A \wedge B \vdash A \wedge B
\quad\to\quad
\frac { \displaystyle \frac { A \vdash A } { A \wedge B \vdash A } \;\;\; \frac { B \vdash B } { A \wedge B \vdash B} } { A \wedge B \vdash A \wedge B } $$

reconstructs the identity on $A \wedge B$ from identities on $A$ and on $B$, by first applying the ${\wedge}R$ rule followed by the two ${\wedge}L$ rules (reading the derivation on the right bottom-up).

(Compare these two conversions arising from cut- and identity-elimination to the lambda calculus conversions $(\lambda x.t_1) t_2 \to t_1[t_2/x]$ and $t \to \langle\pi_1t,\pi_2 t\rangle$, i.e., a $\beta$ reduction and an $\eta$ expansion respectively.)


## Alternative forms of the cut rule  

In [[linear logic]] (for instance), one sometimes sees sequents written in one-sided form: 

$$\; \vdash \Gamma.$$ 

Here the [[negation]] operator is used to mediate between classical two-sided sequents and one-sided sequents, according to a scheme where a sequent $\Gamma, A \vdash \Delta$ is associated with a sequent $\Gamma \vdash \Delta, \neg A$ (each being derivable from the other). Thus one can contemplate sequents where all formulae have been pushed to the right of the entailment symbol $\vdash$. 

For such one-sided sequents, say in multiplicative linear logic, the cut rule may be expressed in the form 

$$\frac{\vdash \Gamma, \neg A \;\;\; \vdash \Delta, A}{\vdash \Gamma, \Delta} \; cut$$ 

and this rule is 'dual' to one which introduces an identity: 

$$\frac{}{\vdash \neg A, A} \; identity.$$ 

Categorically, the cut rule in this form corresponds to the arrow $\neg A \otimes A \to \bot$ that implements an evaluation, and the identity rule corresponds to an arrow $\top \to \neg A \wp A = A \multimap A$ that names an identity morphism. These two arrows are de Morgan dual to one another. 

## Cut elimination as a computation

[[Gerhard Gentzen]]'s [[Gentzen's Hauptsatz|Hauptsatz]] is often formulated under the form: "The cut rule is an [[admissible rule]]"- ie. the logical system obtained by removing the cut rule proves exactly the same sequents that the original system with the cut rule, it is important that very often, a stronger statement is true.

The theorem of Gentzen was formulated for [[classical logic]] and is also true in the other logics with a cut rule such as [[intuitionistic logic]] or [[linear logic]]. In these two latter systems, one has more, the cut elimination can be formulated as "There exists a cut elimination algorithm specified like this:

* Entry: proof $\pi_{1}$ of a sequent $\Gamma \vdash \Delta$
* Output: proof $\pi_{2}$ of the sequent $\Gamma \vdash \Delta$ which doesn't use the cut rule"

A better way to present things would be: "Here is an algorithm which takes in entry a proof $\pi_{1}$ of $\Gamma \vdash \Delta$ and returns a proof $\pi_{2}$ of $\Gamma \vdash \Delta$ which doesn't use the cut rule", because an actual algorithm is actually given and it is important to know what is this algorithm, we're not interested only by its existence.

The best way to tell it would be in fact as:

"Here is a [[rewriting system]] $\rightarrow$ on the set of proofs of this logic such that if $\pi_{1} \rightarrow \pi_{2}$ then $\pi_{1}, \pi_{2}$ are proofs of the same sequent, and for every proof $\pi$ of $\Gamma \vdash \Delta$, there exists a finite sequence $\pi_{0}, \pi_{1}, \ldots, \pi_{n}$ of proofs of $\Gamma \vdash \Delta$ such that $\pi = \pi_{0} \rightarrow \pi_{1} \rightarrow ... \rightarrow \pi_{n}$
and $\pi_{n}$ doesn't use the cut rule."

One can after this study the properties of this particular rewriting system: is it [[confluent]]? Is it [[normalizing]]? [[strongly normalizing]]? Does it provide a [[deterministic algorithm]] or a [[nondeterministic algorithm]]? What is the [[computational complexity]] of the algorithms it provides to eliminate cuts? 

Unfortunately, the algorithmic aspect of cut elimination is rarely presented as explicitely, and most of the time the cut elimination is presented as the admissibility of the cut rule and the concrete algorithm to eliminate the instance of cuts in a proof $\pi$ must be extracted by the reader from this proof (of the cut elimination) which nevertheless use it in order to do the proof (of the cut elimination).

We're not sure whether there isn't such an algorithm of cut elimination for [[classical logic]] and this an ongoing subject of research. We can think that the usual sequent calculus of classical logic must be modified by using ideas such as [[polarity in type theory|polarization]] and [[focusing]] in order to understand the computational content of the cut elimination of classical logic.

## References

The notion of the cut rule as a [[structural inference rule]] originates (under the German name *Schnitt*) with: 

* {#Gentzen35} [[Gerhard Gentzen]], §1.2.1 in: _Untersuchungen &#252;ber das logische Schlie&#223;en I_ _Mathematische Zeitschrift_ **39** 1 (1935) &lbrack;[doi:10.1007/BF01201353](http://dx.doi.org/10.1007/BF01201353)&rbrack;

* {#Gentzen69} [[Gerhard Gentzen]], §1.21 in: *Investigations into Logical Deduction*, in M. E. Szabo (ed.), *The Collected Papers of Gerhard Gentzen*, Studies in Logic and the Foundations of Mathematics **55**, Springer (1969) 68-131 &lbrack;[ISBN:978-0-444-53419-4](https://www.sciencedirect.com/bookseries/studies-in-logic-and-the-foundations-of-mathematics/vol/55), [pdf](https://logic-teaching.github.io/prop/texts/Gentzen%201969%20-%20Investigations%20into%20Logical%20Deduction.pdf)&rbrack;



* Wikipedia, _[Cut-elimination theorem](http://en.wikipedia.org/wiki/Cut-elimination_theorem)_

* {#Dos99} Kosta Do&#353;en, _Cut Elimination in Categories_ Dordrecht: Springer Netherlands, 1999.

[[!redirects cut-elimination]]
[[!redirects cut elimination]]

[[!redirects cut-elimination theorem]]
[[!redirects cut elimination theorem]]

[[!redirects cut-admissibility]]
[[!redirects cut admissibility]]

[[!redirects cut]]
[[!redirects cuts]]

[[!redirects Gentzen's Hauptsatz]]
[[!redirects Gentzen Hauptsatz]]
