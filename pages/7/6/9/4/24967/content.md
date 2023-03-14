
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



*Epistemic logic* is the branch of [[modal logic]] which is concerned with [[epistemology]], hence with notions of knowledge and belief.  In its applied form it has found considerable use in [[computer science]] and Artificial Intelligence.

Its key [[modal operators]] are *[[necessity and possibility]]* and its popular [[semantics]] is known as *[[possible worlds semantics]]*.

## Introduction

Epistemic modalities are captured in [[epistemic logic|epistemic modal logic]], where [[necessity]] is interpreted as saying _"I know that proposition $\phi$ is true"_, and in 'provability logic', the basic modal operator interprets  as _"it is provable that $\phi$"_. 

If we have the basic [[temporal logic]], then there is a future truth operator, so that $F\phi$ is intended to mean _'' $\phi$ will be true at some future time"_, and also a past operator $P$ so $P\phi$ is intended to mean "$\phi$ was true at some past time". 


Notice that the notions of _[[possibility]]_ and _[[necessity]]_ have different senses in ordinary language. For example, if we say '$P$ is possible', we may mean that $P$ is: *epistemically* possible, not ruled out by anything I know; *physically* possible, not ruled out by the laws of physics; *logically* possible, not ruled out by the laws of logic. Some suggest that there is a further type of possibility, *metaphysical* possibility intermediate between logical and physical possibility. Metaphysical possibility would allow that different laws of physics might apply. 




## Epistemic formulae

These are variants of the formulae of the basic [[modal logic|modal language]].  The basic modal operators are, here, labelled $K_i$ since they relate to 'knowledge'. These correspond to the $\Box$ operators in  the standard form, and are used in preference to the dual $\Diamond$ forms because of their interpretation (given below), which is more immediately relevant to the applications.

More formally, we have $P$ or $Prop$, is a set of countably (finite or infinite) many atomic formulae.  there is also a set $A$, often called the set of 'agents' and taken to be $A = \{1,\ldots,m\}$.  The set of epistemic formluae (= basic $m$-agent epistemic language) will be denoted  $\mathcal{L}^m_K(P)$ is given by the rules

$$\phi ::= p \mid \bot \mid \neg \phi \mid \phi_1 \wedge \phi_2 \mid K_i\phi for i\in A.$$  

We read $K_i \phi$ as ''agent $i$ knows that $\phi$''.

The converse or dual operators, denoted $M_i$ (so that $M_i \phi = \neg K_i\neg \phi$) reads as ''agent $i$ considers $\phi$ is possible''.

+-- {: .un_remark}
###### Note

The 'agent' terminology is extremely useful, but in pure modal logic texts is not used so much.  It does provide an 'intuition' and an interpretation however.
=--


## List of frequently encountered epistemic logics

* [[the logic K(m)| K(m)]];

* [[the logic T(m)| T(m)]];

* [[the logic S4(m)|S4(m)]];

* [[the logic S5(m)|S5(m)]].


## Models for epistemic logics

The geometric or combinatorial semantics of epistemic models follows the same techniques of [[Kripke frames]] as at [[geometric models for modal logics]], whilst the [[algebraic models for modal logics|algebraic models]] are BAOs that is [[algebraic models for modal logics|Boolean algebras with operators]].  As usual the [[Kripke frames]] semantics is an example of [[coalgebraic semantics]].


## Related entries

* [[epistemology]]

* [[necessity and possibility]]

* [[modal logic]]

* [[epistemology of mathematics]]



## References

A fairly recent book on epistemic logics and their applications (which was used for some of the material above):

* J.- J. Ch. Meyer and W. Van der Hoek, _Epistemic logic for AI and Computer Science_, Cambridge Tracts in Theoretical Computer Science, vol. 41, 1995,

General books on [[modal logic]] with discussion of epistemic logic:

* [[Patrick Blackburn]], M. de Rijke and [[Yde Venema]], _Modal Logic_, Cambridge Tracts in Theoretical Computer Science, vol. 53, 2001.

* [[Marcus Kracht]], _Tools and Techniques in Modal Logic,_ Studies in Logic and the Foundation of Mathematics, 142, Elsevier, 1999,

* Johan van Benthem, _Dynamic logic for belief revision_ ([pdf](http://www.illc.uva.nl/Research/Reports/PP-2006-11.text.pdf))

See also:

* Wikipedia, *[Epistemic modal logic](https://en.wikipedia.org/wiki/Epistemic_modal_logic)*

[[!redirects epistemic modal logics]]

[[!redirects epistemic logic]]
[[!redirects epistemic logics]]







