## Modal Logics ## 

## Idea## 
The modal logics are the logic of [[relational structures]].  They are built on **modal languages**.
It is usual to classify them using their axiom systems, but also in terms of the type of general interpretation applied to them, such as :

*  [[temporal logics]];

*  [[epistemic logics]];


(this list may get added to later).

Modal logics have semantics given in terms of [[Kripke frames]], which are simply [[relational structures]]. For instance, [[temporal logics]] have [[posets]] as models.

The modal languages add one or more modal operator, often denoted $\square$ or $\diamond$ in to the usual propositional logics.

## Monomodal Logic## 

We will give a simple modal language with one modal operator, $\square$, which can  be applied to propositions of the language to form new propositions:

+--{: .un_defn}
######Definition ######
The basic monomodal language,
 $\mathcal{ML} = \mathcal{ML}(Prop)$, is built up from  a set $Prop$ of atomic propositions by the rule 

$$\phi := p \mid \bot \mid \neg \phi |\phi_1\vee \phi_2\mid \square\phi$$

where $p$ ranges over elements of $Prop$. 
=--
####Gloss####
1. The interpretation of $\square \phi$ depends on the context (to some extent), but in the initial form here it is usually said to mean ' necessarily $\phi$'.

1. Some authors use an equivalent generation rule using $\diamond \phi$ which is $\neg \square \neg \phi$. Of course, this interprets as 'possibly $\phi$'.

1. Another 



## References## 

General books on modal logics include

* P. Blackburn, M. de Rijke and Y. Vedema, _Modal Logic_, Cambridge Tracts in Theoretical Computer Science, vol. 53, 2001.

* M. Kracht, _Tools and Techniques in Modal Logic,_ Studies in Logic and the Foundation of Mathematics, 142, Elsevier, 1999.

and more particularly on epistemic logics and their applications,

* J.- J. Ch. Meyer and W. Van der Hoek, Epistemic logic for AI and Computer Science, Cambridge Tracts in Theoretical Computer Science, vol. 41, 1995. 