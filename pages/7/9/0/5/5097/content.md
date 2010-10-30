
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