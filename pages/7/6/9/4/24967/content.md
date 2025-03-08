
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
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



# Epistemic logic
* table of contents
{:toc}

## Idea


*Epistemic logic* is the branch of [[modal logic]] which is concerned with [[epistemology]], hence with notions of knowledge and sometimes also notions of belief, although these may be treated separately by [[doxastic logic]]. In its applied form it has found considerable use in [[computer science]] and Artificial Intelligence.

The key [[modal operators]] for epistemic logic are forms of *[[necessity and possibility]]* corresponding to "It is known to be the case that" and "It may be the case that (so far as is known)". As a form of modal logic, the [[semantics]] typically used is *[[possible worlds semantics]]* where the worlds correspond to maximally specific ways the world could have been. Philosophers disagree as to whether to distinguish the space of *metaphysically* possible worlds from the space of *epistemically* possible worlds ([Kment 21](#Kment21)).

## Introduction

Epistemic modalities are captured in [[epistemic logic|epistemic modal logic]] by interpreting "*necessarily $\phi$*" as saying _"It is known that proposition $\phi$ is true"_. It is common also to indicate the epistemic agent, so that corresponding to agent $x$ we have "$x$ knows that proposition $\phi$ is true".

In the closely related 'provability logic', the basic modal operator interprets  as _"it is provable that $\phi$"_. 

Notice that the notions of _[[possibility]]_ and _[[necessity]]_ have different senses in ordinary language. For example, if we say '$P$ is possible', we may mean that $P$ is: *epistemically* possible, not ruled out by anything I know; *physically* possible, not ruled out by the laws of physics; *logically* possible, not ruled out by the laws of logic. Some suggest that there is a further type of possibility, *metaphysical* possibility intermediate between logical and physical possibility. Metaphysical possibility would allow that different laws of physics might apply. 

## Epistemic formulae

These are variants of the formulae of the basic [[modal logic|modal language]].  The basic modal operators are, here, labelled $K_i$ since they relate to 'knowledge' and indicate the epistemic agent, the knower, $i$. These correspond to the $\Box$ operators in  the standard form, and are used in preference to the dual $\lozenge$ forms since they are more immediately relevant to applications.

More formally, we have $P$ or $Prop$, is a set of countably (finite or infinite) many atomic formulae.  there is also a set $A$, often called the set of 'agents' and taken to be $A = \{1,\ldots,m\}$.  The set of epistemic formulae (= basic $m$-agent epistemic language) will be denoted  $\mathcal{L}^m_K(P)$ is given by the rules

$$\phi ::= p \mid \bot \mid \neg \phi \mid \phi_1 \wedge \phi_2 \mid K_i\phi for i\in A.$$  

We read $K_i \phi$ as ''agent $i$ knows that $\phi$''.

The converse or dual operators, denoted $M_i$ (so that $M_i \phi = \neg K_i\neg \phi$) reads as ''agent $i$ considers $\phi$ is possible''.

+-- {: .un_remark}
###### Note

The 'agent' terminology is extremely useful, but in pure modal logic texts is not used so much.  It does provide an 'intuition' and an interpretation however.
=--


## Axioms for epistemic logic {#Axioms}

The question then arises as to which axioms of modal logic are appropriate to the epistemic case. Answers will depend on what interpretation is given to 'know' in specifying how the operator $K$ behaves. E.g., there is a difference between the knowledge of a realistic, cognitively-limited agent and that of some idealized agent with boundless resources.

It is generally admitted that axiom (T) should hold, here 

$$
\mathbf{T}: K \phi \to \phi,
$$

which states that if $\phi$ is known then $\phi$ is true. Truth is generally taken to be a precondition of knowledge.

A much more contentious issue in the field is whether to admit an epistemic version of axiom (4). Known as the _[[KK principle]]_ or _KK thesis_, this corresponds to 

$$
\mathbf{4}: K \phi \to K K \phi,
$$

which states that when $\phi$ is known to be true then it is also known that it is known. T

{#EvenPossible} It is even possible to challenge the admission of two of the most fundamental modal axioms, axioms (N) and (K). These correspond to 

$$
  \mathbf{N}
  \phantom{,}\colon\phantom{,} 
  \text{If}\phantom{,}P\phantom{,}\text{is a theorem, then so is}\phantom{,}K P
$$
and 

$$
  \mathbf{K}: K(P \to Q) \to (K P \to K Q).
$$
An understanding of **N** that it states that all theorems are known is evidently problematic. Similarly for **K**, it is not clear that we know the deductive consequences of the collection of propositions that we know, such as the application of _modus ponens_ to every instance of known $P \to Q$ and $P$. 

On the other hand, we might consider epistemic logic to represent the reasoning of an ideal, logically omniscient, agent, and so admit **N** and **K**.



## Models for epistemic logics

The geometric or combinatorial semantics of epistemic models follows the same techniques of [[Kripke frames]] as at [[geometric models for modal logics]], whilst the [[algebraic models for modal logics|algebraic models]] are BAOs that is [[algebraic models for modal logics|Boolean algebras with operators]].  As usual the [[Kripke frames]] semantics is an example of [[coalgebraic semantics]].


## Related entries

* [[epistemology]]

* [[necessity and possibility]]

* [[modal logic]]

* [[epistemology of mathematics]]

* [[the logic K(m)| K(m)]];

* [[the logic T(m)| T(m)]];

* [[the logic S4(m)|S4(m)]];

* [[the logic S5(m)|S5(m)]].



## References

### General

Early discussion of epistemic modal logic:

* [[Georg H. von Wright]], Section IV of: *An Essay in Modal Logic*, North-Holland Publishing (1951)

and introducing the formalization as [[K modal logic]]:

* [[K. Jaakko J. Hintikka]], *Knowledge and belief: An introduction to the logic of the two notions*, Cornell University Press (1962) &lbrack;[ark:/13960/t9k437s65](https://archive.org/details/knowledgebeliefi00hint_0)&rbrack;


A fairly recent book on epistemic logics and their applications (which was used for some of the material above):

* J.- J. Ch. Meyer and W. Van der Hoek, _Epistemic logic for AI and Computer Science_, Cambridge Tracts in Theoretical Computer Science, vol. 41, 1995,

General books on [[modal logic]] with discussion of epistemic logic:

* [[Patrick Blackburn]], M. de Rijke and [[Yde Venema]], _Modal Logic_, Cambridge Tracts in Theoretical Computer Science, vol. 53, 2001.

* [[Marcus Kracht]], _Tools and Techniques in Modal Logic,_ Studies in Logic and the Foundation of Mathematics, 142, Elsevier, 1999,

* Johan van Benthem, _Dynamic logic for belief revision_ ([pdf](http://www.illc.uva.nl/Research/Reports/PP-2006-11.text.pdf))

* {#Kment21} Boris Kment, _Varieties of Modality_, [SEP](https://plato.stanford.edu/entries/modality-varieties/#Dua)

See also:

* Wikipedia, *[Epistemic modal logic](https://en.wikipedia.org/wiki/Epistemic_modal_logic)*




[[!include S5 modal logic as epistemic logic -- references]]




[[!include possible-worlds and many-worlds -- references]]





[[!redirects epistemic modal logics]]

[[!redirects epistemic logic]]
[[!redirects epistemic logics]]

[[!redirects epistemic modality]]
[[!redirects epistemic modalities]]







