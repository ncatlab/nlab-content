


#Contents#
* table of contents
{:toc}

## Modal Logics ## 

## Idea## 
The modal logics are the logic of [[relational structures]].  They are built on **modal languages**.
It is usual to classify them using their axiom systems, but also in terms of the type of general interpretation applied to them, such as :

*  [[temporal logics]];

*  [[epistemic logics]];


(this list may get added to later).

Modal logics have semantics given in terms of [[Kripke frames]], which are simply [[relational structures]]. For instance, [[temporal logics]] have [[posets]] as models.

The modal languages add one or more modal operator, often denoted $\square$ or $\Diamond$ in to the usual propositional logics.

## Multimodal Logics## 

We will give a modal language with $n$ modal operators, $\Diamond_i$, $i = 1,\ldots, n$, which can  be applied to propositions of the language to form new propositions:

+--{: .un_defn}
######Definition ######
We suppose given a set of variables, the $n$-operator basic modal language $\mathcal{L}_\omega(n)$ given by  

$$\phi ::= p_\lambda \mid \bot \mid \neg \phi \mid \phi_1 \vee \phi_2 \mid \Diamond_i\phi,$$  

where the $p_\lambda$ are the propositional variables ordered by finite ordinals, $\lambda$, and, as usual, $\Diamond_i$ is a modality for each  $i=1, \ldots , n$.  

=--
####Gloss####
1. The interpretation of $\Diamond \phi$ depends on the context (to some extent), but in the initial form here it is usually said to mean 'possibly $\phi$'.

1. Some authors use an equivalent generation rule using $\square \phi$, which is $\neg \Diamond \neg \phi$. Of course, this interprets as 'necessarily $\phi$'.

1. Another formulation replaces $\vee$ and $\neg$ by implication $\phi_1\to \phi_2$.

+--{: .un_defn}
######Definition ######
A **logic** in $\mathcal{L}_\omega(n)$ is any set $\Lambda$ of $\mathcal{L}_\omega(n)$-formulae such that   

* $\Lambda$ includes all $\mathcal{L}_\omega(n)$-formulae that are instances of tautologies, 
 
and

* $\Lambda$ is closed under the inference rule 
_if $\phi$, $\phi\to \psi \in \Lambda$ then $\psi \in \Lambda$_ , i.e. detachment or __modus ponens__.

The logic is **uniform** if it is closed under the rule of uniform substitution of $\mathcal{L}_\omega(n)$-formulae for propositional variables and is **normal** if it contains the schemata:
  
(K)  $\Diamond_i(\psi \vee \chi) \to \Diamond_i(\psi)\vee \Diamond_i(\chi)$  
  
(N) $\neg \Diamond_i(\bot)$

and monotonicity (for each $i$):
 
if $\psi \to \chi \in \Lambda$ then $\Diamond_i \psi \to \Diamond_i \chi \in \Lambda$.  
 
=--



## References## 

General books on modal logics include

* P. Blackburn, M. de Rijke and Y. Vedema, _Modal Logic_, Cambridge Tracts in Theoretical Computer Science, vol. 53, 2001.

* M. Kracht, _Tools and Techniques in Modal Logic,_ Studies in Logic and the Foundation of Mathematics, 142, Elsevier, 1999.

and more particularly on epistemic logics and their applications,

* J.- J. Ch. Meyer and W. Van der Hoek, Epistemic logic for AI and Computer Science, Cambridge Tracts in Theoretical Computer Science, vol. 41, 1995. 