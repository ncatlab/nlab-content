[[!redirects epistemic logic]]
[[!redirects epistemic logics]]

#Contents#
* table of contents
{:toc}

## Epistemic Logics ## 
Epistemic logic is the branch of [[modal logic]] concerning notions of knowledge and belief.  In its applied form it has found considerable use in Computer Science and Artificial Intelligence.

##Epistemic formulae##
These are variants of the formulae of the basic [[modal logic|modal language]].  The basic modal operators are, here, labelled $K_i$ since they relate to 'knowledge'. These correspond to the $\box$ operators in  the standard form, and are used in preference to the dual $\Diamond$ forms because of their interpretation (given below), which is more immediately relevant to the applications.

More formally, we have $P$ or $Prop$, is a set of countably (finite or infitinte) many atomic formulae.  there is also a set $A$, often called the set of 'agents' and taken to be $A = \{1,\ldots,m\}$.  The set of epistemic formluae (= basic $m$-agent epistemic language) will be denoted  $\mathcal{L}^m_K(P)$ is given by the rules

$$\phi ::= p \mid \bot \mid \neg \phi \mid \phi_1 \wedge \phi_2 \mid K_i\phi for i\in A.$$  

We read $K_i \phi$ as ''agent $i$ knows that $\phi$''.

The converse or dual operators, denoted $M_i$ (so that $M_i \phi = \neg K_i\neg \phi$) reads as ''agent $i$ considers $\phi$ is possible''.

####Note####
The 'agent' terminology is extremely useful, but in pure modal logic texts is not used so much.  It does provide an 'intuition' and an interpretation however.

##List of frequently encountered epistemic logics##

* [[The logic K(m)| K(m)]];

* [[The logic S4(m)|S4(m)}]];

* [[The logic S5(m)|S5(m)]].



##Models for epistemic logics##
The geometric or combinatorial semantics of epistemic models follows the same techniques of [[Kripke frames]] as at [[geometric models for modal logics]], whilst the [[algebraic models for modal logics|algebraic models]] are again [[Boolean algebras with operators]].


## References## 


A fairly recent book on epistemic logics and their applications is

* J.- J. Ch. Meyer and W. Van der Hoek, _Epistemic logic for AI and Computer Science_, Cambridge Tracts in Theoretical Computer Science, vol. 41, 1995,

and this has been used for some of the material here.

eneral books on modal logics include

* P. [[Blackburn]], M. de Rijke and Y. [[Venema]], _Modal Logic_, Cambridge Tracts in Theoretical Computer Science, vol. 53, 2001.

* M. Kracht, _Tools and Techniques in Modal Logic,_ Studies in Logic and the Foundation of Mathematics, 142, Elsevier, 1999.

and these have discussions about epistemic logics and their place within the wider framework of modal logic.